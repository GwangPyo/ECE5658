Arachne is introduced to solve the high throuput and low latency at the same time. 
Under traditional operating systems, application can only interact with the OS with virtual resource of CPU, threads. It is undesirable 
because there are not so much information to OS, which results in under utilization and over commitment. 

Thus Arachne gives visiblity of the physical resource, the CPU cores, to application. Some application using threads only for fast response time will requires less core, while application using thread 
to achieve high throughput will requires large number of cores.

The core will negotiated by core arbiter. 
In implementation level, the core arbiter is implemented in user-level, not kernel level. Thus, it does not requires kernel rebuild, 
and moreover, Arachne can coexists with traditional application at the same time; which solves legacy issues. 
