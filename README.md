# VSD_Physical-Design-Openlane-SKY130
This is about a 5 day Workshop conducted by VLSI System Design on SOC Design/ Physical Design using Open-Source tools. The entire workflow was carried out in OpenLANE,  an automated RTL to GDSII flow based on several components . The PDK's used here is SKYWATER 130nm, which is an open source Process Design Kit.

# Workshop Contents
 - DAY 1: Inception of Open-source EDA, OpenLane and Sky130 PDK
   - ASIC design Flow
   - OpenLane Directory Hierarchy
   - Lab [Day 1] - Determine Flip-flop Ratio
   
 - DAY 2: Good Floorplan vs Bad Floorplan and Introduction to Library Cells
   - Floorplan Stage
   - Placement Stage
   - Lab [Day 2] - Determine Die Area
    - Library Characterization
    - Timing Characterization
     
 - DAY 3: Design a Library Cell using Magic Layout and Ngspice Characterization
   - Designing a Library Cell
     - SPICE Deck Netlist Description
     - SPICE Analysis for Switching Threshold and Propagation Delay
   - CMOS Fabrication Process (16-Mask CMOS Process)
   - Lab [DAY 3] - Introduction to Sky130 basic layers layout and LEF using inverter
   
 - DAY 4: Pre-layout Timing Analysis and Importance of Good Clock Tree
   - Lab [Day 4] - Extracting the LEF File
   - Plug-in the Customized Inverter Cell to OpenLane
   - Delay Table
   - Fix Negative Slack
   - Locating the Custom Inverter Cell in Layout
   - Setup Timing Analysis
   - Timing Analysis with Real Clocks
   - Multi-corner STA for Post-CTS
   -     
 - DAY 5: Final Steps for RTL2GDS using TritonRoute and OpenSTA
   - Maze Routing - Lee's Algorithm
   - DRC Cleaning
   - Routing Stage and TritonRoute
   - Lab [Day 5] - Power Distribution Network (PDN) and routing
   - SPEF Extraction and GDSII Streaming

### ** DAY-1 - Inception of open-source EDA, OpenLANE and Sky130 PDK ** 
### Theory:
- The Day 1 is all about introduction to the interaction between the software and hardware component of a computer. We came across the use of Open Source EDA tools and about the OpenLANE workflow.
-  Open Source Digital ASIC Design requires three open-source components:  
- **RTL Designs** = github.com, librecores.org, opencores.org
- **EDA Tools** = OpenROAD, OpenLANE,QFlow  
- **PDK** = Google + Skywater 130nm Production PDK
### ASIC Design FLOW
![screenshot 1](https://github.com/user-attachments/assets/07e1fe8b-de49-4ebd-bfaa-ed509f22fd7f)

### Tasks:
-Run 'picorv32a' design synthesis using OpenLANE flow and generate necessary outputs.
-Calculate the Flop ratio and the percentage of D-FFs.

###Introduction to openLANE workflow using linux commands in VDI:
'''
# change the directory to OpenLANE flow directory
cd Desktop/work/tools/openlane_woking_dir/openlane

# To run the OpenLANE docker sub-system
docker

# Invoking the OpenLANE flow in the interactive mode
./flow.tcl -interactive

# Required package
package require openlane 0.9

# To prep the design for running the specific 'picorv32a' design
prep -design picorv32a

# To run synthesis
run_synthesis
'''
### Screenshots of running these commands:

![Screenshot 2024-09-20 142436](https://github.com/user-attachments/assets/6e22a783-0779-4658-88a0-d250d878e198)

![Screenshot 2024-09-20 142336](https://github.com/user-attachments/assets/42b86b5d-f65a-4e59-9e26-06c437f64520)

![Screenshot 2024-09-20 143755](https://github.com/user-attachments/assets/6a49391e-a8f4-407e-adb0-322a99693e2a)

### 2.Calulate the flop ratio with reference to number of dflipflop and number of cells 

### Chip Area for the module - 'picorv32a'

![Screenshot 2024-09-20 144231](https://github.com/user-attachments/assets/b19ac39c-9538-4b78-949d-cc2a1dfa2c10)

### Number of D flip-flop

![Screenshot 2024-09-20 144527](https://github.com/user-attachments/assets/854fd101-9300-4d04-b8af-325b344c8b32)

### Number of cells 

![Screenshot 2024-09-20 144645](https://github.com/user-attachments/assets/40f79759-b810-4056-9ec7-0c7618894cd2)

### flop ratio and Percentage of flop ratio

###### flop ratio = 1613 / 14876 = 0.1084296
###### percentage of flop ratio = 0.1084296 * 100 = 10.84296 %

### Synthesis result file view 
![Screenshot 2024-09-20 145351](https://github.com/user-attachments/assets/8dc3eca7-b648-410b-b75e-834c8ae46409)



