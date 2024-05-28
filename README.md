---
page_type: sample
languages:
- php
products:
- azure
description: "This sample demonstrates a tiny Hello World PHP app for App Service."
urlFragment: php-docs-hello-world
---

Sure, let's break down each step of creating a PHP web app in Azure App Service:

1. **Get the sample repository**:
   - First, you need to clone a sample PHP application repository from GitHub to your local machine.
   - Open your terminal or command prompt and run the following commands:
     ```
     git clone https://github.com/abhixsh/ByteBash_PHP
     ```
   - These commands download the sample PHP application code to your machine and navigate to its directory.

2. **Deploy your application code to Azure**:
   - After you've cloned the sample repository and made any necessary changes to your application code, you need to deploy it to Azure.
   - Use Azure CLI (Command Line Interface) to deploy your code. In your terminal, run the following command:
     ```
     az webapp up --runtime "PHP:8.2" --os-type=linux
     ```
   - This command creates the necessary resources on Azure and deploys your application in a single step.
   - The `--runtime "PHP:8.2"` argument specifies the PHP version to use.
   - The `--os-type=linux` argument specifies the operating system for the App Service.
   - Optionally, you can provide a name for your app using `--name <app-name>`. If you don't, a name will be generated automatically.
   - Once the deployment is complete, you'll receive a message with the URL where your app is hosted on Azure.

3. **Update and redeploy the app**:
   - If you make changes to your application code later on, you can update and redeploy it to Azure.
   - Open the `index.php` file in your local PHP application directory using a text editor.
   - Make your desired changes to the code.
   - Save your changes and run the following command in your terminal to redeploy the updated app:
     ```
     az webapp up --runtime "PHP:8.2" --os-type=linux
     ```
   - This command will update your application on Azure with the changes you made locally.

4. **Manage your new Azure app**:
   - You can manage your deployed app through the Azure portal.
   - Go to the Azure portal and search for "App Services".
   - Select your Azure app from the list.
   - Here, you can perform various management tasks such as browsing your app, stopping or restarting it, and eventually deleting it when no longer needed.

5. **Clean up resources**:
   - When you're finished with your app and want to remove it from Azure, you can delete the associated resources.
   - Use Azure CLI to delete the resource group associated with your app. Run the following command in your terminal:
     ```
     az group delete --name myResourceGroup
     ```
   - This command removes all resources related to your app from Azure, helping you avoid extra charges and keeping your Azure subscription tidy.