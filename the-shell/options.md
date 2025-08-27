# Options

Consider the **ls** command.

**ls** is a single command which gives a listing of the working directory.

**ls -l** is a single command with one option specified which gives a long listing of the working directory.

**ls** worked a bit different from **copy**. Rather than having arguments is has options. Options are a special type of argument which modify the behaviour of a command. With most commands, the options come first and then the arguments.

For example, what does the command &#x20;

```
ls -l *.txt
```

do?

One special case is the command option **--help** which can be very useful to get help!

For example, try&#x20;

```
ls --help
```

In some case we may need to string multiple options together. Try the following sequence of commands.

```
ls -i
ls -l
ls -il
```

The two options are concatenated and **ls** does both.
