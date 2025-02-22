# Sky130_Day1: Introduction to QFN-48 Package, Chip, Pads, Core, Die, and IP

## Understanding the Chip Inside a Microcontroller

### **1. Package**
It is the protective enclosure and interface for an ic providing electrical connections,thermal management,and mechanical support
Below is QFN-48(quad flat no leads).

![package](./../images/Day1_images/Package.png)
 
Chip is located inside a package.chip is connected to different pins of package. In 
package,we have 
### **GPIO PINS:**
General purpose input output pins inthe package of a chip are versatile digital pins that 
can be configured by the user to act as either inputs or outputs. 
### **FLASH PINS:**
Flash I/O pins refer to the pins on a microcontroller or microprocessor that are 
specifically designated for interfacing with external flash memory. These pins are used 
to transfer data between the chip and the flash memory
### **Pin Functions:**
#### **Clock (CLK):**
 Synchronizes data transfer between the microcontroller and flash memory.
Data In/Out (MOSI/MISO):
 Used for sending data to and from the flash memory.
#### **Chip Select (CS):**
 Activates the flash memory chip that the microcontroller wants to communicate with Additional Data Lines: 
In protocols like QSPI, additional data lines (e.g., IO0, IO1, IO2, IO3) are used to 
facilitate faster data transfer
#### **Flash csb:**
The term "Flash_CSB" refers to the Chip Select Bar (CSB) pin used in flash memory 
interfaces, particularly in serial communication protocols like SPI (Serial Peripheral 
Interface) and QSPI (Quad SPI).
- Here are the details about the Flash_CSB pin:
- Function: The CSB (Chip Select Bar) pin is an active-low signal used to select the flash 
memory chip that the microcontroller or processor wants to communicate with. When 
the CSB pin is driven low (0V), the corresponding flash memory chip is enabled and 
can participate in data transfer. When the CSB pin is high (inactive), the flash memory 
chip is disabled and ignores communication signals on the other lines
#### **XclkFunction:**
XCLK serves as an external timing source for the device. It provides a stable clock 
signal that the microcontroller or DSP can use for its internal operations, such as 
executing instructions, timing peripheral operations, and driving other clock-dependent 
processes.
#### **VREF_L (Voltage Reference Low)Function:**
The VREF_L pin provides the low reference voltage for the ADC or DAC. This voltage 
defines the lower limit of the input voltage range that the ADC can convert or the output
voltage range that the DAC can produce.
#### **VREF_H (Voltage Reference High)Function:**
The VREF_H pin provides the high reference voltage for the ADC or DAC. This 
voltage defines the upper limit of the input voltage range that the ADC can convert or 
the output voltage range that the DAC can produce
#### **ADC_0_IN:**
 The 0th (first) analog input channel of an ADC, used to sample and convert an analog 
signal to a digital value.
#### **ADC1_IN:**
The 1st (second) analog input channel of an ADC, used similarly for a different analog 
signal.These channels allow the ADC to measure multiple analog signals by converting 
their voltage levels to digital values that the microcontroller can process.
#### **X0 (XTAL_OUT/OSC_OUT):**
 Output pin for the clock signal from the external crystal oscillator.
#### **XI (XTAL_IN/OSC_IN):**
 Input pin for the clock signal to the microcontroller from the external crystal oscillator.
  ![chip_in_package](./../images/Day1_images/chip_in_package.png)
  
 There are also some other components which we need to know:
 
  ![pads_die_core](./../images/Day1_images/pads_die_core.png)
#### **Wire bonds:**
Wire bonds are tiny wires used to connect integrated circuit (IC) chips or semiconductor
devices to the external leads of the package or to other components on a printed circuit 
board (PCB). 
#### **Wire BondsFunction:**
Wire bonds serve as electrical connections between the active elements (such as 
transistors, diodes, or resistors) within the IC chip and the external leads or terminals of 
the package.They provide a means for transmitting electrical signals, power, and ground
connections between the IC and the rest of the electronic circuit.Wire bonds:
Wire bonds are tiny wires used to connect integrated circuit (IC) chips or semiconductor
devices to the external leads of the package or to other components on a printed circuit 
board(PCB). 



 ![pwire_bonds](./../images/Day1_images/wire_bonds.png)
