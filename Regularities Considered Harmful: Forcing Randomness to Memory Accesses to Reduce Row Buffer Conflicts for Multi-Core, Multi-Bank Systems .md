For the multi-core, multi-bank system, row buffer conflicts can be significantly happen and degrade DRAM latency seriously. 
A row buffer is a kind of cache for each Bank, and row buffer conflicts happens when a sequence of requests on different rows
goes to the same memory bank. 
That is, if different threads accessing different page frame in the same memory bank, row buffer conflicts will be significant. 
The authors suggests to randomize the memory access pattern to reduce this kind of situation, and yields better performance.

The author modified allocator to satisfies  
i. Prevent row buffer conflict when the code is executed by it self on a single core
ii. Incrementing 12 MB starting address from each core, they let memory accessing range be intact from each other.  


The authors has contributions as followings 
  1. For multi-core multi-bank system, the authors suggest to randomized memory access pattern
  2. The author developed kernel-level memory allocator, called M<sup>3 </sup>
  3. The author alos developed memory organization analysis tool 

