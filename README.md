# sky130RTLDesignandSynthesisWorkshop
![Workshop Banner](/docs/workshop_banner.png)

# About

A cloud based 5 day training workshop which offeres insights into verilog coding techniques for successful elaboration and synthesis using sky130 PDK.

Workshop conducted by VLSI System Design : [VSD website](https://www.vlsisystemdesign.com/)

# Outline

1. [Introduction](#1-Introduction)
2. [Verilog RTL Design and Synthesis](#2-verilog-rtl-and-synthesis) 
    1. [Lab - To create a directory and clone .git files]
    2. [Commands to simulate a RTL design]
    3. [Lab - Simulation]
    4. [Commands to run Synthesis]
    5. [Lab - Synthesis]
3. [Decoding Library File(s)](#3-decoding-library-file(s))
4. [Hierarchial vs Flat Synthesis](#4-hierarchial-vs-flat-synthesis)
5. [Flop Coding Style](#5-flop-coding-style)
6. [Combinational Optimisations](#6-combinational-optimisations)
7. [Sequential Optimisations](#7-sequential-optimisations)
8. [Gate Level Simulation (GLS)](#8-gate-level-simulation-(GLS))
9. [Synthesis - Simulation Mismatch](#9-synthesis-simulation-mismatch)
    1. [Blocking vs Non- Blocking Statements](#9-1-Blocking-vs-Non-Blocking-statements)
10. [Synthesis Optimisation Techniques](#10-synthesis-optimisation-techniques)

# 1. Introduction

Register Transfer Level (RTL) is an abstraction technique for defining the digital portions of a design. It serves as the golden model in the design and verification flow. The RTL design is usually captured using a hardware description language (HDL) such as Verilog or VHDL. When the language is fed into a synthesis tool, abstraction of the design that is used for all downstream implementation operations.

In this workshop, **Verilog** was used as the target HDL language. **iverilog** was used to generate Value Change Dump Files (VCD) and **gtkwave** was used to view the simulation outputs. OpenLANE's synthesis tool **yosys** was used to synthesise the RTL models.

# 2. Verilog RTL and Synthesis

The functional behaviour of any circuit design is verified by simulating the device under test(DUT). Famous simulation tools include LTSpice and NgSpice for analog circuits. ModelSim simulator is widely used to simulate digital circuits. To verify the behaviour of a circuit, test cases pertaining to various use cases should be fed and the corresponding output should be observed and analysed. Simulations often reveal the functionality and the potential pitfalls associated with the design. 

To simulate digital circuits, a test signal can be **forced** on the simulator or a **testbench** can be written to automate the simulation process. *Testbench* applies stimulus(often known as test vectors) to the design. A simulator evaluates output when a change in the input is detected. Any simulator on applying stimulus to the DUT generates a **.vcd** file as output which can be opened using a VCD waveform viewer (gtkwave in this workshop).

| ![files](docs/Day02/2022-05-01%20(8).png) | 
|:--:| 
| Files used throughout the course|

## 2.i Lab 1 - Cloning git files and viewing directory contents

| ![Creating directory](docs/Day01/2022-04-27%20(2).png) | 
|:--:| 
| Creating a directory and checking if iverilog and yosys are functional |

| ![Cloning required files](docs/Day01/2022-04-27%20(3).png) |
|:--:| 
| To clone required .lib and verilog files [Link to Files](https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop)|

| ![Cloning required files](docs/Day01/2022-04-27%20(4).png) | 
|:--:| 
| To view the files|

## 2.iii Lab 2 - To simulate a counter

| ![Simulation commands](docs/Day01/2022-04-27%20(7).png) | 
|:--:| 
| Commands for simulating a RTL Model |

| ![Simualtion output](docs/Day01/2022-04-27%20(5).png) | 
|:--:| 
| GTKWave Window |

## 2.v Lab 3 - To synthesize a RTL design

| ![Launch yosys](docs/Day01/2022-04-27%20(8).png) | 
|:--:| 
| Launch yosys |

| ![read commands](docs/Day01/2022-04-27%20(9).png) | 
|:--:| 
| Read the library file, design files and sythesize the top module |

| ![Stats](docs/Day01/2022-04-27%20(12).png) | 
|:--:| 
| Synthesis Statistics - Displayed on successful synthesis ; Generate netlist |

| ![Net res](docs/Day01/2022-04-27%20(13).png) | 
|:--:| 
| Netlist Result ; Show command to display synthesised design |

| ![show op](docs/Day01/2022-04-27%20(14).png) | 
|:--:| 
| Synthesised Design|

| ![Write netlist](docs/Day01/2022-04-27%20(19).png) | 
|:--:| 
| To write netlist with attributes |

| ![attr op](docs/Day01/2022-04-27%20(16).png) | 
|:--:| 
| Generated Netlist |

| ![no attr net](docs/Day01/2022-04-27%20(21).png) | 
|:--:| 
| To write netlist without attributes |

| ![no attr op](docs/Day01/2022-04-27%20(20).png) | 
|:--:| 
| Generated Netlist |


# 3. Decoding Library Files

## 3.1 Lab 4 - Analysing .lib file

| ![Initial lines of .lib file](docs/Day02/1.png) | 
|:--:| 
| Highlighted text shows i) File name - process,voltage and operating temperature given ii) Units for various parameters and other required information|

| ![Pin_det](docs/Day02/2022-05-01%20(2).png) |
|:--:| 
| Pin Specific Details |

| ![tim](docs/Day02/2022-05-01%20(3).png) | 
|:--:| 
| Timing related details|

| ![flavours](docs/Day02/2022-05-01%20(5).png) | 
|:--:| 
| Same logic unit available in different flavours|

| ![flavours](docs/Day02/2022-05-01%20(6).png) | 
|:--:| 
| Comparison of area between mux2_2, mux2_4 and mux2_8 respectively - More Area, less delay but increased power consumption|



# 4. Hierarchial vs Flat Synthesis

## 4.1. Lab 5 - Hierarchial Synthesis and flattened design

| ![mul_mod_synth](docs/Day02/2022-05-01%20(10).png) | 
|:--:| 
| Synthesis result of a multi-module RTL design|

| ![mul_mod_synth1](docs/Day02/2022-05-01%20(12).png) | 
|:--:| 
| Generated netlist|

| ![mul_mod_synth2](docs/Day02/2022-05-01%20(19).png) | 
|:--:| 
| Hierarchial design output |

| ![mul_mod_synth3](docs/Day02/2022-05-01%20(20).png) | 
|:--:| 
| Flattened Design|

| ![mul_mod_synth4](docs/Day02/2022-05-01%20(25).png) | 
|:--:| 
| Synthesis of a sub module|

# 5. Flop Coding Style

| ![mul_mod_synth](docs/Day02/2022-05-01%20(10).png) | 
|:--:| 
| Synthesis result of a multi-module RTL design|

| ![mul_mod_synth1](docs/Day02/2022-05-01%20(12).png) | 
|:--:| 
| Generated netlist|

| ![mul_mod_synth2](docs/Day02/2022-05-01%20(19).png) | 
|:--:| 
| Hierarchial design output |

| ![mul_mod_synth3](docs/Day02/2022-05-01%20(20).png) | 
|:--:| 
| Flattened Design|

| ![mul_mod_synth4](docs/Day02/2022-05-01%20(25).png) | 
|:--:| 
| Synthesis of a sub module|


# 6. Combinational Optimisations

# 7. Sequential Optimisations

# 8. Gate Level Simulation (GLS)

# 9. Synthesis - Simulation Mismatch

## 9.i. Blocking vs Non- Blocking Statements

# 10. Synthesis Optimisation Techniques
