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
![Screenshot 2024-12-03 084951](https://github.com/user-attachments/assets/b5503988-febf-45f6-ad30-e2ceb5a965b4)

FULL SUBTRACTOR:
![Screenshot 2024-12-03 085129](https://github.com/user-attachments/assets/871e08c6-0069-442d-96e6-fad712715614)

**Procedure**
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.
\

### **Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: Vishal C
RegisterNumber: 24001428

```
module fulladddataflow(a, b, cin, sum, carry); 
  input a; 
  input b;
  input cin; 
    output sum; 
    output carry; 
 assign sum=a^b^cin; 
 assign carry=(a & b) | (b & cin) | (cin & a); 
 endmodule
```
```
module fulsubdataflow(a, b, cin, diff, borrow); 
    input a; 
    input b; 
    input cin; 
    output diff; 
    output borrow; 
  wire abar; 
  assign abar= ~ a; 
  assign diff=a^b^cin; 
  assign borrow=(abar & b) | (b & cin) |(cin & abar); 
endmodule
```
*/

**RTL Schematic**
FULL ADDER: 
![WhatsApp Image 2024-12-03 at 08 18 01_ee99fd11](https://github.com/user-attachments/assets/bb6379df-37b2-4236-917e-580bdd0c9432)

FULL SUBTRACTOR: 
![WhatsApp Image 2024-12-03 at 08 18 00_76e15b42](https://github.com/user-attachments/assets/12e773c1-dd3c-439c-a164-ea26bf3c7f7d)

**Output Timing Waveform**
![WhatsApp Image 2024-12-03 at 08 18 00_cad176a1](https://github.com/user-attachments/assets/c13acc83-bfe9-4a50-b95c-9c10f301156e)
![WhatsApp Image 2024-12-03 at 08 18 01_abc62c7f](https://github.com/user-attachments/assets/39610aa1-111c-4068-acb5-636c0d978338)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
