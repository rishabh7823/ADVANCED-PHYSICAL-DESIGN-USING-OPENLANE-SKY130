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










 


  
 




  
































   




   



















