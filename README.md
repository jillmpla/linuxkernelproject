<b>A loadable Linux Kernel Module (LKM) that can read and write between user-space and kernel-space, via /proc.</b>

Focus was placed on learning about and understanding /proc, how to communicate between user-space and kernel-space, as well as how to load and unload Kernel modules while the kernel is running.

<b>Overview:</b>

- The proc file system is a virtual file system created when the system boots and destroyed at system shut down. It contains information about various processes running and is generally considered the main kernel information source.
- Linux kernel supports loadable device drivers / kernel modules. These can be added at runtime and they can be added without recompiling the entire kernel. They are particularly useful when working with kernel code.

<b>To Use:</b>
- install Linux headers - apt-get install linux-headers-generic
- run make command within directory procfun.c and accompanying make file are located
- insmod procfun.ko - loads the module into the kernel
- lsmod - lists which loadable kernel modules are currently running
- rmmod procfun - removes module from kernel



Please view powerpoint (Linux.pptx file) for further details on the project.

Linux type/Kernel version used - Linux Mint 19.2, kernel 4.15.0-54-generic, x86-64 architecture.
