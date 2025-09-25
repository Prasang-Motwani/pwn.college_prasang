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
-Then I used `cd` to change the directory to challenge and used the same `ls` command to no fruitition
<br>
-Then I catted the file and I thought I will get the flag by `cat /flag` as it displayed that I found it but was again fooled as it showed permission denied<br>
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



# Challenge 8 removing files

This challenge will create a delete_me file in your home directory! Delete it, then run /challenge/check, which will make sure you've deleted it and then give you the flag

## Solution:

-When the terminal opened up I used the `rm` command to remove or delete the asked file which was "delete_me"
<br>
-Then I used `ls` to check whether it was deleted or not
<br>
-Then I executed /challenge/check to capture the flag

### Commands used:

```sh
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ ls
a
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{4fbLaw3QAi5BgzarHcu5mBZ8mFP.QX2kDM1wyNzAzNzEzW}
```

## Flag:

`
pwn.college{4fbLaw3QAi5BgzarHcu5mBZ8mFP.QX2kDM1wyNzAzNzEzW}
`

### Notes:
-In this challenge i used how to delete or remove a file using `rm` command
<br>
-Sample syntax:
<br>
```
hacker@dojo:~$ touch PWN
hacker@dojo:~$ touch COLLEGE
hacker@dojo:~$ ls
COLLEGE     PWN
hacker@dojo:~$ rm PWN
hacker@dojo:~$ ls
COLLEGE
hacker@dojo:~$
```



# Challenge 9 Moving files

This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

## Solution:

-I moved the given file "/flag" to the given location i.e. "/tmp/hack-the-planet" 
<br>
-Then I ran "/challenge/check" and captured the flag

### Commands used:

```sh
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{IoM14cQ2WDMG245IpYoI-4IqKeY.0VOxEzNxwyNzAzNzEzW}
```

## Flag:

`
pwn.college{IoM14cQ2WDMG245IpYoI-4IqKeY.0VOxEzNxwyNzAzNzEzW}
`

### Notes:
-I leant that how to use the move command to change the location of files
<br>
-Here is a sample syntax:
<br>
```
hacker@dojo:~$ ls
my-file
hacker@dojo:~$ cat my-file
PWN!
hacker@dojo:~$ mv my-file your-file
hacker@dojo:~$ ls
your-file
hacker@dojo:~$ cat your-file
PWN!
hacker@dojo:~$
```



# Challenge 10 Hidden files

In this challenge we have to find the hidden flag, hidden as a dot-prepended file in /.

## Solution

- First it was written that the hidden file is iin the `/` directory so I went into that directory by `cd` command
 <br>
 -Then I tried to execute the file where in the shell displayed permission denied so I tried to read the flag using the `cat` command and captured the flag

  ### Commands used:

```sh
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-30205249219892  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ /.flag-30205249219892
bash: /.flag-30205249219892: Permission denied
hacker@commands~hidden-files:/$ cat .flag-30205249219892
pwn.college{4zWD05UKatxqezf7KgTOdUkAZ16.QXwUDO0wyNzAzNzEzW}
```

## Flag

`
pwn.college{4zWD05UKatxqezf7KgTOdUkAZ16.QXwUDO0wyNzAzNzEzW}
`

### Notes 
-In this challenge I learnt that we can't view all the files using `ls` commands some files are hidden 
<br>
-We can view them using the `ls -a` command.
<br>

-A sample of the above this:

```
hacker@dojo:~$ touch pwn
hacker@dojo:~$ touch .college
hacker@dojo:~$ ls
pwn
hacker@dojo:~$ ls -a
.college	pwn
hacker@dojo:~$
```



# Challenge 11 An Epic filesystem Quest

In this challenge, I have hidden the flag! Here, you will use ls and cat to follow my breadcrumbs and find it! Here's how it'll work:

