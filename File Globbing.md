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


