# baseimage-MIPS
Create base docker images by using Febootstrap.
==
1. introduction of Febootstrap
Febootstrap is a tool that allows us to make native OS base images, such as Centos, Ubuntu and other operating systems. It can also specify the installation of specific software into the image, which makes it easier for us to understand and control the composition of the base image. Finally, the base image is expanded into an application image to finally deploy the service.

2. installation of Febootstrap
  Since the Febootstrap does not exist in the default source on the Kylin7 system, it cannot be installed directly with yum. But you can download the rpm package on Kylin6. Here is the link:http://download.cs2c.com.cn/neokylin/server/releases/6.0/ls_64/Packages/

1) download rpm package

Here is the Febootstrap and its dependent rpm package. Download to the local, and install directly.(rpm -ivh *.rpm)
  fakechroot-2.9-24.5.ns6.0.01.mips64el.rpm
  fakeroot-libs-1.12.2-22.2.ns6.0.1.mips64el.rpm
  fakechroot-libs-2.9-24.5.ns6.0.01.mips64el.rpm
  febootstrap-2.7-1.2.ns6.0.1.mips64el.rpm
  fakeroot-1.12.2-22.2.ns6.0.1.mips64el.rpm

2)operations of Febootstrap
febootstrap -i bash -i wget neokylin7 neokylin-base http://download.cs2c.com.cn/neokylin/server/releases/7.0/ls_64

-i  Package that needs to be installed, for example, install bash, wget here
neokylin7   Operating system version
neokylin-base   Image directory, for example, generate neokylin-base directory in the current directory here
http://download.cs2c.com.cn/neokylin/server/releases/7.0/ls_64   Mirror OS source address



