# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. half-subtractor9

Sum = X'Y+XY' = X ⊕ Y Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. full-subtractor6

Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
1.Use module projname(input,output) to start the Verilog programmming. 2.Assign inputs and outputs using the word input and output respectively. 3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression. 4.Use each output to represnt onre for differnce and the other for borrow. 5.End the verilog program using keyword endmodule.

## Program:
```
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Harish R
RegisterNumber: 22005828
*/
HALF SUBTRACTOR:
module half(a,b,diff,borrow);
input a,b;
output diff,borrow;
wire x;
xor(diff,a,b);
not(x,a);
and(borrow,x,b);
endmodule


FULL SUBTRACTOR:
module full(a,b,c,diff,borrow);
input a,b,c;
output borrow,diff;
wire an,q,r,s,t,cn,u;
not(an,a);
not(cn,c);
xor(q,a,b);
xor(diff,q,c);
and(s,a,b);
and(t,q,cn);
or(borrow,s,t);
endmodule
```
## Output:
![image](https://user-images.githubusercontent.com/117935868/211155220-690d7b2a-7ef5-41f3-aea7-67e7bcf1c904.png)


Half subtractor

![image](https://user-images.githubusercontent.com/117935868/211155224-9df512d4-44e4-41a6-b32c-02a9eb16e8b0.png)


Full subtractor

![image](https://user-images.githubusercontent.com/117935868/211155231-cac815f6-9a2b-4f82-bafb-f07c3da53e4b.png)


Timing diagram:

HALF SUBTRATOR


![image](https://user-images.githubusercontent.com/117935868/211155240-03a3f727-dceb-474f-8af1-afacc773bcfa.png)


Full subtractor

![image](https://user-images.githubusercontent.com/117935868/211155254-6a7e4dca-5295-4a63-93af-e5f816f96072.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
