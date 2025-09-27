# Redirecting output

### use the output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

**Flag:**  `pwn.college{4RR9yhzqB7Iys4W-3uLygycGkrC.QX0YTN0wCN2kjNzEzW}`

 We copy PWN to COLLEGE by using >

```
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{4RR9yhzqB7Iys4W-3uLygycGkrC.QX0YTN0wCN2kjNzEzW}

```

## What I learnt

How to copy what we have to echo in a particular file.

# Redirecting more output

### In this level, /challenge/run will once more give you a flag, but only if you redirect its output to the file myflag. Your flag will, of course, end up in the myflag file!

**Flag:**  `pwn.college{0dZaPF_UGLnnF36jcv5Rcq0CPds.QX1YTN0wCN2kjNzEzW}`

Copied the contents of /challenge/run to myflag file and then-cat myflag.

```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.

hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{0dZaPF_UGLnnF36jcv5Rcq0CPds.QX1YTN0wCN2kjNzEzW}

```

## What I learnt

Redirecting the output of any command.


# Appending output

### To practice, run /challenge/run with an append-mode redirect of the output to the file /home/hacker/the-flag. The practice will write the first half of the flag to the file, and the second half to stdout if stdout is redirected to the file. 

**Flag:** `pwn.college{MGfXm3qrl5ak2VOIV42-C16j48L.QX3ATO0wCN2kjNzEzW}`

We first append the first half of the flag using > followed by >> for getting the second half.

```
hacker@piping~appending-output:~$ /challenge/run >> ~/the-flag
hacker@piping~appending-output:~$ cat ~/the-flag
 | 
\|/ This is the first half:
 v 
pwn.college{MGfXm3qrl5ak2VOIV42-C16j48L.QX3ATO0wCN2kjNzEzW}
                              ^
     that is the second half /|\
                              |


```

## What I learnt 

To append a particular file.


# Redirecting errors

###  you will need to redirect the output of /challenge/run, like before, to myflag, and the "errors" (in our case, the instructions) to instructions

**Flag:**  `pwn.college{U0eSkA4XcaNkRvHjaWwS2O1GOXu.QX3YTN0wCN2kjNzEzW}`
`

We redirected the output of /challenge/run to my flag and its errors to instructions. Then we catted the files instructions and myflag.

```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{U0eSkA4XcaNkRvHjaWwS2O1GOXu.QX3YTN0wCN2kjNzEzW}

```

## What I learnt

2> Redirects errors

# Redirecting input

###  practice using /challenge/run, which will require you to redirect the PWN file to it and have the PWN file contain the value COLLEGE

**Flag:**  `pwn.college{Qwj8nFguh0AzUzsN5z65LiZ2E5E.QXwcTN0wCN2kjNzEzW}`
`

We first echo college to pwn. Then redirect the input of pwn to /challenge/run

```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{Qwj8nFguh0AzUzsN5z65LiZ2E5E.QXwcTN0wCN2kjNzEzW}


```

## What I learnt

Redirecting the input of one file to another

# Grepping stored result

### Redirect the output of /challenge/run to /tmp/data.txt.This will result in a hundred thousand lines of text, with one of them being the flag, in /tmp/data.txt.grep that for the flag!

**Flag:**  `pwn.college{ITK6DfGvz1IVQgkhXj5hlavv_bR.QX4EDO0wCN2kjNzEzW}`

We get the flag by searching for pwn in the grep command


```

#!/bin/bash

hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
hacker@piping~grepping-stored-results:/tmp$ grep pwn  /tmp/data.txt
pwned
pwning
pwn
pwns
pwn.college{ITK6DfGvz1IVQgkhXj5hlavv_bR.QX4EDO0wCN2kjNzEzW}


```

## What I learnt

Revision of what I had learnt till now


# Grepping live output

### challenge/run will output a hundred thousand lines of text, including the flag. grep for the flag

**Flag:**  `pwn.college{w_u8wLMkpofGIDESyudsXvuWwNv.QX5EDO0wCN2kjNzEzW}`

We simply run /challenge/run by grepping it with pwn using | 

```

#!/bin/bash

hacker@piping~grepping-live-output:~$  /challenge/run | grep pwn
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{w_u8wLMkpofGIDESyudsXvuWwNv.QX5EDO0wCN2kjNzEzW}
pwned
pwns
pwn
pwning

```

## What I learnt

If we have to give the instructions of one command to other without using a temporary file we use |

# Grepping errors

### Like the last level, this level will overwhelm you with output, but this time on standard error. grep through it to find the flag

**Flag:**  `pwn.college{kQiaYiQpLL3gQA9-Kv212y_wAXY.QX1ATO0wCN2kjNzEzW}`

This time to get the flag we use 2>&1

```

#!/bin/bash

hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn
[PASS] Success! You have satisfied all execution requirements.
pwned
pwning
pwn.college{kQiaYiQpLL3gQA9-Kv212y_wAXY.QX1ATO0wCN2kjNzEzW}
pwns
pwn

```

## What I learnt

2>&1-This is used to merge the main output with the errors so that the pipe can catch everything.


# Filtering with grep -v

