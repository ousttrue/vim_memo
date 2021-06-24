# vim

.gvimrc
```vim
set iminsert=0
set imsearch=-1
set lines=40
set columns=80
set guicursor+=a:blinkon0
set guioptions-=r  "remove right-hand scroll bar
set guioptions-=L  "remove left-hand scroll bar
set guifont=Cica:h14:cANSI:qDRAFT
set renderoptions=type:directx,renmode:5

filetype plugin indent on
syntax enable

set belloff=all
set hidden
set noswapfile nobackup noundofile
set laststatus=2
set ts=4 sw=4 sts=4 expandtab
set hlsearch
set clipboard=
set ambiwidth=double
set autochdir
set list
set listchars=tab:»-,trail:-,eol:↲,extends:»,precedes:«,nbsp:%
if has('win32')
    set clipboard=unnamed
else
    set clipboard=unnamedplus
endif
if has('nvim')
    set nopaste
    noremap! <S-Insert> <C-R>+
else
    set t_Co=256
endif
hi MatchParen ctermbg=239
```

