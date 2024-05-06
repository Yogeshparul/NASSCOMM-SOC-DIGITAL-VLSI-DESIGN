**NASSCOMM SOC DIGITAL VLSI DESIGN**

**Day 1:Introduction to IC package**

### Integrated Circuits (ICs) are the backbone of contemporary electronic devices, ranging from smartphones to sophisticated computing systems. Grasping the architecture and functionality of ICs is essential for understanding the operation of electronic devices at their core. ICs are composed of several critical elements, including packaging, semiconductor chips, connection pads, the central processing core, and Intellectual Properties (IPs), among others. ###

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/d3e1f173-a1b7-4e27-8397-3fd0791805ef)

### Arduino Microcontroller Board: The section in focus depicts the microprocessor (chip) integrated with other components on the board. The chip’s design journey, from conceptualization to physical production, follows the Register-Transfer Level (RTL) to the Graphic Data System II (GDSII) flow. The Arduino platform includes a programmable hardware entity, known as a microcontroller, and a software aspect, the Integrated Development Environment (IDE). This IDE is executed on a computer to develop and upload programs to the microcontroller hardware. ###
NASSCOMM SOC DIGITAL VLSI DESIGN


Introduction to IC package, chip, pads, core and IPs

Integrated Circuits (ICs) serve as the backbone of contemporary electronic devices, ranging from smartphones to sophisticated computing systems. To grasp the workings of electronic devices at their core, one must understand the architecture and functionality of ICs. The essential elements of ICs encompass their encasement, semiconductor chips, connection points, the central processing area, and Intellectual Properties (IPs), among others.
Regarding the Arduino microcontroller board: The emphasized portion depicts the microprocessor (chip) and its connections to various components on the board. The chip’s design journey, from conceptualization to physical production, follows the RTL to GDSII sequence. The Arduino system includes a programmable hardware board, known as a microcontroller, and a piece of software called the IDE (Integrated Development Environment). This software runs on a computer and facilitates the writing and uploading of programs to the hardware board.

 


The processor or System on Chip (SoC) connects to the external environment via various peripheral components on the board. These include the JTAG interface, Flash memory, I2C-EEPROM, power connectors, multiplexed ADCs with General Purpose Input/Output (GPIOs), SDRAM, and others.
  


Upon dissecting the chip, we are presented with the following view: The focus here is on the Quad Flat No-leads (QFN) - 48 package chip configuration. Packaging can vary, featuring assorted dimensions. At the heart of this package lies the chip, to which each pin from the outer package is connected via wire bonds to its corresponding pins on the chip. This configuration facilitates the transmission of external signals from the outside world to the chip.

 

Upon opening the chip, we’re greeted by an array of intricate components. The PADS serve as the gatekeepers, facilitating the flow of signals into and out of the chip, connecting it with the broader world. At the heart lies the Core, a hub where the myriad circuit and digital blocks reside. Tucked away in the corner, the Die mirrors the chip’s overall dimensions. This typical core is a bustling neighborhood, home to the System on Chip (SoC), Static Random-Access Memory (SRAM), Phase-Locked Loop (PLL), Analog-to-Digital Converters (ADCs), Digital-to-Analog Converters (DACs), and more. Among these, the PLL, ADC, DAC, and SRAM are collectively known as Foundry IPs, while the SoC and Serial Peripheral Interfaces (SPIs) are referred to as Macros, the building blocks of digital design.

 
(Foundry IPs: Needs intelligent to build these blocks)

QFN-48 Package : The QFN-48 package acts as a safeguarding shell, encapsulating integrated circuits (ICs) to streamline handling and integration onto a printed circuit board, shielding the devices from potential harm.
The designation QFN-48 stands for Quad Flat No-leads, indicating a configuration with 48 contact points designed for surface mounting. The electronics industry employs a diverse array of packaging types, such as through-hole, surface mount, chip carriers, pin grid arrays, flat packages, and ball grid arrays. These compact housings enable the precise placement of ICs onto circuit boards.
These packages find their utility across a spectrum of applications, including but not limited to:
•	Automotive
•	Consumer electronics
•	Industrial and power applications, among others.
 


