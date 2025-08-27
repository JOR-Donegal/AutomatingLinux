# If loops

One very powerful construct in most languages is if-then-else. We have a construction of this nature in Linux, and we will also use this to demonstrate a range of tests. We finish the construct with fi, which is the only case I know where we use if backwards! The structure is;

```
If condition is true
then
               do stuff
else
               do other stuff
fi
```

&#x20;We need comparisons for our **if** command, something to check conditions against. Some examples are;

<table data-header-hidden><thead><tr><th width="169"></th><th></th></tr></thead><tbody><tr><td>str1 = str2</td><td>Returns true (0) if strings are equal, false (-1) if not</td></tr><tr><td>str1 != str2</td><td>Returns false (-1) if strings are equal, true (0) if not</td></tr><tr><td>exp1 -eq exp2</td><td>Returns true (0) if expressions are equal, false (-1) if not</td></tr><tr><td>exp1 -ne exp2</td><td>Returns false (-1) if expressions are equal, true (0) if not</td></tr><tr><td>exp1 -gt exp2</td><td>Returns true (0) if exp1 is greater than exp2, false (-1) if not</td></tr><tr><td>exp1 -ge exp2</td><td>Returns true (0) if exp1 is greater than or equal to exp2, false (-1) if not</td></tr><tr><td>exp1 -lt exp2</td><td>Returns true (0) if exp1 is less than exp2, false (-1) if not</td></tr><tr><td>exp1 -ge exp2</td><td>Returns true (0) if exp1 is less than or equal to exp2, false (-1) if not</td></tr></tbody></table>

In both cases, the script is successful, so we return an exit code of “0”. An if-then-else-fi structure is perfect for handling exit codes.

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Simple number check
# Script: script10

X=-4
# Check if less than
if [ "$X" -lt "0" ]
then
    echo "X is less than zero"
    exit 0
else
    echo "X is greater than zero"
    exit 0
fi

```

Modify the above programme to take X (the value to be tested) from user using the **read** command.
