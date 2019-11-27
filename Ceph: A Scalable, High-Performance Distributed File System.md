Ceph is a distributed file system leverages separation between data management and meta datamangement.

This separation relies on CRUSH, a data distribution function, which allows client to compute object location
rather than looking up. 

It distribute replica of data, so that failure detection and recovery is done in semi-autonomous manner, with RADOS.
By occupying a unique point in the design space, it gaurantees scalability, performance, and reliablity.

and EBOFS provides provides sophisticated semantic and high performance by addressing the specific workloads and interface.

The metadata management architecture provides scalable storages, obeying POSIX semantics. 
