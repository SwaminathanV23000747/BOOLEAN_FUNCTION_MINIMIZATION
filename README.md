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

Developed by: RegisterNumber:*/
```
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module boolean_function(a,b,c,d,w,x,y,z,f1,f2);
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
//type code for f2 as like f1
and(s,ydash,y);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule
```

**RTL realization**
![Screenshot 2024-04-02 081651](https://github.com/SwaminathanV23000747/BOOLEAN_FUNCTION_MINIMIZATION/assets/148931113/29b51d74-65ca-4487-8187-9a2728d27e0f)

**Output:**
![Screenshot 2024-04-02 081637](https://github.com/SwaminathanV23000747/BOOLEAN_FUNCTION_MINIMIZATION/assets/148931113/0c5ebc72-3e5f-42a7-ac82-bb0864d2f16d)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

