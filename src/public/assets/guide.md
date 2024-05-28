# **Guide**
1. **Add the bot to your server**: In order to get started you need to add the bot to your server. You can do this by clicking the **Servers** button in the top right. After you have added the bot to your server you can select that server in order to configure it.
2. **Tokens**: In order to use commands and get notifications from services like GitHub, Trello and Google Calendar you need to register tokens. In the sidebar to the left you can register tokens by clicking the service you want to register tokens for, click the gear, fill in the tokens for that service and hit apply. **Get GitHub tokens**, **Get Google Calendar tokens** and **Get Trello tokens** later in this guide can help you find the tokens needed.
3. **Service settigns**: You can configure the bot for GitHub, Trello and Google Calendar by going to their tab. Here you can configure in what channel notifications should appear in by modifying **Discord Channel**. You can modify tokens by clicking the gear. You can modify what notifications and what commands which should be enabled, by clicking the plus sign for enableing and trash icon for removeal.


# **Get GitHub tokens**
The GitHub tokens are: **Access token** and **Organization ID**
1. The **Organization ID** Is the title of the organization
2. In GitHub go to [Token settings](https://github.com/settings/tokens)
3. Click **Generate new token**, confirm access and fill in the following scopes:
    -  **repo**
        -  **repo:status**
        -  **repo_deployment**
        -  **public_repo**
      - **admin:org** (all)
        -  **write:org**
        -  **read:org**
        -  **manage_runners:org**
      - **notifications**
      - **user**
        -  **read:user**
      - **delete_repo**
      - **write:discussion** (all)
        -  **read:discussion**
      - **project** (all)
        - **read:project**
4. Press **Generate token**
5. Save **Access token**

# **Get Google Calendar tokens**
The Google Calendar tokens are: **Client ID**, **Client secret**, **Refresh token** and **Calendar ID**
1. [Create a Google Cloud Project](https://console.cloud.google.com)
2. [Enable the Google Calendar API](https://console.cloud.google.com/apis/library)
    - make sure the correct project is selected in the top-left drop-down menu
    - In the search bar search for: **Google Calendar API**
        - Click **Enable**
4. [Create OAuth](https://console.cloud.google.com/apis/credentials/consent)
    - For **User Type** choose **External**
    - For **Test users** add yourself
    - Insert the required values
5. [Create credentials](https://console.cloud.google.com/apis/credentials)
    - Click **Create Credentials > OAuth client ID**
    - For **Applicataion type** choose **Web application** and give it a name
    - For **Authorized redirect URIs** click **ADD URI** and insert `https://developers.google.com/oauthplayground`
    - Save the **Client ID** and **Client secret**
6. [Generate your token](https://developers.google.com/oauthplayground)
    - Click the cogwheel, **OAuth 2.0 Configuration** in the top right
        - Click the checkbox **Use your own OAuth credentials**
        - Insert the **Client ID** and **Client secret** from step 3.
    - Go to [Google Cloud Project](https://console.cloud.google.com) and look for **Google Calendar API v3** and select **https://www.googleapis.com/auth/calendar.events**
    - Click **Authorize APIs** and select your account in the pop-up window
        - Click **Continue** and allow access for the two properties, then click **Continue** again
    - In [OAuth](https://console.cloud.google.com/apis/credentials/consent) click **Exchange authorization code for tokens** and save the **Refresh token**
7. Get [**Calendar ID**](https://calendar.google.com/calendar/)
    - Press the **triple vertical dots** > **Settings**
    - Scroll down until **Calendar ID** is located

# **Get Trello tokens**
The Trello tokens are: **API key**, **API Token** and **Organization ID**
1. [Create](https://id.atlassian.com/signup)  or [login](https://id.atlassian.com/login) to your Trello account
2. Create a **Trello board** and take notice of what **workspace** it is located in
3. Access your API key page in the [Power-Up Admin Portal](https://trello.com/power-ups/admin/)
4. Press the **New** button (If you already have created a power-up, you can skip this and the next step)
5. Fill the fields
    - **Integration name**, give it a fitting name 
    - **Workspace**, select the workspace you want to connect
    - **Email**, for Trello to reach you regarding the integration we are creating
    - **Support contact**, an email that will work as a contact for support
    - **Author**, either the name of the company or personal name
6. Select the **Workspace** the integration is meant for
    - Then select **API Key**
    - Fetch **API Key**
    - To the right of the copied **API Key** there is a link on the text saying **Token**
    - Then press **Allow** and fetch the **API Token**
7. Getting the **Organization ID** is done by accessing a board within the organization
    - Then access the sharing option by clicking the **three horizontal dots** > **Print, export and share**
    - Press **Export as JSON**
    - Use the search function **Ctrl + F** and search for "idOrganization" and fetch it

