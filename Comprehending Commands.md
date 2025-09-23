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
-I was a bit confused in the syntax of grep command which is evident from the commands used section
<br>
-I was using "SEARCH_pwn.college" and not "pwn.college" as I thought to follow the search and string part word to word as Syntax in linux is very particular so I had to use reference to confirm the syntax of grep command in linux



# Comparing Files

There are two files in /challenge:

/challenge/decoys_only.txt contains 100 fake flags
/challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag
Use diff to find what's different between these files and get your flag

## Solution








