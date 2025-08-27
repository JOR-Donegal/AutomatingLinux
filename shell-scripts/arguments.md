# Arguments

At the start of this document we saw how to pass arguments. In this exercise, we will try and evaluate a range of positional parameters.

* $# allows us to get the number of command line arguments.
* $0 returns the command typed to call the script.
* $1 returns the first parameter passed to the script, $2 returns the second and so on.

Run the script below, using the command **script11 dog cat**

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Command Line Arguments
# Script: script12

echo "This script was called with $# arguments" 
echo "This script was called by $0" 
echo "The first parameter passed was $1, the second was $2"
exit 0

```

The shift command promotes each argument, allowing you to run through them in sequence. Try calling the script below with the command **script12 dog cat mouse**

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Command Line Arguments
# Script: script13

echo "The parameters are arg1=$1   arg2=$2   arg3=$3"
shift
echo "The parameters are arg1=$1   arg2=$2   arg3=$3"
shift
echo "The parameters are arg1=$1   arg2=$2   arg3=$3"
shift
echo "The parameters are arg1=$1   arg2=$2   arg3=$3"
shift
exit 0
```

We can view all the passed parameters by using **$\***

The **set** command allows us to set the arguments from within the script. This can be a handy way to deal with standard output from another programme.&#x20;

Try the command **date**. This will return a value like Fri Nov 26 11:03 GMT 2010.

We could consider that to be six arguments....?

Try the script below.

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Command Line Arguments
# Script: script14

set $(date)
echo $*
echo
echo "It is $1"
echo "The date is $3 $2"

exit 0
```
