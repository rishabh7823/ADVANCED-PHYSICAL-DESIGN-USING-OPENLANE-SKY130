


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













































   




   



