### **Foundry IPs**
Foundry IPs are pre-designed and pre-verified functional blocks or modules that are 
licensed by semiconductor companies for use in their custom IC designs.These IPs are 
developed by semiconductor foundries, specialized IP vendors, or in-house design 
teams and are made available for integration into custom SoCs or ASICs.
#### **Types of Foundry IPs**
- #### **Standard Cells:**
These are basic building blocks of digital ICs, consisting of logic gates (AND, OR, 
etc.), flip-flops, and other fundamental digital circuit elements.
- #### **Memory IPs:**
 These include memory arrays such as SRAM (Static Random Access Memory) and 
ROM (Read-Only Memory), as well as specialized memory controllers
- #### **Interface IPs:**
 These provide standardized interfaces for connecting different components or 
subsystems within an SoC, such as USB (Universal Serial Bus), PCIe (Peripheral 
Component Interconnect Express), HDMI (High-Definition Multimedia Interface), and 
Ethernet.
- #### **Analog and Mixed-Signal IPs:**
These include analog-to-digital converters (ADCs), digital-to-analog converters 
(DACs), analog filters, PLLs (Phase-Locked Loops), and other analog and mixed-signal
circuitry.
- #### **Process-Specific IPs:**
 These IPs are tailored to specific semiconductor manufacturing processes and 
technologies offered by the foundry. They are optimized for performance, power, and 
area characteristics of a particular process node.
### **Die:**
The "die," also known as the "chip" or "dielectric," is the actual semiconductor material 
on which the integrated circuit is fabricated.It is a small, rectangular piece of silicon (or 
other semiconductor material) on which multiple electronic components, such as 
transistors, resistors, capacitors, and interconnects, are fabricated using semiconductor 
manufacturing processes.
- Function:
The die contains the active electronic components of the integrated circuit, including 
logic gates, memory cells, analog circuits, and other functional blocks.It is where the 
primary computational and data processing functions of the IC occur.
### **Core:**
The "core" of an integrated circuit refers to a specific functional block or 
processing unit within the IC.In a multi-core processor, each core is a separate 
processing unit capable of executing instructions independently and concurrently with 
other cores.
- Function:
Cores execute program instructions and perform computational tasks, such as arithmetic
and logic operations, data processing, and control flow operations.In a multi-core 
processor, multiple cores can work together to execute tasks in parallel, improving 
overall performance and efficiency
# **SKY_L2:-INTRODUCTION TO RISC-V**
### **RISC-V:**
RISC-V (pronounced "risk-five") is an open-source Instruction Set Architecture (ISA) 
based on the principles of Reduced Instruction Set Computing (RISC). It was developed
at UC Berkeley and is designed to be simple, modular, and extensible, making it ideal 
for a wide range of applications, from microcontrollers to supercomputers.

![riscv](./../images/Day1_images/RISC-V.png)
### **INSTRUCTION SET ARCHITECTURE:**
An Instruction Set Architecture (ISA) is the interface between hardware and software 
in a computer system. It defines the set of instructions that a processor can execute and 
acts as a blueprint for how software communicates with the hardware. 
- #### **Types of ISA:**
 ##### **1. RISC (Reduced Instruction Set Computer):** 
• Simple instructions, fixed-length, optimized for performance (e.g., RISC-V,
ARM).
 ##### **2. CISC (Complex Instruction Set Computer):**
• Complex instructions, variable length, hardware-intensive (e.g., x86).
 ##### **3. VLIW (Very Long Instruction Word):**
• Executes multiple instructions simultaneously (e.g., Itanium).
 ### **INTERACTION BETWEEN HARDWARE AND SOFTWARE:**
We see that apps run on our laptops,mobile phones etc. They are all hardware. How 
does this happen?
So,there is an interaction between apps and hardware, i.e system software.
 #### **SYSTEM SOFTWARE:**
 System software converts high level programming language like c,c++,java or python to binary level language which is understand by the hardware 
 ![system_softwarre](./../images/Day1_images/System_software.png)
 The major components in system software are 
- 1.Operating system
- 2.Compiler
- 3.Assembler
Os generally handles input/output operations,allocates memory, and does low level 
operations and other part of the operating system converts into assembly language.
Apps are written in high level languages like c,c++. they are fed to the compiler. We 
have a set of instructions. These instructions are dependent on hardware. The hardware 
may belong to mips,intel etc.
we obtain a *exe files. The obtained *exe files are fed to the assembler.The job of 
assembler is to convert *exe file into binary language. This is given to hardware, now it 
generates ouptut.
So, in general, The Instruction set Architecture is fed to the assembler through RISC-V 
assembly language. We write a RTL(Register Transfer level) snippet which understands 
instructions. Then we get a netlist for given RTL. It is implemented to hardware.
![risc_flow](./../images/Day1_images/RISC_flow.png)
  ### **SOC:**
