# Digital-VLSI-SoC-design-and-planning
# Sky130 Day-1
## Introduction to QFN-48 Package,chips,pads,die, and core

The QFN-48 (Quad Flat No-lead, 48 pins) package is a compact, surface-mount integrated circuit package widely used in modern electronic devices due to its low-profile design and efficient heat dissipation. Measuring typically around 7mm x 7mm with a height of about 0.9mm, the QFN-48 package is designed to save space on printed circuit boards (PCBs). Unlike traditional leaded packages, the QFN-48 does not have leads extending from its sides, which helps to minimize its footprint and improve electrical performance.

![S1](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S1.png)

The pads on a QFN-48 package play a crucial role in establishing electrical connections between the chip and the PCB. These pads are located on the bottom of the package and are usually made of copper, plated with a thin layer of tin or gold to ensure reliable soldering. The pads are divided into peripheral pads, which are arranged around the perimeter for signal and power connections, and a larger thermal pad in the center. The thermal pad is primarily used for heat dissipation and often also serves as an electrical ground. This design helps manage heat more effectively, which is critical for maintaining the performance and longevity of the chip.

![S2](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S2.png)
At the heart of the QFN-48 package lies the core, the central part of the semiconductor die where the main circuitry is located. The core contains active and passive components, including transistors, resistors, capacitors, and interconnects, which collectively perform the chip's intended functions. The core's design is crucial for the chip's performance, as it dictates how efficiently the chip processes signals and performs computations.

The die, a small piece of silicon wafer, contains the integrated circuit and is the fundamental building block of the chip. The die is fabricated through processes like photolithography and etching to create the intricate circuits necessary for the chip's functionality. Once the die is completed, it is mounted onto the lead frame or substrate within the QFN-48 package. Connections between the die and the pads are made using bond wires or advanced methods like flip-chip bonding, ensuring reliable electrical pathways for signal transmission.

Intellectual Properties (IPs) are essential components of modern chip design, providing pre-designed and pre-verified blocks of logic or functions that can be integrated into the chip. IPs come in various forms, such as hard IPs, which are fixed layouts integrated directly into the silicon, and soft IPs, which are synthesizable RTL (Register Transfer Level) code that can be customized. Examples of IPs include processors, memory controllers, interfaces like USB and Ethernet, analog components like ADCs and DACs, and various other functional blocks. By incorporating IPs, designers can speed up the development process, reduce costs, and ensure the reliability of the chip by reusing proven components.

## Introduction to RISC-V

RISC-V (Reduced Instruction Set Computing, Version 5) is an open, free, and extensible instruction set architecture (ISA) that is rapidly gaining popularity in the field of computer architecture. Developed at the University of California, Berkeley, RISC-V aims to provide a standardized and streamlined ISA that can be used for a wide range of applications, from small embedded systems to large-scale data centers. Its open nature means that anyone can use, modify, and extend the ISA without licensing fees, fostering innovation and collaboration across the industry.
![S3](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S3.png)

## From Software Application to Hardware
Here we get to know ,how software and hardware interacts
![S4](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S4.png)

## Digital ASIC Design

The journey from Electronic Design Automation (EDA) tools to an Application-Specific Integrated Circuit (ASIC) involves several key stages. EDA tools, such as schematic capture software, are used to create detailed circuit diagrams, while simulation tools like SPICE for analog and ModelSim for digital designs verify the functionality of these circuits. Synthesis tools, such as Synopsys Design Compiler, then convert high-level RTL (Register Transfer Level) code into a gate-level netlist. Following this, Place and Route (P&R) tools, like Cadence Innovus or Synopsys IC Compiler, are used to physically layout the circuit on the chip, ensuring optimal performance and area efficiency.

![S5](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S5.png)

## Simplified RTL2GDS flow

The RTL2GDS flow, transforming a high-level Register Transfer Level (RTL) design into a final GDSII (Graphic Data System II) format, is streamlined through several stages. Initially, RTL code written in hardware description languages like Verilog or VHDL is synthesized into a gate-level netlist using synthesis tools. This netlist, representing the logical structure of the circuit, undergoes Design-for-Test (DFT) enhancements to facilitate post-production testing. The design is then processed through Place and Route (P&R) tools, arranging the netlist components and routing interconnections on the silicon. Subsequent stages involve timing analysis, signal integrity checks, and power optimization to ensure the design meets all performance criteria. Finally, the completed layout is verified against the original design specifications before being exported in the GDSII format, ready for fabrication.

![S6](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S6.png)

## Strive Chipsets
![S7](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S7.png)

## OpenLANE Design Flow
![S8](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S8.png)

# Day-1 Labs
![s1](https://github.com/user-attachments/assets/29398ddc-9ee8-4061-b0ef-3be9fbc132fc)
![s2](https://github.com/user-attachments/assets/723517d7-ef56-472f-beed-413c45e37e91)
![s3](https://github.com/user-attachments/assets/83181aa4-8db7-4544-af69-1a4f086ed8a8)
![s4](https://github.com/user-attachments/assets/882a633c-86c5-4698-b3e2-7284457b7ba5)
![s5](https://github.com/user-attachments/assets/059fd3ae-9be4-43ff-8053-e37c1a8c9d3a)
![s6](https://github.com/user-attachments/assets/27ccee7c-4b5e-47ad-a5d8-440e88888dee)
![s7](https://github.com/user-attachments/assets/50570253-b051-4781-b1e3-69b867c7e0a0)
![s8](https://github.com/user-attachments/assets/d0776651-99b8-43d6-9f6c-5da04629b0e1)

# Day-2 Labs
![s9](https://github.com/user-attachments/assets/04af9ac6-9e9a-42c0-8401-6104283b81ec)
![s10](https://github.com/user-attachments/assets/4ad7a631-4559-41f2-bd7b-9b0a49ec77bb)
![s11](https://github.com/user-attachments/assets/ded786fd-632a-43c7-8f45-b011cb5385d0)
![s12](https://github.com/user-attachments/assets/cde2d041-0c35-4cef-a282-a7f8b2cc144c)
![s13](https://github.com/user-attachments/assets/a8d60f7b-265d-4f20-8efa-6e88b3f3bc30)
![s14](https://github.com/user-attachments/assets/d2613a8e-e603-45ac-9f19-8e517c109573)

# Day-3 Labs
![s15](https://github.com/user-attachments/assets/d27d1498-79f5-46f8-ad0b-0e889b41675b)
![s16(d3_lec1_1)](https://github.com/user-attachments/assets/b88a8595-e822-4e4e-bf84-cb8e248dc822)
![s17(equidistant before setting variable)](https://github.com/user-attachments/assets/6f6fd5e3-b27b-477e-be4a-56a00250f278)
![s18(cells are stacked over each other)](https://github.com/user-attachments/assets/c0384d5a-8ebd-4515-9959-4d3bb731c06f)
![s19](https://github.com/user-attachments/assets/ee7317ce-8f3b-4782-902c-79216bcaae02)
![s20](https://github.com/user-attachments/assets/d3f0ef44-ff43-4bd4-b063-1b57d03cf7d1)
