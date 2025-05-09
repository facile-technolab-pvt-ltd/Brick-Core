# Sendgrid configuration
By default, SMTP email configuration is used to send outgoing emails. You can use Sendgrid for sending emails. This page documents process of using sendgrid instead of SMTP in your project.

## Pre-requisite
- Sendgrid account
- Domain Authentication process completed
- Send Authentication process completed
- Configuration uses the verified domain and send.

## Signing up for sendgrid account
- Go to sendgrid website and sign up using your business email.
- Generally, your account is not by default activiated and you will be asked to provide more information about how you are collecting user information.
- I recommend to follow the link and submit contact page screenshot of your website that is matching with the domain. 
- Once you submit this information, sendgrid support will activate your account in some hours.

## Domain Authentication
Follow [this documentation](https://www.twilio.com/docs/sendgrid/ui/account-and-settings/how-to-set-up-domain-authentication) to do domain verification.

## Sender Authentication
Follow [this documentation](https://www.twilio.com/docs/sendgrid/glossary/sender-authentication) to complete sender authentication process.

## Generate Sendgrid API Key
Follow [this documentation](https://www.twilio.com/docs/sendgrid/ui/account-and-settings/api-keys) to generate Sendgrid API Key. When asked for the options, Full Access, Restricted Access, or Billing Access choose Full Access if you want to avoid going through lots of options. For production usage, create restricted API key that only allow permission of sending emails.

## Configuring Sendgrid in Brick
![Login](/images/3-Sendgrid.gif "Sendgrid Configuration")

- Login to your account
- Go to settings
- Switch to `Sendgrid Settings` tab
- Enter from name, from email, and API Key
- click `Test Email` to test configuration. 

## Switch from SMTP to Sendgrid - Manual code changes
Since we are in early version, switching from SMTP to sendgrid requires some manual code changes. 

## Back to Index
- [Paid version documentation](./brick.md)