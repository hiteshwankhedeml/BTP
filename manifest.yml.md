# 🟢 manifest.yml

* <mark style="color:purple;background-color:purple;">**File which we must create as a developer to let sap btp know everything about our project properties like**</mark>
  * <mark style="color:purple;background-color:purple;">**App name ⇒ Mandatory**</mark>
  * <mark style="color:purple;background-color:purple;">**Size**</mark>
  * <mark style="color:purple;background-color:purple;">**Runtime environment**</mark>
  * <mark style="color:$danger;background-color:purple;">**buildpack**</mark>
  * <mark style="color:purple;background-color:purple;">**Automatically allocate URL**</mark>
  * <mark style="color:$danger;background-color:purple;">**Services to be binded**</mark>
* Runtime environment is also optional, as per file extension it will take up the runtime
* [https://docs.cloudfoundry.org/devguide/deploy-apps/manifest-attributes.html#minimal-manifest](https://docs.cloudfoundry.org/devguide/deploy-apps/manifest-attributes.html#minimal-manifest)

```yml
applications:
  - name: jd-generation-app
    memory: 512M
    instances: 1
    buildpack: python_buildpack
    command: streamlit run app.py --server.port=$PORT --server.address=0.0.0.0
    env:
      STREAMLIT_SERVER_ADDRESS: 0.0.0.0
      STREAMLIT_BROWSER_GATHER_USAGE_STATS: false
    services:
      - destination-service
```
