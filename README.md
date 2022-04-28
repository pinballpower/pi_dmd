# Pi DMD
How to use a Raspberry PI as DMD renderer and more

## Install from scratch

### Install Raspberry Pi OS

Make sure, you use the latest releases based on Debian "Bullseye". As a graphical user interface isn't supported, the "Lite" version is recommended. 

### Install minimal packages

```
sudo apt update
sudo apt -y dist-upgrade
sudo apt install git
``` 

### Enable SPI

Edit /boot/config.txt and make sure
```
dtparam=spi=on
```
is configured. If you change this file, you need to reboot the system before to activate the change.

### Pi DMDReader

This is the software that runs directly on the Pi.
```
git clone https://github.com/pinballpower/code_dmdreader
cd code_dmdreader
. install-pi-software.sh
. compile-pi.sh
´´´
