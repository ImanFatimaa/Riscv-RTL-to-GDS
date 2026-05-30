# RISC-V RTL-to-GDS Physical Design Flow

This repository presents a complete **end-to-end RTL-to-GDSII implementation** of a RISC-V based digital design using an open-source ASIC design flow. The project demonstrates the full VLSI backend flow starting from RTL description to final GDSII generation, suitable for fabrication.

---

## Project Run Information

This implementation corresponds to the following automated flow run:

All stages from synthesis to signoff were executed successfully using an OpenROAD/OpenLane-based toolchain.

---

## Project Overview

The goal of this project is to implement a **RISC-V digital system** and transform it into a manufacturable chip layout using standard ASIC design methodology.

The flow includes:

- RTL Design (Verilog)
- Logic Synthesis
- Floorplanning
- Placement Optimization
- Clock Tree Synthesis (CTS)
- Routing (Global + Detailed)
- Physical Verification
- Timing Signoff
- GDSII Generation

---

## ⚙️ RTL-to-GDS Design Flow

### 1. RTL Design
- Written in synthesizable Verilog HDL
- Modular RISC-V architecture design
- Clean hierarchical structure for backend mapping

---

### 2. Logic Synthesis
- RTL converted into gate-level netlist
- Technology mapping using standard cell libraries
- Timing constraints applied via SDC file
- Optimization for area and timing

---

### 3. Floorplanning
- Core area defined based on utilization target
- Power planning with VDD/VSS rails
- Macro placement and I/O pin configuration
- Aspect ratio optimization

---

### 4. Placement
- Standard cells placed according to timing and congestion constraints
- Global placement followed by detailed placement
- Optimization for wirelength and density

---

### 5. Clock Tree Synthesis (CTS)
- Balanced clock distribution network generated
- Clock skew minimized
- Buffer insertion and clock optimization applied

---

### 6. Routing
- Global routing defines approximate routing paths
- Detailed routing ensures DRC-compliant connections
- Parasitic extraction performed for timing accuracy

---

### 7. Signoff Verification
- Static Timing Analysis (STA)
- Design Rule Check (DRC)
- Layout vs Schematic (LVS)
- Power analysis (dynamic + leakage)

All checks passed successfully in the final stage.

---

### 8. GDSII Generation
- Final verified layout exported as GDSII file
- Ready for tape-out and fabrication
- Represents complete physical implementation of RTL design

---

## Results Summary

From the final run reports:

### Timing Analysis
- Design meets setup and hold constraints after optimization
- Clock tree balanced for minimal skew
- No critical timing violations in final signoff stage

---

### Area Utilization
- Efficient standard cell utilization achieved
- Placement optimized for minimal congestion
- Balanced trade-off between area and performance

---

### Power Analysis
- Power estimation performed using switching activity
- Both dynamic and leakage power analyzed
- Optimized for low-power design considerations

---

### Physical Verification
- DRC: Clean (no rule violations in final layout)
- LVS: Matched (netlist matches layout)
- Parasitic Extraction: Completed successfully

---

---

## Toolchain Used

This project uses a fully open-source ASIC tool flow:

- **Yosys** → RTL Synthesis
- **OpenROAD** → Placement & Routing
- **OpenLane Flow** → Automation pipeline
- **OpenSTA** → Static Timing Analysis
- **Magic / KLayout** → Layout inspection
- **TritonRoute / FastRoute** → Routing engine

---

## Key Achievements

- Complete RTL-to-GDS implementation of RISC-V design
- Successful ASIC backend flow execution
- Clean signoff (DRC, LVS, STA passed)
- Industry-standard VLSI physical design methodology applied
- Fully reproducible open-source flow

---

## Learning Outcomes

This project demonstrates:

- Real-world ASIC physical design flow
- Timing closure techniques in digital IC design
- Floorplanning and congestion handling strategies
- Clock tree optimization methods
- Signoff verification processes
- GDSII generation for fabrication

---

## Author

**Iman Fatima**  
Computer Engineer

---

## future Improvements

- Pipeline optimization of RISC-V core
- Power gating and low-power enhancements
- Multi-clock domain support
- Advanced PPA optimization (Power, Performance, Area)
- Migration to advanced technology nodes (e.g., 28nm / 7nm simulation)

---

## Note

This project is developed for educational and research purposes using open-source tools and publicly available PDKs.