A System on chip(S0C) is an integrated circuit that consolidates multiple components of a complete 
system into a single chip. It typically includes Processor, memory, input/output interfaces,specialized 
modules,power management. Soc optmize power,size and performance,making them ideal for compact
and energy efficient deisgns.
 ### **SOC DESIGN FLOW:**
SOC design flow involves several stages to develop a complete system on a chip.Here’s a brief overview 
![aoc_design_flow](./../images/Day1_images/SOC_design_flow.png)
### **ASIC DESIGN FLOW:**
The ASIC (Application-Specific Integrated Circuit) Design Flow is the step-by-step 
process of designing and fabricating an ASIC .
They require three important key components: 
1. Register Transfer level Intellectual properties.
2. Electronic design automation tools.
3. Process design kit Data
![pasic_design_flow](./../images/Day1_images/ASIC_design_flow.png)
### **RTL IP’S:**
RTL IPs (Register-Transfer Level Intellectual Properties) are reusable pre-designed 
hardware components described in an HDL (e.g., Verilog, VHDL). They represent 
functional blocks that can be integrated into larger digital systems during chip design. 
RTL IPs are a critical part of modern ASIC and SoC (System-on-Chip) design, enabling 
faster development cycles and reduced effort for implementing complex designs.
They are built once, and can be reused.
### **ELECTRONIC DESIGN AUTOMATION TOOLS:**
EDA Tools are specialized software platforms used in the design, analysis, verification, 
and manufacturing of complex integrated circuits (ICs). These tools enable the 
automation of VLSI design processes, handling the complexity of modern ICs with 
millions to billions of transistors. 
Some EDA tools are Openlane, OpenRoad, Qflow.
### **PROCESS DESIGN KITS:** 
PDKs are collection of files used to model fabrication for the EDA tools to design a IC.
It acts as a interface between fabrication units and designers. 
The key components of PDK are design rules,technology files,standard cell libraries, 
SPICE models etc.
### **DESIGN FLOW**
![ASIC_](./../images/Day1_images/design_flow.png)
 ### **INTRODUCTION TO OPENLANE AND STRIVE SOC FAMILY**
 Strive is a family of open everything. For example like open pdk, open eda, open rtl
 ![pstrive](./../images/Day1_images/Strive.png)
 ### **OPENLANE:**
OpenLane is an open-source, fully automated RTL-to-GDSII (Register Transfer Level 
to Graphic Database System II) flow for digital ASIC design. It is a part of the 
OpenROAD project, developed under the DARPA IDEA program, and is actively 
maintained by the community, including contributions from organizations like Efabless 
and Google.
OpenLane aims to democratize chip design by providing a platform that integrates 
open-source tools and methodologies, enabling users to design and tape out custom 
ASICs with minimal cost..Its main goal is to produce a clean GDS||.. It is tuned for 
skywater 130nm open pdk.
There are two modes of operation:
1.Autonomous
2. Interactive
 #### **AUTONOMOUS MODE OF OPERATION:** 
In this mode, OpenLane executes the entire ASIC design flow from start to finish 
automatically, requiring minimal user intervention.User provide configuration files 
and input files (e.g., RTL code, constraints) at the beginning, and OpenLane 
handles all steps, including synthesis, floorplanning, placement, routing, and 
verification. 
#### **INTERACTIVE MODE OF OPERATION:**
Provides a step-by-step execution of the design flow, allowing users to control and 
customize individual steps as needed.In this mode, designers interact with OpenLane 
via a command-line interface (CLI) to execute specific stages of the flow manually. 
Openlane has the best of flow configuration. They have 43 best design configuration
### **Tools used in openlane flow:**
![Openlane_flow](./../images/Day1_images/Openlane_flow.png)
 
