# abandon all divergent commits

have to use `jj abandon --ignore-immutable` but making sure all children are covered as well

```bash
jj abandon -r '(main..(49131143|4372ba3b))::' --ignore-immutable
```

