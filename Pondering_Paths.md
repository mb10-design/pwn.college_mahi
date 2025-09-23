# The Root

### Basics about filesystem
**Flag:**  `pwn.college{As5GrbszdGqkwDNiQvHevVPhmVr.QX4cTO0wCN2kjNzEzW}`

/- This gives a start to the file system. Under this we have many directories. Here we get the flag by invoking the pwn program using its absolute path. /pwn is an absolute path.

```

#!/bin/bash

/pwn
BOOM!!!
Here is your flag:
pwn.college{As5GrbszdGqkwDNiQvHevVPhmVr.QX4cTO0wCN2kjNzEzW}

```

## What I learnt

About file directories and what an absolute path is.


# Program and Absolute Path

### We learnt about how programs are created under a directory
**Flag:**  `pwn.college{4sBo3eWi1_fNf-xzLFlDPcZbBll.QX1QTN0wCN2kjNzEzW}`

Path to challenge directory is /challenge. Any program under challenge directory is /challenge/program. Here the name of the prpgram is run. We get the program y invoking the program under the challenge directory.
```

#!/bin/bash

/challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{4sBo3eWi1_fNf-xzLFlDPcZbBll.QX1QTN0wCN2kjNzEzW}

```

## What I learnt

Got to know that there could be a program under a specific directory.



# Position thyself

### Function of cd 
**Flag:** `pwn.college{g6jAD4CKEqWTHIX0Y0tT3_wKVw3.QX2QTN0wCN2kjNzEzW}`

cd-change directory-it navigates around directories. Here the directory was /system/kernel. Then we had to invoke the path /challenge/run in the the directory.

```

#!/bin/bash

cd /sys/kernel
hacker@paths~position-thy-self:/sys/kernel$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{g6jAD4CKEqWTHIX0Y0tT3_wKVw3.QX2QTN0wCN2kjNzEzW}

```

## What I learnt 

About the function of cd-how it navigates a directory.


# Position Elsewhere

### Execute the /challenge/run with a specific path
**Flag:**  `pwn.college{AuGoMzwyJkYZqd4qFHLoHypyjzf.QX3QTN0wCN2kjNzEzW}`

/var/log was the path with cd. Then I entered /challenge/run program which gave me the flag.

```

#!/bin/bash

cd /var/log
hacker@paths~position-elsewhere:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{AuGoMzwyJkYZqd4qFHLoHypyjzf.QX3QTN0wCN2kjNzEzW}

```

## What I learnt

We can navigate around directories using cd command.

# Position yet elsewhere 

### Execute the /challenge/run with a specific path
**Flag:**  `pwn.college{YJYRxs6lRggLYxrnZ3o1bmY6ag4.QX4QTN0wCN2kjNzEzW}`

/proc/138 was the path with cd. Then I entered /challenge/run program which gave me the flag.

```

#!/bin/bash

cd /proc/138
hacker@paths~position-yet-elsewhere:/proc/138$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{YJYRxs6lRggLYxrnZ3o1bmY6ag4.QX4QTN0wCN2kjNzEzW}


```

## What I learnt

We can navigate around directories using cd command.

# Implicit relative paths,from /

### Run /challenge/run using a relative path
**Flag:**  `pwn.college{EOSnXzoKbmoirPloX1PdU9Xt9ZD.QX5QTN0wCN2kjNzEzW}`

The challenge requires us to invoke /challenge/run via a relative path. 
cd/-sets working directory to root.

```

#!/bin/bash

cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{EOSnXzoKbmoirPloX1PdU9Xt9ZD.QX5QTN0wCN2kjNzEzW}


```

## What I learnt

About relative paths-any path which does not start with /

# Implicit relative paths,from /

### Generate the flag by using . in your relative path.
**Flag:**  `pwn.college{Urs_Tn5G0HU2iJoQQm4vHv0RP3M.QXwUTN0wCN2kjNzEzW}`

First generate cd /. Flag is generated when we write the relative path starting in a different way starting from '.' .

```

#!/bin/bash

cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{Urs_Tn5G0HU2iJoQQm4vHv0RP3M.QXwUTN0wCN2kjNzEzW}

```

## What I learnt

About how we can write absolute and relative paths in different ways.

# Implicit relative path

### Generate the flag by using relative path from a given directory.
**Flag:**  `pwn.college{463_hKxe4v3KpxQtDLmjtZhp8VW.QXxUTN0wCN2kjNzEzW}`

Here the directory was /challenge. Then we used the relative path ./run to generate the flag.

```

#!/bin/bash

 cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{463_hKxe4v3KpxQtDLmjtZhp8VW.QXxUTN0wCN2kjNzEzW}

```

## What I learnt

About how we explicitly execute a program in the current directory.

# Home Sweet Home

### To copy the flag using /challenge/run as we specify an argument in the commandline.
**Flag:**  `pwn.college{YXiqVto1qd0lJOQrRB8onK0A_ID.QXzMDO0wCN2kjNzEzW}`

/challenge/run ~/f tells the program to copy the flag in the home directory.

```

#!/bin/bash

  /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{YXiqVto1qd0lJOQrRB8onK0A_ID.QXzMDO0wCN2kjNzEzW}

```

## What I learnt

~ is shorthand for home directory. cd uses home directory as default.

## References 

I took the help of chatgpt.



