# Using seq

When we are iterating through a list, the **seq** command can be very handy. Go to the command prompt and type&#x20;

```
seq 10
```

Very handily, it has iterated through numbers from 1 to 10.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

In a case where I want to iterate through something, this gives me nice, tight code.

Consider the script below where I use indexnumber as a variable.&#x20;

```
#!/bin/bash
# By: John O'Raw
# Date: 27NOV19
# Function: Simple number check
# Script: script11

for indexnumber in ‘seq 10’
do
    touch TextFile$indexnumber.txt
done

```

The result will be;

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
