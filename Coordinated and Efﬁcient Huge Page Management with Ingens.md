Although there are many approaches to support huge page size, the software support has not been enough.
Linux, the most popular OS behaves aggressive and greedy, which invokes problems for huge pages.
1. Latency
2. Bloat
3. Unfair 
4. Fragmentation 

The authors suggest Ingens framework.  Ingens manages contiguity as a first-class resource.
and tracks utilization and access frequency of memory pages, enabling it to eliminate pathologies that plague current systems. 
i.e., Monitoring space and time, util vector, access bits 

Via utilize base promotion and demotion Ingens solves bloat and performance issues, and Proactive batched compaction reduces 
fragmentation. Balancing page sharing and fair sharing solves unfairness for the performance issues. 

However, there are page level false sharing in NUMA architecture, which is not solved. 
