# UNTANGLING USERS

## BECOMING ROOT WITH SU

In this challenge we learnt about the **su (the switch user command)** 

su is discerning: before allowing the user to elevate privileges to root, it checks to make sure that the user knows the root password.
This check against the root password is what obsoletes su.

Here we just had to run the su command and enter the password to hence get the flag

## OTHER USERS WITH SU

We can also give a username as an argument to switch to that user instead of root.

```su zardus```

## CRACKING PASSWORDS

If a hacker gets their hands on a leaked /etc/shadow, they can start cracking passwords and wreaking havoc.

The cracking can be done via the famous John the Ripper.

```john /challenge/shadow-leak```

Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04866g/s 283.3p/s 283.3c/s 283.3C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed

So here we got the password as aardvark.

## USING SUDO 

Unlike su, which defaults to launching a shell as a specified user, sudo(superuser do) defaults to running a command as root.

Also unlike su, rather than authenticating via password, sudo relies on policies that
it checks to determine the user's authorization run things as root.

```sudo cat /flag```



