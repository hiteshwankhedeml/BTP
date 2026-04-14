# 🔴 Implement XSUAA

* <mark style="color:$danger;background-color:purple;">**Create instance of xsuaa**</mark>&#x20;
* <mark style="color:$danger;background-color:purple;">**In our application, bind this application by adding in manifest.yml**</mark>
* <mark style="color:$danger;background-color:purple;">**In xs-security.json, we add details for scope, role, role templates,**</mark>&#x20;
  * cf update-service xsuaa\_api -c xs-security.json
  * cf create-service xsuaa application xsuaa\_api -c xs-security.json
* <mark style="color:$danger;background-color:purple;">**Based on this role and role collections will get created**</mark>
* <mark style="color:$danger;background-color:purple;">**Inside the application, we need to verify token as below**</mark>
  * Load the xsuaa service which is binded to it
  * <mark style="color:$danger;background-color:purple;">**Get the bearer token passed**</mark>
  * <mark style="color:$danger;background-color:purple;">**Decode the token**</mark>
  * <mark style="color:$danger;background-color:purple;">**Get the security content**</mark>
  * <mark style="color:$danger;background-color:purple;">**Validate the scope**</mark>
* Generating tokens:
  * From the xsuaa we get the url, clientid and clientsecret — using which we can generate the bearer token
  * curl --location 'https://5c1782d0trial.authentication.us10.hana.ondemand.com/oauth/token'\
    \--header 'Content-Type: application/x-www-form-urlencoded'\
    \--data-urlencode 'grant\_type=client\_credentials'\
    \--data-urlencode 'client\_id=sb-hello-app\_2!t624561'\
    \--data-urlencode 'client\_secret=9a564e73-0480-4acb-a6d3-da908873436b$3Yb0DfnbNwj7JHGPOjmcuuZOknA6ZUWQ8dgQz\_xYCKQ='
  * <mark style="color:$danger;">**curl --location 'https://5c1782d0trial.authentication.us10.hana.ondemand.com/oauth/token'**</mark>\ <mark style="color:$danger;">**--header 'Content-Type: application/x-www-form-urlencoded'**</mark>\ <mark style="color:$danger;">**--header 'Authorization: Basic c2ItaGVsbG8tYXBwXzIhdDYyNDU2MTo5YTU2NGU3My0wNDgwLTRhY2ItYTZkMy1kYTkwODg3MzQzNmIkM1liMERmbmJOd2o3SkhHUE9qbWN1dVpPa25BNlpVV1E4ZGdRel94WUNLUT0='**</mark>\ <mark style="color:$danger;">**--data-urlencode 'grant\_type=password'**</mark>\ <mark style="color:$danger;">**--data-urlencode 'username=hiteshbwankhede@gmail.com'**</mark>\ <mark style="color:$danger;">**--data-urlencode 'password=Hitesh@01'**</mark>
