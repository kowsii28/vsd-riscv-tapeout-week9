# vsd-riscv-tapeout-week9
Summary of the VSDBabySoC Design
# VSDBabySoC – Complete Documentation (VSD Internship Week-9 Submission)

**Author:** Kowsalya M  
**Internship:** VLSI SoC Design – VSD x IIT Gandhinagar  
**PDK:** SKY130A – Open PDK  
**Tools Used:** OpenLane, OpenROAD, Yosys, Magic, NGSPICE, GTKWave  

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



