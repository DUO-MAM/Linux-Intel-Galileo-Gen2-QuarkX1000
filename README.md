# Linux-Intel-Galileo-Gen2-QuarkX1000

Contains a Linux 3.8.7 source code with all patches for Intel Galileo Gen2 ( Quark X1000 SoC ), so it is 3.8.7-yocto-standard source.  
  
The .config file was copied from /proc/config.gz on a system running a kernel compiled by Intel. The kernel is compiled with symbol information to facilitate debugging.  
  
The BSPv1.1.0/x86_64-linux.tar.gz archive contains cross-compiler for Ubuntu 14 x64. This is a stripped down version of meta-clanton build environment.  
  
To build the kernel. ( Below YOUR-DIR stands for a full path to a working directory on your machine, i.e. /work/mykernel )  
  
$ mkdir YOUR-DIR  
$ cd YOUR-DIR  
$ git clone https://github.com/slavaim/Linux-Intel-Galileo-Gen2-QuarkX1000  
$ cd Linux-Intel-Galileo-Gen2-QuarkX1000/BSPv1.1.0  
$ tar zxf x86_64-linux.tar.gz  
$ cd linux_v3.8.7/work  
$ export PATH=YOUR-DIR/Linux-Intel-Galileo-Gen2-QuarkX1000/BSPv1.1.0/x86_64-linux/usr/bin/i586-poky-linux:$PATH  
$ ARCH=i386 CROSS_COMPILE=i586-poky-linux- make  
  
The built kernel is BSPv1.1.0/linux_v3.8.7/work/arch/x86/boot/bzImage  
