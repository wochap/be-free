# Instalar Android Studio en elementary o cualquier distro

## [Java 8](http://zonaelementaryos.com/2015/09/02/instalar-java-8-en-elementary-os/)

```sh
  $ sudo add-apt-repository ppa:webupd8team/java           
  $ sudo apt-get update                  
  $ sudo apt-get install oracle-java8-installer                          
```

## [Android Studio](https://juanpc617.wordpress.com/2015/03/02/instalar-android-studio-en-elementary-os-luna/)

```sh
# before install
$ sudo apt-get install lib32stdc++6

# after install
# create desktop 
$ nano ~/.local/share/applications/androidstudio.desktop

[Desktop Entry]
Version=1.0
Type=Application
Name=Android Studio
Exec="/opt/android-studio/bin/studio.sh" %f
Icon=/opt/android-studio/bin/studio.png
Categories=Development;IDE;
Terminal=false
StartupNotify=true
StartupWMClass=android-studio
```


