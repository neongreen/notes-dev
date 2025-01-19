# Save and close with Ctrl+D

To configure Neovim to save and close with Ctrl+D, add these lines to init.vim:

```vim
nnoremap <C-d> :wq<CR>
inoremap <C-d> <Esc>:wq<CR>
```

This will work in both normal mode and insert mode (in insert mode it will first escape to normal mode).
