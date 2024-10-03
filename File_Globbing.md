# FILE GLOBBING

## MATCHING WITH *

When it encounters a * character in any argument, the shell will treat it as 
"wildcard" and try to replace that argument with any files that match the pattern.

The * matches any part of the filename except for "**/**" or a leading "**.**" character

In this challenge we had to change the directory to /challenge by using atmost 4 characters:

```cd /c*e```

## MATCHING WITH ?

When it encounters a ? character in any argument, the shell will treat it as
**single-character** wildcard. This works like *, but only matches one character.

In this challenge we had to use ? in place of "l" and "c" and change the directory

```cd /?ha??enge```

## MATCHING WITH []

The square brackes are, essentially, a limited form of ?, in that instead of matching 
any character, [] is a wildcard for some subset of potential characters, specified within the brackets.


For example, [pwn] will match the character p, w, or n.

In this challenge we had to run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h:

```/challenge/run file_[bash]```

## MATCHING PATHS WITH []

Globbing happens on a path basis, so we can expand entire paths with your globbed arguments.

In this challenge we had to expand the specified paths to get the flag:

```/challenge/run /challenge/files/file_[bash]```

## MIXING GLOBS

In this challenge, we had to write a single, short (6 characters or less) glob that will match the files "challenging", "educational", and "pwning"

```/challenge/run [cep]*```

## EXCLUSIONARY GLOBBING

[] also helps in filtering out the globs by using "!" or "^" as the first character in the bracket. The glob inverts, and that bracket
instance matches characters that aren't listed.

In this challenge we had to find all files that dont start with p,w,n:

```/challenge/run [!pwn]*```






