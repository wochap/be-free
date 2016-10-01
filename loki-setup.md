# Loki Setup (Elementary OS)

## 1. Fixes

### Graphic drivers

add this [ppa](https://launchpad.net/~oibaf/+archive/ubuntu/graphics-drivers) and update your system

### Compatibilidad con Android y Iphone/Ipod 

```sh
$ sudo apt install mtp-tools ipheth-utils ideviceinstaller ifuse
```

### Post install

```sh
$ sudo apt-get update
$ sudo apt-get install software-properties-common
$ sudo apt-get install autoconf
```

### Brightness

```sh
$ sudo apt-get install xdotool

# Change brightness with commands
$ xdotool key XF86MonBrightnessDown
$ xdotool key XF86MonBrightnessUp
```

## 2. Apps

### [Tweaks](https://github.com/elementary-tweaks/elementary-tweaks)

```sh
$ sudo add-apt-repository ppa:philip.scott/elementary-tweaks
$ sudo apt-get update
$ sudo apt-get install elementary-tweaks

# Freya
$ curl -sL  http://i-hate-farms.github.io/spores/install | sudo bash - 
$ sudo apt-get install elementary-tweaks
```

### [Albert](https://github.com/ManuelSchneid3r/albert)

```sh
$ sudo add-apt-repository ppa:noobslab/macbuntu
$ sudo apt-get update
$ sudo apt-get install albert

# config
# Websearch
# URL: https://www.google.com.pe/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=%s
# URL: https://github.com/search?utf8=✓&q=%s
# Name: Google
# Trigger: gg
```

### Snap

Universal linux app packages

Explore snap packages, [here](https://uappexplorer.com/apps?type=snappy)

```sh
$ sudo apt install snapd

# For create a snap
# $ sudo apt install snapcraft
```

### Many apps

* [Rambox](http://rambox.pro/)
* [Katu](https://github.com/EragonJ/Kaku)
* Gitkraken
* Gitter
* Hourglass
* qbitorrent
* Nylas n1
* Simplenote
* Shutter
* Y PPA Manager
* Gpick
* Spotify
* Simple Screen Recorder
* Caffeine Plus
* [Shotcut](https://www.shotcut.org/download/)
* Gnome System Monitor
```sh
$ sudo apt-get install gnome-system-monitor
```

### VLC

```sh
$ sudo apt-get install vlc
```

### Chrome

```sh
# add PPA repo
$ wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
$ sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'

# install
$ sudo apt-get update
$ sudo apt-get install google-chrome-stable

# remove duplicate file
# /etc/apt/sources.list.d/google.list
```

### Spotify

```sh
# 1. Add the Spotify repository signing key to be able to verify downloaded packages
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BBEBDCB318AD50EC6865090613B00F1FD2C19886

# 2. Add the Spotify repository
echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list

# 3. Update list of available packages
sudo apt-get update

# 4. Install Spotify
sudo apt-get install spotify-client
```

### [Silentcast](https://github.com/colinkeenan/silentcast)

```sh
$ sudo add-apt-repository ppa:sethj/silentcast
$ sudo apt-get update
$ sudo apt-get install silentcast
```

### [Wine + PlayOnLinux](http://zonaelementaryos.com/2015/05/13/instalar-playonlinux-en-elementary-os/)

```sh
# 14.04 only
$ sudo apt-get install wine

# trow GPG error
$ wget -q "http://deb.playonlinux.com/public.gpg" -O- | sudo apt-key add - sudo wget http://deb.playonlinux.com/playonlinux_trusty.list -O /etc/apt/sources.list.d/playonlinux.list
$ sudo apt-get update
$ sudo apt-get install playonlinux
```

# 3. SSD Config

### [Create a ram disk](http://www.hecticgeek.com/2015/12/create-ram-disk-ubuntu-linux/) [for](https://bugs.launchpad.net/elementaryos/+bug/1415516):

* /var/log
* /tmp 
* /var/cache/apt/archives
* /home/%NOMUSR%/.cache

```sh
$ sudo mkdir /mnt/ram   
$ sudo cp /etc/fstab /etc/fstab.bak

# add/update lines as
tmpfs /mnt/ram tmpfs rw,size=1G,x-gvfs-show 0 0

tmpfs /var/log tmpfs defaults,nosuid,nodev,noatime,mode=0755,size=5% 0 0
tmpfs /var/cache/apt/archives tmpfs defaults,size=4g 0 0
tmpfs /home/%NOMUSR%/.cache tmpfs defaults,size=1g 0 0
```

### [No Writes for Read Timestamps](http://askubuntu.com/questions/1400/how-do-i-optimize-the-os-for-ssds)

add noatime, nodiratime

```sh
# /etc/fstab

# / was on /dev/sda2 during installation
UUID=587e0dc5-2db1-4cd9-9792-a5459a7bcfd2 /               ext4    noatime,nodiratime,errors=remount-ro 0       1

# /home was on /dev/sda3 during installation
UUID=2c919dc4-24de-474f-8da0-14c7e1240ab8 /home           ext4    noatime,nodiratime,defaults        0       2
```

### [Enable TRIM](http://askubuntu.com/questions/18903/how-to-enable-trim)

## 4. Tunes

### Font family

Install [Fira Code](https://github.com/tonsky/FiraCode)

Install [San Francisco](https://developer.apple.com/fonts/)

### Icons

Install [Capitaine Cursors](https://www.gnome-look.org/p/1148692/)

Install [Elementary Plus](https://github.com/mank319/elementaryPlus)

### Themes

[Xenite](https://github.com/Xenite/Xenite)

[Panther](https://www.gnome-look.org/p/1150507/)

[Arc light](https://www.gnome-look.org/p/1013344/)

[Arc dark](https://www.gnome-look.org/p/1013481/)

[Flatabulous](https://github.com/anmoljagetia/Flatabulous) (ubuntu)
