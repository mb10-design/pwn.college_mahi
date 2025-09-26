# Matching with *

### Gobble the directory challenge 
**Flag:**  `pwn.college{83HHF01kZ8Z5aBySvlh3nS-hGSY.QXxIDO0wCN2kjNzEzW}`

We cd into /challenge by using gobbling and get the flag by running /challenge/run

```
hacker@globbing~matching-with-:/challenge$ cd /c*e
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{83HHF01kZ8Z5aBySvlh3nS-hGSY.QXxIDO0wCN2kjNzEzW}

```

## What I learnt

When we encounter a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files that match the pattern.

# Matching with ?

### Use ? to enter /challenge directory
**Flag:**  `pwn.college{MXPWlKk-md5XOnlkDuC6GvcU0DK.QXyIDO0wCN2kjNzEzW}`

We enter the challenge directory and get the flag by running /challenge/run.

```
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{MXPWlKk-md5XOnlkDuC6GvcU0DK.QXyIDO0wCN2kjNzEzW}

```

## What I learnt


?-Matches 1 character 


# Matching with[]

### Go to /challenge/files and run /challenge/run using []
**Flag:** `pwn.college{UOWkNOTw_wSPkBhp_TLtL_dtpeU.QXzIDO0wCN2kjNzEzW}`

Once we get into the given directory we run /challenge/run with argument files_[bash]

```
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{UOWkNOTw_wSPkBhp_TLtL_dtpeU.QXzIDO0wCN2kjNzEzW}

```

## What I learnt 

The square brackets are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters, specified within the brackets.


# Matching paths with []

###  Starting from your home directory, run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files!

**Flag:**  `pwn.college{QVSdPbHLRyDa14v57ZdtDInE2QH.QX0IDO0wCN2kjNzEzW}`
`

We need to run the command /challenge/run with the path that leads to the above mentioned files. The path is /challenge/files.

```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{QVSdPbHLRyDa14v57ZdtDInE2QH.QX0IDO0wCN2kjNzEzW}

```

## What I learnt

How to expand paths with gobbled arguments.

# Multiple globs

###  We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.

**Flag:**  `pwn.college{sRVYwIIYssovrh9s0jU0scFyhPM.0lM3kjNxwCN2kjNzEzW}`

We first go to /challenge/files and run /challenge/run with the argument- * p *

```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{sRVYwIIYssovrh9s0jU0scFyhPM.0lM3kjNxwCN2kjNzEzW}


```

## What I learnt

We can use multiple globs in an argument.

# Mixing globs

### Write a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning"!

**Flag:**  `pwn.college{MYaAYqvSoxNtvNSAQx4MzY_L6yN.QX1IDO0wCN2kjNzEzW}`

[cep] matches the first letters of three words and * includes the rest of the word. We get the flag by running /challenge/run with [cep]*


```

#!/bin/bash

hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{MYaAYqvSoxNtvNSAQx4MzY_L6yN.QX1IDO0wCN2kjNzEzW}


```

## What I learnt

Revision of what I learnt till now.

# Exclusionary globbing

### go forth to /challenge/files and run /challenge/run with all files that don't start with p, w, or n.
**Flag:**  `pwn.college{QsX6-dx5L5Bk5IFovT_QKcFSlOA.QX2IDO0wCN2kjNzEzW}`
We cd the given directory and use ^ to exclude the words starting with p,w,n.

```

#!/bin/bash

hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{QsX6-dx5L5Bk5IFovT_QKcFSlOA.QX2IDO0wCN2kjNzEzW}

```

## What I learnt

^-this is used to exclude mentioned characters

# Exclusionary globbing

### This challenge has copied the flag into /challenge/pwncollege, and you can freely cat that file. But you can't type the filename: we used some serious trickery to make sure that you must tab-complete it.

**Flag:**  `pwn.college{4n3D6weSy6FGVfBJZy-ZGHlhn65.0FN0EzNxwCN2kjNzEzW}`

We get the flag by catting /challenge/pwncollege but we tab 'college'

```

#!/bin/bash

hacker@globbing~tab-completion:/challenge$ cat /challenge/pwncollege​ 
pwn.college{4n3D6weSy6FGVfBJZy-ZGHlhn65.0FN0EzNxwCN2kjNzEzW}

```

## What I learnt

Tab completion is a safer alternative when it comes to specifying a specific target.

# Multiple options for tab completion

### This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. Tab-complete from /challenge/files/p or so, and make your way to the flag

**Flag:**  `pwn.college{0SrNDf4qww0osIwuvOzZsTozFpr.0lN0EzNxwCN2kjNzEzW}`

We get the flag by running cat /challenge/files/pwncollege-flag (by tab completion)

```

#!/bin/bash

hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter  
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-f
cat: /challenge/files/pwncollege-f: No such file or directory
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-fl
pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-flag
pwn.college{0SrNDf4qww0osIwuvOzZsTozFpr.0lN0EzNxwCN2kjNzEzW}

```

## What I learnt

Tab completion is a safer alternative when it comes to specifying a specific target.

# Tab completion on commands

###  This level has a command that starts with pwncollege, and it'll give you the flag. Type pwncollege and hit the tab key to auto-complete it

**Flag:**  `pwn.college{coKCp8DgXC7GKCohZ3qtJFIsvz0.0VN0EzNxwCN2kjNzEzW}`

We type pwncollege and hit the tab key. It autocompletes the command and gives us the flag.

```

#!/bin/bash

hacker@globbing~tab-completion-on-commands:~$ pwncollege-5372 
Correct! Here is your flag:
pwn.college{coKCp8DgXC7GKCohZ3qtJFIsvz0.0VN0EzNxwCN2kjNzEzW}

```

## What I learnt

We can have tab completion on commands as well.
