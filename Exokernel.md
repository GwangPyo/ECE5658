Exokernel
============= 
Exokernel has philosophy that minimize the role of the kernel between users and device to achieve performance.
Thus, it tries to give the lowest-level interface of devices to applications, 
which induces to the goal of seperating protection from manangement.

In this sense, it is very similar to virtual machines, while exokernel export the hardware rather than emulate because of performance. 

Meanwhile, exokernel is very similar to microkernel, but unlike microkernel, exokernel can modify an application specific abstraction 
such as IPC.  
