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
![319946102-5f8fd602-1f64-4305-94ed-a00425815952](https://github.com/keerthigasudhagar/BOOLEAN_FUNCTION_MINIMIZATION/assets/163229129/4629493a-2f5c-43e2-9fbc-51c3fccbe744)


**Timing Diagram**

![316250520-e6c8b78e-c29b-46ee-aee9-29ee38d94cd0](https://github.com/keerthigasudhagar/BOOLEAN_FUNCTION_MINIMIZATION/assets/163229129/6391d811-af51-4e18-9461-3a68d1967d1a)
![319946818-12685259-eff6-4f38-a688-18485b77fe4a](https://github.com/keerthigasudhagar/BOOLEAN_FUNCTION_MINIMIZATION/assets/163229129/e308d527-5cc9-45ee-831a-84be836349d4)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
