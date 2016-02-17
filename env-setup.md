# Environment Setup (Elementary OS)

## 1. GIT

```sh
$ sudo add-apt-repository ppa:git-core/ppa
$ sudo apt-get update
$ sudo apt-get install git
```

## 2. [PHP + Composer](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-14-04)

* PHP

```sh
$ sudo apt-get install php5-cli
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

## 4. [Docker](https://gist.github.com/wdullaer/f1af16bd7e970389bad3)


# Clear 

## [Y PPA Manager](http://askubuntu.com/questions/13065/how-do-i-fix-the-gpg-error-no-pubkey)

Tu lista de repositorios limpia como una patena Y PPA Manager

```
sudo add-apt-repository ppa:webupd8team/y-ppa-manager
sudo apt-get update
sudo apt-get install y-ppa-manager
```