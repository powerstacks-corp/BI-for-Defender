---
title: "Release Notes"
---

# BI for Defender Release Notes

## Version 15.0 February 26, 2026

# What's New in BI for Defender v15
**Release Date**: February 26, 2026
**App Source Version**: 1015

BI for Defender v15 expands visibility into software artifacts and improves Secure Score navigation.

This release introduces new objects for software file paths and registry paths, enhancing investigative reporting capabilities.

It also improves performance by optimizing vulnerability-related measures and adding direct links to remediation controls and recommendations.


## Version 15.0 Release Details


### Product Enhancements

- Updated the **Secure Score** page to include direct links to control details from the Control Name field.
- Updated the **Missing Security Updates** page to include a direct link to the **Recommendation Name** for easier remediation access.
- Optimized performance of vulnerability-related measures within the **Device** object.

### New Features

- Added new object **Software Devices File Path** to provide visibility into associated file paths.
- Added new object **Software Devices Registry Path** to provide visibility into associated registry paths.

### Semantic Model Changes

- Added new fields to the **Software Devices File Path** object: File Path, File Path Count.
- Added new fields to the **Software Devices Registry Path** object: Registry Path, Registry Path Count.
- Added **Control Link** field to the **Secure Score Control** object.
- Added **Recommendation Link** field to the **Vulnerability Recommendation** object.
- Removed measures Missing Security Updates Average, Vulnerabilities Detected Average, and Vulnerabilities Exploitable Average from the **Device** object due to performance considerations.
- Optimized measures Missing Security Updates Count, Vulnerabilities Detected Count, and Vulnerabilities Exploitable Count within the **Device** object for improved sync performance.

### Important Notes

- Always [backup your custom reports](/bi-for-intune/guides/backup-custom-reports.md) before upgrading!

---

## Version 14.0 Jan. 23, 2026

# What's New in BI for Defender v14
**Release Date**: January 23, 2026
**App Source Version**: 1014

BI for Defender v14 expands device tagging capabilities and enhances vulnerability reporting.

This release introduces support for System device tags and updates tagging behavior for inactive devices. It also refines vulnerability reporting by consolidating fields into the Device object for improved clarity and consistency.

These changes improve reporting accuracy and visibility into device security posture.

**Important Notes:**
As always—before upgrading, [back up your custom reports](create-backup-workspace.md) to prevent data loss.


## Version 14.0 Release Details


### Product Enhancements

- Added support for **System** device tags within the **Device Tag**
- Updated tagging behavior so that manual tags on inactive devices may appear as **System**

### Semantic Model Changes

- Removed the **Vulnerabilities** field from the **Software Vulnerabilities** This field has been replaced by **Vulnerabilities Detected** in the **Device** object.
- Added new fields to the **Device** object: Missing Security Updates, Missing Security Updates Average, Missing Security Updates Count, Vulnerabilities Detected, Vulnerabilities Detected Average, Vulnerabilities Detected Count, Vulnerabilities Exploitable, Vulnerabilities Exploitable Average, Vulnerabilities Exploitable Count.

### Important Notes

- Always [backup your custom reports](/bi-for-intune/guides/backup-custom-reports.md) before upgrading!

---

## Version 13.0 Nov. 24, 2025

# What's New in BI for Defender v13
**Release Date**: November 25, 2025
**App Source Version**: 1013

Version 13 is a small maintenance release to fix some minor bugs that affected a limited number of customers.

**Important Notes:**
As always—before upgrading, [back up your custom reports](create-backup-workspace.md) to prevent data loss.


## Version 13.0 Release Details


### Product Enhancements

- N/A

### New Features

- N/A

### Bug Fixes

- On the "**Missing Security Update**s" page some missing vulnerabilities have no linked devices. This has been resolved in version 13.

### Semantic Model Changes

- N/A

### Important Notes

- Always [backup your custom reports](/bi-for-intune/guides/backup-custom-reports.md) before upgrading!

---

## Version 12.0 Oct. 12, 2025

# What's New in BI for Defender v12
**Release Date**: October 12, 2025
**App Source Version**: 1012

BI for Defender v12 improves Cloud App reporting reliability and introduces enhanced filtering capabilities.

This release adds new tag-based parameters to control which Cloud Apps are loaded during sync, reducing timeout issues in large environments.

