# mClock: Handling Throughput Variability for Hypervisor IO Scheduling

#### For the hypervisor, CPU and memories are well scheduled by reservation, share andd limit. However, for the I/O it is not; 
- First, virtualized server access a shared storage device using clustered file system, while sorage device in the guest OS or VM
 is just a large file on the shared storage device. 
- Second, the IO scheduler in the hypervisor needs to handle issues such as locality of accesses across VMs, 
high variability in IO sizes, different request priorities based on the applications running in the VMs, and bursty workloads. 
- Third,  the IO throughput to host can variate widely influenced by the behavior of other hosts accessing the shared device.
That is, a host cannot fully control the IO throughput by its own.

#### M Clock Design Goal 
- Maximize limit and minimize reservation for IO scheduling 
