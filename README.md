How to build:

* `pacman -S dtc android-tools sunxi-tools patch`
* install from AUR simg-tools
* install from AUR arm-linux-gnueabihf-gcc
  * correct order of the dependencies [source](https://aur.archlinux.org/packages/arm-linux-gnueabihf-gcc/):
    * `arm-linux-gnueabihf-binutils`
    * `arm-linux-gnueabihf-gcc-stage1`, also requires `flex` [source](https://github.com/golang/go/issues/316)
    * `arm-linux-gnueabihf-linux-api-headers`
    * arm-linux-gnueabihf-glibc-headers
    * arm-linux-gnueabihf-gcc-stage2
    * arm-linux-gnueabihf-glibc
    * arm-linux-gnueabihf-gcc
  * in case of missing GPG keys [source](https://aur.archlinux.org/packages/mingw-w64-binutils/):
    * `gpg --recv-keys 13FCEF89DD9E3C4F` (req'd by `arm-linux-gnueabihf-binutils`)
    * `gpg --recv-keys BBE43771487328A9` (req'd by `arm-linux-gnueabihf-gcc-stage1`)
    * `gpg --recv-keys 38DBBDC86092693E` (req'd by `arm-linux-gnueabihf-linux-api-headers`)
* `git clone https://github.com/mydzor/chip-arch-build.git`
* `cd chip-arch-build`
* `git submodule init`
* `git submodule update`
* `./build.sh`

More info:
http://www.chip-community.org/index.php/Archlinuxarm_on_chip
