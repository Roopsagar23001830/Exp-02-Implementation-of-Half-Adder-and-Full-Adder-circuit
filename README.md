# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: ROOP SAGAR S L
RegisterNumber:  212223040175
*/
1. Program to design a half adder:
   
module halfadder(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum=a^b;
assign carry=a&b;
endmodule

code:

![Screenshot 2023-12-25 143721](https://github.com/Roopsagar23001830/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145972515/36e031ec-7b27-4eca-8b0b-d0f846a70376)

2. Program to design a full adder:

module fulladder(input a,b,cin,output s,Cout);
assign s=a^b^cin;
assign Cout=(a&b)|(b&cin)|(a&cin);
endmodule    

code:

![Screenshot 2023-12-25 150424](https://github.com/Roopsagar23001830/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145972515/6bdfc16e-e02d-4b05-8b80-0a26ad15e58c)

Truthtable:Half adder:

![Screenshot 2023-12-25 145456](https://github.com/Roopsagar23001830/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145972515/ae48601a-5981-48d4-b555-401fbd172dbb)

full adder:

![Screenshot 2023-12-25 145542](https://github.com/Roopsagar23001830/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145972515/cf5dab55-a32c-4a26-b179-df62818ff731)

RTL realization
half adder:

![Screenshot 2023-12-25 143735](https://github.com/Roopsagar23001830/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145972515/d9f90ebd-f3a7-4581-9612-f9dd2d566339)

full adder:

![Screenshot 2023-12-25 150438](https://github.com/Roopsagar23001830/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145972515/5645a32d-5687-46a3-a7c4-8ed0181673ad)

### Output waveform:
half adder:

![Screenshot 2023-12-25 143906](https://github.com/Roopsagar23001830/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145972515/a1a8c5f5-1f64-4771-ab8f-ee15a7b877cc)

full adder:

![Screenshot 2023-12-25 150643](https://github.com/Roopsagar23001830/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145972515/ef6cb984-0d4a-4976-bf70-bd2373aa21ce)

### Result:
Thus the half adder and full adder circuit are designed and the truth table for half adder and full adder are verified.
