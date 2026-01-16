# 🟢 Authentication vs Authorization(Security)

* **Authentication:**&#x20;
  * Check valid user
  * Enforced by login screen
* **Authorization:**&#x20;
  * It controls what part of application, which activities, which data allowed to be accessed by the user
  * It controls the level of permission in app



<mark style="color:purple;background-color:purple;">**SAP BTP has XSUAAA - Extended service, user account and administration)**</mark>

* <mark style="color:purple;background-color:purple;">In-build application in BTP</mark>
* <mark style="color:purple;background-color:purple;">Responsible to control the user account and authorization</mark>
* <mark style="color:purple;background-color:purple;">It manages our application security as well</mark>
* <mark style="color:purple;background-color:purple;">As a developer we need to decide what roles and levels we need in our app with scopes(View, edit, delete)</mark>
* <mark style="color:purple;background-color:purple;">We need to define the scopes, role templates, and role collections in BTP to control the permissions</mark>
* <mark style="color:purple;background-color:purple;">These definitions are specific to application, which a developer decides to control permissions</mark>
* <mark style="color:purple;background-color:purple;">This is done using xs-security.json to define our scope, role templates and collections</mark>
* <mark style="color:purple;background-color:purple;">XSUAA also has a trusted relation with IDP</mark>
* <mark style="color:purple;background-color:purple;">We need to create an instance of XSUAA service to communicate between our app and this XSUAA component</mark>
* <mark style="color:purple;background-color:purple;">XSUAA components issues JWT token to CF router which let user access our app using permissions</mark>