It also enhances the Cloud App object with additional activity metrics and renames key download and upload fields for clarity. Please review breaking changes if you reference Cloud App data in custom reports.


## Version 12.0 Release Details


### Product Enhancements

- Improved Cloud App sync reliability by introducing tag-based filtering to control which Cloud Apps are loaded during sync.
- Added new fields to the **Cloud App** page: **Cloud App Device Count**, **Cloud App IP Address Count**, and **Cloud App Transaction Count** to improve visibility into Cloud App activity metrics.

### New Features

- Added new parameter **AzureAD Cloud App Tags Only** to the semantic model (Default: True). When enabled, only Cloud Apps with matching tags defined in **AzureAD Cloud App Tags** will be loaded during sync.
- Added new parameter **AzureAD Cloud App Tags** to the semantic model. This parameter allows administrators to specify a comma-separated list of Cloud App tags to include during sync.

### Bug Fixes

- Resolved an issue causing Cloud App sync timeouts in certain environments.
- Resolved an issue where **Device Type** was blank on the **Cloud App** page in v11.

### Semantic Model Changes

- Added new fields to the **Cloud App** object: Cloud App Device Count, Cloud App IP Address Count, Cloud App Transaction Count.
- Renamed **Download (MB)** to **Cloud App Download (MB)** on the **Cloud App** See the Important Notes section.
- Renamed **Upload (MB)** to **Cloud App Upload (MB)** on the **Cloud App** See the Important Notes section.

### Important Notes

- Renamed **Download (MB)** to **Cloud App Download (MB)** on the **Cloud App** This is a breaking change. Custom reports referencing the previous field name must be updated.
- Renamed **Upload (MB)** to **Cloud App Upload (MB)** on the **Cloud App** This is a breaking change. Custom reports referencing the previous field name must be updated.
- Always [backup your custom reports](/bi-for-intune/guides/backup-custom-reports.md) before upgrading!

---

## Version 11.0 Oct. 3, 2025

# What's New in BI for Defender v11
**Release Date**: October 3, 2025
**App Source Version**: 1011

Version 11 is a very big update. We've added several new report pages and many new data fields.

**Important Notes:**
[**Action Required!**] This version requires and additional permission to be added to the app registration in Entra ID. Without this new permission the sync will fail! Please add **CloudApp-Discovery.Read.All**to your [app registration](create-azure-ad-app-registration.md). And as always—before upgrading, [back up your custom reports](create-backup-workspace.md) to prevent data loss.


## Version 11.0 Release Details


## Product enhancements

- Changed how we determine the number of clients for licensing purposes. We now only count “**Active**”, “**Onboarded**” devices that are not “**Excluded**” in Microsoft Defender.

## New features

- Added new “**User Info**” page.
- Added new “**Cloud App**” page.
- Added new “**Antivirus**” page.
- Updated the “**Incident & Alerts**” page to include an “**IP Address**” visual.

## Bug fixes

- N/A

## Semantic model changes

