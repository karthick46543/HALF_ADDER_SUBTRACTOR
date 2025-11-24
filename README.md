# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

```HALF ADDER TRUTHTABLE```

![Screenshot 2024-11-12 102450](https://github.com/user-attachments/assets/ee0c7cc4-4b0f-462c-bf97-eecfacb7c1ee)

```HALF SUBTRACTOR TRUTHTABLE```

![hs_truthtable](https://github.com/user-attachments/assets/ec06694e-4c6b-43bf-90a7-aca635af6b94)



**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module ex03(a,b,cy,sm,df,bo);
input a,b;
output sm,cy,df,bo;
xor (sm,a,b);
and (cy,a,b);
xor (df,a,b);
and (bo,~a,b);
endmodule
```

/* Program to design a half adder and half subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: RISHI BALA KAERTHICK K,25010929

**RTL Schematic**

![Screenshot 2024-11-12 101336](https://github.com/user-attachments/assets/0667ce93-345a-4bec-8c25-a2cf7cf47731)


**Output/TIMING Waveform**
![Screenshot 2024-11-12 101508](https://github.com/user-attachments/assets/0564f8a4-97da-4ce7-8740-eb97c0f35d0a)


**Result:**
 The half adder and half subtractor circuit and its truth table in Quartus are verified using Verilog programming.

