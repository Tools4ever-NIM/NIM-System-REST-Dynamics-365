# NIM-System-REST-Dynamics-365

## Current Available Data
- Accounts
- Contacts

## Setup Authentication

- Go to your Azure AD portal at https://portal.azure.com/.
- Click Azure Active Directory under Azure Services.
- Go to App Registrations.
- Click New Registration.
- Enter a Name. For example, NIM.
- Click Register.
- You are taken to the new app registration.
- Create and upload your certificate in NIM and Azure.
- Outside of Azure, use your preferred method to generate a self-signed certificate. Create both X.509 encoded binary .cer and .pfx formats.
- In Azure, go to Certificates & Secrets. Click Upload Certificate. Use the .cer format. Click Add. The certificate is uploaded.
- In NIM, Add a certificate. Use the .pfx format.
- In Azure, go to the new app's Overview.
- Copy and paste the Application (Client) ID and Directory (Tenant) ID fields into the corresponding fields of the Connection tab in NIM.
- In NIM, select the newly uploaded certificate in the Certificates pane. The Certificate (Name) field is automatically populated.
- Click Save.
- In Azure, go to API Permissions.
- Click Add a Permission.
- Click Dynamics CRM.
- Click Delegated Permissions.
- Select the following permissions:
  - user_impersonation
- Click Add Permissions.
- Click Grant Admin Consent for <app name>. Click Yes to confirm.
- Open Power Platform Environments https://admin.powerplatform.microsoft.com/environments
- Click on Environment you want to access
- Click Settings
- Expand Users + permissions, Click Application Users
- Click "New App User"
- Select App created in Azure
- Select Appropriate Security roles for permissions

## Reference
https://docs.microsoft.com/en-us/dynamics365/customer-engagement/web-api/entitytypes?view=dynamics-ce-odata-9
