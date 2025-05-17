# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1.Define the Module
- Create a Verilog module for the D flip-flop with inputs (D, clk) and outputs (Q, Q').
2.Write the Behavioral Code
- Use an always block triggered on the positive edge of the clock to assign Q = D.
3.Include Reset Logic (Optional)
- Implement synchronous or asynchronous reset to initialize the flip-flop state.
4.Create a Testbench
- Write a Verilog testbench to apply different input values (D) and observe the output (Q).
5. Simulate the Design
- Use simulation tools like ModelSim or Quartus to verify the functional behavior.
6.Validate Using Functional Tables
- Compare the simulation results with the expected truth table of a D flip-flop.



**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
```
 module Dflipflop (d, clk, rst, q);
 input d, clk, rst;
 output reg q;
 always @(negedge clk or posedge rst) begin
 if (rst)
 q <= 0; // Reset the flip-flop
 else
 q <= d; // D input is passed to Q on the negative clock edge
 end
 endmodule
```
Developed by:DIVYASHREE B RegisterNumber:212224040081
*/

**RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/user-attachments/assets/67caba38-c484-4ed2-9693-51e14793181c)


**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/user-attachments/assets/c06a6334-52c8-4d24-911d-2d6b7f032e3b)



**RESULTS**
D flipflop using verilog and validating their functionality using their functional tables are verified
