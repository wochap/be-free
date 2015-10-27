# Comandos basicos

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


