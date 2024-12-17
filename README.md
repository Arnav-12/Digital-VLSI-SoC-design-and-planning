![Group 1](https://github.com/user-attachments/assets/0d6fd73e-3dce-4c6f-8512-2c401be07d78)

# Sky130 Day 1 - Inception of Open source EDA,OpenLane and Sky130PDK
## Introduction to QFN-48 Package,chips,pads,die, and core

The **QFN-48** (*Quad Flat No-lead, 48 pins*) package is a compact, surface-mount integrated circuit package widely used in modern electronic devices due to its low-profile design and efficient heat dissipation.

Measuring typically around **7mm x 7mm** with a height of about **0.9mm**, the QFN-48 package is designed to save space on printed circuit boards (PCBs). 

Unlike traditional leaded packages, the QFN-48 does not have leads extending from its sides, which helps to **minimize its footprint** and **improve electrical performance**.

![S1](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S1.png)

The **pads** on a QFN-48 package play a crucial role in establishing electrical connections between the chip and the PCB. These pads are located on the **bottom of the package** and are usually made of **copper**, plated with a thin layer of **tin** or **gold** to ensure reliable soldering. 

The pads are divided into:
- **Peripheral Pads**: Arranged around the perimeter for signal and power connections.
- **Thermal Pad**: A larger pad located in the center, primarily used for **heat dissipation** and often serving as an **electrical ground**.

This design helps manage heat more effectively, which is critical for maintaining the **performance** and **longevity** of the chip.

![S2](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S2.png)

At the **heart of the QFN-48 package** lies the **core**, the central part of the semiconductor die where the main circuitry is located. The core contains **active and passive components**, including transistors, resistors, capacitors, and interconnects, which collectively perform the chip's intended functions. The **core's design** is crucial for the chip's performance, as it dictates how efficiently the chip processes signals and performs computations.

The **die**, a small piece of silicon wafer, contains the integrated circuit and is the fundamental building block of the chip. The die is fabricated through processes like **photolithography** and **etching** to create the intricate circuits necessary for the chip's functionality. Once the die is completed, it is mounted onto the **lead frame** or **substrate** within the QFN-48 package. Connections between the die and the pads are made using **bond wires** or advanced methods like **flip-chip bonding**, ensuring reliable electrical pathways for signal transmission.

**Intellectual Properties (IPs)** are essential components of modern chip design, providing **pre-designed** and **pre-verified** blocks of logic or functions that can be integrated into the chip. IPs come in various forms:
- **Hard IPs**: Fixed layouts integrated directly into the silicon.
- **Soft IPs**: Synthesizable RTL (Register Transfer Level) code that can be customized.

Examples of IPs include:
- Processors
- Memory controllers
- Interfaces like **USB** and **Ethernet**
- Analog components like **ADCs** (Analog-to-Digital Converters) and **DACs** (Digital-to-Analog Converters)
- Various other functional blocks

By incorporating **IPs**, designers can **speed up development**, **reduce costs**, and ensure the **reliability** of the chip by reusing proven components.


## Introduction to RISC-V

**RISC-V** (*Reduced Instruction Set Computing, Version 5*) is an **open, free, and extensible instruction set architecture (ISA)** that is rapidly gaining popularity in the field of computer architecture. Developed at the **University of California, Berkeley**, RISC-V aims to provide a **standardized** and **streamlined ISA** that can be used for a wide range of applications, from **small embedded systems** to **large-scale data centers**.

Its **open nature** means that anyone can **use**, **modify**, and **extend** the ISA without licensing fees, fostering **innovation** and **collaboration** across the industry.

![S3](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S3.png)

## From Software Application to Hardware
The **below diagrams** show how **application software**, **system software**, and **hardware** interact.

![S4](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S4.png)

## Digital ASIC Design

The journey from **Electronic Design Automation (EDA)** tools to an **Application-Specific Integrated Circuit (ASIC)** involves several key stages:
- **EDA tools**, such as **schematic capture software**, are used to create detailed circuit diagrams.
- **Simulation tools**, like **SPICE** for analog designs and **ModelSim** for digital designs, verify the functionality of these circuits.
- **Synthesis tools**, such as **Synopsys Design Compiler**, convert high-level **RTL (Register Transfer Level)** code into a gate-level netlist.
- Finally, **Place and Route (P&R)** tools, like **Cadence Innovus** or **Synopsys IC Compiler**, are used to physically layout the circuit on the chip, ensuring **optimal performance** and **area efficiency**.

![S5](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S5.png)

## Simplified RTL2GDS flow

The **RTL2GDS** flow, transforming a high-level **Register Transfer Level (RTL)** design into a final **GDSII** (*Graphic Data System II*) format, is streamlined through several stages:

1. **Synthesis**: RTL code written in hardware description languages like **Verilog** or **VHDL** is synthesized into a **gate-level netlist** using synthesis tools.
2. **Design-for-Test (DFT)**: Enhancements are applied to facilitate post-production testing.
3. **Place and Route (P&R)**: Tools like **Cadence Innovus** or **Synopsys IC Compiler** arrange the netlist components and route interconnections on the silicon.
4. **Timing Analysis and Optimization**: Includes **timing analysis**, **signal integrity checks**, and **power optimization** to ensure the design meets all performance criteria.
5. **Layout Verification**: The completed layout is verified against the original design specifications.
6. **Export to GDSII**: The final design is exported in the **GDSII format**, ready for fabrication.
   
![S6](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S6.png)

## Strive Chipsets

![S7](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S7.png)

## OpenLANE Design Flow

## Learn More About OpenLane

The following YouTube video is useful for understanding OpenLane and its working:

[Watch the video on YouTube](https://www.youtube.com/live/Vhyv0eq_mLU?si=xflMkyOfawGhRuRM)

![S8](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S8.png)

# Day-1 Labs
## Basic Linux Commands

### 1. `cd` (Change Directory)  
Navigates between directories.

- **Example:**  
  ```bash
  cd Documents
  ```

### 2. `ls` (List Files)  
Lists files in a directory.

- **Example:**  
  ```bash
  ls -ltr
  ```

### 3. `pwd` (Print Working Directory)  
Shows the current directory path.

- **Example:**  
  ```bash
  pwd
  ```

### 4. `mkdir` (Make Directory)  
Creates a new directory.

- **Example:**  
  ```bash
  mkdir new_folder
  ```

### 5. `rm` (Remove Files)  
Deletes files or directories.

- **Example:**  
  ```bash
  rm file.txt
  ```
## Working Directory for the Lab

The working directory for this lab is:

```
/Desktop/work/tools/openlane_working_dir/openlane
```
This is where all the files and tools related to the lab will be located.

To start OpenLane, run the following command in your terminal:

```
bash-4.2$ ./flow.tcl -interactive
```
![s1](https://github.com/user-attachments/assets/29398ddc-9ee8-4061-b0ef-3be9fbc132fc)

### `config.tcl` File

The `config.tcl` file contains configuration settings for the OpenLane flow, including tool options and design parameters. It customizes the flow's behavior to match the specific requirements of your design.

![s2](https://github.com/user-attachments/assets/723517d7-ef56-472f-beed-413c45e37e91)

## Merged LEF File

The merged LEF file can be accessed from the following directory:

```
/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/14-12_06-43/tmp
```

![s3](https://github.com/user-attachments/assets/83181aa4-8db7-4544-af69-1a4f086ed8a8)
![s4](https://github.com/user-attachments/assets/882a633c-86c5-4698-b3e2-7284457b7ba5)
![s5](https://github.com/user-attachments/assets/059fd3ae-9be4-43ff-8053-e37c1a8c9d3a)

## Objective

The first objective of this workshop is to **calculate the flop ratio**.

## **Flop Ratio**

The **Flop Ratio** is an important metric in digital design that represents the ratio of **flip-flops** (memory elements) to the total number of **logic gates** in a circuit.

- A **higher flop ratio** indicates a design with **more memory storage**, which is typically used for sequential processing or state retention.
- A **lower flop ratio** suggests a design focused more on **logic operations**, aiming for faster, combinational logic.

Optimizing the **Flop Ratio** is crucial for balancing **area**, **power**, and **performance** in digital circuits, leading to more efficient designs.

![s7](https://github.com/user-attachments/assets/50570253-b051-4781-b1e3-69b867c7e0a0)

## Final Synthesis Report

- The number of **D flip-flops** is `1613`.
- The total number of **cells** is `14876`.
- The **flop ratio** is `0.1084`.
- In percentage, the **flop ratio** is `10.84%`.

```plaintext
# Calculation of Flop Ratio
Number of D Flip-Flops = 1613
Total Number of Cells = 14876
Flop Ratio = 1613 / 14876 = 0.1084
Flop Ratio in Percentage = 0.1084 * 100 = 10.84%
```
![s8](https://github.com/user-attachments/assets/d0776651-99b8-43d6-9f6c-5da04629b0e1)

# Sky130 Day 2 - Good floorplan vs bad floorplan and introduction to library cells

### What is a Floorplan?

A **floorplan** in digital design refers to the layout of a chip, including the placement of its functional blocks, such as logic gates, memory, and I/O components. It defines how these blocks are arranged in the chip's physical space to optimize performance, power, and area.

### Good vs Bad Floorplan

- **Good Floorplan**: A well-optimized floorplan minimizes wirelength, reduces power consumption, and improves signal integrity, leading to faster and more reliable designs.
- **Bad Floorplan**: A poorly designed floorplan can cause congestion, longer wirelength, higher power usage, and slower performance due to inefficient placement of components.

### Significance

A good floorplan is crucial for ensuring that the chip functions efficiently, fits within design constraints, and meets performance goals. It plays a vital role in the success of the chip during fabrication and operation.

![t1](https://github.com/user-attachments/assets/6112cd6c-dd39-4239-a832-15e4b9d309d5)

### Chip Floorplanning Considerations

When designing a chip, several key factors need to be considered to ensure an optimal floorplan:

- **Utilization Factor and Aspect Ratio**: These determine the efficiency of space usage and the overall shape of the chip, balancing the design between area and performance.
  
- **Location of Pre-placed Cells**: Ensuring that critical cells (e.g., I/O cells, macros) are strategically placed to minimize routing congestion and optimize performance.
  
- **Decoupling Capacitors**: Proper placement of decoupling capacitors is essential for stabilizing power supply and reducing noise in the design.
  
- **Power Planning**: Planning the power grid to ensure efficient power delivery and avoid issues like voltage drops or excessive power consumption.
  
- **Pin Placement**: Optimizing the location of input/output pins to minimize signal delay and improve overall design efficiency.

Each of these considerations plays a vital role in achieving a balanced and efficient chip design.

![t2](https://github.com/user-attachments/assets/73c4e253-0919-4e86-8a83-ebce3b6f108b)

### Accessing Floorplan Output  

After successfully running the `run_floorplan` command, the **floorplan output file** `picorv32a.floorplan.def` can be found in the following directory:  

```
/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/14-12_06-43/results/floorplan
```
### Floorplan Dimensions and Die Area Calculation  

The floorplan's dimensions and area are calculated as follows:

1. **Unit Distance to Micron Conversion**:  
   - `1000 Unit Distance = 1 Micron`  

2. **Die Width and Height in Unit Distance**:  
   - **Die Width**: `660685 - 0 = 660685` (unit distance)  
   - **Die Height**: `671405 - 0 = 671405` (unit distance)  

3. **Conversion to Microns**  

- **Formula**:  
   ```math
   \text{Distance in Microns} = \frac{\text{Value in Unit Distance}}{1000}
   ```

- **Die Width**:  
   ```math
   \text{Die Width} = \frac{660685}{1000} = 660.685 \, \text{Microns}
   ```

- **Die Height**:  
   ```math
   \text{Die Height} = \frac{671405}{1000} = 671.405 \, \text{Microns}
   ```
4. **Die Area Calculation**  

- **Formula**:  
   ```math
   \text{Area} = \text{Width} \times \text{Height}
   ```

- **Substituting Values**:  
   ```math
   \text{Area} = 660.685 \times 671.405 = 443587.212425 \, \text{Square Microns}
   ```

![s9](https://github.com/user-attachments/assets/04af9ac6-9e9a-42c0-8401-6104283b81ec)

### Opening Floorplan in Magic

To open the floorplan using **Magic**, use the following command:

```bash
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech \
    lef read ../../tmp/merged.lef \
    def read picorv32a.floorplan.def &
```
This command loads the **merged LEF** and the **floorplan DEF** files into the Magic layout editor for visualization.

![s10](https://github.com/user-attachments/assets/4ad7a631-4559-41f2-bd7b-9b0a49ec77bb)
![s11](https://github.com/user-attachments/assets/ded786fd-632a-43c7-8f45-b011cb5385d0)
![s12](https://github.com/user-attachments/assets/cde2d041-0c35-4cef-a282-a7f8b2cc144c)
![s13](https://github.com/user-attachments/assets/a8d60f7b-265d-4f20-8efa-6e88b3f3bc30)

## **Placement and Routing**

### **1. Placement**  
Placement is the process of determining the exact locations of standard cells and macro blocks on the chip layout. The goal is to optimize **timing, power consumption**, and **area utilization**.  
- **Good Placement** minimizes wirelength and reduces routing congestion.  
- **Bad Placement** can cause timing delays, congestion, and higher power usage.

### **2. Routing**  
Routing connects the placed components (cells and blocks) using interconnect wires to ensure proper signal flow. It involves two main steps:  
- **Global Routing**: Determines approximate paths for signals.  
- **Detailed Routing**: Finalizes exact wire paths while avoiding design rule violations (e.g., overlaps).  

### **Significance**  
Effective **Placement and Routing** is crucial for:  
- **Minimizing wirelength** and congestion.  
- Achieving **timing closure** to meet design constraints.  
- Reducing **power consumption** and improving overall chip performance.

![s14](https://github.com/user-attachments/assets/d2613a8e-e603-45ac-9f19-8e517c109573)

# Sky130 Day 3 - Design library cell using Magic layout and ngspice characterization

### **Magic**  
**Magic** is an open-source VLSI layout editor used for designing and viewing chip layouts. It supports tasks such as creating, editing, and verifying physical layouts, and integrates well with tools like OpenLane for physical design workflows.

### **Ngspice**  
**Ngspice** is an open-source circuit simulator used for SPICE-based simulation of analog and mixed-signal circuits. It helps analyze circuit behavior, such as voltage, current, and timing characteristics, to ensure design accuracy.

![s15](https://github.com/user-attachments/assets/d27d1498-79f5-46f8-ad0b-0e889b41675b)

The Pins in the below layout are equidistant

![s16(d3_lec1_1)](https://github.com/user-attachments/assets/b88a8595-e822-4e4e-bf84-cb8e248dc822)

### **Setting FP_IO_MODE and Running Floorplan**

To modify the **Input/Output (I/O) mode** for floorplanning, use the following command:

```tcl
set ::env(FP_IO_MODE) 2
```

- Here, `FP_IO_MODE` is an environment variable that defines the I/O pin placement mode during floorplanning.  
   - `2` enables **automatic I/O pin placement**.  

After setting the variable, run the floorplan step with:

```tcl
run_floorplan
```

![s17(equidistant before setting variable)](https://github.com/user-attachments/assets/6f6fd5e3-b27b-477e-be4a-56a00250f278)

Now cells are stacked over each other

![s18(cells are stacked over each other)](https://github.com/user-attachments/assets/c0384d5a-8ebd-4515-9959-4d3bb731c06f)

### **Next Step: Clone the Required Repository**  

To proceed, clone the following repository using the command:

```bash
git clone https://github.com/nickson-jose/vsdstdcelldesign.git
```

### **About the Repository**  
This repository contains all the necessary information to **build and run the OpenLane flow**, which performs a full ASIC implementation from **RTL to GDSII**.  

In addition, it includes:  
- Procedures to create a **custom LEF file**.  
- Steps to integrate the custom LEF file into the **OpenLane flow**.

### **Opening Magic with sky130A.tech**

To view the contents of `sky130A.tech` using Magic, use the following command:

```bash
magic -T sky130A.tech sky130_inv.mag &
```

![s19](https://github.com/user-attachments/assets/ee7317ce-8f3b-4782-902c-79216bcaae02)

### **16-Mask CMOS Process Steps**

1. **Selecting a Substrate**  
   Choose the substrate material (usually silicon) on which the entire process will be built.

2. **Creating Active Regions for Transistors**  
   Define the active regions where the transistors will be fabricated on the silicon substrate.

3. **N-Well and P-Well Formation**  
   Create the **N-Well** and **P-Well** regions, which form the foundation for the complementary transistors (NMOS and PMOS).

4. **Formation of Gate**  
   Deposit and pattern the **gate material** (usually polysilicon) to define the channel of the transistor.

5. **Lightly Doped Drain (LDD) Formation**  
   Perform a light doping process to create lightly doped regions in the source and drain areas to reduce short-channel effects.

6. **Source-Drain Formation**  
   Implant high concentrations of dopants to form the **source** and **drain** regions of the transistor.

7. **Steps to Form Contact and Interconnects (Local)**  
   Create **contacts** to the source, drain, and gate, followed by local interconnects to connect the transistors to each other and to the rest of the chip.

8. **High-Level Metal Formation**  
   Deposit and pattern higher metal layers (Metal 1, Metal 2, etc.) to connect different parts of the chip, completing the routing of signals and power.

### **Creating a SPICE File for Ngspice**

To generate a SPICE file that can be used with **Ngspice**, follow these steps in the **Tkcon** window:

1. **Extract all netlist information**:
   ```tcl
   extract all
   ```

2. **Generate SPICE netlist with specified thresholds**:
   ```tcl
   ext2spice cthresh 0 rthresh 0
   ```

3. **Export the SPICE netlist**:
   ```tcl
   ext2spice
   ```
![s20](https://github.com/user-attachments/assets/d3f0ef44-ff43-4bd4-b063-1b57d03cf7d1)

### **Updating SPICE File with pshort.lib and nshort.lib**

 **Modify the SPICE file** to include the required libraries. Add the following lines at the top of your SPICE file:

   ```spice
   .include ./libs/pshort.lib
   .include ./libs/nshort.lib
   ```

![s21](https://github.com/user-attachments/assets/5219cacb-d97a-4ebb-93a3-0ff0778706a9)

### **Opening Ngspice for Simulation**

To run the simulation using **Ngspice**, use the following command:

```bash
ngspice sky130_inv.spice
```

- This command will launch **Ngspice** and load the **sky130_inv.spice** netlist file for simulation.

![s22](https://github.com/user-attachments/assets/d571d16c-1a06-40fe-a793-f8c9318c8016)
![s23(rise time)](https://github.com/user-attachments/assets/3bbf8810-881a-448b-80cc-bd314d601262)
![s24(cell rise delay)](https://github.com/user-attachments/assets/8655e6db-d217-4c4a-a90b-44e4e72c9e27)
![s25(prop delay)](https://github.com/user-attachments/assets/c0309ff5-3b99-4a8e-add5-11c2f5475398)
![s26(magicrc file)](https://github.com/user-attachments/assets/99a39c08-f978-4271-8df5-33a16d6287df)
![s27](https://github.com/user-attachments/assets/a53058b3-444b-4395-86d1-e7b4488af608)
![s28](https://github.com/user-attachments/assets/f65addec-e6ba-4a8a-8968-07600cc168f1)
![s30](https://github.com/user-attachments/assets/75b9ae3f-884a-4925-b095-89ae41a1af8b)
![s31](https://github.com/user-attachments/assets/a30934d7-9be6-4fb7-8937-87d0ace28087)
![s32](https://github.com/user-attachments/assets/af16fac8-cd6b-4d14-ad75-7dbc8ea6bb92)
![s33](https://github.com/user-attachments/assets/9e7eda47-3cc0-4d4f-aff9-0af54553f7f4)
