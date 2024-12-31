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

1.Compile and run the program.

2.Generate the RTL schematic and save the logic diagram.

3.Create nodes for inputs and outputs to generate the timing diagram.

4.For different input combinations generate the timing diagram

**PROGRAM**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by:KESHAVARTHINI B  RegisterNumber: 24900033
*/

module exp127(

input wire clk, // Clk input

output reg [3:0] count //4-bit counter output

);
always @(posedge clk) begin

if (count ==4'b1111) // Reset when count reaches 15

    count <=4'b0000;
    
else 

    count <= count + 1; // Increment count
    
end

endmodule


**RTL LOGIC FOR 4 Bit Ripple Counter**

![Screenshot (75)](https://github.com/user-attachments/assets/74277fc2-b6cc-4825-8a4c-93ac076dcd78)


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![Screenshot (76)](https://github.com/user-attachments/assets/86022d16-fca8-448e-9cf6-e5102ab45087)


**RESULTS**

4 Bit Ripple Counter using verilog and validating their functionality using their functional tables is
implemented.
