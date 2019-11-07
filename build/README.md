# About build qemu and xv6
Q:How to get qemu?  
A:git clone https://github.com/mit-pdos/6.828-qemu.git qemu 
(However it usually works slowly.There may be a solution for you: clone this repo to 
gitee and download, or git clone https://gitee.com/jackyzt/6.828-qemu.git qemu) 

Q:How to build qemu?  
A: cd qemu  
   sudo ./configue  
   sudo make  
   sudo make install  
  In my machine:Linux jacky 4.15.0-55-generic #60-Ubuntu SMP Tue Jul 2 18:22:20 UTC 2019   
x86_64 x86_64 x86_64 GNU/Linux, I have to install some libraries like libsdl1.2-dev,  
libtool-bin,libglib2.0-dev,libz-dev,and libpixman-1-dev.  
  Two Errors when you start to build it.   
  1).qga/commands-posix.c:633:13: error: In the GNU C Library, "major" is defined  
  2).block/blkdebug.c:749:31: error: ‘%s’ directive output may be truncated writing up to   
     4095 bytes into a region of size 4086 [-Werror=format-truncation=]  
  First of all, add header file (#include <sys/sysmacros.h>) to qga/commands-posix.c, and   
  then sudo ./configure --disable-werror (ingore warnings).  

Q:How to get xv6?  
A:git clone  https://pdos.csail.mit.edu/6.828/2018/jos.git lab  

Q:How to build and start xv6?  
A: cd lab  
   make  
   make qemu  

If you get no error, you will get the following information :  
  qemu-system-i386 -drive file=obj/kern/kernel.img,index=0,media=disk,format=raw -serial mon:stdio -gdb tcp::26000 -D qemu.log  
VNC server running on `::1:5900'  
  ......  
  Type 'help' for a list of commands.  
  K>  

