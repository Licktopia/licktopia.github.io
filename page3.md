# User Authorization
### Asking Permission

Now that we have the application all set up, we can proceed to get authorization from the user to allow our app to connect to their
Spotify account. First we need to make a page that asks the user permission access their user data from Spotify. For brevity we will 
omit the HTML code, but examples can be found at <https://developer.spotify.com>.

![GrantAccess](/images/grantAccess.jpg)

The authorization process has several steps and several pieces information that need to be sent to Spotify.

First we will put our client id and secret in variables, as well as the callback redirect.

    var client_id = 'ddeb4e3b2e3e465fa67505e22803f9c4'; // Your client id
    var client_secret = '87dfbe77d1414e8280a75ed6bb6a8565'; // Your secret
    var redirect_uri = 'http://localhost:8888/callback'; // Your redirect uri


We will begin by making a GET request to the authorization endpoint. 

The entire block of code for this authorization request will look like this:


    app.get('/login', function(req, res) {

      var state = generateRandomString(16);
      res.cookie(stateKey, state);

      var scope = 'user-read-private user-read-email';
      res.redirect('https://accounts.spotify.com/authorize?' +
        querystring.stringify({
          response_type: 'code',
          client_id: client_id,
          scope: scope,
          redirect_uri: redirect_uri,
          state: state
        }));
    }

<button onclick="location.href = 'https://licktopia.github.io/page2';" id="myButton" class="float-left submit-button" >Back</button>
<button onclick="location.href = 'https://licktopia.github.io/page4';" id="myButton" class="float-right submit-button" >Next</button>

