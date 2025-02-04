# Nasscom_Vsd_Soc_design
This is a 5 day workshop on **Digital vlsi design and soc planning** where we can learn how to use opensource eda tools using sky130nm technology.This course covers the complete design process from logic synthesis to layout generation.

The **PicoRV32A chip** is a compact and efficient **RISC-V** based soft-core processor, designed for FPGA and ASIC implementations. It is an extension of the PicoRV32 processor, optimized for area and power efficiency while maintaining flexibility for various applications. The RTL-to-GDS flow of the PicoRV32A chip follows a standard ASIC design methodology using **OpenLane**, an open-source EDA toolchain. The process begins with **Register Transfer Level (RTL)** design, which is synthesized into a gate-level netlist. This is followed by **floorplanning, placement, clock tree synthesis (CTS), routing, and Design Rule Check (DRC)/Layout Versus Schematic (LVS) verification** to ensure manufacturability. The final step generates the **GDSII layout**, which can be fabricated using the **SKY130 process node**, making it suitable for open-source silicon projects.
## Table of contents


---

## Sky130_Day1: Inception of Open-source EDA, OpenLane, and Sky130 PDK  
[📄 Go to full document](docs/sky130_day1.md)  

---

## Sky130_Day2: Good Floorplan vs Bad Floorplan & Introduction to Library Cells  
[📄 Go to full document](docs/sky130_day2.md)  

---

## Sky130_Day3: Design Library Cell using Magic Layout & NGSpice Characterization  
[📄 Go to full document](docs/sky130_day3.md)  

---

## Sky130_Day4: Pre-layout Timing Analysis & Importance of Good Clock Tree  
[📄 Go to full document](docs/sky130_day4.md)  

---

## Sky130_Day5: Final Steps for RTL2GDS using TritonRoute & OpenSTA  
[📄 Go to full document](docs/sky130_day5.md)  





## Acknowledgments

I would like to express my sincere gratitude to **Kunal Ghosh sir** for his invaluable guidance and mentorship throughout the development of the **Picorv32A chip**. His insights and support were instrumental in the successful completion of this project.

I also extend my appreciation to the **NASSCOM VSD SoC Design Program** for providing a structured learning environment and resources that made this project possible.

A special thanks to the **OpenLane** tool developers and the open-source community for their contributions, which played a crucial role in the design and implementation process.

Finally, I acknowledge everyone who supported and contributed directly or indirectly to this project.
