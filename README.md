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

module Boolean_min(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

and g1(s,ydash,z);
and g2(t,x,y);
and g3(u,w,z);
or g4(f2,s,t,u);
endmodule




```
**RTL realizetion**
![316396172-5ffd7097-c99c-4ef3-a82d-0108e72a8b9e](https://github.com/keerthigasudhagar/BOOLEAN_FUNCTION_MINIMIZATION/assets/163229129/f7b9d2fc-8e84-4951-bebf-ff0c1479b8e8)

**Timing Diagram**
![316396315-3294f442-723b-4550-ab9c-49ed60325deb](https://github.com/keerthigasudhagar/BOOLEAN_FUNCTION_MINIMIZATION/assets/163229129/460bf703-d1f1-4799-9304-08e7c4e778c9)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

