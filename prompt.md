# Multimodal UEBA Threat Detection System for Windows AD Environments

## 1. Project Objective

Design an end-to-end **User and Entity Behavior Analytics (UEBA)** system for detecting malicious activity in Windows Active Directory environments by jointly analyzing:

1. **Sysmon process and endpoint telemetry**
2. **Windows Security / Active Directory authentication and security events**
3. **User-specific behavioral baselines**
4. **Temporal and statistical behavioral features**

The system should learn both the **local maliciousness of individual processes** and the **broader behavioral context of the user/session**.

The final objective is to classify a time window or activity sequence as:

> **Benign / Suspicious / Malicious**

while also producing interpretable behavioral risk indicators explaining why the activity was considered anomalous.

---

# 2. High-Level Architecture

```text
                 RAW WINDOWS LOGS
                       │
          ┌────────────┴────────────┐
          │                         │
          ▼                         ▼
     SYSMON LOGS             WINDOWS SECURITY /
                              ACTIVE DIRECTORY LOGS
          │                         │
          ▼                         ▼
   Log Filtering +             Log Filtering +
   Normalization               Normalization
          │                         │
          ▼                         ▼
   Sysmon Tokenizer          Security Log Sequence
          │                         │
          ▼                         ▼
   SecureBERT / MLM              LSTM
          │                         │
          ▼                         ▼
   Sysmon Embedding        Security Embedding
          │                         │
          └───────────┬─────────────┘
                      │
                      ▼
          USER BEHAVIORAL CONTEXT
                      │
          ┌───────────┴────────────┐
          │                        │
          ▼                        ▼
   Per-User Behavioral       Statistical/Risk
        Baseline                  Features
          │                        │
          └───────────┬────────────┘
                      │
                      ▼
               FEATURE FUSION
                      │
                      ▼
              MLP CLASSIFIER
                      │
                      ▼
          Malicious / Benign Score
                      │
                      ▼
          Explainable Risk Output
```

---

# 3. Stage 1 — Raw Log Collection

The system consumes JSONL-formatted Windows telemetry containing two primary data sources.

### A. Sysmon

Relevant Sysmon events may include:

* Process creation
* Network connections
* DNS queries
* Image/DLL loading
* File creation
* Registry activity
* Process access
* Alternate Data Streams
* PowerShell activity
* Parent-child process relationships

The Sysmon stream is primarily responsible for understanding:

> **What processes executed, how they were spawned, what they accessed, and what network/file/registry activity they generated.**

### B. Windows Security / Active Directory Logs

Relevant Security events include:

* Successful logons
* Failed logons
* Logoff events
* Account changes
* Privilege assignments
* Kerberos authentication
* NTLM authentication
* Explicit credential usage
* Special privilege events
* Object/share access
* Remote authentication
* Account-management activity

The Security stream is primarily responsible for understanding:

> **Who authenticated, from where, when, against what resource, and under which security context.**

---

# 4. Stage 2 — Log Preprocessing and Normalization

Before applying machine learning, both log sources are filtered and normalized.

### Processing steps

```text
Raw JSONL
   ↓
Event filtering
   ↓
Field extraction
   ↓
Schema normalization
   ↓
Timestamp normalization
   ↓
User/session normalization
   ↓
IP/domain/process normalization
   ↓
Sequence construction
```

Different Windows event types expose similar information under different field names. Therefore, create a unified internal schema such as:

```text
timestamp
user
domain
host
session_id
logon_id
process_id
parent_process_id
process_name
command_line
source_ip
destination_ip
domain
event_id
event_type
authentication_type
privilege
resource
```

This normalized representation becomes the common foundation for both ML pipelines.

---

# 5. Stage 3 — User, Session, and Process Correlation

A critical part of the architecture is establishing the relationship between:

```text
User
  ↓
Logon Session
  ↓
Process
  ↓
Child Process
  ↓
Network / File / Registry Activity
```

Windows process IDs cannot be treated as globally unique because **PIDs can be recycled**.

Therefore, process identity should incorporate temporal information and process creation context, for example:

```text
Process Identity =
    Host
    + PID
    + Process Creation Time
```

Similarly, Security events should be correlated through identifiers such as:

* Logon ID
* Session ID
* User
* Host
* Timestamp

This allows the system to answer:

> "Which user/session ultimately caused this process and its associated activity?"

