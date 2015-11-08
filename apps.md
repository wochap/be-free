# [Aplicaciones](https://oduso.com/)

## Utiles

- Redshift: programa para aliviar el cansancio ocular.

  * instalacion
  ```sh
  $ sudo add-apt-repository ppa:jonls/redshift-ppa
  $ sudo apt-get update && sudo apt-get install redshift
  ```

  * uso  
  ```sh
  $ redshift -l -18.010529:-70.240198
  ```
  
- [Show Desktop](https://www.reddit.com/r/elementaryos/comments/2sbgrs/showdesktop_doesnt_work_on_freya/)
 
 * instalacion       
 ```sh
  $ sudo apt-get install wmctrl
  ```
 Then add the custom command in Settings > Desktop > Hot Corners:    
 ```sh
  $ wmctrl -k on
  ```
 

## [Apps](https://oduso.com/)

- [Elementary apps](https://quassy.github.io/elementary-apps/)

- Gimp

  * instalacion  
  ```sh
  $ sudo apt-get install gimp
  ```
  
- Indicator synapse

  * instalacion  
  ```sh
  $ sudo add-apt-repository ppa:synapse-core/ppa
  $ sudo apt-get update
  $ sudo apt-get install synapse
  ```
  
  * instalar plugin [save for web](http://registry.gimp.org/node/33), install [guide](https://github.com/auris/gimp-save-for-web)


- Dconf
  
  * Instalacion
  ```sh 
  $ sudo apt-get install dconf-tools
  ```


## Apps non-free

- Spotify

  * [instalacion](http://howtoubuntu.org/how-to-install-spotify-in-ubuntu)
  ```sh
  $ sudo apt-add-repository -y "deb http://repository.spotify.com stable non-free" && sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys D2C19886 && sudo apt-get update -qq && sudo apt-get install spotify-client
  ```

  * bloquear [publicidad](https://rhoconlinux.wordpress.com/2015/06/25/megapost-spotify-gratis-y-sin-anuncios-en-ubuntu-14-04-o-superior/)
 
- Whatsapp                                           
  
  * [instalacion](https://rhoconlinux.wordpress.com/2015/06/27/whatsapp-en-ubuntu-como-instalarlo-y-configurarlo-super-facil/)                        
  ```sh
  $ cd /tmp/ && clear ; wget https://github.com/Aluxian/WhatsApp-Desktop/releases/download/v1.1.0/UnofficialWhatsApp_linux64.deb -O whatsapp.deb && sudo apt-get install gdebi -y ; sudo gdebi -n whatsapp.deb ; cd ; clear
  ```

