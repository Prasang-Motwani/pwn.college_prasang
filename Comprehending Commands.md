# Challenge 1 cat: not the pet, but the command!

In this challenge, pwn college will copy the flag to the flag file in your home directory (where your shell starts). Go read it with cat!

## Solution:

-When the terminal opened I accessed read the file named "flag" using the cat command and captured the flag<br>

### Commands used:

`
hacker@commands~cat-not-the-pet-but-the-command:~$ cat ~/flag
`

## Flag:

`
pwn.college{k9jaD8ym6xptIRaUuDjVGKR3pje.QXxcTN0wyNzAzNzEzW}
`

### Notes:

I learnt that:<br>

One of the most critical Linux commands is cat. cat is most often used for reading out files, like so:

`
hacker@dojo:~$ cat /challenge/DESCRIPTION.md
`

One of the most critical Linux commands is `cat`.
`cat` is most often used for reading out files, like so:
cat will concatenate (hence the name) multiple files if provided multiple arguments. For example:

```
hacker@dojo:~$ cat myfile
This is my file!
hacker@dojo:~$ cat yourfile
This is your file!
hacker@dojo:~$ cat myfile yourfile
This is my file!
This is your file!
hacker@dojo:~$ cat myfile yourfile myfile
This is my file!
This is your file!
This is my file!
```

Finally, if you give no arguments at all, cat will read from the terminal input and output it.
<br>
-I learnt what is cat in a nutshell and how to use it



# Challenge 2 Catting absolute paths

In this directory, I will not copy it to your home directory, but I will make it readable. You can read it with cat at its absolute path: /flag.

## Solution:

-Here also I used cat to read the file flag but this time we didn't had to distract it from the home directory but from `/flag`

### Commands used:

`
hacker@commands~catting-absolute-paths:~$ cat /flag
`

## Flag:

`
pwn.college{M5vjmiWC1z56TE3ZguumXlc5to5.QX5ETO0wyNzAzNzEzW}
`

### Notes:

-Here in this challenge, I learnt that you can specify cat's arguments as absolute paths not compulsarily from the home directory<br>
-Apart from this this challenge was pretty much the same as challenge 1



# Challenge 3 More Catting Practice

You can specify all sorts of paths as arguments to commands, and we'll practice some more with cat. In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with cd, so no cat flag for you. You must retrieve the flag by absolute path, wherever it is.

## Solution:

- When I opened the terminal, it was mentioned:<br>
-`cd` is not allowed in this challenge, we have to use an absolute path as an argument in `cat`<br>
-The required absolute path was given so just used that as an argument and captured the flag<br>

### Commands run:

`
hacker@commands~more-catting-practice:~$ cat /usr/lib/p7zip/flag
`

## Flag:

`
pwn.college{w_Nmtit20w0UVmXa4aRuRiLKTx2.QXwITO0wyNzAzNzEzW}
`

## Notes:

-You can specify all sorts of paths as arguments to commands<br>
-Absolute paths can be arguments in a cat command



# Challenge 4 Grepping for a Needle in a Haystack

In this challenge, pwn college has  put a hundred thousand lines of text into the /challenge/data.txt file. grep it for the flag!

HINT: The flag always starts with the text pwn.college.

## Solution:

-Use `grep` command to search for flag in the given text file<br>
-Every flag starts from "pwn.college" so use that and search for flag 
-Capture the flag

### Commands used:

```sh
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep SEARCH_pwn.college{ /challenge/data.txt
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep "pwn.college" /challenge/data.txt
pwn.college{wpnwAL8DAKmEXucA49esAASb5kU.QX3EDO0wyNzAzNzEzW}
```

## Flag:

```
pwn.college{wpnwAL8DAKmEXucA49esAASb5kU.QX3EDO0wyNzAzNzEzW}
```
### References:

