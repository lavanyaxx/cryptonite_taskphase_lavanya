# PROCESSES AND JOBS

## LISTING PROCESSES

In this we learnt about the ps command which stands for "process status" and it lists the running processes in the terminal.

"Standard" Syntax: in this syntax, we can use -e to list "every" process and -f for a "full format" output, 
including arguments. These can be combined into a single argument -ef.

"BSD" Syntax: in this syntax, we can use a to list processes for all users, x to list processes that aren't 
running in a terminal, and u for a "user-readable" output. These can be combined into a single argument aux.

In this challenge we had to find the random filename by using the above commands and further print the flag

```ps -ef```

## KILLING PROCESSES

We can use the **kill** command to terminate it by passing the process identifier(PID)

```ps aux | grep dont_run```
```kill 73 ```
```/challenge/run```

## INTERRUPTING PROCESSES

Sometimes we just want to get rid of the process that's clogging up your terminal. We can use **Ctrl-C** for this to 
"interrupt" to whatever application is waiting on input from the terminal and, typically, this causes the application to cleanly exit.

## SUSPENDING PROCESSES

We can suspend processes to the background with Ctrl-Z.

In this challenge we just had to suspend /challenge/run once and launch it again.

## RESUMING PROCESSES

We can easily resume the processes by using the **fg** command.

## BACKGROUNDING PROCESSES

We can resume the processes in the backgroud by using the **bg** command.

This will allow the process to keep running, while giving us our shell back to invoke more commands in the meantime.

## FOREGROUNDING PROCESSES

We can foreground a backgrounded process with **fg** just like we foreground a suspended process.

## STARTING BACKGROUNDED PROCESSES

We can do this by appending a "&" after the command.

```/challenge/run &```

## PROCESS EXIT CODES

Every shell command, including every program and every builtin, exits with an exit code when it finishes running and terminates.


This can be used by the shell, or the user of the shell to check if the process succeeded in its functionality.

We can access the exit code of the most recently-terminated command using the special ? variable and prepending it with $ to read its value.

```/challenge/get-code $?```


```echo $?```


```/challenge/submit-code 60```

