# Chat Bot with Moderation Control

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Interacting with the bot](#interacting-with-the-bot)
- [Setting up the app](#setting-up-the-app)
- [Setting up the app in Github Codespaces](#setting-up-the-app-in-github-codespaces)

<!-- /code_chunk_output -->

## Interacting with the bot

You can interact with the bot by messaging it.

## Setting up the app  
1. Ensure you have [Python](https://www.python.org/downloads/), [Rust](https://www.rust-lang.org/tools/install) and [Node.js](https://nodejs.org/en/download/package-manager) installed.
2. Ensure you have downloaded and installed [Visual Studio Code](https://code.visualstudio.com/docs/setup/setup-overview).
3. Install the [Teams Toolkit extension](https://marketplace.visualstudio.com/items?itemName=TeamsDevApp.ms-teams-vscode-extension).
4. Install the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python).
5. Install [Poetry](https://python-poetry.org/docs/#installation).
6.  Clone the repository:
    ```bash
    git clone https://github.com/t-mbindra/echobot.git
    ```
7. Open this project in VS Code.
8. Using the Teams toolkit extension, sign in with your Microsoft 365 account where you have permissions to upload custom apps.
9. Run the following command to install dependencies:
    ```bash
    poetry install
    ```
10. Run the following command to build this sample:
      ```bash
      poetry build
      ```
11. Duplicate the ```sample.env``` file and rename it as ```.env```. If you are using ```OpenAI``` then only populate the ```OPENAI_KEY variable. Otherwise if you are using ```AzureOpenAI``` then only populate the AZURE_OPENAI_KEY, AZURE_OPENAI_ENDPOINT variables.
12. Press **Ctrl+Shift+P** to view the Command Palette. Select the command **Python: Select Interpretor** and choose ```'.venv': (Poetry)```.
13. Press **Ctrl+Shift+D** top open the **Run and Debug** menu. Select **Debug (Edge)** or **Debug(Chrome)** and press **F5** or click on the play button.14. In the browser that launches, select the **Add** button to install the app to Teams.

> If you do not have permission to upload custom apps (sideloading), Teams Toolkit will recommend creating and using a Microsoft 365 Developer Program account - a free program to get your own dev environment sandbox that includes Teams.

## Setting up the app in Github Codespaces

1. Click on **Use this template > Open in a codebase**.
2. Wait for the codespace to be setup, it may take a few minutes.
3. Using the Teams Toolkit extension, sign in with your Microsoft 365 account where you have permissions to upload custom apps.
4.  Duplicate the ```sample.env``` file and rename it as ```.env```. If you are using ```OpenAI``` then only populate the ```OPENAI_KEY variable. Otherwise if you are using ```AzureOpenAI``` then only populate the AZURE_OPENAI_KEY, AZURE_OPENAI_ENDPOINT variables.
5. Press **Ctrl+Shift+D**. Select **Debug** and press **F5** or click on the play button
6. Go to the link (https://dev.botframework.com/bots?id=...) from the Output console.
7. Click on **Microsoft Teams**. Use the web app or launch the Teams app to use the bot.

> If you do not have permission to upload custom apps (sideloading), Teams Toolkit will recommend creating and using a Microsoft 365 Developer Program account - a free program to get your own dev environment sandbox that includes Teams.
