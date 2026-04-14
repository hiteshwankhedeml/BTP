# 🟢 Read - HDI

* <mark style="color:$danger;background-color:purple;">**Use hdbcli**</mark>
* <mark style="color:$danger;background-color:purple;">**Create connection**</mark>
* <mark style="color:$danger;background-color:purple;">**Get cursor**</mark>
* <mark style="color:$danger;background-color:purple;">**Using cursor execute the select statement**</mark>
* Driver: `pip install hdbcli` (SAP HANA client for Python).
* Credentials: from BTP — SAP HANA Cloud instance Service Key (or binding env), or CF `VCAP_SERVICES` / local `default-env.json` when using `cf` tooling.
* From service key JSON (typical fields): `host`, `port` (often `443`), `user`, `password`, `certificate` (if using cert auth — then follow SAP doc for `ssl*` options).
* HANA Cloud: use encrypted connection (`encrypt=True`); align SSL with your org (cert validation / trust store).
* Table must live in a schema your DB user can SELECT (e.g. HDI-deployed table in that container’s schema).

```python
from hdbcli import dbapi

# Replace with values from BTP HANA Cloud service key / binding
conn = dbapi.connect(
    address="<host from service key>",
    port=443,
    user="<user>",
    password="<password>",
    encrypt=True,
    sslValidateCertificate=True,
)

cur = conn.cursor()
cur.execute('SELECT * FROM "<SCHEMA>"."MY_TABLE" WHERE ROWNUM <= 10')
for row in cur.fetchall():
    print(row)

cur.close()
conn.close()
```

* Use quoted identifiers `"SCHEMA"."TABLE"` when names are case-sensitive.
