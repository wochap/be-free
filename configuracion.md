# Configuración de eOS

## Cambiar comportamiento al cerrar la tapa de la laptop

* Para ello, ariremos una terminal en la que escribiremos:

  ```sh
  $ sudo gedit /etc/systemd/logind.conf
  ```

* En el fichero que se abrirá, busca la línea:

  `#HandleLidSwitch=suspend`

* y descoméntala (borra el símbolo # del inicio)

* Ahora cambia la palabra "suspend" por la acción que quieres que ejecute el sistema al cerrar la pantalla:

  HandleLidSwitch=poweroff para apagar el ordenador cuando se cierre la pantalla.
  HandleLidSwitch=hibernate para hibernar el ordenador cuando se cierre la pantalla
  HandleLidSwitch=ignore para no hacer nada

* Reinicia el sistema. 

## [Continuar escuchando la musica al bloquear (lock screen)](http://elementaryos.stackexchange.com/questions/3468/is-it-possible-to-continue-playing-music-even-system-gets-locked-for-inactivity)

```
$ sudo usermod -a -G audio <myusername>
```

