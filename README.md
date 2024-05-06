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

**
**Get familiar to OpenSource EDA tool****

In order to access the OpenLane tool, we will be needing some basic linux commands.They are listed below

pwd : It displays the present working directory and its path.

cd : Using this command we can move in both ways in the directory tree.

ls : It lists all the sub-directories and files present in the current directory.

mkdir : Using this command, we can create a new directory.

rmdir : Using his command, we can delete an existing directory.

rm : This command is used to delete the files.

help : using this command we can know the working of any command.

clear : This command clears the terminal.

**Design Preparation Setup**

OpenLane directory, one should use the docker command. This command grants access to BASH. Upon entering BASH, it is necessary to execute the flow.tcl script, as this file contains the required steps for OpenLane operation. Additionally, the -interactive switch must be used alongside the tcl file to facilitate a step-by-step process. Without the -interactive switch, the entire flow, from RTL to GDS, will execute at once, culminating in a final report. The appropriate command for this procedure is ./flow.tcl -interactive. Once OpenLane is activated, a change in the prompt will be noticeable, indicating the need to input the packages essential for running the flow. To do this, the command package require openlane 0.9 is used.

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/e5d9bed2-8da7-430d-8d65-e05d7c340e62)

we need to setup the design and for that the command will be prep -design picorv32a.
![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/1a5830ae-2f24-4642-900a-7d9264a99adc)

After Preparation is done a directory with current date will be created in the runs folder.And in that directory all the directorys that are needed to store the results , reports etc.. will be created.

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/937f220e-217c-4415-b3ef-30152dfaf67b)

there will be a directory named ‘tmp’ which contains various types of files. One of these files is the ‘merged.lef’ file; it includes information on both the metal layer level and the cell level

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/4212bbbb-9f8e-4d12-a15b-690a256e3915)

We need to perform synthesis on the design. To do this, we must use the command run_synthesis. The tool will take some time to perform the synthesis; upon completion, it will display the message ‘Synthesis was successful
![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/76e329f8-9c57-4b4c-8259-018289783302)

**Synthesis results**

Now we need to find out the flipflop percentage in total cells. For this we use reports from Synthesis stage

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/471e0bc7-6aeb-41e9-91af-927e1eb5c485)

We can observe that the total number of cells used in the design is 14,876 and the number of D-flip-flops is 1,613. Therefore, the percentage of flip-flops, also known as the Flop Ratio, is calculated as follows:
Flop Ratio=(Total number of cellsnumber of flip-flops​)×100=(148761613​)×100=10.84%
Before performing synthesis, the reports directory was empty. After synthesis, the reports generated during the process are stored in the reports directory

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/14a59109-33a5-403e-8abe-2b0c6d25a389)

**##DAY 2 - Good floorplan vs bad flooeplan and introduction to library cells##**

**Steps to Run a Floorplan Using OpenLANE**

To ensure a smooth floorplan run in OpenLANE, designers must be mindful of certain switches that affect changes in the floorplan. For instance, the utilization factor and aspect ratio are among these switches. It is crucial for the designer to verify that these switches are correctly configured and aligned with the project’s requirements before initiating the floorplan. The image below illustrates the various types of switches available at the floorplan stage

**see the configurations in the OpenLANE**
![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/5667cd1a-3d0c-4b16-8100-4af029130c89)

**The floorplanning.tcl and readme files look like this**

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/40175765-8673-4e2c-9dea-1014c76e2fca)

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/84627902-9bf9-4ab9-a91f-a06983ee7cd2)

In OpenLane, the lowest priority is assigned to the system default (Floorplanning.tcl), the second highest priority to config.tcl, and the highest priority to PDK_variant.tcl when determining the values for switches

**##Review Floorplan files and steps to view floorplan##**
After confirming that all the switches meet the requirements, we should execute the run_floorplan command to initiate the floorplan stage.

If any errors arise during the floorplan stage, they will be displayed. If no errors are displayed, then our floorplan stage has successfully completed.

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/81751291-1d50-4c43-8bea-459203a8811b)

After completion of the floorplan we can check the report generated by the tool and check some of the aspects like die area etc but in order to view the design in GUI we should use MAGIC tool.

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/e1056499-aec5-4f41-8e59-273316dbdcf7)

**Steps for acessing magic tool:**
Enter this command magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &

GUI floorplan looks like this
![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/96f52414-119d-4aba-8ebe-8e8af1c6d010)

**##Review Floorplan layout in magic##**
Press Q+S to select the layout. Press V to center the selected layout. Tap cells are utilized to control the latch-up condition by connecting the N-Well to Vdd and the substrate to Gnd. The layout will appear as follows in Magic
![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/3b495aa2-276e-49a1-b19b-25ff6a097aea)

In order to select the pin just palce the cursor and press S. The Pin layers and the dimensions along with the co-ordinates are seen like this

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/de802cfd-5007-4648-8a7c-f5c48128a877)

Images for pin saperation.

![image](https://github.com/Yogeshparul/NASSCOMM-SOC-DIGITAL-VLSI-DESIGN/assets/168162609/199bc06e-c81f-4fa6-8b4c-44ee088e0bcf)



























