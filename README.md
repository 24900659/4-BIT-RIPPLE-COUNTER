# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by: Mohana k.v.s.l
 RegisterNumber:24900659
*/
 module BRC(

 input clk,
 
 input reset,
 
 output [3:0]q
 
 );

 reg [3:0]q_int;

 assign q=q_int;
 
 always@(posedge clk or posedge reset)begin
 
 if(reset)
 
 q_init[0]<=1'b0;
 
 else
 
 q_init[0]<=~q_int[0];
 
 end
 
 genvar i;
 
 generate
 
 for(i=1;i<4;i=i+1)begin:ripple
 
 always@(posedge q_int[i-1] or posedge reset)begin
 
 if(reset)
 
 q_init[0]<=1'b0;
 
 else
 
 q_init[i]<=~q_int[1];
 
 end
 
 end
 
 endgenerate

endmodule

**RTL LOGIC FOR 4 Bit Ripple Counter**
![image](https://github.com/user-attachments/assets/4103981b-ca4b-4689-ac0e-837a40eaa301)

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
![image](https://github.com/user-attachments/assets/e7b6a593-a6e5-4346-85b5-3f2fbe90e684)

**RESULTS**
thus the implementation of 4 Bit Ripple Counter using verilog and validating their functionality using their functional tables
