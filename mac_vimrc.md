cat .vimrc

```
set number
set showcmd
set tabstop=4
set nobackup
set virtualedit=onemore
set smartindent
set showmatch
set matchtime=1
set ignorecase
set smartcase
set wrapscan
set expandtab
set shiftwidth=4
set hidden
set title
set wrap
set whichwrap=b,s,[,],<,>
set backspace=indent,eol,start
set display=lastline
set pumheight=10
set laststatus=2
""set statusline=%{expand('%:p:t')}\ %<[%{expand('%:p:h')}]%=\ %m%r%y%w[%{&fenc!=''?&fenc:&enc}][%{&ff}][%3l,%3c,%3p]


 " Note: Skip initialization for vim-tiny or vim-small.
 if 0 | endif

 if &compatible
   set nocompatible               " Be iMproved
 endif

 " Required:
 set runtimepath+=~/.vim/bundle/neobundle.vim/

 " Required:
 call neobundle#begin(expand('~/.vim/bundle/'))

 " Let NeoBundle manage NeoBundle
 " Required:
 NeoBundleFetch 'Shougo/neobundle.vim'

 " My Bundles here:
 " Refer to |:NeoBundle-examples|.
 " Note: You don't set neobundle setting in .gvimrc!

 "statusbar lightline
NeoBundle 'itchyny/lightline.vim'

NeoBundle 'scrooloose/nerdtree'

 call neobundle#end()

 " Required:
 filetype plugin indent on

 " If there are uninstalled bundles found on startup,
 " this will conveniently prompt you to install them.
 NeoBundleCheck

 "set colorscheme
let g:solarized_termcolors=256
syntax enable
set background=dark
colorscheme solarized

 "set statusbar
"NeoBundle 'itchyny/lightline.vim'
let g:lightline = { 'colorscheme': 'wombat' }


"{} () "" '' 2つ付与自動化
inoremap { {}<LEFT>
inoremap {<Enter> {}<LEFT><CR><Esc><S-o>
inoremap ( ()<LEFT>
inoremap " ""<LEFT>
inoremap ' ''<LEFT>
inoremap [ []<LEFT>

"show Tree
""auto StdinReadPre * let s:std_in=1
""auto VimEnter * if argc() == 0 && !exists("s:std_in") | NERDTree | endif
map <C-n> : NERDTreeToggle<CR>

```




