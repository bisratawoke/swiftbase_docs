---
sidebar_position: 1
---

# Tutorial Basics

Let's discover **Swiftbase in less than 5 minutes**.

## Getting Started

Get started by **creating a new site**.

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

After installing the swiftbase cli you can use the Swiftbase cli to bootstrap your project and start coding your dream project.

The cli will be the tool that you will use to intract with the swiftbase backend , meaning you will use it for authentication purposes such as registration and or login purposes as well as for deployment of your static site and or your lambda function.

To bootstrap your project just type swiftbase in your terminal. NB if your are using powershell you might have to precede the swiftbase command with the term npx.

```bash
swiftbase
```

or if your using powershell

```powershell
npx swiftbase
```

When your run this command for the first time your will be prompted to enter your credentials and if this is your first time using swiftbase you will be prompted to register.

After that you will be prompted to create a project by entering the project name and selecting the services you want in your project.

NB. If you included static site deployment as one of the services then make sure that your static files are located in /dist folder located at the root of your project. For more info check out [Static Site Deployment](Static-site-deployment).

<!-- NB even though you can multiple files and directory that contain your code the `handler.js` will be the entry point of your lambda function meaning it is this file that will receive the http request object therefore the `handler.js` must be present at the root of your project. Other than that you can design your project and as you see fit. -->

## Deploy your project

Once you have written your code you can deploy you project with by just typing the magic word `swiftbase` into your terminal.

```bash
swiftbase
```

or if you are using powershell

```powershell
npx powershell
```

Swiftbase cli will prompt you on which services you would like to deploy if multiple services are configure and will deploy your services and it will display the url to your project in the terminal. using the url you can interact with your live project !!!.
