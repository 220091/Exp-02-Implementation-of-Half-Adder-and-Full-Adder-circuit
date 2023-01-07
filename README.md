 AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

 Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

 Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

 Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

 Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

 Figure -02 FULL ADDER 

 Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
HALF ADDER  

module HalfAdder(a,b,sum,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule  

FULL ADDER  

module FullAdder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum = ((a^b)^c);

assign carry = ((a&b)|(b&c)|(c&a));

endmodule  

Developed by: JENIFER.A
RegisterNumber:  22009141

Logic symbol 
![symbol](https://user-images.githubusercontent.com/121572543/211146821-10aed368-5c07-4094-8dfa-7d06b59bd37d.png)

OUTPUT
RTL realization
HALF ADDER
![HADDER1](https://user-images.githubusercontent.com/121572543/211146867-be4d78aa-5dfd-4f3a-946b-d1331cf5679a.png)

FULL ADDER
![FADDER1](https://user-images.githubusercontent.com/121572543/211146895-b2d75cd6-a317-408e-aed8-4239c4365a5f.png)


 TIMING DIAGRAM
 
 HALF ADDER
 ![timing diagram1](https://user-images.githubusercontent.com/121572543/211146972-57ad99f7-0336-4f7a-bd53-4fc571ed88f8.png)

FULL ADDER
![timing diagram2](https://user-images.githubusercontent.com/121572543/211146988-6d73dfe9-f826-4f8b-992e-f23c5e256aff.png)



TRUTH TABLE 

HALF ADDER
![output1](https://user-images.githubusercontent.com/121572543/211147000-a3d05df0-a93a-410c-8470-55134e362aa9.png)

FULL ADDER
![output2](https://user-images.githubusercontent.com/121572543/211147009-9904b8c3-5ff5-4845-a54d-fe1a2480c1cc.png)


Result:
Thus the implementation of half adder and full adder are studied and the truth table for different logic gates are verified.
