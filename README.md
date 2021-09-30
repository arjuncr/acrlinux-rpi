# acrlinux-rpi-yocto

Build Steps:  

git clone --recurse-submodules https://github.com/arjuncr/acrlinux-rpi-yocto.git      

cd acrlinux-rpi-yocto   

TEMPLATECONF=meta-raspberrypi/conf/ . oe-init-build-env

bitbake core-image-base      

```
Parsing recipes: 100% |#################################################################################| Time: 0:01:25
Parsing of 2200 .bb files complete (0 cached, 2200 parsed). 3294 targets, 143 skipped, 0 masked, 0 errors.
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
meta-yocto-bsp
meta-acrlinux
meta-raspberrypi
meta-oe
meta-multimedia
meta-networking
meta-python          = "master:03676983f69f1b5896a22237c984eca7d6485220"
```

Build Image Location:  
build/tmp/deploy/images/repberrypi4/core-image-base-raspberrypi4.wic.bz2    

Extract The zip:  
bzip2 -d -f tmp/deploy/images/raspberrypi4/core-image-base-raspberrypi4.wic.bz2   

Then Copy Image To sd Card  
https://www.raspberrypi.org/documentation/installation/installing-images/