### Use grep -v to filter out all the lines containing "DECOY" and reveal the real flag!

**Flag:**  `pwn.college{kNzElu1O7GWOxgzbyHq2M2MvL_5.0FOxEzNxwCN2kjNzEzW}`

We get the flag by running /challenge/run with | grep -v DECOY

```

#!/bin/bash

hacker@piping~filtering-with-grep-v:~$  /challenge/run | grep -v DECOY
pwn.college{kNzElu1O7GWOxgzbyHq2M2MvL_5.0FOxEzNxwCN2kjNzEzW}

```

## What I learnt

Normal grep shows lines that MATCH a pattern, grep -v shows lines that do NOT match a pattern.


# Duplicating piped data with tee

###  This process' /challenge/pwn must be piped into /challenge/college, but you'll need to intercept the data to see what pwn needs from you

**Flag:**  `pwn.college{gZ7YhjotmhY0jpKWVh3VVkIDDQI.QXxITO0wCN2kjNzEzW}`

I first went to the tmp directory and got to know that there is a file name pwn_intercept. I catted the path to know the argument to be used with /challenge/pwn. Then I piped the data with tee 

```

#!/bin/bash

hacker@piping~duplicating-piped-data-with-tee:~$ cat /tmp/pwn_intercept
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "gZ7Yhjot"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret gZ7Yhjot | tee /tmp/pwn_intercept | /challenge/college
Processing...
WARNING: you are overwriting file /tmp/pwn_intercept with tee's output...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{gZ7YhjotmhY0jpKWVh3VVkIDDQI.QXxITO0wCN2kjNzEzW}

```

## What I learnt

The tee command, named after a "T-splitter" from plumbing pipes, duplicates data flowing through your pipes to any number of files provided on the command line.


# Process substitution for input

###  Use  diff with two sets of command outputs: /challenge/print_decoys, which will print a bunch of decoy flags, and /challenge/print_decoys_and_flag which will print those same decoys plus the real flag.

**Flag:**  `pwn.college{8uuD-aR37jN0c3X9o4lPjUHSy-S.0lNwMDOxwCN2kjNzEzW}`

diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)-This compared the two files and gave us the flag.

```

#!/bin/bash

hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
33a34
> pwn.college{8uuD-aR37jN0c3X9o4lPjUHSy-S.0lNwMDOxwCN2kjNzEzW}

```

## What I learnt

We can go further and hook input and output of programs to arguments of commands. This is done using Process Substitution. For reading from a command (input process substitution), use <(command). When we write <(command), bash will run the command and hook up its output to a temporary file that it will create. This isn't a real file, of course, it's what's called a named pipe.

 # Writing to multiple programs

### In this challenge, we have /challenge/hack, /challenge/the, and /challenge/planet. Run the /challenge/hack command, and duplicate its output as input to both the /challenge/the and the /challenge/planet commands.

**Flag:**  `pwn.college{UpdwDF7_9KWFj6XnyN3bSaHdcaf.QXwgDN1wCN2kjNzEzW}`

We used output process substitution to duplicate the data of the file /challenge/hack to the two given programs.

```

#!/bin/bash

hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee  >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
3603170992290430264
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{UpdwDF7_9KWFj6XnyN3bSaHdcaf.QXwgDN1wCN2kjNzEzW}

```

## What I learnt

How output process substitution works

# Writing to multiple programs

### 1-/challenge/hack: this produces data on stdout and stderr 
### 2-/challenge/the: you must redirect hack's stderr to this program 
 ### 3-/challenge/planet: you must redirect hack's stdout to this program

**Flag:**  `pwn.college{4AdwSwuIcGfBCFkCAObqc-AlEDD.QXxQDM2wCN2kjNzEzW}`


We  redirect hack's stderr by using 2>. We redirect hack's output using >(command)

```

#!/bin/bash

hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2>  >( /challenge/the) | tee  >(/challenge/planet)
This secret data must directly make it to /challenge/planet over my stdout. 
Don't try to copy-paste it; it changes too fast.
604330313561313776
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{4AdwSwuIcGfBCFkCAObqc-AlEDD.QXxQDM2wCN2kjNzEzW}

```

## What I learnt

Revision of what I learnt till now.

# Writing to multiple programs

### This challenge will be a simple introduction to FIFOs. You'll need to create a /tmp/flag_fifo file and redirect the stdout of /challenge/run to it. If you're successful, /challenge/run will write the flag into the FIFO.

**Flag:**  `pwn.college{s1_knhk131cnDY7b_GzX-sAc1he.01MzMDOxwCN2kjNzEzW}`


We create a FIFO and then redirect the output of /challenge/run to /tmp/flag_file.

```

#!/bin/bash

hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{s1_knhk131cnDY7b_GzX-sAc1he.01MzMDOxwCN2kjNzEzW}
pwn.college{s1_knhk131cnDY7b_GzX-sAc1he.01MzMDOxwCN2kjNzEzW}

```

## What I learnt

We can also create your own persistent named pipes that stick around on the filesystem! These are called FIFOs, which stands for First (byte) In, First (byte) Out.


## References 

I took the help of chatgpt.

