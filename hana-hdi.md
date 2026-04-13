# 🟢 HANA HDI

* HDI = <mark style="color:purple;background-color:purple;">**HANA Deployment Infrastructure (deployment layer on HANA, not a separate DB).**</mark>
* <mark style="color:purple;background-color:purple;">**Deploys design-time artifacts (tables, views, procedures, etc.) into an HDI container.**</mark>
* Container = isolated DB area + metadata so deploy/update/remove stays consistent.
* Typical on SAP BTP: SAP HANA Cloud + Business Application Studio, CAP apps, MTA deploy.
* External or shared data: use synonyms and grants — not ad-hoc cross-schema access.
