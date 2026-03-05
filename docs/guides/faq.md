---
title: "FAQ"
---
# Frequently Asked Questions

### How often should I refresh my dataset?

We recommend configuring your dataset to refresh at least **once per day**. Power BI allows up to 8 scheduled refreshes per day depending on your license. See [Configure Data Sync](configure-data-sync.md) for setup instructions.

### What permissions does the app registration need?

The Azure AD app registration requires several Microsoft Graph API permissions to access Defender for Endpoint data. See [Azure AD App Permissions](azure-ad-app-permissions.md) for the complete list of required and optional permissions.

### My data is not refreshing. What should I check?

1. Confirm that the **API Key**, **Tenant ID**, **Client ID**, and **Client Secret** are correctly entered in the dataset parameters. See [Configure the Dataset](configure-the-dataset.md).
2. Verify that admin consent has been granted for all required API permissions in the Azure portal.
3. Check that the client secret has not expired — create a new one if needed.
4. Ensure the scheduled refresh is configured. See [Configure Data Sync](configure-data-sync.md).

### How do I set up Application Controls reporting?

Application Controls reporting allows you to monitor and report on application control policies in Defender for Endpoint. See [Application Controls](application-controls.md) for the configuration steps.

### How do I fix broken visuals after an upgrade?

When we rename fields in a new version, any visualization containing a renamed field will appear broken (showing an exclamation point on the affected columns). To fix this:

1. Open the page containing the broken visual in **Edit** mode.
1. Select the broken visualization.
1. On the **Visualizations pane**, find the columns with an exclamation point ("!").
1. Select the "**X**" to remove the old column from the visualization.
1. On the **Data pane**, search for the new field name (check the [Release Notes](../release-notes/index.md) for the renamed fields).
1. Add the new field by placing a checkmark next to it.
1. Rearrange the field order if needed by dragging it in the Visualizations pane.
1. **Save** the changes.

!!! tip
    Always review the [Release Notes](../release-notes/index.md) before upgrading and [back up your custom reports](backup-custom-reports.md) first.
