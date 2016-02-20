# Performance (Elementary OS)

## 1. [Change swappiness value](http://askubuntu.com/questions/157793/why-is-swap-being-used-even-though-i-have-plenty-of-free-ram)

```sh
# to check the swappiness value
$ cat /proc/sys/vm/swappiness

# To change the swappiness value A temporary change (lost on reboot) 
$ sudo sysctl vm.swappiness=10

# To make a change permanent, edit the configuration file with your favorite editor:
$ sudo subl /etc/sysctl.conf

# Search for vm.swappiness and change its value as desired. If vm.swappiness does not exist, add it to the end of the file like so:
vm.swappiness=10
```

## 2. [Setting up a trim job on Freya](http://elementaryos.stackexchange.com/questions/1199/how-do-i-optimize-my-ssd-with-trim-in-freya)

```sh
# Type in the terminal: 
$ sudo subl /etc/rc.local
```

Above the line exit 0 in that file, you now add the TRIM command fstrim for every automatically mounted EXT4 partition.
If you have a separate home partition, then you add the following line as well, above exit 0: fstrim /home

```
# /etc/rc.local

#!/bin/sh -e
#
# rc.local
#
# This script is executed at the end of each multiuser runlevel.
# Make sure that the script will "exit 0" on success or any other
# value on error.
#
# In order to enable or disable this script just change the execution
# bits.
#
# By default this script does nothing.

# Trim SDD
fstrim /
fstrim /home

exit 0
```
