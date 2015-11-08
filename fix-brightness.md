# How to fix brightness problem

## Option 1: Install xbacklight (work for me)
  
  ```sh
  $ sudo apt-get install xbacklight
  ```
  
## [Option 2](http://itsfoss.com/fix-brightness-ubuntu-1310/) (not work for me)

## [Option 3](http://justplainobvious.blogspot.pe/2014/11/acer-c720-linux-ubuntu-brightness-keys.html) (best)
  
  ```sh
  $ sudo apt-get install xdotool
  $ xdotool key XF86MonBrightnessDown
  $ xdotool key XF86MonBrightnessUp
  ```
