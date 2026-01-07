# Microservice vs Monolithic Architecture

* In BTP we can build microservices using different languages
* **Monolithic:**&#x20;
  * UI + Application + DB APIs inside single packet
  * Easy to build
  * When one thing breaks everything breaks
  * Cannot scale a single component, everything will have to be scaled
* **Microservice:**
  * All the components are broken into smaller micro units
  * <mark style="color:$danger;">**A micro service is represented like a polygon in diagram**</mark>
  * Each micro service can scale up individually
  * Application is safe even if one part breaks down
  * We have choice of technology
* There are also reusable micro service provided by SAP ⇒ Like connectivity, hana, destination
*
