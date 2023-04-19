# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
 
 
 
## Equipments Required:
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'
 

## Logic Diagram

![image](https://user-images.githubusercontent.com/113497104/233025109-6356c1f2-35f0-48d6-b1fb-f62c1bab5bd5.png)

## Procedure

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:
```
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using 
Verilog programming.

Developed by: SHARANGINI T K
RegisterNumber: 212222230143


Using NAND gates:

module NAND(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P=(~(~C & B & A));
assign Q=(~(~D & C & A));
assign R=(~(C & ~B & A));
assign F=~(P & Q & R);
endmodule

Using NOR gates:

module NOR(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = (C & ~B & A);
assign Q = (D & ~C & A);
assign R = (C & ~B & A);
assign S = (~(P | Q | R));
assign F = (~S);
endmodule
```
## RTL realization
## Output:
## NAND combination
![image](https://user-images.githubusercontent.com/113497104/233026055-d6d4233c-98b3-417e-be09-c5ad704ccd44.png)

## NOR combination
![image](https://user-images.githubusercontent.com/113497104/233026231-d21ea7b0-1a73-4737-b718-3957bd2aba6c.png)

## Timing Diagram

## NAND combination
![image](https://user-images.githubusercontent.com/113497104/233026561-8d4acd99-4672-435c-a796-1db1f49e0b85.png)

## NOR combination
![image](https://user-images.githubusercontent.com/113497104/233030131-20094862-4cc5-4170-8cce-f8e67f97644d.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
