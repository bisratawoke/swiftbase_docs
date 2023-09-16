---
sidebar_position: 3
---

# SwiftStore

Learn how to work with SwiftStore **in less than 3 minutes**.

## Introduction

In this tutorial you will learn how work with swiftbase's Nosql database called SwiftStore.

### Create Swiftbase project

Get started by **Creating swiftbase project**.

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

## Install SwiftStore sdk

Install the swiftstore sdk using your node package manager:

```bash
npm i swiftbase_db_sdk
```

## Bootstrap your project

After installing the swiftbase cli you can use the cli to bootstrap your project.The cli will be the tool that you will use to intract with the swiftbase backend.

NB. When bootstapping your application swiftbase will ask you which services you want to include in your project and since this tutorial is about Swiftbase database make sure to select the lambda service.

Bootstrap your project by simply typing swiftbase in you terminal

```bash
swiftbase
```

## Authentication

When Swiftbase creating a project that includes SwiftStore the cli will print your authentication token that you will need to interact with the database.

N.B The authentication token will only be printed once in the terminal so make sure to copy and store it somewhere safe.

## Initialize swiftstore sdk

```javascript
const { SwiftbaseDb } = require("swiftbase_db_sdk");
```

Once you have imported the sdk you will need to create a new instance of SwiftbaseDb and it takes your authentication token in the constructor. After you have created your database connector you can start performing CRUD operations immediately.

```javascript
const dao = new SwiftbaseDb("authentication_token");
```

## Perform CRUD operations

Once the DAO is created, you can start interacting with the Swiftbase DB service:

- **Insert a record:**

```javascript
dao.model("my_model").insert({
  name: "John Doe",
  email: "john.doe@example.com",
});
```

If the model does not exist, it will be created automatically.

- **Find all records:**

```javascript
const records = await dao.model("my_model").find();
```

- **Find a specific record:**

```javascript
const record = await dao
  .model("my_model")
  .find({ email: "john.doe@example.com" });
```

- **Update a record:**

```javascript
dao
  .model("my_model")
  .update({
    name: "Jane Doe",
  })
  .where({ email: "john.doe@example.com" });
```

- **Delete a record:**

```javascript
dao.model("my_model").delete({ email: "john.doe@example.com" });
```

**Full code**

Here is the entire code:

```javascript
const { SwiftbaseDb } = require("swiftbase_db_sdk");
const dao = new SwiftbaseDb("authentication_token");

// Insert a record
const dao = new SwiftbaseDb("YOUR_AUTH_TOKEN");
dao.model("my_model").insert({
  name: "John Doe",
  email: "john.doe@example.com",
});

// Find all records
const records = await dao.model("my_model").find();

// Find a specific record
const record = await dao
  .model("my_model")
  .find({ email: "john.doe@example.com" });

// Update a record
dao
  .model("my_model")
  .update({
    name: "Jane Doe",
  })
  .where({ email: "john.doe@example.com" });

// Delete a record
dao.model("my_model").delete({ email: "john.doe@example.com" });
```

## Security

Inorder to prevent unauthorized access to your database make sure to save your authentication token in a private location. When in development it is good to utilize environment variables to store your authentication token and make sure to not accidentally publish your code to github with your authentication token in your codebase.