[link 1](https://www.geeksforgeeks.org/linux-unix/grep-command-in-unixlinux/)
## Notes:

-I learnt what the grep command does i.e searches for data in a very large file like as the name of the challenge suggests a needle in a haystack<br>
-Sometimes, the files that you might cat out are too big. Luckily, we have the grep command to search for the contents we need! We'll learn it in this challenge.

There are many ways to grep, and we'll learn one way here:

`
hacker@dojo:~$ grep SEARCH_STRING /path/to/file
`
<br>
Invoked like this, grep will search the file for lines of text containing SEARCH_STRING and print them to the console.

<br>
-I was a bit confused in the syntax of `grep` command which is evident from the commands used section
<br>
-I was using "SEARCH_pwn.college" and not "pwn.college" as I thought to follow the search and string part word to word as Syntax in linux is very particular so I had to use reference to confirm the syntax of `grep` command in linux



# Challenge 5 Comparing Files

There are two files in /challenge:

/challenge/decoys_only.txt contains 100 fake flags
/challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag
Use diff to find what's different between these files and get your flag

## Solution:

-In this challenge when the terminal opened up I used the `diff` command to separate between the 2 files as it was told that one file had 100 fake flags and the other one had the same 100 fake flags and 1 real flag
<br>
-So I used `diff` command to capture the flag

### Commands used:

`
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
`

## Flag:

`
pwn.college{oSldvOk8a2Se1iNUEvdOHwL48LE.01MwMDOxwyNzAzNzEzW}
`

### Notes:

-In this challenge I understood the working of the `diff` command
<br>

When looking for changes between similar files, eyeballing them might not be the most efficient approach! This is where the diff command becomes invaluable.

diff compares two files line by line and shows you exactly what's different between them. For example:

```
hacker@dojo:~$ cat file1
hello
world
hacker@dojo:~$ cat file2
hello
universe
hacker@dojo:~$ diff file1 file2
2c2
< world
---
> universe
```

The output tells us that line 2 changed (2c2), with world in the first file (<) being replaced by universe in the second file (>).

Sometimes, when new lines are added, you'll see something like:

```
hacker@dojo:~$ cat old
pwn
hacker@dojo:~$ cat new
pwn
college
hacker@dojo:~$ diff old new
1a2
> college
```
This tells us that after line 1 in the first file, the second file has an additional line (1a2 means "after line 1 of file1, add line 2 of file2").



# Challenge 6 listing files

In this challenge, pwn college has named /challenge/run with some random name! List the files in /challenge to find it.

# Solution:

-First when the terminal opened up I used `ls` to see the updated name of `run` using ls /challenge 
<br>
-Then I just typed `ls` to see the contents in the directory and found a file named "a" with a flag but it was a fake one
<br>
-I tried to read the the new file given to us by ls /challenge by `cat` but it was showing no directory or file by this name
<br>
-Then I used `cd` to change the directory to ls and used the same `ls` command to no fruitition
<br>
-Then I catted the file and I thought I will get the flag by `cat /flag` now but was again fooled as it showed permission denied<br>
-Then instead to reading the file I tried to execute it and I finally captured the flag

### Commands used:

```sh
hacker@commands~listing-files:~$ ls /challenge
21727-renamed-run-5682  DESCRIPTION.md
hacker@commands~listing-files:~$ ls
a
hacker@commands~listing-files:~$ cat a
pwn.college{sX_fRV1qq9nehY5HL7PbgJ60XyR.QXzMDO0wyNzAzNzEzW}
hacker@commands~listing-files:~$ cat DESCRIPTION.md
cat: DESCRIPTION.md: No such file or directory
cat: run-5682: No such file or directory
hacker@commands~listing-files:~$ cat 21727-renamed-run-5682
cat: 21727-renamed-run-5682: No such file or directory
hacker@commands~listing-files:~$ cd /challenge
hacker@commands~listing-files:/challenge$ ls
21727-renamed-run-5682  DESCRIPTION.md
hacker@commands~listing-files:/challenge$ cat 21727-renamed-run-5682
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:/challenge$ cat /flag
cat: /flag: Permission denied
hacker@commands~listing-files:/challenge$ /21727-renamed-run-5682
bash: /21727-renamed-run-5682: No such file or directory
hacker@commands~listing-files:/challenge$ cd
hacker@commands~listing-files:~$ /challenge/21727-renamed-run-5682
Yahaha, you found me! Here is your flag:
pwn.college{4kYo-5JrjE665VUHr96X2Xw3h8C.QX4IDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{4kYo-5JrjE665VUHr96X2Xw3h8C.QX4IDO0wyNzAzNzEzW}
`

### Notes:

-I learnt:

```
So far, we've told you which files to interact with. But directories can have lots of files (and other directories) inside them, and we won't always be here to tell you their names. You'll need to learn to list their contents using the ls command!

ls will list files in all the directories provided to it as arguments, and in the current directory if no arguments are provided. Observe:

hacker@dojo:~$ ls /challenge
run
hacker@dojo:~$ ls
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$ ls /home/hacker
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$
```

-I also was accustommed to a bit straightforwardness in finding the flag which this challenge was not
<br>
-I really enjoyed doing it but I think it was dragged alot and many line of codes were redundant from my side



# Challenge 7 touching files

In this level, please create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get your flag

## Solution:

-When the terminal opened I used `cd` to access the tmp directory
<br>
-Then I used `touch` command to create 2 files named "pwn" and "college"
<br>
-Then I used `ls` command to check whether the files have been created or not
<br>
-Then using the `cd` command I went back to the home directory and executed the run file by `/challenge/run` and captured the flag

## Commands used:

```sh
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ cd
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{cmPoZpDSzaNte5k72_73BBZAvlL.QXwMDO0wyNzAzNzEzW}
```

## Flag:
`
pwn.college{cmPoZpDSzaNte5k72_73BBZAvlL.QXwMDO0wyNzAzNzEzW}
`

### Notes:
-In this challenge I learnt how to create a file using `touch` command
<br>
-Sample syntax:
<br>
```
hacker@dojo:~$ cd /tmp
hacker@dojo:/tmp$ ls
hacker@dojo:/tmp$ touch pwnfile
hacker@dojo:/tmp$ ls
pwnfile
hacker@dojo:/tmp$
```



# Challenge 8 

















