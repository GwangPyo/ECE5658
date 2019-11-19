The paper is focusing on crash consistency: Maintaining data invariants accross a system crash.
They are important in file system, DBMS, key-value stores, etc. However it is difficult to analyse 
crash consisency. For instance, ARIES is announced in 1992 but it tooks 5 years to prove that ARIES
is correct 

The filesystems differs in crash-related behavior while applications usually depend on some behavior.
That is confirming the crash consistency in a single file system does not guarntees crash consistency
in general file systems. 

The authors suggest BOB, the block order breaker, and ALICE, Appplication Level Intelligent Crash Explorer.
BOB works as following
1. Run user level workload stressing the atomicity and ordering 
2. Record block level trace of the workload 
3. Reconstruct disk state possible on a powerloss 

Using BOB, they prove that crash consistency differs from the file system and its configurations. 

while ALICE works as following
When ALICE gets user supplied application workloads, it traces system calls as its abstract persistent model
(default for many possible, but user can specify a file system)  
Then expoler runs, targeting specific states related atomicity and reordering. For each states, user runs application 
checker and check the violation showing that what kinds of ordering and atomicity does application needs and which 
syscall  violates.

In short, a file system itself can affect crash consistency of applications, while application are usually vulnerable
with crashs 

