# Day 1: Introduction to Verilog RTL Design and Synthesis

Welcome to Day 1 of the RTL Workshop!  
Today, you'll start building your digital design skills by writing Verilog code, simulating it with Icarus Verilog, and synthesizing designs using Yosys.  
This guide is hands-on, with clear steps and labs to help you get started.

---

## Table of Contents
- [Introduction to open source simulatior iverilog,Design and Test Bench](#introduction-to-open-source-simulator-iverilog)
- [Labs using Icarus Verilog and GTKWave](#labs-using-icarus-verilog-and-gtkwave)
- [Introduction to Yosys and Logic Synthesis](#introduction-to-yosys-and-logic-synthesis)
- [Labs using Yosys and Sky130 PDK](#labs-using-yosys-and-sky130-pdk)
- [Summary](#summary)

---

# Understanding Simulator, Design, and Testbench in Verilog

Understanding the roles of **Simulator**, **Design**, and **Testbench** is essential for anyone working with **Verilog RTL design**.  
These three components form the backbone of **digital design verification** before moving to synthesis or actual chip fabrication. 🚀

---

## 📌 1. Simulator
- A **simulator** is a tool that **mimics the behavior of your digital circuit** before it’s built in hardware.  
- It helps you verify whether your Verilog design works as expected and debug issues in a safe, virtual environment.
- **`iverilog`** is the open source simulator we are using in our workshop

## ⚙️ 2. Design (DUT – Design Under Test)
- The **Design**, also called the **UUT (Unit Under Test)** or **DUT (Design Under Test)**, represents the **actual hardware logic**.
- Actual **verilog** code which describes how data flows and how operations are performed at the **Register Transfer Level (RTL)**.

## 🧪 3. Testbench
- Testbench is an environmental setup to apply stimulus(test_vectors) to design and check functionality.
- It supplies **inputs (stimulus)** to the DUT and monitors the **outputs (responses)**.

---

## 🔄 4. How simulator works
- Simulator looks for the changes on the input signals.
- If there is no change to the input ➡️ no change to the output.
- Generates **waveform files (`.vcd`)** to visualize signals in tools like **GTKWave**.



## Labs using Icarus Verilog and GTKWave

-[githyb link for sky130](https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git)
**Icarus Verilog (iverilog)** lets you compile and simulate Verilog designs.


