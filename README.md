# 1-bit-Magnitude-Comparator
This repository presents the Design and Implementation of 1-bit Magnitude Comparator using Synopsis custom Design Compiler on 28nm CMOS Technology .

# Implementation of CMOS based 1-bit Magnitude Comparator using 28nm Technology


## Table of Contents
1. [Abstract](#abstract)
2. [Reference Circuit Details](#referencecircuitdetails)
3. [Reference Circuit Design](#ReferenceCircuitDesign)
4. [Reference Circuit Waveforms](#referencecircuitwaveforms)
5. [Tools used](#toolsused)
6. [Simulation in Synopsys](#simulationinsynopsys)
   - [Pre-Layout Schematics](#pre-layoutschematics)
   - [Parameters set for Voltage Source for Input A](#ParameterssetforVoltageSourceforInputA)
   - [Parameters set for Voltage Source for Input B](#ParameterssetforVoltageSourceforInputB)
   - [Transient Settings](#TransientSettings)
   - [1-bit Magnitude Comparator Circuit for testing](#1-bitMagnitudeComparatorCircuitfortesting)
   - [Netlist of the Circuit](#NetlistoftheCircuit)
   - [Output Waveform](#OutputWaveform)
7. [Conclusion](#Conclusion)
8. [Author](#Author)
9. [Acknowledgement](#Acknowledgement)
10. [References](#References)




## Abstract

This repository presents the Implementation of CMOS based 1-bit Magnitude Comparator in 28nm technology. Design and Implementation will be done using Synopsys Custom Design Platform. Data comparison is needed in digital systems while performing arithmetic or logical operations. A single bit magnitude digital comparator is a combinational circuit that compares two digital or binary numbers in order to find out whether one binary number is equal, less than or greater than the other binary number. The complete design implementation is done using CMOS technology which has the features such as low static power consumption, temperature stability and stronger anti-noise ability.

## Reference Circuit Details

A magnitude comparator is a hardware electronic device that takes two numbers as input in binary form and determines whether one number is greater than, less than or equal to the other number. The logical design of a circuit will have two inputs one for A and other for B and have three output terminals, one for A > B condition, one for A = B condition and one for A < B condition.

![Block diagram](https://user-images.githubusercontent.com/100518323/156031063-23d96f5b-74d6-4a53-8c6e-b104bd2581d9.png)

Fig 1. Block Diagram

![Truth table](https://user-images.githubusercontent.com/100518323/156031204-a6603e4e-3cc0-4912-91f6-f8e7227ed732.png)




From the above truth table logical expressions for each output can be expressed as:

- (A=B) = A'B'+AB=(AB'+A'B)'
- (A>B) = AB'=(A'+B)'
- (A<B) = A'B=(A+B')'

By using these Boolean expressions, we can implement a logic circuit for this comparator as:

![combinational circuit](https://user-images.githubusercontent.com/100518323/156031116-65157d87-4a90-480b-ab18-0ae09d9900fe.png)

Fig 3. Combinational Circuit

## Reference Circuit Design

![ref circuit](https://user-images.githubusercontent.com/100518323/156031931-ca3e359b-52bf-4fc9-bb2f-42b7045f3f60.PNG)

## Reference Circuit Waveforms

![ref waveform](https://user-images.githubusercontent.com/100518323/156032320-b69c7c1a-5e76-404e-bfa1-982b53c0f014.PNG)

## Tools used
## Simulation in Synopsys
## Pre-Layout Schematics

![comparator schematic](https://user-images.githubusercontent.com/100518323/156026811-2769a02d-b2e6-4bc7-98d7-1bd047b4c20c.PNG)


![Comparator Symbol](https://user-images.githubusercontent.com/100518323/156026985-2bfca537-217f-492a-a4cf-a74290ca48f9.PNG)

## Parameters set for Voltage Source for Input A

![A input](https://user-images.githubusercontent.com/100518323/156028514-217740b5-ad6a-4809-8a3e-04774d1b1568.png)

## Parameters set for Voltage Source for Input B

![B input](https://user-images.githubusercontent.com/100518323/156029747-6db07c50-8537-45a4-b94e-568089c27122.png)

## Transient Settings

![Transiant Analysis](https://user-images.githubusercontent.com/100518323/156026726-92e26efb-836d-423b-9236-877c0632e562.PNG)

## 1-bit Magnitude Comparator Circuit for testing

![Circuit for testing](https://user-images.githubusercontent.com/100518323/156026435-d4cbe864-0e45-40b2-b0ef-21831c8e7918.PNG)

## Output Waveform

![OutputWaveforms](https://user-images.githubusercontent.com/100518323/155940267-744ff2c9-53d7-4152-bf77-68dfbdff9b0c.PNG)

## Netlist of the Circuit

```

*  Generated for: PrimeSim
*  Design library name: cp_lib1
*  Design cell name: cp_comparator_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Mon Feb 28 07:34:20 2022

.global gnd!
********************************************************************************
* Library          : cp_lib1
* Cell             : cp_comp
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt cp_comp a_input b_input vdd_equal vdd_greater vdd_in vdd_lesser
+ vout_equal vout_greater vout_lesser vss vss_equal vss_in
xm35 vss net60 vout_lesser vss n105 w=0.1u l=0.03u nf=1 m=1
xm30 vss b_input vout_greater vss n105 w=0.1u l=0.03u nf=1 m=1
xm36 vout_lesser a_input vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm28 vout_greater net26 vss vss n105 w=0.1u l=0.03u nf=1 m=1
xm14 net60 b_input vss_in vss_in n105 w=0.1u l=0.03u nf=1 m=1
xm5 net20 a_input vout_equal vss_equal n105 w=0.1u l=0.03u nf=1 m=1
xm4 vss_equal net60 net20 vss_equal n105 w=0.1u l=0.03u nf=1 m=1
xm3 vout_equal net26 net14 vss_equal n105 w=0.1u l=0.03u nf=1 m=1
xm2 net14 b_input vss_equal vss_equal n105 w=0.1u l=0.03u nf=1 m=1
xm11 net26 a_input vss_in vdd_in n105 w=0.1u l=0.03u nf=1 m=1
xm24 net108 net26 vdd_greater vdd_greater p105 w=0.1u l=0.03u nf=1 m=1
xm25 vout_greater b_input net108 vdd_greater p105 w=0.1u l=0.03u nf=1 m=1
xm26 net116 a_input vdd_lesser vdd_lesser p105 w=0.1u l=0.03u nf=1 m=1
xm27 vout_lesser net60 net116 vdd_lesser p105 w=0.1u l=0.03u nf=1 m=1
xm13 net60 b_input vdd_in vss_in p105 w=0.1u l=0.03u nf=1 m=1
xm10 net76 net26 vdd_equal vdd_equal p105 w=0.1u l=0.03u nf=1 m=1
xm9 vdd_equal b_input net76 vdd_equal p105 w=0.1u l=0.03u nf=1 m=1
xm8 net76 net60 vout_equal vdd_equal p105 w=0.1u l=0.03u nf=1 m=1
xm12 vout_equal a_input net76 vdd_equal p105 w=0.1u l=0.03u nf=1 m=1
xm6 net26 a_input vdd_in vdd_in p105 w=0.1u l=0.03u nf=1 m=1
.ends cp_comp

********************************************************************************
* Library          : cp_lib1
* Cell             : cp_comparator_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 a_in b_in net28 net30 net26 net24 a_equal_b a_greater_b a_lesser_b gnd! gnd!
+ gnd! cp_comp
v2 b_in gnd! dc=0 pulse ( 0 1.8 0 0.1u 0.1u 4u 8u )
v1 a_in gnd! dc=0 pulse ( 0 1.8 0 0.1u 0.1u 5u 10u )
c12 a_lesser_b gnd! c=1p
c11 a_greater_b gnd! c=1p
c10 a_equal_b gnd! c=1p
v16 net30 gnd! dc=1.08
v15 net28 gnd! dc=1.08
v14 net26 gnd! dc=0.8
v13 net24 gnd! dc=0.9








.tran '1u' '20u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(a_equal_b) v(a_greater_b) v(a_in) v(a_lesser_b) v(b_in)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end
```
## Conclusion
## Author
## Acknowledgement
  1. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalpghosh@gmail.com
  2. Chinmay panda, IIT Hyderabad
  3. Sameer Durgoji, NIT Karnataka
  4. [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
  5. [VLSI Custom Design (VSD) Corp. Pvt. Ltd India](https://www.vlsisystemdesign.com/)
  6. [Synopsys India](https://www.synopsys.com/)
## References
  1.Improved Design of CMOS 1-Bit Comparator with Stacking Technique. Arvindkumar, Manoj Kumar. 2017 2nd International Conference on Telecommunication network.
  2.https://www.researchgate.net/publication/303805925_1_Bit_Comparator_CMOS_90nm_Layout_Design#:~:text=The%20comparator%20is%20a%20circuit,analog%2Dto%2Ddigital%20converter.




