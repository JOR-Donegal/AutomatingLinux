# Flow Control

Most languages have the concept of loops: If we want to repeat a task twenty times, we don't want to have to type in the code twenty times, with maybe a slight change each time. As a result, we have for and while loops in the Bourne shell. Try the following programme.

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Show users who are logged on
# Script: script6

for i in 1 2 3 4 5 
do   
    echo "Looping ... number $i" 
done
exit 0

```

Even more usefully, we can loop through all the files in the current directory.

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV10
# Function: List all the files in home directory
# Script: script7

for file in ~
do   
    ls -l 
done
exit 0
```

We can also have while loops. Try the code below. Notice the use of the read command to get input from the user. Be careful, there are spaces between the 3 fields in the test brackets \[], it’s hard to see them on the web page, so let me explain in RED!

When typing, its \[<mark style="color:red;">SPACE</mark>"$INPUT\_STRING"<mark style="color:red;">SPACE</mark>!=<mark style="color:red;">SPACE</mark>"bye"<mark style="color:red;">SPACE</mark>]&#x20;

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Show users who are logged on
# Script: script8

INPUT_STRING=hello 
while [ "$INPUT_STRING" != "bye" ] 
do   
    echo "Please type something in (bye to quit)"   
    read INPUT_STRING   
    echo "You typed: $INPUT_STRING" 
done
exit 0

```

In C or Java, you will have seen flow commands which allow you to select one of a number of possibilities. Depending on the language, this is referred to as switch, select case, case, etc.

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Check language for hello greeting
# Script: script9

echo "press [ctrl][c] to exit"

while read f
do
case $f in
    Hello)                 echo English    ;;
    "Dia Duit")         echo Irish          ;;
    Ciao)                  echo Italian       ;;
    *)                       echo Unknown: $f
;;
esac
done
exit 0
```
