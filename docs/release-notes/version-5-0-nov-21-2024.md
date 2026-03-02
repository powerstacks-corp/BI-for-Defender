---
title: "Version 5.0 Nov. 21, 2024"
---
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
