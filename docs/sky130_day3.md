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
### **Hot electron effect** 
The hot electron effect (HEE) occurs in MOSFETs when electrons gain excessive kinetic energy due to a high electric field, particularly near the drain. These high-energy electrons can cause impact ionization, generating electron-hole pairs that lead to increased substrate current. Some of these electrons may also get trapped in the gate oxide, leading to threshold voltage shifts, reduced transconductance, and long-term degradation of the transistor. This effect is more pronounced in older CMOS technologies with high drain-source voltages. To mitigate HEE, techniques such as lightly doped drain (LDD) structures, reduced supply voltages, and high-k dielectrics are used. Modern FinFETs and advanced doping techniques further help minimize the impact, making HEE less of a concern in today's low-power and scaled-down semiconductor devices. However, in high-voltage and RF applications, careful design considerations are still necessary to prevent reliability issues.
### **Short channel effect**
The short-channel effect (SCE) occurs in MOSFETs as the channel length is reduced to the submicron scale, leading to undesirable electrical behaviors. In short-channel devices, the depletion regions of the source and drain come closer, weakening the gate’s control over the channel. This results in several issues, including threshold voltage (V_th) roll-off, where V_th decreases with reduced channel length, and drain-induced barrier lowering (DIBL), where a high drain voltage reduces the potential barrier at the source, causing increased leakage currents. Additionally, SCE leads to higher subthreshold currents and degraded subthreshold slope, making the transistor less efficient in switching between ON and OFF states. To mitigate SCE, modern technologies employ techniques such as lightly doped drain (LDD) structures, halo implants, thin gate oxides, and advanced architectures like FinFETs and SOI (Silicon-on-Insulator), which improve electrostatic control and minimize leakage currents.
**images**
As a result of Plasma anisotropic etching, the Si3N4 , is removed expect at the locations, adjacent to Polysilicon material. And the Si3N4, present on the adjacent sides of the Polysilicon are known as Side-wall Spacers.
**images**
Now, a thin oxide layer is formed on the surface as shown below to avoid the channelling during implants.
**images**
Now, using mask 9 and mask 10, the Source and Drain are formed. During this process, Ion implantation process takes place with a less amount of energy of around 70 eV, and the source and drain are formed. 
**images**
Now, the process, High temperature annealing will takes place. High-temperature annealing is a process used in semiconductor fabrication to modify the properties of materials through heat treatment at elevated temperatures. Annealing involves heating a material to a specific temperature and holding it at that temperature for a certain duration, followed by controlled cooling. High-temperature annealing typically refers to annealing processes conducted at temperatures above 600°C, although exact temperatures can vary depending on the materials and desired outcomes. Generally, Ion implantation is commonly used to introduce dopants into semiconductor materials. However, this process can also introduce damage to the crystal lattice. High-temperature annealing helps to repair this damage and activate the implanted dopants, ensuring proper device functionality
**images**
 Now, the thin oxide layer formed all over the surface is etched in Hydro Flouric solution.
 **images**
 The wafer is heated at about 650 to 700 C in N2 ambient for 60 sec. And then, as a result of this heating process, TiN layer is formed all over the wafer surface. This TiN is used for the purpose of local communication. TiN possesses excellent electrical conductivity, thermal stability, and chemical inertness, making it highly suitable for interconnect applications. Secondly, TiN serves as an effective barrier layer between different metal layers and the underlying semiconductor substrate, preventing diffusion and maintaining device integrity. Its low resistivity compared to alternative barrier materials ensures efficient signal transmission and minimal voltage drop across the interconnects, contributing to enhanced device performance. The use of TiN interconnects helps reduce the resistance capacitance (RC) delay in ICs, resulting in faster signal propagation and improved overall device performance. These attributes collectively make TiN a crucial component in the development of high-performance and reliable semiconductor devices.   
 **images**
 Now, the mask 11 is used to form the below pattern which includes formation of photoresist, placing the mask, etching of photoresist 
 **images**
  Now, the mask is removed, and the TiN layer is removed/stripped/etched using RCA Cleaning technique. RCA cleaning, a vital process in semiconductor fabrication, involves a series of chemical cleaning steps aimed at removing organic and inorganic contaminants from silicon wafers. Consisting of RCA-1 and RCA-2 steps, this method effectively cleanses wafers prior to subsequent processing stages like oxidation and deposition. In RCA-1, a mixture of ammonium hydroxide (NH4OH), hydrogen peroxide (H2O2), and deionized water eliminates organic residues, while RCA-2 employs hydrochloric acid (HCl), hydrogen peroxide (H2O2), and deionized water to eradicate metallic impurities. These solutions act respectively as bases and acids, supported by oxidizing agents, to dissolve contaminants. Thorough rinsing with deionized water completes the process, ensuring a pristine substrate surface. Widely adopted in semiconductor facilities, RCA cleaning maintains silicon wafer purity, facilitating high-quality device fabrication and enhancing overall manufacturing reliability 
  **images**
   Now, the phase of higher level metal formation will starts. And now, the photoresist is etched away. Now, 1um of Silicon dioxide with phosphorous or boron which is usually known as phosphosilicate glass or borophosphosilicate glass is deposited on the wafer surface. 
