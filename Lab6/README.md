# Lab 6: Video Game PONG

* Extend the FPGA code developed in Lab 3 (Bouncing Ball) to build a PONG game using a 5k&Omega; potentiometer with a 12-bit [analog-to-digital converter](https://en.wikipedia.org/wiki/Analog-to-digital_converter) (ADC) called [Pmod AD1](https://store.digilentinc.com/pmod-ad1-two-12-bit-a-d-inputs/) connected to the top pins of the Pmod port JA (See Section 10 of the [Reference Manual](https://reference.digilentinc.com/_media/reference/programmable-logic/nexys-a7/nexys-a7_rm.pdf))

### 1. Create a new RTL project _pong_ in Vivado Quick Start

* Create six new source files of file type VHDL called **_clk_wiz_0_**, **_clk_wiz_0_clk_wiz_**, **_vga_sync_**, **_bat_n_ball_**, **_adc_if_**, and **_pong_**

  * clk_wiz_0.vhd and clk_wiz_0_clk_wiz.vhd are the same files as in Lab 3
  
  * vga_sync.vhd, bat_n_ball.vhd, adc_if.vhd, and pong.vhd are new files for Lab 6

* Create a new constraint file of file type XDC called **_pong_**

* Choose Nexys A7-100T board for the project

* Click 'Finish'

* Click design sources and copy the VHDL code from clk_wiz_0, clk_wiz_0_clk_wiz, vga_sync.vhd, bat_n_ball.vhd, adc_if.vhd, pong.vhd

* Click constraints and copy the code from pong.xdc

### 2. Run synthesis

### 3. Run implementation and open implemented design
![Schem](./implementation.PNG)

### 4. Generate bitstream, open hardware manager, and program device

![Vid](./IMG_2121.gif)

* Click 'Generate Bitstream'

* Click 'Open Hardware Manager' and click 'Open Target' then 'Auto Connect'

* Click 'Program Device' then xc7a100t_0 to download pong.bit to the Nexys A7-100T board

* Push BTNC to start the bouncing ball and use the bat to keep the ball in play

### 5. Edit code with the following [modifications](https://github.com/kevinwlu/dsd/tree/master/Nexys-A7/Lab-6/Modifications)

![Vid1](./IMG_2122.gif)

#### A) Change ball speed

* The ball speed is currently 6 pixels per video frame

* Use the slide switches on the Nexys A7-100T board to program the ball speed in the range of 1-32 pixels per frame

  * **WARNING: Avoid setting the speed to zero as the ball will then never reach the bat or wall**

* See how fast to move the ball and still keep it in play

#### B) Change bat width and count hits

* Double the width of the bat to make the game really easy

* Modify the code so that the bat width decreases one pixel each time successfully hitting the ball and then resets to
starting width when missing the ball

* See how many times hitting the ball in a row as the bat slowly shrinks

* Count the number of successful hits after each serve and display the count in binary on the 7-segment displays of the Nexys A7-100T board

### 6. Close project

* File > Close Project