# Configure Option+Delete for word deletion

Configure Option+Delete (Alt+Backspace) in zsh to properly delete words:

```zsh
# Define what characters are considered part of a word
WORDCHARS="*?_.[]~=&;!#$%^(){}<>"

# Bind Option+Delete to backward-kill-word
bindkey '^[^?' backward-kill-word
```

This configuration:
1. Sets which special characters are treated as part of words
2. Maps Option+Delete to delete the whole word behind the cursor

Useful particularly in macOS Terminal and iTerm2.
