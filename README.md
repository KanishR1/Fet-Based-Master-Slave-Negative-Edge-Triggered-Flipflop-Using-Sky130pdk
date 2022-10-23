# Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk
This repository has been created for the circuit simulation project in eSim

## Table of Contents
- [Circuit Details](#circuit-details)
- [Software Used](#software-used)
  * [eSim](#esim)
  * [NgSpice](#ngspice)
- [Circuit Diagram in eSim](#circuit-diagram-in-esim)
- [Netlists](#netlists)
- [NgSpice Plots](#ngspice-plots)
- [GAW Plot](#gaw-plot)
- [Steps to run this project](#steps-to-run-this-project)
- [Acknowlegdements](#acknowlegdements)
- [References](#references)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## Circuit Details
A negative-edge triggered D type master-slave flip-flop consists of a pair of D-latches, positive latch (master) and negative latch (slave) connected in series. The latches are designed using mux by giving feedback from output to one of the inputs of 2:1 mux in. The mux is constructed using the transmission gates. The transmission gate is a bidirectional circuit which is made by connecting the pfet and nfet in parallel. The clock is given to the select lines of the mux so that the entire circuit behaves as the master slave negative edge triggered flipflop. During the high level of the clock, the master samples the input and the slave retains the previous output through feedback. At low level of the clock, the slave will go to transparent mode and samples the output of the master and the master will go to the hold mode, retaining the previous value. Thus, the output of master slave negative edge triggered flipflop changes once in one clock cycle during the high to low transition of clock. The transistors for desi

## Software Used
### eSim
It is an Open Source EDA developed by FOSSEE, IIT Bombay. It is used for electronic circuit simulation. It is made by the combination of two software namely NgSpice and KiCAD.
</br>
For more details refer:
</br>
https://esim.fossee.in/home

### NgSpice
It is an Open Source Software for Spice Simulations. For more details refer:
</br>
http://ngspice.sourceforge.net/docs.html

## Circuit Diagram in eSim
The following is the schematic in drawn in eSim:
**Power Supply**
![power_supply](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/schematic/power_supply.png)

**Clock Circuit**
![clock_circuit](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/schematic/clock_circuit.png)

**Input Data**
![input_data](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/schematic/input_data.png)

**Master Slave Negative Edge Flipflop Using SKY130PDK**
![schematic](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/schematic/schematic.png)




## Netlists
The following figure show the contents in the ms_ff.cir.out : 

![netlist](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/outputs/netlist.png)</br>


## NgSpice Plots

The following waveforms are the ngspice plots for the designed circuit :

**Clk Signal**

![Clk](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/outputs/Clk.png)

**Clk_bar Signal**

![Clk_bar](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/outputs/Clk_bar.png)

**Input Data (D) **
![D](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/outputs/D.png)

**Master Output (Qm)**
![Qm](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/outputs/Qm.png)

**Output (Q)**
![Q](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/outputs/Q.png)


**Combined Waveform** </br>

![Combined_Waveform](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/outputs/Combined_Waveform.png)

## GAW Plot

![gaw_waveform](https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk/blob/main/outputs/gaw_waveform.png)

## Steps to run this project
1. Open a new terminal
2. Clone this project using the following command:</br>
```git clone https://github.com/KanishR1/Fet-Based-Master-Slave-Negative-Edge-Triggered-Flipflop-Using-Sky130pdk.git ```</br>
3. Change directory:</br>
```cd ms_ff ```</br>
4. Run ngspice:</br>
```ngspice ms_ff.cir.out```</br>
5. To run the project in eSim:

  - Run eSim</br>
  - Load the project</br>
  - Open eeSchema</br>

## Acknowlegdements
1. FOSSEE, IIT Bombay

## References
1. Morris Mano & Michael D Ciletti, “Digital Design: With an Introduction to Verilog HDL, 5th Edition, Pearson Education, 2013
2. Neil H.E. Weste, David Money Harris ―CMOS VLSI Design: A Circuits and Systems Perspective.
3. https://www.sciencedirect.com/topics/computer-science/master-slave-flip#:~:text=A%20negative%2Dedge%20triggered%20D,edge%20of%20the%20clock%20pulse.
4. https://skywater-pdk.readthedocs.io/en/main/

