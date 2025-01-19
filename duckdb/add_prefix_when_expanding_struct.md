# add prefix when expanding struct

```sql
FROM
  messages_table
SELECT
  _filename,
  _xml,
  * EXCLUDE (Data, _filename, _xml),
  COLUMNS (Data.*) AS "Data.\0"
```

NOTE: would be nice if this was documented in duckdb docs
