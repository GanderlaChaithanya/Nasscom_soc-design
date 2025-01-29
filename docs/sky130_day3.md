# SKY130_DAY3: DESIGN LIBRARY CELL USING MAGIC LAYOUT AND NGSPICE CHARACTERIZATION
### **SPICE DECK CREATION FOR CMOS INVERTER:**
SPICE deck refers to a text file written in SPICE (Simulation Program with Integrated Circuit Emphasis) syntax that describes the electrical behaviour of an integrated circuit (IC) component or a circuit net list A spice deck creation needs some information about the Component connectivity, it’s values and values for the nodes and it’s name.
**images**
There is a specific syntax for the Spice deck creation.

 The syntax for connectivity information for MOSFET is MOSFET name (like M1 or M2), DRAIN, GATE, Source, Substrate, type of MOSFET (PMOS or NMOS), width, length. 
 
Let’s see the connectivity information of PMOS and NMOS separately
**images**
**images**
we will sweep the voltage at the input from 0 -2.5V with the step size of 0.05. Final step is describe the model file. Below description says the complete description for PMOS & NMOS means all technological parameters.
**images**
### **Spice simulation for CMOS Inverter:**
The Spice simulations are processed in ngspice. “ngspice” is an open-source electronic circuit simulator based on the SPICE (Simulation Program with Integrated Circuit Emphasis) simulation engine. It stands for "Next Generation SPICE." ngspice is widely used in VLSI (Very Large Scale Integration) design for simulating and verifying the behaviour of electronic circuits at the transistor level. The steps to follow for SPICE simulation 

 Go to ngspice. 

 Change the directory (where the related files kept). 

 Source the circuit file. it says the now the circuit is present in the ngspice simulator.

 To execute the circuit, the command is run.

  Give command setplot --> it will show which plots are currently available in the simulator.
 
  Select the plot. Give command name as that plot name. 

  Give display command to see which nodes are available.
 
  To plot the graph give command plot out vs in. 
 
  We can see the plot for above inputs. In this the width of both PMOS & NMOS is same.  
 **images**
 If we keep the width of PMOS is 2.5 times of NMOS, The whole procedure will be same, only the width of PMOS will vary                                                                                         
### **SWITCHING THRESHOLD Vm:**
The switching threshold, also known as the switching threshold voltage or simply threshold voltage, is a critical parameter. Switching threshold it is the point where the Vin = Vout. and also both PMOS & NMOS are in saturation region. In saturation region, they will be turned on and becaouse of this there is high chance of leakage. In this case there is high possibility that the current will flow directly from VDD to GND. In remaining areas one of the device turned off.so that there will not be direct path. Because of this conditions CMOS is a kind of short circuit device. 

CMOS is a robust device. Based on the W/L ratio, the properties of CMOS will vary. Because of this ratio only, the following two graphs are varying in their position but not in their shapes.
**images**
CMOS Inverter’s robustness is essential for ensuring reliable performance across various operating conditions. One key aspect contributing to the robustness of CMOS inverters is their high noise immunity. By utilizing both NMOS and PMOS transistors in complementary pairs, CMOS inverters can effectively mitigate the impact of noise on the output signal, ensuring accurate signal processing in noisy environments.
**images**
**images**

As shown above, the delay is calculated for rise delay.

And similarly to check for fall delay, we have to check t the 50% of the fall edge of the output. 

