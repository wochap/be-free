# Loki Setup (Elementary OS)

## 1. Fixes

### Post install

```sh
$ sudo apt-get update
$ sudo apt-get install software-properties-common
```

### Brightness

```sh
$ sudo apt-get install xdotool

# Change brightness with commands
$ xdotool key XF86MonBrightnessDown
$ xdotool key XF86MonBrightnessUp
```sh

## 2. Apps

### [Tweaks](https://github.com/elementary-tweaks/elementary-tweaks)

```sh
$ sudo add-apt-repository ppa:philip.scott/elementary-tweaks
$ sudo apt-get update
$ sudo apt-get install elementary-tweaks
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
* Gnome System Monitor
```sh
$ sudo apt-get install gnome-system-monitor
```

### Chrome

```sh
# add PPA repo
$ wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
$ sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'

# install
$ sudo apt-get update
$ sudo apt-get install google-chrome-stable
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
