# COMPREHENDING COMMANDS

## CAT FUNCTION 

cat is most often used for reading out files. cat will concatenate (hence the name) multiple files if provided multiple arguments.
In this we just had to capture the flag by

```cat flag```

We can also **cat absolute paths** by specifying the absolute path after the cat function. We can use this directly without using the **cd** command.

example- cat /challenge/DESCRIPTION.md

## GREPPING FUNCTION

Sometimes, the files that we might cat out are too big. Luckily, we have the grep command to search for the contents we need.

We just simply had to use it as:

```grep SEARCH_STRING /path/to/file```

## LISTING FILES 

ls will list files in all the directories provided to it as arguments.

```ls /challenge```

This gives all the files in the directory "/challenge"

## TOUCHING FILES 

The "touch" command is used to create files 

```touch pwn```

## REMOVING FILES 

The "rm" command is use to remove the files.

```rm pwn```

## HIDDEN FILES 

ls doesnt list all the files by default. Linux has a convention where all the files starting with "." dont show up by default in ls.
We have to use "ls -a" for this.

```ls -a /challenge```

## MAKING DIRECTORIES 

We can make directories by using the "**mkdir**" command.

```mkdir /tmp/pwn```

## FINDING FILES 

The find command takes optional arguments describing the search criteria and the search location. If we don't 
specify a search criteria, find matches every file. If we don't specify a search location, find uses the 
current working directory.

```find / flag```

This is used for searching the whole filesytem and then inturn searching for the flag in different absolute paths provided.

## LINKING FILES 

Linux comes in two flavors: hard and soft(symbolic) links.

Symbolic links are the most popular and better than hard links.

Symbolic links are created with the ln command with the -s argument. 

**The original file path comes before the link path in the command.**

```ln -s /flag /home/hacker/not-the-flag```




