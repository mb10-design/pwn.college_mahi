# Translating characters

### n this level, /challenge/run will print the flag but will swap the casing of all characters (e.g., A will become a and vice-versa)

**Flag:**  `pwn.college{0_C5-K7m7xj9jbrHu2XLuWDuHOw.01MxEzNxwCN2kjNzEzW}`

Here tr 'a-zA-Z' 'A-Za-z' tells tr to:

replace every lowercase letter (a-z) with uppercase (A-Z),

replace every uppercase letter (A-Z) with lowercase (a-z).

We get the flag by running the following command-

```

#!/bin/bash

hacker@data~translating-characters:~$ /challenge/run | tr 'a-zA-Z' 'A-Za-z'
yOUR CASE-SWAPPED FLAG:
pwn.college{0_C5-K7m7xj9jbrHu2XLuWDuHOw.01MxEzNxwCN2kjNzEzW}

```

## What I learnt

tr translates the character provided in its first argument to the character provided in its second argument.


# Deleting characters 

### The challenge has interspersed some decoy characters (specifically: ^ and %) among the flag characters. Use tr -d to remove them.

**Flag:**  `pwncollege{MM6wDLHu9p6iYjWWGzxTuU8FsR0FNxEzNxwCN2kjNzEzW}`

I first ran /challenge/run to know what special characters are there on the flag. Then I removed them and got the flag

```

#!/bin/bash

hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{MM6wDLHu9p6iYjWWGzxTuU8_FsR.0FNxEzNxwCN2kjNzEzW}

```

## What I learnt

tr can also translate characters to nothing (i.e., delete them). This is done via a -d flag and an argument of what characters to delete.



# Deleting newlines

### In this challenge, we'll inject a bunch of newlines into the flag. Delete them with tr's -d flag and the escaped newline specification

**Flag:** `pwn.college{UN41x2nBZgXeTfx4WdgWVWBVm1x.0VNxEzNxwCN2kjNzEzW}`

We deleted all the new lines in the flag.

```

#!/bin/bash

hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{UN41x2nBZgXeTfx4WdgWVWBVm1x.0VNxEzNxwCN2kjNzEzW}

```

## What I learnt 

The concept of "\n"-This indicates a new line


# Extracting the first lines with head 

### This challenge's /challenge/pwn outputs a bunch of data, and you'll need to pipe it through head to grab just the first 7 lines and then pipe them onwards to /challenge/college, which will give you the flag if you do this right!

**Flag:**  `pwn.college{smkJGup4t3rYe4PjbbtxMBMLoPi.0lNxEzNxwCN2kjNzEzW}`

We got the flag by piping the output of /challenge/pwn to /challenge/college. (we use head -n 7 to print the first 7 lines of /challenge/pwn)

```

#!/bin/bash

hacker@data~extracting-the-first-lines-with-head:~$  /challenge/pwn | head -n 7 |  /challenge/college
Congratulations, you piped the right codes!
pwn.college{smkJGup4t3rYe4PjbbtxMBMLoPi.0lNxEzNxwCN2kjNzEzW}

```

## What I learnt

The head command is used to display the first few lines of its input:

# Extracting specific sections of the text 

### Use cut to extract the flag characters, then pipe them to tr -d "\n

**Flag:**  `pwn.college{4cwR-qWCu_SWahfn6f8Xu0YZkDc.01NxEzNxwCN2kjNzEzW}`

We extract the 2nd column of the output of /challenge/run and delete the  newline.

```

#!/bin/bash

 hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d" " -f2 | tr -d "\n"
pwn.college{4cwR-qWCu_SWahfn6f8Xu0YZkDc.01NxEzNxwCN2kjNzEzW}

```

## What I learnt

cut is used to grab specific columns of the data.The -d argument specifies the column delimiter (how columns are separated). The -f argument specifies the field number (which column to extract).

# Sorting Data 

### In this challenge, there's a file at /challenge/flags.txt containing 100 fake flags, with the real flag mixed among them. When sorted alphabetically, the real flag will be at the end 

**Flag:**  `pwn.college{027bUS3V-J--bchpdQMjsfuErWE.0FM0MDOxwCN2kjNzEzW}`


We sort the file alphabetically by using the sort command . The real flag is at the end.

```

#!/bin/bash

hacker@data~sorting-data:~$ sort /challenge/flags.txt


```

## What I learnt

By default, sort orders lines alphabetically. Arguments can change this:

-r: reverse order (Z to A)

-n: numeric sort (for numbers)

-u: unique lines only (remove duplicates)

-R: random order


