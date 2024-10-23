# Pondering_PATH

## THE PATH VARIABLE

There is a special shell variable, called **PATH**, that stores a bunch of directory paths in
which the shell will search for programs corresponding to commands.

Without a PATH, bash cannot find the ls command.

```export PATH=""```

```/challenge/run```

## SETTING PATH

By adding directories to or replacing directories in this list, we can expose these programs to be
launched using their bare name.

The challenge was :

Let's practice. This level's /challenge/run will run the win command via its bare name, but this command exists 
in the /challenge/more_commands/ directory, which is not initially in the PATH. The win command is the only thing 
that /challenge/run needs, so you can just overwrite PATH with that one directory. Good luck!

```export PATH="/challenge/more_commands"```

```/challenge/run```

## ADDING COMMANDS

In this challenge we had to make a shell script called win, add its location to the PATH, and
enable /challenge/run to find it.

``` mkdir -p /home/hacker/my_commands```

``` nano /home/hacker/my_commands/win```

 ```chmod +x /home/hacker/my_commands/win```

 ## HIJACKING COMMANDS

This challenge deleted the flag using the rm command. 

  ```mkdir -p /home/hacker/fake_commands ```

 ``` nano /home/hacker/fake_commands/rm ```

  ```chmod +x /home/hacker/fake_commands/rm ```

  ```export PATH="/home/hacker/fake_commands:$PATH"```
