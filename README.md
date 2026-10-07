# SkyWater 130nm 2-Input AND Gate (RTL-to-GDSII)

This repository contains the complete physical design implementation, test results, timing reports, and GDSII deliverables for a 2-input AND gate designed using **OpenLane** and the **SkyWater 130nm PDK** (`sky130A`).

## 📌 Design Summary
* **Cell Name:** `and_gate`
* **Target Technology:** SkyWater 130nm High-Density (`sky130_fd_sc_hd`)
* **Core Area:** $100 \times 100\ \mu\text{m}$
* **DRC / LVS Status:** Clean (0 violations)
* **Primary EDA Tools:** Yosys (Synthesis), OpenROAD (Floorplan/Place/Route), Magic & KLayout (DRC/GDSII/XOR), Netgen (LVS)

---

## 📁 Repository Structure
```text
git_clean/
├── config.json             # OpenLane run configuration parameters
├── README.md               # Project documentation and summary
├── src/
│   └── and_gate.v          # Verilog HDL design source
├── results/
│   ├── and_gate.gds        # Final physical layout file (GDSII)
│   └── and_gate.v          # Synthesized gate-level netlist
└── reports/
    ├── metrics.csv         # Complete run metrics summary
    ├── manufacturability.rpt # DRC/LVS manufacturability report
    ├── synthesis/          # Yosys gate counts, area, and pre-layout STA
    ├── floorplan/          # Core & die area specs
    ├── placement/          # Global & detailed placement STA reports
    ├── cts/                # Clock tree synthesis STA and skew logs
    ├── routing/            # Global & detailed routing STA and wire lengths
    └── signoff/            # Parasitic extraction (RCX), LVS, and Magic DRC reports
