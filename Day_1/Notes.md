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

## Introduction to open source simulatior iverilog

- Verilog is a hardware description language (HDL) used for designing digital circuits.
- RTL (Register Transfer Level) describes how data moves between registers and how combinational logic operates on that data.
- Key abstraction levels:
  - Behavioral → what the circuit does
  - RTL → how data flows between registers
  - Gate-level → actual logic gates

> RTL is the blueprint before the physical implementation of a chip.

---

## Labs using Icarus Verilog and GTKWave

-[githyb link for sky130](https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git)
**Icarus Verilog (iverilog)** lets you compile and simulate Verilog designs.

### Commands
```bash
# Compile design and testbench
iverilog -o simulation.vvp design.v testbench.v

# Run the simulation
vvp simulation.vvp

# Open waveform
gtkwave dump.vcd
