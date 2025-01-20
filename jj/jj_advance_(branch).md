# jj advance (branch)

Move bookmark to the latest commit:

```toml
# config

[aliases]
advance = [
    "bookmark",
    "move",
    "--from",
    "heads(::@- & bookmarks())",
    "--to",
    "@-"
]
```

