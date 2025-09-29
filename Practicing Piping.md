# Challenge 1 Redirecting output

In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase)

## Solution:

-This challenge was pretty straightforward I redirected the text "PWN" to the file "COLLEGE" using `>` and captured the flag
<br>

### Commands used:

```sh
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{QMk5MadvXwheXe0aGaANlhxL0yf.QX0YTN0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{QMk5MadvXwheXe0aGaANlhxL0yf.QX0YTN0wyNzAzNzEzW}
`

### Notes:

-In this challenge I learnt how to redirect output to a file
<br>
- You can accomplish this with the > character, as so:

`
hacker@dojo:~$ echo hi > asdf
`

This will redirect the output of echo hi (which will be hi) to the file asdf. You can then use a program such as cat to output this file:

```
hacker@dojo:~$ cat asdf
hi
```



# Challenge 2 Redirectng more output

In this level, /challenge/run will once more give you a flag, but only if you redirect its output to the file myflag. Your flag will, of course, end up in the myflag file!

## Solution:

-This was a pretty straightforward challenge too I redirected the output for "/challenge/run" to "myfile" using `>` and then catted "myfile" to capture the flag
<br>

### Commands used:

```sh
[FAIL]   You have not redirected anything for this process' stdout.
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
'[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{odZN6qFEgQ7mKftSjFZ4VUsj78_.QX1YTN0wyNzAzNzEzW}
```

## Flag:

`
pwn.college{odZN6qFEgQ7mKftSjFZ4VUsj78_.QX1YTN0wyNzAzNzEzW}
`

### Notes:

-Aside from redirecting the output of echo, you can, of course, redirect the output of any command.
<br>
-You'll notice that /challenge/run will still happily print to your terminal, despite you redirecting stdout. That's because it communicates its instructions and feedback over standard error, and only prints the flag over standard out



# Challenge 3 Appending output