This is especially important for service accounts and `SYSTEM` processes.

---

# 6. Stage 4 — Sysmon Behavioral Model

The first ML branch focuses specifically on Sysmon telemetry.

## Input

A chronological sequence of Sysmon events:

```text
Process Creation
      ↓
Network Connection
      ↓
DNS Query
      ↓
Process Access
      ↓
File Creation
      ↓
Registry Modification
      ↓
Child Process
```

## Tokenization

Develop a custom tokenizer that converts structured Sysmon events into behavioral tokens.

For example:

```text
WINWORD.EXE
    ↓
POWERSHELL.EXE
    ↓
ENCODED_COMMAND
    ↓
DNS_QUERY
    ↓
EXTERNAL_IP
    ↓
LSASS_ACCESS
```

The tokenizer should preserve important semantic information rather than treating the log as ordinary natural language.

Potential token categories:

```text
PROCESS
PARENT_PROCESS
COMMAND
NETWORK
DNS
FILE
REGISTRY
USER
PRIVILEGE
ACCESS
LOLBIN
TECHNIQUE
```

---

# 7. Stage 5 — Sysmon SecureBERT / MLM Representation

Use a masked-language-modeling approach to learn contextual representations of Sysmon event sequences.

The model learns relationships such as:

```text
WINWORD → POWERSHELL → ENCODED_COMMAND
```

or:

```text
POWERSHELL → DNS → EXTERNAL_IP → LSASS
```

rather than evaluating each event independently.

The output is a fixed-dimensional:

```text
Sysmon Embedding
```

representing the contextual behavior of the process/activity sequence.

The Sysmon branch can additionally have a classification head that learns:

```text
Sysmon Sequence
       ↓
SecureBERT
       ↓
Sysmon Embedding
       ↓
Process-Level Classifier
       ↓
Malicious / Benign
```

The learned embedding is then passed to the multimodal fusion stage.

---

# 8. Stage 6 — Windows Security / AD Behavioral Model

The second branch focuses on authentication and identity behavior.

Security events should be ordered chronologically and grouped into meaningful sequences.

Example:

```text
4624 — Interactive Logon
      ↓
4768 — Kerberos Authentication
      ↓
4769 — Service Ticket
      ↓
4672 — Special Privileges
      ↓
5140 — Network Share Access
      ↓
4624 — Remote Logon
```

These sequences provide information about:

* Authentication behavior
* Lateral movement
* Privilege escalation
* Account usage
* Remote access
* Resource access
* Abnormal login patterns

---

# 9. Stage 7 — LSTM Security-Log Encoder

The normalized Security/AD event sequence is passed through an LSTM.

```text
Security Events
      ↓
Event Embeddings
      ↓
LSTM
      ↓
Hidden State
      ↓
Security Embedding
```

The LSTM captures temporal dependencies such as:

```text
Failed Logons
      ↓
Successful Remote Logon
      ↓
Privilege Assignment
      ↓
Sensitive Resource Access
```

The resulting hidden representation becomes the:

> **Security/AD Embedding**

This embedding represents the temporal identity and authentication behavior of the user/session.

---

# 10. Stage 8 — User Behavioral Baseline

Alongside the learned representations, construct a statistical behavioral model for each user.

Create behavioral windows such as:

```text
User A
   ├── 10:00–10:10
   ├── 10:10–10:20
   ├── 10:20–10:30
   └── ...
```

For every user and time window, calculate behavioral features.

The existing implementation contains approximately **69 security-oriented features**, including:

### Process behavior

* Process count
* Unique processes
* Process depth
* Suspicious parent-child relationships
* LOLBin usage
* PowerShell usage
* Encoded PowerShell
* Office → PowerShell chains

### Network behavior

* Unique destination IPs
* Unique domains
* External connections
* Rare destinations
* DNS request counts
* DNS entropy
* DGA-like domain behavior

### Security behavior

* LSASS access
* Privileged activity
* Authentication anomalies
* Sensitive share access
* Remote access
* Registry persistence
* Credential-related activity

### Behavioral novelty

* First-seen process
* First-seen domain
* First-seen IP
* First-seen process relationship
* First-seen command pattern

---

# 11. Stage 9 — Per-User Behavioral Baseline

Instead of creating a global definition of normal behavior, create a baseline for each individual user.

Conceptually:

```text
User
   +
Hour of Day
   +
Historical Behavior
   ↓
User-Specific Baseline
```

