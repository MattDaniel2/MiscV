
# MISC V
Miscellaneous RISC-V core based on RISC, implementing the RV32I ISA for FPGA Targets
## Alpha (needs a better name)
Start with "Bare Metal" physical processor threads and full physical address space. Only the standard encoding space will be used in Alpha. 
### High Level Goals
Explore the RISC-V ISA and implement a software-programmable core on small FPGA to demonstrate the concepts. Software should be capable of running basic programs as expected of any 32 bit embedded processor as well as device I/O specific to the FPGA.
RTL implementation should be succinct wherever possible, with extensive use of SystemVerilog features to improve portability and modularity such as Interfaces, Modports, and other synthesizable constructs. 

### Timeline
 * Basic Architectural Definition 
<<<<<<< HEAD
   * 8/31/2020
 * Basic Microarchitectural Definition 
   * 9/14/2020
=======
   * Not Relevant -- Spec Given
 * Basic Microarchitectural Definition 
>>>>>>> 8c742d4858c7f13cadfe85a3578c13f4c1d4268e
   * Functional block shells complete and stitched
   * C Model Work?
   * Basic Verification Infrastructure around shells
 * Implementation Milestone 1
<<<<<<< HEAD
   * 9/21/2020
=======
>>>>>>> 8c742d4858c7f13cadfe85a3578c13f4c1d4268e
   * TBD Subset of instructions complete
   * Basic core to memory accesses simulated
   * 50% of instruction and code-primitive unit tests written
   * Compiler toolchain for implementation investigated and documented
 * Implementation Milestone 2
<<<<<<< HEAD
   * 10/5/2020
=======
>>>>>>> 8c742d4858c7f13cadfe85a3578c13f4c1d4268e
   * All RV32I instructions implemented
   * 100% of instruction and code-primitive unit tests written
   * Architectural-level performance optimizations investigated
   * Program-level simulations run
 * Implementation Finished
<<<<<<< HEAD
   * 10/19/2020
=======
>>>>>>> 8c742d4858c7f13cadfe85a3578c13f4c1d4268e
   * 100% of tests written and passing
   * 4 major performance optimizations performed
   * Final C code programs simulated in full on implementation
 * Core Finished
<<<<<<< HEAD
   * 10/26/2020
=======
>>>>>>> 8c742d4858c7f13cadfe85a3578c13f4c1d4268e
   * MISC-V demonstrated on Xilinx Arty-7-35T FPGA board with working code
   
 

### Reading Notes
 * Since lower 2 bits always 2'b11, can make I$ entries 30b wide and append after fetch
 * General behavior of most RISC-V EEIs is that a trap to some handler occurs when an exception is signaled on an instructions. The manner of interrupt generation and handling depends on implementation
 * Registers -- standard software calling conventions
   * x1 to hold return address of a call
   * x5 as an alternate link register
   * x2 as the stack pointer
   * Can choose to accelerate function calls and returns that use x1 or x5 (See JAL and JALR instruction descriptions)
