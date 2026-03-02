---
title: "Version 4.0 Oct. 4, 2024"
---
# Version 4.0 (AppSource Version 1004)
BI for Defender Version 4.0, shown as version 1004 in AppSource, was released on October 4, 2024. Version 4 includes many requested improvements.

**Important Notes:**

- New permissions are required on the [App Registration](azure-ad-app-permissions.md) in Azure. Reports will be blank if these are not added.Directory.Read.All
Several customers have recently reported upgrade failures resulting in the loss of their custom reports. Please do not forget to [backup before you upgrade](create-backup-workspace.md)!


## Below Are The Changes in Version 4.0


- **Features:**New parameter, "AzureAD Advanced Hunting Day(s)" added to semantic model.Default and max value is 30 days.
- Some of the new entities/fields are collected by use of Advanced Hunting. This parameter defines the numbers of days since a device was last active to get the data.
New entity "Alert Evidence" added to the semantic model. New fields include:
- Created Date
- Created Date (Days)
- Detection Status
- Evidence Instance Name
- Evidence IP Address
- Evidence Type
- Evidence File Name
- Evidence File Publisher
- Evidence File Size
- Evidence Folder Path
- Remediation Status
- Remediation Status Details
- Verdict
New entity "Device Tag" added to the semantic model. New fields include:
- Tag
- Tag Type
New entity "User" added to the Semantic Model. New fields include:
- User Countv
- User ID
- User Name
- User Source
- Logon User
New entity "User Devices" added to the Semantic Model. New fields include:
- Logon User
**Enhancements:**
- New fields added to the "Alert Object" entity in the semantic model:Alert ID
- Alert Impacted Device
- Alert Impacted File
- Alert Impacted Folder
- Alert Impacted Instance
- Alert Impacted Type
- Alert Impacted User
New fields added to the "Incident" entity in the semantic model:
- Assigned To
New fields added to the "Device" entity in the semantic model:
- Agent Version
- Device Category
- Device Info Time
- Device Info Time (Days)
- Device Manufacturer
- Device Model
- Device Tag
- Device Type
- Logon User
- OS Architecture
**Bug Fixes:**
- Resolved an issue preventing alerts from showing up on the "Incidents & Alerts" page.
**Important Notes:**
- New permissions are required on the App Registration in Azure. Reports will be blank if these are not added.Directory.Read.All
Always backup your custom reports using our [backup process.](create-backup-workspace.md)
