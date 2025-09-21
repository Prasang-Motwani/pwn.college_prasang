# Intro to Commands

To invoke the hello command

## Solution:

Connected my ubuntu terminal to pwn.college host using ssh command
After connecting I typed the hello command in the terminal 
This was the asked challenege and on completing I got the flag


```sh
prasang@DESKTOP-7JBR2OV:~$ ssh -i key hacker@dojo.pwn.college
Connected!
hacker@hello~intro-to-commands:~$ hello
```

## Flag:
```
pwn.college{0e9QujOjmIdmozqiGW-iQRA4hJN.QX3YjM1wyNzAzNzEzW}
```
### References:
- [link 1](https://pwn.college/linux-luminarium/hello/)

### Notes:
While solving this challenge I learnt how to connect my desktop ubuntu to the host pwn.college
I learnt what a command is and how it is run



# Intro to Arguments

Run the hello command with an argument "hacker"

## Solution:
After starting this challenge
I typed hello then typed a single word "hacker" acter it
I did this cause first we write the command and the subsequent words are arguments for it
In this challenge only a single argument "hacker" was asked

```sh
hacker@hello~intro-to-arguments:~$ hello hackers
```

## Flag:
```
pwn.college{cjP5MboIa6pyP2AQUTVqj9wB403.QX4YjM1wyNzAzNzEzW}
```
### References:
- [link 1](https://pwn.college/linux-luminarium/hello/)

### Notes:
I learnt what an argument is ie additional data passed to the command
The first word is the command and the subsequent words are arguments
Here only one argument "hacker" was asked to be added after the hello command



# Command History

In this challenge we will  inject the flag into my history. 
Bring up a terminal, hit the up arrow, and grab it.

## Solution:

I pressed the upwards arrow on my keyboard
The flag appeared on my terminal to be grabbed and thats what I did

```sh
hacker@hello~command-history:~$ the flag is pwn.college{QNBfhOym3W6fuqruW5d-Qrd9rCP.0lNzEzNxwyNzAzNzEzW}
```

## Flag:
```
pwn.college{QNBfhOym3W6fuqruW5d-Qrd9rCP.0lNzEzNxwyNzAzNzEzW}
```

### References
- [link 1](https://pwn.college/linux-luminarium/hello/)

### Notes

In this challenge I learnt that the shell saves the previous commands that we invoked or typed in the past
We can navigate through them using the up/down arrow keys
This is helpful as if we have to repeat some commands in a program then we can just access the old one in our history using up and down keys
This will save us alot of time

  


