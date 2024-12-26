
#  4 BIT- ARIHMETIC AND LOGICAL UNIT (ALU) 





## Overview

 This is a 4 bit ALU made in NI Multisim that does Addition, Subtraction as well as bit wise logical operations(AND, OR, XOR) of two 4 bit binary number.



## Documentation

This ALU has two units, one is the Arithmetic Unit and othe ris a Logical unit.

- The **Arithmetic Unit** is responsible for the addition and subtraction of two 4 bit numbers based on the value of the select line M. M is set to 0 for addition and 1 for subtraction.   

   **Note** : The result shown in 7 segment display, in case of subtraction, is the actual result of the differnce if the borrow bit is 1 (i.e the result is a positive number). if the borrow bit is 0 then the result is the 2's complement in binary.

- The Arithmetic unit (AU) is made of 4 full adders connected to a select line M (for mode input).

- The **Logical Unit** does bitwise logical operations such as AND, OR, XOR of two 4 bit binary numbers. Based on the selec lines s1*s0 combinations different modes can be chosen.
  
| s1*s0 | MODE   |
|:-----:|:------:|
|00     |DISABLED|
|01     |AND     |
|10     |OR      |
|11     |XOR     |

- The logical unit is comprised of four 4x1 MUX wher for each MUX  the 0th input line is grounded and 1st, 2nd and 3rd input is connected to AND, OR , XOR gate respectively for each bits for number A and B.

- At the end the output fo each bit is connected to a 2x1 MUX and according to the select lines (M, S1, S0), it allows to pass the addition/subtraction or logical operation results to the 7 seg display and also the four probes for 4 bits.
   
   **Note**: The OR gate at the select lines of the logical input is put so that the it is 0 when the select lines are both 0(to make the select line of 2x1 MUXs non zero if any one of s1,s0 is non zero). This output is the select line for all the four 2x1 MUX. This ensures that the output will be of AU when s1,s0 = 0,0. else the outpu will be according to the logical unit.




## Project Circuit

![4 bit ALU](https://github.com/Yashraj-Debnath/ALU-in-multisim/blob/main/Screenshot%202024-12-26%20195809.png?raw=true)

