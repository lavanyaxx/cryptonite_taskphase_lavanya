# PONDERING PATHS 

## THE ROOT 

In this we learnt that the filesystem starts at /. Under that, there are a whole mess of other directories, configuration files, programs.
One that starts with the root directory, is referred to as an "absolute path" which starts from "/". We had to print "**/pwn**" to get the flag.

## PROGRAM AND ABSOLUTE PATHS

In this we had to execute the run file which was in the challenge directory.

```/challenge/run```

## POSITION THY SELF, ELSEWHERE, YET ELSEWHERE

In this we learnt that each process has a directory in which it is currently hanging out. We can navigate around the directories by using the "**cd**" command.

```cd /```

## IMPLICIT RELATIVE PATHS, from /

In this we learnt that the current working directory does matter for relative paths. A relative path is any path that does not start at root (i.e., it does not start with /).
For example, if we want to access some file located at /tmp/a/b/my_file, and cwd is /, then the relative path to the file will be tmp/a/b/my_file.

## EXPLICIT RELATIVE PATHS, from /

In this we learnt that every directory has two implicit entries that we can reference in paths: . and ..
All of these absolute paths are identical:
/challenge
/challenge/.
/challenge/./././././././././
/./././challenge/././

All these relative paths are identical:
challenge
./challenge
./././challenge
challenge/.

## HOME SWEET HOME 

We learnt that the expansion of ~ is an absolute path, and only the leading ~ is expanded.

In this /challeng/run had to write a copy of the flag keeping the following conditions in mind:
Your argument must be an absolute path.
The path must be inside your home directory.
Before expansion, your argument must be three characters or less.

```/challenge/run ~/k```


