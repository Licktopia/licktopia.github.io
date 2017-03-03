# Retrieving User Information
### Returning a JSON object

Finally, we are ready to retrieve information about the user from Spotify with our access token. We will do this with our 
POST request passing in the authorization options from above.

    request.post(authOptions, function(error, response, body) {
          if (!error && response.statusCode === 200) {

            var access_token = body.access_token,
            refresh_token = body.refresh_token;

            var options = {
            url: 'https://api.spotify.com/v1/me',
            headers: { 'Authorization': 'Bearer ' + access_token },
            json: true
        };
        
The returned JSON object may be parsed to display information about the user like in the image below.

![Profile](\images\Profile.jpg)

Finally, we can change our post request to get any kind of information we want within the limits of the scope we have requested and been granted.

![Endpoints](\images\Endpoints.png)

Here we will request the user playlist by changing the options url to:

    var options = {
          url: 'https://api.spotify.com/v1/playlists',
          headers: { 'Authorization': 'Bearer ' + access_token },
          json: true
        };

We will make a GET request and log the contents of the body to the log. This should contain our playlists.

    request.get(options, function(error, response, body) {
          console.log(body);
        });

![Contents](\images\Contents.jpg]

Here we have completed what we set out to do, get authorization from the user and return a list of their playlists.

<button onclick="location.href = 'https://licktopia.github.io/page5';" id="myButton" class="float-left submit-button" >Back</button>
  
        

        
