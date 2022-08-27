# Introduction

This repo is committed to make it easier for Vim/Neovim package managers to install the gtags scripts provided by the [GNU Global](https://www.gnu.org/software/global/) source code tag system.

# Install

## vim-plug

Put the following line along with other plugins:

```vim
Plug 'xbot/gtags.vim'
```

Then restart vim and execute `:PluginInstall`.

# Config

This is just an example:

```vim
let Gtags_Auto_Update       = 1
let Gtags_Close_When_Single = 1
let g:cscope_silent         = 1
augroup gtags
    au!
    au FileType php,python,c,cpp,javascript,go map <buffer> <C-]> :Gtags<CR><CR>
    if has('gui_running')
        au FileType php,python,c,cpp,javascript,go map <buffer> <C-S-]> :Gtags -r<CR><CR>
    endif
augroup END
```

# Usage

https://www.gnu.org/software/global/globaldoc_toc.html#Vim-editor
