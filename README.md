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
```
**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
```

## Full_adder
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule 

## Full_subtractor
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule


Developed by: PRITHVIRAJ.V
RegisterNumber: 212222100038
```
## RTL Schematic:

![318405073-2e45d893-4f83-4a98-8bc2-d0d30b70e7e2](https://github.com/prithviraj5703/FULL_ADDER_SUBTRACTOR/assets/121418418/a3a35e10-bdbf-4554-9732-397b33cd4249)

## Output Timing Waveform:
```
FULL_ADDER:
```

![318405216-5d286c1d-e62e-454a-a389-00ba2c2a91fc](https://github.com/prithviraj5703/FULL_ADDER_SUBTRACTOR/assets/121418418/a37037e6-a25c-416e-a29b-46c2913e643e)

```
FULL_SUBRACTOR:
```


![318405344-03d5d030-815e-4847-a976-2fd282cf0333](https://github.com/prithviraj5703/FULL_ADDER_SUBTRACTOR/assets/121418418/f0e35e7a-1f94-4729-af37-d84550e44b34)



## Result:
```
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



