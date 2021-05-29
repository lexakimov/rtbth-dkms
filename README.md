This is a Linux kernel module for a Ralink RT3290 wireless device.
It enables [Bluez](http://www.bluez.org) software and driver support for RT3290.

This module has no official support by Mediatek. Support was discontinued.

This version also supports linux 5.12.

## Installation: ##
*Adapted for Arch and derivatives (e.g. Manjaro).*

Before build, install corresponding version of `linux-headers` package for you kernel.
```sh
# example (kernel version 5.12)
sudo pacman -S linux512-headers
```

#### Build and install kernel module ####

```sh
# clean previously compiled files
make clean

# build module
make

# install kernel module
sudo make install

# next, add `rtbth` (without quotes) to the end of file /etc/modules-load.d/modules.conf

# then, reboot PC:
sudo reboot now
```

#### Further setup ####
A further setup described [here](https://wiki.archlinux.org/title/Bluetooth).
