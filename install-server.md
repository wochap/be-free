# Instalar servidor local (apache y postgre)

## Errores

### Apache

- 403 Forbidden

  * Intentar dar permisos de lectura a la carpeta
  
  * Intenta esta [solucion](http://stackoverflow.com/questions/10873295/error-message-forbidden-you-dont-have-permission-to-access-on-this-server)
  
  
## [Instalacion](http://laravel.io/forum/05-25-2014-installing-laravel-on-ubuntu)

### Git

 ```sh
  $ sudo add-apt-repository ppa:git-core/ppa       
  $ sudo apt-get update                             
  $ sudo apt-get install git                                                 
 ```

### Apache
 - instalacion
 
 ```sh
  $ sudo apt-get update                
  $ sudo apt-get install apache2                
 ```
 - reiniciar servidor
 
 ```sh
  $ sudo service apache2 restart                                               
 ```
 
 - solucionar problemas al [reiniciar](http://tutorialforlinux.blogspot.pe/2013/10/solve-problem-ah00558-when-restarting.html) apache
 

### Php
 - instalacion
 
 ```sh
  $ sudo apt-get install libapache2-mod-php5 php5 php5-mcrypt                            
 ```
 
 - [mcrypt](http://www.kvcodes.com/2014/07/laravel-requires-mcrypt-php-extension/)       
 ```sh
  $ cd /etc/php5/cli/conf.d                         
  $ sudo ln -s ../../mods-available/mcrypt.ini 20-mcrypt.ini               
 ```
 
 - postgres driver
 ```sh
  $ sudo apt-get install php5-pgsql
 ```
 
 - composer                   
 ```sh
  $ curl -sS https://getcomposer.org/installer | php                     
  $ mv composer.phar /usr/local/bin/composer                 
 ```
 
 - requires ext-curl                   
 ```sh
  $ sudo apt-get install php5-curl                      
 ```
 
### PostgresSQL                           
- instalacion

 * instalar server                           
 
 ```sh
  $ sudo apt-get install postgresql postgresql-contrib                                    
  $ apt-cache search postgres  
 ```
 * instalar cliente                                                      

 ```sh
  $ sudo apt-get install pgadmin3                                                      
  $ sudo apt-get install postgresql-client                           
 ```
- configuracion                   
 1) ingresar como super usuario                 
  ```sh
   $ sudo su                     
  ```
 2) ingresar como usuario posgtgres                   
  ```sh
   $ su postgres                     
  ```
 3) cambiar contraseña al usuario postgres             
  ```sh
   $ psql -U postgres                
   $ postgres=# alter user postgres with password 'CONTRASENA_DEL_USUARIO';  
   $ \q                     
   
   $ exit
  ```
 4) reiniciar postgres
  ```sh
   $ service postgresql restart
  ```
 
### Nodejs 

 - instalacion                     
 ```sh
  $ curl --silent --location https://deb.nodesource.com/setup_0.12 | sudo bash -
  $ sudo apt-get install --yes nodejs                       
 ```
 - upgrade [npm](https://docs.npmjs.com/getting-started/installing-node)                     
 ```sh
  $ sudo npm install npm@latest -g                
 ```
 
 - upgrade [node](http://davidwalsh.name/upgrade-nodejs)                     
 ```sh
  $ sudo npm cache clean -f             
  $ sudo npm install -g n                  
  $ sudo n stable                 
  $ node -v             
 ```
 
### Ruby
 - [rvm](http://elementaryos.stackexchange.com/questions/2577/how-to-install-ruby-2-2-3-on-elementary-os-freya)
 ```sh
  $ -keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 
\curl -O https://raw.githubusercontent.com/rvm/rvm/master/binscripts/rvm-installer 
\curl -O https://raw.githubusercontent.com/rvm/rvm/master/binscripts/rvm-installer.asc 
gpg --verify rvm-installer.asc && 
bash rvm-installer stable                       
 ```
 - ruby
 ```sh
  $ rvm get stable --autolibs=enable
  $ rvm install 2.2.3    
  $ rvm --default use ruby-2.2.3
 ```
 
 - sass
 ```sh
  $ gem install sass
 ```
