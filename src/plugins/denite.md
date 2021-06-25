# denite

<https://github.com/Shougo/denite.nvim>

## 設定
dein.toml

```toml
[[plugins]]
repo = 'Shougo/denite.nvim'
hook_add = '''
" Define mappings
autocmd FileType denite call s:denite_my_settings()
function! s:denite_my_settings() abort
    nnoremap <silent><buffer><expr> <CR>
                \ denite#do_map('do_action')
    nnoremap <silent><buffer><expr> d
                \ denite#do_map('do_action', 'delete')
    nnoremap <silent><buffer><expr> p
                \ denite#do_map('do_action', 'preview')
    nnoremap <silent><buffer><expr> q
                \ denite#do_map('quit')
    nnoremap <silent><buffer><expr> i
                \ denite#do_map('open_filter_buffer')
    nnoremap <silent><buffer><expr> <Space>
                \ denite#do_map('toggle_select').'j'
endfunction

call denite#custom#var('file/rec', 'command',['rg', '--files', '--glob', '!.git'])
call denite#custom#var('grep', 'command', ['rg', '--threads', '1'])
nmap <silent> [prefix]<Space> :<C-u>DeniteProjectDir -buffer-name=files file/rec buffer<CR>
nmap <silent> [prefix]b :<C-u>Denite buffer<CR>
nmap <silent> [prefix]g :<C-u>Denite ghq<CR>
'''
```

* https://secret-garden.hatenablog.com/entry/2021/05/16/152715

## floating-window

* (denite.nvimのFloating Windowオプションを使おう)[https://qiita.com/lighttiger2505/items/d4a3371399cfe6dbdd56]

## source

<https://github.com/Shougo/denite.nvim/wiki/External-Sources>
* https://qiita.com/iyuuya/items/8a7e9cc0c9dd6d0e4c32

* <https://endaaman.me/tips/denite-extension>

### ghq

## action

```vim
call denite#custom#kind('directory', 'default_action', 'cd')
```

## auto-action

* https://zenn.dev/matsui54/articles/2021-03-24-denite-auto-action


## preview

* https://zenn.dev/matsui54/articles/f6adb2a6f4c963637949

