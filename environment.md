# 🟢 Environment

* Constitute the actual platform as a service offering of BTP that allows for the development and administration of business applications
* <mark style="color:$danger;background-color:purple;">**At sub account level**</mark>
* 3 diff environment, some still have Neo but its no longer used



* <mark style="color:$danger;background-color:purple;">**Cloud Foundry:**</mark>
  * <mark style="color:$danger;background-color:purple;">**Supports runtime for python, java, node, c etc**</mark>
  * <mark style="color:$danger;background-color:purple;">**Provides runtime called buildpack for running apps**</mark>
  * <mark style="color:$danger;background-color:purple;">**Its controlled by cf, we just use it**</mark>
* **ABAP Environment:**
  * Only ABAP
  * Done using RAP
* **Kyma Environment ⇒ Powered by google k8s:**
  * Supports runtime for python, java, node, c etc
  * We can decide runtime
  * We can package application and runtime together ⇒ This is called docker container
  * Used for high avalilability applications with billions of users



**60-80%** application built using CF

