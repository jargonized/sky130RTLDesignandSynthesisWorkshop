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

In this workshop, **Verilog** was used as the target HDL language. **iverilog** was used to generate Value Dump Files (VCD) and **gtkwave** was used to view the simulation outputs. OpenLANE's synthesis tool **yosys** was used to synthesise the RTL models.

# 2. Verilog RTL and Synthesis

# 3. Decoding Library Files

# 4. Hierarchial vs Flat Synthesis

# 5. Flop Coding Style

# 6. Combinational Optimisations

# 7. Sequential Optimisations

# 8. Gate Level Simulation (GLS)

# 9. Synthesis - Simulation Mismatch

## 9.i. Blocking vs Non- Blocking Statements

# 10. Synthesis Optimisation Techniques
