### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:Harshadharshini.R RegisterNumber: 212224230089
*/
```module EXP11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
    if(!rstn)
	   out<=0;
	 else
	   out <= out+1;
end
endmodule
```
**RTL LOGIC UP COUNTER**

![443292521-7e8fb58c-9bd9-4dbe-9297-613da1a19c36](https://github.com/user-attachments/assets/4ee54684-a728-4ad5-887f-45766e6f525c)


**TIMING DIAGRAM FOR IP COUNTER**
![393628915-05fa190c-d69c-4547-bdd9-798238ba91d5](https://github.com/user-attachments/assets/552948d5-7122-4f38-b9fb-32a994ddf725)


**TRUTH TABLE**

![326659069-30bd014d-26c8-41a7-9685-fd68b593621a](https://github.com/user-attachments/assets/d6d5d272-e67e-430b-b0e8-44ffb8803485)


**RESULTS**
4 bit synchronous up counter and validate functionality are verified.