- Added new parameter “**AzureAD Alert Enable**” (Default: **TRUE**).
- Added new parameter “**AzureAD Cloud App Day(s)**” (Possible values: **7**, **30**, **90** days; **-1** = Disabled).
- Removed “**IP Address**” from the “**Device Network**” object.
- Updated the “**Last Logon User**” object → Added Local Sign-In User as part of the “**User**” object.
- Updated the “**Alert Evidence**” object → Added Local Sign-In User as part of the “**User**” object and added “**IP Address**” as part of the “**IP Address**” object.
- Updated the “**Device**” object → Added “**IP Address**” as part of the “**IP Address**” object.
- Updated the “**Software Vulnerabilities**” object. New fields include:“**Missing Security Update ID**”
- “**Missing Security Update URL**”.
Updated the “**IP Address**” object. New fields include:
- “**IP Address**”
- “**IP Address Count**”
Updated the “**Software Vulnerabilities**” object. New fields include:
- “**Last Update**”
- “**Last Update (Days)**”
Updated the “**Secure Configuration**” object. New fields include:
- “**Last Update**”
- “**Last Update (Days)**”
Updated the “**User**” object. New fields include:
- “**Account Enabled**”
- “**Azure AD**”
- “**City**”
- “**Company**”
- “**Country**”
- “**Department**”
- “**Directory Distinguished Name**”
- “**Directory Last Sync**”
- “**Directory Last Sync (Days)**”
- “**Directory Synced**”
- “**Directory User Name**”
- “**Email Address**”
- “**Employee ID**”
- “**Attribute 1**”
- “**Attribute 2**”
- “**Attribute 3**”
- “**Attribute 4**”
- “**Attribute 5**”
- “**Attribute 6**”
- “**Attribute 7**”
- “**Attribute 8**”
- “**Attribute 9**”
- “**Attribute 10**”
- “**Attribute 11**”
- “**Attribute 12**”
- “**Attribute 13**”
- “**Attribute 14**”
- “**Attribute 15**”
- “**First Name**”
- “**Full Name**”
- “**Last Name**”
- “**Mobile Phone**”
- “**Office**”
- “**Password Last Change**”
- “**Password Last Change (Days)**”
- “**Place**”
- “**Postal Code**”
- “**State**”
- “**Street Address**”
- “**Title**”
- “**User Type**”
Updated the “**User Manager**” object. New fields include:
- “**Manager Company**”
- “**Manager Department**”
- “**Manager Email Address**”
- “**Manager Employee ID**”
- “**Manager First Name**”
- “**Manager Full Name**”
- “**Manager Last Name**”
- “**Manager Mobile Phone**”
- “**Manager Title**”
Updated the “**User Proxy Addresses**” object. New fields include:
- “**Proxy Address**”
Updated the “**Authorization**” object. New fields include:
- “**Viewer Email**”
Updated the “**Cloud App**” object. New fields include:
- “**Category**”
- “**Cloud App Count**”
- “**Cloud App Name**”
- “**Cloud App Tag**”
- “**Download (MB)**”
- “**Last Seen**”
- “**Last Seen (Days)**”
- “**Risk Score**”
- “**Upload (MB)**”
Updated the “**Cloud App Data Type**” object. New fields include:
- “**Data Type**”
Updated the “**Cloud App Details**” object. New fields include:
- “**Cloud App Data Type**”
- “**Cloud App Logon URL**”
- “**CSA STAR Level**”
- “**Data Center**”
- “**Data Retention Policy**”
- “**Domain Registration**”
- “**Domain Registration (Days)**”
- “**Encryption Protocol**”
- “**FedRAMP Level**”
- “**Founded**”
- “**GDPR Readiness Statement**”
- “**Headquarters**”
- “**Holding**”
- “**Holding Company**”
- “**Is Admin Audit Trail**”
- “**Is COBIT Compliant**”
- “**Is COPPA Compliant**”
- “**Is Data Audit Trail**”
- “**Is Data Classification**”
- “**Is Data Ownership**”
- “**Is Disaster Recovery Plan**”
- “**Is DMCA**”
- “**Is FERPA Compliant**”
- “**Is FFIEC Compliant**”
- “**Is File Sharing**”
- “**Is FINRA Compliant**”
- “**Is FISMA Compliant**”
- “**Is GAAP Compliant**”
- “**Is GDPR Data Protection Impact Assessment**”
- “**Is GDPR Data Protection Officer**”
- “**Is GDPR Secure Cross Border Data Transfer**”
- “**Is GDPR Lawful Basis For Processing**”
- “**Is GDPR Report Data Breaches**”
- “**Is GDPR Right To Access**”
- “**Is GDPR Right To Be Informed**”
- “**Is GDPR Right To Data Portability**”
- “**Is GDPR Right To Erasure**”
- “**Is GDPR Right To Object**”
- “**Is GDPR Right To Rectification**”
- “**Is GDPR Right To Restriction Of Processing**”
- “**Is GDPR Rights Related To Automated Decision Making**”
- “**Is GLBA Compliant**”
- “**Is HIPAA Compliant**”
- “**Is HITRUST CSF Compliant**”
- “**Is HTTP Security Headers Content Security Policy**”
- “**Is HTTP Security Headers Strict Transport Security**”
- “**Is HTTP Security Headers X-Content-Type-Options**”
- “**Is HTTP Security Headers X-Frame-Options**”
- “**Is HTTP Security Headers X-XSS-Protection**”
- “**Is IP Address Restriction**”
- “**Is ISAE 3402 Compliant**”
- “**Is ISO 27001 Compliant**”
- “**Is ISO 27017 Compliant**”
- “**Is ISO 27018 Compliant**”
- “**Is ITAR Compliant**”
- “**Is Multi-Factor Authentication**”
- “**Is Password Policy Change Password Period**”
- “**Is Password Policy Character Combination**”
- “**Is Password Policy Password History And Reuse**”
- “**Is Password Policy Length Limit**”
- “**Is Password Personal Information Use**”
- “**Is Penetration Testing**”
- “**Is Privacy Shield Compliant**”
- “**Is Remember Password**”
- “**Is Requires User Authentication**”
- “**Is SOC 1 Compliant**”
- “**Is SOC 2 Compliant**”
- “**Is SOC 3 Compliant**”
- “**Is SOX Compliant**”
- “**Is SP 800-53 Compliant**”
- “**Is SSAE 16 Compliant**”
- “**Is Supports SAML**”
- “**Is Trusted Certificate**”
- “**Is User Audit Trail**”
- “**Is User Can Upload Data**”
- “**Is User Roles Support**”
- “**Is Valid Certificate Name**”
- “**Latest Breach**”
- “**Latest Breach (Days)**”
- “**PCI DSS Version**”
- “**Vendor**”
Updated the “**Cloud App Logon URL**” object. New fields include:
- “**Logon URL**”
Updated the “**Cloud App Tag**” object. New fields include:
- “**Tag**”
Updated the “**Device AntiVirus**” object. New fields include:
- “**AntiVirus Active**”
- “**AntiVirus Active Rate (%)**”
- “**AntiVirus Disabled**”
- “**AntiVirus EDR Blocked**”
- “**AntiVirus Mode**”
- “**AntiVirus Other**”
- “**AntiVirus Passive**”
- “**AntiVirus Passive Audit**”
- “**Engine Update**”
- “**Engine Update (Days)**”
- “**Engine Version**”
- “**Full Scan**”
- “**Full Scan (Days)**”
- “**Is Engine Up-To-Date**”
- “**Is Platform Up-To-Date**”
- “**Is Signature Up-To-Date**”
- “**Last Update**”
- “**Last Update (Days)**”
- “**Platform Update**”
- “**Platform Update (Days)**”
- “**Platform Version**”
- “**Quick Scan**”
- “**Quick Scan (Days)**”
- “**Quick Scan Error Code**”
- “**Quick Scan Status**”
- “**Signature Published On**”
- “**Signature Published On (Days)**”
- “**Signature Update**”
- “**Signature Update (Days)**”
- “**Signature Version**”

