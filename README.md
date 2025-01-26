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

   



















