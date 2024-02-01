---
sidebar_position: 2
---

# Static Site Deployment

Deploy your Static Site application with ease.

## Introduction

In this tutorial you will learn how to deploy your Static Site application by creating a basic react application and deploying on Swiftbase.

### Create React Application

Get started by **creating a new react application using vite**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 16.14 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.
- [Vite](https://vitejs.dev/)

## Intialize your project

Initialize a new react application using the vite create script and follow the instuction to create your react application.

```bash
npm create vite@latest
```

The script will automatically create all the files and directories needed to build a react application. Next cd into your react application and install all the required dependencies.

```bash
npm i
```

## Install Swiftbase cli

Install the swiftbase cli using your node package manager:

```bash
npm i swiftbase_cli
```

## Bootstrap your project

After installing the swiftbase cli you can use the cli to bootstrap your project. For more information follow [Basics](intro).
Bootstrap your project by simply typing swiftbase in you terminal

```bash
swiftbase init
```

## Project structure

After initialization there will be a .swb file in the projects root directory which contains project configuration information such as project id and your access token.
NB Make sure to not include the this file into your project repo as it contains sensitive information so keep it confidential at all cost!!

## Build your react application

Swiftbase cli by defaults your deployment ready static files to be found inside and you run the command below vite will generate this directory.

```bash
npm run build
```

## Deploy your react application

Once you have written your code you can deploy your project by just typing the magic word `swiftbase deploy` into your terminal.

```bash
swiftbase deploy
```

or if you are using powershell

```powershell
npx swiftbase
```

Swiftbase cli will prompt you on which services you would like to deploy if multiple services are configure. For the purpose of this demo make sure to select static site service and confirm your wish to deploy your react application.

After confirmation swiftbase will deploy your react application and it will display the url to your project in the terminal. using the url you can interact with your live project !!!.
