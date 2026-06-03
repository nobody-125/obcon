Linux is a monolithic multitasking kernel from which the family of GNU/Linux operating systems are built upon.
It is primarily responsible for 4 things: processes, allocating memory, acting as the layer between the hardware and processes, and receiving and processing system calls.
##### Process Management
Linux is built upon preemptive multitasking, meaning that while it may appear that a Linux OS can run multiple processes simultaneously, in reality processes do not run at *exactly* the same time. Subsequently the kernel is responsible for deciding when to switch between processes and threads.
	 The kernel allocates "time slices" to processes, allowing them adequate time to finish a significant computation. The kernel scheduler has complete freedom to decide if the task should keep running, or if it should switch. This happens through context switching, essentially a series of interactions between the kernel and CPU.
All of this is in contrast to cooperative multitasking, found on many older systems such as classic Mac OS. Processes were given the freedom to decide when to relinquish resources, meaning that if one process was to hang, the entire system would no longer function.
##### Memory Management
During context switching, the kernel is responsible for memory management. This is achieved through VRAM, tricking processes into believing they have an entire machine's worth of memory to themselves. From there, the CPU's memory management unit translates the memory location in the process to the physical memory location. 
##### Device Drivers
Device drivers are often included as part of the kernel to simplify developers' jobs since programming interfaces widely vary across drivers, regardless of if they achieve the same task. Most drivers included in the kernel are proprietary blobs.
##### System Calls
System calls are the way that processes access the aforementioned kernel features. They are often used for opening, reading and writing files. This includes most userspace applications. When the user runs a shell command, like `ls`, the process uses system call `fork()` to create a copy of the shell. This copy then calls `exec(ls)` to start `ls`. 