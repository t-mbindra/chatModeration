# Chat Bot with Moderation Control

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Interacting with the bot](#interacting-with-the-bot)
- [Setting up the app](#setting-up-the-app-in-VS-Code)
- [Setting up the app in Github Codespaces](#setting-up-the-app-in-github-codespaces)

<!-- /code_chunk_output -->

## Interacting with the bot

You can interact with the bot by messaging it.

## Setting up the app in VS Code
1. Ensure you have [Python](https://www.python.org/downloads/), [Rust](https://www.rust-lang.org/tools/install) and [Node.js](https://nodejs.org/en/download/package-manager) installed.
2. Ensure you have downloaded and installed [Visual Studio Code](https://code.visualstudio.com/docs/setup/setup-overview).
3. Install the [Teams Toolkit extension](https://marketplace.visualstudio.com/items?itemName=TeamsDevApp.ms-teams-vscode-extension) and the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python).
4. Install [Poetry](https://python-poetry.org/docs/#installation).
5.  Clone the repository:
    ```bash
    git clone https://github.com/t-mbindra/echobot.git
    ```
6. Open this project in VS Code.
7. Using the Teams toolkit extension, sign in with your Microsoft 365 account where you have permissions to upload custom apps. Also sign into your Azure account.
8. Run the following command to install dependencies:
    ```bash
    poetry install
    ```
9. Run the following command to build this sample:
      ```bash
      poetry build
      ```
10. Duplicate the ```sample.env``` file and rename it as ```.env```. If you are using OpenAI then only populate the ```OPENAI_KEY, OPENAI_MODEL``` variable. Otherwise if you are using AzureOpenAI then only populate the ```AZURE_OPENAI_KEY, AZURE_OPENAI_MODEL, AZURE_OPENAI_ENDPOINT, AZURE_CONTENT_SAFETY_ENDPOINT, AZURE_CONTENT_SAFETY_KEY``` variables.
11. Press **Ctrl+Shift+P** to view the Command Palette. Select the command **Python: Select Interpretor** and choose ```'.venv': (Poetry)```.

#### If you want to debug locally, continue to step 12, else skip to step 14.
12. Press **Ctrl+Shift+D** to open the **Run and Debug** menu. Select **Debug (Edge)** or **Debug(Chrome)** and press **F5** or click on the play button.
13. In the browser that launches, select the **Add** button to install the app to Teams.

#### Continue here to deploy the app on Azure.
14. Using the Teams Toolkit Extension tab, click on **Provision** under lifecycle. Select relevant subscription and resource group when prompted.
15. Using the Teams Toolkit Extension tab, click on **Deploy** under lifecycle.
16. Go to your Teams app and click on the **App** icon.
17. Select **Manage your apps** followed by **Upload an app**.
18. Select **Upload a custom app** and open the ```appPackage/build/appPackage.dev.zip``` zip file from the project folder.
19. Click on **Add** when prompted. Select where you want to use the app.
    
> If you do not have permission to upload custom apps (sideloading), Teams Toolkit will recommend creating and using a Microsoft 365 Developer Program account - a free program to get your own dev environment sandbox that includes Teams.

## Setting up the app in Github Codespaces

1. Click on **Use this template > Open in a codebase**.
2. Wait for the codespace to be setup, it may take a few minutes.
3. Using the Teams Toolkit extension, sign in with your Microsoft 365 account where you have permissions to upload custom apps. Also sign into your Azure account.
4. Duplicate the ```sample.env``` file and rename it as ```.env```. If you are using OpenAI then only populate the ```OPENAI_KEY, OPENAI_MODEL``` variable. Otherwise if you are using AzureOpenAI then only populate the ```AZURE_OPENAI_KEY, AZURE_OPENAI_MODEL, AZURE_OPENAI_ENDPOINT, AZURE_CONTENT_SAFETY_ENDPOINT, AZURE_CONTENT_SAFETY_KEY``` variables.
   
#### If you want to debug locally, continue to step 5, else skip to step 8.
5. Press **Ctrl+Shift+D** to open the **Run and Debug** menu. Select **Debug** and press **F5** or click on the play button
6. Go to the link (https://dev.botframework.com/bots?id=...) from the Output console.
7. Click on **Microsoft Teams**. Use the web app or launch the Teams app to use the bot.

#### Continue here to deploy the app on Azure.
8. Using the Teams Toolkit Extension tab, click on **Provision** under lifecycle. Select relevant subscription and resource group when prompted.
9. Using the Teams Toolkit Extension tab, click on **Deploy** under lifecycle.
10. Download the zip file ```appPackage/build/appPackage.dev.zip```.
11. Go to your Teams app and click on the **App** icon.
12. Select **Manage your apps** followed by **Upload an app**. Select **Upload a custom app** and open the downloaded zip file.
13. Click on **Add** when prompted. Select where you want to use the app.
    
> If you do not have permission to upload custom apps (sideloading), Teams Toolkit will recommend creating and using a Microsoft 365 Developer Program account - a free program to get your own dev environment sandbox that includes Teams.
