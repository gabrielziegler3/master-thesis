## Compile files

```sh
compilation_files/compile full
```

## Neovim keymap

Compile the document with `F3` key.

```lua
vim.api.nvim_create_augroup("CompileDocument", { clear = true })

vim.api.nvim_create_autocmd("FileType", {
    group = "CompileDocument",
    pattern = "tex",
    command = "silent map <F3> :wall<cr>:silent !compilation_files/compile full<cr><esc>",
})
```

