# 4-bit ALU Design using Cadence Virtuoso

This project presents the design and verification of a **4-bit Arithmetic and Logic Unit (ALU)** using **Cadence Virtuoso**. The ALU supports 8 fundamental operations and is implemented at the transistor level using **CMOS logic**.

---

## 🧠 Project Overview

The ALU is designed to perform **arithmetic and logic operations** on two 4-bit input operands. Each operation is selected using a 3-bit select line through an 8:1 multiplexer-based control structure.

---

## ⚙️ Supported Operations

| Select Lines (S2 S1 S0) | Operation      | Description                      |
|--------------------------|----------------|----------------------------------|
| 000                      | AND            | A & B (4-input AND gate)         |
| 001                      | OR             | A | B (4-input OR gate)         |
| 010                      | XOR            | A ^ B (4-input XOR gate)         |
| 011                      | XNOR           | ~(A ^ B) (4-input XNOR gate)     |
| 100                      | ADD            | A + B (using 4-bit RCA)          |
| 101                      | 2's Complement | 2's complement of input A        |
| 110                      | CLEAR          | All outputs set to 0             |
| 111                      | INVERT         | Bitwise NOT of input A           |

---

## 🧱 Design Flow

1. **CMOS-Level Circuit Design**:
   - Designed each logic block (AND, OR, XOR, etc.) using CMOS gates.
   - Arithmetic operations (ADD, 2's complement) built using:
     - Mirror Adder (for full adder logic)
     - 4-bit Ripple Carry Adder (RCA)

2. **Schematic Creation**:
   - Created individual schematic files for each operation.
   - Combined symbols using hierarchical design in Virtuoso.

3. **Symbol Creation**:
   - Generated symbols for each block for modular connection.

4. **Testbench Design**:
   - Designed a testbench schematic with input pins, VDD, and select lines.
   - Used `vpulse` and `vdc` sources to simulate input patterns.

5. **Simulation & Verification**:
   - Verified waveform outputs using **Cadence Virtuoso Spectre simulator**.
   - Checked functional correctness for each operation via transient analysis.

---

## 🛠 Tools Used

- **Cadence Virtuoso** (Schematic + Symbol + Simulation)
- **gpdk 90nm CMOS Technology**
- **Spectre Simulator**

---

## 📌 Learning Outcomes

- CMOS circuit design & simulation in Cadence
- Hierarchical design methodology
- Symbol abstraction and reusability
- ALU architecture and logic integration
- Multiplexer-based operation control

---

## 🧩 Future Improvements

- Layout and DRC/LVS verification
- Area and power optimization
- 8-bit ALU extension
- Pipelined ALU design for performance

---

## 👤 Author

**Suraj Singh Bisht**  
B.Tech | Electronics and Communication Engineering (ECE)  
Designed and verified this project using Cadence Virtuoso as part of hands-on learning in digital IC design.

---

