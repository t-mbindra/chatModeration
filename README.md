# Chat Bot with Moderation Control

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Interacting with the bot](#interacting-with-the-bot)
- [Setting up the app in Github Codespaces](#setting-up-the-app-in-github-codespaces)

<!-- /code_chunk_output -->

## Interacting with the bot

You can interact with the bot by messaging it.

## Setting up the app in Github Codespaces

1. Click on **Use this template > Open in a codebase**.
2. Wait for the codespace to be setup, it may take a few minutes.
3. Using the Teams Toolkit extension, sign in with your Microsoft 365 account where you have permissions to upload custom apps.
4. Duplicate the ```sample.env``` file and rename it as ```.env```. If you are using OpenAI then only populate the ```OPENAI_KEY, OPENAI_MODEL``` variable. Otherwise if you are using AzureOpenAI then only populate the ```AZURE_OPENAI_KEY, AZURE_OPENAI_MODEL, AZURE_OPENAI_ENDPOINT, AZURE_CONTENT_SAFETY_ENDPOINT, AZURE_CONTENT_SAFETY_KEY``` variables.
   
#### If you want to debug locally, continue to step 5, else skip to step 8.
5. Press **Ctrl+Shift+D** to open the **Run and Debug** menu. Select **Debug** and press **F5** or click on the play button
6. Go to the link (https://dev.botframework.com/bots?id=...) from the Output console.
7. Click on **Microsoft Teams**. Use the web app or launch the Teams app to use the bot.

#### Continue here to deploy the app on Azure.
8. Using the Teams Toolkit extension, sign into your Azure account.
9. Using the Teams Toolkit Extension tab, click on **Provision** under lifecycle. Select relevant subscription and resource group when prompted.
10. Using the Teams Toolkit Extension tab, click on **Deploy** under lifecycle.
11. Download the zip file ```appPackage/build/appPackage.dev.zip```.
12. Go to your Teams app and click on the **App** icon.
13. Select **Manage your apps** followed by **Upload an app**. Select **Upload a custom app** and open the downloaded zip file.
14. Click on **Add** when prompted. Select where you want to use the app.
    
> If you do not have permission to upload custom apps (sideloading), Teams Toolkit will recommend creating and using a Microsoft 365 Developer Program account - a free program to get your own dev environment sandbox that includes Teams.
