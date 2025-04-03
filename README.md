# Pipelined MIPS-32 Processor in Verilog

## 🚀 Overview
This project implements a **5-stage pipelined MIPS-32 processor** in Verilog, simulating instruction execution with a testbench. The design optimizes instruction execution by leveraging **instruction-level parallelism**.

## 📌 Pipeline Stages
1️⃣ **Instruction Fetch (IF)** – Fetches the instruction from memory.  
2️⃣ **Instruction Decode (ID)** – Decodes the opcode and reads registers.  
3️⃣ **Execute (EX)** – Performs ALU operations.  
4️⃣ **Memory Access (MEM)** – Reads/writes data memory.  
5️⃣ **Write Back (WB)** – Stores results into registers.  

## 🛠️ Features
✅ Supports ALU operations (ADD, SUB, MUL, AND, OR, SLT)  
✅ Handles memory operations (LW, SW)  
✅ Implements branch instructions (BEQZ, BNEQZ)  
✅ Uses **two-phase clocking** for optimized execution  
✅ Simulated using a testbench for verification  

## 🏗️ File Structure
```
📂 mips_pipeline
 ├── 📜 mips_pipeline.v      # Verilog code for the 5-stage MIPS processor
 ├── 📜 testbench.v          # Testbench to verify execution
 ├── 📜 README.md            # Project documentation
```

## 🔬 Simulation & Verification
The project is tested using a **Verilog testbench**, initializing registers, loading instructions, and verifying the results using `$display` statements.

#### ✅ Example Instruction Execution:
```verilog
mips.Mem[0]=32'h2801000a; // ADDI R1, R0, 10
mips.Mem[1]=32'h28020014; // ADDI R2, R0, 20
mips.Mem[2]=32'h28030019; // ADDI R3, R0, 25
mips.Mem[5]=32'h00222000; // ADD R4, R1, R2
mips.Mem[7]=32'h00832800; // ADD R5, R4, R3
mips.Mem[8]=32'hfc000000; // HALT

```
## 📢 Contribute
Feel free to fork this repository, report issues, or suggest improvements! 
📌 **Connect with me on LinkedIn:** www.linkedin.com/in/lakshmi-vana-b6378a2ba
