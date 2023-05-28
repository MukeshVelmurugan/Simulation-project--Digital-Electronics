# TITLE
### 4-BIT PARITY GENERATOR
# SOFTWARE REQUIRED
#### Hardware : PC
#### Software : Quartus II Software
# THEORY
A 4-bit parity generator is a digital circuit that calculates the parity bit for a 4-bit binary input. The parity bit is used for error detection in data transmission or storage systems. The purpose of the parity bit is to ensure that the number of 1s in the data word, including the parity bit, is either even or odd.

Parity: Parity refers to the property of having an even or odd number of bits set to 1 in a binary sequence. In even parity, the number of 1s, including the parity bit, is even. In odd parity, the number of 1s, including the parity bit, is odd.

4-bit Binary Inputs: A 4-bit binary input consists of four individual bits, denoted as A, B, C, and D. Each bit can have a value of either 0 or 1.

Parity Bit Calculation: The parity bit is calculated by performing an XOR (exclusive OR) operation on the four input bits. XOR returns 1 if the number of 1s is odd, and 0 if the number of 1s is even.

Circuit Implementation: The 4-bit parity generator circuit consists of four input lines (A, B, C, D), one output line for the parity bit (P), and an XOR gate. The XOR gate takes the four input lines as inputs and produces the output parity bit (P).

Truth Table: The truth table for the 4-bit parity generator lists all possible combinations of the four input bits (A, B, C, D) and the corresponding parity bit (P) calculated using the XOR operation.

# LOGIC DIAGRAM
![XOR](https://github.com/MukeshVelmurugan/Simulation-project--Digital-Electronics/assets/118707363/175c70c0-8d8b-4683-a1ba-d07229ecf619)

# ODD PARITY
### PROGRAM
``` VERILOG
PROGRAM DEVELOPED BY : MUKESH V
REG NO : 212222230086

module parity(a,b,c,d,p);
input a,b,c,d;
output p;
xor(p,a,b,c,d);
endmodule
```
### NETLIST DIAGRAM
![image](https://github.com/MukeshVelmurugan/Simulation-project--Digital-Electronics/assets/118707363/103bb11e-3c50-4c2f-bf2a-25f68600c8b7)


### TIMING DIAGRAM
![image](https://github.com/MukeshVelmurugan/Simulation-project--Digital-Electronics/assets/118707363/0be6f09f-6ec2-40c2-b880-c1c95521f990)

### TRUTH TABLE
![image](https://github.com/MukeshVelmurugan/Simulation-project--Digital-Electronics/assets/118707363/45306121-ab7d-4400-b597-825612310d9e)

# EVEN PARITY
### PROGRAM
``` VERILOG
PROGRAM DEVELOPED BY : MUKESH V
REG NO : 212222230086

module evenparity(a,b,c,d,p);
input a,b,c,d;
output p;
assign p = ~(a ^ b ^ c ^ d);
endmodule
```
### NETLIST DIAGRAM
![image](https://github.com/MukeshVelmurugan/Simulation-project--Digital-Electronics/assets/118707363/2a43ec88-7c73-4c13-81b5-7efcc40d9a37)


### TIMING DIAGRAM
![image](https://github.com/MukeshVelmurugan/Simulation-project--Digital-Electronics/assets/118707363/d0b1f516-d557-4bfa-a499-693a5ffa3b39)

### TRUTH TABLE
![image](https://github.com/MukeshVelmurugan/Simulation-project--Digital-Electronics/assets/118707363/302e5337-b827-4d61-86c5-5e63ae039fe6)

# REFERENCE
https://codestall.wordpress.com/2017/09/04/parity-generator-in-verilog/
