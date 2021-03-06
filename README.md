
# Implementation of CMOS based 1-bit Magnitude Comparator in 28nm Technology

## Table of Contents
1. [Abstract](#abstract)
2. [Reference&nbsp;Circuit&nbsp;Details](#ReferenceCircuitDetails)
3. [Reference&nbsp;Circuit&nbsp;Design](#ReferenceCircuitDesign)
4. [Reference&nbsp;Circuit&nbsp;Waveforms](#referencecircuitwaveforms)
5. [Tools&nbsp;used](#toolsused)
6. [Simulation&nbsp;in&nbsp;Synopsys](#simulationinsynopsys)
   - [Pre-Layout&nbsp;Schematics](#pre-layoutschematics)
   - [Parameters&nbsp;set&nbsp;for&nbsp;Voltage&nbsp;Source&nbsp;for&nbsp;Input&nbsp;A](#ParameterssetforVoltageSourceforInputA)
   - [Parameters&nbsp;set&nbsp;for&nbsp;Voltage&nbsp;Source&nbsp;for&nbsp;Input&nbsp;B](#ParameterssetforVoltageSourceforInputB)
   - [Transient&nbsp;Settings](#TransientSettings)
   - [Circuit&nbsp;for&nbsp;testing](#Circuitfortesting)
   - [Output&nbsp;Waveform](#OutputWaveform)
   - [Netlist&nbsp;of&nbsp;the&nbsp;Circuit](#NetlistoftheCircuit)
7. [Conclusion](#Conclusion)
8. [Author](#Author)
9. [Acknowledgement](#Acknowledgement)
10. [References](#References)


## Abstract
This repository presents the Implementation of CMOS based 1-bit Magnitude Comparator in 28nm technology. Design and Implementation is done using Synopsys Custom Design Platform. Data comparison is needed in digital systems while performing arithmetic or logical operations. A single bit magnitude digital comparator is a combinational circuit that compares two digital or binary numbers in order to find out whether one binary number is equal, less than or greater than the other binary number. The complete design implementation is done using CMOS technology which has the features such as low static power consumption, temperature stability and stronger anti-noise ability.

## Reference&nbsp;Circuit&nbsp;Details
A magnitude comparator is a hardware electronic device that takes two numbers as input in binary form and determines whether one number is greater than, less than or equal to the other number. The logical design of a circuit will have two inputs one for A and other for B and have three output terminals, one for A > B condition, one for A = B condition and one for A < B condition.

<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177407-1fd9f887-a852-4734-ab8d-845d96991953.png"
  >
  <br/><b>Fig. 1.	 Block Diagram of 1-bit Magnitude Comparator</b>
</p>

<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177500-81aa4e47-edf3-4c67-bc45-a97c030f9543.png"
  >
  <br/><b>Fig. 2.	 Truth Table of 1-bit Magnitude Comparator</b>
</p>

From the above truth table logical expressions for each output can be expressed as:

- (A=B) = A'B'+AB=(AB'+A'B)'
- (A>B) = AB'=(A'+B)'
- (A<B) = A'B=(A+B')'

By using these Boolean expressions, we can implement a logic circuit for this comparator as:

<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156178244-2b43d6d1-5084-475d-afdb-26279635f087.png"
  >
  <br/><b>Fig. 3.	Gate level Schematic Diagram of 1-bit Magnitude Comparator</b>
</p>

## Reference&nbsp;Circuit&nbsp;Design

<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177538-e9db2923-ffe7-49b3-a9fb-9c4ef614d0ca.PNG"
  >
  <br/> <b>Fig. 4. Reference Circuit Diagram of 1-bit Magnitude Compator using CMOS technology which consists of 10-PMOS4T and 10-NMOS4T transistors</b>
</p>

## Reference&nbsp;Circuit&nbsp;Waveforms
<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177682-f45ef271-d1e1-403b-b774-7929b4abfe83.PNG"
  >
  <br/> 
   <b>Fig. 5. Reference Circuit Output Waveforms</b>
</p>


## Tools&nbsp;used
- ### Synopsys Custom Compiler: 
  The Synopsys Custom Compiler??? design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys   Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the   circuit on a transistor level.

- ### Synopsys Primewave: ???
  PrimeWave??? Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and       memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.

- ### Synopsys 28nm PDK: ???
  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.
  
# Simulation&nbsp;in&nbsp;Synopsys

## Pre-Layout&nbsp;Schematics
Initially Schematic of the 1-bit Magnitude Comparator cell with input and output pins was implemented,then it was converted into a symbol so that it could be used directly as instance cell from the library.

### Schematic Diagram
<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177736-272660c5-57e6-4a4a-b9ee-86036c9801c5.PNG"
  >
  <br/> <b>Fig. 6. Schematic Diagram of 1-bit Magnitude comparator circuit with 10-PMOS4T,10-NMOS4T transistors,Input and Output pins  </b>
</p>

### Symbol
<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177766-58cb046a-aec3-4f4a-9068-032399f72ed0.PNG"
  >
  <br/> <b>Fig. 7. Symbolic representation of Comparator Circuit, which could be used as a instance cell from library </b>
</p>


## Parameters&nbsp;set&nbsp;for&nbsp;Voltage&nbsp;Source&nbsp;of&nbsp;Input&nbsp;A
<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156178099-1e141823-618f-4191-b1c4-e63c03b4b9c8.png"
  >
  <br/> <b>Fig. 8. Parameters of Input A  </b>
</p>

## Parameters&nbsp;set&nbsp;for&nbsp;Voltage&nbsp;Source&nbsp;of&nbsp;Input&nbsp;B
<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156180063-cef91ca9-32a3-4d09-b375-d2768c9712b3.png"
  >
  <br/> <b>Fig. 9. Parameters of B  </b>
</p>


## Transient&nbsp;Settings
<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177927-d60cc500-90f9-4b4c-987d-6341f5f3fcf0.PNG"
  >
  <br/> <b>Fig. 10.Transient settings  </b>
</p>


## Circuit&nbsp;for&nbsp;testing
The Final Schematic of 1-bit magnitude comparator has been implemented using the above created symbol by providing A, B Vpulse with 1.8V supply voltage , Vdc supply and Gnd to the input pins. 
<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177876-2d917aa0-150d-4c84-90e7-76c803af6970.PNG"
  >
  <br/> <b>Fig. 11. 1-bit magnitude comparator circuit for testing </b>
</p>


## Output&nbsp;Waveform
<p align="center">
  <img 
    src="https://user-images.githubusercontent.com/100518323/156177849-62b04390-da4b-45e0-9074-1dbb3bcc08c6.PNG"
  >
  <br/> <b>Fig. 12. Output Waveforms</b>
</p>


## Netlist&nbsp;of&nbsp;the&nbsp;Circuit

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
 Thus,A CMOS based 1-bit Magnitude Comparator circuit has been designed and implemented using Synopsys Custom Design Compiler in 28nm technology and its Output Waveforms 
 has been verified using Synopsys Primewave.
## Author
 Jeyanthi M, BE(Electronics and Communication Engineering), Thiagarajar College of Engineering, Madurai-625051
## Acknowledgement
1. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. - kunalpghosh@gmail.com
2. Chinmay panda, IIT Hyderabad
3. Sameer Durgoji, NIT Karnataka
4. [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
5. [VLSI Custom Design (VSD) Corp. Pvt. Ltd India](https://www.vlsisystemdesign.com/)
6. [Synopsys India](https://www.synopsys.com/)
  
## References
1.Improved Design of CMOS 1-Bit Comparator with Stacking Technique. Arvindkumar, Manoj Kumar. 2017 2nd International Conference on Telecommunication network.
 2.https://www.researchgate.net/publication/303805925_1_Bit_Comparator_CMOS_90nm_Layout_Design#:~:text=The%20comparator%20is%20a%20circuit,analog%2Dto%2Ddigital%20converter

