# Final Project - Crossy Road
FPGA remake of the popular mobile game crossy road
Modeled off of Lab 3 - Bouncing Ball

## Project Research
After completing some research on the project and previous projects, I found that crossy road is essentially frogger with the ability to move side to side along with up and done

## Project Template
To get a start for the project, I cloned a previous frogger project from Corey Benson of Spring 2022

## Execution
1. Clone the repo, get the environment set up for changes

    * ## NOTE FOR FUTURE ISSUES: 
        * If someone is having problems with vivado getting stuck at "initializing language server" and then the project becomes unresponsive, a resolution to the problem is to change the option "Tools -> Settings -> Tool Settings -> Text Editor -> Syntax Checking -> Syntax checking" from Sigasi to Vivado, then restart Vivado. Hopefully this can save someone the days i spent trying to figure this out

2. Map BTNL to move the player to the left and map BTNR to move the player to the right
3. Run synthesis

4. Run implementation and open implemented design

![Schem](./implementation.PNG)

5. Generate bitstream, open hardware manager, and program device

    * Click 'Generate Bitstream'

    * Click 'Open Hardware Manager' and click 'Open Target' then 'Auto Connect'

    * Click 'Program Device' then xc7a100t_0 to download vga_top.bit to the Nexys A7 board
6. Play the game

    * BTNC resets the game
    * BTNU moves the player up
    * BTND moves the player down
    * BTNL moves the player left
    * BTNR moves the player right
    * Counter lets you know the number of successful trips
    * Counter will reset if killed

![Vid](./DSD_final_proj_vid.gif)

    
7. Close project

    * File > Close Project