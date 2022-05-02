# sky130RTLDesignandSynthesisWorkshop
![Workshop Banner](/docs/workshop_banner.png)

# About

A cloud based 5 day training workshop which offeres insights into verilog coding techniques for successful elaboration and synthesis using sky130 PDK.

Workshop conducted by VLSI System Design : [VSD website](https://www.vlsisystemdesign.com/)

# Outline

1. [Introduction](#1-Introduction)
2. [Verilog RTL Design and Synthesis](#2-verilog-rtl-and-synthesis)
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

## 2.i Lab 1 - Cloning git files and viewing directory contents

# 3. Decoding Library Files

# 4. Hierarchial vs Flat Synthesis

# 5. Flop Coding Style

# 6. Combinational Optimisations

# 7. Sequential Optimisations

# 8. Gate Level Simulation (GLS)

# 9. Synthesis - Simulation Mismatch

## 9.i. Blocking vs Non- Blocking Statements

# 10. Synthesis Optimisation Techniques
