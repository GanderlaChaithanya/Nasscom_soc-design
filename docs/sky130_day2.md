# SKY_D2:GOOD FLOORPLANNING VS BAD FLOORPLAN AND INTRODUCTION TO LIBRARY CELLS
## CHIP FLOORPLANNING CONSIDERATIONS:
Let us know breifly about core and Die.

### **CORE:** 
The core of a chip refers to the central functional area where the primary 
computation, processing, or logic operations occur. It houses the key logic elements, 
functional blocks, or processing units that perform the chip's intended tasks. The core is 
surrounded by supporting structures like input/output (I/O) pads, power delivery 
networks, and clock distribution systems.core and die dimensions adhere to strict rules 
ensuring optimal functionality and manufacturability. These rules cover aspects like 
aspect ratio constraints, minimum dimensions, spacing rules, alignment guidelines, 
clearance requirements, power distribution, routing channels, and thermal management.
### **DIE:**
The die of a chip refers to the small, rectangular piece of silicon that contains the 
integrated circuits (ICs) and all the functional elements of the chip. It is the physical 
manifestation of the chip's design, created through intricate fabrication processes. The 
die is housed inside a package to form the complete chip.
### **UTILIZATION RATE:**
It is the ratio of the total cell area (for hard macros and standard cells or soft macro cells) to the core area.
**images**
### **ASPECT RATIO:**
aspect ratio refers to the proportional relationship between the 
height and width of a given region, such as a die, cell, or layout block. It is the ratio of 
height to the width of chip. 
If the ratio =1( it signifies that chip is in sqaure shape)

other than 1( it signifies that chip is in rectangle shape)
**images**
since, aspect ratio is 1, the given shape of chip is sqaure.
**images**
In the given above example, aspect ratio is 0.5. shape of the chip is rectangle

### **MACRO:**
A macro in VLSI design refers to a pre-designed, reusable block or module 
within a chip that performs a specific function. Macros can be large functional units, 
such as memories, processors, or custom logic, and are integrated into the larger design.
Macros are reusable and helps designers to speeds up design by eliminating the need to 
create the block from scratch.
### **IP:**
In VLSI design, IP (Intellectual Property) refers to pre-designed and reusable 
blocks or modules that implement specific functionalities within a chip. These IPs are 
developed by design teams, third-party vendors, or foundries and can be integrated into 
larger systems-on-chip (SoC) designs, saving time and effort.IPs are tested and 
validated, ensuring reliability and reducing verification effort. IPs are the backbone of 
modern VLSI design, enabling innovation, scalability, and faster development cycles in 
semiconductor technology.Ips are also called preplaced cells. The arrangement of Ips are
referred as **IP integration**
**images**
### **DIFFERENCE BETWEEN IP AND MACRO:**
Macros and IPs serve as reusable functional blocks in VLSI design, yet they differ in 
ownership, licensing, design processes, customization options, and market availability. 
Macros are internally developed and owned by the designing company, tailored to 
specific chip requirements, and not typically licensed externally. IPs, on the other hand, 
are commercially available from IP vendors, undergoing rigorous design and verification
processes, and are licensable for integration into multiple projects. While macros can be 
customized to some extent, IPs often offer more configurable options. Despite 
similarities in functionality, their distinctions lie in their origin, accessibility, and 
flexibility within the chip design ecosystem.
**images**
from above, The Ip blocks have user defined locations and placed in a chip before 
placement and routing. Hence they are referred to as preplaced cells. The location of 
preplaced cells are never touched by designers during designing. The preplaced cells are 
nothing but the ips which are built once and reused. The preplaced cells may be either of
the given example below.
**images**
### **DECOUPLING CAPACITOR:**
Decoupling capacitors stabilize the power supply 
voltage in integrated circuits (ICs) by reducing noise and voltage fluctuations caused by 
sudden changes in current demand.They are typically placed close to active devices 
(e.g., transistors, logic gates) or at key power distribution points in the circuit. They acts 
as a local energy reservoir, supplying current when demand spikes, and absorbs excess 
energy when demand decreases. It Minimizes switching noise and voltage ripples caused
by high-speed digital transitions The capacitance value is chosen based on the frequency
of operation and the magnitude of current variations. Small-value capacitors (e.g., nF 
range) respond quickly to high-frequency noise. Larger-value capacitors (e.g., μF range) 
stabilize low-frequency power variations. They are distributed across the layout to 
ensure effective noise suppression.On-chip decoupling capacitors are preferred for 
reducing parasitic inductance and resistance.Commonly used near clock trees to prevent 
noise from affecting timing signals.
### **POWER PLANNING:**
Power planning is a critical step in the physical design of 
integrated circuits (ICs) to ensure reliable delivery of power (VDD) and ground (GND) 
to all components of the chip. The goal is to minimize voltage drop (IR drop) and 
ground bounce, which can adversely affect the chip's performance and functionality.
#### **Voltage Drop (IR Drop):
- The loss of voltage along the power delivery network due to the resistance 
of interconnects.
- Excessive IR drop can result in components receiving insufficient voltage, 
leading to malfunction.
Ground Bounce:
- A phenomenon where the ground potential rises momentarily due to high 
current demands during switching.
- Causes noise, timing errors, and unreliable operation.
Strategies for Effective Power Planning
#### **1. Power and Ground Rails:**
- Distribute VDD and GND using wide metal rails to reduce resistance.
- Use multiple metal layers if necessary to handle high currents.
#### **2. Power Rings:**
- Place power and ground rings around standard cells, macros, or blocks to 
ensure even power distribution.
#### **3.Power Straps:**
- Add horizontal and vertical straps to create a grid-like power distribution 
network (PDN).
- Helps reduce the overall resistance and ensures current is evenly 
distributed.
  #### **4.Decoupling Capacitors:**
