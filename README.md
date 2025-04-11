# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

```
Software – Quartus prime
modelism altera
```


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
```
```
FULL ADDER
![Screenshot 2025-04-11 015016](https://github.com/user-attachments/assets/c12b52f4-88e3-4d71-9d20-bc94825e32a1)

FULL SUBTRACTOR
![Screenshot 2025-04-11 015044](https://github.com/user-attachments/assets/98c996bd-983d-4d08-88f8-6e5d88142b7f)
```
```

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
Developed by: PRIYA.B
RegisterNumber: 212224230208
*/
```

```
module EXP4(sum, cout, a, b, cin);
output sum;
output cout;
input a;
input b;
input cin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
endmodule

module EXP41(df, bo, a, b, bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```

**RTL Schematic**
```
```
![Screenshot 2025-04-10 112849](https://github.com/user-attachments/assets/79c81dfd-cf30-4421-9aff-9363fafb1379)
 ![Screenshot 2025-04-11 011304](https://github.com/user-attachments/assets/c65467af-a0e7-4678-8eae-361c6b17c047)
```
```

**Output Timing Waveform**
```
```
![Screenshot 2025-04-10 113438](https://github.com/user-attachments/assets/158a6c5c-1769-4103-9e2b-dd816f281b35)

 ![Screenshot 2025-04-11 011510](https://github.com/user-attachments/assets/980f31cc-3f16-4f97-a529-a84035e71385)
```
```
**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



