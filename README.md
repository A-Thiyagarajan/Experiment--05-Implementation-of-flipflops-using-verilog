# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM:
Ref no: 22008681
Nmae: A.Thiyagarajan

To implement all the flipflops using verilog and validating their functionality using their functional tables
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

   1.Using nand gates and wires construct SR flipflop.
   
   2.Repeat same steps to constuct JK,D,T flipflops
   
   3.find Rtl logic and timing diagram for all flipflops
   
   4.End the program.



### PROGRAM 
Program for flipflops  and verify its truth table in quartus using Verilog programming.
```
i) SR FLIP FLOP:

module S(S,R,Clock,Q,Qbar);
input S,R,Clock;
output Q,Qbar;
wire X,Y;
nand (X,S,Clock);
nand (Y,R,Clock);
nand (Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule

ii) D FLIP FLOP:

module D(D,Clock,Q,Qbar);
input D,Clock;
output Q,Qbar;
assign Dbar = ~D;
wire X,Y;
nand (X,D,Clock);
nand (Y,Dbar,Clock);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule

iii) JK FLIP FLOP:

module JK(J,K,Clock,Q,Qbar);
input J,K,Clock;
output Q,Qbar;
wire P,S;
nand (P,J,Clock,Qbar);
nand (S,K,Clock,Q);
nand (Q,P,Qbar);
nand (Qbar,S,Q);
endmodule

iv) T FLIP FLOP:

module T (T,Clock,Q,Qbar);
input T,Clock;
output Q,Qbar;
wire A,B;
nand (A,T,Clock,Qbar);
nand (B,T,Clock,Q);
nand (Q,A,Qbar);
nand (Qbar,B,Q);
endmodule
```
### RTL LOGIC FOR FLIPFLOPS 
#### SR flip flop
![SR flip flop](https://user-images.githubusercontent.com/118707693/212383743-ef267f6c-2ad9-4278-bb64-ea4c091d00a1.png)
#### D flip flop
![D flip flop](https://user-images.githubusercontent.com/118707693/212384082-29b1b98b-9123-414e-bfa8-c4b4ea6f7688.png)
#### JK flip flop
![JK flip flop](https://user-images.githubusercontent.com/118707693/212384398-b3e9480e-89bf-4fdf-9449-2a1f402adbf6.png)
#### T flip flop
![T flip flop](https://user-images.githubusercontent.com/118707693/212384822-5b2c368d-659b-467f-8526-016f36f37826.png)

### TIMING DIGRAMS FOR FLIP FLOPS 
#### SR flip flop

![SR flip flop td](https://user-images.githubusercontent.com/118707693/212385044-923459af-83c1-46a3-a369-e27bea4a527b.png)
#### D flip flop
![D flip flop td](https://user-images.githubusercontent.com/118707693/212385255-4c010127-af73-4ecb-9276-2d43b8853081.png)
#### JK flip flop
![JK flip flop td](https://user-images.githubusercontent.com/118707693/212385404-2a04f6df-c6c8-427a-9ffa-80683898b6ed.png)

#### T flip flop
![T FLIP FLOP TD](https://user-images.githubusercontent.com/118707693/212385533-532153f9-b753-4766-8a76-f49d989d4dd5.png)


### RESULTS 
All the flipflops are implementde using verilog and their functionality has been validated using their functional tables.
