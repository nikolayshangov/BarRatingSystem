# BarRatingSystem
![BarRatingSystem](https://github.com/nikolayshangov/barratingsystem/assets/100240526/668a3c19-445b-41aa-87a9-040fb7b76d30)
##### Web application to serve as a management system for bars, their ratings, and tracking other bars near the user.

## Description
##### Project for "IT Carrer" National Programme of the Ministry of Education and Science (MES) [State Examination - "Software Engineering"]

### Details
##### This application is capable of adding bars with specific image, place and type. Registered users can edit their own profiles, create bars or edit/delete their own ones and see bars of other managers. Unregistered users can see registered managers' bars. The project relies on external service providers, it is accessing them via their API which requires authentication, the application won't be fully functional without them.

## Installation
##### - Download BarRatingSystem.dacpac <a href="https://github.com/nikolayshangov/barratingsystem/blob/master/CustomDatabase/BarRatingSystem.dacpac">[from BarRatingSystem's GitHub Repository]</a>
##### - Start Visual Studio and open SQL Server Object Explorer.
##### - Locate your SQL Server Instance and expand it to Databases then right-click, press Publish Data-tier Application.
##### - Select BarRatingSystem.dacpac, make sure Database Name, Publish Script Name are called BarRatingSystem, then click on Publish.
##### - Download the Code from GitHub, open the project and go back in SQL Server Object Explorer.
##### - Right-click on your SQL Server Instance, click on Properties, find Connection string, copy it and paste it in `appsettings.json`:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "ReplaceWithConnectionString"
  }
```
##### - Get your CloudName, API Key, API Secret from Cloudinary and paste them in `appsettings.json`:
```json
  "CloudinarySettings": {
    "CloudName": "ReplaceWithYourCloudName",
    "ApiKey": "ReplaceWithYourApiKey",
    "ApiSecret": "ReplaceWithYourApiSecret"
  },
```
##### - Get your Token from IPinfo and paste it in `Controllers/HomeController.cs`:
```
var ipInfo = new IPInfo();
var homeViewModel = new HomeViewModel();
try
{
    string url = "https://ipinfo.io?token=ReplaceWithYourToken";
    var info = new WebClient().DownloadString(url);
```

### Required software, files and API
##### - .NET 6.0
##### - SQL Server 2022 (Express or Developer Edition)
##### - SQL Server Management Studio 20.1 (SSMS)
##### - Visual Studio 2022 (Community, Professional or Enterprise Edition)
##### - Custom Database (BarRatingSystem) <a href="https://github.com/nikolayshangov/barratingsystem/blob/master/CustomDatabase/BarRatingSystem.dacpac">[from BarRatingSystem's GitHub Repository]</a>
##### - Cloudinary Account (for CloudName, API Key, API Secret)
##### - IPinfo Account (for Token)

## Built with
#### Programming Languages and Tools
##### - C#
##### - SQL Server
##### - ASP.NET Core Model-View-Controller (MVC) [used Views, Identity, Controller, Dependency Injection for Services]
##### - Entity Framework Core
##### - Javascript
##### - JSON
##### - Bootstrap (Jumbotron) [used Album Example, Wider Cards for Thumbnails]
##### - Cloudinary (.NET SDK)
##### - IPinfo (.NET SDK)

### Screenshots
#### Pages
##### - Home (Logged out)
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/3a1ace99-5355-4635-bdd4-adbb2abd8fc9)
##### - Bars (Logged out)
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/b4d81f3c-f146-4f57-8071-90322291887e)
##### - Bar Details (Logged out)
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/b9fdebfa-8b09-4a1b-8676-f38174c52b9c)
##### - Register (Logged out)
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/bc9bed54-72f5-4a81-b2f9-3ec30a67fc91)
##### - Login (Logged out)
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/30929ace-acbc-4c9d-8e55-5435350bb003)
#### Pages with Special Access
##### - Managers (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/5a6c5a08-62b5-40f0-bb6b-9e1ec1ff712b)
##### - Dashboard (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/61272a36-4fd9-41c2-85f8-8a0893d3ca86)
##### - Edit Account (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/f571fdb9-cab8-4096-8a4f-9066b5915354)
##### - Create Bar (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/e97ca5b7-11f6-4717-969a-6dd499913f00)
##### - Delete Bar (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/barratingsystem/assets/100240526/e9b01014-785d-4a10-a2f9-923b96b50c79)

## Creator
##### Copyright © 2024 Nikolay Shangov
###### Note: Template is from <a href="https://github.com/nikolayshangov/runclubmanager">[My Course Project - RunClubManager for Module 13 - "Software Engineering"]</a>

## License
##### BarRatingSystem is distributed under the MIT License, see the text file LICENSE for more details.
