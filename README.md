# 32-bit Floating Point Multiplication based on IEEE-754

## Overview
This project implements a **32-bit floating point multiplier** based on the **IEEE-754 standard** using **Verilog HDL**. The design performs multiplication of two floating-point numbers with high accuracy and follows the IEEE-754 single-precision format. The project also includes functional verification using **UVM** and GDS-II layout generation using **OpenROAD**.

## Features
- Implements **32-bit floating point multiplication** using IEEE-754 standard
- Designed using **Verilog HDL**
- Functional verification using **Universal Verification Methodology (UVM)**
- Physical design using **OpenROAD-flow**
- Reports **design area, clock frequency with positive slack < 1, and power consumption**

## Project Structure
```
├── src/                 # Verilog source code
│   ├── fp_multiplier.v  # Main floating-point multiplier module
│   ├── tb_multiplier.v  # Testbench for simulation
├── verification/        # UVM-based verification environment
│   ├── testbench.sv     # UVM testbench
│   ├── sequence.sv      # UVM sequence
├── physical_design/     # OpenROAD flow scripts
│   ├── constraints.sdc  # Timing constraints
│   ├── floorplan.tcl    # Floorplanning script
│   ├── placement.tcl    # Placement script
│   ├── routing.tcl      # Routing script
├── reports/             # Generated reports
│   ├── area_report.txt  # Design area report
│   ├── timing_report.txt # Timing analysis
│   ├── power_report.txt # Power consumption report
├── fp_multiplier_project.tar.xz  # Compressed project files
├── README.md            # Project documentation
```

## Setup & Usage
### 1. Clone the Repository
```bash
git clone https://github.com/sharanurk/32-bit-Floating-Point-multiplication-based-on-IEEE-754-.git
cd 32-bit-Floating-Point-multiplication-based-on-IEEE-754-
```

### 2. Running Simulation
You can use **EDA Playground**, **Vivado**, or **ModelSim** to run the simulation:
```bash
vlog src/fp_multiplier.v src/tb_multiplier.v
vsim -c -do "run -all"
```

### 3. Functional Verification (UVM)
```bash
vlog verification/testbench.sv
vsim -c -do "run -all"
```

### 4. Physical Design using OpenROAD
```bash
cd physical_design
openroad -script floorplan.tcl
openroad -script placement.tcl
openroad -script routing.tcl
```

## Results
- **Design Area:** Reported in `area_report.txt`
- **Clock Frequency:** Achieved with positive slack < 1
- **Power Consumption:** Reported in `power_report.txt`
