# Tests on files

There are a range of checks we can do on files, some are listed.

* -d  Directory
* -e  Exists (also -a)
* -f   Regular file
* -r   Readable by you
* -s  Not empty &#x20;
* -w  Writable by you
* -N  Has been modified since last being read
* -nt   Test if file1 is newer than file 2. The modification date is used for this and the next comparison.
* -ot  Test if file1 is older than file 2.
* -ef  Test if file1 is a hard link to file2.

Let's try this! Remember, the quote around the expr is the one above the tab on the top left of the keyboard!!

```
#!/bin/bash
# By: John O'Raw
# Date: 24NOV19
# Function: Test for File and Directory
# Script: script17

echo "This script checks a file and directory to see if they exist"

# Check to see if we have two arguments
if [ $# -ne 2 ]
then
  echo "Usage - $0 x y"
  echo "Where x and y are FileName and Directory"
  exit 1
fi

if [ -f $2/$1 ]
then
  echo "This filename [$1] exists"
elif [ -d $1 ]
then
  echo "This dirname [$2] exists"
else
  echo "Neither [$2] or [$1] exist"
fi
 
exit 0
```
