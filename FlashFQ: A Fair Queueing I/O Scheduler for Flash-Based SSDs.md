For the current fair scheduling, the most popular method is time slice based fair scheduling. 
However, for the IO, especially flash storage, time-slice based scheduling may not appropriate.
The io operation responsiveness varies and inevitable with time-slice based scheduling.

The authors suggest fair queueing scheduler

using tags, it manages virtual time based fair scheduling, and manages under-utilized tasks 
Using start time fair queueing, it achieves parrallsim on flash



