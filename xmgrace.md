#### 1. Plot multiple files with multiple data columns. This example plots the 1st column as x axis and 5th column as y axis. 
```
$xmgrace -block q1.dat -bxy 1:5 -block q2.dat -bxy 1:5 -block q3.dat -bxy 1:5
```

#### 2. Axis label
```
\1 : start italics
\0: end italics
\s: start subscript
\S: start superscript
\N: end subscript or superscript
\cE\C: angstrom symbol
```

#### 3. Plot `x = y` line for parity plot
```
a. data > transformation > evaluate expression
b. right click on the data set > create new > by formula
c. set starting and ending point, and set an arbitrary length. Set y = $t and x = $t
```

#### 4. Plot probability histogram (e.g., umbrella sampling and WHAM. interparticle distance as a function of time)
```
a. data > transformation > histogram
b. in the new dialog, select data under "source" on the left side, 
   check the "normalize" box 
c. set the start and end point, and set the number of bins for the histogram
d. click "apply"
e. this will duplicate the original data. Hide the original data under "source"
   and select the new data under "destination"
f. autoscale the graph 
g. to change the histogram structure, can consider doing the following:
   * line property: straight 
   * line > unselect "draw drop lines"
   * fill properties: "to baseline" 
```

#### 5. Change the canvas size
```
a. file > print setup > letter > custom > set dimension (e.g. 1000x1000, dpi = 300) > apply
b. edit > arrange graphs > make arrangements accordingly > apply 
```

6. Save to xmgrace agr/image file. Perform this step after step 5.  
```
a. file > save as > type <filename>.agr at the destination
b. if save as png, redo step 5 except choose "png"/"jpeg" instead of "PostScript" as the device
   Then file > print
```