At the center of the quad flat package, you’ll find the core of the chip, a marvel of engineering neatly nestled within.
An integrated circuit (IC) is a miniature ecosystem of millions of transistors, capacitors, and resistors, all residing on a semiconductor chip. These ICs come in an assortment of sizes and packages, each tailored for its unique role.
The System on Chip (SoC) is a specialized type of IC that amalgamates the functional elements of numerous electronic devices onto a single chip. It’s a microcosm of technology, potentially housing a CPU, memory, inputs, outputs, along with various ICs and Intellectual Properties (IPs). SoCs are the powerhouses behind a multitude of computing tasks and are commonly found in devices like mobile phones, laptops, tablets, and AI-driven gadgets.
The architecture of the chip comprises two primary areas: the core and the die. The die is a slice of semiconductor material where the core, the essence of the chip’s logic, is crafted.
The core is the domain where the chip’s fundamental logic circuits are positioned, forming the brain of the design.
Chips begin their life as part of a silicon wafer, typically ranging from 9 to 12 inches in diameter. This wafer is then segmented into individual pieces, each embodying the same functionality as the core logic circuit, known as the Die.

 

External connections can be established by positioning Pads onto the rectangular metal patches, as illustrated in the figure above.


Introduction to RISC V –ISA

RISC-V is an open-source Instruction Set Architecture (ISA), originally created at the University of California, Berkeley. It adheres to the classic RISC (Reduced Instruction Set Computing) principles and is distributed under open-source licenses. A variety of companies are currently offering or planning to release hardware based on the RISC-V architecture, and there are open-source operating systems available that support it. This instruction set is compatible with numerous widely-used software toolchains.
Designed for flexibility, the RISC-V instruction set features 32-bit instructions that are fixed in length and naturally aligned, while also allowing for extensions that can vary in length, composed of 16-bit units. The architecture accommodates 32-bit and 64-bit address spaces, catering to different computing needs.
In terms of hardware design, the chip is linked to its package through bond wires. The process of executing a C-program involves its translation by a compiler into Assembly language, which is then converted into binary streams that are processed by the chip. Additionally, there is an HDL (Hardware Description Language) interface where a C-program is translated into a RISC-V specification in RTL (Register Transfer Level), which is then used to create the chip layout.

 





Application software to Hardware

 


Application Software - > System Software - > Hardware chip
Applications are integrated into a segment of system software, which translates the entire program into binary code. Within the system software, there are several layers, including the Operating System, Compiler, and Assembler. The Operating System is responsible for managing input/output operations, memory allocation, and overseeing low-level system functions. The Compiler processes the output from the Operating System, which could be in languages like C, C++, or Java, and transforms it into a set of instructions specific to the hardware in use (for example, if an ARM processor is used, the instructions will be in the ARM set). The Assembler then converts these instructions into corresponding binary numbers. This binary code is sent to the hardware, which executes the operations based on the received functions and produces the output. In essence, the instructions serve as an abstract layer between the C-language and the hardware components.

 

 



SoC Design using OpenLane
 
