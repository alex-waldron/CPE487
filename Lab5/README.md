# Lab 5: DAC Siren

Program the FPGA on the Nexys A7-100T board to generate a wailing audio siren using a 24-bit [digital-to-analog converter](https://en.wikipedia.org/wiki/Digital-to-analog_converter) (DAC) called Pmod I2S ([Inter-IC Sound](https://en.wikipedia.org/wiki/I%C2%B2S)) to the top six pins of the Pmod port JA (See Section 10 of the [Reference Manual](https://reference.digilentinc.com/_media/reference/programmable-logic/nexys-a7/nexys-a7_rm.pdf))

### 1. Create a new RTL project _siren_ in Vivado Quick Start

* Create four new source files of file type VHDL called **_dac_if_**, **_tone_**, **_wail_**, and **_siren_**

* Create a new constraint file of file type XDC called **_siren_**

* Choose Nexys A7-100T board for the project

* Click 'Finish'

* Click design sources and copy the VHDL code from dac_if.vhd, tone.vhd, wail.vhd, siren.vhd

* Click constraints and copy the code from siren.xdc

### 2. Run synthesis

### 3. Run implementation and open implemented design

![Implementation](/implementation.PNG)


### 4. Generate bitstream, open hardware manager, and program device

* Click 'Generate Bitstream'

* Click 'Open Hardware Manager' and click 'Open Target' then 'Auto Connect'

* Click 'Program Device' then xc7a100t_0 to download siren.bit to the Nexys A7-100T board

### 5. Edit code with the following [modifications](https://github.com/kevinwlu/dsd/tree/master/Nexys-A7/Lab-5/Modifications)

#### A) Change the upper and lower tone limits

* Modify the tone module to create a square wave instead of a triangle wave when the upper push button (BTNU) is depressed

* Add this push button as an input to siren.vhd and pass its value down to the tone module

* Get the correct pin number for this push button from the Reference Manual

* Note the difference in the quality of the tone when switching to a square wave tone

#### B) Change the wailing speed

* Use the eight slide switches (SW0-SW7) on the Nexys A7-100T board to set the wailing speed

* Add these as inputs to siren.vhd

* Get the correct pin numbers for these switches from the Reference Manual

#### C) Add a second wail instance to drive the right audio channel

* Use different high and low tone limits and wailing speed for the right audio channel

### 6. Close project

* File > Close Project
