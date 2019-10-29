Contribution:
1. Introduce the concept sloppy counter
2. Set of application benchmark MOSBENCH 
3. Increase scalability of MOSBENCH application

MOSBENCH applications are consists of 
1. mail server (Exim)
2. object cache (memcached)
3. web server (apache)
4. data base (PostgreSQL)
5. parallel build (gmake)
6. file indexer (Psearchy) 


Sloppy counter is the new concept introduced in this paper. 

The idea is that for the many counter, it is okay to let reading expensive or overestimate.
For example, it is crucial that a garbage collector remove an object which is in use for the reference counter 
(under-estimate reference cunter)
However, since garbage collector is executed very less frequently than the code, it is not so harmful paying expensive to check 
whether a reference counter is 0.

Sloppy counter := base counter + local counter
   
The actual value of sloppy counter is sum of local counters 
If need to increment, first try local core's value, then get spinlock for base
If need to decrement,  just add to local core's value

But checking whether it is zero is expensive because, it bus locked. 

Conclusion

Small portion of modification to applications or kernel, we can remove most kernel bottleneck. 
