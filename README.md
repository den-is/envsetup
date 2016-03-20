Plain ansible module making basic environment setup by installing common packages, dotfiles and vimplugins.

# Usage
- Tested on: Centos 7, Fedora 23
- Ansible 2.0+ required
- `root` account required on remote hosts.
- `sshd` running service required on remote hosts
- `sshpass` package required for ssh connections without keys (user/pass)


- Add/edit your host to hosts file or uncomment localhost node.
- Setup configuration happens via files in group_vars directory; add/remove packages/services there as you need.
- `ansible-playbook -i hosts site.yml`
- `-k` - SSH connection password will be asked. This is needed in case if you don't have key authentication with dedicated node.
- `-K` - sudo password will be asked.

**Fedora localhost complete example**
```bash
sudo dnf install -y python python-devel python-pip gcc rpm-build
sudo pip install 'ansible>=2.0'
git clone https://github.com/den-is/envsetup.git
cd envsetup
# uncomment localhost line in [fedora] group in hosts file
sudo ansible-playbook -i hosts site.yml -K
```
**Install or skip certain tags**
```bash
ansible-playbook -i hosts site.yml --tags "dotfiles" 
ansible-playbook -i hosts site.yml --skip-tags "dotfiles"
```

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
