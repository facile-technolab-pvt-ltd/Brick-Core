# Brick-Core
This documentation is for free version of the Brick - SaaS Starter kit.

## Pre-requisite
- Visual Studio 2022 community or Visual Studio Code
- .NET SDK 8.0 Latest
- Node latest

## Running Back end Project
Open Brick.Core.sln file in Visual Studio from the root folder of the source code.

### Setting up appsettings.Development.json
- Open appsettings.Development.json and set value of `DbProvider` setting to `SqlServer` or `PostgreSQL` based on what you want to use.
- Set values of `DefaultConnection` & `TenancyDefaultConnection` in `ConnectionStrings` section if you want to use `SqlServer` and remove the other two connection strings.
- Notice the {0} in the database value in the `TenancyDefaultConnection`. Could you keep it with it so that tenant database can be set dynamically? 
- If you want to use `PostgreSQL`, delete `DefaultConnection` & `TenancyDefaultConnection` and set connection string values in the other two settings of the connectionStrings section.
- By default `MultiTenancy` is true, set it to false if you do not want to use MultiTenancy features.
- `UISelection` setting can take 2 values, `React` or `Angular`
- you will need either `AngularURI` or `ReactURI` depending on the UI you use. Remove other configuration
- in the `Authentication:JwtBearer:SecurityKey` configuration, update the security key to something more strong and secure. Use 

### Run update database
- Open tools > Nuget Package Manager > Package Manager console
- Select Brick.Core.Data as the project
- enter command `Add-Migration "Initial"` and wait for the migration to be created.
- enter the command `Update-Database` and wait for it to build and finish running migrations.
- Set Brick.Core.Web as a startup project and hit F5 to run the project.

## Running Front end project
Front end application of the project is under root folder /Brick.Core.Web/UI/Angular or /Brick.Core.Web/UI/React depending upon which front end you are using. We will call it root folder of your front end project. 

### NPM install 
- root folder of your front-end project in the command prompt 
- run `npm install --force` to install all npm dependencies.

### Run Angular project 
- The angular project was tested on Node.js version 22.13.0 (We use NVM to switch between node versions.)
- run `ng serve` to run the front-end project and wait for the message that says compiled successfully
- go to the browser and enter http://localhost:4200 to see the front end running 

### Run React.js/Next.js project 
- The react project was tested on Node.js version 22.13.0 (We use NVM to switch between node versions.)
- run `npm run dev` to run the front-end project.
- go to the browser and enter http://localhost:3000 to see the front end running 

### Default credentials
- use `admin@yourdomain.com` as default username and `123qwe` as password

## Screenshots
- [Angular version Screenshots](./docs/angular-screens.md)
- [React version Screenshots](./docs/react-screens.md)
