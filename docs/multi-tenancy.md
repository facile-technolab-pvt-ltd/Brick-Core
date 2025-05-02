# Multi-tenancy
Brick paid version enables multi-tenancy by default. 

## Default tenant
Default tenant or host tenant is a tenant that is used by Super Admin to perform multi-tenancy owner activities like provisioning new tenants, creating other super admins and can be customized to support other Super Admin level features as required.

## Getting started
- When you run the project first time, Default tenant is automatically provisioned using seed methods along with super admin account.
- That's the reason you see default company when you login for the first time.

## Adding more tenants 
- At the time of development, you can login to Default tenant, create a new tenant and use 'Login with tenant' feature to test your tenant specific features
- At the time of production, tenant name in the tenant management section will be used to automatically map it to the subdomain. For example, brick.faciletechnolab.com will map to tenant called Brick. It's case insensitive.

## Back to Index
- [Paid version documentation](./brick.md)