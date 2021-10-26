# Check Voisinage Interop'fibre

Check Voisinage Interop'fibre is an application aimed at referencing FTTx clients disconnected during the intervention of a technician on a PM

This tool requires an access to a PM repository as well as to a system auditing the connection status of FTTx clients.
Since docking to these two services is specific to each operator, it is not integrated into this solution.

The steps imagined for this application are:
1. Entering an intervention (requires a PM, and date and time of the start of the intervention)
2. Query of  audit system as well as the connection status for the given PM
3. summary of all disconnected clients and all customers having undergone disconnections / reconnections during the intervention


## Table of contents

- [Quick start](#quick-start)
- [Status](#status)
- [Profiles](#profiles)
- [Run FrontEnd](#run-frontend)
- [Run BackEnd](#run-backend)
- [Copyright and license](#copyright-and-license)

## Quick start

Several quick start options are available:

- Clone the repo:	`git clone https://github.com/HamzaMouza/CheckVoisinageInterop.git`
- Using SSH:		`git@github.com:HamzaMouza/CheckVoisinageInterop.git`
- With GitHub CLI:	`gh repo clone HamzaMouza/CheckVoisinageInterop`

## Status

[![npm version](https://img.shields.io/npm/v/bootstrap)](https://www.npmjs.com/package/bootstrap)
[![Meteor Atmosphere](https://img.shields.io/badge/meteor-twbs%3Abootstrap-blue)](https://atmospherejs.com/twbs/bootstrap)
[![NuGet](https://img.shields.io/nuget/vpre/bootstrap)](https://www.nuget.org/packages/bootstrap/absoluteLatest)
[![BrowserStack Status](https://www.browserstack.com/automate/badge.svg?badge_key=SkxZcStBeExEdVJqQ2hWYnlWckpkNmNEY213SFp6WHFETWk2bGFuY3pCbz0tLXhqbHJsVlZhQnRBdEpod3NLSDMzaHc9PQ==--3d0b75245708616eb93113221beece33e680b229)](https://www.browserstack.com/automate/public-build/SkxZcStBeExEdVJqQ2hWYnlWckpkNmNEY213SFp6WHFETWk2bGFuY3pCbz0tLXhqbHJsVlZhQnRBdEpod3NLSDMzaHc9PQ==--3d0b75245708616eb93113221beece33e680b229)


## What's included

Within the download you'll find the following directories and files. You'll see something like this:

```text
CHECKVOISINAGEINTEROPFIBRE/
├── CHECKVOISINAGEINTEROPFIBRE
└── CHECKVOISINAGEINTEROPFIBREAPI/
```
It is a web service achitecture project. so you find the BackEnd (CHECKVOISINAGEINTEROPFIBREAPI) and the FrontEnd (CHECKVOISINAGEINTEROPFIBRE)

The global vision of the FrontEnd is sort of that:

```text
CHECKVOISINAGEINTEROPFIBRE/
├── public/
│   ├── favicon.ico
│   └── index.html
└── src/
    ├── assets/
    ├── components/
    ├── mixins/
    ├── router/
    ├── services/
    ├── store/
    ├── types/
    ├── views/
    ├── App.vue/
    └── main.ts
```

On the other hand, you'll find the BackEnd : 

```text
├── CVI.API/
│   ├── Properties/
│   │   └── lunchSettings.json
│   ├── Controllers/
│   │   ├── AdminController.cs
│   │   ├── AuthentController.cs
│   │   └── HomeController.cs
│   ├── SendWork/
│   ├── ViewModel/
│   ├── WebLogFiles/
│   ├── appsettings.json
│   ├── Program.cs
│   └── Startup.cs
│
├── CVI.DOMAIN/
│
├── CVI.INFRASTRUCTURE/
│
└── CVI.Service/

```

## Profiles
In this application there is 3 different profiles:


| Profile/Permissions        | Administration      | Export | Intervention | Photo | History |
| ------|-----|-----|-----|-----|-----|
| Administrateur  	| r-w 	| r 	|r-w      | r-w   | r |
| Consultation  	| --	| r 	|r-w      | r-w   | r |
| Hotline  	| -- 	| - 	|r-w      | r-w   | r |


## Run FrontEnd
After you recover the project, before the first run start by installing dependencies. 
In terminal:  
```
npm install
```

now that you have installed all the dependencies you can run the application:
Run by:
```
npm run serve
```
or 
```
vue-cli-service serve
```
you can also use our predefined scripts (find them in package.json) 
```
"scripts": {
    "serve": "vue-cli-service serve --open --skip-plugins @vue/cli-plugin-eslint",
    "build": "vue-cli-service build --skip-plugins @vue/cli-plugin-eslint",
    ...
  }
```

- the option `--open` is for open the interface in the browser once the project is ready.
- the option `-skip-plugins` for skipping some hard plugins.

Building your application:
```
npm run build -- --mode testing
```




## Run BackEnd
prerequisites:
- Sql Server installed in your host. By default the app will use a local SQL Data Base.
- An integrated development environment (IDE) that supports C# (visual studio)
- .net core framework version 3.1 
- Entity framework Core version 5.0.2

Run 
In your visual studio : 
- Set your CVI.API project as startup project
- run the solution by pressing F5
- On first lunch, a local database will be created and populated with seed data automatically.
- -seed data are located in folder data under CVI.API project in seedData.sql file.   
- To change database connection go to `CVI.API/appsettings.json` and change the `connectionString` section.



## Copyright and license

Copyright 2020-2021 FITDev team.

