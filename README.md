# FULL_ADDER_SUBTRACTOR
Implementation-of-Full-Adder-and-Full-subtractor-circuit


```
Developed by: VIJEY K S
RegisterNumber: 212223040239
```

## **AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## **Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## **Full Adder and Full Subtractor**

### **Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

### **Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## **Truthtable**

### **FULL ADDER:**

![DE E-4 truthtable](https://github.com/04Varsha/FULL_ADDER_SUBTRACTOR/assets/149035374/7116d2bf-8e90-4e96-bfd5-d62af11a317a)

### **FULL SUBTRACTOR:**

![DE E-4 subtractor truth table](https://github.com/04Varsha/FULL_ADDER_SUBTRACTOR/assets/149035374/33d8ba16-9169-40b0-8696-3bb8e5c3a0b7)

## **Procedure**
```
1. Open Quartus Software   
2. Create a New Project  
3. Create a New Design File  
4. Compile the Program  
5. Generate RTL Schematic  
6. Create Nodes for Inputs/Outputs  
7. Generate Timing Diagram  
8. Simulate Different Input Combinations  
9. Save Your Work  
```

**Program:**

```
#Full adder
module Exp_3(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

#Full Subtractor
module Exp_3i(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule
```
**RTL Schematic:**

#Full adder
![image](https://github.com/user-attachments/assets/65ea7866-f870-46af-b3ff-701110d5aba0)

#Full Subtractor
![image](https://github.com/user-attachments/assets/3d25a5a9-a73d-466c-ba45-c6106c943439)

**Output Timing Waveform:**

#Full adder
![image](https://github.com/user-attachments/assets/dfbeb61e-332a-49c7-883e-95bbca55b117)

#Full Subtractor
![image](https://github.com/user-attachments/assets/db5b7fb0-37a7-41e5-8bf4-8f83a2fae7c6)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



