# Authentication bypass via OAuth implicit flow

## Description
This lab uses an OAuth service to allow users to log in with their social media account. Flawed validation by the client application makes it possible for an attacker to log in to other users' accounts without knowing their password.

To solve the lab, log in to Carlos's account. His email address is carlos@carlos-montoya.net.

You can log in with your own social media account using the following credentials: wiener:peter.

## Solution
1. Click "My account" and complete the OAuth login process, you will be redirected back to the blog website.
2. In HTTP history, the requests starts from the authorization request `GET /auth?client_id=[...].`
![Picture](lab01-01.png)
3. The client application (the blog website) receives some basic information about the user from the OAuth service. It then logs the user in by sending a `POST` request containing this information to its own `/authenticate` endpoint, along with the `access token`.
4. Send the `POST /authenticate` request to Burp Repeater. In Repeater, change the **email address** to `carlos@carlos-montoya.net` and send the request. 
Observe that you do not encounter an error.
![Picture](lab01-02.png)
5. Right-click on the POST request and select "Request in browser" > "In original session". Copy this URL and visit it in the browser. You are logged in as Carlos and the lab is solved.
![Picture](lab01-03.png)
## Question


## Conclusion