For each feature, estimate normal behavior using:

```text
Median
MAD (Median Absolute Deviation)
```

rather than relying only on mean and standard deviation.

This is appropriate because security telemetry is highly sparse, heavy-tailed, and contains many binary/rare events.

For example:

```text
User: Alice
Hour: 10 AM

Normal LSASS access:
    Median = 0
    MAD    = 0

Current window:
    LSASS access = 1
```

This should produce a very strong behavioral novelty signal.

---

# 12. Stage 10 — Behavioral Risk Engine

The baseline produces explicit behavioral risk features.

Instead of relying only on a traditional z-score, calculate a composite risk representation combining:

```text
Rarity
   +
Magnitude
   +
Severity
```

Conceptually:

```text
Behavioral Risk
=
f(
    Statistical Rarity,
    Deviation Magnitude,
    Security Severity
)
```

For example:

```text
Encoded PowerShell
       +
Rare External IP
       +
LSASS Access
       +
Novel Process Chain
       ↓
High Behavioral Risk
```

This branch provides an explicit representation of:

> **"How abnormal is this activity for this particular user?"**

---

# 13. Stage 11 — Multimodal Feature Fusion

At this point there are three complementary representations:

```text
                 ┌─────────────────────┐
                 │ Sysmon SecureBERT    │
                 │ Embedding            │
                 └──────────┬──────────┘
                            │
                            │
                 ┌──────────▼──────────┐
                 │ Security LSTM       │
                 │ Embedding            │
                 └──────────┬──────────┘
                            │
                            │
                 ┌──────────▼──────────┐
                 │ Behavioral Baseline │
                 │ / Risk Features      │
                 └──────────┬──────────┘
                            │
                            ▼
                    FEATURE FUSION
```

Concatenate or otherwise fuse:

```text
Fused Feature =
[
    Sysmon Embedding,
    Security Embedding,
    Behavioral Risk Features
]
```

This creates a multimodal representation containing:

* **Process-level context**
* **Identity/authentication context**
* **User-specific behavioral context**

---

# 14. Stage 12 — MLP Fusion Classifier

The fused representation is passed into an MLP.

```text
Fused Representation
        ↓
Dense Layer
        ↓
Activation
        ↓
Dropout
        ↓
Dense Layer
        ↓
Activation
        ↓
Output Layer
        ↓
Malicious Probability
```

The classifier should produce something such as:

```text
P(Benign)
P(Malicious)
```

or, for a multiclass formulation:

```text
P(Benign)
P(Suspicious)
P(Malicious)
```

The MLP therefore learns relationships that may not be visible from any individual stream.

For example:

```text
Normal PowerShell
+
Normal User Login
+
Normal Destination
=
Likely Benign
```

while:

```text
Office → Encoded PowerShell
+
New User/Session Behavior
+
LSASS Access
+
DGA Domain
+
External C2 IP
=
High Malicious Probability
```

---

# 15. Complete Model Architecture

The final architecture can be represented as:

```text
                         WINDOWS TELEMETRY
                               │
             ┌─────────────────┴─────────────────┐
             │                                   │
             ▼                                   ▼
        SYSMON LOGS                      SECURITY / AD LOGS
             │                                   │
             ▼                                   ▼
     Preprocessing +                    Preprocessing +
       Tokenization                       Sequencing
             │                                   │
             ▼                                   ▼
      SecureBERT / MLM                         LSTM
             │                                   │
             ▼                                   ▼
      SYSMON EMBEDDING                  SECURITY EMBEDDING
             │                                   │
             │                                   │
             └─────────────────┬─────────────────┘
                               │
                               ▼
                     USER BEHAVIOR WINDOW
                               │
                    ┌──────────┴──────────┐
                    │                     │
                    ▼                     ▼
              69 Behavioral        User Baseline
                 Features          Median + MAD
                    │                     │
                    └──────────┬──────────┘
                               ▼
                     BEHAVIORAL RISK SCORE
                               │
                               ▼
                    ┌────────────────────┐
                    │   FEATURE FUSION   │
                    │                    │
                    │ Sysmon Embedding   │
                    │ Security Embedding │
                    │ Behavioral Risk    │
                    └─────────┬──────────┘
                              │
                              ▼
                         MLP CLASSIFIER
                              │
                              ▼
                  MALICIOUS PROBABILITY
                              │
                              ▼
                    BENIGN / MALICIOUS
```

