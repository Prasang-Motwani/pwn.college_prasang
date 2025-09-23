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







