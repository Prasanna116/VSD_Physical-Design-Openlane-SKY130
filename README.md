# VSD_Physical-Design-Openlane-SKY130
This is about a 5 day Workshop conducted by VLSI System Design on SOC Design/ Physical Design using Open-Source tools. The entire workflow was carried out in OpenLANE,  an automated RTL to GDSII flow based on several components . The PDK's used here is SKYWATER 130nm, which is an open source Process Design Kit.

# Workshop Contents
 - [DAY 1: Inception of Open-source EDA, OpenLane and Sky130 PDK]
   - [ASIC design Flow]
   - [What is Openlane?]
   - [OpenLane Directory Hierarchy]
   - [Lab [Day 1] - Determine Flip-flop Ratio]
   
 - [DAY 2: Good Floorplan vs Bad Floorplan and Introduction to Library Cells]
   - [Floorplan Stage]
   - [Placement Stage]
   - [Lab [Day 2] - Determine Die Area]
    - [Library Characterization]
    - [Timing Characterization]
     
 - [DAY 3: Design a Library Cell using Magic Layout and Ngspice Characterization]
   - [Designing a Library Cell]
     - [SPICE Deck Netlist Description]
     - [SPICE Analysis for Switching Threshold and Propagation Delay]
   - [CMOS Fabrication Process (16-Mask CMOS Process)]
   - [Lab [DAY 3] - Introduction to Sky130 basic layers layout and LEF using inverter]
   
 - [DAY 4: Pre-layout Timing Analysis and Importance of Good Clock Tree]
   - [Lab [Day 4] - Extracting the LEF File]
   - [Plug-in the Customized Inverter Cell to OpenLane]
   - [Delay Table]
   - [Fix Negative Slack]
   - [Locating the Custom Inverter Cell in Layout]
   - [Setup Timing Analysis]
   - [Timing Analysis with Real Clocks]
   - [Multi-corner STA for Post-CTS]
   -     
 - [DAY 5: Final Steps for RTL2GDS using TritonRoute and OpenSTA]
   - [Maze Routing - Lee's Algorithm]
   - [DRC Cleaning]
   - [Routing Stage and TritonRoute]
   - [Lab [Day 5] - Power Distribution Network (PDN) and routing]
   - [SPEF Extraction and GDSII Streaming]

### ** DAY-1 - Inception of open-source EDA, OpenLANE and Sky130 PDK ** 

- The Day 1 is all about introduction to the interaction between the software and hardware component of a computer. We came across the use of Open Source EDA tools and about the OpenLANE workflow.
-  Open Source Digital ASIC Design requires three open-source components:  
- **RTL Designs** = github.com, librecores.org, opencores.org
- **EDA Tools** = OpenROAD, OpenLANE,QFlow  
- **PDK** = Google + Skywater 130nm Production PDK
### ASIC Design FLOW
![screenshot1] (https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.einfochips.com%2Fblog%2Fasic-design-flow-in-vlsi-engineering-services-a-quick-guide%2F&psig=AOvVaw0wfd_tSpGxdA5zhbFbJhGC&ust=1737689844122000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCIDtiKD1iosDFQAAAAAdAAAAABAE)


