# SHELL VARIABLES

## PRINTING VARIABLES

In this we learnt that we can also print variables by using echo by prepending the variable name with a "**$**"

```echo $FLAG```

## SETTING VARIABLES

We can assign variables by using "=" operator **without any spaces**.

 And the $ is only prepended to access variables and is a source of many potential vulnerabilities.

 ```PWN=COLLEGE```

 ## MULTI WORD VARIABLES

 To assign multi word variables we need to put them in " " because if we directly assign then the shell will
 consider the word after the space as a command

  ```PWN="COLLEGE YEAH"  ```

  ## EXPORTING VARIABLES

  Variables that we set in a shell session are local to that shell process.

  Hence we can export the variables by using the following command :

  ```export PWN=COLLEGE```

  ## PRINTING EXPORTED VARIABLES

  We can print the exported variables by using the **env** command.

  ## STORING COMMAND OUTPUT

  To store the output of any command we can do this by:

  ```PWN=$(/challenge/run)```
  ```echo "$PWN"```

  ## READING INPUT

  In this challenge we had to take the input from the user and assign the value of the variable by
  using the **read** command

  ```read -p "INPUT:" PWN```
  ```INPUT:COLLEGE```

  ## READING FILES

  This can be easily done by using the redirection command

  ```read PWN < /challenge/read_me```

  

    

 
