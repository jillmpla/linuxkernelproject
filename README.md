<b>A loadable Linux Kernel Module (LKM) that creates a "pseudo"-file in /proc and reads/writes a message on the current development state of the running kernel.</b>

Focus was placed on learning about and understanding /proc, how to communicate between user-space and kernel-space, as well as how to load and unload kernel modules while the kernel is running.

<b>Overview:</b>

- The proc file system is a virtual file system created when the system boots and destroyed at system shut down. It contains information about various processes running and is generally considered the main kernel information source about the kernel while the kernel is running.
- Linux kernel supports loadable device drivers / kernel modules. These can be added at runtime and can be added without recompiling the entire kernel. They are particularly useful when developing for the kernel and debugging the kernel while the kernel is live.
- After building the C program available in this GitHub, it can be loaded to create a new "pseudo"-file under /proc.
- Current developer/development status can be written and read via the command-line / user-space, helping to keep track of what part of the kernel was last worked on, when it was last worked on, and who last worked on it.
- <i>Can easily be repurposed to keep track of other information relevant while the Linux OS/kernel is running.</i>

<b>To Use on a Linux machine:</b>
- download devstate.c and Makefile from folder "Code" in this GitHub
- <b>sudo -s</b> - to stay in superuser mode
- <b>apt-get install linux-headers-generic</b> - installs Linux headers (if you need to)
- run <b>make</b> command within directory devstate.c and accompanying Makefile are located
- <b>insmod devstate.ko</b> - loads the module into the kernel
- <b>lsmod</b> - lists kernel modules that are currently running, look for devstate
- <i>To Write: </i><b>echo "Date:12/01/19, Time:12:00PM, Working on:/proc file system, Author:JPlatts" >> /proc/devstate</b> - updates/overwrites previous development state message
- <i>To Read: </i><b>cat /proc/devstate</b> - get current development state message
- <b>rmmod devstate</b> - removes module from kernel

Please view powerpoint (Linux.pptx file) for further details on the project.

<b>Linux distribution/kernel used - Linux Mint 19.2, kernel: 4.15.0-54-generic, x86-64 architecture.</b>
