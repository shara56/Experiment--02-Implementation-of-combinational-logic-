# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
## Equipments Required:
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Procedure
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output(RTL Viewer and Timing Diagram) to represent F1 and F2.

5.End the verilog program using keyword endmodule.

## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

Developed by:SHARANGINI T K

RegisterNumber:212222230143

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module exp2f1(A,B,C,D,f1);
input A,B,C,D;
output f1;
assign f1=(~B&~D)|(A&B&~C)|(~A&B&D);
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=(~y&z)|(x&y)|(w&y);
endmodule
```
# RTL realization
## Output:
## RTL

## F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![image](https://github.com/shara56/Experiment--02-Implementation-of-combinational-logic-/assets/113497104/9c1132c7-503a-4bfe-85d5-c571721755de)

## F2=xy’z+x’y’z+w’xy+wx’y+wxy
![image](https://github.com/shara56/Experiment--02-Implementation-of-combinational-logic-/assets/113497104/80df5bcc-54dd-45c1-9111-22ee97548e7c)

## Timing Diagram

## F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![image](https://github.com/shara56/Experiment--02-Implementation-of-combinational-logic-/assets/113497104/bf8f5c48-571d-4d12-9b7a-1c73d97a1d03)

## F2=xy’z+x’y’z+w’xy+wx’y+wxy
![image](https://github.com/shara56/Experiment--02-Implementation-of-combinational-logic-/assets/113497104/1d8879e2-2604-4856-a643-332fa5cf4d5b)

# Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
