# NetList Checker-SAT Apparoach
This implementation performs the formal equivalence checking given two netlists using a SAT-based approach. The method reads the two netlist files in a specific format. If the netlists are functionally equivalent, the program displays “OK”. If not, it prints an input assignment which leads to different output values (counter example).</br></br>
To achieve this, the following steps are necessary:
- Create an appropriate miter circuit,
- Convert the miter circuit to a formula in CNF, and
- Check the CNF for satisfiability
# Gate Type
There are six gate types which are allowed in a netlist:
| Gate Type | Input Ports | Output Ports |
| :--- | :--- | :--- |
| AND | 2 | 1 |
| OR | 2 | 1 |
| INV | 1 | 1 |
| XOR | 2 | 1 |
| One | 0 | 1 |
| Zero | 0 | 1 |
