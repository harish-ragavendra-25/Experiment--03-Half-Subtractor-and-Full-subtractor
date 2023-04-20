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



Write the detailed procedure here 


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: HARISH RAGAVENDRA S
RegisterNumber:  212222230045
```
```
module halfsub(A,B,Diff,Borrow);
input A,B; 
output Diff,borrow;
asssign Diff = (A ^ B);
assign Borrow = (~A & B);
endmodule
```
```
module fullsub(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
assign Diff = (A^B^C);
assign borrow = (~a&(b^c)|(b&c));
endmodule 
```

## Output:
## HALF SUBRACTOR:
![Screenshot 2023-04-20 113612](https://user-images.githubusercontent.com/114852180/233273307-5658f9b1-4892-4f98-9b6e-f2dc1029a460.png)
## FULL SUBRACTOR:
![Screenshot 2023-04-20 113631](https://user-images.githubusercontent.com/114852180/233273507-43f9744f-c0ba-4a08-af77-99002e9095d3.png)

## Truthtable

## HALF SUBRACTOR:
![Screenshot 2023-04-20 113644](https://user-images.githubusercontent.com/114852180/233273594-312e784b-2db6-4c10-bb56-09e6713c967a.png)

## FULL SUBRACTOR:
![Screenshot 2023-04-20 113651](https://user-images.githubusercontent.com/114852180/233274298-80a76d38-6f00-448f-bda7-40ca32984d90.png)

##  RTL realization

## HALF SUBRACTOR:
![Screenshot 2023-04-20 113659](https://user-images.githubusercontent.com/114852180/233274618-71f74595-6cda-4e12-852c-0e27b4b090f0.png)

## FULL SUBRACTOR:
![Screenshot 2023-04-20 113707](https://user-images.githubusercontent.com/114852180/233274651-0c85dc93-ffda-47de-be3d-2c5dbb181762.png)


## Timing diagram 

## HALF SUBRACTOR:
![Screenshot 2023-04-20 120040](https://user-images.githubusercontent.com/114852180/233277538-5b4c0f1b-7c57-4119-9f8f-9057065c63de.png)
## FULL SUBRACTOR:
![Screenshot 2023-04-20 115703](https://user-images.githubusercontent.com/114852180/233277276-0cd68075-501d-4345-8a81-e2c40ccf3796.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
