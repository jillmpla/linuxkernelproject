<b>A loadable Linux Kernel Module (LKM) that can read and write between user-space and kernel-space, via /proc.</b>

Focus was placed on learning about and understanding /proc, how to communicate between user-space and kernel-space, as well as how to load and unload Kernel modules while the kernel is running.

<b>Overview:</b>

- The proc file system is a virtual file system created when the system boots and destroyed at system shut down. It contains information about various processes running and is generally considered the main kernel information source.
- Linux kernel supports loadable device drivers / kernel modules. These can be added at runtime and they can be added without recompiling the entire kernel. They are particularly useful when working with kernel code.


- install Linux headers - apt-get install linux-headers-generic //delete this


Please view powerpoint (Linux.pptx file) for further details on the project.

Kernel version used - <a href="https://cdn.kernel.org/pub/linux/kernel/v4.x/linux-4.19.87.tar.xz">4.19.87</a>
