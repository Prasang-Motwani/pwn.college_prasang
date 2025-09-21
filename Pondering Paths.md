
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



