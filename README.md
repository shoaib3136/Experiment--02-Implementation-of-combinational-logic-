# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
# AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.

i.) F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

ii.) F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
# Equipments Required:
i.) Hardware – PCs, Cyclone II , USB flasher

ii.) Software – Quartus prime


# Theory:
The above expressions one and two are reduced into their minimal form by taking common variables from them and applying k-map, theorems to it.

# Procedure:
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.


# Program:
```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Shaik Shoaib Nawaz
RegisterNumber: 212222240094 
*/
i.)
module exp2 (a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (~b & ~d) | (~a &b & d) | (a & b & ~c);
endmodule

ii.)
module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = (x&y) | (y&w) | (`y&z);
endmodule

```

# Output:
## RTL:
i.) For f1:
![rtl](./images/def1(exp2)logic.png)

ii.) For f2:
![rtl](./images/def2(exp2)logic.png)

# Timing Diagram:
i.) For f1:
![rtl](./images/def1(exp2)time.png)

ii.) For f2:
![rtl](./images/def2(exp2)time.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
