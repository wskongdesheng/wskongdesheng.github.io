---
layout: post
title: 'My vimrc Settings'
date: 2015-09-15 17:15:00
categories: my Settings
---
### common plugins
*** AutoComplPop
*** bufexplorer
*** nerdcommenter
*** NERDTree
*** syntastic
*** vim-bundler
*** vim-fugitive
*** vim-jsbeautify
*** vim-NERDTree-tabs
*** vim-rails
*** vim-ruby
{% highlight sh %}
execute pathogen#infect()
set nocompatible              " be iMproved, required
syntax on                     " Enable syntax highlighting
filetype plugin indent on
set expandtab
set tabstop=2 shiftwidth=2 softtabstop=2
set autoindent
set nowrap
set encoding=utf-8
set fileencodings=utf-8,gb2312,gb18030,gbk,ucs-bom,cp936,latin1
set termencoding=utf-8
set guifont=Bitstream\ Vera\ Sans\ Mono\ 12
autocmd FileType ruby,eruby,yaml set ai ts=2 sw=2 sts=2 et
set list
set listchars=tab:,.,trail:.,extends:#,nbsp:. " Highlight problematic whitespace
set number
set hlsearch    " highlight search
set incsearch   " incremental search
set ignorecase  " Do case in sensitive matching with
set smartcase   " be sensitive when there's a capital letter
set ignorecase
set smartcase
let mapleader=","

" navigate
nmap mh <C-w>h
nmap ml <C-w>l
nmap mk <C-w>k
nmap mj <C-w>j
nmap - :w<CR>
nmap <leader>z :q<CR>
nmap <leader>za :qa<CR>
nmap <leader>s :sp<CR>
nmap <leader>v :vsp<CR>
nmap <leader>w :noh<CR>
imap jj <ESC>

au BufRead,BufNewFile {Gemfile,*.god,Rakefile,Capfile,*.rake,config.ru} set ft=ruby
au BufRead,BufNewFile {*.md,*.mkd,*.markdown} set ft=markdown
au BufRead,BufNewFile {*.thrift} set ft=c

" NERDTree
nmap <leader>n :NERDTreeToggle<CR>
let NERDTreeHighlightCursorline=1

" bufexplorer
let g:bufExplorerShowDirectories=0   " Not show directories.
let g:bufExplorerShowRelativePath=1  " Show relative paths.


hi Comment ctermfg=DarkGrey
" disable auto insert comments when paste
autocmd FileType * setlocal formatoptions-=c formatoptions-=r formatoptions-=o
runtime macros/matchit.vim

{% endhighlight %}