## Important notes

- Always [backup your custom reports](/bi-for-intune/guides/backup-custom-reports.md) before upgrading!
- **ATTENTION**: Add permission “**CloudApp-Discovery.Read.All**” – **without it, the sync will fail.**


## New Cloud App Page
![](images/Cloud_App_Page-1024x613.png)

## New Antivirus Page
![](images/Antivirus_page-1024x604.png)

## New User Info Page
![](images/User_Info_Page-1024x604.png)

---

## Version 10.0 June 15, 2025

# What's New in BI for Defender v10
**Release Date**: June 15, 2025
**App Source Version**: 1010

Version 10 is a small maintenace release to fix some minor bugs that affected a limited number of customers and to add minor new feature requested by a customer.

**Important Notes:**
If you missed version 8.0, please [review the critical change](http://ec2-35-94-201-107.us-west-2.compute.amazonaws.com/wordpress/bi-for-defender-change-log/version-8-0-march-10-2025/) related to vulnerabilities and security update filtering.  And as always—before upgrading, [back up your custom reports](create-backup-workspace.md) to prevent data loss.


## Version 10.0 Release Details


### Product Enhancements

- N/A

### New Features

- N/A

### Bug Fixes

- Fixed a bug causing sync timeouts when the “**AzureAD Export URL Enable**” parameter is set to “**False**”.
- On the “**Device Info**” page “**Last Logon**” without a "**User SID**" were causing timeout issue on the visual.

### Semantic Model Changes

- Added "**User Manager**" object. This aligns with the “User Manager” object in BI for Intune. Columns in the “**User Manager**” object include:"**Manager Count**"
- "**Manager User ID**"
- "**Manager User Name**"

### Important Notes

- Always [backup your custom reports](/bi-for-intune/guides/backup-custom-reports.md) before upgrading!

---

## Version 9.0 April 21, 2025

# Version 9.0 (AppSource Version 1009)
Version 9.0 introduces powerful new reporting features, including comprehensive browser extension visibility and key enhancements to device and license management. This update also adds a new semantic model parameter and continues to build on highly requested capabilities.

**Important Notes:**
If you missed version 8.0, please [review the critical change](http://ec2-35-94-201-107.us-west-2.compute.amazonaws.com/wordpress/bi-for-defender-change-log/version-8-0-march-10-2025/) related to vulnerabilities and security update filtering.  And as always—before upgrading, [back up your custom reports](create-backup-workspace.md) to prevent data loss.


## Below are the Changes in Version 9.0


### New pages added to the BI for Defender report

**Browser Extensions** – The new Browser Extensions page provides visibility into installed browser extensions, their versions, risk ratings, and required permissions.
**Note**: To copy the new pages to your custom reports, see the article [How to Copy Pages](http://ec2-35-94-201-107.us-west-2.compute.amazonaws.com/wordpress/how-to-copy-pages/).


### New objects added to the semantic model

**Browser Extension** object – The new fields in the **Browser Extension** object include:

- Extension Activated
- Extension Install Date
- Extension Install Date (Days)
- Extension Risk
- Extension Risk Highest
- Extension Version
- Extension Version Count
- Is Extension Activated
- Is Permission Required
- Permission Required
- Permission Risk

**Browser Extension Details** object – The new fields in the Browser Extension Details object include:

- Browser Name
- Extension Description
- Extension ID
- Extension Link
- Extension Name
- Extension Vendor

**Browser Extension Permission** object – The new fields in the **Browser Extension Permission** object include:

- Permission Description
- Permission ID
- Permission Name
- Permission Type


-


### New parameters added to the semantic model

**AzureAD Incident Enable**

- Type: Boolean
- Default: TRUE
- When FALSE, the Incidents are not reported on.
- **Known issue**: This API supports a maximum of 50 results per call and 20 calls per minute. Large incident volumes may cause timeouts which will require disabling incident reporting.


### Product enhancements

Additions to the **Device** object in the semantic model:

- Device Sub Type
- Is Excluded
- Exclusion Reason

Changes to the **Device Info** page. New fields to main table and filter pane:

- Device Sub Type
- Is Excluded
- Exclusion Reason

Changes to what PowerStacks considers a "valid device" for licensing purposes. BI for Defender licensing now counts only devices where:

- License Status = Active
- Is Excluded = FALSE
- Previously we counted all active devices regardless of exclusion.


## The New Browser Extensions Page


We've added a new **Browser Extensions** report page to BI for Defender, providing detailed visibility into installed browser extensions across your environment. This report helps you identify potential risks, track versioning, and understand permission requirements at scale. By surfacing extension-level risk ratings and activation status, it supports proactive threat assessment and helps ensure that only trusted extensions are in use. Use this report to enhance visibility, tighten browser security, and reduce your overall attack surface.
![defender browser extensions](images/defender_browser_extensions-1024x579.png)

---

## Version 8.0 March 9, 2025

# Version 8.0 (AppSource Version 1008)
BI for Defender Version 8.0, shown as version 1008 in AppSource, was released on March 09, 2025.

**Important Notes:**

- Several customers have recently reported upgrade failures resulting in the loss of their custom reports. Please do not forget to [backup before you upgrade](create-backup-workspace.md)!


## Below are the Changes in Version 8.0


**New Features:**

- Added the ability to report on fixed software vulnerabilities.
- New page "Fixed Vulnerabilities"

**Semantic Model Changes:**

- Added new fields to the "Software" category:"End Of Support Date"
- “End Of Support Date (Days)"
Added new fields to the "Software Vulnerabilities" category:
- "Is Active"
- "Last Status Update"
- "Last Status Update (Days)"
- "Vulnerability Status"
Added new field to the "Software Device" category"
- "Is Active"
Added two new parameters in the semantic model:
- "AzureAD Vulnerability History Day(s)" (Default: 1 Day) (Max: 14 Days)  (Disabled: -1)
- "AzureAD Vulnerability History PageSize API" (Default: 200,000)

**Bug Fixes:**

- Fixed pagination issues with Alerts and Incidents. Previously only 50 incidents and 2,000 alerts were loaded.

**Important Notes:**

- The "Vulnerabilities" and the "Missing Security Updates" pages are impacted by updates made in this version.You will need to add the filter "Software Vulnerabilities":"Is Active" = True to these pages in your custom reports.
The "Summary "page is impacted by updates made in this version.
- You will need to add the filter "Software Vulnerabilities":"Is Active" = True on the following visuals in your custom reports:"Missing Security Updates"
- "Vulnerabilities"
You will need to add the filter "Software Vulnerabilities":"Is Active" = True and the filter "Vulnerability Name" Is Not BLANK on the following visual in your custom reports:
- "Exposed Devices"
Always backup your custom reports using our [backup process.](create-backup-workspace.md)

## The New Fixed Vulnerabilities Page


We've added a new "Fixed Vulnerabilities" report page to **BI for Defender**, giving you clear visibility into how many security vulnerabilities have been resolved over the last **XX** days. This report helps you track remediation progress, assess security team performance, and ensure threats are being addressed efficiently. With near real-time insights, you can stay proactive in strengthening your organization's security posture.
![fixed vulnerabilities](images/fixed_vulnerabilities-1024x532.png)

---

## Version 7.0 Jan. 14, 2025

# Version 7.0 (AppSource Version 1007)
BI for Defender Version 7.0, shown as version 1007 in AppSource, was released on January 14, 2025.

This release introduces multi-cloud support and brings several new features.

**Important Notes:**

- Several customers have recently reported upgrade failures resulting in the loss of their custom reports. Please do not forget to [backup before you upgrade](create-backup-workspace.md)!


## Below are the Changes in Version 7.0


- **Product Enhancements:**

- Renamed the "**Process Events**" page to "**Processes**"

- Added support for multi-cloud environments. The following new dataset parameters are required for multi-cloud environments:AzureAD Login URL (Default: [https://login.microsoftonline.com](https://login.microsoftonline.com/))
- AzureAD Graph URL (Default: [https://graph.microsoft.com](https://graph.microsoft.com/))
- AzureAD SecurityCenter URL (Default: [https://api.securitycenter.microsoft.com](https://api.securitycenter.microsoft.com/))

- **Semantic Model Changes:**

- Renamed the “**Process Events**" object to "**Process**"
- Added new fields to the “**Process**” object. Field names:File Name
- File Size
- First Event Time
- First Event Time (Days)
- Folder Path
- Last Event Time
- Last Event Time (Days)
Added new fields to the “**Application Control**” object. Field names:
- Action Type
- Application Control Count
- Authenticode Hash
- Event Type
- File Name
- File Type
- First Event Time
- First Event Time (Days)
- Folder Path
- Last Event Time
- Last Event Time (Days)
- Validated Signing Level
Renamed the "**AzureAD AdvancedHunting Process Event Day(s)**" dataset parameter to "**AzureAD AdvancedHunting Process Day(s)**"
- Default value for the "**AzureAD AdvancedHunting Process Day(s)**" is 1 Day.
**Bug Fixes:**
- Proxy Parameter. When "AzureAD Proxy Enable" = "TRUE" (Default: TRUE)

- **Important Notes:**Always backup your custom reports using our [backup process.](create-backup-workspace.md)

---

## Version 6.0 Nov. 22, 2024

# Version 6.0 (AppSource Version 1006)
BI for Defender Version 6.0, shown as version 1006 in AppSource, was released on November 22, 2024.



**Important Notes:**
 	Several customers have recently reported upgrade failures resulting in the loss of their custom reports. Please do not forget to [backup before you upgrade](create-backup-workspace.md)!


## Below are the Changes in Version 6.0


- **Features:**N/A
**Enhancements:**
- N/A
**Bug Fixes:**
- In some rare occasions you might see duplicate devices in BI for Defender. These devices would have different names and Defender ID's but the same Entra ID Device ID. We improved our deduplication logic to account for, and resolve, this issue.
**Important Notes:**
- Always backup your custom reports using our [backup process.](create-backup-workspace.md)

---

## Version 5.0 Nov. 21, 2024

# Version 5.0 (AppSource Version 1005)
BI for Defender Version 5.0, shown as version 1005 in AppSource, was released on November 21, 2024.



**Important Notes:**
 	Several customers have recently reported upgrade failures resulting in the loss of their custom reports. Please do not forget to [backup before you upgrade](create-backup-workspace.md)!


## Below Are The Changes in Version 5.0


- **Features:**

  N/A


 	**Enhancements:**

- N/A


 	**Bug Fixes:**

- In some environments the sync might fail with the error: "Expression.Error: The parameter is expected to be of type Text.Type or Binary.Type."

  This issue is due to a problem with the Defender export API. We implemented a retry to resolve the issue.
- Two new parameters "AzureAD Export URL Wait (s)"  and "AzureAD Export URL Timeout (s)"  should only be modified if directed to do so by PowerStacks support.


 	**Important Notes:**

- Always backup your custom reports using our [backup process.](create-backup-workspace.md)

---

## Version 4.0 Oct. 4, 2024

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

---

## Version 3.0 Sept. 3, 2024

# Version 3.0 (AppSource Version 1003)
BI for Defender Version 3.0, shown as version 1001 in AppSource, was released on September 3, 2024. Version 3 includes many requested improvements such as Secure Score and Incidents and Alerts.

**Important Notes:**

- New permissions are required on the [App Registration](azure-ad-app-permissions.md) in Azure. Reports will be blank if these are not added.SecurityEvents.Read.All
- SecurityAlert.Read.All
- SecurityIncident.Read.All
Several customers have recently reported upgrade failures resulting in the loss of their custom reports. Please do not forget to [backup before you upgrade](create-backup-workspace.md)!


## Below Are The Changes in Version 3.0


- **Features:**Added new "Incidents & Alerts" page.
- Added new "Secure Score" page.
- New "Alert" category added to the Semantic Model. Fields include:Alert Category
- Alert Classification
- Alert Count
- Alert Description
- Alert Detection Source
- Alert Determination
- Alert Link
- Alert Recommended Actions
- Alert Severity
- Alert Status
- Alert Title
- Created Date
- Created Date (Days)
- First Activity Date
- First Activity Date (Days)
- Last Activity Date
- Last Activity Date (Days)
- Last Update Time
- Last Update Time (Days)
- Resolved Date
- Resolved Date (Days)
New "Secure Score Control" category added to the Semantic Model. Fields include:
- Control Category
- Control Completed
- Control Description
- Control ID
- Control Max Score
- Control Name
- Control Points Achieved
- Control Rank
- Control Score
- Control Score (%)
- Control Score Impact (%)
- Control Status
- Control to Address
- Implementation Status
- Last Synced
- Last Synced (Days)
New "Secure Score Benchmark" category added to the Semantic Model. Fields include:
- Apps Score (%)
- Average Score (%)
- Basis
- Data Score (%)
- Device Score (%)
- Identity Score (%)
- Seat Size Range Lower Value
- Seat Size Range Upper Value
**Enhancements:**
- Updated the "Summary" page.Added Incident(s)
- Added Alert(s)
- Removed Inactive Device(s)
- Added Secure Score
- Added Incident by Severity
- Added Alert by Severity Removed
- Managed by
- Removed OS
Updated the "Device Info" page.
- Added "OS Build Number"
New fields added to the "Device" category in the Semantic Model:
- Device Exploitable (%)
- OS Build Number
**Bug Fixes:**
- Fixed issue causing devices without IP Address not showing up on the Device Info page.
**Important Notes:**
- New permissions are required on the App Registration in Azure. Reports will be blank if these are not added.SecurityEvents.Read.All
- SecurityAlert.Read.All
- SecurityIncident.Read.All
Always backup your custom reports using our [backup process.](create-backup-workspace.md)

## New Incidents & Alerts Page
![defender incident report](images/defender_incident_report-1024x569.png)

## New Secure Score Page
![defender secure score report](images/defender_secure_score_report-1024x568.png)

---

## Version 2.0 Feb. 28, 2024

# Version 2.0 (AppSource Version 1001)
BI for Defender Version 2.0, shown as version 1001 in AppSource, was released on February 28, 2024.



## Below Are The Changes in Version 2.0


- **Features:**N/A
**Enhancements:**
- Added new parameters to the Semantic Model.AzureAD Proxy Enable - Default Value is "TRUE". This resolves some issues with the "Connect Your Data" wizard. Customers should change this to FALSE in production environments.
**Bug Fixes:**
- N/A
**Important Notes:**
- Always backup your custom reports using our [backup process.](create-backup-workspace.md)

---
