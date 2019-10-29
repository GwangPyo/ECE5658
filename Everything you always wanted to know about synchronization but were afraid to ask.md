In modern concurrency system design, it is difficult to the system scalable or not at frist, but it is able to determine in experience.
This is because, there are no results on modern architectures connecting the low-level details of the underlying hardware. 

That is, it is not clear if the issues are due to the underlying hardware,to the synchronization algorithm itself, 
to its usage of specific atomic operations, to the application context, or to the workload.

The aurthors analyzed the problem via measuring the performacne for each synchronization layers; 
latency of cache coherency protocol, atomic operation performacne, concurrent hash table...

And also they analyzed the infulence of the architectural attributes; single socket chips vs multi-socket chips 


The result is following.

Crossing socket is significant to synchronization. However, it is inevitable for every case. In this case, message passing may be a solution,
but message passing still has a problem with cost of lower performance (than locks) on a few cores or low contention.

Multi-socket coherence using broadcast or an incomplete directory is not favorable to synchronization.

Also  non-uniformity affects scalability even within a single-socket architecure. 

For the lock, Spin lock should be preferred than complex ones. Complex locks only outperform spin locks under relatively high contention.

