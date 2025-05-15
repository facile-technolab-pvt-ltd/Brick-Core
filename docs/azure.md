# Configure Entra ID/Azure AD Authentication
- Go through [Multi-tenancy](./multi-tenancy.md) documentation to understand how to setup multiple tenants.

Similar to other settings, Entra ID/Azure AD Authentication configuration is also per tenant. This means Entra ID/Azure AD Authentication needs to be configured per tenant. In order to configure twilio with specific tenant, you can:
- Login to your Azure Account and go to (this article)[https://www.faciletechnolab.com/blog/how-to-implement-azure-ad-authentication-in-aspnet-core-50-web-application/] and follow steps described in `Setting up your App in Azure AD` section to configure your application. Once this is done, you can switch to brick starter kit.
- login to tenant you want to conifgure using http://{tenant-name}.localhost:3000 
- go to `Social Auth Settings` section and check `Microsoft` checkbox. 
- This will enable a form with below settings:
- `Instance Id`: enter `https://login.microsoftonline.com/`.
- `TenantId`: copy the GUID of the tenant from the application you created in Azure.
- `ClientId`: client id from the application you created in Azure.
- `Domain`: domain.onmicrosoft.com at the time of development. In production you can set specific domain if it's configured in Azure.
- `Secret`: client secret from the application you created in Azure.

Once you are done with setting this values, hit save. logout from current session to see Microsoft authentication icon will be shown. Now any new user who will click it will automatically be added to the tenant and also visible in the users section. 

## Back to Index
- [Paid version documentation](./brick.md)