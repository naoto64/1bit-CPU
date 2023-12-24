# 1bit-CPU
1bit CPU using 74HC series logic IC.

## Overview
This is a 1bit CPU KiCad file.
You can make a CPU using the 74HC series logic IC.

## Circuit Diagram
![1bit-cpu.jpg](./docs/img/schematic.jpg)

## Description
Left switch: Controls MUX to choose whether to update Reg A or PC
Right switch: Controls second XOR operand or sets destination PC address

LR
00: MUX=0, RA=RA^0=RA,  PC=!PC
01: MUX=0, RA=RA^1=!RA, PC=!PC
10: MUX=1, RA=RA,       PC=0
11: MUX=1, RA=RA,       PC=1

In regular words:  
OFF, OFF will preserve the value of A and advance PC (0->1, 1->0)  
OFF, ON will invert the value of A (0->1, 1->0) and advance PC (0->1, 1->0)  
ON, OFF will preserve the value of A and set PC to 0  
ON, ON will preserve the value of A and set PC to 1  

## Video
[![1bit-CPU](https://img.youtube.com/vi/7_g6IDrb5PI/0.jpg)](https://www.youtube.com/watch?v=7_g6IDrb5PI)
