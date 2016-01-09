# Tuneando eOS

## Pequeños detalles

- Plank: Efecto zoom

  * instalacion:
  ```sh
  $ sudo add-apt-repository ppa:ricotz/docky
  $ sudo apt-get update
  $ sudo apt-get install plank
  ```
  * parametros:
  ~/.config/plank/dock1/settings
  ZoomEnabled=true
  ZoomPercent=150

## Instalar [iconos](http://gnome-look.org/)

  * instalacion:  
  descomprimes en `/home/<user_name>/.icons/`
  cambias los iconos con tweaks
  si no te funciona, copialos tambien en `/usr/share/icons/`

## Instalar [temas](http://gnome-look.org/)

  * instalacion:  
  descomprimes en `/home/<user_name>/.themes/`
  cambias el tema con tweaks o con el siguiente comando
 ```sh
 $ gsettings set org.gnome.desktop.interface gtk-theme "CoolestThemeOnEarth"
 ```
  si no te funciona, copialos tambien en `/usr/share/themes/`

## Instalar [conky](http://elementaryos.stackexchange.com/questions/222/how-install-conky-manager-on-freya)

  * instalacion:  
  ```sh
   $ sudo add-apt-repository ppa:teejee2008/ppa                   
   $ sudo apt-get update                    
   $ sudo apt-get install conky-manager                                      
  ```
  añadir conky-manager al arranque
  
  * instalar themas                                  
  copiar themas dentro de `/home/<user>/.conky/`

## Cambiar theme del terminal
  * instalacon
   [link](http://mayccoll.github.io/Gogh/)
   [4 bit](http://ciembor.github.io/4bit/)

## Me

* Icons             
 [Yosemite Icons](http://zacpier.deviantart.com/art/Yosemite-Icons-for-Linux-494175906)

* Terminal                  
 [powerline](http://www.tecmint.com/powerline-adds-powerful-statuslines-and-prompts-to-vim-and-bash/) 

* Plank                
  [rainer](https://burguerblog.wordpress.com/2015/11/16/como-personalizar-plank-en-elementary-os-freya/)


## Instalar burg

Here I leave the tutorial to install the system startup BURG


We open the terminal and follow these steps:

Add the repository:

$sudo add-apt-repository ppa:n-muench/burg

$sudo apt-get update

Install Burg:

$sudo apt-get install burg

We leave all options as they come, except there "Grub Install brands Devices ", check / dev / sda  with the space key, then accept and go.

To install the themes:

We unzip the .zip folder, copy the folder that contained, and paste in the following path in a file browser as administrator: /boot /burg /themes

After update the burg in terminal with the following command:

$sudo update-burg

To choose a theme and configure its resolution emulate the burg with the following command in the terminal:

$sudo burg-emu -D

Press "T" ket to choose theme, "R" to change resolution, and "F"  to group the distro versions elements.

Download the themes:

https://drive.google.com/folderview?id=0B5bLNnaSeLcXfkhyZ3loMUJUTVRuYlF5ekJLSFI3bWdPbC1tUVBwdkxhUkEwNE1HMUpMWkk&usp=sharing

To uninstall:

$sudo apt-get purge burg burg-emu burg-pc burg-themes-common burg-common burg-themes

and reinstall:

$sudo apt-get install burg burg-emu burg-pc burg-themes-common burg-common burg-themes﻿
