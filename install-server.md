# Instalar servidor local (apache y postgre)

## Errores

### Apache

- 403 Forbidden

  * Intentar dar permisos de lectura a la carpeta
  
  * Intenta esta [solucion](http://stackoverflow.com/questions/10873295/error-message-forbidden-you-dont-have-permission-to-access-on-this-server)
  * 
  
## Instalacion

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
 

### Php
 - instalacion
 
 ```sh
  $ sudo apt-get install libapache2-mod-php5 php5 php5-mcrypt                            
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

### Nodejs 

 ```sh
  $ curl --silent --location https://deb.nodesource.com/setup_0.12 | sudo bash -
  $ sudo apt-get install --yes nodejs                       
 ```
 
