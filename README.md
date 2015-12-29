Plain ansible module making basic environment setup installing common packages and dotfiles and vimplugins.

Configures: Centos 7, Fedora 23

# Usage
- Add/edit your host to hosts file or uncomment localhost node.
- Setup configuration happens via group_vars/targets.yml
- `ansible-playbook -i hosts site.yml`
- `-k` - SSH connection password will be asked. This is needed in case if you don't have key authentication with dedicated node.
- `-K` - sudo password will be asked.

##### Packages for CentOS
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
If you choose vim_complete option in configuration it will install Vundle, vim plugin manager. Requires git on system. Otherwise it will include basic vimrc. Included plugins in case of vim_complete:
- [scrooloose/nerdtree][1]
- [tpope/vim-fugitive][2]
- [ctrlpvim/ctrlp.vim][3]
- [SirVer/ultisnips][4]
- [honza/vim-snippets][5]
- [ervandew/supertab][6]
- [godlygeek/tabular][7]
- [bling/vim-airline][8]

[1]: https://github.com/scrooloose/nerdtree
[2]: https://github.com/tpope/vim-fugitive
[3]: https://github.com/ctrlpvim/ctrlp.vim
[4]: https://github.com/SirVer/ultisnips
[5]: https://github.com/honza/vim-snippets
[6]: https://github.com/ervandew/supertab
[7]: https://github.com/godlygeek/tabular
[8]: https://github.com/bling/vim-airline
