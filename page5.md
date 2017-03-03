# Gaining the Access Token
### POST Request to get the token

Spotify will then go back to the redirect URI and make a post to use the authorization code in order to get an access token. 
This is done via a POST request to the address [token list]:https://accounts.spotify.com/api/token


The POST request will contain the following paramenters in it’s body. The “code” contains the authorization code from the authorization 
GET call and “Grant_type” contains the value “authorization_code.” 

   
The authorization header parameter is an encoded string and contains the client ID and secret key.

    var authOptions = {
      url: 'https://accounts.spotify.com/api/token',
      form: {
        code: code,
        redirect_uri: redirect_uri,
        grant_type: 'authorization_code'
      },
      headers: {
        'Authorization': 'Basic ' + (new Buffer(client_id + ':' + client_secret).toString('base64'))
      },
      json: true
    };


If the request is successful and status code 200 is returned then a JSON object is returned

Spotify returns a JSON object like this:

   "access_token": "BQDF8W4E7jrt2Ntu72tCG7wAg",
   "token_type": "Bearer",
   "scope": "user-read-private user-read-email",
   "expires_in": 3600,
   "refresh_token": "AQCTCJlzFXWGJ0sl5DIfsRUIBVbolZxDhTfc"

The most important part here is the access token which we can now use to make requests to the Spotify Web API for further information. It’s also important to not e that the token expires in 1 hour, and the refresh token will be need to get a new token later.

<button onclick="location.href = 'https://licktopia.github.io/page4';" id="myButton" class="float-left submit-button" >Back</button>
<button onclick="location.href = 'https://licktopia.github.io/page6';" id="myButton" class="float-right submit-button" >Next</button>

