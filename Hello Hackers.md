# Challenge 1 Intro to Commands

To invoke the hello command

## Solution:

Connected my ubuntu terminal to pwn.college host using ssh command.<br>
After connecting I typed the hello command in the terminal.<br> 
This was the asked challenege and on completing I got the flag.<br>

### Commands run:

```sh
prasang@DESKTOP-7JBR2OV:~$ ssh -i key hacker@dojo.pwn.college
Connected!
hacker@hello~intro-to-commands:~$ hello
```

## Flag:

```
pwn.college{0e9QujOjmIdmozqiGW-iQRA4hJN.QX3YjM1wyNzAzNzEzW}
```

### Notes:

While solving this challenge I learnt how to connect my desktop ubuntu to the host pwn.college<br>
I learnt what a command is and how it is run.



# Challenge 2 Intro to Arguments

Run the hello command with an argument "hacker"

## Solution:

After starting this challenge;<br>
I typed hello then typed a single word "hacker"<br>
I did this because first we write the command and the subsequent words are arguments for it<br>
In this challenge only a single argument "hacker" was asked<br>

### Commands run:

```sh
hacker@hello~intro-to-arguments:~$ hello hackers
```

## Flag:

```
pwn.college{cjP5MboIa6pyP2AQUTVqj9wB403.QX4YjM1wyNzAzNzEzW}
```

### Notes:

I learnt what an argument is ie additional data passed to the command<br>
The first word is the command and the subsequent words are arguments<br>
Here only one argument "hacker" was asked to be added after the hello command<br>



# Challenge 3 Command History

In this challenge we will  inject the flag into my history. 
Bring up a terminal, hit the up arrow, and grab it.

## Solution:

I pressed the upwards arrow key on my keyboard<br>
The flag appeared on my terminal to be grabbed and thats what I did<br>

### Commands run:
```sh
hacker@hello~command-history:~$ the flag is pwn.college{QNBfhOym3W6fuqruW5d-Qrd9rCP.0lNzEzNxwyNzAzNzEzW}
```

## Flag:

```
pwn.college{QNBfhOym3W6fuqruW5d-Qrd9rCP.0lNzEzNxwyNzAzNzEzW}
```

### Notes:

In this challenge I learnt that the shell saves the previous commands that we invoked or typed in the past<br>
We can navigate through them using the up/down arrow keys<br>
This is helpful as if we have to repeat some commands in a program then we can just access the old one in our history using up and down keys<br>
This will save us alot of time<br>

  


