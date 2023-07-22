# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

## Implementation-of-Half-Adder-and-Full-Adder-circuit

## AIM:

To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime Theory Adders are digital circuits that carry out addition of numbers.

## Half Adder

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

![image](https://user-images.githubusercontent.com/117935868/211154305-f4c773bf-995f-4adf-be84-c2ba118fe3b2.png)


## Figure -01 HALF ADDER

![image](https://user-images.githubusercontent.com/117935868/211154327-113dec32-9365-4990-8f1b-9b2844e98b4e.png)


## Figure -02 FULL ADDER

Procedure

Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

## Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Harish R
RegisterNumber: 22005828
*/
Half Adder
module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

Full Adder
module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
## Output:
## Half Adder
RTL
![image](https://user-images.githubusercontent.com/117935868/211154050-d98be24c-3b7a-4f41-b360-8cc4ede6b986.png)


## TIMING DIAGRAM
![image](https://user-images.githubusercontent.com/117935868/211154039-46e4f816-b969-4281-8b94-f0fbf5156c81.png)


## TRUTH TABLE
![image](https://user-images.githubusercontent.com/117935868/211154008-8fdff8e8-d089-4d0f-9f79-43704f447ba7.png)


## Full Adder
## RTL
![image](https://user-images.githubusercontent.com/117935868/211154098-b46aae54-a3b0-4522-baee-ae33a4f19c97.png)


## TIMING DIAGRAM
![image](https://user-images.githubusercontent.com/117935868/211154107-df3227df-ad8c-4b0d-b6a2-d85e9b0ebf61.png)


## TRUTH TABLE
![image](https://user-images.githubusercontent.com/117935868/211154112-1d8e3d11-c910-43c6-9da3-499ac8fd68d9.png)


## Result:

Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
