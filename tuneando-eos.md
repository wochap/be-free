# Tuneando eOS

## 1. Add desktop

```sh
# Install Nautilus without all the related Gnome packages and dconf-editor
$ sudo apt-get install --no-install-recommends nautilus dconf-tools

# Open dconf-tool and go to, and tick the show-desktop-icons box
org.gnome.nautilus.desktop

# Then go to
org.pantheon.desktop.cerbere

# Add nautilus -n so the entry should look somewhat like this:
['wingpanel', 'plank', 'slingshot-launcher --silent', 'nautilus -n']

# Open terminal and run:
$ nautilus -n

# Go to and tick the show-desktop-icons box
org.gnome.desktop.background
```

## Instalar rEEF

 * Instalar 

```sh
$ sudo apt-add-repository ppa:rodsmith/refind
$ sudo apt-get update
$ sudo apt-get install refind
```

 * Instalar [tema minimal](http://evanpurkhiser.com/rEFInd-minimal/)
 

## Install Tweaks

```sh
$ sudo apt-add-repository ppa:mpstark/elementary-tweaks-daily
$ sudo apt-get update
$ sudo apt-get install elementary-tweaks
```

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

## [Docky](https://twobytech.wordpress.com/2016/01/15/instala-y-personaliza-docky-el-dock-que-el-dinero-no-puede-comprar/) 

## Tunear [VLC](https://twobytech.wordpress.com/2016/01/09/dos-hermosos-skins-para-vlc-player/)

## [Customize your theme](http://eos-snippets.blogspot.pe/2014/12/fix-toolbar-synaptic-in-freya.html)
Dev tools for customize themes:
* [GTK Parasite](https://github.com/chipx86/gtkparasite)
* [GTK Inspector](http://askubuntu.com/questions/597259/how-do-i-open-gtk-inspector)

## [Customize theme and window buttons](http://srv12.cpanelhost.cl/~cl119365/eos/ )

## [Instalar plymouth](http://mhsnotes.blogspot.co.id/2016/02/install-custom-plymouth-on-elementary_3.html)

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
 antes [habilitar cambio](http://unix.stackexchange.com/questions/141066/change-colors-for-the-pantheon-terminal-emulator)

  * instalacon
   [varios](http://mayccoll.github.io/Gogh/)

   [4 bit](http://ciembor.github.io/4bit/)


## Instalar GLOBAL MENU

  * instalacion:  
  ```sh
   $ sudo add-apt-repository ppa:varlesh-l/test
   $ sudo apt-get update
   $ sudo apt-get install --reinstall wingpanel=0.3~r217-1 indicator-appmenu
   $ gsettings set org.pantheon.desktop.wingpanel blacklist "['']"
   $ killall wingpanel                                    
  ```
  * desinstalacion (volver a instalar wingpanel):  
  ```sh
   $ sudo apt-get purge wingpanel indicator-appmenu
   $ sudo add-apt-repository -r ppa:varlesh-l/test
   $ sudo apt-get update
   $ sudo apt-get install --reinstall pantheon-shell wingpanel
   $ gsettings set org.pantheon.desktop.wingpanel blacklist "['libappmenu.so']"
   $ killall wingpanel                          
  ```

## [Instalar Fish](https://github.com/fisherman/fisherman/wiki/Installing-Fish)

* install [fisherman](https://github.com/fisherman/fisherman/wiki/Quickstart-Guide)

* install [oh my fish](https://github.com/oh-my-fish/oh-my-fish)

## [Cambiar Splash Screen](http://gnome-look.org/content/show.php?content=171239)

## Mi configuracion

* Iconos        

  [Yosemite Icons](http://zacpier.deviantart.com/art/Yosemite-Icons-for-Linux-494175906)
 


## [personalizar iconos de lanzadores](https://burguerblog.wordpress.com/2015/11/30/como-personalizar-facilmente-nuestros-lanzadores-en-elementary-os-freya/)


## Compiz

```sh
sudo apt-get install compiz compizconfig-settings-manager compiz-plugins-extras
```
