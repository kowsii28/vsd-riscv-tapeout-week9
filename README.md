# vsd-riscv-tapeout-week9
Summary of the VSDBabySoC Design
# VSDBabySoC – Complete Documentation (VSD Internship Week-9 Submission)

**Author:** Kowsalya M  
**Internship:** VLSI SoC Design – VSD x IIT Gandhinagar  
**PDK:** SKY130A – Open PDK  
**Tools Used:** OpenLane, OpenROAD, Yosys, Magic, NGSPICE, GTKWave  


---


## 1. Introduction

This repository contains the complete documentation of my **VSDBabySoC** implementation done during the VSD Internship.  
The design was built using the **RTL-to-GDSII OpenLane Flow** over Sky130A PDK.  
All stages — simulation, synthesis, placement, routing, parasitic extraction, and STA — are included.

This repo consolidates:

- Week-wise documentation  
- Screenshots with terminal username  
- Timing reports  
- SPEF-based STA  
- Learning notes and unique workflow  


## 2. Toolchain and Environment

| Tool | Purpose |
|------|---------|
| **OpenLane** | End-to-end physical design flow |
| **Yosys** | Logic synthesis |
| **OpenROAD** | Placement, CTS, Routing, STA |
| **Magic** | Layout visualization & DRC |
| **GTKWave** | Waveform analysis |
| **PDK: SKY130A** | Technology files used for design |


## 3. Week-Wise Learning and Work


## Week 2 – RTL, Functional Simulation, Pre & Post Synthesis

### ✔ RTL Analysis
- Understood VSDBabySoC architecture and module hierarchy.

### ✔ Pre-Synthesis Functional Simulation
- Used Icarus Verilog for simulation.
- Observed waveforms in GTKWave.
- Ensured RTL matches expected behavior.

### ✔ Post-Synthesis Verification
- Synthesized using **Yosys**.
- Generated gate-level netlist using Sky130 standard cells.
- Performed GLS (Gate Level Simulation).
- Confirmed RTL vs GLS consistency.


## Week 3 – Static Timing Analysis on Synthesized Netlist

### What I Learned:
- Setup time / Hold time  
- Slack calculation  
- Critical path  
- WNS (Worst Negative Slack)  
- TNS (Total Negative Slack)


### Outcomes:
- Identified timing paths
- Analyzed violations (if any)
- Understood synthesis timing behavior

👉 *Screenshots in `docs/week3/`.*


## Weeks 4 – 6: Physical Design Fundamentals

Focused on understanding concepts before running the full flow.

### ✔ Floorplanning Basics:
- Die/Core area  
- Utilization factor  
- Aspect ratio  
- Pin placement  
- Power planning  

### ✔ Placement Concepts:
- Global & detailed placement  
- Congestion analysis  

### ✔ Clock Tree Synthesis:
- Clock buffers  
- Skew  
- Latency  

### ✔ Routing:
- Global routing  
- Detailed routing  
- DRC concepts  

👉 *These fundamentals prepared me for Week 7 physical design.*


## Week 7 – Complete Physical Design of VSDBabySoC

Performed the **full OpenLane flow** from synthesis to routing.

### ✔ 1. Synthesis
- Yosys mapped RTL → standard cells  
- Collected cell usage and area reports  

### ✔ 2. Floorplanning
- Generated core & die  
- Power straps/rings  
- Pin placement  

### ✔ 3. Placement
- Global placement  
- Detailed placement  
- Verified density & congestion  

### ✔ 4. Clock Tree Synthesis (CTS)
- Clock buffers inserted  
- Clock skew + latency verified  

### ✔ 5. Routing
- Global routing  
- Detailed routing  
- DRC checked  
- Final GDS generated  



## Week 8 – Post-Route STA Using SPEF

Performed full STA after routing using extracted parasitics.

### Steps Performed:
1. Load routed DEF  
2. Read SPEF:


# 4. Understanding the VSDBabySoC

The **VSDBabySoC** is a minimal, open-source System-on-Chip designed for learning the fundamentals of digital design, SoC integration, and the complete RTL-to-GDSII VLSI flow.  
It is small enough to run efficiently through open-source tools but contains all essential blocks found inside a real SoC.

---

## 4.1 VSDBabySoC Architecture

## 4.2 Real Block Diagram

![VSDBabySoC Block Diagram](vsdbabysoc_block_diagram.png)

The SoC consists of:

- **Controller (FSM)** – Manages the overall operation  
- **Counter/Timer Block** – Performs counting operations  
- **ALU (Arithmetic Logic Unit)** – Handles arithmetic operations like add/sub  
- **GPIO/Output Block** – Sends output to pins  
- **Clock & Reset Logic** – Synchronization mechanism  
- **Internal Interconnect** – Wires connecting modules  


# 4.2 What I Learned from VSDBabySoC

Working on VSDBabySoC gave me a deep understanding of both **digital design** and the **full SoC design flow**.

### ### 📌 **RTL-Level Learning**
- How different modules are connected in a SoC  
- How ALU, counters, and controllers operate together  
- How to simulate and verify RTL design  
- Writing and verifying testbenches  

### 📌 **Synthesis-Level Learning**
- How RTL converts into standard cells  
- Cell mapping and technology libraries  
- Gate-level simulation and equivalence  

### 📌 **STA Learning**
- Critical path identification  
- Setup and hold timing  
- WNS / TNS understanding  
- SPEF-based timing variation  

### 📌 **Physical Design Learning**
- Floorplanning: area, pin placement, PDN  
- Placement: congestion, density  
- CTS: skew & buffering  
- Routing: DRC, wirelength  
- GDS generation  

### 📌 **Post-Route Learning**
- How parasitics affect timing  
- How SPEF file improves STA accuracy  
- Final timing closure reasoning  

---

## 4.3 Why VSDBabySoC is a Good Learning Platform

- Small size → fast iterations  
- Clean RTL → easy to understand  
- Full SoC structure → realistic  
- Works very well with OpenLane  
- Great for learning RTL → GDS flow entirely  

---

