Requires next variables:

**Dotfiles** role doesn't require you to have corresponding applications to be installed.

Except the case when `vim_complete` equals `yes`, git should be preinstalled.

| Variable | Values | Description |
| --- | --- | --- |
| **git** | *yes/no* | Install Git and place configuration files |
| **gitname** | *Xxxx Yyyyyyyyyyyy* | Git author name |
| **gitemail** | *x.yyyyyyyyyyyy@example.com* | Git author email |
| **tmux** | *yes/no* | Install Tmux and place configuration files |
| **vim_complete** | *yes/no* | Install Vim and place configuration files. `yes` will setup plugins |
| **vim_solarized** | *yes/no* | Include solarized configuration in vimrc. `vim_complete` required |
| **vimplugins** | | List of plugins to be enabled. Vundle format `github_user/plugin_name` |
