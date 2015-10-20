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
  cambias el tema con tweaks
  si no te funciona, copialos tambien en `/usr/share/themes/`

## Instalar [conky](http://elementaryos.stackexchange.com/questions/222/how-install-conky-manager-on-freya)

  * instalacion:  
  ```sh
   $ sudo add-apt-repository ppa:teejee2008/ppa
   $ sudo apt-get update 
   $ sudo apt-get install conky-manager
  ```
  añadir conky-manager al arranque
