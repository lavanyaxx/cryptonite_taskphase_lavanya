# DIGESTING DOCUMENTATION

## LEARNING FROM DOCUMENTATION

A typical need for documentation s just to figure out how to use all these dang programs,
and a specific case of that is figuring out what arguments to specify on the command line.

In this we just had to give the argument properly as:

```/challenge/challenge --giveflag```

## LEARNING COMPLEX USAGE 

In this challenge, we just had to add the /flag after the argument.

```/challenge/challenge --printfile /flag```

## READING MANUALS

The **man** command is short for manual and will display (if available) the manual of 
the command you pass as an argument.

When you're done reading the manpage, you can hit **q** to quit.

In this challenge we had to learn about "challenge" using:

```man challenge```

And then inturn print the flag by analysing.

## SEARCHING MANUALS

We can scroll man pages with the arrow keys (and PgUp/PgDn) and search with **/**.

After searching, we can hit **n** to go to the next result and **N** to go to the previous result.

Instead of /, we can use ? to search backwards.

In this challenge we had to learn about "challenge" by using the man command and further search
for the flag by using the "/" and hence print it.

```man challenge```
```/challenge/challenge --aeu```

The flag was present in "--aue".


## SEARCHING FOR MANUALS 

In this first we went throught the manual of man by using:

```man man```

Then found out about the command:

```man -k challenge```

Which basically searched short descriptions and manual page names for the  keyword ** challenge**  as
regular expression and print out any matches.

And then finally found the flag by using "man challenge".

## HELPFUL PROGRAMS

In this we had to search for manpage using the "**--help**" command and with further information get the flag.

## HELP FOR BUILTINS

Some commands, rather than being programs with man pages and help options, are built into the shell itself. 
These are called builtins. Builtins are invoked just like commands, but the shell handles them internally 
instead of launching other programs. 

In this challenge we used:

```help challenge```

