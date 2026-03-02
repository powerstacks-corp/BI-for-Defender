---
title: "Version 10.0 June 15, 2025"
---
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
