# SKY_L1: Introduction to QFN-48 Package, Chip, Pads, Core, Die, and IP

## Understanding the Chip Inside a Microcontroller

### **1. Package**
It is the protective enclosure and interface for an ic providing electrical connections,thermal management,and mechanical support
Below is QFN-48(quad flat no leads).
 **IMAGES**
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
  **IMAGES**
 There are also some other components which we need to know:
  **IMAGES**
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
board (PCB). 
 **IMAGES**
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
**IMAGES**
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
 System software converts high level programming language like c,c++,java or python to binary level language which is understand by the hardware **IMAGES**
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
**IMAGES**
  ### **SOC:**
A System on chip(S0C) is an integrated circuit that consolidates multiple components of a complete 
system into a single chip. It typically includes Processor, memory, input/output interfaces,specialized 
modules,power management. Soc optmize power,size and performance,making them ideal for compact
and energy efficient deisgns.
 ### **SOC DESIGN FLOW:**
SOC design flow involves several stages to develop a complete system on a chip.Here’s a brief overview **IMAGES**
### **ASIC DESIGN FLOW:**
The ASIC (Application-Specific Integrated Circuit) Design Flow is the step-by-step 
process of designing and fabricating an ASIC .
They require three important key components: 
1. Register Transfer level Intellectual properties.
2. Electronic design automation tools.
3. Process design kit Data **IMAGES**
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
**IMAGES**
 ### **INTRODUCTION TO OPENLANE AND STRIVE SOC FAMILY**
 Strive is a family of open everything. For example like open pdk, open eda, open rtl**IMAGES**
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
**images**
 
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

