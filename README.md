# Parallel-coupled-AB-amplifier
The purpose of this Hackathon is to implement the proposed design in 28 nm PDK (Process Design Kit) suing CMOS technology.

As a result of literature survey and Implemantation, this is a final Report Submission for successful completion of Parallel_AB amplifier design and simulation, for Cloud Based Analog IC Design Hackathon
# Table of Contents
1.Introduction
2.Working
3.Schematic results
4.Challanges
5.Limitations
6.REfarences
7.Acknowledgements
8.Author
# Introduction
Power amplifiers (PAs) are among the most crucial functional blocks in the radio frequency (RF) frontend for reliable wireless communication. PAs amplify and boost the input signal to the required output power. The signal is amplified to make it sufficiently high for the transmitter to propagate the required distance to the receiver. Attempted advancements of PA have focused on attaining high-performance RF signals for transmitters. Such PAs are expected to require low power consumption while producing a relatively high output power with a high efficiency. However, current PA designs in nanometer and micrometer complementary metal–oxide semiconductor (CMOS) technology present inevitable drawbacks, such as oxide breakdown and hot electron effect. A well-defined architecture, including a linear and simple functional block synthesis, is critical in designing CMOS PA for various applications.
# Working
In the PA design in CMOS technology, two main issues must be addressed Oxide breakdown and the hot carrier effect. In this design, two amplifiers operate in parallel to improve the dynamic range and power efficiency. The input transistor M1 was biased with a fixed voltage of 1.2 V. The cascode configuration was formed by the CS transistors M1, M2, M3, and M4, and the CG transistors M5 and M6. The CS transistors form the transconductance of the class-A and the class-B PAs in order to provide more linear transconductance, which led to high power gain of 12dB. At low input levels, the class-A amplifier contributed the majority of the gain, and the class B amplifier had a very low gain. As the input level increased, the gain of the class- B amplifier increased, and its contribution to the overall gain increased proportionately. The outputs from both amplifiers were combined in the current domain with a slight overhead, thereby producing an improved isolation property and highpower efficiency of 44%. AC coupling capacitors and the matching network were used for the output impedance matching.
# Refarence Circuit
![refarence circuit](https://user-images.githubusercontent.com/58004631/156006452-41a8d200-e841-4779-b5f0-c598dbb6ed23.png)

# Scimatic Circuit
![scimatic circuit](https://user-images.githubusercontent.com/58004631/156006249-abb9c4ea-f09e-4bab-8d9b-8b12a78e3c74.png)

# Waveform
![waveform](https://user-images.githubusercontent.com/58004631/156006443-d193e5b8-229c-4fce-b328-0a478756260f.png)




# Scimatic result
  Generated for: PrimeSim
*  Design library name: lib_1
*  Design cell name: r_amp
*  Design view name: schematic
.include '/home/rakeshreddykunduru24/Desktop/analog/cp_lib1/cp_inp/defs.lib'

*Custom Compiler Version S-2021.09
*Mon Feb 28 14:11:16 2022

.global gnd!
********************************************************************************
* Library          : lib_1
* Cell             : r_amp
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xm20 net32 net113 gnd! gnd! n105 w=0.1u l=30n nf=1 m=1
xm19 net32 net45 gnd! gnd! n105 w=0.1u l=30n nf=1 m=1
xm18 net53 net109 net32 gnd! n105 w=0.1u l=30n nf=1 m=1
xm2 net4 net103 gnd! gnd! n105 w=0.1u l=30n nf=1 m=1
xm1 net4 net100 gnd! gnd! n105 w=0.1u l=30n nf=1 m=1
xm0 net21 net99 net4 gnd! n105 w=0.1u l=30n nf=1 m=1
r39 net113 gnd! r=12.5k
r38 net103 gnd! r=12.5k
r25 net45 net113 r=25k
r24 net109 net45 r=25k
r26 net99 net100 r=25k
r51 net100 net103 r=12.5k
c44 gnd! net80 c=0.0001256
c43 gnd! net78 c=0.0001256
c42 net78 net21 c=0.25u
c41 net80 net53 c=0.25u
c31 net109 net107 c=0.25u
c32 net45 net107 c=0.25u
c33 net113 net107 c=0.25u
c34 net103 net97 c=0.25u
c35 net100 net97 c=0.25u
c36 net99 net97 c=0.25u
v53 net116 gnd! dc=10
v40 net107 gnd! dc=0 sin ( 0 3 1k 0 0 0 )
v9 net97 gnd! dc=0 sin ( 0 3 1k 0 0 0 )
l46 net80 gnd! l=0.0001256
l45 net78 gnd! l=0.0001256
l29 net116 net53 l=0.0001256
l28 net116 net109 l=0.0001256
l14 net116 net99 l=0.0001256
l15 net116 net21 l=0.0001256








.tran '1u' '20u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(net78) v(net80)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end

# Challanges
. The real challange is to adjust W/L ratio of pMos and nMos such that both have approximately equal rise and fall time.

# Limitations
The efficiency of the class AB power Amplifiers are low.

# Refarences
Design Architectures of the CMOS Power Amplifier for 2.4 GHz ISM Band Applications:
1. Electrical and Electronics Engineering, Xiamen University Malaysia, Bandar Sunsuria, Sepang 43900, Selangor, Malaysia. 
2. Electronic and Telecommunication Engineering, RMIT University, Melbourne, VIC 3000, Australia.
3. Electrical, Electronic and Systems Engineering, Universiti Kebangsaan Malaysia, Bangi 43600, Selangor, Malaysia.

# Acknowledgements
Kunal Ghosh, Founder, VSD Corp. Pvt. Ltd
Indian Institute Of Technology (IIT), Hyderabad
Synopsys

# Author
K.Rakesh Reddy,Bachelor of Technology in Electronics and Communication Engineering