Exploring Open Source Solutions in Digital ASIC Design
Understanding RTL Design: In the realm of digital circuit design, Register-Transfer Level (RTL) represents a conceptual layer that encapsulates the movement of digital signals between hardware registers and the logical manipulations applied to these signals. This abstraction is pivotal in modeling synchronous digital circuits. A variety of open-source resources are accessible to support such designs.
Decoding EDA Tools: Electronic Design Automation (EDA) encompasses a suite of tools employed in the crafting and validation of integrated circuits (ICs), printed circuit boards (PCBs), and comprehensive electronic systems. The open-source community offers a plethora of tools in this domain, including notable ones like Qflow, OpenROAD, and OpenLANE.
Demystifying PDK: The Process Design Kit (PDK) serves as an instrumental software package in the arena of semiconductor process design and simulation. It furnishes an extensive array of tools and libraries that aid in the modeling and simulation of diverse facets of semiconductor manufacturing processes. These facets include but are not limited to process flows, equipment configurations, and procedural parameters. Semiconductor manufacturers leverage PDKs to refine and hone their manufacturing processes, spanning from the nascent stages of development to the culmination of production. Utilizing PDKs facilitates the identification and resolution of process bottlenecks and prospective issues, thereby mitigating defect risks and enhancing the yield and quality of the final semiconductor products.

 
In 2020, Google unveiled an open-source Process Design Kit (PDK) for the production of 130nm chips using SkyWater Technology’s processes. Although the industry has progressed to a 3nm technology node, such advanced nodes are not always necessary for many applications. Moreover, the cost associated with these advanced nodes is significantly higher compared to 130nm processors. Despite being an older technology, 130nm processors are still capable of delivering high performance. For instance, Intel’s Pentium 4 Extreme Edition, which operates at 3.46 GHz (released in Q4 2004), and the Sky130_OSU (a single-cycle RV32i CPU) pipeline version, can both achieve clock speeds exceeding 1 GHz.

 





 

Step 2: Floor and Power Planning - The process of floor planning involves segmenting the silicon expanse of a chip into defined regions or blocks, where components and interconnects are strategically distributed. The primary goal is to enhance the chip’s layout by optimizing the placement of components and interconnects, thereby shortening the distances between them, reducing the quantity of interconnects, and ultimately boosting the chip’s performance.
During this stage, the chip is partitioned into smaller sections known as ‘dies,’ which are further subdivided into ‘cores.’ This subdivision allows for a more efficient arrangement of components and interconnects within the cores.
The overarching aim is to meticulously plan the silicon territory and ensure an even distribution of power across the entire circuit. Chip floor planning entails allocating chip dies to various system components and positioning the input/output pads. Micro floor planning specifies the dimensions, pin locations, and row arrangements. In constructing the power network, a series of metal strips are laid out horizontally and vertically to connect all components to the power supply, which typically includes multiple VDD and GND lines. The use of parallel structures in this network minimizes resistance and the resultant IR drop. To combat electromigration issues, the power distribution network employs the thicker upper metal layers, which offer lower resistance compared to the thinner lower layers."

 

 

Step 3: Placement - Following the completion of floor and power planning, the next phase is placement. In this stage, macros are positioned according to the gate-level netlist. To minimize delays caused by interconnects, cells are arranged in proximity within an organized grid of rows and columns. This phase typically involves two stages of placement: an initial Global Placement, which provides a rough layout, followed by Detailed Placement, which meticulously positions each cell to optimize the design.

 


Step 4: Clock Tree Synthesis - Once placement is finalized, the next critical step is to distribute the clock signal prior to signal routing. The clock tree synthesis phase is dedicated to dispersing the clock signals across the chip with the least possible skew. Various methodologies are employed in clock tree synthesis, including the H-tree, X-tree, fishbone, and sometimes a hybrid approach combining elements of these techniques.

 


Step 5: Routing Following the clock tree synthesis, the next phase involves signal routing. This step requires determining a valid configuration of horizontal and vertical wires within a given placement, utilizing a fixed number of metal layers. The objective is to establish connections between the cells. The router selects from the metal layers specified in the Process Design Kit (PDK), which outlines their properties such as thickness, width, length, and vias.

 

