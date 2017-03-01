# Getting Started
### Gaining User Account Access

1. First we need to have an active user. For the purposes of this tutorial, we will assume that you have already signed up for and downloaded Spotify.
2. Navigate first to https://developer.spotify.com/ and click on MyApps. Once there, click on the "Create an App" button on the top right. In this case we can see we have created a project called "290 Project" as illustrated below.

  ![CreateApp](/images/Getapp.jpg)

3. Once the app is been created, click on it. You will be taken to the project settings page. Here we can edit the Application name and description. More importantly though, we will be given a Client ID and a Client Secret. Make sure to copy these into a text file because we will be needing them later.  In this case our client ID is ddeb4e3b2e3e465fa67505e22803f9c4  Typically this would not be made public, but for now it's ok for the purposes of this tutorial. Lastly, we need to enter a Redirect URI. This is the address that the Spotify Accounts service will call once the user authentication is finished.  For now, we will use the address http://localhost:8888/callback as illustrated below and highlighted in yellow.


  ![CreateApp](/images/ClientID.jpg)

4. Lastly, don't forget to click Save or else your settings will not stick.