**images**
The wafer surface is planerized using the Chemical mechanical polishing(CMP) technique. Chemical mechanical polishing (CMP) is a key process in semiconductor fabrication aimed at planarizing and polishing silicon wafer surfaces. This technique involves the simultaneous application of chemical and mechanical forces to remove surface irregularities and achieve high flatness and smoothness. CMP finds extensive use in semiconductor fabrication for planarizing interlayer dielectrics and metal layers, smoothing silicon wafer surfaces, removing surface damage, and achieving uniformity essential for advanced semiconductor device fabrication. 
**images**
Now, by using mask 12, the patterns as mentioned below are formed. 
Now, a layer of Aluminium is deposited on the surface to make the metal connections, with the drain source and gate regions. And after that, the photoresist is formed on the surface, and then using the mask 13, we will make the first level of interconnect of the aluminium.       
**images**
Now, again a layer of Silicon dioxide is deposited on the wafer surface and the surface is again planerized by the chemical mechanical polishing 
**images**
Now, the mask 14 is used to define the contact holes with the aluninium. After defining contact holes, a layer of TiN is deposited on the wafer surface at the region of contact holes. And, then a lyer of Tungsten is formed on the wafer surface, and CMP will takes place to make the Tungsten interconnection with the contact holes that is with Aluminium
**images**
 
Now, mask 15 is used to make the second level of interconnection. Nd after forming the interconnection, it is shown as below.                                                                    
 **images**
 Now a highly dielectric material such as Si3N4 is deposited on the wafer surface which acts as the protection barrier to the chip. And it protects the chip from external environment 
 **images**
 Now, we will use mask 16 to drill the contact holes, and to bring the contact outside of the chip 
 **images**
 We can clearly see that the upper level interconnections are must be thicker than the lower level inter connections. After the fabrication of the chip, it is sent for testing and then packaging.

Lab steps to make a CMOS inverter(Standard cell): 

 In this case we are not building the CMOS inverter form scratch, but we are using the existing design for checking furthur parameters related to building a standard cell. 

 Now, we are taking Inverter design the github from the link as mentioned below.   
  • https://github.com/nickson-jose/vsdstdcelldesign.git 
  
 To clone the gitlink, first go to the openlane directory, then run the following
 • git clone https://github.com/nickson-jose/vsdstdcelldesign.git
 
 Now, we will get a folder which contains all dependencies and requirements for the Standard cell.

  Now, go to the newly created directory in openlane directory, which contains inverter design. 
 
 Now, run the following command to view the Layot of the CMOS inverter in MAGIC 
magic -T sky130a.tech sky130_inv.mag &
**images**
  To select the whole layout, press S.
 
  To place the layout at the centre of the window, press V. 
 
  To see a particular portion in a zoom view, press S to select a particular  portion and then press Z, to zoom on that particular portion.
 
  Now, if we want to know about the particular layer in the layout, follow the below steps: 
 
• Select the particular portion or layer about which you want to know. 

• Then, in the tkcon window, run the command “what” 

• Then, you will get description about that particular layer in the tkcon window.
### **SPICE EXTRACTION:**

 for spice extraction run the following commands:
1.extract all

2.ext2spice cthresh 0 rthresh 0

3.ext2spice 

This .spice file will be created in the respected folder.
**images**
Spice deck file will be as follows:
**images**
modify the .spice file as below:
**images**
To simulate the .spice file use ngpsice. Use the command ngspice sky130_inv.spice

 **images**
 The output waveforms are as follows
 **images**
 ### **TIMING CHARCTERIZATION:**
 **images**
 **images**
### **RISE TIME:**
Time taken for a output waveform 20% to 80% of max value vdd.
2.19307ns -2.142ns =0.05107ns

similarly we can calculate fall time.

### **TRACKS. INFO:**
. A track is a virtual horizontal or vertical line on the metal layers of a chip that serves as a guide for placing and routing wires (interconnects) during physical design. Tracks are defined by their pitch, which is the distance between two adjacent tracks, and are a crucial component in standard cell placement and routing optimization
**images**
Now, we have to make use of the li1 layer dimensions to convert tracks info to grid info as follows 
 in tckon.tcl, type grid 0.46um 0.34um 0.23um 0.17um. We get the output as follows:
 **images**
###  **LAB INTRODUCTION TO MAGIC AND STEPS TO LOAD SKY130 TECH RULES:**

Now, in this session, we will some osme of the DRC rules of sky130 tech. 
 For that, first we have to install a zip file. 
 The link for zip file is  http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz
 after opening drc tests directory, we can see number of .mag files.
 **images**
 Now lets open met3.mag , it can viewed as follows:
 **images**
 **images**
 ### **LAB EXERCISE TO FIX POLY.9 ERROR:**
The "poly.9" error encountered in Magic layout typically points to an issue with the polygon layer within the layout file. In Magic, layers are often denoted by their corresponding technology layers, with "poly" usually representing the polysilicon layer used for gates and interconnections. The "9" likely refers to a specific polygon or layer number within this polysilicon layer stack 
drc errors for the above are:
 **images**
 **images**
 drc errors for the above are:
  **images**
  **images**
  ### **LAB EXERCISE TO DESCRIBE DRC ERROR AS GEOMETRICAL CONSTRUCT.**
   **images**
  **images**
 ### ** LAB CHALLANGE TO FIND MISSING OR INCORRECT RULES AND FIX THEM:
  **images**
  Here we got an error after placing an nsubstratecontact.
Now we are going to edit sky130A.tech to fix the incorrect implementation
   **images**
    **images**
      **images**
   

                                                                   
