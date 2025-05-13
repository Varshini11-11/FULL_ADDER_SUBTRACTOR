DEVOLOPED BY: VARSHINI.G
REG NO: 212224050056




# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULL ADDER 

![image](https://github.com/user-attachments/assets/026a22d1-a0b6-43e2-bbf2-861ff7719d05)

FULL SUBTRACTOR 

![image](https://github.com/user-attachments/assets/437c175b-f03c-49e4-8f6a-394013dd7304)

**Procedure**

 Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram

**Program:**


**FULL ADDER**

~~~

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
~~~
**FULL SUBTRACTOR**
~~~

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule

~~~
**RTL Schematic**

FULL ADDER 


![image](https://github.com/user-attachments/assets/ba25d6cd-eec3-4584-8455-fc2c04691c6e)

FULL SUBTRACTOR 

![image](https://github.com/user-attachments/assets/b4ede25b-39c2-40bb-9047-c1e919d29b37)

**Output Timing Waveform**


FULL ADDER 

![image](https://github.com/user-attachments/assets/80e27046-b5da-448b-87ad-185ce7d55517)


FULL SUBTRACTOR 

![image](https://github.com/user-attachments/assets/150a9770-30a7-44cf-a7d3-c841cac99e9a)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



