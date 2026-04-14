---
hidden: true
---

# ✈️ Implementation Steps

* <mark style="color:purple;background-color:purple;">**Add a new service instance - Authorization and Trust Management**</mark>
* <mark style="color:purple;background-color:purple;">**While creating instance, we need to provide json with app name, scope, redirect url etc**</mark>
* <mark style="color:purple;background-color:purple;">**Bind service with the app**</mark>
* <mark style="color:purple;background-color:purple;">**Add it as required resource in manifest**</mark>
* We also need to add code in our app in SecurityConfiguration.java ⇒ for springboot spplication
* The role and rolecollection which we have added in security configuration file, will be created in BTP
* This can now we assigned to the user
* <mark style="color:purple;background-color:purple;">**In xsuaa service we will get url and client secret to generate JWT token**</mark>
