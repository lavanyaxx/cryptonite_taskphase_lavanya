# PRACTICING PIPING

## REDIRECTING OUTPUT

We can redirect the output to different files by using the ">" character.

In this challenge we just had to input redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

## REDIRECTING MORE OUTPUT

We can also redirect the output of any command.

```/challenge/run > myflag```

## APPENDING OUTPUT

This is basically used for running a bunch of commands, saving their output and grepping through it later.

We can redirect input in append mode using ">>"

```/challenge/run >> /home/hacker/the-flag```

## REDIRECTING ERRORS

Just like standard output, we can also redirect the error channel of commands.

A File Descriptor (FD) is a number the describes a communication channel in Linux.
FD 0: Standard Input
FD 1: Standard Output
FD 2: Standard Error

In this challenge we had to redirect the output of /challenge/run, like before, to myflag, and the "errors" (in our case, the instructions) to instructions.

```/challenge/run > myflag 2> instructions```

## REDIRECTING INPUT 

We can also redirect input to the programs by using the "<" character.

In this challenge we were required to redirect the PWN file to /challenge/run and have the PWN file contain the value COLLEGE.

```echo "COLLEGE" > PWN
/challenge/run < PWN```

## GREPPING STORED RESULTS

In this challenge we simply had to redirect the output of /challenge/run to /tmp/data.txt and grep the flag.

Important thing was to remember that flag always starts with "pwn.college" during grepping.

## GREPPING LIVE OUTPUT

In this we learnt about the pipe operator "|".

Standard output from the command to the left of the pipe will be connected to (piped into) the standard input of the command to the right of the pipe.

```/challenge/run | grep "pwn.college"```

## GREPPING ERRORS

The shell has a >& operator, which redirects a file descriptor to another file descriptor.

This means that we can have a two-step process to grep through errors: 
First, we redirect standard error to standard output (2>& 1) and then pipe the now-combined stderr and stdout as normal (|)

```/challenge/run 2>&1 | grep "pwn.college"```

## DUPLICATING PIPED DATA WITH tee

The tee command, named after a "T-splitter" from plumbing pipes, duplicates data flowing through our pipes to any number of files provided on the command line.

## WRITING TO MULTIPLE PROGRAMS

In this challenge we just had to run the /challenge/hack command, and duplicate its output as input to both the /challenge/the and the /challenge/planet commands.

```/challenge/hack | tee >( /challenge/the ) >( /challenge/planet )```

## SPLIT PIPING STDERR AND STDOUT

In this challenge, we had to:
/challenge/hack: this produces data on stdout and stderr
/challenge/the: you must redirect hack's stderr to this program
/challenge/planet: you must redirect hack's stdout to this program

```/challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )```
