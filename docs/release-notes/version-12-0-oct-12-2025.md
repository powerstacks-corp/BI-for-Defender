---
title: "Version 12.0 Oct. 12, 2025"
---
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
