# 🟢 CI/CD Setup

* <mark style="color:purple;background-color:purple;">**Subscribe CD CD service**</mark>
* <mark style="color:purple;background-color:purple;">**Subscribe Cloud Transport Management ⇒ To move from Dev to QA to Prod**</mark>
* <mark style="color:purple;background-color:purple;">**Prod can also be in another sub account**</mark>
* Assign Roles for CI CD to the user
* Open CI CD Application

1. <mark style="color:purple;background-color:purple;">**Maintain Git Credentials**</mark>
2. <mark style="color:purple;background-color:purple;">**Maintain btp account credentials**</mark>
3. <mark style="color:purple;background-color:purple;">**Register the repo**</mark>

* git url and credentials
* Create webhook credentials
* After creation we will get webhook data

4. <mark style="color:purple;background-color:purple;">**In git ⇒ Webhook ⇒ Add webhook**</mark>

* Add the webhook data

5. <mark style="color:purple;background-color:purple;">**Create Job:**</mark>

* Job name
* Enter repo, branch, pipeline ⇒ cloud repo
* Select Build test
* We can add unit testing script also
* Code checks can be assed
* Release:
  * Subaccount details
  * Deployment = blue-green ⇒ Zero downtime
  * Space
  * Select Cloud TMS if it is to be moved to QA and Prod
