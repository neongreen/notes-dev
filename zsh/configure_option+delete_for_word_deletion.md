# Configure Option+Delete for word deletion

Configure Option+Delete (Alt+Backspace) in zsh to properly delete words:

```zsh
# Define what characters are considered part of a word
WORDCHARS="*?_.[]~=&;!#$%^(){}<>"

# Bind Option+Delete to backward-kill-word
bindkey '^[^?' backward-kill-word
```

