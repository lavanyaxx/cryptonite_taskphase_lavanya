# PERCEIVING PERMISSIONS

## CHANGING FILE OWNERSHIP

We can change the ownership of the files by using the chown command.

```chown [username] [file]```

In this challenge we had to change the ownership to the hacker and hence get the flag.

```chown hacker /flag```

## GROUPS AND FILES

Group ownership can be changed with the **chgrp** (change group) command.

We can check what groups you are part of with the **id** command.

In this challenge we had to change the group ownership to hacker and hence get the flag.

```chgrp hacker /flag```

## FUN WITH GROUPS NAMES

In this challenge we had to look for the randomized name of the group that the user is in 
by using the id command and hence get the flag by changing the group.

```id```
```chgrp grp23985 /flag```

## CHANGING PERMISSIONS

In this we learnt about the chmod (change mode) command for changing the permissions of the file.

Some important things to remember:

"r" = user/group/other can read the file (or list the directory)

"w" = user/group/other can modify the files (or create/delete files in the directory)

"x" = user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)

"-" = nothing 

In this challenge, we had to change the permissions of the /flag file to read it:

```chmod [OPTIONS] MODE FILE```


```chmod +r /flag```

## EXECUTABLE FILES

In the challenge we just had to make the files executable by using the following:

```chmod +x /challenge/run```

## PERMISSION TWEALING/SETTING PRACTICE

In this challenge we had to repeatedly use chmod to satisfy the given conditions and hence get the flag.

## THE SUID BIT '

There are many cases in which non-root users need elevated access to do certain system tasks. The system admin 
can't be there to give them the password every time a user wanted to do a task that only root/sudoers can do. 
The **"Set User ID" (SUID)** permissions bit allows the user to run a program as the owner of that program's file.

The s part in place of the executable bit means that the program is executable with SUID.

As the owner of a file, we can set a file's SUID bit by using chmod:

```chmod u+s [program]```




