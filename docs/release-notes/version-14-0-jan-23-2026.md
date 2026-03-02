---
title: "Version 14.0 Jan. 23, 2026"
---
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
