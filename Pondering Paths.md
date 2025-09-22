
# Challenge 1 The Root

Alright, so the filesystem starts at /. Under that, there are a whole mess of other directories, configuration files, programs, and, most importantly, flags. In this level, we've added a program right in /, called pwn, that will give you the flag. All you need to do for this level is to invoke this program!

You can invoke a program by providing its path on the command line. In this case, you'll be giving the exact path, starting from /, so the path would be /pwn. This style of path, one that starts with the root directory, is referred to as an "absolute path".

Start the challenge, launch a terminal, invoke the pwn program using its absolute path, and Capture that Flag! Good luck!

## Solution:

-Write /pwn to invoke the path of pwn.<br>  
-The flag will be displayed, capture the flag.<br>

### Commands run:
```sh
hacker@paths~the-root:~$ /pwn
```

## Flag:

```
pwn.college{gDXqAS_YxIyiTvhTYQ8ooGTJXiZ.QX4cTO0wyNzAzNzEzW}
```

### Notes:

In this challenge I learnt:<br>
-The linux filesystem is a tree<br>
-It has a root written as / which is a directory and every directory can further contain other directories by their path<br>
-A path from the root starts from / and goes futher into the set of directories to be opened to find the desired file<br>
-In every piece in the path different directories are differentiated by /<br>



# Challenge 2 Program and Absolute paths

Let's explore a slightly more complicated path! Except for in the previous level, challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/). The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.

This challenge again requires you to execute it by invoking its absolute path. You'll want to execute the run file that is in the challenge directory that is, in turn, in the / directory. If you invoke the challenge correctly, it will give you the flag.

## Solution:

-This was a simple challenge or should I say a one step extension of the previous challenge.<br>
-I was asked to find it's absolute path which I did by doing /challenge/run on the terminal.<br>
-By doing this the run file got executed which was in the challenge directory which in turn was in the / directry i.e. in the root directory 

### Commands run:

```sh
hacker@paths~program-and-absolute-paths:~$ /challenge/run
```

## Flag:

```
pwn.college{wFL4T4HyGJ09DL81GqlS9FYwbMY.QX1QTN0wyNzAzNzEzW}
```

### Notes:

-In this challenge I learnt what an absolute path is and how to invoke it. <br>
-I also saw how a file can be stored in a directory which in turn is also stored in the root directory.<br>
-Mistake: Not a mistake per se but a clearity in the concept. Earlier I thought that in the previous challenge /challenge is a root directory which we are accessing but via this challenge I understood that the root directory is always / only and challenge was the file to be ran just like in this program run was the file to be ran whih was in the challenge directory which in turn was in the / directory.<br>
-So the directory concept which got a bit mangled got cleared in this challenge 



# Challenge 3 Position Thyself

The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program.

## Solution:

-After the terminal comes up the user will invoke the path of ```run``` file via ```challenge``` to access the run file.<br>
An error will show up telling us to change the directory and will tell the path of the directory in which the file is present.<br>
The user will change the directory to the one the system gave using the cd command on the terminal.<br>
Now run the file and capture the flag.

### Comaands run:

```sh
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/aarch64-linux-gnu/include/gnu
hacker@paths~position-thy-self:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
```

## Flag:

```
pwn.college{0xesnk3h_h94DMAcO7eY7I3hvT4.QX2QTN0wyNzAzNzEzW}
```

### Notes:

-I learnt what a cd command does i.e changes directory.<br>
-I also learnt what the ~ was in the prompt. It shows the current path that your shell is located at.



# Challenge 4 Position Elsewhere

The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:

```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. 

## Solution:












