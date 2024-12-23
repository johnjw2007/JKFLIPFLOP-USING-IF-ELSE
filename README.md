# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

/* write all the steps invloved */
1. Define the specifications and initialize the design.
2.  Declare the name of the entity and architecture by using VHDL source code
3.  Write the source code in VERILOG.
4.  Check the syntax and debug the errors if found, obtain the synthesis report.
5.  Verify the output by simulating the source code.
6.  Write all possible combinations of input using the test bench
7.  Obtain the place and route report.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
Developed by: John Wilfred Thomas J W
Register number: 24013517
*/

module exp_7(J,K,clk,q,qbar);
input J,K,clk;
output reg q;
output reg qbar;
initial q=0; 
initial qbar=1;
always@(posedge clk) begin q=((J&(~q))|((~k)&q)); qbar=~q;
end endmodule

**RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/user-attachments/assets/78ef9930-89c3-47fe-bc20-97bf8ef67e34)

**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/user-attachments/assets/8c9b0685-8d30-4862-aae8-b5e5c219cb79)

**RESULTS**
Thus the Flip flop designed and the truth tables is verified using Quartus software
