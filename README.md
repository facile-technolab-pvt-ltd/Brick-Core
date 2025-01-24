# Brick-Core
Brick Core is a free version of Brick SaaS Starter kit. 

## Pre-requisite
- Visual Studio 2022 community or Visual Studio Code
- .NET SDK 8.0 Latest
- Node latest (or version 18+)

## Folder Structure
![folder structure screenshot](/images/project-structure.png)
## Running Back end Project
Open Brick.Core.sln file in visual studio from the root folder of the source code.

### Setting up DbProvider & ConnectionStrings
- Open appsettings.json and set value of `DbProvider` setting to `SqlServer` or `PostgreSQL` based on what you want to use.
- Set values of `DefaultConnection` & `TenancyDefaultConnection` if you want to use `SqlServer` and remove other two connection strings.
- Notice the {0} in the database value in the `TenancyDefaultConnection`. Keep it as it so that tenant database can be set dynamically. 
- In case you want to use `PostgreSQL`, then delete `DefaultConnection` & `TenancyDefaultConnection` and set connection string values in the other two settings of the connectionStrings section.

### Run update database
- Open tools > Nuget Package Manager > Package Manager console
- Select Brick.Core.Data as the project 
- enter command `Update-Database` and wait for it to build and finish running migrations.
- Set Brick.Core.Web as startup project and hit F5 to run the project.

## Running Front end project
Front end application of the project is under root folder /Brick.Core.Web/UI/Angular or /Brick.Core.Web/UI/React depending upon which front end you are using. We will call it root folder of your front end project. 

### NPM install 
- root folder of your front end project in command prompt 
- run `npm install --force` to install all npm dependincies.

### Run Angular project 
- run `ng serve` to run the front end project and wait for the message that says compiled successfully
- go to browser and enter http://localhost:4200 to see the front end running 

### Run Angular project 
- run `npm run dev` to run the front end project and wait for the message that says compiled successfully
- go to browser and enter http://localhost:3000 to see the front end running 

### Default credentials
- use `admin@gmail.com` as default username and `123qwe` as password


## Screenshots
- [Angular version Screenshots](./docs/angular-screens.md)
- [React version Screenshots](./docs/react-screens.md)

### 