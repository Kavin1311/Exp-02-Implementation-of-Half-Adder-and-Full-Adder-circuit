## NAME : T.KAVINAJAI
## REGISTER NUMBER: 212223100020

# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Procedure
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

##   THEORY:
Adders are digital circuits that carry out addition of numbers.

### Half Adder:
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## FIGURE-01-HALF ADDER: 
![image](https://github.com/Kavin1311/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145695724/f7655204-0cd0-4c6e-b3d7-d3d0def9321f)

### Full Adder:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
## FIGURE - 02- FULL ADDER:
![image](https://github.com/Kavin1311/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145695724/f0f5b44e-ee26-4234-be69-1abd306b4633)

###  Program:
Program to design a half and full adder circuit and verify its truth table in quartus using Verilog programming.
## HALF ADDER
```
module half_adder(A,B,C,S);
input A,B;
output S,C;
assign c=A&B;
assign S=A^B;
endmodule
```
## FULL ADDER
```
module Full_Adder(a,b,carryin,sum,carryout);
input a,b,carryin;
output sum,carryout;
wire x,p,q,r;
xor(x,b,carryin);
xor(sum,x,a);
and(p,a,b);
and(q,b,carryin);
and(r,a,carryin);
or(carryout,p,q,r);
endmodule
```
## OUTPUT:
## Logic symbol & Truthtable
## HALF ADDER:
![image](https://github.com/Kavin1311/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145695724/cccd6f09-e2ea-4cb5-bbce-526ac122009a)

## FULL ADDER:
![image](https://github.com/Kavin1311/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145695724/8c0389d6-27de-4d78-8ed7-436f5f5711c9)

## RTL realization:
## HALF ADDER:
![image](https://github.com/Kavin1311/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145695724/7930bac4-7dc3-44f5-9420-316c09605ae6)

## FULL ADDER:
![image](https://github.com/Kavin1311/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145695724/1d8c265a-d046-416f-8b2d-b26e3475b193)
## TIMING DIAGRAM:

## HALF ADDER:
![image](https://github.com/Kavin1311/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145695724/6f58239b-1d09-43ea-b63a-43c250de8669)

## FULL ADDER:
![image](https://github.com/Kavin1311/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145695724/73bbccbd-d8e0-4704-b158-90fece884c91)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
