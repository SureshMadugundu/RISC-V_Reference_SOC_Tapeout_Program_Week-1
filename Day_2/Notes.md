# Day 2: Timing Libraries, Hierarchical vs Flat Synthesis & Efficient Flop Coding Styles

Welcome to **Day 2** of the **RISC-V Reference SoC Tapeout Program**!  
Today's focus is on understanding **timing libraries**, exploring **synthesis strategies**, and learning **efficient flip-flop coding styles** to design optimized digital circuits.

---

## 📚 Topics for Today
- [Introduction to Timing Libraries (`.lib` files)](#-introduction-to-timing-libraries)
- [Hierarchical vs Flat Synthesis](#-hierarchical-vs-flat-synthesis)
- [Efficient Flip-Flop Coding Styles & Optimizations](#-efficient-flip-flop-coding-styles--optimizations)

---

## ⏱ Introduction to Timing Libraries
Timing libraries (`.lib` files) are **essential files** used by synthesis tools to:
- Provide **timing, power, and area** information for each standard cell.
- Ensure **accurate synthesis and timing analysis**.
- Define how gates and flip-flops behave under **different PVT (Process, Voltage, Temperature)** conditions.

---
### 🌡 Understanding PVT (Process, Voltage, Temperature)

**PVT** represents the three **critical variables** that affect chip behavior and timing:
- **Process (P):** Variation in manufacturing leads to **fast (`ff`)**, **slow (`ss`)**, or **typical (`tt`)** transistor performance.
- **Voltage (V):** The operating voltage of the circuit.  
  - Higher voltage → **faster switching**, but **higher power consumption**.  
  - Lower voltage → **slower performance**, but **reduced power consumption**.
- **Temperature (T):** Impacts transistor speed.  
  - Higher temperature → **slower operation** due to increased resistance.
 
  #### Decoding tt_025C_1v80 in the SKY130 PDK

  | Factor      | Description | Example |
  |-------------|-------------|---------|
  | **Process (P)** | Fabrication variations in transistors. | `tt` = Typical |
  | **Voltage (V)** | Power supply voltage level. | `1v80` = 1.8V |
  | **Temperature (T)** | Operating temperature in °C. | `025C` = 25°C |

> **Why PVT is Important:**  
> - Ensures the circuit functions correctly in **all possible conditions**.  
> - Helps identify **worst-case** and **best-case timing scenarios** for reliable chip performance.

---

### Example Naming Convention:
