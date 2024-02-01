---
sidebar_position: 1
---

# Tutorial Basics

Let's discover **Swiftbase in less than 5 minutes**.

## Getting Started

Get started by **creating a new site**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 16.14 or above:
  - When installing Node.js, it is recommended to check all checkboxes related to dependencies.

## Intialize your project

Initialize a new project using the **classic npm init script**.

The classic script will automatically create a package.json file that will hold information about your project: Fill in your project information by following the prompt

```bash
npm init
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

## Install swiftbase cli

Install the swiftbase cli using your node package manager:

```bash
npm i swiftbase_cli
```

## Get to know your CLI

The cli will be the tool that you will use to intract with the swiftbase backend , meaning you will use it for authentication purposes such as registration and or login purposes as well as for deployment of your static site and or your lambda function.

To communicate with swiftbase services just type swiftbase in your terminal followed by an action you would like swiftbase to do. To see all the available actions or commands just type swiftbase into the cli.
NB if your are using powershell you might have to precede the swiftbase command with the term npx.

```bash
swiftbase
```

## Authentication

You can you the swiftbase cli to register and login into swiftbase. To do so just type swiftbase followed by either register or login command and passing in your email and password.

```bash
swiftbase login -e youremail@example.com -p yourpassword
```

or

```bash
swiftbase register -e youremail@example.com -p yourpassword
```

Once registered please make sure to login with your credentials and proceed to creating your project

## Bootstrap your project

After installing the swiftbase cli you can use the Swiftbase cli to bootstrap your project and start coding your dream project.
To bootstrap your project just type swiftbase followed by the 'init' command into your terminal. You will be asked to select between creating a new project or using an existing project then you will be prompted selected the services you would like to include into your project.

```bash
swiftbase init
```

And thats it your project has been created and you can start build your application using the services that you selected.

## Application structure

So when you selected your services in your project initalization you might have noticed that some files and folders were created. Upon the creation of any project a .swb file will be created at the root of your project. This fill will contain all you configuration such as the project identifiers as well as your access token.

NB You must not include your .swb file into you repo and always keep this file confidential.

Another folder you might have noticed is the function folder that is created at your sroot of your project. This folder will be created if you selected lambda function as one of the services during your project initialization and as you might have already guessed it is in this folder that swiftbase will expect your lambda function to be stored. In this folder there is a file called hander.js and it is the entry of your lambda function and it will be the file that will be called when the function is run so it is manditory to have this file included in this project along with its initial structure. Other than that you can structure your lambda function as you wish, For more info check out [Swiftbase servless application](Lambda-function-deployment).

PS. If you included static site deployment as one of the services then make sure that your static files are located in /dist folder located at the root of your project. For more info check out [Static Site Deployment](Static-site-deployment).

<!-- NB even though you can multiple files and directory that contain your code the `handler.js` will be the entry point of your lambda function meaning it is this file that will receive the http request object therefore the `handler.js` must be present at the root of your project. Other than that you can design your project and as you see fit. -->

## Deploy your project

Once you have written your code you can deploy you project with by just typing the magic word `swiftbase` into your terminal.

```bash
swiftbase deploy
```

Swiftbase cli will prompt you on which services you would like to deploy if multiple services are configure and will deploy your services and it will display the url to your project in the terminal. using the url you can interact with your live project !!!.
