---
title: "Version 7.0 Jan. 14, 2025"
---
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
