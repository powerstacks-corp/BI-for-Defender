---
title: "Version 8.0 March 9, 2025"
---
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
