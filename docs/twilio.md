# Twilio configuration

Similar to other settings, Twilio configuration is also per tenant. This means twilio needs to be configured per tenant. In order to configure twilio with specific tenant, you can:
- login to the http://{tenant-name}.localhost:3000 
- go to settings
- click on twilio tab
- enter `AccountSid`, `AuthToken`, and `Mobile Number with country code` that you want to use to send sms
- Go through [Multi-tenancy](./multi-tenancy.md) documentation to understand how to setup multiple tenants.

Once you have configured this, users will be able to use SMS in the two factor verification and will be able to receive sms from these number.

Please note that twilio provides you credit of $15.50 to get started with your development but you many need to upgrade to use twilio sms service in the production mode. 

Check country specific charges to estimate your budget for sms verification.


## Back to Index
- [Paid version documentation](./brick.md)