SKYwater PDK Routing Layer Definitions: The SKYwater PDK outlines the hierarchy of routing layers, starting with the lowest layer, which is the local interconnect layer composed of a TiN layer. Above this are five metal layers made of aluminum. The majority of routers operate on a grid system. These metal tracks create extensive routing grids, and the routing process employs a ‘divide and conquer’ strategy. Specifically, global routing is responsible for generating routing guides, while detailed routing utilizes these guides along with fine-grained methods to implement the wiring.
Upon completion of the routing, the process advances to the final layout phase, which includes verification. The Design Rule Check (DRC) ensures compliance with design standards, followed by the Layout Versus Schematic (LVS) check. The final step is timing verification, conducted through static timing analysis to identify any timing discrepancies.


Introduction to Openlane and Strive chipsets
OpenLane streamlines the process from RTL to GDSII, integrating tools like OpenROAD, Yosys, Magic, Netgen, CVC, SPEF-Extractor, and KLayout, along with custom scripts to enhance design exploration and optimization. It encompasses the complete ASIC implementation process, from RTL all the way to GDSII. OpenLane is versatile, suitable for creating Macros and entire chips, and offers two operational modes: autonomous for automated workflows or interactive for hands-on control.

 

 


Flow diagram of OpenLane ASIC Flow: Design to GDSII

OpenLane integrates a suite of open-source tools, including MAGIC, OpenRoad, Fault, Yosys, and QFlow. The process begins with RTL synthesis, where the RTL is input into Yosys alongside design constraints. This RTL is then transformed into logic circuits using SCL components. Following optimization, it is mapped onto synthesized cells with the help of ABC, resulting in the generation of ABC scripts.

 
Exploration of synthesis offers a detailed report on the delay and area of the synthesized netlist, enabling design optimization. OpenLane features a Design Exploration tool that assists in selecting optimal configurations tailored to specific design requirements. This tool is instrumental in identifying configurations that yield the most efficient layout. Additionally, the OpenLane regression report provides a compilation of the best-known results and alerts users to any timing violations within the design.

 

The DFT test, which utilizes the FAULT tool, is an optional step. Following this, the process transitions to physical implementation, encompassing a series of steps executed by the OpenROAD application. This phase includes floor and power planning, the insertion of decoupling capacitors and tap cells, component placements, clock tree synthesis, and routing, collectively referred to as automated Place and Route (PnR).

 

The OpenROAD application is utilized after the physical implementation phase, which encompasses multiple steps such as floor and power planning, the insertion of decoupling capacitors and tap cells, component placement, clock tree synthesis, and global routing. This suite of processes is collectively referred to as automated Place and Route (PnR). The antenna rule is a guideline that determines the allowable ratio between the area of metal lines and the connected gate areas.
The VLSI process begins with the substrate, followed by the device layer, and subsequently the metal layers. During the etching process, electrical charges accumulate on the metal layers. As part of the synthesis process, antenna diodes are integrated into the gate netlist.
Further optimization transforms the gate-level netlist within OpenRoad. This transformed netlist is then verified for logic equivalence using the YoSys tool, ensuring functional consistency with the original design. Yosys also carries out detailed routing post-LEC. Subsequently, an antenna violation check is conducted, and if necessary, antenna diodes are repositioned to rectify any violations. These antenna diodes are provided by the Standard Cell Library (SCL).
 

 

 

 

In the OpenLane design process, the finalization phase encompasses Static Timing Analysis (STA), Design Rule Checking (DRC), Layout Versus Schematic (LVS), and the extraction of Resistance-Capacitance (RC) data from the analysis of the routed layout. This phase culminates in the production of a suite of reports that facilitate the Static Timing Analysis. The RC extraction is performed by converting DEF to SPEF, and the STA is conducted using OpenSTA within the OpenROAD framework.


Get familiar to OpenSource EDA tool

Get familiar with open-source EDA Tools
We are actually interested in working in openlane_working_dir directory.

image


But let's explore what is inside the vsdflow directory--

Screenshot 2024-05-01 170426

Screenshot 2024-05-01 170645

Actually in the openlane_working_dir, there will be two directories-- openlane and pdks.
Screenshot 2024-05-01 175007