- Place decoupling capacitors close to active components to mitigate voltage 
fluctuations and ground bounce.
#### **5. Proximity to Components:**
- Place VDD and GND lines as close as possible to the components to 
minimize parasitic resistance and inductance.
**images**
### **PIN PLACEMENT:**
In VLSI design, "placement" refers to the process of determining the physical locations 
of various components, such as logic gates, flip-flops, and other circuit elements, on the 
silicon die. This placement phase occurs after the logical design phase where the 
functionality of the circuit is defined. Minimizing the total wire length is a primary 
objective during placement. Shorter interconnects lead to reduced signal delays and 
power consumption.

Congestion occurs when certain regions of the chip become densely packed, leading to 
routing difficulties and potential timing violations. Effective placement algorithms 
employ congestion-aware techniques to evenly distribute components and alleviate 
congestion hotspots.

They are two different types of placement:
- 1.global placement
- 2.detailed placement
### **GLOBAL PLACEMENT:**
Global placement, also known as coarse placement or 
floorplanning, focuses on allocating large functional blocks or macros to specific regions
of the chip. It establishes a high-level floorplan that defines the approximate placement 
of major components, such as processor cores, memory arrays, and I/O pads. Global 
placement helps set the overall chip organization and layout constraints before detailed 
placement.
### **DETAILED PLACEMENT:**
Detailed placement, also referred to as fine placement, 
involves refining the positions of individual cells or standard cells within each functional
block or macro. Detailed placement algorithms optimize the placement of cells to 
minimize wirelength, reduce congestion, and meet timing constraints. This stage of 
placement requires considering detailed routing considerations and physical design 
rules. 
### **STANDARD CELLS:**
Standard cells with different sizes play a crucial role in VLSI design by providing 
flexibility and efficiency during placement and routing in the physical design flow. 
These cells are pre-designed blocks that implement basic logic functions such as NAND,
NOR, or flip-flops, and they come in varying widths and heights based on their drive 
strength and functionality. The availability of standard cells in multiple sizes allows 
designers to select the most appropriate cell for a specific location based on 
performance, power, and area requirements.
**images**
The use of smaller cells enables compact placement in regions with limited space or 
lower performance requirements, optimizing the overall chip area. Conversely, larger 
cells, which have higher drive strengths, are used in critical paths where timing 
constraints demand faster signal transitions. This diversity in cell sizes also helps 
manage power consumption, as smaller cells consume less power and generate less heat.
Moreover, having a range of cell sizes simplifies routing by reducing congestion in 
densely packed areas. By balancing the placement of cells with varying dimensions, 
designers can achieve better utilization of the available area while maintaining signal 
integrity and meeting design constraints. Ultimately, the availability of standard cells in 
different sizes enhances the flexibility, efficiency, and performance of the overall chip 
design.
**images**
For example, consider the following netlist, with various logic elements. 

