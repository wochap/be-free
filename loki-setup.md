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
