# Check Voisinage Interop'fibre

Check Voisinage Interop'fibre is an application that offer a set of easy communications between company operators about interventions.
It is everything you need to create an intervention: SAV, RACCORDEMENT and others.
This application is designed to look great and to provide powerful functionality in any browser.

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

   | Profile/Permissions | Administration | Export | Intervention | Photo | History |
   | ------|-----|-----|-----|-----|
    | Administrateur     |       r-w      |    r   |     r-w      | r-w   | r |
     | Consultation       |       --       |    r   |     r-w      | r-w   | r|
     |Hotline            |       --       |    -   |     r-w      | r-w   | r |

| Format        | Syntax      | Example |
| ------|-----|-----|
| Italic  	| \*Text\* 	| *This is italic* 	|
| Bold  	| \*\*Bold\*\* 	| **This is bold** 	|


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

For the build you can use:
```
npm run build -- --mode testing
```




## Run BackEnd
Prerequisits:
Sql Server installed in your host.
By default the app will use a local SQL Data Base.
To change database connection go to `CVI.API/appsettings.json` and change the `connectionString` section.



## Copyright and license

Copyright 2020-2021 FITDev team.

