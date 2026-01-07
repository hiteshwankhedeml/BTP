# Organization of BTP CF

* **Global Account:**
  * Used for billing purpose
  * Representation of a customer
* **Entitlement:**
  * Services which the customer opted for
* **Sub Account:**
  * Organization by the customer how they want to split their services and development teams
  * Sub account - Europe Region
  * Sub account - HR Team
  * For sub account ⇒ we can select sub region, infra provider
* **Space:**
  * It is the compute unit in which we actually deploy and run our application
  * It constructs our landscape for development
  * Dev | Quality | Production
  * Space will be assigned with Quota on how much it can use
* **Application:**
  * Micro application will be deployed in space
* **Directories:**
  * Additional grouping of sub account to manage policies easily
* We do assign entitlement which we got from global to sub account to organize what is really needed at each sub account level
*

    <figure><img src=".gitbook/assets/{D024A165-2E3F-48B0-810C-203BF08B3A32}.png" alt=""><figcaption></figcaption></figure>
