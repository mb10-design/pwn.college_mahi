# cat: not the pet, but the command

### copying the flag into the flag file in the home directory
**Flag:**  `pwn.college{ozbF89r6Ctr5PQ8QzMKjrEvaZca.QXxcTN0wCN2kjNzEzW}`

By running cat flag command-we got the flag.

```

#!/bin/bash

cat flag
pwn.college{ozbF89r6Ctr5PQ8QzMKjrEvaZca.QXxcTN0wCN2kjNzEzW}

```

## What I learnt

cat-concatenates files if provided multiple arguments.


# cattling absolute paths

### Reading flag with its absolute path
**Flag:**  `pwn.college{QuVdRjhoENyVWopCCTAdiufRK8E.QX5ETO0wCN2kjNzEzW}`

We got the flag by using /flag command with cat.

```

#!/bin/bash

cat /flag
pwn.college{QuVdRjhoENyVWopCCTAdiufRK8E.QX5ETO0wCN2kjNzEzW}

```

## What I learnt

Instead of copying flag in the home directory, this directory made it readable-/flag.



# More catting pratice

### The flag is in a different directory this time
**Flag:** `pwn.college{EhJIV1H3agI9AHmXeXgLmthls_f.QXwITO0wCN2kjNzEzW}`

We get the flag by using cat with a different directory.

```

#!/bin/bash

cat /usr/share/bash-completion/flag
pwn.college{EhJIV1H3agI9AHmXeXgLmthls_f.QXwITO0wCN2kjNzEzW}

```

## What I learnt 

How to use different absolute paths with cat


# grepping for a needle in haystack

### To search particular lines of text in a particular file.
**Flag:**  `pwn.college{8auasoqAe-b_pyNxH_bmrhkgWwc.QX3EDO0wCN2kjNzEzWp}`

We used grep with pwn.college to find the flag in the given file

```

#!/bin/bash

grep pwn.college /challenge/data.txt
pwn.college{8auasoqAe-b_pyNxH_bmrhkgWwc.QX3EDO0wCN2kjNzEzWp}

```

## What I learnt

When files are too big we use grep instead of cat to search for text.

# Comparing files 

### Use diff to find out what's different between the two given files.
**Flag:**  `pwn.college{0t0cGxS7OYiwecMxwikYY7xj68j.01MwMDOxwCN2kjNzEzW}`

We first set the given directory /challenge. Then we go to the specific files given by using cat.   Then by using diff-we compare the two files and get the flag.
```

#!/bin/bash

 diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
17a18
> pwn.college{0t0cGxS7OYiwecMxwikYY7xj68j.01MwMDOxwCN2kjNzEzW}


```

## What I learnt

diff compares two files and shows us what is different about them.

# listing files

### The challenge has renamed the file /challenge. Find that name and generate the flag.
**Flag:**  `pwn.college{EUtOZxjJPv0dAxDh8cM-jJW29Kb.QX4IDO0wCN2kjNzEzW}`
`

We first list the contents of /challenge. Then find the name and run /challenge with cd command with the relative path listed in the /challenge earlier.

```

#!/bin/bash

 ls /challenge
21679-renamed-run-26149  DESCRIPTION.md
hacker@commands~listing-files:/challenge$ cd /challenge
hacker@commands~listing-files:/challenge$ ./21678-renamed-run-26149
bash: ./21678-renamed-run-26149: No such file or directory
hacker@commands~listing-files:/challenge$ ./21679-renamed-run-26149
Yahaha, you found me! Here is your flag:
pwn.college{EUtOZxjJPv0dAxDh8cM-jJW29Kb.QX4IDO0wCN2kjNzEzW}


```

## What I learnt

ls command-lists the names of the files in all directories.

# touching files 

### Create new files in a directory and run /challenge/run
**Flag:**  `pwn.college{cmTgTVRZFMHluIon12tB_0HERzn.QXwMDO0wCN2kjNzEzW}`

After creating the files, we simply ran /command/files to get the flag.

```

#!/bin/bash

cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
cd /challenge
hacker@commands~touching-files:/challenge$ ./run
Success! Here is your flag:
pwn.college{cmTgTVRZFMHluIon12tB_0HERzn.QXwMDO0wCN2kjNzEzW}

