# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:Keerthika.S
RegisterNumber:212223040093

**program**

```
module combinationalcircuit(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign F1=x1|x2|x3|x4|x5;
endmodule
```
**RTL realization**
![312535957-dbd64921-6857-40ee-a21b-55fa17e9f89b](https://github.com/keerthigasudhagar/BOOLEAN_FUNCTION_MINIMIZATION/assets/163229129/20c74833-19b9-4b3e-b48c-b11a1136280d)

**Truth table**
![312536822-849f41b1-394f-48f4-b451-88315b927f79](https://github.com/keerthigasudhagar/BOOLEAN_FUNCTION_MINIMIZATION/assets/163229129/d43706c9-ae4d-4974-8e6f-3763deb24a9b)


**Timing Diagram**
![312537126-533d1307-308c-4a6d-9495-b6f289bf8479](https://github.com/keerthigasudhagar/BOOLEAN_FUNCTION_MINIMIZATION/assets/163229129/7021421e-a601-455b-b518-5b5ea0886dc4)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

