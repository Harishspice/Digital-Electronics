# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
```
1.Using nand gates and wires construct sr flip flop.

2.Repeat same steps to construct JK,D,T flipflops.

3.Find Rtl logic and timing diagram for all flipflops.

4.End the program.
```


### PROGRAM 
```
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Harish R
RegisterNumber:  22005828
```

### PROGRAM 1
```
module sr(S,R,clock,Q,Qbar);
input S,R,clock;
output Q,Qbar;
wire X,Y;
nand(X,S,clock);
nand(Y,R,clock);
nand(Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule
```
### PROGRAM 2
```
module d(D,clock,Q,Qbar);
input D,clock;
output Q,Qbar;
assign Dbar = ~D;
wire X,Y;
nand(X,D,clock);
nand(Y,Dbar,clock);
nand(Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule
```
### PROGRAM 3
```
module jk(J,K,clock,Q,Qbar);
input J,K,clock;
output Q,Qbar;
wire P,S;
nand(P,J,clock,Qbar);
nand(S,K,clock,Q);
nand(Q,P,Qbar);
nand(Qbar,S,Q);
endmodule
```
### PROGRAM 4
```
module t(T,clock,Q,Qbar);
input T,clock;
output Q,Qbar;
wire A,B;
nand(A,T,clock,Qbar);
nand(B,T,clock,Q);
nand(Q,A,Qbar);
nand(Qbar,B,Q);
endmodule
```



### RTL LOGIC FOR FLIPFLOPS 

### RTL 1
![194702098-dcfff254-26b9-4e01-b34c-0a7fd3fec711](https://user-images.githubusercontent.com/117935868/212852427-75571f00-0b84-417f-9a31-4133fb47a5a2.jpg)

### RTL 2
![194702101-2d6daeba-d66b-422c-8546-e2183ed6d15c](https://user-images.githubusercontent.com/117935868/212852538-653b0697-8c72-4008-b83e-d6b33e4eac1b.jpg)

### RTL 3
![194702105-b54ea8dd-5c05-4770-b2a4-03a864887f56](https://user-images.githubusercontent.com/117935868/212852611-06738e3c-3f0f-4904-90e5-6c8ef88000ff.jpg)

### RTL 4
![194702108-8e214d97-86ad-4b7d-ab68-c329b01cc7b8](https://user-images.githubusercontent.com/117935868/212852691-d6c8dea2-a183-48ce-a3b8-f9478556e943.jpg)



### TIMING DIGRAMS FOR FLIP FLOPS 

### TIMING DIAGRAM 1
![194702120-72d9d9fa-59a4-4bbd-b84f-e5d8d8faa182](https://user-images.githubusercontent.com/117935868/212852908-39611922-2df9-48a4-b02f-89a116cd8d4d.jpg)

### TIMING DIAGRAM 2
![194702140-0e207690-c12a-419d-b637-993b161a3aee](https://user-images.githubusercontent.com/117935868/212852999-da1ab49e-f85b-4e42-809d-4ea305092876.jpg)

### TIMING DIAGRAM 3
![194702148-6433a823-ae47-43c5-9f52-ab91343dc215](https://user-images.githubusercontent.com/117935868/212853127-6038081e-0d37-46f4-9fd3-c102b2836a67.jpg)

### TIMING DIAGRAM 4
![194702168-dc56c92b-b920-4aa5-8b77-cbbb6597f477](https://user-images.githubusercontent.com/117935868/212853219-0e7c48ed-13fb-436c-831e-f0a51de46342.jpg)


### RESULTS 
Thus implementation of JK,SR,T and D flipflops using NAND gates are executed sucessfully.
