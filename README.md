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

/* Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. */
**Full Adder**
```
module ex4a(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;
xor(sl,a,b);
and(cl,a,b);
xor(sum,sl,cin);
and (c2,sl,cin);
or(cout,c2,cl);
endmodule
```
**Full Subtractor**
```
module ex4b (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2, w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```

Developed by: Dinesh Prabhu S
RegisterNumber: 24004388

**RTL Schematic**

**Full Adder**
![Screenshot (113)](https://github.com/user-attachments/assets/fbd9fa76-97b3-4022-a081-0698695e563e)


**Full Subtractor**

![Screenshot (111)](https://github.com/user-attachments/assets/719d0a65-7c45-48d6-83e9-551c02cf39a4)


**Output Timing Waveform**

**Full Adder**
![Screenshot (114)](https://github.com/user-attachments/assets/0d1ab4dc-34d0-44b1-9687-b456a6ed352d)


**Full Subtractor**
![Screenshot (112)](https://github.com/user-attachments/assets/38e2b5f0-b9f8-4df4-856c-c28ed9dbf60f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



