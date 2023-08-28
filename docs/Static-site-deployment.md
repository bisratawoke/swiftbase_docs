---
sidebar_position: 2
---

# Static Site Deployment

Deploy your Static Site application **in less than 3 click**.

## Introduction

In this tutorial you will learn how to deploy your Static Site application by creating a basic react application and deploying on Swiftbase.

### Create React Application

Get started by **creating a new react application using vite**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 16.14 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.
- [Vite](https://vitejs.dev/)

## Intialize your project

Initialize a new project using the vite create script **npm create vite@latest** and follow the instuction to create your react application.

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

After installing the swiftbase cli you can use the cli to bootstrap your project.The cli will be the tool that you will use to intract with the swiftbase backend. NB When bootstapping your application swiftbase will ask you which services you want to include in your project and since this tutorial is about static site deployment make sure to select the static site service.

Bootstrap your project by simply typing swiftbase in you terminal

```bash
swiftbase
```

## Build your react application

```bash
npm run build
```

or if you are using powershell

```powershell
npx swiftbase
```

## Deploy your react application

Once you have written your code you can deploy you project by just typing the magic word `swiftbase` into your terminal.

```bash
swiftbase
```

or if you are using powershell

```powershell
npx swiftbase
```

Swiftbase cli will prompt you on which services you would like to deploy if multiple services are configure. For the purpose of this demo make sure to select static site service and confirm your wish to deploy your react application.

After confirmation swiftbase will deploy your react application and it will display the url to your project in the terminal. using the url you can interact with your live project !!!.
