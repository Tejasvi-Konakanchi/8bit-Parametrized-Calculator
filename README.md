# 8-bit Calculator ASIC (RTL → GDSII Flow)

**Skills Used:** Verilog/SystemVerilog, Digital Logic Design, RTL Design, Functional Verification, Simulation & Debugging, Timing Analysis Basics, FPGA Prototyping, ASIC Physical Design Flow

<br>

## 1. Introduction

This project documents the design and implementation of an 8-bit digital calculator, developed using a full RTL-to-GDSII ASIC design flow in Verilog/SystemVerilog.

The goal of this project is to implement a complete digital system that performs arithmetic operations and to take it through all stages of an ASIC design pipeline, from RTL description to final GDSII layout generation.


### 1.1 Design Flow Overview

The project follows a standard ASIC RTL-to-GDSII flow used in modern semiconductor design:

- RTL Design (Verilog/SystemVerilog)
- Functional Verification (Testbench Simulation)
- Logic Synthesis
- Static Timing Analysis (STA)
- Floorplanning
- Placement
- Clock Tree Synthesis (CTS)
- Routing
- Physical Verification (DRC/LVS)
- GDSII Generation



## 2. Design Specification

### 2.1 Functional Description

The calculator operates on two 8-bit unsigned operands:

- Operand A (8-bit)
- Operand B (8-bit)

Arithmetic operations are selected using a 2-bit control signal:

| OP[1] | OP[0] | Operation      |
|-------|-------|----------------|
| 0     | 0     | Addition       |
| 0     | 1     | Subtraction    |
| 1     | 0     | Multiplication |
| 1     | 1     | Division       |



### 2.2 Hardware Interface (RTL-Level Specification)

This is a standalone ASIC module with the following input/output interface:

| Signal  | Direction | Width  | Description         |
|---------|----------|--------|---------------------|
| A       | input    | 8-bit  | Operand A           |
| B       | input    | 8-bit  | Operand B           |
| OP      | input    | 2-bit  | Operation select    |
| CLK     | input    | 1-bit  | System clock        |
| RST     | input    | 1-bit  | Active-high reset   |
| RESULT  | output   | 16-bit | Computation result  |



## 3. RTL Architecture

The design consists of the following main blocks:

- 8-bit ALU (Arithmetic Logic Unit)
- Operand registers (A and B)
- Control logic (operation decode)
- Optional FSM controller (for sequential operation)
- Output register stage



## 4. FPGA Prototype (Test Platform)

For functional validation, the design can be mapped to an FPGA development board.

### 4.1 FPGA Input Mapping

| Signal | Bits     | Purpose            |
|--------|----------|--------------------|
| SW     | [7:0]    | Operand A          |
| SW     | [15:8]   | Operand B          |
| SW     | [17:16]  | Operation select   |
| KEY    | [0]      | Compute / Execute  |

> Note: FPGA mappings are used only for prototyping and verification. They are not part of the ASIC specification.

---

## 5. Project Author

**Tejasvi Konakanchi**  
Email: tejasvi.konakanchi@gmail.com  

Last Updated: **04/22/2026**
