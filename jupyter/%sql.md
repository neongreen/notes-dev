# %sql

```python
import duckdb

%load_ext sql
conn = duckdb.connect()
%sql conn --alias duckdb
```
