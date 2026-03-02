---
title: "Create Azure AD App Registration"
---
# Create Azure App Registration
Synchronizing data from Microsoft Defender for Endpoint is done using application permissions. Here we are configuring the permissions required for Power BI to connect to the Microsoft API's to retrieve the data.


**Prerequisites:**The user performing this step requires Global Admin and Subscription Admin rights.

### Step 1





1. Login to **portal.azure.com** using a global administrator account.
1. Search for and select **App registrations**.
1. Select **New registration**.
![](../images/New_Registration-1024x491.png)
### Step 2





1. Enter a **Name** for the application. (This will not be seen by anyone other than admins.)
1. Specify who can use the application as **Accounts in this organizational directory** only.
1. Select **Register**.
![register defender app](../images/register_defender_app-812x1024.png)
### Step 3





1. On the Enterprise App page select **API Permissions**.
1. Remove the **User.Read** permission.
1. Select **Add a permission**.
![defender remove default permmissions](../images/defender_remove_default_permmissions-1024x472.png)
### Step 4





1. Select **Microsoft Graph**.
![](../images/MS_graph-1024x434.png)
### Step 5





1. Select **Application permissions**.
![](../images/application_permissions-1024x403.png)
### Step 6





1. Search for **Security**.
1. Select the following permissions:**SecurityAlert.Read.All**
1. **SecurityEvents.Read.All**
1. **SecurityIncident.Read.All**
**Do not select the Add permissions button, continue to the next step.**
![defender security read permissionspng](../images/defender_security_read_permissionspng-680x1024.png)
### Step 7





1. Search for **Directory**.
1. Select the following permissions:**Directory.Read.All**
**Do not select the Add permissions button, continue to the next step.**
![directory read](../images/directory_read-692x1024.png)
### Step 8





1. Search for **CloudApp-Discovery**.
1. Select the following permissions:**CloudApp-Discovery.Read.All**
**Do not select the Add permissions button, continue to the next step.**
![](../images/Cloud-app-discovery-permission-686x1024.png)
### Step 9





1. Search for **Directory**.
1. Select the following permissions:**Directory.Read.All**
**Do not select the Add permissions button, continue to the next step.**
![directory read](../images/directory_read-692x1024.png)
### Step 10





1. Search for **ThreatHunting**.
1. Select **ThreatHunting.Read.All.**
1. Select the **Add permissions button.**
![threat hunting readall](../images/threat_hunting_readall-677x1024.png)
### Step 11





1. On the Enterprise App page select **API Permissions**.
1. Select **Add a permission**.
![defender add more permissions](../images/defender_add_more_permissions-1024x533.png)
### Step 12





1. Select **APIs my organization uses**.
1. Search for **WindowsDefenderATP**.
1. Select **WindowsDefenderATP** in the search results.
![windows defender atp api](../images/windows_defender_atp_api-1024x460.png)
### Step 13





1. Select **Application permissions**.
![windows defender atp app permissions](../images/windows_defender_atp_app_permissions-1024x393.png)
### Step 14





1. Search for **Machine**.
1. Select the following permissions:**Machine.Read.All**
**Do not select the Add permissions button, continue to the next step.**
![defender machine readall](../images/defender_machine_readall-678x1024.png)
### Step 15





1. Search for **SecurityRecommendation**.
1. Select the following permissions:**SecurityRecommendation.Read.All**
**Do not select the Add permissions button, continue to the next step.**
![defender security read all](../images/defender_security_read_all-1-677x1024.png)
### Step 16





1. Search for **Software**.
1. Select the following permissions:**Software.Read.All**
**Do not select the Add permissions button, continue to the next step.**
![defender software read all](../images/defender_software_read_all-687x1024.png)
### Step 17





1. Search for **Vulnerability**.
1. Select the following permissions:**Vulnerability.Read.All**
Select the **Add permissions**button.
![defender vulnerability read all](../images/defender_vulnerability_read_all-681x1024.png)
### Step 18





1. Select **Grant admin consent for **.
![grant defender permissions](../images/grant_defender_permissions-1024x628.png)
### Step 19





1. Select **Yes**at the prompt.
![](../images/Admin-Consent-Yes-1024x108.png)
### Step 20





1. Select **Certificates & secrets**.
1. Select **New client secret**.
1. Enter a **Description**.
1. Select a value for **Expires**.
1. Select **Add**.
![defender new secret](../images/defender_new_secret-1024x513.png)
### Step 21





1. Record the **Value** data as the **Azure AD Client Secret**. This will be used later in the installation process. The value can only be displayed once, if you fail to record it here you will have to create a new one.
1. **NOTE: This is the most common mistake made. You do not need the "Secret ID" You just need the "Value".**
![defender secret value](../images/defender_secret_value-1024x302.png)
### Step 22





1. Select **Overview**.
1. Record the **Application (client) ID** as the **Azure AD Client ID**. This will be used later in the installation process.
1. Record the **Directory (tenant) ID** as the **Azure AD Tenant ID**. This will be used later in the installation process.
1. The **Azure AD Application registration** is now **complete**.
![defender app overview](../images/defender_app_overview-1024x601.png)
