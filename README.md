# SKY130 Day 1: Inception of OpenSource EDA, OpenLANE and SKY130 PDK 
  
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


# DAY 2

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

![Screenshot 2025-01-29 065721](https://github.com/user-attachments/assets/f321c087-da56-432d-b68c-546c30cdc27f)

![Screenshot 2025-01-29 072439](https://github.com/user-attachments/assets/c40699c9-e31d-4e9c-8117-d06a896d8535)


magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef read ../../tmp/merged.lef def read picorv32a.p/acement.def &


![Screenshot 2025-01-29 072406](https://github.com/user-attachments/assets/92958058-4acb-43f4-bcc2-57af4ebf31e5)



weget as follows


![Screenshot 2025-01-29 073644](https://github.com/user-attachments/assets/fee1387e-1828-4474-9d98-361ebd559bae)

![Screenshot 2025-01-29 073953](https://github.com/user-attachments/assets/4a385d60-5c0b-4437-8c37-86488a64f323)

![Screenshot 2025-01-29 074447](https://github.com/user-attachments/assets/f111b4bd-2ef9-4b60-9fa1-59fd99024e1d)

![Screenshot 2025-01-29 074801](https://github.com/user-attachments/assets/0a1835af-277e-4680-ae34-858aaf30830b)


Bindlist with physical cells 

In reality gates are square on rectangle in shape 


1. Library :-
   All components are present in shelf and it is called as library it will delay information about height width delay and require condition of every cell


![Screenshot 2025-01-29 132138](https://github.com/user-attachments/assets/8bde0fea-91b8-47b7-ace0-5867285a0dbf)


3. Plcement :-
   we have loreplan and netlist and physical view of logical gates so now let us place in properway as followes input are placed near input and output near outputs as much as possible

![Screenshot 2025-01-29 132633](https://github.com/user-attachments/assets/77c6d5a4-278d-4559-a3c8-2eb42c7d3984)

## Optimize placement

This isthe stage where we estimate wire length and capacitance and based on that insert repeaters . 

To maintain signal integtraty we place repeaters [ buffers ] . Buffers are placed if distance is more 

![Screenshot 2025-01-29 133645](https://github.com/user-attachments/assets/16f519a8-d0f7-4593-a860-cc3d7908f55c)


## Final placement optimization 


![Screenshot 2025-01-29 134521](https://github.com/user-attachments/assets/89b42163-2a92-4839-abe0-917efd4a775a)


Need for Libreries and charactorization logic synthesis :- 


![Screenshot 2025-01-29 140132](https://github.com/user-attachments/assets/d9a4f797-a1e8-4d64-a9e4-a10f568d4a63)


synthesis is the process of converting a RTL code to optimized gate level netlist to the targeted technology CTS - Clock Tree Synthesis - clock being spread across whole the logiccells at an equal time 

Steps  -logic synthesis - floor planning -placement - CTS - routing 

STA - Static Timing Analysis is the last step in chip design 

Placement :- 

commend to conreze design 

% run_placement [ Global Placement Happens ]

placement in done let us check how our design is fun that command is 



cd Desktop/wirk/tools//openlane_working_dir/openlane/designs/picorv32a/run/28-01_17-09/results/floorplan 

cd Desktop/wirk/tools//openlane_working_dir/openlane/designs/picorv32a/28-01_17-09/results/placement

we can see def life created 

magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef read ../../tmp/merged.lef def read picorv32a.placement.def &

SKY.L1 - inputs for cell design flow 

Standard cells in IC design are nothing but buffer , flipflops , and , OR , gate , inverter  and there are kept in library . 

Each components flow foundary parameter some examples are sh0wn below 

![Screenshot 2025-01-29 142242](https://github.com/user-attachments/assets/b75e6f18-2857-4205-89f9-62fb9e5d4f3e)

![Screenshot 2025-01-29 142646](https://github.com/user-attachments/assets/215c1e53-8aaa-43fe-aa26-5b3822048e58)

![Screenshot 2025-01-29 152149](https://github.com/user-attachments/assets/51ef9527-e10c-4bce-87c3-841744c8a1fc)

Design steps involves :- 

is steps circuit design layout steps involves 3 steps circuit design , layout design and characterization 

Circuit design - 

we get value of [ WP/LP ] of pmos and WN/LN of nmos 

implement these value in layout design using

![Screenshot 2025-01-29 153218](https://github.com/user-attachments/assets/c2aaaf66-4274-40ef-aaf0-78a710a44399)

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

![Screenshot 2025-01-29 153338](https://github.com/user-attachments/assets/1918f3a8-80bb-45e6-88f5-ce00a521a79d)

# Day - 3 

## SKY_L0 - IO placer revision

DESIGN LIBRARY CELL USING MAGIC LAYOUT AND NGSPICE CHARACTERISATION

LABS FOR CMOS INVERTER NGSPICE

open lane with configuration can be changed by using command set :: env(FP_IO_MODE)  2

before input output pins were equidistant and after using set command it will change 2

![Screenshot 2025-01-29 155521](https://github.com/user-attachments/assets/e96d0d03-c8f4-45ca-b3ec-9ef52d2041e4)

## SKY L1 + L2 SPICE deck for creation of cmos inverter + SPICE simulation lab for cmos inverter

SPICE DECK CREATION FOR CMOS INVERTE

create spice deck

*component connection

*component values

*identify the nodes

*name nodes

![Screenshot 2025-01-29 181518](https://github.com/user-attachments/assets/fae0c60d-8f7e-4897-b607-6dc55b4e7031)

![Screenshot 2025-01-29 182353](https://github.com/user-attachments/assets/3166a955-79b4-4e7e-b173-f9670b66a178)


FOR PSICE SIMULATION


for spice simulation there are various steps

.open the NGSPICE SIMULATOR

*source command

*command run

*set plot

*we can views plots

*display this will give us choice of nodes to be plotted

*plot out Vs in  to plot on graph

*screen shot

THRESHOLD Vm

*screenshot

*cmos is a robust device as it gives same shaped graph

*the switching threshold is the pooint where both input and output are euual

*screen shot

STATIC AND DYNAMIC SIMULATION OF CMOS INVERTER

Screen shot

LABS STEPS TO GITCLONE VSDSTD CELL DESIGN

COMMANDS TO FOLLOW

#cd dDesktop /work/tools/openlane_working_dir/openlane

#gitclone https://github.com/nickson-jose/vsdstdcelldesign

#cd vsdstdcelldesign

#cp /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign/


#sky130A/libs.tech/magic/sky130A.t

#ls

And this are the process :- 

1.- 

![Screenshot 2025-01-29 210401](https://github.com/user-attachments/assets/75f5f637-40ff-4f81-91eb-831c7f6f89c0)

2.-

![Screenshot 2025-01-29 211424](https://github.com/user-attachments/assets/f15283e2-6918-4c8c-9d82-c52b27da7836)

3.-

![Screenshot 2025-01-29 211447](https://github.com/user-attachments/assets/06d08e46-94ad-473a-b826-c35eeb231805)

4.-

![Screenshot 2025-01-29 211813](https://github.com/user-attachments/assets/68114c74-8c26-47f1-9c8d-be4fb73a3db1)

5.-

![Screenshot 2025-01-29 212210](https://github.com/user-attachments/assets/6fd889eb-0e60-4165-8056-8318982527b4)

6.-

![Screenshot 2025-01-29 215522](https://github.com/user-attachments/assets/d88a4337-a244-4bfc-aace-47f01b462254)

7.-

![Screenshot 2025-01-29 215753](https://github.com/user-attachments/assets/d19d1979-7fd4-4228-ab57-169cc689c3d5)

8.-

![Screenshot 2025-01-29 223032](https://github.com/user-attachments/assets/7609055e-8383-4067-b517-984903d18c76)

9.-

![Screenshot 2025-01-29 223938](https://github.com/user-attachments/assets/7d605990-ca95-4257-b1a7-d4dc74fe3d65)

10.-

![Screenshot 2025-01-29 224016](https://github.com/user-attachments/assets/743fc4ac-e74d-4b0c-a95d-084b59d5452f)

## SKY_L3 Swiching threshold Vm 

Spice analysis - spice cmos 

study spice waveform 

1. SPICE wave form : Wn = 0.375u , WP = 0.9375 , ln , p = 0.25u device [ wn/ln = 1.5 , wp/lp = 3.75 ]

2. SPICE wave form = WN = WP = 0.375u , n , p = 0.25u device [ wn.ln = wp/lp = 1.5 ]

Both are same so it tells us the cmos inverter is a rubest device

![Screenshot 2025-01-30 204851](https://github.com/user-attachments/assets/62d0ac0b-e8d2-46ab-aaf1-ac21f109b6b0)

The parameters which define the rubestnest : 

1. Switching threshold , Vm

   Swiching threshold is a point where Vin the point where Vin = Vout

   ![Screenshot 2025-01-30 205310](https://github.com/user-attachments/assets/e3a3735e-a443-4081-a157-ef25df0f2058)

  The point of switching threshold 

  ![Screenshot 2025-01-30 205310](https://github.com/user-attachments/assets/e4b757d0-c062-4f18-9584-0681e576369c)


 ## Sky130_D3_SK2_L1 create active regions 

  16 mask CMOS process 

1. selecting a substrate [ layout ] most common is p-type

2. Creating active region for transistors , this are buckets of Pmos - Nmos

A - To create isoltion active region ,we can use Sio2 

B - Then deposit potoresist , so we can identify the active regions 

Mask*1 is ready -

mask is any layout

![Screenshot 2025-01-31 220251](https://github.com/user-attachments/assets/da9b6873-5c12-4de0-9512-78bc510f3fb3)

after exposed to UV light the sides or the part not covered by mask gets washed away 

![Screenshot 2025-01-31 220317](https://github.com/user-attachments/assets/ec002ee2-78f2-4398-a1ec-0796c9443822)

C - then remove the mask 

![Screenshot 2025-01-31 220612](https://github.com/user-attachments/assets/48eab084-9b1d-4fb2-b7bf-3595b048491c)

E - then Si3N4 will be etched from other areas 

![Screenshot 2025-01-31 220648](https://github.com/user-attachments/assets/edd13b74-5178-42df-8c22-808f0fe68885)

F - then resisit will be removed 

![Screenshot 2025-01-31 220710](https://github.com/user-attachments/assets/07c00b57-935c-4f52-8a2f-54f122030888)

G - Then it is kept in furnance 

![Screenshot 2025-01-31 220836](https://github.com/user-attachments/assets/ce905aa7-281d-4f99-90d4-ede89dfdcb0c)

the big wooden things are isolation areas , its known as field oxide and the process is LACOS

H - Si3N4 is striped out 

![Screenshot 2025-01-31 221022](https://github.com/user-attachments/assets/54b08d68-61ee-4f8e-8731-43ec242ec7d6)

3. - To create N-well and P-well

![Screenshot 2025-01-30 171443](https://github.com/user-attachments/assets/662c76d7-d446-49b7-9a65-0d5be447c5d8)

![Screenshot 2025-01-30 173119](https://github.com/user-attachments/assets/5ba21fb8-d000-4ee8-8092-af5a07e32754)

![Screenshot 2025-01-30 180744](https://github.com/user-attachments/assets/579eec1f-eded-4323-9ba3-7d40ce9b1565)

![Screenshot 2025-01-30 182406](https://github.com/user-attachments/assets/a01352bc-482f-4b11-8bcf-747cca58ac91)

![Screenshot 2025-01-30 182537](https://github.com/user-attachments/assets/c40e1eea-05e5-4be9-8e06-2625c57d807b)

![Screenshot 2025-01-30 185116](https://github.com/user-attachments/assets/b68bb2f3-d7ad-4dac-b150-538c07a8b1ed)

![Screenshot 2025-01-30 190456](https://github.com/user-attachments/assets/2b056e63-0134-468c-80a4-576280dedcd5)

![Screenshot 2025-01-30 191336](https://github.com/user-attachments/assets/5658ac13-a520-4c97-b056-2f1e7652b08c)

![Screenshot 2025-01-30 191426](https://github.com/user-attachments/assets/dc32c674-ef70-46f2-ad33-0300301fc1ed)

![Screenshot 2025-01-30 193826](https://github.com/user-attachments/assets/697d0699-c490-4162-89d5-42d89c916b3a)

![Screenshot 2025-01-31 113144](https://github.com/user-attachments/assets/f9c87bae-b6b7-4ce7-86c4-93c291f7b0e6)

![Screenshot 2025-01-31 124621](https://github.com/user-attachments/assets/be8c4b87-aa63-4900-9823-8d3059a22780)
 
![Screenshot 2025-01-31 125003](https://github.com/user-attachments/assets/8762ce7f-c9a3-425b-98fa-2b28dd161310)

![Screenshot 2025-01-31 125221](https://github.com/user-attachments/assets/bfd769b7-aabb-4118-95ad-bf735bef2c3c)

![Screenshot 2025-01-31 131151](https://github.com/user-attachments/assets/381fa76c-80d2-4118-bf56-13b0089068f4)
  
![Screenshot 2025-01-31 132944](https://github.com/user-attachments/assets/d164d171-deb2-4aef-a7db-ea358c897b16)
 
![Screenshot 2025-01-31 134022](https://github.com/user-attachments/assets/9fb5f87c-9f88-43d1-b736-33b882c6bc5e)

![Screenshot 2025-01-31 134158](https://github.com/user-attachments/assets/e3961557-b243-4afa-bffa-d31322c0c555)

![Screenshot 2025-01-31 143418](https://github.com/user-attachments/assets/5428ed0c-86ec-40ed-9dfa-636a42b218f7)

![Screenshot 2025-01-31 143556](https://github.com/user-attachments/assets/94582932-684e-4084-bc56-492a0bf4c6eb)

![Screenshot 2025-01-31 160821](https://github.com/user-attachments/assets/f20cffd5-95e9-4980-b443-7ad2655bb1e5)

![Screenshot 2025-01-31 163123](https://github.com/user-attachments/assets/95e10814-ba14-4aa4-9e1f-5c2df842051c)

![Screenshot 2025-01-31 164850](https://github.com/user-attachments/assets/6ffd5e07-5421-4580-9f37-83e169de8bae)

![Screenshot 2025-01-31 165435](https://github.com/user-attachments/assets/c379a3c6-5906-4e09-8d9c-2dc0811c7384)

![Screenshot 2025-01-31 165621](https://github.com/user-attachments/assets/31df7bf3-43a7-479f-85bd-9bb3b796ba91)

![Screenshot 2025-01-31 171728](https://github.com/user-attachments/assets/390d078b-8463-4912-8181-5134f0b4a721)

![Screenshot 2025-01-31 180059](https://github.com/user-attachments/assets/1cb9d072-7db3-4f35-8560-7eb698f202d8)

![Screenshot 2025-01-31 180814](https://github.com/user-attachments/assets/a13758e9-276e-4805-aa69-4553934338fd)

![Screenshot 2025-01-31 180933](https://github.com/user-attachments/assets/456d39de-83d3-49de-9132-31959fec6412)


# Day-4 labs


![Screenshot 2025-01-31 182101](https://github.com/user-attachments/assets/36966f7b-9c77-4587-876d-b89bae06931d)

![Screenshot 2025-01-31 183232](https://github.com/user-attachments/assets/3f29f7f3-be24-4634-9543-cee7c8ae7f99)

![Screenshot 2025-01-31 183358](https://github.com/user-attachments/assets/46f0db82-0bb9-48ca-a393-dea3b7b63ed9)

![Screenshot 2025-01-31 184044](https://github.com/user-attachments/assets/c1c56eac-8367-4d7d-ac28-ec26c196c7fc)

![Screenshot 2025-01-31 184536](https://github.com/user-attachments/assets/0c31cb53-0567-4f20-a903-172b8354fa04)

![Screenshot 2025-01-31 184935](https://github.com/user-attachments/assets/e0231ce9-57b6-485b-a5bc-b1aee7629e65)

![Screenshot 2025-01-31 185547](https://github.com/user-attachments/assets/5c8b620d-220e-469c-b63e-6a19835107f9)

![Screenshot 2025-01-31 185636](https://github.com/user-attachments/assets/ea9beb0a-8161-4b63-abb4-4812dc84c83d)
   
![Screenshot 2025-01-31 185800](https://github.com/user-attachments/assets/2ab574b2-846b-464d-9806-3459240ab521)

![Screenshot 2025-01-31 192107](https://github.com/user-attachments/assets/93441123-0a5d-45e3-95ea-720fe43a635e)

![Screenshot 2025-01-31 192238](https://github.com/user-attachments/assets/8a28f238-b7ca-44f7-8973-50495f8735d0)

![Screenshot 2025-01-31 192752](https://github.com/user-attachments/assets/8fe0f85c-c346-401a-80af-75469ba2c694)

![Screenshot 2025-01-31 193449](https://github.com/user-attachments/assets/6754e7e6-ddff-4674-9d44-8e4a4e606d62)
   
![Screenshot 2025-01-31 193532](https://github.com/user-attachments/assets/a12ef9c5-831d-4c19-a704-9a62ee7bae79)

![Screenshot 2025-01-31 195231](https://github.com/user-attachments/assets/f2fc97f4-e953-4bcb-b6c0-065a7676db22)

![Screenshot 2025-02-01 063911](https://github.com/user-attachments/assets/40adde5e-8990-4f13-bd3e-cdf999cd1c73)

![Screenshot 2025-02-01 064249](https://github.com/user-attachments/assets/b704f875-bcc4-4ed9-bcc1-35abaf4e4578)

![Screenshot 2025-02-01 065416](https://github.com/user-attachments/assets/9d7b5c21-6ffd-416e-a13e-e87747be7686)

![Screenshot 2025-02-01 070252](https://github.com/user-attachments/assets/efbc382b-3b9e-4380-aeab-89787bb964b7)

![Screenshot 2025-02-01 070815](https://github.com/user-attachments/assets/da9d2e6e-451d-47bb-ad46-187c3b720f05)

![Screenshot 2025-02-01 071629](https://github.com/user-attachments/assets/e645121e-5fe9-48c4-a3c3-0e9f427f7f94)

![Screenshot 2025-02-01 071651](https://github.com/user-attachments/assets/f30abd74-f2cb-4b0f-9b63-08fbab7cf77c)

![Screenshot 2025-02-01 102255](https://github.com/user-attachments/assets/1f807db3-cf3e-461b-800f-10464b60b094)

![Screenshot 2025-02-01 103355](https://github.com/user-attachments/assets/8b0e9b84-2502-4aef-8fb1-7fa8b9bba8cb)

![Screenshot 2025-02-01 104604](https://github.com/user-attachments/assets/ae1810d6-d505-4193-ac17-0dd4b0c92d4c)

![Screenshot 2025-02-01 140357](https://github.com/user-attachments/assets/bff08a35-9934-4261-82a6-e3e55f3adf20)

![Screenshot 2025-02-01 144000](https://github.com/user-attachments/assets/35ea6494-4a79-4c75-835b-9f042beca888)

![Screenshot 2025-02-01 145623](https://github.com/user-attachments/assets/c46c6698-05dd-44ef-b59e-0a3a8d097669)

![Screenshot 2025-02-01 151618](https://github.com/user-attachments/assets/1a7f9ce8-3038-47fa-94a2-420e694da118)

![Screenshot 2025-02-01 152055](https://github.com/user-attachments/assets/ae0d5b07-9089-47cf-ab76-04f991981d75)

![Screenshot 2025-02-01 152216](https://github.com/user-attachments/assets/47c065b9-9f0c-4cf0-a8f8-ea964a7d5747)

![Screenshot 2025-02-01 152434](https://github.com/user-attachments/assets/bacb856f-64f3-429b-ad50-e3fe697747f9)

![Screenshot 2025-02-01 152724](https://github.com/user-attachments/assets/321eda90-61db-4898-996f-0ca864570a06)

![Screenshot 2025-02-01 152800](https://github.com/user-attachments/assets/2d4cbce9-7f36-4e3a-b92e-4b5c6d7c37ff)

![Screenshot 2025-02-01 160044](https://github.com/user-attachments/assets/b5966009-a15e-4772-a835-e71a25769862)

![Screenshot 2025-02-01 161236](https://github.com/user-attachments/assets/1fbf090f-50df-4248-acb7-0322d2815d44)

![Screenshot 2025-02-01 161412](https://github.com/user-attachments/assets/375d1d10-fbd9-41e5-a583-9b663f8d1b8a)

![Screenshot 2025-02-01 162136](https://github.com/user-attachments/assets/009d07a8-4a71-483f-8cb6-e1ba110468f7)

![Screenshot 2025-02-01 162306](https://github.com/user-attachments/assets/c617adca-2e10-482d-bc88-0659bb5ed12f)

![Screenshot 2025-02-01 170059](https://github.com/user-attachments/assets/409c8f54-9b2d-4480-89a4-e3b72aabd44a)

![Screenshot 2025-02-01 221203](https://github.com/user-attachments/assets/37de8221-21b1-4dd7-9073-7eba4a659b14)

![Screenshot 2025-02-01 221440](https://github.com/user-attachments/assets/69485384-a315-43f3-82f5-9b5f06855e89)

![Screenshot 2025-02-01 230421](https://github.com/user-attachments/assets/e475d0fa-3d66-4638-aa7a-d92428d772e6)

![Screenshot 2025-02-01 232115](https://github.com/user-attachments/assets/6ddfeece-a511-4962-b5c4-c149b447d842)







   




   



















