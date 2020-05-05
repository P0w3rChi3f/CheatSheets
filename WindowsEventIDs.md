# Windows Events  

## Windows EventIDs  

| EventID | Description |  
| --- | --- |  
| 104  | Audit log cleared **(System log)** |  
| 106/4698 |scheduled task created (task scheduler  security log) |
| 140/4702 | scheduled task updated (task scheduler | security log) |  
| 141/4699 | scheduled task deleted ( task scheduler | security log) |
| 200/201 | scheduled task executed/ completed (task scheduler log) (code 0 means succeeded) |  
| 1102 | Audit log cleared |  
| 4104 | Script Contents |  
| 4105/6 | Script start/stop |  
| 4700/4701 | scheduled task enabled/disabled **(security log)** |  
| 4624 | Successful login |  
| 4625 | Failed login |  
| 4634/4647 | Successful logoff |  
| 4648 | Login using explicit credentials (runas/share mounted?) Logged on source |  
| 4688 | New Process Created **(Security)** PS? |  
| 4672 | Account login with superuser rights (Admin) |  
| 4674 | Specified user exercised specified right |  
| 4720 | An account was created |  
| 4722 | User account enabled |  
| 4724 | Attempt to reset an account password |  
| 4728 | member added to security-enabled global group |  
| 4732 | member added to a security enabled local group |  
| 4735 | security enabled local group changed |  
| 4738 | A user account was changed |  
| 4756 | A member was added to a security-enabled universal group |  
| 4768 | TGT was granted (successful logon) Acct Logon |  
| 4769 | TGT requested (access to server) Acct Logon |  
| 4771 | Pre-authentication failed (failed logon) Acct Logon |  
| 4776 | successful/ failed account authentication (NTLM) Acct Logon |  
| 4778 | RDP (or fast user switching) Session Connected/Reconnected |  
| 4779 | RDP (or fast user switching)Session Disconnected |  
| 131/1149 | record remote ip, user, and date/time of successful connection |  
| 119 | tasks are triggered by account logons |  
| 98 | successful TCP connection |  
| 5140 | network share was accessed Share |  
| 5142 | share created Share |  
| 5143 | share modified  Share |  
| 5144 | share deleted Share |  
| 5145 | shared object accessed Share |  
| 7034 | Service crashed unexpectedly Sys (process injection?) |  
| 7035 | Service sent a Start/Stop control Sys |  
| 7036 | Services started or stopped (Psexecsvc will start this)  Sys |  
| 7040 | Start type changed (Boot|On Request|Disabled) Sys |  
| 7045 | A service was installed on the system (Win2kr2)  Sys |  
| 4697 | A service was installed on the system (from security log) |  

---

## Windows Logon Type Codes (Goes with eventID 4624)  

|Type Code | Description|  
|--- | --- |  
| 2 | Logon via console (keyboard/terminal) |  
| 3 | Network Logon |  
| 4 | Batch Logon (used by Scheduled Tasks |  
| 5 | Windows Service Logon |  
| 7 | Credentials used to lock or unlock screen |  
| 8 | Network logon sending credentials in cleartext |  
| 9 | Different Credentials than logged on user (runas) |  
| 10 | Remote interactive logon (RDP) |  
| 11 | Cached Credentials used to logon- offline from DC |  
| 12 | Cached remote Interactive (Similar to 10) |  
| 13 | Cached unlock (Similar to 07) |  

---  

## 4771 Failed Pre-Authentication Events  

| Failed Description Code | 4771 Failed Pre-Authentication Events|  
|--- | --- |  
| 0xC0000064 | ox6 Invalid username |  
| 0xC000006A | ox7 requested server not found |  
| 0xC000006F | oxC Policy restriction prohibited logon (day/time rest) |  
| 0xC0000070 | ox12 Account locked, disabled, expired |  
| 0xC0000071 | ox17 Password expired |  
| 0xC0000072 | ox18 Password invalid  |  
| 0xC00000193 | ox25 Clock skew between machines is too great  |  

---

## Application Installation  

 | EventID | Description |  
 | --- | --- |  
 | 1033 | Installation completed (with success/failure status) |  
 | 1034 | Application removal completed (with success/failure status) |  
 | 11707 | Installation completed successfully |  
 | 11708 | Installation operation failed |  
 | 11724 | Application removal completed successfully |  
 | 1001 | Windows Error reporting (BSOD?) |  
 | 1000/1002 | Application error/hang |  

---

## Event Log Summary  

 | Event Type | Event Log Type | EventIDs |  
 | --- | --- | --- |  
 | Logons | Security | 4624, 4625, 4634, 4647, 4672, 4720, 4648 |  
 | Account Logon | Security | 4768, 4769, 4771, 4776 |  
 | RDP | Security, RDPCoreTS, TerminalServices-Remote | 4624, 4625, 4778, 4779, 131, 1149 |  
 | Network Shares | Security | 5140, 5141, 5142, 5143, 5144, 5145 |  
 | Scheduled Tasks | Security | Task Scheduler | 4698, 106, 141, 200 |  
 | Installation | Application | 1033, 1034, 11707, 11708, 11724 |  
 | Malware Execution | Security, System, Application | 4668, 1001, 1000, 1001, 1002 |  
 |Services | System, Security | 7034, 7035, 7036, 7040, 7045, 4697 |  
 | Command Lines | Security, Application/PowerShell | 4688, 4104, 4105, 4106 |  
 | Log Clearing | Security, System | 1102, 104 |  
