# Environment Setup (Elementary OS)

## 1. GIT

```sh
$ sudo add-apt-repository ppa:git-core/ppa
$ sudo apt-get update
$ sudo apt-get install git
```

### [Git addons](https://github.com/stevemao/awesome-git-addons)

* [Hub](https://github.com/github/hub)

## 2. [PHP + Composer](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-14-04)

* PHP

```sh
$ sudo apt-get install php5-cli php5-mcrypt php5-curl

# enable mcrypt
$ cd /etc/php5/cli/conf.d                         
$ sudo ln -s ../../mods-available/mcrypt.ini 20-mcrypt.ini               
```

* Composer

```sh
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

## 4. [RVM](https://github.com/rvm/rvm)

```sh
$ gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
$ curl -L https://get.rvm.io | bash -s stable --autolibs=enabled --ruby --trace

# restart terminal

$ rvm install ruby --latest
$ rvm use 2.2.1 --default 
```

## 5. [Docker](https://docs.docker.com/linux/step_one/)

# Apps

## 1. Terminal

* [Terminator](http://gnometerminator.blogspot.pe/p/introduction.html)

```sh
$ sudo add-apt-repository ppa:gnome-terminator
$ sudo apt-get update
$ sudo apt-get install terminator
```

* [ZSH](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)
* [Theme](https://github.com/oskarkrawczyk/honukai-iterm-zsh)


## 2. Atom editor

```sh
$ sudo add-apt-repository ppa:webupd8team/atom
$ sudo apt-get update
$ sudo apt-get install atom
```

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
