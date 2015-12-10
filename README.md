Plain ansible module making basic environment setup installing common packages and dotfiles and vimplugins.

Currently tested and works only on CentOS 7, using root user.

# Usage
- Add/edit your host to hosts file or uncomment localhost node.
- Setup configuration happens via group_vvars/targets.yml
- ```bash ansible-playbook -i hosts site.yml ```

##### Packages
- mlocate
- wget
- zip
- unzip
- vim-enhanced
- bash-completion
- uuid
- bind-utils
- net-tools
- tmux
- git
- htop
- rsync
- strace
- lsof
- mtr
- traceroute
- deltarpm
- yum-cron
- yum-utils
- gcc
- cpp
- gcc-c++

##### Dotfiles
- .gitconfig
- .vimrc
- .tmux.conf

##### Vimrc
If you choose vim_complete option in configuration it will install Vundle, vim plugin manager. And next plugins included in default configuration. Otherwise it will include basic vimrc. Included plugins in case of vim_complete:
- scrooloose/nerdtree
- tpope/vim-fugitive
- kien/ctrlp.vim
- SirVer/ultisnips
- honza/vim-snippets
- ervandew/supertab
- godlygeek/tabular
- bling/vim-airline
