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

## **Parameters to Characterize Using Sky130 Model Files**

### **Rise Time**

**Rise Time** is the amount of time it takes for a signal to transition from a low voltage level to a high voltage level, typically defined between 10% and 90% of the maximum value of the waveform.

- **Formula**:  
   ```math
   \text{Rise Time} = x_0 - x_1
   ```

   The **Rise Time** is calculated as:  
   ```math
   \text{Rise Time} = 2.2396 \, \text{ns} - 2.1799 \, \text{ns} = 0.0597 \, \text{ns}
   ```
![s23(rise time)](https://github.com/user-attachments/assets/3bbf8810-881a-448b-80cc-bd314d601262)

### **Cell Rise Delay**

**Cell Rise Delay** refers to the time it takes for a signal to transition from a low logic level (typically 0) to a high logic level (typically 1) at the output of a logic gate or cell. This delay is often measured at the output node when the input transitions from low to high.

- **Formula**:  
   ```math
   \text{Cell Rise Delay} = t_{\text{high}} - t_{\text{low}}
   ```

   The **Cell Rise Delay** is calculated as:  
   ```math
   \text{Cell Rise Delay} = 2.20647 \, \text{ns} - 2.14941 \, \text{ns} = 0.05706 \, \text{ns}
   ```
![s24(cell rise delay)](https://github.com/user-attachments/assets/8655e6db-d217-4c4a-a90b-44e4e72c9e27)

### **Propagation Delay**

**Propagation Delay** is the time taken for a signal to propagate through a logic gate or cell, from the moment the input changes to the moment the output changes. It is typically measured between 50% of the input signal and 50% of the output signal.

- **Formula**:  
   ```math
   \text{Propagation Delay} = t_{\text{output}} - t_{\text{input}}
   ```

   The **Propagation Delay** is calculated as:  
   ```math
   \text{Propagation Delay} = 6.20766 \, \text{ns} - 6.15 \, \text{ns} = 0.05766 \, \text{ns}
   ```

![s25(prop delay)](https://github.com/user-attachments/assets/c0309ff5-3b99-4a8e-add5-11c2f5475398)

### **Downloading Lab Files**

To download the lab files, use the following command:

```bash
wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz
```

### **Opening Magic Tool with Better Graphics**

To launch the **Magic tool** with improved graphics, use the following command:

```bash
magic -d XR &
```

- The `-d XR` option ensures that Magic uses the **XR** display server for better graphical rendering.
- The `&` runs the command in the background.

![s26(magicrc file)](https://github.com/user-attachments/assets/99a39c08-f978-4271-8df5-33a16d6287df)

### **Opening the met3.mag File in Magic**

To open the **met3.mag** file in **Magic**, follow these steps:

1. Launch **Magic** by running the following command:
   ```bash
   magic -d XR &
   ```

2. In the **Magic** window, go to the **File** menu and select **Open**.

3. Navigate to the location of the **met3.mag** file and open it.

This will load the **met3.mag** layout file in Magic for viewing and editing.

![s27](https://github.com/user-attachments/assets/a53058b3-444b-4395-86d1-e7b4488af608)

## **Lab Exercise to fix poly.9 error in Sky130 tech file**

Poly Rules

![Screenshot 2024-12-17 165550](https://github.com/user-attachments/assets/cbb59f60-960b-4ded-b28e-100d60e19b2b)

![s28](https://github.com/user-attachments/assets/f65addec-e6ba-4a8a-8968-07600cc168f1)

After inseritng new commands to update drc below is the fixed drc

![s31](https://github.com/user-attachments/assets/a30934d7-9be6-4fb7-8937-87d0ace28087)

N well Rules

![Screenshot 2024-12-17 174918](https://github.com/user-attachments/assets/09b2ad90-cbcc-4384-a13f-5123186723e6)

![s32](https://github.com/user-attachments/assets/af16fac8-cd6b-4d14-ad75-7dbc8ea6bb92)

After inserting new commands to sky130A.tech file 

![s33](https://github.com/user-attachments/assets/9e7eda47-3cc0-4d4f-aff9-0af54553f7f4)

# Sky 130 Day 4- Pre Layout Timing Analysis and importance of good clock tree

## Convert grid info to track info
The track information file plays a vital role in the physical design process by defining routing paths and layout constraints. It ensures efficient signal routing, prevents design rule violations, and optimizes resource utilization. By converting grid data to track data, it helps reduce congestion and enhances overall design performance. Additionally, it provides essential input for EDA tools to automate placement and routing effectively.

Below is the **track.info** file:-

![s34](https://github.com/user-attachments/assets/a032ea44-7093-4bc6-b19b-00feb051b4bc)

### Setting Grid File Values in TkCon

To set grid file values in the TkCon window, use the following commands:

1. **Check the `grid` Command Syntax**:
   ```tcl
   help grid
   ```

2. **Set Grid Values**:
   Assign specific grid spacing values using:
   ```tcl
   grid 0.46um 0.34um 0.23um 0.17um
   ```
![s35](https://github.com/user-attachments/assets/4e43650a-7d01-49ae-9274-4bdccd43c079)
![s36](https://github.com/user-attachments/assets/ba2fbda2-bb9f-484c-a7f5-cf58912c83ba)

### Saving the Final Custom Cell in the `vsdstdcelldesign` Folder

To save final custom cell in the **TkCon** window:

1. **Command to Save the Layout**:
   ```tcl
   save sky130_vsdinv.mag
   ```

2. **Generate the LEF File**:
   ```tcl
   lef write
   ```

The screenshot below demonstrates the `sky130_vsdinv.mag` file saved in the `vsdstdcelldesign` folder.

![s37](https://github.com/user-attachments/assets/e92d6298-19d2-4d73-8e5e-b7dace78c289)

Newly Created **LEF** file

![s38](https://github.com/user-attachments/assets/91ed6232-9f12-4800-a556-a390232585de)

### Editing `config.tcl` to Add a Custom Cell into OpenLane

```tcl
set ::env(LIB_SYNTH) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"
set ::env(LIB_FASTEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__fast.lib"
set ::env(LIB_SLOWEST) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__slow.lib"
set ::env(LIB_TYPICAL) "$::env(OPENLANE_ROOT)/designs/picorv32a/src/sky130_fd_sc_hd__typical.lib"

set ::env(EXTRA_LEFS) [glob $::env(OPENLANE_ROOT)/designs/$::env(DESIGN_NAME)/src/*.lef]
```

### Running OpenLane Flow for the Design

```bash
# Enter the OpenLane flow in interactive mode
./flow.tcl -interactive

# Load the OpenLane package
package require openlane 0.9

# Prep the design for 'picorv32a'
prep -design picorv32a -tag 18-12_00-40 -overwrite

# Include newly added LEF files to the OpenLane flow
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Run synthesis
run_synthesis
```
![s39](https://github.com/user-attachments/assets/70b4bc15-3482-41a3-a1d5-4650ea8b5dac)

There is a slack 

![s40](https://github.com/user-attachments/assets/7e291843-221d-4ff0-af2e-f7afd8fcc303)

### Improving Timing Analysis in OpenLane

```tcl
# Prep the design again to update variables
prep -design picorv32a -tag 18-12_00-40 -overwrite

# Include newly added LEF files to the OpenLane flow
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Display current value of the SYNTH_STRATEGY variable
echo $::env(SYNTH_STRATEGY)

# Set a new value for SYNTH_STRATEGY
set ::env(SYNTH_STRATEGY) "DELAY 3"

# Display current value of SYNTH_BUFFERING to check whether it's enabled
echo $::env(SYNTH_BUFFERING)

# Display current value of SYNTH_SIZING
echo $::env(SYNTH_SIZING)

# Set a new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Display current value of SYNTH_DRIVING_CELL to check whether it's the proper cell
echo $::env(SYNTH_DRIVING_CELL)

# Run synthesis after applying all updates
run_synthesis
```

![s44](https://github.com/user-attachments/assets/cd4a0fc3-c2da-40b7-bc61-ed11b1ed80f1)

**merged.lef** file :-

![s41](https://github.com/user-attachments/assets/a3aad78b-6865-49eb-ae8a-c247a39ab99f)

### Introduction to Delay Tables and Their Usage

Delay tables are crucial components in the timing analysis and optimization of digital circuits. They provide a systematic way to represent the delay characteristics of standard cells, interconnects, and other elements in a design. These tables map input signal transitions to output delays, helping designers understand how signals propagate through the circuit at various operating conditions, such as voltage, temperature, and load.

In **OpenLane** and other EDA tools, delay tables are used to accurately model and simulate the timing behavior of a design during synthesis and optimization processes. They allow tools to predict the delay of paths and ensure that the design meets the required timing constraints.

### Key Uses of Delay Tables:
1. **Timing Analysis**: They provide essential data for static timing analysis, helping to ensure that all paths in the design meet setup and hold time requirements.
2. **Optimization**: Delay tables are used during the optimization process to adjust cell sizing, buffering, and placement for better performance.
3. **Design Validation**: They help verify that the design will function as expected under different environmental conditions, such as varying voltages or temperatures.
4. **Accurate Simulation**: Delay tables enable more accurate simulation of signal propagation delays during verification and post-layout analysis.

![Screenshot 2024-12-21 155945](https://github.com/user-attachments/assets/3158680b-3d95-44b6-99ba-93fcbd387601)

### Handling `run_floorplan` Command Failure

```tcl
# Initialize the floorplan
init_floorplan

# Place IO cells in the design
place_io

# Add tap and decap cells for noise reduction and power stability
tap_decap_or
```

![s45](https://github.com/user-attachments/assets/ebb451c5-2ffd-4e94-a54b-2dc94dec9da7)

Screenshot of Placement def file in magic after successful floorplan and placement

![s48(correct one)](https://github.com/user-attachments/assets/d7267bf1-0974-4300-8621-b70fa29ee027)

Custom cell sky130_vsdinv is successfully placed

![s49](https://github.com/user-attachments/assets/e85c6f93-9a12-4cc2-a43d-afa24191d5cc)

### Command to View Internal Layers of Cells in TkCon Window

To view the internal layers of cells in the TkCon window, use the following command:

```tcl
expand
```

![s50](https://github.com/user-attachments/assets/7fc0aaa4-e684-4d53-a8a9-070434257017)

### Setup Timing Analysis, Clock Jitter, and Uncertainty

**Setup Timing Analysis**:  

Setup timing analysis ensures that data signals arrive at the flip-flop's input long enough before the clock edge to be reliably captured. It checks if the time between the data signal and the clock signal is sufficient to meet the setup time requirement of the flip-flop, ensuring correct data capture.

**Clock Jitter**:  

Clock jitter refers to small variations or deviations in the timing of the clock signal. These variations can cause fluctuations in the arrival time of the clock edge, potentially leading to setup and hold violations in sequential elements. Proper clock management is crucial to minimize jitter.

**Uncertainty**:  

Uncertainty in timing analysis refers to variations in signal arrival times caused by process variations, temperature fluctuations, or voltage changes. These uncertainties must be accounted for during design to ensure the circuit operates reliably across different operating conditions.

**my_base.sdc** file :-

![s52](https://github.com/user-attachments/assets/399bcc7d-5628-4376-97ba-47be1d7c7732)

### Running STA (Static Timing Analysis) in OpenLane

To run Static Timing Analysis (STA) using OpenLane, follow these steps:

1. **Change Directory to OpenLane**:
   Navigate to your OpenLane directory:
   ```bash
   cd Desktop/work/tools/openlane_working_dir/openlane
   ```

2. **Invoke OpenSTA Tool with Script**:
   Run the STA tool using the configuration script `pre_sta.conf`:
   ```bash
   sta pre_sta.conf
   ```
   
![s53](https://github.com/user-attachments/assets/a21b20e8-15e4-44fe-ab85-ce48c40e967f)

Since more fanout is causing more delay we can add parameter to reduce fanout and do synthesis again

### Preparing and Running Synthesis in OpenLane

```tcl
# Prep the design 'picorv32a' and create necessary files and directories
prep -design picorv32a -tag 18-12_00-40 -overwrite

# Include newly added LEF files to the OpenLane flow
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Set a new value for SYNTH_SIZING to adjust cell sizing during synthesis
set ::env(SYNTH_SIZING) 1

# Set a new value for SYNTH_MAX_FANOUT to control maximum fanout during synthesis
set ::env(SYNTH_MAX_FANOUT) 4

# Display the current value of SYNTH_DRIVING_CELL to ensure the proper cell is being used
echo $::env(SYNTH_DRIVING_CELL)

# Run synthesis now that the design is prepped and variables are set
run_synthesis
```

These commands ensure that the design `picorv32a` is properly prepared, that newly added LEF files are included, and that synthesis is configured with optimized settings for sizing, fanout, and driving cells. 

![s51](https://github.com/user-attachments/assets/c251d14b-6345-4501-aa49-a2926d8f18eb)

### Basic Timing ECO (Engineering Change Order)

**Basic Timing ECO** refers to a set of changes made to a design to meet its timing requirements after an initial timing analysis. It typically involves adjustments to the design, such as resizing cells, adding buffers, or changing placement, to fix timing violations such as setup or hold time errors.

**Why it is Done**:  
Timing ECO is essential to ensure that the design meets the required performance specifications, especially after synthesis or layout. If timing violations are detected during static timing analysis (STA), an ECO is performed to correct these issues and ensure that the design functions correctly under real-world conditions.

![s54](https://github.com/user-attachments/assets/10e55f9a-57b2-4f01-b081-63c8692f28e2)

Starting Slack

![s55 (starting slack)](https://github.com/user-attachments/assets/3c88213e-1f8f-46bb-8a7f-ee5a4551fa8b)

Commands to perform analysis and optimize timing by replacing with OR gate of drive strength 4

```tcl
# Reports all the connections to a net
report_net -connections _11672_

# Checking command syntax
help replace_cell

# Replacing cell
replace_cell _14510_ sky130_fd_sc_hd__or3_4

# Generating custom timing report
report_checks -fields {net cap slew input_pins} -digits 4
```

![s56(slack reduced)](https://github.com/user-attachments/assets/32b26779-72cc-4779-921b-43d439977957)

![s57](https://github.com/user-attachments/assets/7ff26137-5bca-4b3e-8b2e-aa3fc1ada745)

Commands to perform analysis and optimize timing by replacing with OR gate of drive strength 4

```tcl
# Report all the connections to a specific net
report_net -connections _11675_

# Replace the existing cell with an OR gate (drive strength 4)
replace_cell _14514_ sky130_fd_sc_hd__or3_4

# Generate a custom timing report with specified fields and precision
report_checks -fields {net cap slew input_pins} -digits 4
```

![s58(slack reduced)](https://github.com/user-attachments/assets/ae15941f-4fda-4f55-850c-ad398678881a)

Commands to perform analysis and optimize timing by replacing with OR gate of drive strength 4

```tcl
# Reports all the connections to a net
report_net -connections _11643_

# Replacing cell
replace_cell _14481_ sky130_fd_sc_hd__or4_4

# Generating custom timing report
report_checks -fields {net cap slew input_pins} -digits 4
```

![s59(slack reduced)](https://github.com/user-attachments/assets/80e6c411-de78-4124-ad42-d34c1d9ba2d8)

Commands to verify instance _14506_ is replaced with sky130_fd_sc_hd__or4_4

```tcl
# Generating custom timing report
report_checks -from _29043_ -to _30440_ -through _14506_
```

![s61](https://github.com/user-attachments/assets/ffdbbc45-a3ee-434a-b830-ff1fc3545972)

Commands to perform analysis and optimize timing by replacing with OR gate of drive strength 4

```tcl
# Reports all the connections to a net
report_net -connections _11668_

# Replacing cell
replace_cell _14506_ sky130_fd_sc_hd__or4_4

# Generating custom timing report
report_checks -fields {net cap slew input_pins} -digits 4
```
Starting value :- **36.63ns**

Present value :- **35.3473**

Reduced around = **36.63ns**-**35.3473** = **1.2827** violations

![s60(slack reduced)](https://github.com/user-attachments/assets/712824dd-a76d-45f1-89b9-d1ef0281e9e6)

Placement is done we are now ready to run cts:-
```tcl
run_cts
```

![s62](https://github.com/user-attachments/assets/050a9bfb-820d-446d-bd08-08614ad51d2d)

### OpenROAD Timing Analysis in OpenLane After Changing `CTS_CLK_BUFFER_LIST`

The following commands guide you through performing OpenROAD timing analysis after modifying the `CTS_CLK_BUFFER_LIST` in OpenLane:

```tcl
# Checking the current value of 'CTS_CLK_BUFFER_LIST'
echo $::env(CTS_CLK_BUFFER_LIST)

# Removing 'sky130_fd_sc_hd__clkbuf_1' from the list
set ::env(CTS_CLK_BUFFER_LIST) [lreplace $::env(CTS_CLK_BUFFER_LIST) 0 0]

# Checking the updated value of 'CTS_CLK_BUFFER_LIST'
echo $::env(CTS_CLK_BUFFER_LIST)

# Checking the current value of 'CURRENT_DEF'
echo $::env(CURRENT_DEF)

# Setting the DEF file as the placement definition
set ::env(CURRENT_DEF) /openLANE_flow/designs/picorv32a/runs/18-12_00-40/results/placement/picorv32a.placement.def

# Run Clock Tree Synthesis (CTS) again with the updated settings
run_cts

# Checking the updated value of 'CTS_CLK_BUFFER_LIST'
echo $::env(CTS_CLK_BUFFER_LIST)

# Launch OpenROAD for timing analysis
openroad

# Read the LEF file for the design
read_lef /openLANE_flow/designs/picorv32a/runs/18-12_00-40/tmp/merged.lef

# Read the DEF file after CTS
read_def /openLANE_flow/designs/picorv32a/runs/18-12_00-40/results/cts/picorv32a.cts.def

# Create an OpenROAD database for the design
write_db pico_cts1.db

# Load the created database in OpenROAD
read_db pico_cts.db

# Read the netlist after CTS
read_verilog /openLANE_flow/designs/picorv32a/runs/18-12_00-40/results/synthesis/picorv32a.synthesis_cts.v

# Read the Liberty file for the design
read_liberty $::env(LIB_SYNTH_COMPLETE)

# Link the design with the Liberty file
link_design picorv32a

# Read the custom SDC file for timing constraints
read_sdc /openLANE_flow/designs/picorv32a/src/my_base.sdc

# Set all clocks as propagated clocks
set_propagated_clock [all_clocks]

# Generate a custom timing report with min and max path delays
report_checks -path_delay min_max -fields {slew trans net cap input_pins} -format full_clock_expanded -digits 4

# Report hold skew for the design
report_clock_skew -hold

# Report setup skew for the design
report_clock_skew -setup

# Exit OpenROAD and return to OpenLane flow
exit

# Checking the current value of 'CTS_CLK_BUFFER_LIST' again
echo $::env(CTS_CLK_BUFFER_LIST)

# Inserting 'sky130_fd_sc_hd__clkbuf_1' back into the list
set ::env(CTS_CLK_BUFFER_LIST) [linsert $::env(CTS_CLK_BUFFER_LIST) 0 sky130_fd_sc_hd__clkbuf_1]

# Checking the updated value of 'CTS_CLK_BUFFER_LIST'
echo $::env(CTS_CLK_BUFFER_LIST)
```

![s64](https://github.com/user-attachments/assets/3496398d-36df-4cf1-a6a7-1f6d31febe0f)
![s65](https://github.com/user-attachments/assets/2cf313e6-7b4d-41b2-9d74-38e19d70d31b)
![s66](https://github.com/user-attachments/assets/1ce577dd-1ce4-4a4f-8cfb-b0a4afc53883)
![s67](https://github.com/user-attachments/assets/360bc4b5-df59-4085-b6a4-bda0ff50b6eb)
![s68](https://github.com/user-attachments/assets/7a5bbd4b-8f54-42c9-b17d-cdc58a85f674)
![s69](https://github.com/user-attachments/assets/8583492e-4fb9-466d-aea6-8b46d0c80030)
![s70](https://github.com/user-attachments/assets/7c87d83a-5873-4354-8455-79a62838baf3)

# Sky130 Day 5- Final steps for RTL2GDS using triton route and openSTA

### Routing and Design Rule Check (DRC) in OpenLane

**Routing**:  

Routing in OpenLane refers to the process of connecting the various components of the design (cells, pins, and ports) using metal layers to establish the necessary electrical connections. The routing process ensures that signals are properly routed between the cells, and all connectivity requirements are met while adhering to design constraints like wire length, resistance, and capacitance.

**Design Rule Check (DRC)**:  

Design Rule Check (DRC) is a verification process that ensures the design meets the fabrication rules and physical constraints of the manufacturing process. DRC checks for errors such as rule violations (e.g., spacing, width, and overlap of metal layers) that could lead to manufacturing defects or performance issues. It ensures that the design is manufacturable and functions as expected in the real-world environment.

### Maze Routing and Lee Algorithm

**Maze Routing**:  

Maze routing is a method used in VLSI design to find paths for routing signals between pins on a chip. It is inspired by solving a maze, where the goal is to navigate from a start point (source) to an endpoint (destination) while avoiding obstacles. The algorithm ensures that the routed paths do not overlap or violate design rules.

**Lee Algorithm**:  

The Lee algorithm is a specific maze-routing algorithm that uses breadth-first search (BFS) to find the shortest path between two points on a grid. It works by exploring all possible routes from the source in layers, expanding outward until it reaches the destination. The algorithm guarantees an optimal path without violating any connectivity or design rules, making it useful for interconnect routing in integrated circuit designs.

![Screenshot 2024-12-21 174307](https://github.com/user-attachments/assets/caba5d36-a4aa-44fb-b878-d34e2d964747)

## Power Distribution Network and Routing

A **Power Distribution Network (PDN)** is a system designed to deliver electrical power efficiently and reliably from a power source to various components in a circuit or system. It plays a critical role in maintaining stable power levels and minimizing noise and losses in electronic devices.

Key components of a PDN include:
- **Power Sources:** Batteries, power supplies, or other energy sources.
- **Voltage Regulators:** Ensure stable and consistent voltage levels.
- **Planes and Traces:** Conductive paths on PCBs for distributing power.
- **Decoupling Capacitors:** Minimize voltage fluctuations and provide local energy storage.
- **Connectors:** Facilitate power transfer between components or modules.

Commands to perform all necessary stages up until now
```tcl
# Now that we have entered the OpenLANE flow contained docker sub-system we can invoke the OpenLANE flow in the Interactive mode using the following command
./flow.tcl -interactive

# Now that OpenLANE flow is open we have to input the required packages for proper functionality of the OpenLANE flow
package require openlane 0.9

# Now the OpenLANE flow is ready to run any design and initially we have to prep the design creating some necessary files and directories for running a specific design which in our case is 'picorv32a'
prep -design picorv32a

# Addiitional commands to include newly added lef to openlane flow merged.lef
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
add_lefs -src $lefs

# Command to set new value for SYNTH_STRATEGY
set ::env(SYNTH_STRATEGY) "DELAY 3"

# Command to set new value for SYNTH_SIZING
set ::env(SYNTH_SIZING) 1

# Now that the design is prepped and ready, we can run synthesis using following command
run_synthesis

# Following commands are alltogather sourced in "run_floorplan" command
init_floorplan
place_io
tap_decap_or

# Now we are ready to run placement
run_placement

# With placement done we are now ready to run CTS
run_cts

# Now that CTS is done we can do power distribution network
gen_pdn
```
![s71](https://github.com/user-attachments/assets/402e1f3b-cf3c-4308-a3b8-64fd2b869912)

Screenshot of PDN Def

![s72](https://github.com/user-attachments/assets/3de90620-2445-4bb1-9c9b-9e336ad468cb)
![s73](https://github.com/user-attachments/assets/34ecfe1b-f905-4bd0-99c5-86667f590cdc)

Command to perform routing

```tcl
# Check value of 'CURRENT_DEF'
echo $::env(CURRENT_DEF)

# Check value of 'ROUTING_STRATEGY'
echo $::env(ROUTING_STRATEGY)

# Command for detailed route using TritonRoute
run_routing
```
![s74](https://github.com/user-attachments/assets/cbec5217-51e6-4445-a811-d70cf6fafc89)

Screenshot of Routed def

![s75](https://github.com/user-attachments/assets/598b2b5d-35a0-46cf-a217-0908e95590d1)

### Routing

**Routing** is the process of connecting various components or modules in an integrated circuit (IC) or printed circuit board (PCB) using conductive paths. The goal is to create electrical connections while adhering to design rules and performance requirements.

#### Types of Routing

1. **Fast Route:**
   - **Purpose:** Quickly generates initial connections between components for feasibility analysis.
   - **Characteristics:** Focuses on approximate paths, avoiding detailed optimization.
   - **Use Case:** Early stages of design to estimate routing feasibility and congestion.

2. **Detailed Route:**
   - **Purpose:** Completes precise connections, ensuring adherence to design rules like spacing, width, and vias.
   - **Characteristics:** Optimized for performance, reliability, and manufacturability.
   - **Use Case:** Final stages of design for production-ready layouts.

![d1](https://github.com/user-attachments/assets/0f35a487-25d3-4a56-abbe-78845c67b05f)

Screenshot of fast route guide present in `openlane/designs/picorv32a/runs/20-12_18-37/tmp/routing directory`

![s76](https://github.com/user-attachments/assets/a192654d-0b45-460e-8ff6-f1be38334fdf)

picorv32a.synthesis_cts.v file generated in synthesis folder:-

![s77](https://github.com/user-attachments/assets/7961f643-bba1-4bf6-9ab6-4317956f211b)

Commands to be run in OpenLANE flow to do OpenROAD timing analysis with integrated OpenSTA in OpenROAD

```tcl
# Command to run OpenROAD tool
openroad

# Reading lef file
read_lef /openLANE_flow/designs/picorv32a/runs/20-12_18-37/tmp/merged.lef

# Reading def file
read_def /openLANE_flow/designs/picorv32a/runs/20-12_18-37/results/routing/picorv32a.def

# Creating an OpenROAD database to work with
write_db pico_route.db

# Loading the created database in OpenROAD
read_db pico_route.db

# Read netlist post CTS
read_verilog /openLANE_flow/designs/picorv32a/runs/20-12_18-37/results/synthesis/picorv32a.synthesis_preroute.v

# Read library for design
read_liberty $::env(LIB_SYNTH_COMPLETE)

# Link design and library
link_design picorv32a

# Read in the custom sdc we created
read_sdc /openLANE_flow/designs/picorv32a/src/my_base.sdc

# Setting all cloks as propagated clocks
set_propagated_clock [all_clocks]

# Read SPEF
read_spef /openLANE_flow/designs/picorv32a/runs/20-12_18-37/results/routing/picorv32a.spef

# Generating custom timing report
report_checks -path_delay min_max -fields {slew trans net cap input_pins} -format full_clock_expanded -digits 4

# Exit to OpenLANE flow
exit
```
Screenshots of commands run and timing report generated

![s78](https://github.com/user-attachments/assets/6329f719-aba4-45b6-990f-a80674dca7e2)
![s79](https://github.com/user-attachments/assets/2fe4e190-9f80-4057-8b03-a502574d733d)
![s80](https://github.com/user-attachments/assets/095f8eff-147d-4773-bfab-890fc762c5e8)

# Reference

https://github.com/fayizferosh/soc-design-and-planning-nasscom-vsd.git
