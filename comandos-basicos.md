# Comandos basicos

- Ubicar un ejecutable
```sh
$ which <nombre_del_ejecutable> 
```

- Ingresar como superusuario
```sh
$ sudo su
```

- Cambiar permisos de una carpeta
```sh
$ sudo chmod -R 777 <nombre_de_la_carpeta>
```

- Ver la ruta completa en la que te encuentras
```sh
$ pwd
```

- Cambiar propietario de una carpeta y todo su contenido
```sh
$ sudo chown <usuario> -R <carpeta>
```

- Cambiar permisos a futuros archivos de una carpeta
```sh
$ sudo setfacl -Rdm g:groupnamehere:rwx <carpeta>

$ sudo umask 0000
```


- Montar disco ([Solve Windows Partition Mount Problem In Ubuntu Dual Boot](Solve Windows Partition Mount Problem In Ubuntu Dual Boot))
```sh
$ sudo ntfsfix /dev/sdXY
```

## [Ver informacion de tu hardware](http://www.thegeekstuff.com/2008/11/how-to-get-hardware-information-on-linux-using-dmidecode-command/)

| Keyword   | Types     |
|-----------|:---------:|
| bios   | 0, 13   |
| system   | 1, 12, 15, 23, 32   |
| baseboard   | 2, 10   |
| chassis   | 3   |
| processor   | 4   |
| memory   | string   |
| memory   | string   |
| memory   | string   |
| memory   | string   |

```sh
$ sudo dmidecode -t bios -q
```




## Grub 

```sh
$ root=(hd0,gpt7)       
$ configfile /boot/grub/grub.cfg
```