```

## What I learnt

Using the touch argument to create new files.

# Removing files 

### The challenge asked us to delete a particular file. Then check by running /challenge/check.
**Flag:**  `pwn.college{491qfOuuAA5zal88kxLQOWzySwv.QX2kDM1wCN2kjNzEzW}`

We got the flag by running /challenge/check after deleting the given file.

```

#!/bin/bash

hacker@commands~removing-files:~$ rm delete_me 
hacker@commands~removing-files:~$ cd /challenge
hacker@commands~removing-files:/challenge$ ./check
Excellent removal. Here is your reward:
pwn.college{491qfOuuAA5zal88kxLQOWzySwv.QX2kDM1wCN2kjNzEzW}

```

## What I learnt

rm-delets files

# moving files 

###  Move one file to another 
**Flag:**  `pwn.college{UEoSw5HXm9zakm_RfPHzVvm4bxm.0VOxEzNxwCN2kjNzEzW}`

Generate flag (after moving one file to another) by using the /challenge/check command.

```

#!/bin/bash

mv /flag /tmp/hack-the-planet
hacker@commands~moving-files:/tmp$ cd /challenge
hacker@commands~moving-files:/challenge$ ./check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{UEoSw5HXm9zakm_RfPHzVvm4bxm.0VOxEzNxwCN2kjNzEzW}

```

## What I learnt

mv-moves one file to another 

# Hidden files

## To find the hidden file in /. 

**Flag:**  `pwn.college{ctlPGRhf0f--gET8vBSzxWczvoW.QXwUDO0wCN2kjNzEzW}`

We generate the file by using cat with the flag file found.

```

#!/bin/bash

hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-269352026431689  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-269352026431689
pwn.college{ctlPGRhf0f--gET8vBSzxWczvoW.QXwUDO0wCN2kjNzEzW}
```

## What I learnt

files starting with a . are hidden. We need to use ls -a to display them.


# Epic File System Quest

## Find the flag which is hidden in a specific file 

**Flag:**  `pwn.college{wD8ZlM4oiVGPoOGMPSKP4g5QL5V.QX5IDO0wCN2kjNzEzW}`

We generate the file following the clues generated in the subsequent files.



## What I learnt

It was a good practice of all the concepts I learnt till now.

# Making directories

## Create a directory and and create a file in it

**Flag:**  `pwn.college{o_RV-Pf_29d3kC1f78rlEnXW_sI.QXxMDO0wCN2kjNzEzW}`

We generate the file by creating the given directory by using mkdir. Then we make a file in it named college. Then we check using /challenge/check.

```
#!/bin/bash
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ cd /challenge
hacker@commands~making-directories:/challenge$ ./run
Success! Here is your flag:
pwn.college{o_RV-Pf_29d3kC1f78rlEnXW_sI.QXxMDO0wCN2kjNzEzW}


```

## What I learnt

mkdir-creates new directories.

# Finding Files

## find the file having flag

**Flag:**  `pwn.college{w-t5AjE6InRMHxGi5lJr8ba7DeX.QXyMDO0wCN2kjNzEzW}`

We generate the file by searching the files having the name flag in them. Then we cat a specific file and find the flag.

```
#!/bin/bash
hacker@commands~finding-files:~$ find / -name flag
/usr/lib/file/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /usr/lib/file/flag
pwn.college{w-t5AjE6InRMHxGi5lJr8ba7DeX.QXyMDO0wCN2kjNzEzW}


```

## What I learnt

find command is used to search for specific files. If we just type find then it uses current working directory.

# Linking Files 

##  Use ln -s to link copy /flag to /challenge/catflag and find the flag.

**Flag:**  `pwn.college{k18_jhTm6ywWgV-V-8bDoGo7bip.QX5ETN1wCN2kjNzEzW}`

First, we delete the file not-the-flag so that we can make a new link. Then we create a pointer(symlink). Then we follow the pointer to the real file(/challenge/catflag) to get the flag.

```
#!/bin/bash

hacker@commands~linking-files:~$ cat /challenge/catflag
#!/opt/pwn.college/bash

fold -s <<< "About to read out the /home/hacker/not-the-flag file!"
cat /home/hacker/not-the-flag
hacker@commands~linking-files:~$ rm -f ~/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{k18_jhTm6ywWgV-V-8bDoGo7bip.QX5ETN1wCN2kjNzEzW}


```

## What I learnt

How to link two files.


## References 

I took the help of chatgpt.



