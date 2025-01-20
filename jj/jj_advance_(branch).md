# jj advance (branch)

Move bookmark from previous commit to current one automatically:

```toml
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

Location: ~/Library/Application Support/jj/config.toml
