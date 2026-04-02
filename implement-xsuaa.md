# Implement XSUAA

* Create instance of xsuaa&#x20;
* In our application, bind this application by adding in manifest.yml
* In xs-security, we add details for scope, role, role templates,&#x20;
  * cf update-service xsuaa\_api -c xs-security.json
  * cf create-service xsuaa application xsuaa\_api -c xs-security.json
* Based on this role and role collections will get created
* Inside the application, we need to verify token as below
  * Load the xsuaa service which is binded to it
  * Get the bearer token passed
  * Decode the token
  * Get the security content
  * Validate the scope
* Generating tokens:
  * From the xsuaa we get the url, clientid and clientsecret — using which we can generate the bearer token
  * curl --location 'https://5c1782d0trial.authentication.us10.hana.ondemand.com/oauth/token'\
    \--header 'Content-Type: application/x-www-form-urlencoded'\
    \--data-urlencode 'grant\_type=client\_credentials'\
    \--data-urlencode 'client\_id=sb-hello-app\_2!t624561'\
    \--data-urlencode 'client\_secret=9a564e73-0480-4acb-a6d3-da908873436b$3Yb0DfnbNwj7JHGPOjmcuuZOknA6ZUWQ8dgQz\_xYCKQ='
  * curl --location 'https://5c1782d0trial.authentication.us10.hana.ondemand.com/oauth/token'\
    \--header 'Content-Type: application/x-www-form-urlencoded'\
    \--header 'Authorization: Basic c2ItaGVsbG8tYXBwXzIhdDYyNDU2MTo5YTU2NGU3My0wNDgwLTRhY2ItYTZkMy1kYTkwODg3MzQzNmIkM1liMERmbmJOd2o3SkhHUE9qbWN1dVpPa25BNlpVV1E4ZGdRel94WUNLUT0='\
    \--data-urlencode 'grant\_type=password'\
    \--data-urlencode 'username=hiteshbwankhede@gmail.com'\
    \--data-urlencode 'password=Hitesh@01'
