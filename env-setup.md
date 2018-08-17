# Environment Setup (Elementary OS)

## 1. GIT

```sh
# install git
$ sudo add-apt-repository ppa:git-core/ppa
$ sudo apt-get update
$ sudo apt-get install git

# config git
$ git config --global push.followTags true
$ git config --global user.email "gean.marroquin@gmail.com"
$ git config --global user.name "wochap"
$ git config --global color.ui true
$ git config --global push.default current
$ git config --global alias.co checkout
```

### [Git addons](https://github.com/stevemao/awesome-git-addons)

* [Hub](https://github.com/github/hub)
* [commitizen](https://www.npmjs.com/package/commitizen)

```sh
$ npm install -g commitizen
$ npm i -g cz-conventional-changelog
$ echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc

# now you can commit with 
$ git cz
```

## 2. [PHP + Composer](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-14-04)

* PHP

```sh
# 16.04

$ sudo apt-get install php-cli php-mcrypt php-mbstring unzip
```

```sh
# 14.04

$ sudo apt-get install php5-cli php5-mcrypt php5-curl

# enable mcrypt
$ cd /etc/php5/cli/conf.d                         
$ sudo ln -s ../../mods-available/mcrypt.ini 20-mcrypt.ini               
```

* Composer

```sh
# 16.04

$ cd ~
$ curl -sS https://getcomposer.org/installer -o composer-setup.php

# verify installation (optional)
$ php -r "if (hash_file('SHA384', 'composer-setup.php') === '92102166af5abdb03f49ce52a40591073a7b859a86e8ff13338cf7db58a19f7844fbc0bb79b2773bf30791e935dbd938') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

$ sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
```

```sh
# 14.04

$ curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```

test

```sh
$ composer
```

## 3. [NVM](https://github.com/creationix/nvm#installation)

* Pre requires

```sh
$ sudo apt-get install build-essential libssl-dev
```

* Install and config

```sh
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash

# restart terminal

$ nvm install stable
$ nvm alias default 5.6.0
```

Globals packages 

* [yarn](https://yarnpkg.com/en/docs/install)

## 4. [RVM](https://github.com/rvm/rvm) [Ubuntu guide](https://gorails.com/setup/ubuntu/16.04)

```sh
$ gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
$ curl -L https://get.rvm.io | bash -s stable --autolibs=enabled --ruby --trace

# restart terminal

$ rvm install ruby --latest
$ rvm use 2.2.1 --default 

# fisherman rvm
$ fisher rvm

# **IMPORTANT** if you have broken packages, you cant install ruby
```

## 5. [Docker](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/#next-steps)

install docker CE and follow post installation

```sh
# access ssh
$ sudo docker exec -i -t <docker-container-id> /bin/bash

# monitor docker containers
$ docker stats --all --format "table {{.ID}}\t{{.Name}}\t{{.CPUPerc}}\t{{.MemUsage}}"
```

## 6. [Java JDK](https://www.unixmen.com/install-oracle-java-jdk-8-elementary-os-luna-via-ppa/)

## 7. [LAMP](https://www.lifeofgeek.com/install-lamp-elementary-os-loki/)

# Apps

## 1. Terminal

* [neofetch](https://github.com/dylanaraps/neofetch#ubuntu)

```sh 
$ sudo add-apt-repository ppa:dawidd0811/neofetch
$ sudo apt update
$ sudo apt install neofetch
``` 

* [Terminix](https://github.com/gnunn1/terminix)

* Tmux
 
```sh
$ sudo apt-get install tmux

# run fish when start tmux
# create a file ~/tmux.conf, with the content
# set-option -g default-shell /usr/bin/fish
```

* Fish

```sh
# installation a
$ sudo echo 'deb http://download.opensuse.org/repositories/shells:/fish:/release:/2/Debian_8.0/ /' >> /etc/apt/sources.list.d/fish.list 
$ sudo apt-get update
$ sudo apt-get install fish
# add repo key
wget http://download.opensuse.org/repositories/shells:fish:release:2/Debian_8.0/Release.key
apt-key add - < Release.key 

# installation b
# from link, select version
# https://launchpad.net/~fish-shell/+archive/ubuntu/release-2/+packages

# set fish default shell
$ chsh -s /usr/bin/fish

# install fish [fnm](https://github.com/fisherman/fnm)
$ fisher fnm

# install fish theme simple
$ fisher simple
# or
$ fisher /oh-my-fish/theme-cmorrell.com
```

  - create a /home/{user_name}/.config/fish/config.fish file

```
# nvm use default 6.7.0
set -gx NVM_DIR ~/.nvm

# remove greeting
set fish_greeting ""
```

* [Go Terminal](http://rungoterminal.com/)

* [Terminator](http://gnometerminator.blogspot.pe/p/introduction.html)

```sh
$ sudo add-apt-repository ppa:gnome-terminator
$ sudo apt-get update
$ sudo apt-get install terminator
```

* [ZSH](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)

* [Theme](https://github.com/oskarkrawczyk/honukai-iterm-zsh)

* Change pantheon-terminal scheme theme to Aci

```sh
$ gsettings set org.pantheon.terminal.settings palette "#363636:#ff0883:#83ff08:#ff8308:#0883ff:#8308ff:#08ff83:#b6b6b6:#424242:#ff1e8e:#8eff1e:#ff8e1e:#1e8eff:#8e1eff:#1eff8e:#c2c2c2"
$ gsettings set org.pantheon.terminal.settings background '#0d1926'
$ gsettings set org.pantheon.terminal.settings foreground '#b4e1fd'
$ gsettings set org.pantheon.terminal.settings cursor_color '#b4e1fd'

$ gsettings set org.pantheon.terminal.settings palette "#000000:#D5362C:#B9CA49:#E7C547:#268ACC:#C397D8:#268ACC:#FFFEFE:#000000:#D44D53:#B9C949:#E6C446:#268ACC:#C396D7:#268ACC:#FFFEFE"
$ gsettings set org.pantheon.terminal.settings background 'rgba(0,40,51, 85)'
$ gsettings set org.pantheon.terminal.settings foreground '#1C5C8C6'
$ gsettings set org.pantheon.terminal.settings cursor_color '#C4C8C5'
```

## 2. Atom editor

```sh
$ sudo add-apt-repository ppa:webupd8team/atom
$ sudo apt-get update
$ sudo apt-get install atom
```

Issues

* [gvfs-trash](https://github.com/atom/tree-view/issues/345#issuecomment-135779498)

* [terminal-plus](https://github.com/jeremyramin/terminal-plus/issues/321#issuecomment-242193432)

## 3. [ngrok](https://ngrok.com/)

Linux install: Download zip and extract on /bin

## 4. [dbvis](https://www.dbvis.com)

# Clear 

## a) [Y PPA Manager](http://askubuntu.com/questions/13065/how-do-i-fix-the-gpg-error-no-pubkey)

Tu lista de repositorios limpia como una patena Y PPA Manager

```
$ sudo add-apt-repository ppa:webupd8team/y-ppa-manager
$ sudo apt-get update
$ sudo apt-get install y-ppa-manager
```

## b) [banish404](https://datafull.co/p/como-puedo-solucionar-un-error-404-cuando-uso-un-ppa-o-actualizo-mi-lista-de-paquetes)

Eliminar ppas con 404

```sh
$ sudo add-apt-repository ppa:fossfreedom/packagefixes
$ sudo apt-get update
$ sudo apt-get install banish404
```

# Extras

## a) [Linuxbrew](https://github.com/Linuxbrew/linuxbrew)

Linuxbrew is a fork of Homebrew, the Mac OS package manager, for Linux.

```sh
# Pre requires
$ sudo apt-get install build-essential curl git m4 python-setuptools ruby texinfo libbz2-dev libcurl4-openssl-dev libexpat-dev libncurses-dev zlib1g-dev

# Follow instruction https://github.com/Linuxbrew/linuxbrew#installation
```

# Drivers

## [Video Nvidia](http://www.ubuntu-guia.com/2010/04/instalar-driver-de-tarjetas-nvidia-en.html)

```sh
$ sudo add-apt-repository ppa:graphics-drivers/ppa

$ sudo apt-get update

$ sudo apt-get install nvidia-352 nvidia-settings
```

# Environment Ubuntu (Digital Ocean)

## Commands

```
# systemctl <restart|start|stop> nginx
# 

# open port
$ iptables -I INPUT -p tcp --dport 12345 --syn -j ACCEPT
$ iptables -S
```
