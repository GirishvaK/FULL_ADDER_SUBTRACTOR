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

**Truthtable Full adder**
<img width="654" height="430" alt="498744805-cf80cd7b-5c9a-4a76-ac0f-4618eb9242ea" src="https://github.com/user-attachments/assets/b9e147c7-f8f2-473b-bb32-e4691c523279" />
Full subtractor
<img width="438" height="393" alt="498745542-4434a03c-27a2-4394-8066-8a552e4508fb" src="https://github.com/user-attachments/assets/f8fd13b0-118d-471f-8b34-a9e12e7c8587" />


**Procedure**

Write the detailed procedure here

**Program:**
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.*/

Developed by:Girishva.K RegisterNumber:25009292


**RTL Schematic Full adder**
<img width="1920" height="1080" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/17c6f628-05b1-43e5-9b00-8b799e6841b7" />
Full subtractor
<img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/ac5d4475-1f5a-4237-96c9-719178d09f29" />

**Output Timing Waveform Full adder**
<img width="1920" height="1080" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/5200a5c4-b8ed-4e03-8ca7-ccdc56622057" />
Full subtractor
<img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/480515f8-3945-4128-ad03-3bb4911a5381" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



