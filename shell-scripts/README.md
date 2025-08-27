# Shell Scripts

We have covered the background, now we are going to work through creating a first script. At the command prompt, type the command;

```
echo $USER
```

This command takes the environment variable USER and echoes it to standard output e.g. the screen. Every user has a user/password combination in a file called /etc/passwd and these entries also store data relating to your group and login shell.

We could use **grep** to find it. Try the command

```
grep $USER /etc/passwd
```

This will take your user name as a search parameter and look for it in the password file.

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

We can take this simple command and include it in a file which we can then run. Make a directory called **scripts** and then make this you’re working directory. All future scripts will be stored here!

Using **nano**, create the following text file (change the editor name etc. to match your own) and call it **script1.sh**

The hash symbol (**#**) introduces a comment; this line is not further processed.

```
# By: John O'Raw
# Date: 17NOV10
# Function: show the users entry in the password file
# Script: script1
grep $USER /etc/passwd
exit 0
```

Now do an **ll** to make sure the file is there. The editor just creates text files, we need to change the permissions on the file to make it executable.

Try the command&#x20;

```
chmod u+rx script1
```

Now do another **ll.**

What happened?

To run our first script, we have one more problem!

Our script directory is not in the path, so if we try to run it, the shell will search for the script and not find it, even though we are in the working directory with the script. To run we need to tell the shell to run it from the working directory. Try the command;

```
./script1.sh
```