### **YOSYS:**
Yosys is an open-source framework for Verilog synthesis. It converts high level RTL descriptions into gate-level netlists optimized for technology libraries.Supports Verilog input.
- Performs logic synthesis, optimization, and technology mapping.
- Integrates seamlessly with tools like ABC for logic optimization.
- Widely used in open-source ASIC design workflows like OpenLane. 
### **ABC:**
ABC is a tool for logic optimization and synthesis, specializing in sequential and 
combinational logic circuits. It operates on gate-level representations to improve circuit 
performance, area, and power. 
### **OPENSTA:**
OpenSTA (Open Source Timing Analyzer) is a static timing analysis tool 
used to verify whether a design meets its timing constraints.
### **MAGIC:**
Magic is an open-source layout editor and analysis tool for VLSI design. It is 
used for creating and verifying IC layouts.
### **NETGEN:**
Netgen is an open-source tool used for comparing netlists and performing 
Layout Versus Schematic (LVS) checks. 
### **KLAYOUT:**
KLayout is a powerful, open-source IC layout viewer and editor. It 
supports multiple formats like GDSII and OASIS.
### **FAULT:** 
Detects and analyzes faults or defects in the ASIC design layout to ensure 
reliability and robustness. It performs DFT(Design Foe Test). 
## **FILE FORMATS IN OPENLANE FLOW**
#### **1. RTL Files (Verilog/VHDL)(.v)**
Represents the design in Register Transfer Level 
(RTL) code.
### **2.NETLIST FILE(.V):**
Represents the circuit after synthesis, showing the logical 
components (gates, flip-flops, etc.) and their connections. 
### **3.CONSTRAINTS FILE:(.tcl):**
Defines various constraints like timing, placement, and
area that must be met during the design flow. 
### **4.DESIGN EXCHANGE FORMAT(.def):**
Represents the physical design of the 
circuit, including cell placements, routing, and pin information. 
### **5.STANDARD PARASITIC EXCHANGE FORMAT(.spef):**
Contains parasitic 
resistance and capacitance data, which is extracted from the layout to help in accurate 
timing analysis. 
### **6.Graphic Database System II (.gds):**
Represents the final layout of the design in a 
standard format for fabrication. 
### **7.LIBRARY EXCHANGE FORMAT(.lef):**
Describes the physical attributes of cells 
in a library, including cell sizes, pin positions, and layer information. 
### **8.LIBERTY FILES(.lib):**
Contains timing and power models for standard cells 
(libraries). It is essential for synthesis and timing analysis tools. 
### **9.SYNOPSYS DESIGN CONSTRAINT(.sdc):**
Specifies constraints for the design, 
such as clock definitions, input/output delays, and timing exceptions. 
### **10.RC EXTRACTION(.rcs):**
Represents the extracted resistance and capacitance 
values for parasitic analysis. 
### **11. REPORT FILES(.rpt OR .log):**
Contain detailed logs and status reports of each 
tool executed during the design flow.
### **12.LAYOUT VS SCHEMATIC(.lvs):**
Contains results from the Layout Versus 
Schematic check, ensuring that the layout matches the schematic in terms ofconnectivity. 
### **13.DESIGN RULE CHECK(.drc):**
Contains results from the Design Rule Check, 
which ensures that the layout adheres to the design rules specified by the foundry
# *WORKING WITH OPENSOURCE EDA TOOLS:*
Openlane consists of various tools.Let’s know about openlane_directory 

➢ Open the Terminal. 

➢ Go to openlane directory using cd Desktop/work/tools/openlane_working_dir.

![pss9](./../images/Day1_images/s_9.png)

**openlane_working_dir** consists of three subdirectories:

1.pdks 2.openlane_old 3.openlane

➢ Go to **pdks** directory.

Pdks directory consits of all the inofrmation related sky130nm technology. We can see three sub directories: 1) sky130A 2)open_pdks 3)skywater_pdk

![pss10](./../images/Day1_images/s_11.png)

we work with skywater-pdk. This pdk contains all related lef files, .lib files, 
timing etc.

Now lets go to the sky130A directory

![pss11](./../images/Day1_images/s_10.png)




let us see libs.tech

**libs.tech:**
This directory consists of list of tools used in the openlane.
![pss13](./../images/Day1_images/s_12.png)

**libs.ref:**
it contains all the process specific files with cell , timing etc.
![s_29](./../images/Day1_images/s_13.png)


ow lets go to the **sky_130_fd_sc_hd** directory. (fd-abbrivieated for foundry, sc-standard cell, hd-high density)
![pss14](./../images/Day1_images/s_14.png)

➢ open **sky130_fd_sc_hd** directory and then techlef. 

![pss9](./../images/Day1_images/s_16.png)

![pVirtual_box](./../images/Day1_images/VirtualBox_VLSI_26_01_2025_14_47_56.png)

techlef files are saved with .tlef extension.
Now go back to the **openlane_working_directory**. And then open **openlane.**


![pss17](./../images/Day1_images/s_17.png)
This directory consists of various files related to the openlane flow like 
configurations, README.md and design examples and many more. 

- Now, go to the designs directory. 
- Here, we will see different design examples, which are already present in 
openlane and also some new designs are going to be added later. 

