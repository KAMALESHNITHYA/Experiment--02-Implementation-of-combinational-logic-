## NAME : KAMALESH R
## REGISTER NUMBER : 212223230094
# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
 
 
 
## Equipments Required: 
Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime


## Theory:
A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.

## Procedure:
1.Create a New Project:

  (i) Open Quartus and create a new project by selecting "File" > "New Project Wizard."
  (ii) Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2.Create a New Design File:

  (i) Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
  (ii) Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3.Write the Combinational Logic Code:

  (i) Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4.Compile the Project:

  (i) To compile the project, click on "Processing" > "Start Compilation" in the menu.
  (ii) Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5.Analyze and Fix Errors:

  (i) If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
  (ii )Review and fix any issues in your code if necessary.
  (iii) View the RTL diagram.

6.Verification:

  (i) Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
  (ii) Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
  (iii) Give the Input Combinations according to the Truth Table and then simulate the Output Waveform.

## Program:

Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

```
module combinationalcircuit(f1,a,b,c,d);
input a,b,c,d;
output f1;
wire abar,bbar,cbar,dbar,x1,x2,x3,x4,x5;
assign abar=~a;
assign bbar=~b;
assign cbar=~c;
assign dbar=~d;
assign x1=abar&bbar&cbar&dbar;
assign x2=a&cbar&dbar;
assign x3=bbar&c&dbar;
assign x4=abar&b&c&d;
assign x5=b&cbar&d;
assign f1=x1|x2|x3|x4|x5;
endmodule
```

## RTL realization
![image](https://github.com/KAMALESHNITHYA/Experiment--02-Implementation-of-combinational-logic-/assets/145743119/cde7e792-4b8d-4d69-a941-b896e459cc67)

## Truth Table:
![image](https://github.com/KAMALESHNITHYA/Experiment--02-Implementation-of-combinational-logic-/assets/145743119/4fa1f72f-f84f-4139-86be-212325727520)

## Timing Diagram
![image](https://github.com/KAMALESHNITHYA/Experiment--02-Implementation-of-combinational-logic-/assets/145743119/8ed31432-e36c-41f8-800a-dca1f5331081)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
