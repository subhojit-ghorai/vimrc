# vimrc
vimrc file for c++

Open terminal and paste the following:
```
sudo vim  ~/.vimrc
```

Paste the following in .vimrc:
```
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
```
  
To get predefined template each time you create new c++ file :
Open terminal and paste the following :
``` 
mkdir ~/.vim
cd .vim/
mkdir templates && cd templates
sudo vim skeleton.cpp
```
Inside skeleton.cpp paste the following :
```
#include <bits/stdc++.h>
using namespace std;

int main()
{

}
```
Save and close vim :
```
:wq
```
Now each time anyone creates a new cpp filw using vim, the above template will be automatically loaded.
  
  
