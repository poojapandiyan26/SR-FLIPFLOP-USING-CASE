# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using Verilog and validate their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, the SR latch operates with an enable signal. The circuit diagram of the SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of the SR flipflop is similar to SR Latch. However, this flip-flop affects the outputs only when the positive transition of the clock signal is applied instead of active enable. The following table shows the state table of the SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are the present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when the positive transition of the clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**


1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**PROGRAM**

Program for flipflops and verify its truth table in quartus using Verilog programming. 
### Developed by: Pooja Sri P B Register Number: 24007629
```
module ed(s,r,clk,q,qbar);
input s,r,clk;
output q,qbar;
wire w1,w2;
nand(w1,s,clk);
nand(w2,r,clk);
nand(q,w1,qbar);
nand(qbar,q,w2);
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![WhatsApp Image 2024-10-24 at 10 54 29_3d904ae4](https://github.com/user-attachments/assets/53736e29-7a13-404c-a5ba-42661c147abe)


**TIMING DIAGRAMS FOR FLIP FLOPS**
![WhatsApp Image 2024-10-24 at 10 58 24_1dbcfe98](https://github.com/user-attachments/assets/9c6e10cb-0d29-4771-9556-ed7c6e9a61ce)


**RESULTS:**
Implementation of SR flipflop using Verilog is successfull.
