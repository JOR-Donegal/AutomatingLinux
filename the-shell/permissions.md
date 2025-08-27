# Permissions

You have already covered file permissions, this is a quick recap.

Try an **ll** command at the command prompt. Look at the leftmost part of the screen. There are a group of 10 characters in the format _drwxrwxrwx_. The first character defines the file type, in this case we can have d for directory or - for a regular file. There are some other possibilities,

* b for a block device
* c for a character device
* p for a pipe
* l for a symbolic link

The next nine characters are the access permissions of each file. The first three _rwx_ specifies whether the file's owner can read, write or execute the file. Execute in this context means run the file as a programme, that it contains a list of instructions which can be understood by the shell. You can tell who the owner is by looking in the leftmost name column. The second three _rwx_ specifies whether the file's group can read write or execute the file. You can tell who the group is by looking in the rightmost name column. The final three _rwx_ specifies whether anyone else can read write or execute the file.

Sometimes I switch user (**su**) to root to do things I would not normally be allowed to do. For this reason, a few files and folders are owned by root.

Open a terminal window and create a folder called **MyTest**. Do an **su** and create a folder called **RootTest**. Type **exit** to switch back from root to your normal login. Do an **ll** command.&#x20;

What are the owner, group and permissions on the directories?&#x20;

Now use **rmdir** command to remove both directories. Can you do so? Why not? Can you figure out how to delete **RootTest**?

The main reason we have looked at permissions now is that we need to be able to make simple permission changes to be able to run shell script files. To do this we use the **chmod** command with some arguments.

* chmod a+rx adds read and execute for all users
* chmod u+wx adds write and execute for the owner (or current user)
* chmod g+x adds execute for the group
* chmod o+rwx adds read, write and execute for the everyone.

Similarly,

* chmod a-rx removes read and execute for all users
* chmod o-rwx removes read, write and execute for the everyone.

Create a directory called **dummy**. Try different combinations of the **chmod** command, alternating with **ll** to see what the effect is.

Delete all three directories when finished.
