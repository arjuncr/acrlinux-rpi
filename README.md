# acrlinux-rpi-yocto
acrlinux-rpi  

Build steps:  

git clone https://github.com/arjuncr/acrlinux-rpi-yocto.git      

cd acrlinux-rpi-yocto   

. oe-init-build-env   

bitbake core-image-base    

build image location:  
tmp/deploy/images/repberrypi4/core-image-base-raspberrypi4.wic.bz2    

extract the zip:  
bzip2 -d -f tmp/deploy/images/raspberrypi4/core-image-base-raspberrypi4.wic.bz2   

Then copy this image to sd card  
https://www.raspberrypi.org/documentation/installation/installing-images/
