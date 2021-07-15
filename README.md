# vimrc
vimrc file for c++

=>Open terminal:
sudo vim  ~/.vimrc

=>Paste the following:

" set tabstop=4
" Default Indentation
set autoindent
set expandtab       " expand tab to space
set smartindent     " indent when
set tabstop=4       " tab width
set softtabstop=4   " backspace
set shiftwidth=4    " indent width
" Automatically closing braces
inoremap { {}<Esc>ha
inoremap ( ()<Esc>ha
inoremap [ []<Esc>ha
inoremap " ""<Esc>ha
inoremap ' ''<Esc>ha
inoremap ` ``<Esc>ha
" Make it so that a curly brace automatically inserts an indented line
inoremap {<CR> {<CR>}<Esc>O<BS><Tab>
:autocmd BufNewFile *.cpp 0r ~/.vim/templates/skeleton.cpp
  
=>To get predefined template each time you create new c++ file :
=>Open terminal and paste the following :
  mkdir ~/.vim
  cd .vim/
  mkdir templates && cd templates
  sudo vim skeleton.cpp
  => Inside skeleton.cpp
     #include <bits/stdc++.h>
     using namespace std;
      
     int main()
     {
      
     }
    Save it.
  
  
