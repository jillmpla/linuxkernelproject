<b>A loadable Linux Kernel Module (LKM) that can read and write between user-space and kernel-space, using /proc.</b>

Focus was placed on learning about and understanding /proc, how to communicate between user-space and kernel-space, as well as how to load and unload kernel modules while the kernel is running.

<b>Overview:</b>

- The proc file system is a virtual file system created when the system boots and destroyed at system shut down. It contains information about various processes running and is generally considered the main kernel information source while the kernel is running.
- Linux kernel supports loadable device drivers / kernel modules. These can be added at runtime and can be added without recompiling the entire kernel. They are particularly useful when developing for the kernel and debugging the kernel while the kernel is live.
- After building the C program, it can be loaded to create a new file under /proc.
- Current development status can be written and read via the command-line / user-space, helping to keep track of what was last edited, when it was last edited, and who last edited it.
- Can easily be repurposed to keep track of other information relevant while the Linux OS/kernel is live and running.

<b>To Use on a Linux machine:</b>
- download procfun.c and Makefile from folder "Code" in this GitHub
- <i>sudo -s</i> - to stay in superuser mode
- <i>apt-get install linux-headers-generic</i> - installs Linux headers (if you need to)
- run <i>make</i> command within directory procfun.c and accompanying Makefile are located
- <i>insmod procfun.ko</i> - loads the module into the kernel
- <b>Write: </b><i>echo "Date:12/01/19, Time:12:00PM, Working on:/proc file system, Author:JPlatts" >> /proc/devstate</i> - overwrites previous development state message
- <b>Read: </b><i>cat /proc/devstate</i> - get current development state message
- <i>lsmod</i> - lists which loadable kernel modules are currently running, look for procfun
- <i>rmmod procfun</i> - removes module from kernel

Please view powerpoint (Linux.pptx file) for further details on the project.

<b>Linux distribution/kernel used - Linux Mint 19.2, kernel: 4.15.0-54-generic, x86-64 architecture.</b>
