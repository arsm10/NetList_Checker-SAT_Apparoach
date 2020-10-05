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
# Input Format (NetList - .net files)
- Line 1: Number of nets.
- Line 2: Names of all input nets.
- Line 3: Names of all output nets.
- Line 4-6: Mapping from net numbers to port names (for all inputs and outputs).
- Line 7: Empty line.
- Line 8 to end of file: Gate instantiations in the form: Depending on the gate type, there number of parameters may vary e.g. "AND Gate" has three parameters, while "NOT Gate" has only two parameters.
