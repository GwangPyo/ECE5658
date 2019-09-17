This paper argues that the Linux kernel scheduler's bug which let some cores idel, while others be busy.
Mixed up many optimization techniques which are not decouplized, we could not control the total scheduling algorithm as we desired,
especially for the load balancing problem. 

To solve the problem, the author suggests that the load balancing paradigm considering both threads' weights and CPU utilization. 
Moreover, since there are still NUMA problem, and thread migration, the author also suggests to use the cgroup feature; load balancing 
considering structure of CPU. 
