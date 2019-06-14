"echo ">^.^<"
set nu
set hlsearch
let mapleader=","

inoremap <leader>w <Esc>:w<cr>
noremap <leader>w :w<cr>
noremap <leader>q :q<cr>
nnoremap <leader>v :NERDTreeFind<cr>
nnoremap <leader>g :NERDTreeToggle<cr>
let NERDTreeShowHidden=1

inoremap jj <Esc>

"inoremap <C-h> <C-w>h
"inoremap <C-j> <C-w>j
"inoremap <C-k> <C-w>k
"inoremap <C-l> <C-w>l


" Specify a directory for plugins
" - For Neovim: ~/.local/share/nvim/plugged
" - Avoid using standard Vim directory names like 'plugin'
call plug#begin('~/.vim/plugged')

Plug 'scrooloose/nerdtree', { 'on': 'NERDTreeToggle' }
Plug 'mhinz/vim-startify'
Plug 'Xuyuanp/nerdtree-git-plugin'
Plug 'tpope/vim-fugitive'
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'
Plug 'w0ng/vim-hybrid'
Plug 'kien/ctrlp.vim'
Plug 'easymotion/vim-easymotion'
Plug 'tpope/vim-surround'
Plug 'brooth/far.vim'
Plug 'tpope/vim-commentary'
Plug 'tpope/vim-fugitive'
Plug 'airblade/vim-gitgutter'
Plug 'junegunn/gv.vim'
"Plug 'artur-shaik/vim-javacomplete2'

"Plug 'majutsushi/tagbar'
"Plug 'Yggdroot/indentLine'
" Initialize plugin system
call plug#end()

"autocmd FileType java setlocal omnifunc=javacomplete#Complete

"autocmd vimenter * NERDTree
"设置F3 未nerd 显示，隐藏
map <F3> :NERDTreeMirror<CR>
map <F3> :NERDTreeToggle<CR>
let g:NERDTreeIndicatorMapCustom = {
    \ "Modified"  : "✹",
    \ "Staged"    : "✚",
    \ "Untracked" : "✭",
    \ "Renamed"   : "➜",
    \ "Unmerged"  : "═",
    \ "Deleted"   : "✖",
    \ "Dirty"     : "✗",
    \ "Clean"     : "✔︎",
    \ 'Ignored'   : '☒',
    \ "Unknown"   : "?"
    \ }

let g:ctrlp_map = '<c-p>'

let g:ctrlp_custom_ignore = '\v[\/]\.(git|hg|svn|class)$'
nmap ss <Plug>(easymotion-s2)
set updatetime=100
