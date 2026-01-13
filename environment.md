# Environment

* Constitute the actual platform as a service offering of BTP that allows for the development and administration of business applications
* At sub account level
* 3 diff environment, some still have Neo but its no longer used



* **Cloud Foundry:**
  * Supports runtime for python, java, node, c etc
  * Provides runtime called buildpack for running apps
  * Its controlled by cf, we just use it
* **ABAP Environment:**
  * Only ABAP
  * Done using RAP
* **Kyma Environment ⇒ Powered by google k8s:**
  * Supports runtime for python, java, node, c etc
  * We can decide runtime
  * We can package application and runtime together ⇒ This is called docker container
  * Used for high avalilability applications with billions of users



**60-80%** application built using CF

