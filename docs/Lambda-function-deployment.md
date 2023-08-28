---
sidebar_position: 3
---

# Serverless Application Deployment

Deploy your Lambda Function **in less than 3 click**.

## Introduction

In this tutorial you will learn how to deploy your Lambda function application by creating a basic serverless application.

### Create Serveless application

Get started by **creating a new react application using vite**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 16.14 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Intialize your project

Initialize a new project using the **classic npm init script**.

The classic script will automatically create a package.json file that will hold information about your project: File in your project information by following the prompt

```bash
npm init
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

## Install swiftbase cli

Install the swiftbase cli using your node package manager:

```bash
npm i swiftbase_cli
```

## Bootstrap your project

After installing the swiftbase cli you can use the cli to bootstrap your project.The cli will be the tool that you will use to intract with the swiftbase backend.

NB. When bootstapping your application swiftbase will ask you which services you want to include in your project and since this tutorial is about Lambda function deployment make sure to select the lambda service.

Bootstrap your project by simply typing swiftbase in you terminal

```bash
swiftbase
```

# Project directory

By default Swiftbase cli will create a **_function_** directory in you project root and that directory will contain your lambda function entry file named as **handler.js**. This is the file that will receive the request from the client of this function and it is from this file that you can return the a response to the client.

NB. You can structure your code as you wish but the **handler.js** file must always be present in the **_function_** directory.

## Deploy your lambda function

Once you have written your code you can deploy you project by just typing the magic word `swiftbase` into your terminal.

```bash
swiftbase
```

or if you are using powershell

```powershell
npx swiftbase
```

Swiftbase cli will prompt you on which services you would like to deploy if multiple services are configure. For the purpose of this demo make sure to select lambda service and confirm your wish to deploy.

After confirmation swiftbase will deploy your lambda function and it will display the url to your project in the terminal. using the url you can interact with your live function !!!.
