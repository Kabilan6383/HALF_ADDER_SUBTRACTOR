# DATE:15.11.2024
# EXP-3:HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB
![Screenshot 2024-12-27 111606](https://github.com/user-attachments/assets/63a8ba59-d816-478d-a867-54b5bf61087b)


Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B
![Screenshot 2024-12-27 111619](https://github.com/user-attachments/assets/e41e4f01-d80b-46e8-9d59-e4d5062cd84e)


Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

 Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

```

Developed by:PREETHI A K
RegisterNumber:212223230156

module EXP3(a,b,sum,carry,D,Bo);
input a,b;
output sum,carry,D,Bo; 
xor(sum,a,b);
and(carry,a,b);
wire abar;
not(abar,a);
xor(D,a,b);
and(Bo,abar,b);
endmodule
```


Developed by:P.KABILAN
 RegisterNumber:24900859

**RTL Schematic**
![Screenshot 2024-12-27 111630](https://github.com/user-attachments/assets/93be6dce-c7b1-4df4-94c4-7953a3974980)



**Output/TIMING Waveform**
![Screenshot 2024-12-27 111639](https://github.com/user-attachments/assets/faac4f00-9baf-4243-bfd0-2f3243755958)



**Result:**
Thus the output is verified.
