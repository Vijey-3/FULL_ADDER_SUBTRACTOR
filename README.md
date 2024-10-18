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

![Screenshot 2024-09-28 172127](https://github.com/user-attachments/assets/5fb79d2f-1b6b-4235-8647-c5d3a7d67b18)

FULL SUBTRACTOR

![Screenshot 2024-09-28 172452](https://github.com/user-attachments/assets/4e9a5498-493f-4a46-ae16-04254c7a688e)


**Procedure**

Full Adder: 1.Open Quartus II and create a new project. 2.Use schematic design entry to draw the full adder circuit. 3.The circuit consists of XOR, AND, and OR gates. 4.Compile the design, verify its functionality through simulation. 5.Implement the design on the target device and program it.

Full Subtractor: 1.Follow the same steps as for the full adder. 2.Draw the full subtractor circuit using schematic design. 3.The circuit includes XOR, AND, OR gates to perform subtraction. 4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
```
Developed by:VIJEY K S 
RegisterNumber:212223040239
```
FULL ADDER
```
module re(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = (a^b^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```

FULL SUBTRACTOR
```
module fs(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&(~a)));
endmodule
```
**RTL Schematic**

FULL ADDER
![Screenshot 2024-09-20 084707](https://github.com/user-attachments/assets/d6dacc78-20eb-475d-8c1d-32b01eb660ff)

FULL SUBTRACTOR
![Screenshot 2024-09-20 091445](https://github.com/user-attachments/assets/f4d22e08-58d0-49e8-8f69-17e3bbbd21ff)


**Output/Timing Waveform**

FULL ADDER
![Screenshot 2024-09-20 085759](https://github.com/user-attachments/assets/45253411-0700-41c8-a943-0091a08046b9)

FULL SUBTRACTOR
![Screenshot 2024-09-20 091857](https://github.com/user-attachments/assets/e03f8152-ffe3-48fb-a166-51ee8edb0b33)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



