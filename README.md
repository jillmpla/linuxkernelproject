<b>A loadable Linux Kernel Module (LKM) that can read and write between user-space and kernel-space, via /proc.</b>

Focus was placed on learning about and understanding /proc, how to communicate between user-space and kernel-space, as well as how to load and unload Kernel modules while the kernel is running.

<b>Overview:</b>

- The proc file system is a virtual file system created when the system boots and destroyed at system shut down. It contains information about various processes running and is generally considered the main kernel information source.
- Linux kernel supports loadable device drivers / kernel modules. These can be added at runtime and can be added without recompiling the entire kernel. They are particularly useful when developing for the kernel.

<b>To Use:</b>
- download procfun.c and Makefile from folder "ToUse" in this GitHub
- <i>sudo -s</i> - to stay in superuser mode
- <i>apt-get install linux-headers-generic</i> - installs Linux headers
- run <i>make</i> command within directory procfun.c and accompanying Makefile are located
- <i>insmod procfun.ko</i> - loads the module into the kernel
- <i>cat /proc/magiceightball</i> - make sure the /proc entry was made
- <i>lsmod</i> - lists which loadable kernel modules are currently running, look for procfun
- <i>rmmod procfun</i> - removes module from kernel

Please view powerpoint (Linux.pptx file) for further details on the project.

<b>Linux distribution/kernel used - Linux Mint 19.2, kernel 4.15.0-54-generic, x86-64 architecture.</b>
