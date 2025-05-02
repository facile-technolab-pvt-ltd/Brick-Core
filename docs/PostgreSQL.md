# How to use PostgreSQL
Paid version of Brick - SaaS Starter kit uses Microsoft SQL Server by default. This page explains how to switch to PostgreSQL database.

## Why manual work?
We are at early stage of this starter kit. We are working on powershell that can automatically do this for you. In the meanwhile, please follow the below steps to switch to PostgreSQL

![Login](/images/2-PostgreSQL.gif "PostgreSQL")

## Step 1:
- Create a blank database in PostgreSQL. I use PgAdmin, but you can use tool of your choice to do this.

## Step 2:
- Go to /Facile.StarterKit.Web/appSettings.development.json
- You will notice two `ConnectionStrings` section. One of them is commented out which can be used for PostgreSQL connection string. You can umcomment that section and comment out the Microsoft SQL Server section.

## Step 3
- Press ` Ctrl+Shift+F` to search in all solutions and search for `DefaultConnection`, you will see all the places where `DefaultConnection` is being used. You need to replace it with PostgreSQL Connectionstring name called `PGDefaultConnection`. 
- In file /Facile.StarterKit.Data/Extentions/DataExtentions.cs, you will see `option.UseSqlServer(configuration.GetConnectionString("DefaultConnection"));`, replace it with `option.UseNpgsql(configuration.GetConnectionString("PGDefaultConnection"));`

## Step 4
- Save all changes and rebuild your project

## Step 5
- Open tools > Nuget Package Manager > Package Manager console
- Select Brick.Core.Data as the project
- enter command `Add-Migration "Initial"` and wait for the migration to be created.
- enter the command `Update-Database` and wait for it to build and finish running migrations.
- Set Brick.Core.Web as a startup project and hit F5 to run the project.

## Step 6
- Clean up the projects by removing reference of Entity Framework for SQL Server related nuget packages and code.


## Back to Index
- [Paid version documentation](./brick.md)