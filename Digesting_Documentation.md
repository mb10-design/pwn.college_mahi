# Learning from documentation

### Invoking a program with an argument
**Flag:**  `pwn.college{Ypatkmx7Fp-ofEt5I8WTyH1OGbJ.QX0ITO0wCN2kjNzEzW}`

By running the program /challenge/challenge with the argument --give flag

```

#!/bin/bash

hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{Ypatkmx7Fp-ofEt5I8WTyH1OGbJ.QX0ITO0wCN2kjNzEzW}

```

## What I learnt

Reading Documentation


# Learning complex usage 

### We print arbitary files using the --printfile argument.
**Flag:**  `pwn.college{EGJHresytIbOr4pzn60A4Z0BdD_.QX1ITO0wCN2kjNzEzW}`

The challenge program runs when we use the standard path with it which was /flag

```

#!/bin/bash

hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{EGJHresytIbOr4pzn60A4Z0BdD_.QX1ITO0wCN2kjNzEzW}

```

## What I learnt


More basics about documentation. 


# Reading Manuals

### Read the manual challenge and get the correct argumet.
**Flag:** `pwn.college{YDi-veOvyVGAyqay_Cx-xTHBtPG.QX0EDO0wCN2kjNzEzW}`

In the manual it was written that we get the flag if the specific argument is ivevyy with required value 002..

```

#!/bin/bash

hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --ivevyy 002
Correct usage! Your flag: pwn.college{YDi-veOvyVGAyqay_Cx-xTHBtPG.QX0EDO0wCN2kjNzEzW}

```

## What I learnt 

How to read a manual.


# Searching Manuals

### Look for the flag in the manual.
**Flag:**  `pwn.college{4cQO5GsCGHEbjJ4wpp2Ibr9nkiZ.QX1EDO0wCN2kjNzEzW}`
`

We get the flag by searching the word flag in the manual-/flag.

```

#!/bin/bash

hacker@man~searching-manuals:~$ man challenge

gzip: stdout: Broken pipe
hacker@man~searching-manuals:~$ /challenge/challenge --ozczrzt
Initializing...
Correct usage! Your flag: pwn.college{4cQO5GsCGHEbjJ4wpp2Ibr9nkiZ.QX1EDO0wCN2kjNzEzW}

```

## What I learnt

How to look for words in the manual.

# Searching for Manuals

### Search for manuals and find the one which would lead you to tthe flag.
**Flag:**  `pwn.college{sQDtyNyW8oPlWoSy6P_6cCBGtoa.QX2EDO0wCN2kjNzEzW}`

We first search for manuals having the word flag in it. Then by opening the correct manual we get the correct program for generating the flag.

```

#!/bin/bash

hacker@man~searching-for-manuals:~$ man styyoloyct
hacker@man~searching-for-manuals:~$ /challenge/challenge --styyol 866
Correct usage! Your flag: pwn.college{sQDtyNyW8oPlWoSy6P_6cCBGtoa.QX2EDO0wCN2kjNzEzW}


```

## What I learnt

While searching for the word flag in manuals I used the command man -k flag.

# Helpful Programs 

### Read the program documentation with --help
**Flag:**  ` pwn.college{QcPZXfrICyvo586YfL5jwC1tLJZ.QX3IDO0wCN2kjNzEzW}`
`

586 was the correct number for -g to give the flag 

```

#!/bin/bash

 hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -g GIVE_THE_FLAG
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 586
hacker@man~helpful-programs:~$ /challenge/challenge -g 586
Correct usage! Your flag: pwn.college{QcPZXfrICyvo586YfL5jwC1tLJZ.QX3IDO0wCN2kjNzEzW}


```

## What I learnt

If programs dont have a man page, we usually use the --help argument to invoke it.

# Help for Builtins

### Invoke a builtin. 
**Flag:**  `pwn.college{AImllxgliq_Yne3UYTl4eH8MH-i.QX0ETO0wCN2kjNzEzW}`

After we invoked the builtin, we found the correct argument to be --secret to be used with a specific value

```

#!/bin/bash

hacker@man~help-for-builtins:~$ challenge --secret AImllxgl
Correct! Here is your flag!
pwn.college{AImllxgliq_Yne3UYTl4eH8MH-i.QX0ETO0wCN2kjNzEzW}

```

## What I learnt

Some commands, rather than being programs with man pages and help options, are built into the shell itself. These are called builtins.


# References 

I took the help of chatgpt
