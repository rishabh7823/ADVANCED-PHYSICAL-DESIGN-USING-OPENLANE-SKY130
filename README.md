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






















   




   



