- In these examples, we are going to work with the design picorv32a.
 Navigate to the picorv32a directory.
 
 ![desktop](./../images/Day1_images/des.png)
 
 ![pico](./../images/Day1_images/cd_pico.png)
 
Here we can see different files inlcuding config.tcl and src.

 **config.tcl** : Then config.tcl file containsTcl (Tool Command Language) 
commands that define various settings and parameters crucial for executing the 
Openlane flow tailored to a specific design project. Within this file, essential 
design parameters such as the project name, file paths, clock frequency targets, 
and environmental conditions are typically specified. Additionally, it houses 
technology-specific details such as the chosen technology node, library paths, and 
cell specifications necessary for the design process. 

- Now, go to the src directory as shown below:
 ![src](./../images/Day1_images/cd_src.png)
 Here, we can see the important files related to the design.
 - picorv32a.v : It consists the rtl hardware description of the design. 
- picorv32a.sdc: It contains the variois design constraints like timing constraints, 
input, output constraints etc. 
- Now, run the below command, to read the README.md file
![readme](./../images/Day1_images/cd_readme.png)
 ![read](./../images/Day1_images/readme.png)
  This file contains Various parameters about OPENLANE design flow, openlane 
directory structure and various commands used in the openlane flow both in 
Interactive and Autonomous flow.

 Now, go back to the openlane directory, now go to the configuration directory
 ![configuration](./../images/Day1_images/cd_configuration.png)
 here we have all the tcl files, which are essential in executing openlane flow.
Now lets us know how to open openlane prompt.

➔ Open the directory openlane

➔ type docker to launch openlane as below
 ![v5](./../images/Day1_images/v5.png)
 after that, type ./flow.tcl -interactive so that it starts in interactive mode, we can 
see the results and reports in each step.

➔ We require a package of 0.9

➔ for that type package require openlane 0.9

➔ and then type prep -design picorv32a 
![v11](./../images/Day1_images/v11.png)
In this case the lef and tlef are merged and formed as a single file that is 
merged .lef 

This merged.lef file contains the information related to cells and layers.
 With this, the design setup is completed. 
 
 As, we started the design flow of picorv32a, in the picorv32a directory, a folder 
with the name runs is created as shown below indicating the ASIC design flow is 
started 

Now to check, go to designs directory and then go to picorv32a directory.
In that go runs directory. You can see the design you have created.

![s_22](./../images/Day1_images/s_22.png)
Now open the directory you see. You can see different directories like tmp, reports
and results are created. 

In reports directly, we can review reports of every process in openlane flow as 
shown below.

 Similarly, in the results directly, we can review the resultant file of every process 
in the interactive mode of openlane 

Here you can see another config.tcl file. This file contains the information about 
which design parameters are taken. And in this file, we can know, whether the 
proper execution of every process in Openlane flow, is happenning or not

![v12](./../images/Day1_images/v12.png)
Now go to the tmp directory.

Here, we can see the merged.lef file, which contains the design parameters like 
default units for resistance, capacitance etc. 

![s24](./../images/Day1_images/s_24.png)
Now you can go to the reports directory. You can see all the reports for synthesis, 
floorplan,placement etc.

now lets us see config.tcl present in the directory that you have created

![s25](./../images/Day1_images/s_25.png)

![s_26](./../images/Day1_images/s_26.png)

also let us see sky130A_sky130_fd_fc_hd_config.tcl 

![s27](./../images/Day1_images/s_27.png)

There is an order of precendence in openlane to take the values regarding the 
design requirements.

 The precedence is as follows:
- Default values
-  Values from config.tcl file
- Values from sky130A_sky130_fd_sc_hd_config.tcl file 
**sky130A_sky130_fd_sc_hd_config.tcl** file has the highest precendece and 
default values are of lowest precendence.

 Now, let’s go to the openlane prompt, and run synthesis using run_synthesis and
we get this 

![v18](./../images/Day1_images/v18.png)

Now, lets have the reports and results.

In results, go to the synthesis directory.we can see **picorv32a.synthesis.v.**

![s_28](./../images/Day1_images/s_28.png)

![s_29](./../images/Day1_images/s_29.png)

Here, you can see, various reports are generated. Out of these, **1-yosys_4.stat.rpt** 
is the original report of the synthesis process 
![s_30](./../images/Day1_images/s_30.png)
![s_33](./../images/Day1_images/s_33.png)
Now we can know the flipflop ratio: (number of d flip flopcells)/(number of cells)
flip flop ratio=1613/14876=0.108
