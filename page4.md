# User Authorization
### Asking Permission

Now that we have the application all set up, we can proceed to get authorization from the user to allow our app to connect to their
Spotify account. First we need to make a page that asks the user permission access their user data from Spotify. For brevity we will 
omit the HTML code, but examples can be found at https://developer.spotify.com.

![GrantAccess](/images/grantAccess.jpg)

#### Scopes

We need to take a moment to talk about scopes. Scopes are what determine how much information we are authorizing Spotify to grant to our app. For example, getting a users birthday and modifying a user’s playlist require different levels of access. The list of available scopes may be found here https://developer.spotify.com/web-api/using-scopes/

For now we are interested in the area highlighted in yellow, accessing a private playlist.

    var scope = 'user-read-private user-read-email';


In the code from the previous page, we have requested authorization, and Spotify will ask the user for the permission specified in the scope.


![GrantAccess](/images/access.jpg)

![GrantAccess](/images/login.jpg)

Once authorization is granted, or there is some error with the request, you have retrieved the authorization code in the response query string here:

    var code = req.query.code || null;


a users birthday and modifying a user’s playlist require different levels of access. The list of available scopes may be found here https://developer.spotify.com/web-api/using-scopes/

For now we are interested in the area highlighted in yellow, accessing a private playlist.



     var code = req.query.code || null;
     var code = req.query.code || null;

<button onclick="location.href = 'https://licktopia.github.io/page3';" id="myButton" class="float-left submit-button" >Back</button>
<button onclick="location.href = 'https://licktopia.github.io/page5';" id="myButton" class="float-right submit-button" >Next</button>