Your first clue is in /. Head on over there.
Look around with ls. There'll be a file named HINT or CLUE or something along those lines!
cat that file to read the clue!
Depending on what the clue says, head on over to the next directory (or don't!).
Follow the clues to the flag

## Solution

-This was by far the toughest and longest challenge I encountered till now
<br>
-The first steps were easy enough first I opened `/` using `cd` and then I did `ls` and found the next file wherein the clue was stored named "INSIGHT" and I catted it
<br>
-"/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache_" This was next the destination wherein the next file was hidden so I did `ls -a`and found the next file named ".POINTER" so I catted it and it gave the next location
<br>
-After this point I self destructed some points(I tried various things like moving, grepping creating a new file and moving into that and many other things but permission denied was showing and catting and cding was leading to self destruction of files)
<br>
-After a bit of time I tried to use `ls` and write the full path into it so as to not enter that particular directory as I figured out by catting or cding I ws entering that directory but by `ls` I was just listing and not entering
<br>
-Then I repeated this `ls` and `cd` many times in a loop as per the clue directed me and finally I captured the flag

### Commands used:

```sh
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
INSIGHT  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat INSIGHT
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ ls -a
.                        cgc.cpython-38.pyc     snimmuc_nxp.cpython-38.pyc
..                       javavm.cpython-38.pyc  userland.cpython-38.pyc
.POINTER                 linux.cpython-38.pyc   windows.cpython-38.pyc
__init__.cpython-38.pyc  simos.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ cat .POINTER
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/sound/soc/adi

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ ls /opt/linux/linux-5.4/sound/soc/adi
Kconfig  Makefile  SECRET-TRAPPED  axi-i2s.c  axi-spdif.c
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ cat /opt/linux/linux-5.4/sound/soc/adi/SECRET-TRAPPED
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/include/config/strict/kernel

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ ls /opt/linux/linux-5.4/include/config/strict/kernel
ALERT-TRAPPED  rwx.h
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ cat /opt/linux/linux-5.4/include/config/strict/kernel/ALERT-TRAPPED
Congratulations, you found the clue!
The next clue is in: /usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/Encode/Unicode

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ ls -a /usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/Encode/Unicode
.  ..  .TEASER  Unicode.so
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ cat /usr/lib/x86_64-linux-gnu/perl/5.30.0/auto/Encode/Unicode/.TEASER
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/simos/__pycache__$ cd /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular$ ls
GIST  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular$ file GIST
GIST: ASCII text
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular$ cat GIST
Tubular find!
The next clue is in: /usr/share/racket/pkgs/htdp-lib/htdp/bsl/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular$ ls -a /usr/share/racket/pkgs/htdp-lib/htdp/bsl/compiled
.   HINT                 print-width_rkt.zo  reader_rkt.zo    runtime_rkt.zo
..  print-width_rkt.dep  reader_rkt.dep      runtime_rkt.dep
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular$ file /usr/share/racket/pkgs/htdp-lib/htdp/bsl/compiled/HINT
/usr/share/racket/pkgs/htdp-lib/htdp/bsl/compiled/HINT: ASCII text
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular$ cat /usr/share/racket/pkgs/htdp-lib/htdp/bsl/compiled/HINT
Lucky listing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/tornado/test/gettext_translations

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/STIX-Web/Misc/Regular$ cd /usr/local/lib/python3.8/dist-packages/tornado/test/gettext_translations
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/tornado/test/gettext_translations$ ls -a
.  ..  INFO  fr_FR
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/tornado/test/gettext_translations$ cat INFO
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/compatibility-lib/mzlib
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/tornado/test/gettext_translations$ ls -a /usr/share/racket/pkgs/compatibility-lib/mzlib
.                  control.rkt      md5.rkt           stxparam.rkt
..                 date.rkt         os.rkt            surrogate.rkt
NUGGET             deflate.rkt      plt-match.rkt     tar.rkt
a-signature.rkt    defmacro.rkt     port.rkt          thread.rkt
a-unit.rkt         etc.rkt          pregexp.rkt       trace.rkt
async-channel.rkt  file.rkt         pretty.rkt        traceld.rkt
awk.rkt            for.rkt          private           trait.rkt
class.rkt          foreign.rkt      process.rkt       transcr.rkt
cm-accomplice.rkt  include.rkt      restart.rkt       unit-exptime.rkt
cm.rkt             inflate.rkt      runtime-path.rkt  unit.rkt
cmdline.rkt        info.rkt         sandbox.rkt       unit200.rkt
cml.rkt            integer-set.rkt  sendevent.rkt     unitsig.rkt
compat.rkt         kw.rkt           serialize.rkt     unitsig200.rkt
compile.rkt        list.rkt         shared.rkt        zip.rkt
compiled           match.rkt        string.rkt
contract.rkt       math.rkt         struct.rkt
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/tornado/test/gettext_translations$ cat /usr/share/racket/pkgs/compatibility-lib/mzlib/NUGGET
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/tornado/test/gettext_translations$ cat /usr/share/racket/pkgs/compatibility-lib/mzlib/NUGGET
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{0K5vgipgTZ4mfiAJQgW2DsY3yRa.QX5IDO0wyNzAzNzEzW}
```

## Flag :

`
pwn.college{0K5vgipgTZ4mfiAJQgW2DsY3yRa.QX5IDO0wyNzAzNzEzW}
`

### Notes:

-A lot of redundant steps taken by me 
<br>
-I did cd into the file to see what the self destruction would like, I was curious
<br>
-Then I catted it but that also led to self destruction of the flag
<br>
-I also tried creating a new file and moving that file there, grepping "pwn", comparing it with other files using `diff`
<br>
-Then I finally listed it as I realised listing its contents is not entering it and then repeated the steps of `ls` , `cd` and `cat` as directed by the next clue and at at point I thought I was going wrong as the process was seemingly too long but I persisted and captured the flag



# Challenge 12 Making Directories 

-To create a /tmp/pwn directory and make a college file in it! Then run /challenge/run, which will check your solution and give you the flag

## Solution

-I created a directory "/tmp/pwn" using the `mkdir` command
<br>
-Then I created a file "college" in the directory created above using `touch` command
<br>
-Then I ran "/challenge/run" and captured the flag


### Commands used:

```sh
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{YDot-fED7sOBHZ2FslZnVSsq5pB.QXxMDO0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{YDot-fED7sOBHZ2FslZnVSsq5pB.QXxMDO0wyNzAzNzEzW}
`

### Notes:

In this challenge I learnt how to use the create new directories using the `mkdir` command



# Challenge 13 finding files

Now it's your turn. I've hidden the flag in a random directory on the filesystem. It's still called flag. Go find it!

## Solution:

-First I used `find` command in the `/` directory to find all the files named flag
<br>
-Alot of locations turned up I started catting them and found and captured the flag in the second address
<br>

### Commands used:

```sh
hacker@commands~finding-files:~$ find -name flag
hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/tmp/tmp.TpSOPGOVKK’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/share/doc/gcc-9-base/sanitizer/flag
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
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ /usr/local/lib/python3.8/dist-packages/pwnlib/flag
bash: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /usr/share/doc/gcc-9-base/sanitizer/flag
pwn.college{U2YrtCItTDJNqg38GwNlZR5giDs.QXyMDO0wyNzAzNzEzW}hacker@commands~finding-files:~$
```

## Flag:

`
pwn.college{U2YrtCItTDJNqg38GwNlZR5giDs.QXyMDO0wyNzAzNzEzW}
`

### Notes:

-In this challenge I learnt how to use the `find` command to find files and the outcomes if we don't write criterias or locations wherein the file is to be searched
<br>
-So now we know how to list, read, and create files. But how do we find them? We use the find command!

The find command takes optional arguments describing the search criteria and the search location. If you don't specify a search criteria, find matches every file. If you don't specify a search location, find uses the current working directory (.). For example:

```
hacker@dojo:~$ mkdir my_directory
hacker@dojo:~$ mkdir my_directory/my_subdirectory
hacker@dojo:~$ touch my_directory/my_file
hacker@dojo:~$ touch my_directory/my_subdirectory/my_subfile
hacker@dojo:~$ find
.
./my_directory
./my_directory/my_subdirectory
./my_directory/my_subdirectory/my_subfile
./my_directory/my_file
hacker@dojo:~$
```

And when specifying the search location:

```
hacker@dojo:~$ find my_directory/my_subdirectory
my_directory/my_subdirectory
my_directory/my_subdirectory/my_subfile
hacker@dojo:~$
```

And, of course, we can specify the criteria! For example, here, we filter by name:

```
hacker@dojo:~$ find -name my_subfile
./my_directory/my_subdirectory/my_subfile
hacker@dojo:~$ find -name my_subdirectory
./my_directory/my_subdirectory
hacker@dojo:~$
```

You can search the whole filesystem if you want!

```
hacker@dojo:~$ find / -name hacker
/home/hacker
hacker@dojo:~$
```



# Challenge 14 linking files

In this level the flag is, as always, in /flag, but /challenge/catflag will instead read out /home/hacker/not-the-flag. Use the symlink

## Solution:

-This challenge was pretty straightforward
<br>
-What we had to do was to fool the system into gining us the link by creating symlink and by doing `ls -l` we could see noth the flag is actually the flag and hence did /challenge/catflag capture the flag

### Commands used:

```sh
hacker@commands~linking-files:~$ cat /flag
cat: /flag: Permission denied
hacker@commands~linking-files:~$ cat /challenge/catflag
#!/opt/pwn.college/bash

fold -s <<< "About to read out the /home/hacker/not-the-flag file!"
cat /home/hacker/not-the-flag
cat: /home/hacker/not-the-flag: No such file or directory
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ cat /home/hacker/not-the-flag
cat: /home/hacker/not-the-flag: Permission denied
hacker@commands~linking-files:~$ ls -l
total 12
-rw-r--r-- 1 hacker hacker 136 Sep 24 15:00 SECRET-TRAPPED
-rw-r--r-- 1 root   hacker  60 Sep 23 15:44 a
lrwxrwxrwx 1 hacker hacker   5 Sep 25 19:27 not-the-flag -> /flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{Y6d6Wx6hftQF6nvdn684AD8EVBH.QX5ETN1wyNzAzNzEzW}
```

## Flag:

`
pwn.college{Y6d6Wx6hftQF6nvdn684AD8EVBH.QX5ETN1wyNzAzNzEzW}
`

### Notes:

-In this challenge I learnt what hard links and soft/symbolic links are, how to create and use them and  soft links are preferred over hard links
<br>
-If you use Linux (or computers) for any reasonable length of time to do any real work, you will eventually run into some variant of the following situation: you want two programs to access the same data, but the programs expect that data to be in two different locations. Luckily, Linux provides a solution to this quandary: links.

Links come in two flavors: hard and soft (also known as symbolic) links. We'll differentiate the two with an analogy:

A hard link is when you address your apartment using multiple addresses that all lead directly to the same place (e.g., Apt 2 vs Unit 2).
A soft link is when you move apartments and have the postal service automatically forward your mail from your old place to your new place.
In a filesystem, a file is, conceptually, an address at which the contents of that file live. A hard link is an alternate address that indexes that data --- accesses to the hard link and accesses to the original file are completely identical, in that they immediately yield the necessary data. A soft/symbolic link, instead, contains the original file name. When you access the symbolic link, Linux will realize that it is a symbolic link, read the original file name, and then (typically) automatically access that file. In most cases, both situations result in accessing the original data, but the mechanisms are different.

Hard links sound simpler to most people (case in point, I explained it in one sentence above, versus two for soft links), but they have various downsides and implementation gotchas that make soft/symbolic links, by far, the more popular alternative.

In this challenge, we will learn about symbolic links (also known as symlinks). Symbolic links are created with the ln command with the -s argument, like so:

hacker@dojo:~$ cat /tmp/myfile
This is my file!
hacker@dojo:~$ ln -s /tmp/myfile /home/hacker/ourfile
hacker@dojo:~$ cat ~/ourfile
This is my file!
hacker@dojo:~$
You can see that accessing the symlink results in getting the original file contents! Also, you can see the usage of ln -s. Note that the original file path comes before the link path in the command!

A symlink can be identified as such with a few methods. For example, the file command, which takes a filename and tells you what type of file it is, will recognize symlinks:

```
hacker@dojo:~$ file /tmp/myfile
/tmp/myfile: ASCII text
hacker@dojo:~$ file ~/ourfile
/home/hacker/ourfile: symbolic link to /tmp/myfile
hacker@dojo:~$
```















