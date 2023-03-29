# KQL : XDR Custom Detection Rule with NRT
WIP

## KQL : Hunting queries
```kql
DeviceEvents
| where Timestamp > ago(5m)
| where ActionType startswith "asr" and ActionType endswith "audited"
| project Timestamp, ReportId, DeviceId, DeviceName, FileName, FolderPath
```
```kql
DeviceEvents
| where Timestamp > ago(5m)
| where ActionType startswith "asr" and ActionType endswith "blocked"
| project Timestamp, ReportId, DeviceId, DeviceName, FileName, FolderPath
```
## Config : Custom Detection Rule NRT
To configure a custom detection rule in the Microsoft 365 Defender portal, select [Continuous (NRT)](https://learn.microsoft.com/en-us/microsoft-365/security/defender/custom-detection-rules?view=o365-worldwide) to try NRT.

![image](https://user-images.githubusercontent.com/120234772/228133466-69fb1e17-c5f2-4130-ba27-3562ce119c40.png)

![image](https://user-images.githubusercontent.com/120234772/228149676-e2ac0076-f004-46af-8d6b-7845f6d46830.png)

## Alerts : Custom Detection Rule NRT
![image](https://user-images.githubusercontent.com/120234772/228417447-f40b108e-8658-4b4c-b186-5cd20164d99a.png)


#### Disclaimer
The views and opinions expressed herein are those of the author and do not necessarily reflect the views of company.