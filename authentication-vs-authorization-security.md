# Authentication vs Authorization(Security)

* **Authentication:**&#x20;
  * Check valid user
  * Enforced by login screen
* **Authorization:**&#x20;
  * It controls what part of application, which activities, which data allowed to be accessed by the user
  * It controls the level of permission in app



**SAP BTP has XSUAAA - Extended service, user account and administration)**

* In-build application in BTP
* Responsible to control the user account and authorization
* It manages our application security as well
* As a developer we need to decide what roles and levels we need in our app with scopes(View, edit, delete)
* We need to define the scopes, role templates, and role collections in BTP to control the permissions
* These definitions are specific to application, which a developer decides to control permissions
* This is done using xs-security.json to define our scope, role templates and collections
* XSUAA also has a trusted relation with IDP
* We need to create an instance of XSUAA service to communicate between our app and this XSUAA component
* XSUAA components issues JWT token to CF router which let user access our app using permissions

