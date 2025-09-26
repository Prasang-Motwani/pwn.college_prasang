# Challenge 1 Learning from documentation

The program for this challenge is /challenge/challenge, and you'll need to invoke it properly in order for it to give you the flag. Let's pretend that this is its documentation:
<br>
Welcome to the documentation for /challenge/challenge! To properly run this program, you will need to pass it the argument of --giveflag.

## Solution

-This was a pretty straightforward challenge all we had to do was add the "--giveflag" argument to "/challenge/challenge"

### Commands used:

```sh
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{0vAC6IpnZBS63GiUe-KFEf1iwNR.QX0ITO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{0vAC6IpnZBS63GiUe-KFEf1iwNR.QX0ITO0wyNzAzNzEzW}
`

### Notes

-The typical need you'll have for documentation is just to figure out how to use all these dang programs, and a specific case of that is figuring out what arguments to specify on the command line. This module will mostly dig into that concept, as a proxy for figuring out how to use the programs in general. Through the rest of the module, you'll go through various ways of asking the environment for help for the programs, but first, we'll dig into the concept of reading documentation.
<br>
The correct usage of programs depends, in a large part, on the proper specification of arguments to them. Recall the -a of ls -a in the hidden files challenge of the Basic Commands module: that -a was an argument that told ls to list out hidden files as well as non-hidden files. Because we wanted to list out hidden files, invoking ls with the -a argument was the correct way to use it in our scenario.



# Challenge 2 Learning Complex usage

Welcome to the documentation for /challenge/challenge! This program allows you to print arbitrary files to the terminal, when given the --printfile argument. The argument to the --printfile argument is the path of the flag to read. For example, /challenge/challenge --printfile /challenge/DESCRIPTION.md will print out the description of the level!

Given that documentation, go get the flag

## Solution:

-First I wrote the given command and its 2 arguments which displayed the description of the challenge
<br>
-Then after it to find the path of the file I used the `find` command which gave alot of results
<br>
-The most obvious and shortest to type was `/flag` so that's what I started with and it gave me the flag
<br>

### Commands used:

```sh
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DESCRIPTION.md
Correct argument! Here is the /challenge/DESCRIPTION.md file:
While using most commands is straightforward, the usage of some commands can get quite complex.
For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!
Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...

This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](/linux-luminarium/commands).
`find` has a `-name` argument, and the `-name` argument itself takes an argument specifying the name to search for.
Many other commands are analogous.

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!

Given that documentation, go get the flag!
hacker@man~learning-complex-usage:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.TpSOPGOVKK’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{0jBEVHbWLAe9DDhO8Nwlnj4lohb.QX1ITO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{0jBEVHbWLAe9DDhO8Nwlnj4lohb.QX1ITO0wyNzAzNzEzW}
`

## Notes:

-I learnt that are commands whose arguments can have futher arguments of its own
<br>
-An example of that is the file command-find has a -name argument, and the -name argument itself takes an argument specifying the name to search for. There are many other commands like this



# Challenge 3 Reading manuals 

The challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. You must learn this option through the man page for challenge!

## Solution

-First I opened the manual page for challenge using `man challenge` and read the manual
<br>
-It showed 3 different arguments and on executing the 3rd argument we would get the flag when we would put NUM = 837 but I exxecuted all the arguments just because I was curious, first one gave a poem while the other was supposed to give the version but it just prompted "I'm exactly the version I need to be!"

### Commands used:

```sh
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --fortune
Who made the world I cannot tell;
'Tis made, and here am I in hell.
My hand, though now my knuckles bleed,
I never soiled with such a deed.
                -- A. E. Housman
hacker@man~reading-manuals:~$ /challenge/challenge --version
I'm exactly the version I need to be!
hacker@man~reading-manuals:~$ /challenge/challenge --tqdoaj 837
Correct usage! Your flag: pwn.college{8KTtqHdoVW-BN3ajZZvQRr7zobn.QX0EDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{8KTtqHdoVW-BN3ajZZvQRr7zobn.QX0EDO0wyNzAzNzEzW}
`

## Notes:

-In this challenge I learnt how to use `man` command which is short for manual.
<br>
-Its pretty simple to use just the name after the `man` command eg if the name is challenge as it was in this one then just use `man challenge` and not man "path of challenge" if we would put path of any file then the `man` command would give garbage value 



# Challenge 4 Searching Manuals 

Find the option that will give you the flag by reading the challenge man page.

## Solution
-This challenge was pretty straightforward first I opened manual of challenge page using `man` command
<br>
-Then I browsed through the manual to find the correct argument to give the flag
<br>
-I used `/` to search the manual wherein I searched the word flag and used `n` to move forward to the next result and by doing this I found the right argument to obtain the flag after navigating through the manual page a bit
<br>
-Then I pressed q typed the command and argument on the terminal and captured the flag

### Commands used:

```sh
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --wtdu
Initializing...
Correct usage! Your flag: pwn.college{gySYrJwjqaeBDRHYLIGPgw8cARk.QX1EDO0wyNzAzNzEzW}
```

## Flag: 

`
pwn.college{gySYrJwjqaeBDRHYLIGPgw8cARk.QX1EDO0wyNzAzNzEzW}
`

## Notes

-In this I learnt how to navigate through the manual page by searching for words and then moving to the next or previous results
<br>
-You can scroll man pages with the arrow keys (and PgUp/PgDn) and search with /. After searching, you can hit n to go to the next result and N to go to the previous result. Instead of /, you can use ? to search backwards



