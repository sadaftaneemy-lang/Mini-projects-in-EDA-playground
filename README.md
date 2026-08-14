# 📌 Project Overview

This project demonstrates the correct use of assignments in a sequential circuit using Verilog HDL.
The design is simulated using EDA Playground and follows the recommended coding style for sequential logic

## 🔄 Design Flow
Verilog RTL
     ↓
     
   Yosys
     ↓
     
RTL Synthesis
     ↓
D Flip-Flop Recognition
     ↓ 
    $dff
     ↓
     
Schematic Generation

## 💻 Tool Used

- EDA Playground
- Verilog HDL
- Yosys Simulator

# Bad_blocking

## Program
<img width="1280" height="751" alt="image" src="https://github.com/user-attachments/assets/d75ced0f-cfd8-4d67-86d7-f86d5f7bbfe0" />

The important line is:

q <= d;

Here <= is called the non-blocking assignment operator.
## Output
<img width="492" height="317" alt="image" src="https://github.com/user-attachments/assets/fdf4aca2-2117-4d59-aa65-30eee4ab2aee" />

From the code "always @(posedge clk)" means whenever the clock changes from 0 → 1 (positive edge), do the work inside.

Here

clk  → Clock input

d    → Data input

q    → Stored output

When the clock edge comes

q = d

**Why is the block called bad_blocking ?**

Because inside a sequential (always @(posedge clk)) block I used "=", This is called a blocking assignment.

For sequential circuits, we should use " <= " , This is a non-blocking assignment.

# Good_blocking
## Program
<img width="1280" height="756" alt="image" src="https://github.com/user-attachments/assets/04198f8f-1b94-46a8-a938-0e5e0add81cb" />

## Output
<img width="465" height="311" alt="image" src="https://github.com/user-attachments/assets/52c31fd4-2a56-489b-a184-163ab56818b1" />

