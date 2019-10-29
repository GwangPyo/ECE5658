For the scalable desing of API, the authors define the the Scalable Commutativity Rule, and the tool named COMMUTER.

The observation for the author about the Scalable Commutativity Rule is that
if there are operations which cannot distinguish their execution order, they can be scalable. 

The author studied SIM commutativity: State dependent, Interface-based, Monotonic

From the study about COMMUTE, the author suggests guidelines how to design commutative interfaces.

1. Decompose compound operations


2. Embrace specification non-determinism 

3. Permit weak ordering

4. Release resources asynchronously 

and also patterns for designing scalable implementations

1. Layer scalability

2. Defer work

3. Precede pessimism with optimism

4. Don’t read unless necessary
