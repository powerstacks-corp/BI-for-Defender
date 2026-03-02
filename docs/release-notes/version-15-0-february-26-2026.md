---
title: "Version 15.0 February 26, 2026"
---
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
