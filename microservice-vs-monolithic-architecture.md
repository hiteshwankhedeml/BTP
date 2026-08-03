# 🟢 Microservice vs Monolithic Architecture

* In BTP we can build microservices using different languages
* **Monolithic:**&#x20;
  * UI + Application + DB APIs inside single packet
  * Easy to build
  * When one thing breaks everything breaks
  * <mark style="color:purple;background-color:purple;">**Cannot scale a single component, everything will have to be scaled**</mark>
* **Microservice:**
  * All the components are broken into smaller micro units
  * <mark style="color:$danger;background-color:purple;">**A micro service is represented like a polygon in diagram**</mark>
  * <mark style="color:purple;background-color:purple;">**Each micro service can scale up individually**</mark>
  * Application is safe even if one part breaks down
  * We have choice of technology
* There are also reusable micro service provided by SAP ⇒ Like connectivity, hana, destination
*
