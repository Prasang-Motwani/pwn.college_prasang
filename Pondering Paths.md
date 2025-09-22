
# The Root

In this challenge we have to launch a terminal and invoke the path of pwn to capture the flag

## Solution:

Write /pwn to invoke the path of pwn and hence capture the flag or obtain the flag

```sh
hacker@paths~the-root:~$ /pwn
```

## Flag:
```
pwn.college{gDXqAS_YxIyiTvhTYQ8ooGTJXiZ.QX4cTO0wyNzAzNzEzW}
```
### References:

-[link 1](https://pwn.college/linux-luminarium/paths/)

### Notes:
In this challenge I learnt:<br>
The linux filesystem is a tree<br>
It has a root written as / which is a directory and every directory can further contain other directories by their path<br>
A path from the root starts from / and goes futher into the set of directories to be opened to find the desired file<br>
Every piece of path has another /<br>



# Program and Absolute paths

In this challenge, the name of the challenge program in this level is run, and it lives in the /challenge directory.<br>
The challenge requires you to execute it by invoking its absolute path. You to execute the run file that is in the challenge directory that is, in turn, in the / directory.

## Solution
This ws a simple challenge or should I say a one step extension of the previous challenge.<br>
I was asked to find it's absolute path which I did by doing /challenge/run on the terminal.<br>
By doing this the run file got executed which was in the challenge directory which in turn was in the / directry i.e. in the root directory 

```sh
hacker@paths~program-and-absolute-paths:~$ /challenge/run
```

## Flag
pwn.college{wFL4T4HyGJ09DL81GqlS9FYwbMY.QX1QTN0wyNzAzNzEzW}

### References:

-[link 1](https://pwn.college/linux-luminarium/paths/)

### Notes

In this challenge I learnt what an absolute path is and how to invoke it. <br>
I also saw how a file can be stored in a directory which in turn is also stored in the root directory.<br>
Mistake- Not a mistake per se but a clearity in the concept. Earlier I thought that in the previous challenge /challenge is a root directory which we are accessing but via this challenge I understood that the root directory is always / only and challenge was the file to be ran just like in this program run was the file to be ran whih was in the challenge directory which in turn was in the / directory.<br>
So the directory concept which got a bit mangled got cleared in this challenge 



# Position Thyself

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program.

## Solution:
After the terminal comes up the user will invoke the path of run viqa challenge to access the run file.<br>
An error will show up telling us to change the directory and will tell the path of the directory in which the file is present.<br>
The user will change the directory using the cd command on the terminal.<br>







