# 🚀 32-Bit 5-Stage Pipelined RISC-V Processor

This repository contains a **32-bit 5-Stage Pipelined RISC-V Processor** designed in **Verilog HDL** following the **RV32I Instruction Set Architecture (ISA)**. The processor improves instruction throughput by executing multiple instructions simultaneously using a **5-stage pipeline** consisting of Instruction Fetch (IF), Instruction Decode (ID), Execute (EX), Memory Access (MEM), and Write Back (WB). The design is developed and verified using **Visual Studio Code**, **Icarus Verilog (iverilog)**, and **GTKWave**.

---

# 🏗️ Architecture Overview

The processor is divided into modular hardware blocks connected through **pipeline registers**, enabling concurrent execution of multiple instructions while maintaining correct program execution.

## 🧩 Pipeline Stages

### 📥 Instruction Fetch (IF)
- Fetches instructions from Instruction Memory.
- Updates the Program Counter (PC).

### 🧠 Instruction Decode (ID)
- Decodes instructions.
- Reads operands from the Register File.
- Generates control signals.

### ➕ Execute (EX)
- Performs arithmetic and logical operations.
- Calculates branch and memory addresses.

### 💾 Memory Access (MEM)
- Executes Load and Store operations using Data Memory.

### 📤 Write Back (WB)
- Writes computation or memory results back into the Register File.

---

# 🧩 Core Modules

### 🖥️ Top Module (`Pipeline_Top.v`)
Integrates the datapath, control unit, memories, pipeline registers, forwarding logic, and hazard detection.

### 📌 Program Counter (`PC.v`)
Maintains and updates the address of the current instruction.

### 📥 Instruction Memory (`Instruction_Memory.v`)
Stores machine instructions executed by the processor.

### 📚 Register File (`Register_File.v`)
Implements 32 general-purpose 32-bit registers with two read ports and one write port.

### 🧠 Control Unit (`Control_Unit_Top.v`)
Generates processor control signals based on the decoded instruction.

### ➕ Arithmetic Logic Unit (`ALU.v`)
Performs operations including:
- Addition
- Subtraction
- AND
- OR
- XOR
- SLT
- Shift Operations

### 💾 Data Memory (`Data_Memory.v`)
Supports Load and Store instructions.

### 🔄 Pipeline Registers
Stores intermediate data and control signals between:
- IF/ID
- ID/EX
- EX/MEM
- MEM/WB

---

# 📁 File Structure

| 📄 File | 📝 Description |
|---------|----------------|
| `Pipeline_Top.v` | 🏗️ Top-level processor module |
| `PC.v` | 📌 Program Counter |
| `Instruction_Memory.v` | 📥 Instruction Memory |
| `Register_File.v` | 📚 Register File |
| `Control_Unit_Top.v` | 🧠 Control Unit |
| `ALU.v` | ➕ Arithmetic Logic Unit |
| `Data_Memory.v` | 💾 Data Memory |
| `pipeline_tb.v` | 🧪 Processor Testbench |

---

# 🛠️ Development Tools

- 💻 Visual Studio Code
- ⚙️ Icarus Verilog (iverilog)
- 📈 GTKWave

---

# 🧪 Simulation Steps

## 🔨 Compile

```bash
iverilog -o out.vvp pipeline_tb.v Pipeline_Top.v
```

## ▶️ Run Simulation

```bash
vvp out.vvp
```

## 📈 View Waveforms

```bash
gtkwave
```

---

# 🎯 Applications

- 🎓 Computer Architecture
- 📚 RISC-V Pipeline implementation
- 🚀 RTL Design and Verification
- 🖥️ ASIC/ Processor Design
- 🔬 Digital Design

---

# 📸 Simulation

The processor can be simulated using **Icarus Verilog** and analyzed with **GTKWave**, allowing verification of:

- 📌 Program Counter (PC)
- 📥 Instruction Flow
- 📚 Register File
- ➕ ALU Operations
- 🔄 Pipeline Registers
- 💾 Data Memory
- 📊 Control Signals

---

# ⭐ Tools Used

- **Language:** Verilog HDL
- **Editor:** Visual Studio Code
- **Simulator:** Icarus Verilog
- **Waveform Viewer:** GTKWave

---