---

# 16. Why This Architecture Is Different From a Simple Classifier

The key idea is that the system does not rely on only one definition of maliciousness.

It combines three perspectives:

### 1. Process-level intelligence

**Sysmon + SecureBERT**

> "Does this process/event sequence look like malicious behavior?"

### 2. Identity-level intelligence

**Security/AD + LSTM**

> "Does this authentication and security-event sequence look abnormal?"

### 3. User-level intelligence

**Behavioral baseline**

> "Is this behavior unusual for this particular user at this particular time?"

The MLP combines all three.

Therefore:

```text
Maliciousness
=
Process Context
+
Identity Context
+
User Behavioral Context
```

---

# 17. Example Attack Flow

Consider a simulated attack:

```text
User opens malicious Word document
              ↓
WINWORD.EXE
              ↓
POWERSHELL.EXE
              ↓
Encoded PowerShell command
              ↓
DNS request to DGA-like domain
              ↓
Connection to external C2 IP
              ↓
LSASS access
              ↓
Credential-related activity
```

### Sysmon branch

SecureBERT identifies the suspicious process/event relationship:

```text
Office
  →
PowerShell
  →
Encoded Command
  →
DNS
  →
C2
  →
LSASS
```

producing a high-risk Sysmon representation.

### Security branch

The LSTM observes the associated authentication/session behavior and produces a Security/AD embedding.

### Behavioral branch

The user's baseline identifies:

```text
Encoded PowerShell = Rare
C2 IP = Novel
DGA Domain = Novel
LSASS Access = Never Seen
Process Chain = Novel
```

producing a high behavioral risk score.

### Fusion

```text
High Sysmon Risk
       +
Abnormal Security Sequence
       +
High User Behavioral Risk
       ↓
       MLP
       ↓
High Malicious Probability
```

---

# 18. Training Strategy

The system should ideally be trained in stages.

### Stage A — Sysmon representation learning

Train/fine-tune SecureBERT using Sysmon sequences with MLM or related self-supervised objectives.

Then train the Sysmon classification head using labeled malicious/benign activity.

### Stage B — Security-log representation learning

Train the LSTM on chronological Security/AD sequences.

The resulting hidden representation becomes the Security embedding.

### Stage C — Behavioral baseline

Build the baseline using historical benign activity.

Calculate:

```text
Median
MAD
Rarity
Novelty
Severity
Behavioral Risk
```

### Stage D — Multimodal fusion

Combine:

```text
Sysmon Embedding
+
Security Embedding
+
Behavioral Features
```

and train the MLP classifier.

For imbalanced malware datasets, use an appropriate imbalance strategy such as **Focal Loss**, class weighting, or carefully controlled sampling.

Use **Early Stopping** based on validation performance to prevent overfitting.

---

# 19. Evaluation

Do not rely only on accuracy because malicious events will typically be much rarer than benign events.

Evaluate using:

* Precision
* Recall
* F1-score
* PR-AUC
* ROC-AUC
* False-positive rate
* False-negative rate
* Detection rate at a fixed false-positive rate

Also compare the architecture through ablation experiments:

```text
Model 1:
Sysmon only

Model 2:
Security/AD only

Model 3:
Sysmon + Security

Model 4:
Sysmon + Behavioral Baseline

Model 5:
Security + Behavioral Baseline

Model 6:
Sysmon + Security + Behavioral Baseline
```

This demonstrates whether each component actually contributes to detection performance.

---

# 20. Final Research Hypothesis

The central hypothesis of the project is:

> **A UEBA system that jointly models process-level telemetry, authentication/security-event sequences, and user-specific behavioral baselines will detect malicious Windows activity more accurately and with fewer false positives than a model based on any single telemetry source or global anomaly threshold.**

The architecture therefore combines:

```text
Deep Representation Learning
            +
Temporal Modeling
            +
Statistical User Profiling
            +
Explicit Security Indicators
            +
Multimodal Feature Fusion
            ↓
       UEBA Detector
```

The final system is not merely a **Sysmon malware classifier**. It is a **user-context-aware multimodal Windows threat-detection architecture** in which Sysmon explains *what happened at the endpoint*, Security/AD logs explain *who/which session was involved*, and the behavioral baseline explains *whether that activity is normal for that particular user*.