# Challenge 5 Searching for manuals 

-This level is tricky: it hides the manpage for the challenge by randomizing its name. Luckily, all of the manpages are gathered in a searchable database, so you'll be able to search the man page database to find the hidden challenge man page! To figure out how to search for the right manpage, read the man page manpage by doing: man man!

HINT 1: man man teaches you advanced usage of the man command itself, and you must use this knowledge to figure out how to search for the hidden manpage that will tell you how to use /challenge/challenge

HINT 2: though the manpage is randomly named, you still actually use /challenge/challenge to get the flag

## Solution:

-First I used the man page for the man page to understand it more effieciently and to grasp its advanced commands
<br>
-I tried to search "hidden" or "search" inside the man page of man as it was 490 lines long and wasn't possible to read but nothing came out of it
<br>
-Then I I started reading it and found the `-k` command as it searched particular keywords inside the manpage which I thought could be useful
<br>
-I searched the keyword "flag" but alot of results came out so I decided to first try out another keyword and find a comman intersection point
<br>
-I searched the keyword challenge as the comaand was still name "/challenge/challenge" and found it as it had only one and that was in the "flag" keyword search too and its description was literally "printv the flag!"
<br>
-Then I ontained the required page and used `man` on it and as one of the previous challenge it had an argument which on giving a certain number which was 664 in my case as a sub argument gave the flag and that's how I captured the flag
<br>

### Commands used:

```sh
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k flag
dpkg-buildflags (1)  - returns build flags to use during package build
Dpkg::BuildFlags (3perl) - query build flags
dtfkcikmsm (1)       - print the flag!
fegetexceptflag (3)  - floating-point rounding and exception handling
fesetexceptflag (3)  - floating-point rounding and exception handling
i386 (8)             - change reported architecture in new program environment and/or set personality flags
ioctl_iflags (2)     - ioctl() operations for inode flags
linux32 (1)          - change reported architecture in new program environment and/or set personality flags
linux64 (1)          - change reported architecture in new program environment and/or set personality flags
pcap-config (1)      - write libpcap compiler and linker flags to standard output
security_compute_av_flags (3) - query the SELinux policy database in the kernel
security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel
set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity checking and error displaying
set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity checking and error di...
set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity checking and error displa...
setarch (1)          - change reported architecture in new program environment and/or set personality flags
setarch (8)          - change reported architecture in new program environment and/or set personality flags
x86_64 (8)           - change reported architecture in new program environment and/or set personality flags
hacker@man~searching-for-manuals:~$ man -k challenge
dtfkcikmsm (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man dtfkcikmsm
hacker@man~searching-for-manuals:~$ /challenge/challenge  --dtfkci 664
Correct usage! Your flag: pwn.college{ID6dtXJ6fkci49km4ETsKEmc7A-.QX2EDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{ID6dtXJ6fkci49km4ETsKEmc7A-.QX2EDO0wyNzAzNzEzW}
`

### Notes:

-In this challenge I used advanced usage of the `man` command itself by accessing the manual of the `man` command using the `man` command itself



# Challenge 6 Helpful Programs

In this level, you will practice reading a program's documentation with --help. Try it out!

## Solution:

-First it was already told to use the help command so I used the `--help` to access the help page of "/challenge/challenge"
<br>
-Then I used "/challenge/challenge -p" to get the secret number to be used with the -g argument. The number it gave me was 473
<br>
-Then I used "/challenge/challenge -g 473" and obtained the flag

### Commands used:

```sh
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -g
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: expected one argument
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 473
hacker@man~helpful-programs:~$ /challenge/challenge -g 473
Correct usage! Your flag: pwn.college{UzOJtQ-_yA_zbkpMEsZ4UyaNi7w.QX3IDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{UzOJtQ-_yA_zbkpMEsZ4UyaNi7w.QX3IDO0wyNzAzNzEzW}
`

### Notes:

-I learnt what is the `--help` command is and what it does
<br>
-Some programs don't have a man page, but might tell you how to run them if invoked with a special argument. Usually, this argument is `--help`, but it can often be -h or, in rare cases, -?, `help`, or other esoteric values like `/`? (though that latter is more frequently encountered on Windows).



# Challenge 7 Help for builtins

 In this challenge, we'll practice using help to look up help for builtins. This challenge's challenge command is a shell builtin, rather than a program. Like before, you need to lookup its help to figure out the secret value to pass to it!

 ## Solution:

 -First I did "help challenge" for the challenge builtin as asked in the challenge 
 <br>
 -From there I found the argument to challenge was secret and the argument to that argument was "MCIbAI1n"
 <br>
 -So I wrote the above mentioned command and arguments and captured the flag>

 ### Commands used:

 ```sh
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "MCIbAI1n".
hacker@man~help-for-builtins:~$ challenge --secret MCIbAI1n
Correct! Here is your flag!
pwn.college{MCIbAI1nTQ0oPSXLyACpGahDTGo.QX0ETO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{MCIbAI1nTQ0oPSXLyACpGahDTGo.QX0ETO0wyNzAzNzEzW}
`

### Notes:

-In this challenge I learnt:

Some commands, rather than being programs with man pages and help options, are built into the shell itself. These are called builtins. Builtins are invoked just like commands, but the shell handles them internally instead of launching other programs. You can get a list of shell builtins by running the builtin help, as so:

`
hacker@dojo:~$ help
`

You can get help on a specific one by passing it to the help builtin. Let's look at a builtin that we've already used earlier, cd!

```
hacker@dojo:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]

    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable.
...

```



