# 🟢 Save - HDI

* Same connection setup as §3; user needs INSERT on the target table (via HDI grants / role — not covered here).
* Use parameters (`?`) — avoid string concatenation for values.
* Call `conn.commit()` after DML if autocommit is off.

```python
from hdbcli import dbapi

conn = dbapi.connect(
    address="<host>",
    port=443,
    user="<user>",
    password="<password>",
    encrypt=True,
    sslValidateCertificate=True,
)

cur = conn.cursor()
cur.execute(
    'INSERT INTO "<SCHEMA>"."MY_TABLE" ("COL1", "COL2") VALUES (?, ?)',
    ("value1", 42),
)
conn.commit()

cur.close()
conn.close()
```

* Bulk: `cur.executemany(...)` with a list of tuples for many rows.
