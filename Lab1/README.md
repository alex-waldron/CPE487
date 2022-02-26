# Lab 1: Seven-Segment Decoder

* Built a single-digit (4-bit) hex counter to display its value on eight-digit common anode seven-segment LED displays (See Section 9.1 Seven-Segment Display of the [Reference Manual]( https://reference.digilentinc.com/_media/reference/programmable-logic/nexys-a7/nexys-a7_rm.pdf))

![a7.png](https://github.com/kevinwlu/dsd/blob/master/Nexys-A7/Lab-1/a7.png)

![7s.png](https://github.com/kevinwlu/dsd/blob/master/Nexys-A7/Lab-1/7s.png)

* A '0' on the cathode turns a segment on

| Four-Bit Input | Hex Digit | LED Segment Code CA-CG |
| :---: | :---: | :---: |
| 0000 | 0 | 0000001 |
| 0001 | 1 | 1001111 |
| 0010 | 2 | 0010010 |
| 0011 | 3 | 0000110 |
| 0100 | 4 | 1001100 |
| 0101 | 5 | 0100100 |
| 0110 | 6 | 0100000 |
| 0111 | 7 | 0001111 |
| 1000 | 8 | 0000000 |
| 1001 | 9 | 0000100 |
| 1010 | A | 0001000 |
| 1011 | b | 1100000 |
| 1100 | C | 0110001 |
| 1101 | d | 1000010 |
| 1110 | E | 0110000 |
| 1111 | F | 0111000 |


* Slide switches 13, 14, and 15 to determine which display is illuminated (see [modifications](https://github.com/kevinwlu/dsd/tree/master/Nexys-A7/Lab-1/Modifications))


![img_2022](./IMG_2022.gif)


* Slide switches 0, 1, 2, and 3 to display the value of 4-bit hex digit from 0 to F


![img_2023](./IMG_2023.gif)


* Slide only one switch at a time to display the [Gray code](https://en.wikipedia.org/wiki/Gray_code) from 0 to F, i.e., 0-1-3-2-6-7-5-4-C-d-F-E-A-b-9-8


![img_2024](./IMG_2024.gif)

