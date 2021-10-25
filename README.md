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

## What's included

Within the download you'll find the following directories and files. You'll see something like this:

```text
CHECKVOISINAGEINTEROP/
├── CHECKVOISINAGEINTEROPFIBRE
└── CHECKVOISINAGEINTEROPAPI/
```
It is a web service achitecture project. so you find the BackEnd (CHECKVOISINAGEINTEROPAPI) and the FrontEnd (CHECKVOISINAGEINTEROPFIBRE)

The globale vision of the FrontEnd is sort of that:

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

On the other hand you find the BackEnd like that : 

```text
├── CVI.API/
│   ├── Properties/
│   │   └── index.html
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
-  Administrator : the mot prowerful profile and he has all permissions and can visualise all interfaces.
-     : create, and select interventions, view historiers, Export Excel reports .
-  Hotline : create, and select interventions, view historier, he can't do any administration, also he can't export Excel reports.

## Run FrontEnd
After you recover the project, for just one time, you need to install dependencies  
```
npm install
```

Here all the envirement is ready you can run the appliacation:
```
vue-cli-service serve
```

Or you can use our predefined scripts (find them in package.json) 
```
"scripts": {
    "serve": "vue-cli-service serve --open --skip-plugins @vue/cli-plugin-eslint",
    "build": "vue-cli-service build --skip-plugins @vue/cli-plugin-eslint",
    ...
  }
```
Simply run it by:
```
npm run serve
```
the option --open is for open the interface in the browser once the project is ready.
the option -skip-plugins for skipping some hard plugins.

For the build you can use:
```
vue-cli-service build -- --mode testing
```




## Run BackEnd
TO DO
