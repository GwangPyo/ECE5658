Lottery Scheduling 
===================

Lottery scheduling is scheduling policy which tries to approximate both priority scheduling and proportional schedulings. 
Lottery scheduling is basically proportional share scheduling, it shares time quanta of the resource which is the target of scheduling policy. 
However, it approximates priority scheduling, using concepts of the lottery. If a process has a bunch of lottery, the number of the 
lottery guarantees the more probability to access the resource. 
With assumption that a frequency of which a thread requires the resource is sufficiently small, the lower priority thread will eventually
obtain the resource, because it has at least one lottery. Moreover, the less execution means the number of lottery the portion of lottery
will be grown up. 
