# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodule.

Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: ADHITHIYAN.K
RegisterNumber:  212222230006
*/
### Half Subtractor Program:
module HalfSubtractor(A,B,Difference,Borrow);
input A,B;
output Difference,Borrow;
assign Difference = (A ^ B);
assign Borrow = (~A & B);
endmodule

### Full Subtractor Program:
module FullSubtractor(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (~A &(B ^ C) | (B & C));
assign Borrow = ( A^B^C);
endmodule
## Output:
## Truthtable
### HAlf Subractor:
![HALF](https://github.com/AdhithiyanK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121029258/268b5128-2e3d-4742-a025-c3bf499f1d48)
### Full subractor :
![FULL](https://github.com/AdhithiyanK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121029258/92af6847-3ef6-46ee-8224-3ae04b2b2b6d)
## Logic Diagram:
### Half Subractor:
![HALF1](https://github.com/AdhithiyanK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121029258/8ee07ded-67e4-4619-a45a-42be3c9259da)
### Full subtractor :
![FULL 1](https://github.com/AdhithiyanK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121029258/5514ac10-4cb8-41b2-ac51-90bf666a2191)
##  RTL realization
### Half Subractor:
![HALF 2](https://github.com/AdhithiyanK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121029258/aa7de581-0680-40f5-9c46-53e4c14647e2)
###  Full Subtractor:
![FULL 2](https://github.com/AdhithiyanK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121029258/e4f1d1ce-017e-4447-b892-b3db2e585c4e)
## Timing diagram 
### Half Subractor:
![HALF 3](https://github.com/AdhithiyanK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121029258/7a7e99d9-4f1d-43f2-8003-a9ceebb176b4)
### Full Subtractor:
![FULL 3](https://github.com/AdhithiyanK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121029258/db674ad4-9a1d-4638-8903-2d5c515b7596)
## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
