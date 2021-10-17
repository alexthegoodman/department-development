# facebook api
* The Consumer makes a request to the Service Provider authorization endpoint to authorize the user.
* The Service Provider authenticates the user and prompts them whether to authorize the Consumer to access their information.
* If the user authorizes the Consumer, the Service Provider redirects back to the redirect URI on the Consumer’s website with a temporary access code.
* The Consumer calls the token endpoint on the Service Provider website to exchange the code for a more permanent access token.
* The Service Provider grants an access token which can be used to authenticate subsequent requests to protected resources

#department/development/codesnippets