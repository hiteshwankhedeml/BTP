---
hidden: true
---

# ✈️ Demo BTP Application

* mkdir btpdemo ⇒ a new project is like a new folder
* cds init ⇒ Project structure will be created
  *

      <figure><img src=".gitbook/assets/{730692A8-BD7A-40CD-831E-99B110113613}.png" alt=""><figcaption></figcaption></figure>
* db ⇒ datamodel.cds
  * Right click and Open with Graphical Editor
  * Create entity ⇒ Which means a DB table
  * Inside this we can add fields
  *

      <figure><img src=".gitbook/assets/{6F16B454-2A6F-4FF9-A6B4-BAB58615BD39}.png" alt=""><figcaption></figcaption></figure>
  * We can also do the same using text
    *

        <figure><img src=".gitbook/assets/{2AA95A4A-C4A2-480A-BB63-7A3D16EE193F}.png" alt=""><figcaption></figcaption></figure>
* srv ⇒ Service.cds
  * Import the datamodel which was created
  *

      <figure><img src=".gitbook/assets/{CC90B9EC-1D7B-49B0-9B50-007A5E511D62}.png" alt=""><figcaption></figcaption></figure>
* db ⇒ csv ⇒ create a csv as the same as the entity which was created
* It will automatically upload all this data in the entity
* npm install
* cds deploy --to sqlite
* cds run
*   We can see all the data using the Fiori preview

    <figure><img src=".gitbook/assets/{64B472E1-3899-40D5-9B4B-7F3DEA12BB9E}.png" alt=""><figcaption></figcaption></figure>
