How to build:

* `pacman -S dtc android-tools sunxi-tools patch`
* install from AUR simg-tools
* install from AUR arm-linux-gnueabihf-gcc
  * correct order of the dependencies [source](https://aur.archlinux.org/packages/arm-linux-gnueabihf-gcc/):
    * arm-linux-gnueabihf-binutils
    * arm-linux-gnueabihf-gcc-stage1
    * arm-linux-gnueabihf-linux-api-headers
    * arm-linux-gnueabihf-glibc-headers
    * arm-linux-gnueabihf-gcc-stage2
    * arm-linux-gnueabihf-glibc
    * arm-linux-gnueabihf-gcc
  * in case of missing GPG key: `gpg --recv-keys 13FCEF89DD9E3C4F` [source](https://aur.archlinux.org/packages/mingw-w64-binutils/)
* `git clone https://github.com/mydzor/chip-arch-build.git`
* `cd chip-arch-build`
* `git submodule init`
* `git submodule update`
* `./build.sh`

More info:
http://www.chip-community.org/index.php/Archlinuxarm_on_chip
