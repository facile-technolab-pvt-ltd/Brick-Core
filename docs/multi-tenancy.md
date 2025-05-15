# Multi-tenancy
Brick paid version enables multi-tenancy by default. 

## Default tenant
Default tenant or host tenant is a tenant that is used by Super Admin to perform multi-tenancy owner activities like provisioning new tenants, creating other super admins and can be customized to support other Super Admin level features as required.

## Getting started
- When you run the project first time, Default tenant is automatically provisioned using seed methods along with super admin account.
- That's the reason you see default company when you login for the first time.

## Adding more tenants 

### Adding more tenants in `Development environment`
- Login to Default tenant on url http://localhost:3000, login with default admin credentials
- go to Tenants section
- Click on Add tenant
- Set `tenant1` in Name and Tenancy Name, copy connection string from appsettings and set database name to `tenant1`, and create tenant.
- once the tenant is created and shows in the tenant's list. You can switch to another incognito browser and locate: http://tenant1.localhost:3000, you will notice that the login page will show tenant1 instead of default now.
- login with the tenant admin credentials you provided at the time of creating tenant
- now you can configure the tenant specific settings individually for this specific tenant.

## Back to Index
- [Paid version documentation](./brick.md)