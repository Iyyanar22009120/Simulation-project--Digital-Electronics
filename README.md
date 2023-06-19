# TITTLE
Design and simulate the logic diagram using Verilog.
# THEORY
The parity generating technique is one of the most widely used error detection techniques for the data transmission. In digital systems, when binary data is transmitted and processed, data may be subjected to noise so that such noise can alter 0s (of data bits) to 1s and 1s to 0s.

Hence, a Parity Bit is added to the word containing data in order to make number of 1s either even or odd. The message containing the data bits along with parity bit is transmitted from transmitter to the receiver.

Parity Generator is a combinational logic circuit that generates the parity bit in the transmitter. On the other hand, a circuit that checks the parity in the receiver is called Parity Checker. A combined circuit or device of parity generators and parity checkers are commonly used in digital systems to detect the single bit errors in the transmitted data.
# LOGIC DIAGRAM
![image](https://github.com/Iyyanar22009120/Simulation-project--Digital-Electronics/assets/118680259/1d588111-c064-4a5b-9f82-cee68eea61c7)
# NETLIST DIAGRAM
![rtl skill](https://github.com/Iyyanar22009120/Simulation-project--Digital-Electronics/assets/118680259/6333ef72-3cec-4e63-a3f4-89460753a6bb)

# TIMING DIAGRAM
![timing skill](https://github.com/Iyyanar22009120/Simulation-project--Digital-Electronics/assets/118680259/f398c7a6-6358-4f7e-a241-d49d02bf3ac0)

# PROGRAM
```
module logic(x,y,z,f,fbar);
input x,y,z;
output f,fbar;
wire xbar,ybar,zbar,a,b;
not(xbar,x);
not(ybar,y);
not(zbar,z);
and(a,x,ybar);
and(b,xbar,y);
or(fbar,a,b,zbar);
not(f,fbar);
endmodule
```
# REFERENCE
```
PROGRAM DEVELOPED BY:IYYANAR S
REFERENCE NO:212222240036
```
