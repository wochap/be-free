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
