# Challenge 1 Matching with *

 Starting from your home directory, change your directory to /challenge, but use globbing to keep the argument you pass to cd to at most four characters! Once you're there, run /challenge/run for the flag

 ## Solution:

 -First I changed the directory using `cd` command to change the directory into challenge using `*` by typing "cd/ch*" as we couldn't write more then 4 characters for specifying path of the required directory
 <br>
 -Then I ran "/challenge/run" to capture the flag

 ### Commands used:

 ```sh
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{IQVxt20-ozYQ9qIOyLsMVaGP72g.QXxIDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{IQVxt20-ozYQ9qIOyLsMVaGP72g.QXxIDO0wyNzAzNzEzW}
`

### Notes:

-I learnt what globbing a file is 
<br>
-The first glob we'll learn is *. When it encounters a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files that match the pattern. It's easier to show you than explain:

```
hacker@dojo:~$ touch file_a
hacker@dojo:~$ touch file_b
hacker@dojo:~$ touch file_c
hacker@dojo:~$ ls
file_a	file_b	file_c
hacker@dojo:~$ echo Look: file_*
Look: file_a file_b file_c
```

Of course, though in this case, the glob resulted in multiple arguments, it can just as simply match only one. For example:

```
hacker@dojo:~$ touch file_a
hacker@dojo:~$ ls
file_a
hacker@dojo:~$ echo Look: file_*
Look: file_a
```

When zero files are matched, by default, the shell leaves the glob unchanged:

```
hacker@dojo:~$ touch file_a
hacker@dojo:~$ ls
file_a
hacker@dojo:~$ echo Look: nope_*
Look: nope_*
```

The * matches any part of the filename except for / or a leading . character. For example:

```
hacker@dojo:~$ echo ONE: /ho*/*ck*
ONE: /home/hacker
hacker@dojo:~$ echo TWO: /*/hacker
TWO: /home/hacker
hacker@dojo:~$ echo THREE: ../*
THREE: ../hacker
```



# Challenge 2 Matching with ?

Starting from your home directory, change your directory to /challenge, but use the ? character instead of c and l in the argument to cd! Once you're there, run /challenge/run for the flag

## Solution:

-I substituted the given letter with `?` ie substituted "c" and "l" with "?" 
<br>
-Then I changed into the "challenge" directory using `cd`and then ran "/challenge/run" to capture the flag

### Commands used:

```sh
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{0cdiO6kcB7MZK2omjLE699rnJhn.QXyIDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{0cdiO6kcB7MZK2omjLE699rnJhn.QXyIDO0wyNzAzNzEzW}
`

### Notes:

-In this challenge I learnt about "?"
<br>
- When it encounters a ? character in any argument, the shell will treat it as a single-character wildcard. This works like *, but only matches one character. For example:

```
hacker@dojo:~$ touch file_a
hacker@dojo:~$ touch file_b
hacker@dojo:~$ touch file_cc
hacker@dojo:~$ ls
file_a	file_b	file_cc
hacker@dojo:~$ echo Look: file_?
Look: file_a file_b
hacker@dojo:~$ echo Look: file_??
Look: file_cc
```



# Challenge 3 Matching with []

We've placed a bunch of files in /challenge/files. Change your working directory to /challenge/files and run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h!

## Solution:

-First I changed the directory into "/challenge/files" by `cd` command
<br>
-Then I used the [abhs] with "/challenge/run" and hence captured the flag

### Commands used:

```sh
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[abhs]
You got it! Here is your flag!
pwn.college{g3-7i9Zfm-9UkB7OVvuqflN9J1-.QXzIDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{g3-7i9Zfm-9UkB7OVvuqflN9J1-.QXzIDO0wyNzAzNzEzW}
`
### Notes:

-I learnt how to use []
<br>
-The square brackets are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters, specified within the brackets. For example, [pwn] will match the character p, w, or n. For example:

```
hacker@dojo:~$ touch file_a
hacker@dojo:~$ touch file_b
hacker@dojo:~$ touch file_c
hacker@dojo:~$ ls
file_a	file_b	file_c
hacker@dojo:~$ echo Look: file_[ab]
Look: file_a file_b
```



# Challenge 4 Matching paths with []

Once more, we've placed a bunch of files in /challenge/files. Starting from your home directory, run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files!

## Solution:

-Here we don't have to `cd` into the given directory we have to run the command and the argument from the home directory only
<br>
-So we used the path and then used `[]` as argument with the "/challenge/run" command and hence captured the flag

### Command used:

```sh
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[absh]
You got it! Here is your flag!
pwn.college{g8Efjse9wsOxDDEjdmyY58kZ5Fx.QX0IDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{g8Efjse9wsOxDDEjdmyY58kZ5Fx.QX0IDO0wyNzAzNzEzW}
`

### Notes:

Globbing happens on a path basis, so you can expand entire paths with your globbed arguments. For example:

```
hacker@dojo:~$ touch file_a
hacker@dojo:~$ touch file_b
hacker@dojo:~$ touch file_c
hacker@dojo:~$ ls
file_a	file_b	file_c
hacker@dojo:~$ echo Look: /home/hacker/file_[ab]
Look: /home/hacker/file_a /home/hacker/file_b
```



# Challenge 5 Multiple globs

We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.

## Solution:

-It was a pretty straightforward challenge 
<br>
-Then I changed into the "/challenge/files" using `cd` command
<br>
-Then I used multiple globbing by typing "/challenge/run *p*" and captured the flag

