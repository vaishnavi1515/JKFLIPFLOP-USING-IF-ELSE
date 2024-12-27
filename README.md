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

 step-1 Go to quartus software.

step-2 Set new environment.

step-3 Type the code to implement SR flipflop using verilog and validating their functionality using their functional tables.

step-4 Run the program.

step-5 Give inputs in the waveform table.

step-6 Run the program.

**PROGRAM**

Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: Vaishnavi v

RegisterNumber:2400560
~~~
module jk_ff (j, k, clk, rst, q);

  input j, k, clk, rst;
  
  output reg q;
  
  always @(posedge clk or posedge rst) begin
  
    if (rst)
    
      q <= 0; // Reset the flip-flop
      
    else if (j == 0 && k == 0)
    
      q <= q; // No change
      
    else if (j == 0 && k == 1)
    
      q <= 0; // Reset
      
    else if (j == 1 && k == 0)
    
      q <= 1; // Set
      
    else if (j == 1 && k == 1)
    
      q <= ~q; // Toggle
      
  end
~~~

**RTL**

![WhatsApp Image 2024-12-24 at 00 14 14_2afc4159](https://github.com/user-attachments/assets/b86b1b37-f30b-4a07-ab05-c814109d41df)


**OUTPUT**

![WhatsApp Image 2024-12-24 at 00 14 47_5fd1e2f9](https://github.com/user-attachments/assets/d1e878a8-6871-4c52-b0ba-8e14cb092b0e)


**RESULTS**

thus,the code executed successfully.
