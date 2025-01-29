
SKY130 Day 1: Inception of OpenSource EDA, OpenLANE and SKY130 PDK 
  
  How to Talk to Computers
  
    Introduction to QFN - 48 package, chip, pads, core, die and IPs
![Screenshot 2025-01-26 163454](https://github.com/user-attachments/assets/a80af55f-5c0c-4e05-bcf1-e66a8fb5c074) ![Screenshot 2025-01-26 163619](https://github.com/user-attachments/assets/9b5aa2d8-7fdb-4b3f-97ef-fea20620b2b5)


chip are called as package and package are given name as QFN-48 Quad Flat No-leads.chip is fixed at the centre of the package as shown in the figure

![Screenshot 2025-01-26 164005](https://github.com/user-attachments/assets/c60cb78c-33fb-4da0-834c-b7484a648113) 
components of chip 

PADs-pads" refer to the small, exposed areas of metal on the edge of a chip's die that provide a larger surface area for connecting external wires or components to the chip, essentially acting as the points of contact for input and output signals and power supply to the chip itself

CORE-is the place where digital logic gates are placed

DIE-The die is the material that the circuit is made on. In the context of silicon wafers, it’s going to be made of silicon.

![Screenshot 2025-01-26 164533](https://github.com/user-attachments/assets/49df31b8-2b7b-4e70-8d9c-5c4a878d1752)
Foundry IP-Foundry IP" refers to "Foundry Intellectual Property," which essentially means intellectual property (like patents, trademarks, or designs) that is managed or handled by a company called "Foundry,

MACROS-macros refer to pre-designed blocks or functional units that can be reused in different designs. These macros can include standard cells (like logic gates), memory blocks (like SRAM), or complex blocks (like analog circuits or processor cores).

SKY_L2 - Introduction to RISC-V


RISC-V, pronounced "risk-five," is an open-source Instruction Set Architecture (ISA) used in chip design, essentially a set of rules defining how a processor should operate, that allows developers to create custom processors for various applications

for example -While RISC-V itself is not a programming language like C, C code can be compiled into machine code that is executed on a RISC-V processor. The compiler translates the C instructions into the appropriate RISC-V assembly language instructions, which are then executed by the processor.

![image](https://github.com/user-attachments/assets/67bfbfbc-7b6a-466a-bf8c-7ea5e6d919d6)

SKY130_D1_SK1 - How to talk to computers


SKY_L3 - From Software Applications to Hardware

From software to hardware" means moving from the set of instructions or programs (software) that tell a computer what to do, to the physical components (hardware) that actually execute those instructions

![Screenshot 2025-01-26 180317](https://github.com/user-attachments/assets/24a3a92b-84ad-4690-8563-7bfa702d0410)

Compiler-A compiler is a computer program that translates source code written in a high-level programming language into machine code or another programming language

OP-An operating system is the most important software that runs on a computer. It manages the computer's memory and processes, as well as all of its software and hardware.

Assembler-An assembler is a computer program that converts assembly language into machine language. This allows a computer to directly communicate with its hardware.


SKY130_D1_SK2 - SoC design and OpenLANE


SKY_L1 - Introduction to all components of open-source digital asic design

To design digital ASIC we need several elemnts these elements are RTL IPs ,EDA Tools , PDK Data

What is a PDK -Process design kit -collection of files used to model a fabrication process for the EDA tools used to design an IC

Process design rules ;DRC,LVS<PEX

Digital standard cell Libraries 

I/o Libraries 
Google and skywater in Jne 30 ,2020 released open source PDK for mass

![Screenshot 2025-01-26 184659](https://github.com/user-attachments/assets/a06ecc71-2a5d-42aa-ab0a-a6a01c9fd1cf)


SKY130_D1_SK2 - SoC design and OpenLANE


SKY_L2 - Simplified RTL2GDS flow

An RTL model, which stands for "Register Transfer Level" model, is a design abstraction used in digital circuit design to describe the behavior of a circuit by focusing on the flow of data between registers and the logical operations performed on that data

![synthesis](https://github.com/user-attachments/assets/3b8bbd83-f024-4474-96c3-bba2679eaccb)


Process of converting a high-level hardware description into a netlist that represents the physical implementation of a circuit


![floor n power planning](https://github.com/user-attachments/assets/38a2f461-02bd-4882-af3e-a0ea626bd193)


The process of determining the location of each logic cell in a chip's layout.


![placement](https://github.com/user-attachments/assets/82fa41aa-11ab-4e18-8602-346bda96c74b)


It's a technique that distributes clock signals equally to all sequential parts of a VLSI design.


![Screenshot 2025-01-26 191533](https://github.com/user-attachments/assets/65638f00-ebb6-49fe-b72a-a597a84a778f)


The process of creating physical connections between signal pins using metal layers.



![routing](https://github.com/user-attachments/assets/6b3892a9-37e5-4b16-b994-3c7c1299e50e)



The final verification process for a chip design before it's sent to manufacturing.



![Screenshot 2025-01-26 191731](https://github.com/user-attachments/assets/fe2912df-7b65-456f-ae39-fbbb6a9bf3c4)

SKY130_D1_SK2 - SoC design and OpenLANE


SKY_L3 - Introduction to OpenLANE and Strive chipsets

![image](https://github.com/user-attachments/assets/cbed9455-666c-4627-8f7a-15885a8b2f1a)

Main Goat of OPENLANE is
*Produce a clean GDSII with no human intervention(no-human-in-the-loop)

*clean means

   NO LVS violations

   No DRC violations

   Timing violations 

 *Tune for Sky water 130nm open PDK
 
 *Functional out of the box 
 
 *instructions to build and run natively will follow 

 *can be used to harden macros and chips 

 *two modes of operation

   Autonomous or interactive 

*Design space Exploration    

  Find the best set of flow configuration 

*Large number of design examples 

  
  43 designs with their best configurations
  
  
  more will be added soon

SKY130_D1_SK2 - SoC design and OpenLANE

  
SKY_L4 - Introduction to OpenLANE detailed ASIC design flow

![Screenshot 2025-01-26 210147](https://github.com/user-attachments/assets/3f87f17e-8190-4cb5-bb84-68ee0c42f362)

Open Asec flow 

1 sunthesis emploration 

2 Design explosaton 

![Screenshot 2025-01-26 210650](https://github.com/user-attachments/assets/6e4d7fe6-4fa6-4cd7-9715-04e3be768f5d)


3 Design for test [DFT]

![Screenshot 2025-01-26 210804](https://github.com/user-attachments/assets/5dd890d4-735f-4e65-ab09-f56c761e891c)

![Screenshot 2025-01-26 210845](https://github.com/user-attachments/assets/c064a770-72b4-4600-9aa2-f8037cae9d58)

4 physical im plementation 

Aloso called Aumated PnR [ place and route ] 

* Floor / pawer planning * End decaupling capautors and tap calls insertion
  
* pLacement : Globak and detailed

* Post placement optimization

* Clock tree synthesis [ CTS ]

* Routing global and detailed

  Its OPEN ROAD application

  Logic Equation Check [ LEC ]

  * Every time the nethist is madified  , verification  must be performed
 
  * 1. CTS modified the nethlist

    2. Post pLacement optimization modifies the nethist

  * LEG is used to formally confirm that the function did not change after modifying the nethist dealing with Antenna Rules violation
 
![Screenshot 2025-01-26 211656](https://github.com/user-attachments/assets/688f8202-4c6e-4a5d-afd5-17ae2af399bc)

![Screenshot 2025-01-26 211740](https://github.com/user-attachments/assets/80c19b5d-c390-4db3-82b4-1544732ee1ef)

![Screenshot 2025-01-26 211749](https://github.com/user-attachments/assets/441e3bcb-d397-45eb-9f22-0f122b70651c)

Statistining Analysis 

![Screenshot 2025-01-26 211927](https://github.com/user-attachments/assets/d2b0e5a9-c351-4d52-9703-07db0c4b4dfd)

Physical verfication

![Screenshot 2025-01-26 212002](https://github.com/user-attachments/assets/e7f23fb8-8115-43c5-968f-32fa28f07801)

OpenLane is an open-source platform for silicon implementation in VLSI (very large scale integration). It's used to construct digital ASIC physical implementation flows OpenLane's flow includes synthesis, floor planning, placement, clock tree synthesis, routing, RC extraction, STA, sign-off steps, and GDSII extraction.

OpenLane is free to use and modify. 

OpenLane can be customized with Python scripts and utilities. 

OpenLane supports tools like Yosys, OpenROAD, Magic, and KLayout. 

open terminal in  virtualbox as shown below 


![Screenshot 2025-01-27 140500](https://github.com/user-attachments/assets/d05ac0d1-9ebe-4b13-b328-95720b970b68)

1) Type cd Desktop -where "cd" stands for "change directory" and "desktop" refers to the Desktop folder on your computer,then go to work/tools this wher our files r saved

2) ls -ltr  --will list the contents in the folder in chronological order

![Screenshot 2025-01-27 150628](https://github.com/user-attachments/assets/8555fe8d-a4d2-4d9c-944d-7ea26a8ba830)

3)next cd openlane and list the contents of this folder type ls -ltr

4)to check contents of pdk  type cd pdk n ls -ltr

5)in pdk we can see sky130a, cd sky130a will show contents which contain libs.tech. libs.tech contains all tool specific files


![Screenshot 2025-01-27 152313](https://github.com/user-attachments/assets/d9764e37-786b-464c-9ac2-5ed81c708ac3)

6)similarlly libs.ref contains all the technology/foundry related processes


![Screenshot 2025-01-27 152613](https://github.com/user-attachments/assets/9a1b0b7f-1463-459f-a8b2-c95ce0d80a6c)


![Screenshot 2025-01-27 153740](https://github.com/user-attachments/assets/9978dbb4-44b0-4158-9423-5ce3abb47091)

lets work with openlane 


![Screenshot 2025-01-27 154047](https://github.com/user-attachments/assets/b7277024-92d9-499e-9b1c-6ddb4a385ee2)

to start openlane type docker command ,the prompt changes to bash-4.2$,ls -lrth--->then type flow.tcl -interactive---> package require openlane 0.9 will give information about openlane 


![Screenshot 2025-01-27 154515](https://github.com/user-attachments/assets/279de637-b0e0-4b8c-a0e2-18981abf345d)

openlane has many designs in this lets work with picorv32


![Screenshot 2025-01-27 161822](https://github.com/user-attachments/assets/51d2a3bd-42db-4254-9aef-fb80e1c04cb7)


![Screenshot 2025-01-27 162515](https://github.com/user-attachments/assets/b4b740af-541c-4df4-bdf0-9ba7a492f573)

let us prepare design in openlane by command prep _design picorv32a


![Screenshot 2025-01-27 163245](https://github.com/user-attachments/assets/63a4fc83-ea16-4b8e-ab03-4b3e8c17f9ae)

folder run  27-01_11-02 is created inside the picorv32a directory which contains the command log files, results, and the reports dumped of the various tool. The folder will be only have the lef files generated by this design setup stage. The cell LEF files .lef and technology LEF files .tlef merge to generate merged.lef inside runs/tmp/, wherein a a folder with today's date will be created, inside which a tmp folder will have contents, and the merged.lef folder will contain the merged lef files.

![Screenshot 2025-01-27 163822](https://github.com/user-attachments/assets/51ca80b1-51aa-4e2b-906d-817446e60984)

![Screenshot 2025-01-27 164025](https://github.com/user-attachments/assets/4fa9239a-8569-42c9-ad3b-41d23ba5c5f1)

![Screenshot 2025-01-27 164043](https://github.com/user-attachments/assets/a5586bfc-d4d0-492b-ac64-cf54f5352058)

temp file contents are as follow ,when we open merged.lef file we get contents as followes
![Screenshot 2025-01-27 164601](https://github.com/user-attachments/assets/ab055f6b-e2af-4be7-a35c-15d08f202e98)

![Screenshot 2025-01-27 165805](https://github.com/user-attachments/assets/b10def4a-9414-45e4-b895-fa64a102dc0b)

![Screenshot 2025-01-27 170817](https://github.com/user-attachments/assets/2903b857-6826-469e-b5de-5a4acbeaf2a6)

![Screenshot 2025-01-27 170844](https://github.com/user-attachments/assets/0c8ed6f6-dc9d-40a4-8276-bb2b85b0d6a1)

![Screenshot 2025-01-27 170950](https://github.com/user-attachments/assets/4391a0db-47f3-498f-a207-68001350419b)

after run synthesis ,printing statistics as shown below can be used to calculate flip-flops ratio

Flip flop ratio =no of DFFs/no of cells *100

1613/18036*100 = 8.94%

![Screenshot 2025-01-27 200101](https://github.com/user-attachments/assets/dbe81d68-bdfa-48a1-96c3-11f12c5c054d)

![Screenshot 2025-01-27 200929](https://github.com/user-attachments/assets/658ea58a-c781-429a-9374-2b39aeed2e4d)











After this, type the command run_synthesis to run synthesis which converts an abstract netlist into a program to run yosys RTL synthesis, ABC scripts (for technology mapping) and openSTA


DAY 2

1) CHIP FLOOR PLANNING CONSIDERATIONS 

utilisation factor and Aspect Ratio 

Floorplanning is basically the arrangement of logical blocks (i.e. multiplexer, AND, OR gates, buffers) on silicon chiphere we need to plan height and width of the core and die

Example :let us take each cell with standard dimensions as 1 unit there are 4 units arranged as shown below 

![Screenshot 2025-01-29 005817](https://github.com/user-attachments/assets/ba4790ce-81a5-4633-a14e-deb3396e42f6)


![Screenshot 2025-01-29 005320](https://github.com/user-attachments/assets/f3335801-f81c-413c-ba4b-0df633b33187)


utilisation factor :The utilization factor is the ratio of the area of the net list to the total area of the core. 

Aspect ratio:
The aspect ratio is the ratio of the height to the width of a chip. 
if utilization factor is 1 means 100% utilzation of space and it will be in square in shape ,other than 1 it is rectangular in shape 

![Screenshot 2025-01-29 005857](https://github.com/user-attachments/assets/a8964aa9-8d06-4040-afa5-b91ef5243478)


DAY2 
2) Example 2 let us find utilization factore n ascepect ratio of block with 4X 4 unit area and netlist with area 2X2 
utilization factor is 2X2/4X4 = 0.25

it says that out of the complete chip area only 25% is used by netlist and 75% is available for optimization 

aspect ratio is 4/4 =1 that means it is square in shape 

DEFINE LOCATION OF PREPLACED CELLS 


![Screenshot 2025-01-29 010115](https://github.com/user-attachments/assets/7a76e9ca-e6c8-49b0-854d-dca9dba88267)


![Screenshot 2025-01-29 010308](https://github.com/user-attachments/assets/de7616dc-98d2-40f4-b3ec-4dfda3bccad5)


combinational logic is huge circuit suppose if there are 100k logic gates we can divide the circuit into two blocks of 50k each as shown . advantage of doing seperate block is each block can be used multiple time and we dont have to implement multiple times.

![Screenshot 2025-01-29 010521](https://github.com/user-attachments/assets/e62f90ca-98c9-4e27-86ba-3942587c7625)


*The arrangement of these IP's in chip is reffered as FLOOR PLANNING 

*These IP's /blocks have user -defined locations ,and hence are placed in chip before automated plcement and routing and are called PRE-PLACED cells 

*Automated placement and routing tools place the remaining logical cells in the design onto chip

SURROUND pre-placed cells with decoupling capacitors 

When we need 1 in the logic circuit capacitors in the circuit need full charge n dicharge when 0 is needed .power supply is connected to logic circuits with resistors n impedence so some amount of voltage is lost beofre it  reches logic circuit n it is called noise margine .Logic gate to be 0 or 1 it should be in the NM2 and NMh ranges respectivelly the problem can be solved by decoupling capacitor .Decoupling capacitor decouples logic circuit with the main supply.

![Screenshot 2025-01-29 011134](https://github.com/user-attachments/assets/522425aa-03f1-4e60-b146-b641a3815c2a)


POWER PLANNING 

purpose of power planning : all capacitors which were charged to V volts will have to discharge to 0 volts through single grounded tap point this will cause bump in ground tap point and is called Ground bounce 

![Screenshot 2025-01-29 011134](https://github.com/user-attachments/assets/d8a54d4a-a8c4-4ca4-b6ec-6577ada72ed3)


all capacitors which were 0 volts will have to charge to V volts through single Vdd tap point this will cause lowering of voltage at Vdd tap point and ia called voltage drop 

this problem can be solved by multiple power supplies as shown below


![Screenshot 2025-01-29 011639](https://github.com/user-attachments/assets/0baa2bb2-a48d-4da3-8236-1a3f877e4e60)



COMPLETE DESIGN

It involves all steps of the design process, starting with system requirements, moving through RTL coding, logic synthesis, physical design, and ending with verification and layout checks to ensure the chip meets all performance and functionality criteria. 

![Screenshot 2025-01-29 011749](https://github.com/user-attachments/assets/8a20a920-b4dc-4137-9a50-67613f9a6bc0)

# to run floorplan follw below steps/commands

cd Desktop/wirk/tools//openlane_working_dir/openlane

docker

./flow.tcl -interactive

#to prepare package 

package require openlane 0.9

![Screenshot 2025-01-28 204247](https://github.com/user-attachments/assets/5c37bb49-1589-4439-a725-ffa19088a174)


#we can run synthesis y command

% run_synthesis

%run_floorplan 


![Screenshot 2025-01-29 100518](https://github.com/user-attachments/assets/f133526e-c384-4a2a-b58d-4063b6ceea6c)


![Screenshot 2025-01-29 100543](https://github.com/user-attachments/assets/aecbd9fd-8a9b-4f63-aa92-324fd52b13d3)


here we get values to calculate Area of diearea .here die width = 660.685 microns and dieheight=671.405

Area of die in microns =660.685*671.405=671.405 micron

Review floorplan layout in magic 

#commands are as follows

cd Desktop/wirk/tools//openlane_working_dir/openlane/designs/picorv32a/28-01_17-09/results/floorplan/

#follow by magic tool

magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &

![Screenshot 2025-01-28 234606](https://github.com/user-attachments/assets/04bccd04-d689-44d4-b050-dc7769188bf5)

![Screenshot 2025-01-28 234642](https://github.com/user-attachments/assets/2d70ebe5-2f02-471d-b927-d4f41e6a6925)

![Screenshot 2025-01-28 235812](https://github.com/user-attachments/assets/4688cd92-b4aa-45de-b734-3ed07eda2b73)

![Screenshot 2025-01-28 235908](https://github.com/user-attachments/assets/b1784bbf-fe96-4463-9253-235bdfb7be78)

![Screenshot 2025-01-29 000223](https://github.com/user-attachments/assets/97e9cbd9-f7bb-4d36-a6bc-06aaae943bf4)

![Screenshot 2025-01-29 074447](https://github.com/user-attachments/assets/a3d9cd80-f452-4b5f-977d-4b1f4d1377bc)

congestion Aware placement using REPLACE 

#command to run placement

% run_placement

after running placement in another terminal follow below command 

cd Desktop/wirk/tools//openlane_working_dir/openlane/designs/picorv32a/28-01_17-09/results/placement

magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef read ../../tmp/merged.lef def read picorv32a.p/acement.def &

weget as follows

![Screenshot 2025-01-29 065721](https://github.com/user-attachments/assets/cd86f3e5-981b-4fb6-87ee-ffe85d00348e)

![Screenshot 2025-01-29 072406](https://github.com/user-attachments/assets/df7e4cb9-08bc-402a-88f8-cfed71c3d2f7)

![Screenshot 2025-01-29 072421](https://github.com/user-attachments/assets/e713c755-53da-4be4-93d1-5a9c5b51df17)

![Screenshot 2025-01-29 073644](https://github.com/user-attachments/assets/fee1387e-1828-4474-9d98-361ebd559bae)

![Screenshot 2025-01-29 073953](https://github.com/user-attachments/assets/4a385d60-5c0b-4437-8c37-86488a64f323)

Bindlist with physical cells 

In reality gates are square on rectangle in shape 


1. Library :-
   All components are present in shelf and it is called as library it will delay information about height width delay and require condition of every cell

3. Plcement :-
   we have loreplan and netlist and physical view of logical gates so now let us place in properway as followes input are placed near input and output near outputs as much as possible

## Optimize placement

This isthe stage where we estimate wire length and capacitance and based on that insert repeaters . 

To maintain signal integtraty we place repeaters [ buffers ] . Buffers are placed if distance is more 

## Final placement optimization 

Need for Libreries and charactorization logic synthesis :- 

synthesis is the process of converting a RTL code to optimized gate level netlist to the targeted technology CTS - Clock Tree Synthesis - clock being spread across whole the logiccells at an equal time 

Steps  -logic synthesis - floor planning -placement - CTS - routing 

STA - Static Timing Analysis is the last step in chip design 

Placement :- 

commend to coneze design 

% run_placement [ Global Placement Happens ]

placement in done let us check how our design is fun that command is 

cd Desktop/wirk/tools//openlane_working_dir/openlane/designs/picorv32a/run/28-01_17-09/results/floorplan 

cd Desktop/wirk/tools//openlane_working_dir/openlane/designs/picorv32a/28-01_17-09/results/placement

we can see def life created 

magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef read ../../tmp/merged.lef def read picorv32a.placement.def &

SKY.L1 - inputs for cell design flow 

Standard cells in IC design are nothing but buffer , flipflops , and , OR , gate , inverter  and there are kept in library . 

Each components flow foundary parameter some examples are shawn below 

Design steps involves :- 

is steps circuit design layout steps involves 3 steps circuit design , layout design and characterization 

Circuit design - 

we get value of [ WP/LP ] of pmos and WN/LN of nmos 

implement these value in layout design using

Charactorixation flow . 

1. Read in the mode files

2. Extracted spices netlist

3. Defin or recognise the behavior of the buffer

4. Read sub circuit  of the inverter

5. Attach power sources

6. Apply the stimatus

7. Output capacitance

8. Neccessary stimulation common

## Timing Chracterization

   delay = time [ out_*_thr ] - time [ in_*_the ]

   time [ slew_high_rise_thr ] - time [ slew_low_rise_thr ] 

time [ slew_high_fall_the ] - time [ slew_low_fall_the ] 













































   




   



