# Introduction to Fabrication
Fabrication in VLSI (Very Large Scale Integration) refers to the process of manufacturing integrated circuits (ICs) on a semiconductor substrate, typically made of silicon. This process involves a series of intricate steps to create the complex structures and circuitry that constitute modern electronic devices. The goal of VLSI fabrication is to create integrated circuits with high precision, reliability, and performance while maximizing yield and minimizing costs. This process is performed in specialized facilities called semiconductor fabs, which are equipped with advanced tools and clean room environments to ensure the highest level of quality control and precision. 
Let us know about 16-mask cmos fabrication:
**images**
### **16-MASK CMOS FABRICATION:**
The 16-mask CMOS fabrication process is a widely used method for manufacturing complementary metal-oxide-semiconductor (CMOS) integrated circuits. This process involves the use of 16 photolithographic masks to define various layers and structures of the chip. It starts with a silicon wafer, typically doped with impurities to create p-type or n-type regions. The process sequentially applies layers of oxide, polysilicon, metal, and other materials, each patterned using photolithography. Key steps include the creation of wells for pMOS and nMOS transistors, gate oxide growth, source and drain doping through ion implantation, and the deposition of interconnect layers for wiring. Each mask corresponds to a specific stage, such as defining active areas, polysilicon gates, contacts, and metal interconnects. The use of 16 masks ensures precise control over the layout and dimensions of the transistors and interconnections, enabling high-density and high-performance circuit designs. This process strikes a balance between complexity, cost, and functionality, making it a standard in CMOS technology for a range of applications. 
**images**
Now on the substrate, a layer of SiO2(of thickness 40nm) is formed and on this layer, 80nm of Si3N4 layer is formed. And now, the process of Photolithography is started. And as a part of Photolithography, A layer of photoresist is formed above these layers.
**images**
Now the mask1 come into action, and for creating active region for the transistors, mask 1 is placed above the photoresist layer. These masks are used to create patterns on the layer according to the layout. Now a beam of UV light is focused on the mask 
**images**
Now, the photoresist which is not covered with the mask 1 is removed due to UV light
**images**
Now the mask 1 is removed and the Si3N4 is removed through a chemical process. But the Si3N4 under the photoresist is etched away through the process of etching. 
**images**
Now the photoresist is removed by the process of chemical stripping. Chemical stripping involves immersing the wafer in a solution that dissolves the photoresist material. Commonly used chemicals for this purpose include sulfuric acid, hydrogen peroxide, and deionized water mixtures (known as piranha solution) or organic solvents like acetone, methyl ethyl ketone (MEK), or N-methyl-2-pyrrolidone (NMP). The choice of chemical depends on factors such as the type of phototreisst used and the compatibility with the underlying materials on the wafer.
**images**
Now, the above setup is placed inside an oxidation furnace. And as a result of this process, field oxide is grown, and this process is called LOCOS or Local Oxidation of Silicon. The oxide is grown at the regions where it is not covered by Si3N4 layer, and it forms a structure known as Bird’s Beak.
**images**
Now, the Si3N4 is removed or stripped by the hot phosphoric acid and again a layer of phottoresist is formed on the oxide.
**images**
With this, the phase for the formation of n-well and p-well regions is started. And now, the mask – 2 is placed on the photoresist, as shown below to create the wells. And again the UV beam is made to fall on the mask and photoresist.
**images**
Now, the photoresist which is not covered with mask is removed. And now, the process of forming the wells is started. And Boron ions are implanted on the substrate through the process of Ion Implantation with an energy of 200eV for the boron ions to penetrate into the substrate crossing the Silicon oxide layer. Now, the p-well is formed 
**images**
Now, the photoresist is stripped away. And agian a phototresist layer is formed on the oxide layer, and the mask 3 is placed on the photoresist. And again, same process is followed, that is the UV beam id made to fall on the phototresist, and the photoresist is removed 
**images**
Similarly, phosphorus ions are implanted into the substrate with a high energy through the process of Ion Implantation.And as a result of this process, n-well is created. Now, the setup is placed in a high temperature furnace. 
**images**
Due to the high temperature, the n-well and p-well regions are expanded and penetrated deep into the substrate.  
**images**
For the gate formation, the threshold voltage and oxide capacitance is considered as per the properties mentiones below: 
**images**
Now for the formation of gate, again the photoresist is formed on the oxide layer.and then mask-4 is placed on phototresist and again the photoresist not covered with mask 4 is removed by the UV light. 
**images**
Now, Boron ions are implanted into the substrate but with some little energy, so that they will form nearer to the silicon oxide. Now, the p region is created. Similarly, the n region is also created with phosphorus or Arsenic. After that the mask and photoresist are stripped, and the oxide ayer is stripped using Hydro flouric solution, and again a new layer of oxide is formed to maintain the oxide quality.     
**images**
Now, polysilicon layer of thickness 0.4um is formed on the oxide layer for the formation of gate. And then, n-type ions are implanted on the polysilicon layer to maintain the low gate resistance. 
**images**
Now, again the photoresist is formed on the polysilicon layer and mask 6 is placed on the photoresist. And the photoresist which is not covered with the mask, is etched away. And, then we get as shown below. 
**images**
Now, the mask is removed and then the polysislicon is exposed to a plasma containing reactive gases, typically fluorine-based, within a vacuum chamber. These gases react with the polysilicon, forming volatile byproducts that are removed from the surface, effectively etching the polysilicon layer 
**images**
Now, the photoresist is removed chemically. 
**images**




                                                                    


                                                                   
