[Back to main page](README.md)

# Installing with the Postman Desktop App

This is the recommended installation option because it is the fastest to set up and doesn’t require changes on your Salesforce org.

- [Install the Postman App](#install-the-postman-app)
- [Fork the Collection](#fork-the-collection)
- [Configure the Collection](#configure-the-collection)
- [Authenticate with Salesforce](#authenticate-with-salesforce)
- [Execute a Request](#execute-a-request)


## Install the Postman App

Download and install the Postman app from [this link](https://www.postman.com/downloads).


### Fork the Collection

1. Using a browser, [sign up/in to Postman](https://identity.getpostman.com/login).
2. Navigate to [this link](https://www.postman.com/salesforce-developers/workspace/salesforce-developers/collection/12721794-67cb9baa-e0da-4986-957e-88d8734647e2/fork) to create a fork of the collection.
3. Enter a label for your fork (e.g.: “My fork”).
4. Select a workspace (the default “My Workspace” workspace is fine).
5. Click **Fork Collection**.
6. Close the browser tab. We'll continue the installation on the Postman app.


## Configure the Collection

1. Open the Postman desktop app and sign in with your account. This synchronizes the collection you just forked in the web UI into the app.

    ![Collection fork synchronized in app screenshot](doc-gfx/app/collection-fork-synchronized.png)

1. Move your mouse over the “Salesforce APIs” collection, click on the “three dots” icon next to it and select **Edit** from the menu.

    ![Edit collection screenshot](doc-gfx/app/edit-collection.png)

1. Open the **Variables** tab.
1. If needed, update the `CURRENT VALUE` of the `url` variable with:

    - `https://test.salesforce.com` for sandboxes or Scratch orgs.
    - `https://login.salesforce.com` for production, Trailhead Playground and Developer Edition orgs.
    - your custom My Domain URL.

1. Click **Update**.


## Authenticate with Salesforce

You'll need to authenticate with Salesforce to access the APIs. Doing so grants you an access token that is valid for a certain duration.

Repeat this step whenever your access token expires.

1. Move your mouse over the “Salesforce APIs” collection, click on the “three dots” icon next to it and select **Edit** from the menu.
1. Open the **Authorization** tab.
1. Click **Get New Access Token**. This opens a browser tab with the Salesforce login screen.
1. Log in to your Salesforce org.
1. Click **Allow** to grant access to "Salesforce APIs Collection for Postman" to your org.

    ![Grant access screenshot](doc-gfx/salesforce/grant-access.png)

    At this point, if your environment is correctly set up, you should see a success message and you should be redirected to the Postman app.

1. Copy the value of the `instance_url` field from the token details view.

    ![Grant access screenshot](doc-gfx/app/manage-token.png)

1. Click **Use Token**.
1. Open the **Variables** tab.
1. Update the `CURRENT VALUE` of the `_endpoint` variable with the value that you just copied from the `instance_url` field in the access token details.
1. Click **Update**.


## Execute a Request

1. Expand the collection and select the `REST > Limits` request.
1. Click `Send`.

At this point, if your environment is correctly set up, you should see a `200 OK` status. This means that you have successfully authenticated with Salesforce and that you can now use the other collection’s requests.

![Authenticate screenshot](doc-gfx/app/limits-status-200.png)

See [additional documentation](README.md#additional-documentation) for more information on how to keep the collection up to date and work with multiple Salesforce orgs.


[Back to main page](README.md)
