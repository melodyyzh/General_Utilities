1. Plot multiple files with multiple data columns. This example plots the 1st column as x axis and 5th column as y axis. 
```
$xmgrace -block q1.dat -bxy 1:5 -block q2.dat -bxy 1:5 -block q3.dat -bxy 1:5
```
2. Axis label
```
\1 : start italics
\0: end italics
\s: start subscript
\S: start superscript
\N: end subscript or superscript
```
3. Plot `x = y` line for parity plot
```
a. data > transformation > evaluate expression
b. right click on the data set > create new > by formula
c. set starting and ending point, and set an arbitrary length. Set y = $t and x = $t
```
