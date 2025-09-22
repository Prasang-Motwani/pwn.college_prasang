
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
-An error will show up telling us to change the directory and will tell the path of the directory in which the file is present which is /usr/aarch64-linux-gnu/include/gnu<br>
-The user will change the directory to the one the system gave using the ```cd``` command on the terminal.<br>
Now run the file and capture the flag.

### Commands run:

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

-Firstly on opening the terminal, I tried to run the ```run``` command in the ```challenge``` directory<br>
-Then the shell displayed error and displayed the absolute path for the ```run``` file which is /usr/include<br>
-Then use ```cd``` to change the directory to the given one<br>
-Then use /challenge/run as now the required directory is opened and capture the flag<br>

### Commands run:

```sh
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/include directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/include directory
bash: cd: too many arguments
hacker@paths~position-elsewhere:~$ cd /usr/include
hacker@paths~position-elsewhere:/usr/include$ /challenge/run
```

## Flag:

pwn.college{weWWMuhMxAgB162XwM_y1rkdQDJ.QX3QTN0wyNzAzNzEzW}

### Notes:
-This challenge was very similar to last one the concept and working was same as challenge 3<br>
-Only difference was that in this challenge separate lines in the terminals were used



# Challenge 5 Position yet elsewhere

The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program.

## Solution:

-Firstly on opening the terminal, I tried to run the ```run``` command in the ```challenge``` directory<br>
-Then the shell displayed error and displayed the absolute path for the ```run``` file which is /proc/143/fd<br>
-Then use ```cd``` to change the directory to the given one<br>
-Then use /challenge/run as now the required directory is opened and capture the flag<br>

### Commands run:

```sh
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /proc/143/fd directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /proc/143/fd
hacker@paths~position-yet-elsewhere:/proc/143/fd$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
```

## Flag:

pwn.college{YVJq_MfztpAsv7-jW24IkIMmh10.QX4QTN0wyNzAzNzEzW}

### Notes:
-This challenge was very similar to last one the concept and working was same as challenge 3 and 4<br>
-Only difference was that in this challenge separate lines in the terminals were used in challenge 3 and is exactly the same as challenge 4



# Challenge 6 Implicit Relative Paths, from /

Imagine we want to access some file located at /tmp/a/b/my_file.

If my cwd is /, then a relative path to the file is tmp/a/b/my_file.
If my cwd is /tmp, then a relative path to the file is a/b/my_file.
If my cwd is /tmp/a/b/c, then a relative path to the file is ../my_file. The .. refers to the parent directory.
Let's try it here! You'll need to run /challenge/run using a relative path while having a current working directory of /. For this level, I'll give you a hint. Your relative path starts with the letter c 😊

## Solution:

-Firstly it was quite obvious seeing the hint that the relative path starts from challenge so I tried typing challenge/run but the shell displayed ```bash: challenge/run: No such file or directory```<br>
-Then on the terminal I tried to run the file as I did in previous 3 challenges thinking that the correct path would be displayed on the shell after showing error and it told that I am not in the / directory<br>
-So first I opened the / directory using ```cd``` command and then typed challenge/run and captured the flag.

### Commands used:

```
hacker@paths~implicit-relative-paths-from-:~$ challenge/run
bash: challenge/run: No such file or directory
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
```

## Flag

pwn.college{g0_CrP3RWJNaZA4QHjBUQwGY2_7.QX5QTN0wyNzAzNzEzW}

### Notes
-Firstly I learnt in this challenge:<br>
A relative path is any path that does not start at root (i.e., it does not start with /).<br>
A relative path is interpreted relative to your current working directory (cwd).<br>
Your cwd is the directory that your prompt is currently located at.<br>
This means how you specify a particular file, depends on where the terminal prompt is located.<br>

Imagine we want to access some file located at /tmp/a/b/my_file.<br>

If my cwd is /, then a relative path to the file is tmp/a/b/my_file.<br>
If my cwd is /tmp, then a relative path to the file is a/b/my_file.<br>
If my cwd is /tmp/a/b/c, then a relative path to the file is ../my_file. The .. refers to the parent directory.<br>
<br>
-Now my mistake or the redundant approach I took:<br>
I should have seen from the get go I am not in the / directory but since that is the root directory I assumed that by default we would be there only that is why firstly I blindly typed challenge/run in the terminal as I thought we are already in the / directory<br>
When I ran the /challenge/run I knew that would be wrong I just wanted the shell to show me the error and then I realised that I am not in the / directory and then I understood that by default we are in the root directory was wrong<br>
-Hence after that I opened / directory and captured the flag



# Challenge 7 












