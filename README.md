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

**Procedure**

Write the detailed procedure here

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
Developed by: Jagadeesh.A
RegisterNumber: 24010183
```
PROGRAM F1:
```
module full_adder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule
```

PROGRAM F2:
```
module full_subtractor(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule
```



**RTL Schematic**
RTL F1:
![Screenshot (58)](https://github.com/user-attachments/assets/b24cda23-1432-4a77-89a0-d68ac55541e0)
RTL F2:
![Screenshot (60)](https://github.com/user-attachments/assets/efec981f-9472-4e7d-b91e-6cc83c569a51)

**TRUTH TABLE**
F1:
![Screenshot 2024-12-08 115428](https://github.com/user-attachments/assets/a4e4cd4d-ed74-44f5-9529-6f0917dfd7fd)
F2:
![Screenshot 2024-12-08 115857](https://github.com/user-attachments/assets/888258ff-5ec0-45e3-b346-e839d241534e)




**Output Timing Waveform**
FULL ADDER:
![Screenshot (56)](https://github.com/user-attachments/assets/45cf30e7-cdfb-4050-9a09-1942eda8d909)
FULL SUBTRACTER:
![Screenshot (61)](https://github.com/user-attachments/assets/1ca2a314-61cb-4705-b3e6-16636039dd5e)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