**images**
Let’s take the Standard cells from the library for the elements of above netlist. 
After the placement we need some placement optimization to make sure that the design 
is should meet the timing requirement and should not not include any timing violations. 
The design after placement is as follows
**images**
While connectng input ports to the logic cells, it require larger wire length, in which it 
may cause delay, extra prasistic resistances and capacitances occur, due to that signal 
integrity will be lost. To avoid that, we place buffers, so that signal integrity will be 
maintained, and it reduces delay.A buffer is a logic gate that receives an input signal and 
re-transmits it with minimal delay and minimal distortion.
**images**
### **LIBRARY:**
A library of standard cells is a collection of pre-designed, pre-verified 
building blocks used in digital VLSI design to implement various logic functions, such 
as gates, flip-flops, and buffers. Each standard cell in the library is characterized by its 
functional behavior, size, timing, power consumption, and drive strength. These cells are
designed to adhere to specific fabrication process rules and are optimized for a particular
technology node, such as 180nm, 65nm, or 5nm. The library provides different variants 
of each cell to accommodate varying requirements for speed, power, and area. 
The library also includes essential data, such as layout information, abstract views, and 
characterization files (e.g., .lib, .lef), which are used by electronic design automation 
(EDA) tools for synthesis, placement, and routing.

### **CELL DEISGN FLOW:**
It has three main steps:
- 1.INPUT
- 2.DESIGN STEPS
- 3.OUTPUT.
#### **INPUTS:**
We give inputs like pdks, Drc & Lvs rules, SPICE models, library and 
user_defined specs.

Cell height is defined as difference between Vdd and Vss lines.

Cell width: Drive strength decides the cell width.

### **Drive strength:**
Drive Strength refers to the ability of a circuit or a standard cell to source 
or sink current to drive a load. It is a measure of the strength of an output signal in terms
of its capability to maintain signal integrity, especially when driving capacitive or 
resistive loads such as interconnects and input pins of other gates. 
#### **DESIGN STEPS:**
- CIRCUIT DESIGN:Implement function, design nmos and pmos . It is mostly based on 
simulations.
- LAYOUT DESIGN:get a pmos network, write euler’s path, draw stick diagram, 
implement stick diagram.
- OUTPUT:
It includes GDSII, CDL(Circuit Description language), Timing, noise, power libs. 
### **CHARACTERIZATION FLOW:** 
In the process of designing a standard cell, characterization process is one of the most 
important process as it checks whether the cell is working properly or not. 
The characterization flow that is being followed by the Industry is as follows:

 1.Reading the Model files.
 
 2.Read the extracted Spice net list.
 
 3.Recognize the behaviour of the Inverter 
 
4.Read the sub circuits of the Inverter.

 5.Attach the necessary power source
 
. 6.Apply the stimulus.

 7.We have to provide necessary output capacitance. 
 
8.We have to provide necessary simulation command.

 All the characterization process is done by the characaterization software GUNA This 
software will generate Timing, noise and power models.
**images**
### **TIMING CHARCATERIZTION:**
Timing characterization is the process of determining and defining the timing parameters
of a standard cell, macro, or IP block in a VLSI design. It involves analyzing how the 
circuit behaves under various operating conditions, such as changes in input signals, 
supply voltage, temperature, and load capacitance. 
It has some parameters as shown in the given figure below
**images**
Let’s see these timing parameters one by one.
**images**
**images**
**images**
### **PROPAGATION DELAY:**
Propagation delay refers to the time it takes for a signal to 
travel from the input of a circuit element (such as a logic gate or flip-flop) to its output. 
It represents the delay between when an input signal changes state and when the 
corresponding output signal reflects that change. It is typically measured as the time 
between the 50% voltage level of the input signal's transition and the 50% voltage level 
of the output signal's transition
.The timing characterization, the selection of threshold points is very important. Here we
can see negative delay, It is not correct because negative delay is not expected. In 
practical case, we have to make sure that the delay should be positive or 0. But the delay
should not be negative. In this case, the negative delay is because of poor selection of 
threshold points.
### **Labs**
To run floorplan use the command **run_floorplan** in openlane promp
**images**
After running the floorplan we get output as follows:
**images**
Now, to have a review at the results and reports, go to the directory, floorplan inside the 
results directory as shown below. 

 Here, we can see a file with a name **picorv32a.floorplan.def** .It is the file, which 
contains all the information regarding the floorplan
**images**

Now, to can view the floorplan in the tool MAGIC
 For that, run the following command. 
 **images**
 Now, you can view your floorplan in magic as follows:
 **images**
 you can see tap cell by zooming it. Tap cells are used to avoid latch up conditions. They
are equidistant.
**images**
Now, it’s time to run placement in openlane flow.

 For this, run the command run_placement as follows 
 After running the above command, you will see as below:
 **images**
 you can view in magic layout as follows
 **images**
 


