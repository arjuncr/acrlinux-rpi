# acrlinux-rpi-yocto
acrlinux-rpi  

Build steps:  

git clone https://github.com/arjuncr/acrlinux-rpi-yocto.git      

cd acrlinux-rpi-yocto   

. oe-init-build-env   

bitbake core-image-base      

```
Parsing recipes: 100% |#################################################################################| Time: 0:00:47
Parsing of 2198 .bb files complete (0 cached, 2198 parsed). 3292 targets, 142 skipped, 0 masked, 0 errors.
NOTE: Resolving any missing task queue dependencies

Build Configuration:
BB_VERSION           = "1.46.0"
BUILD_SYS            = "x86_64-linux"
NATIVELSBSTRING      = "ubuntu-20.04"
TARGET_SYS           = "arm-poky-linux-gnueabi"
MACHINE              = "raspberrypi4"
DISTRO               = "poky"
DISTRO_VERSION       = "3.1.11"
TUNE_FEATURES        = "arm vfp cortexa7 neon vfpv4 thumb callconvention-hard"
TARGET_FPU           = "hard"
meta
meta-poky
meta-yocto-bsp       = "dunfell:60cfe38b513d474714500d1f5fcf408139c6a146"
meta-raspberrypi     = "dunfell:59c2d6f7a8b1239bd7b587b9180c2a55f9c695a2"
meta-oe
meta-multimedia
meta-networking
meta-python          = "dunfell:5c347d8ce425dcb4896e6f873810b8bfff5e4e92"

```

build image location:  
tmp/deploy/images/repberrypi4/core-image-base-raspberrypi4.wic.bz2    

extract the zip:  
bzip2 -d -f tmp/deploy/images/raspberrypi4/core-image-base-raspberrypi4.wic.bz2   

Then copy this image to sd card  
https://www.raspberrypi.org/documentation/installation/installing-images/
