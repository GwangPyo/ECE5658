Problems
----------
# For the crash consistency, or collision consistency, most of applications leverage complex protocol such as 
atomic rename or logging
# And, for all cases, the application cannot help using fsync syscall to achieve these protocol. 
 fsync is very  expensive

Sol
-----
# TxFS is transactional file system which leverages the file system journal
## Transaction presents an intuitive way to atomically update persistent state. 
# Under the transactional file system, they can do optimize the system such as 
## Eliminate temp durable files 
### e.g., vim, git are using this approaches, and inefficient as if the size of file grows up
## Group commit 
### via Batching updates 
## Eliminate redundant IO across transactions 
### Because transactions are visible to file system at commit time; allowing global optimization
## Consolidate IO across transactions
### With some flags, application can delay the commit time as it expects that data would be overwritten 
## Seperate ordering from durablity 
### fsync may not used if one may wants to preserves order,but need not for durability. 

# TxFS has simple API a single syscall to begin, end, abort 
