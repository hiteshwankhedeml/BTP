# Implementation Steps

* Add a new service instance - Authorization and Trust Management
* While creating instance, we need to provide json with app name, scope, redirect url etc
* Bind service with the app
* Add it as required resource in manifest
* We also need to add code in our app in SecurityConfiguration.java ⇒ for springboot spplication
* The role and rolecollection which we have added in security configuration file, will be created in BTP
* This can now we assigned to the user
* In xsuaa service we will get url and client secret to generate JWT token
*
