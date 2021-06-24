# keymap

* [端末上のvimでctrl+space（ついでにプラグインの上書き回避）](https://h-miyako.hatenablog.com/entry/2014/01/20/053327)

`<c-@>` に変換されて insert される？

* https://vim.fandom.com/wiki/Avoid_the_escape_key


```vim
imap <Nul> <Nop>
inoremap <C-Space> <c-x><c-o>
imap <C-@> <C-Space>
```

```vim
nmap <C-n> :lnext<CR>
nmap <C-p> :lprevious<CR>
nnoremap <C-l> :nohlsearch<CR><C-l>
nnoremap q :close<CR> 
```

