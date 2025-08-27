# Using vi

**vi** is the most ubiquitous screen-oriented text editor. Much of the behaviour of **vi** and **ex** was standardized by the Single Unix Specification and POSIX. The original **vi** program was written by Bill Joy in 1976 for an early BSD Unix release and most current versions of **vi** are largely compatible re-implementations of this original version. The name vi is derived from the shortest unambiguous abbreviation for the command visual in **ex**.

**vi** is important to us!

Although unfriendly and awkward to use, it is the one editor that you can be sure is pre-loaded in every version of Unix or Linux you will experience. There are many better editors, but it is strongly recommended you learn to fall back on **vi** as you will have to some day!

In many Linux implementations, **vi** has been replaced by **vim**, Vi IMproved. This is now amongst the most popular editors available for Linux. A GUI version of **vim** also exists. There is a tutor built into **vim**. Try opening a terminal window and typing **vimtutor**.

With **ed** we saw that two modes exist, command mode and insert mode. The same applies to **vi** and the commands to move between the two modes are the same.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

vi lets you create new files or edit existing ones. Try the command

```
vi viFile1.txt
```

This file does not exist, so vi creates it. Each blank line is marked by a \~ symbol (pronounced "tilda"). At the bottom of the file is the file name and the response \[New File]. As previously mentioned, **vi** has two modes and to get out of **vi** we must be in command mode, so press the escape key \[escape] followed by **:q**

```
[esc]
:q [return]
```

&#x20;You should now be back at the command prompt.

We got in and out of **vi**, but if you check, we didn't create anything! Try the command

```
vi viFile1.txt
```

This time, we will add some text. Type **a** to append, then add the lines below, press return at the end of a line.

```
This is a text file written using vi. [return]
This is the last line in the file when created. [return]
```

&#x20;Type&#x20;

```
[escape] 
:wq 
```

to enter command mode, write and quit.

```
:wq
```

Use **cat** to make sure the file is there and looks as it should!

To edit this file, use the command

```
vi viFile1.txt
```

This time, we will insert some text. Move the cursor to the end of the first line of text, enter insert mode then add the lines below (press return if you need a new line).

```
i [return]
This is a new line written using vi in insert mode. [return]
This is the last line in the file when edited. [return]
```

Type the following to enter command mode, write and quit;

```
[escape]
:wq [return]
```

&#x20; Use **cat** to make sure the file is there and looks as it should.

If you make a mess of your edit, you can exit without saving. Use the command

```
vi viFile1.txt
```

This time, we will insert some mangled text. Move the cursor to the end of the first line of text, the enter insert mode, then add the lines below (press return if you need a new line).

```
i [return]
This is a new line mangled using vi in insert mode. [return]
```

Then type

```
[escape]
:q!
```

&#x20;to enter command mode, and quit without saving.&#x20;

Use **cat** to make sure the file is there and looks as it should. There are very many commands for **vi** and **vim**, review them either through the tutor package or on-line.
