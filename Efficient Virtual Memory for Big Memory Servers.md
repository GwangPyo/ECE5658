Although some main purposes of the virtual memory are 
i. Swapping
ii. Fragmentation mitiagtion
iii. Fine grained protection

The authors observed that many big-memory process does not requires these 3-features.
Moreover, they claim that current page based virtual memory system is the perforamcne
bottleneck for big memory processes, especially for the TLB miss Thus, they propose 
new memory system with assumption that big-memory process and without dynamic execution
environment. 

The key point is reducing TLB miss overhead. 

While there are limitation in the current system's solution. Current systems try to
reduce page miss via large page sizes. However, it is neither scalable (e.g. TLB's 
poor locality), nor flexible (e.g., x86-64 architecture's 4kb, 2mb, 1gb pages is too
far apart) and has mircro architecture dependancy.


The 3-mechanisms the author suggeseted are following
i. Do not export two-dimensional address space to applications, but retain a standard 
linear address space.
ii. Do not replace paging: addresses outside the segment use paging. 
iii. Do not operate on top of paging: direct segments are not paged. 

By doing so, they assert that we can not only reduce TLB miss, but also memory refer for 
virtualized environment, and almost fully direct map kernel memory. 