pdk stands for "process design kit".
In the above openlane directory, we will be actually doing everything.
Coming to the pdks directory, This folder has all the information related to the pdk. The pdk which we will be using for this workshop is SkyWater 130nm pdk. This was recently made open source. So openlane is built around this pdk.
In the pdks directory, there is a skywater-pdk folder which has all the pdk related files (timing libraries, lef files). So all these silicon foundry files are compatible to work with commercial EDA tools and not with open-source EDA tools.
Screenshot 2024-05-01 180333

So open_pdks basically plans to solve that problem. They are basically sets of scripts and files that convert these foundry-level pdks to be compatible with open-source EDA tools like Magic, netgen, etc.
Sky130A is that pdk that has been made compatible to work with an open-source environment.
Inside the Sky130A directory we will see two directories-- libs.ref and libs.tech.
Screenshot 2024-05-01 181429

libs.ref contains all the technology-specific files and libs.tech contains tools-specific files.
Screenshot 2024-05-01 180658

Inside the libs.ref directory, we will be working with sky130_fd_sc_hd which contains all the technology files.

Now, we will actually start our labs from the openlane directory.
vsduser@vsdsquadron:~/Desktop/work/tools/openlane_working-dir/openlane/$
To invoke the openLane we have to use the two commands that are docker and flow.tcl -interactive. (interactive means all the process is done step by step.)

Now the openLane has been invoked.

The next command should be package require openlane 0.9..( this command basically imports all the packages which is required for the flow).


So these 3 steps have to be done every time.

All the designs that are run by the openlane are extracted from the designs folder present inside the openlane directory.

These are all the designs already built-in in the openlane. but we will be doing it for picorv32a.

Screenshot 2024-05-01 183746

The picorv32a directory will have src folder and config.tcl file.
The "src" folder will contain .v and .sdc files inside it.
Screenshot 2024-05-01 185018

config.tcl bypasses any configurations that have been already done into openlane.
command to open config.tcl file--
$ less config.tcl
In the config.tcl file, we actually set the design_name, Verilog files, sdc files, clock period, clock port, and filename variable and then we source this file. if suppose clock period is set to any other value in the flow as default, then we can override that value using config.tcl file.
So, the precedence in which the openlane takes the value is first the "default value already set in the openlane", and second is the "value set in the config.tcl file" and the third is the "sky130A_sky130_fd_sc_hd_config.tcl" which means the last one has the highest priority.
Now coming back to openlane--

The next command is prep -design picorv32a and after that, it will show Preparation complete.
Here we actually prepare the design setup stage. we need to set up the file system specific to the flow. i.e. each & every step of the flow will be fetching files from a particular location. So that location needs to be created.
mergeLef.py means it has merged both the .lef and .tlef files into one mergeLef.py file.
After the Preparation complete state, we will first check if any directory is created in the picorv32 directory or not!!.. We will see that a runs directory is created in the picorv32 directory and inside the "runs" directory a folder with today's date will be created inside this directory.
Screenshot 2024-05-01 194254

Inside this directory, the folder structure required by the openlane will be present.

As per now except for the "tmp" folder, rest all the folders will be empty.

tmp folder is where temporary files are stored.

results folder is present for each of the stage. So as per now, nothing has been run, so there will be nothing inside this folder.

reports folder will contain the report inside each of the stages in the flow.

The config.tcl file present here shows which all parameter is being taken by the run. i.e. "pdk", "lef information", "tracks information", "tlef information", "library information". So if we make any changes in the original configuration file, after running the floorplan, that will be updated here in this config.tcl file.

The cmds.log file takes the record of all the commands that we have used.

After checking "runs" directory, now we will give command as run_synthesis.

Screenshot 2024-03-15 081613

After the synthesis is over, we will check how the result has been displayed in the "runs" directory.
This is the synthesis result. we calculated the flop ratio.

Screenshot 2024-03-15 095813