### Commands used:

```sh
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{oY-P-ekSSwL7BMFbOdscJ2rNS_M.0lM3kjNxwyNzAzNzEzW}
```

## Flag:

`
pwn.college{oY-P-ekSSwL7BMFbOdscJ2rNS_M.0lM3kjNxwyNzAzNzEzW}
`

### Notes:

 Bash supports the expansion of multiple globs in a single word. For example:

```
hacker@dojo:~$ cat /*fl*
pwn.college{YEAH}
hacker@dojo:~$
```

What happens above is that the shell looks for all files in / that start with anything (including nothing), then have an f and an l, and end in anything (including ag, which makes flag).



# Challenge 6 Mixing Globs

We put a few happy, but diversely-named files in /challenge/files. Go cd there and, using the globbing you've learned, write a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning"!

## Solution:

-First I entered the "/challenge/files" directory using the `cd` command
<br>
-Then I wrote a mixture of `*` and `[]` by typing "/challenge/run [cep]*" so that the shell would all files starting from "c", "e" and "p" and then put * so that it won't matter what comes after c,e and p and like this I captured the flag

### Commands used:

```sh
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{cuCVH5vK-EVVSBywDvwRUUrKb2C.QX1IDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{cuCVH5vK-EVVSBywDvwRUUrKb2C.QX1IDO0wyNzAzNzEzW}
`

### Notes

-In this challenge I learnt how to approach problems that have mixyture of globbing that I learnt



# Challenge 7 Exclusionary Globbing

Go forth to /challenge/files and run /challenge/run with all files that don't start with p, w, or n!

## Solution

-First I entered the "/challenge/files" directory using the `cd` command
<br>
-Then I used a mixture of "[]", "!" and "*" by typing "/challenge/run [!pwn]*" so that the shell would give all files that do not start with "p", "w" or "n" and hence I captured the flag([!] means not starting from it and * means anything that comes after it will qualify as the output)



### Commands used:

```sh
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{YIzGE1Qqx5R0LiL2u44dAM1-tvv.QX2IDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{YIzGE1Qqx5R0LiL2u44dAM1-tvv.QX2IDO0wyNzAzNzEzW}
`

### Notes

-Sometimes, you want to filter out files in a glob! Luckily, [] helps you do just this. If the first character in the brackets is a ! or (in newer versions of bash) a ^, the glob inverts, and that bracket instance matches characters that aren't listed. For example:

```
hacker@dojo:~$ touch file_a
hacker@dojo:~$ touch file_b
hacker@dojo:~$ touch file_c
hacker@dojo:~$ ls
file_a	file_b	file_c
hacker@dojo:~$ echo Look: file_[!ab]
Look: file_c
hacker@dojo:~$ echo Look: file_[^ab]
Look: file_c
hacker@dojo:~$ echo Look: file_[ab]
Look: file_a file_b
```
<br>
-The ! character has a different special meaning in bash when it's not the first character of a [] glob, so keep that in mind if things stop making sense! ^ does not have this problem, but is also not compatible with older shells.
<br>
-The "!" is like when we take a compliment in sets in mathematics



# Challenge 8 Tab completion

This challenge has copied the flag into /challenge/pwncollege, and you can freely cat that file. But you can't type the filename: we used some serious trickery to make sure that you must tab-complete it. Try it out!

## Solution:

-This challenge was pretty straightforward
<br>
-I executed the "hacker@globbing~tab-completion:~$ cat /challenge/pwncollege" command but instead of typing the whole command I pressed the tab key and the terminal auto-completed the command and hence I captured the flag

### Commands used:

```sh
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​
pwn.college{4WP9E5Nsjs_YtPMiOBlhgBLbKPD.0FN0EzNxwyNzAzNzEzW}
```

## Flag:

`
pwn.college{4WP9E5Nsjs_YtPMiOBlhgBLbKPD.0FN0EzNxwyNzAzNzEzW}
`

### Notes:

-As tempting as it might be, using * to shorten what must be typed on the commandline can lead to mistakes. Your glob might expand to unintended files, and you might not spot it until the rm command is already running! No one is safe from this style of error.

A safer alternative when you are trying to specify a specific target is tab completion. If you hit tab in the shell, it'll try to figure out what you're going to type and automatically complete it. Auto-completion is super useful, and this challenge will explore its use in specifying files.



# Challenge 9 Multiple options for tab completion

This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. Tab-complete from /challenge/files/p or so, and make your way to the flag!

## Solution





# Challenge 10 Tab completion on commands

This level has a command that starts with pwncollege, and it'll give you the flag. Type pwncollege and hit the tab key to auto-complete it!

## Solution

-This level was pretty straightforward all I had to do was press tab after writing "pwncollege" and the shell auto completed the command to "pwncollege-31517" and hence I captured the flag

### Commands used:

```sh
hacker@globbing~tab-completion-on-commands:~$ pwncollege-31517
Correct! Here is your flag:
pwn.college{Y8qb3B8P-hWD6sTeBhX0ihVbjZ-.0VN0EzNxwyNzAzNzEzW}
```

## Flag:

`
pwn.college{Y8qb3B8P-hWD6sTeBhX0ihVbjZ-.0VN0EzNxwyNzAzNzEzW}
`

### Notes:

-In this challenge I learnt that the tab key on auto-completion can be used not only files but for commands too
