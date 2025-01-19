# load xml as relation

```python
import xmltodict
import pyarrow as pa

xml = xmltodict.parse(Path(file).read_text())
messages = xml.get("SomeRootElement", {}).get("Message", [])
if not isinstance(messages, list):
    messages = [messages]

messages_table = pa.Table.from_pylist(messages)
```
