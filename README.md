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

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:Piyush kumar 
RegisterNumber:2122232220075
*/
~~~

half adder
module ex3(a,b,w,x,y,z);
input a,b;
output w,x,y,z;
xor(w,a,b);
and(x,a,b);
xor(y,a,b);
and(z,~a,b);
endmodule

half subt:
module ex03(a,b,D,Bo);
input a,b;
output D,Bo;
assign D = a ^ b;
assign Bo = ~a & b;
endmodule
~~~


**RTL Schematic**
![Screenshot 2024-03-19 140349](https://github.com/H515piyush/HALF_ADDER_SUBTRACTOR/assets/147472999/dbee0d19-50db-449b-9328-e4a81f0c6b09)
![half sub output rtl](https://github.com/H515piyush/HALF_ADDER_SUBTRACTOR/assets/147472999/05076555-d507-4368-a12a-269185a2b859)

Output/TIMING Waveform:

HALF ADDER:

![318398777-8efe7503-fea8-4272-bf8b-0e334e95cdb1](https://github.com/H515piyush/HALF_ADDER_SUBTRACTOR/assets/147472999/ec78a6a8-456c-47b1-a816-329fa02e93b1)


HALF SUTRACTOR:

![half sub wave form](https://github.com/H515piyush/HALF_ADDER_SUBTRACTOR/assets/147472999/8cf68a8b-09a3-4b76-94c7-3b05d1027a5d)





**Result:**
program executed successfully
