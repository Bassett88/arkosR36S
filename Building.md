## Looking to build ArkOS from scratch?

Since ArkOS is based on Ubuntu 19.10 for Arm, the process is different from a typical fully open source software build.  Below describes the process:

* The base ubuntu 19.10 image can be downloaded from [here](https://wiki.odroid.com/odroid_go_advance/os_image/ubuntu_es#v11).
* The mali gpu driver from [here](https://oph.mdrjr.net/meveric/pool/go2/libm/libmali-rk/libmali-rk-bifrost-g31-rxp0-wayland-gbm_1.7-2+deb10_arm64.deb) 
* The sdl2 package from [here](https://www.areascout.at/libsdl2-2.0-0_2.0.10+dfsg1-1ubuntu1_arm64.deb)
* For the kernel, that is dependent on the device you're targeting:
  * [Click here for the RG351P/M](https://github.com/lualiliu/RG351P-linux) - You can build it following the instructions [here](https://github.com/christianhaitian/linux/blob/rg351/README)
  * [Click here for the RG351V](https://github.com/christianhaitian/linux/tree/rg351) - You can build it following the instructions [here](https://github.com/christianhaitian/linux/blob/rg351/README)
  * [Click here for the OGA/RK2020/RGB10](https://github.com/christianhaitian/linux/tree/odroidgoA-4.4.y) - You can build it following the instructions [here](https://github.com/christianhaitian/linux/blob/odroidgoA-4.4.y/README)
  * [Click here for the Chi](https://github.com/shantigilbert/hardkernel-linux/tree/GameForce-Chi) - You can build it following the instructions [here](https://github.com/christianhaitian/linux/blob/odroidgoA-4.4.y/README).  Instead of `make odroidgoa_tweaked_defconfig` do `make gameforce_defconfig`
* For the uboot, that is also dependent on the device you're targeting:
  * [Click here for the OGA, RGB10, and the RK2020](https://github.com/hardkernel/u-boot/tree/odroidgoA-v2017.09)
  * [Click here for the RG351V](https://github.com/christianhaitian/RG351-u-boot/tree/odroidgoA-v2017.09)
  * [Click here for the CHI](https://github.com/christianhaitian/chi-u-boot)

The rest I add via scripted updates from here:
* [RG351P/M](https://github.com/christianhaitian/arkos/blob/main/Update-RG351P.sh)
* [RG351V](https://github.com/christianhaitian/arkos/blob/main/Update-RG351V.sh)
* [RK2020/OGA 1.0](https://github.com/christianhaitian/arkos/blob/main/Update-RK2020.sh)
* [RGB10/OGA 1.1](https://github.com/christianhaitian/arkos/blob/main/Update-RGB10.sh)
* [CHI](https://github.com/christianhaitian/arkos/blob/main/Update-CHI.sh)

Sources I modified myself are available through my github account [here](https://github.com/christianhaitian).

Many of my sources have been modified to support my build process.  My process involves the use of both 32bit and 64bit ARM debian based chroots within an Ubuntu Mate 20.04 Oracle VirtualBox based VM I utilize.  You can download the prebuilt VM either through this [Mega](https://mega.nz/file/3dIkHTRZ#s2DOkT8nrCRCaXVyng3KQdrixolgxarqplitLt8Ta8c) or [Google Drive](https://drive.google.com/file/d/1_6SLtNurqeUafKrbBM2Ba0fTWyZkGAGi/view?usp=sharing) link.

More info about this VM is available [here](https://forum.odroid.com/viewtopic.php?p=306185#p306185).

## To create debian based chroots in a Linux environment.
### These instructions are based on a Ubuntu 16 or newer install or VM.

install Prereqs:

`sudo apt update`
`sudo apt install -y build-essential debootstrap binfmt-support qemu-user-static`

Then install armhf and arm64 chroots:

`sudo qemu-debootstrap --arch armhf buster /mnt/data/armhf http://deb.debian.org/debian/`

`sudo qemu-debootstrap --arch arm64 buster /mnt/data/arm64 http://deb.debian.org/debian/`

To get into chroots:

For 32 bit Arm environment: \
`sudo chroot /mnt/data/armhf/`
or create a Arm32 shortcut on the desktop gui and click on Arm32 shortcut on desktop

For 64 bit Arm environment
`sudo chroot /mnt/data/arm64/`
or create a Arm64 shortcut on the desktop gui and click on Arm64 shortcut on desktop

Helpful tools to install in both environments for RK3326 app builds

`apt -y install build-essential git wget libdrm-dev python3 python3-pip python3-setuptools python3-wheel ninja-build libopenal-dev premake4 autoconf libevdev-dev ffmpeg libsnappy-dev libboost-tools-dev magics++ libboost-thread-dev libboost-all-dev pkg-config zlib1g-dev libpng-dev libsdl2-dev clang cmake cmake-data libarchive13 libcurl4 libfreetype6-dev libjsoncpp1 librhash0 libuv1 mercurial mercurial-common libgbm-dev libsdl2-ttf-2.0-0 libsdl2-ttf-dev`

`ln -s /usr/include/libdrm/ /usr/include/drm`

`pip3 install meson`

`git clone https://github.com/mesonbuild/meson.git`
`ln -s /meson/meson.py /usr/bin/meson`

libgo2 development headers:

`git clone https://github.com/OtherCrashOverride/libgo2.git`
`cd libgo2`
`mkdir -p /usr/include/go2`
`cp src/*.h /usr/include/go2/`
