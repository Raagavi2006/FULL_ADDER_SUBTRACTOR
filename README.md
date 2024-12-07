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
**FULL ADDER**
![WhatsApp Image 2024-12-07 at 17 48 35_606cf1cd](https://github.com/user-attachments/assets/37ca7a0c-3a95-424a-8411-661cab0495b0)

**FULL SUBTRACTOR**
![WhatsApp Image 2024-12-07 at 17 48 34_b306e8ed](https://github.com/user-attachments/assets/5d44e681-3528-436c-ac3b-f206b39e345a)

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:

**FULL ADDER**

       module fa(a,b,cin,sum,carry);
       input a,b,cin;
       output sum,carry;
       assign sum=( (a ^ b)^cin);
       assign carry= ((a&b)| (cin&(a^b)));
       endmodule

**FULL SUBTRACTOR**

      module fs(a,b,bin,difference,borrow);
      input a,b,bin;
      output difference,borrow;
      assign difference=((a^b)^bin);
      assign borrow=((~a&b)|(bin&(~(a^b))));
      endmodule

Developed by : Raagavi RM Register Number : 24900010

**RTL Schematic**

![WhatsApp Image 2024-12-07 at 17 51 24_7cad9d88](https://github.com/user-attachments/assets/39eee29e-e19e-470c-9ac1-33ce596f63be)

![WhatsApp Image 2024-12-07 at 17 51 23_1606f2db](https://github.com/user-attachments/assets/7f1e5833-8854-4eaf-9a4c-0d849bcb453d)


**Output Timing Waveform**

![WhatsApp Image 2024-12-07 at 17 52 11_073f059d](https://github.com/user-attachments/assets/2511d1b2-25f8-4de0-bfda-1b3662f457fa)

![WhatsApp Image 2024-12-07 at 17 52 11_e2b6e089](https://github.com/user-attachments/assets/ab7a9f6e-93ba-4463-9f8d-cd63dea8f129)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



