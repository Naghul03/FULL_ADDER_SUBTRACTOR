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

![image](https://github.com/user-attachments/assets/685fdb0c-0b96-4e1a-a095-51a383a4ed4c)
![image](https://github.com/user-attachments/assets/d018753c-01b8-4f80-9fad-a9e433e951ef)


**Procedure**

Full Adder:

Inputs: Three inputs: A, B (the two bits to be added), and Cin (the carry-in bit from a previous addition). Outputs: Two outputs: Sum (the resulting sum) and Cout (the carry-out bit). Logic: Sum = A ^ B ^ Cin (XOR operation). Cout = (A & B) | (A & Cin) | (B & Cin) (carry occurs if at least two inputs are 1).

Full Subtractor:

Inputs: Three inputs: A, B (the two bits, where A - B is calculated), and Bin (the borrow-in from a previous subtraction). Outputs: Two outputs: Diff (the resulting difference) and Bout (the borrow-out bit). Logic: Diff = A ^ B ^ Bin (XOR operation). Bout = (~A & B) | ((~A | B) & Bin) (borrow occurs if A is less than B or needs a borrow). Both circuits follow simple XOR logic for the primary result and AND-OR logic to determine carry or borrow conditions

**Program:**
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
 Developed by:N.Naghul varshan
 RegisterNumber:24901302
```
```
module fulladdsub(a,b,cin,bin,sum,carry,difference,borrow); 
input a,b,cin,bin; output sum,carry,difference,borrow; 
assign sum=a^b^cin; 
assign carry=(a^b)&cin|a&b;
assign difference=a^b^bin; 
assign borrow=~(a^b)&bin|(~a)&b;
endmodule
```

**RTL Schematic**

![image](https://github.com/user-attachments/assets/4590dcbd-b361-43b0-a986-cdccd5ad3fc0)


**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/81093cd1-5e4d-4224-9c75-885409b474cd)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



