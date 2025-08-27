# Processes

A process could be defined as a running instance of a programme. Each process is identified by a process ID. Any modern OS can run multiple processes at once and each process is assigned its own block of memory and this may be further subdivided for code, data, stack, heap, etc.

A command typed in the terminal causes the shell to fork a new process. A fork() function is an operation where a process creates a copy of itself as a child process; the original thread of execution is duplicated.

After the new process is created, the child process calls an exec function which clears its original contents and tries to run the new programme, the original command. If the command refers to a binary executable programme created in (for example) C, then exec() succeeds, and the binary programme is overlaid into the new shell. If the exec() call fails, the shell assumes it is dealing with a shell script and tries to execute the commands in the script.

The following script shows the hierarchy of processes, starting from init() which is always process 1.

```
#!/bin/bash
# By: John O'Raw
# Date: 17NOV19
# Function: Show the process tree
# Script: script3
echo " The following processes are running"
ps -f
read -p "Press return to continue"
echo "This script will show the process tree for" $HOSTNAME
read -p "Press return to continue"
pstree | less
exit 0
```

One interesting option is to use the **&** symbol when running a command. This tells the operating system to run a process in the background.
