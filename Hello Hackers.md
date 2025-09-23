# Challenge 1 Intro to Commands

In this challenge, you will invoke your first command! When you type a command and hit enter, the command will be invoked, as so:

```sh
hacker@dojo:~$ whoami
hacker
hacker@dojo:~$
```

Here, the user executed the whoami command, which simply prints the username (hacker) to the terminal. When the command terminates, the shell once again displays the prompt, ready for the next command.

In this level, invoke the hello command to get the flag! Keep in mind: commands in Linux are case sensitive: hello is different from HELLO.

## Solution:

-First the user will connected his Ubuntu terminal to pwn.college host using ssh command.<br>
-After connecting type the `hello` command in the terminal.<br> 
-`hello` command will be invoked. This was the asked challenege and after this capture the flag.<br>

### Commands run:

```sh
prasang@DESKTOP-7JBR2OV:~$ ssh -i key hacker@dojo.pwn.college
Connected!
hacker@hello~intro-to-commands:~$ hello
```

## Flag:

`
pwn.college{0e9QujOjmIdmozqiGW-iQRA4hJN.QX3YjM1wyNzAzNzEzW}
`

### Notes:

-While solving this challenge I learnt how to connect my desktop ubuntu to the host pwn.college<br>
-I learnt what a command is and how it is run.<br>
-The `$` at the end of the prompt shows that the user is not an administrative user.<br>
-Commands in linux are case sensitive



# Challenge 2 Intro to Arguments

Let's try something more complicated: a command with arguments, which is what we call additional data passed to the command. When you type a line of text and hit enter, the shell actually parses your input into a command and its arguments. The first word is the command, and the subsequent words are arguments. Observe:

```sh
hacker@dojo:~$ echo Hello
Hello
hacker@dojo:~$
```

In this case, the command was echo, and the argument was Hello. echo is a simple command that "echoes" all of its arguments back out onto the terminal, like you see in the session above.

Let's look at echo with multiple arguments:

```sh
hacker@dojo:~$ echo Hello Hackers!
Hello Hackers!
hacker@dojo:~$
```

In this case, the command was echo, and Hello and Hackers! were the two arguments to echo. Simple!

In this challenge, to get the flag, you must run the hello command (NOT the echo command) with a single argument of hackers. 

## Solution:

-After starting this challenge;<br>
-I typed hello then typed a single word "hacker"<br>
-I did this because first we write the command and the subsequent words are arguments for it<br>
-In this challenge only a single argument "hacker" was asked<br>
-In short invoke ```hello``` command with argument ```hackers```

### Commands run:

```sh
hacker@hello~intro-to-arguments:~$ hello hackers
```

## Flag:

`
pwn.college{cjP5MboIa6pyP2AQUTVqj9wB403.QX4YjM1wyNzAzNzEzW}
`

### Notes:

-I learnt what an argument is ie additional data passed to the command<br>
-The first word is the command and the subsequent words are arguments<br>
-Here only one argument "hacker" was asked to be added after the hello command<br>
-When you type a line of text and hit enter, the shell actually parses your input into a command and arguments.



# Challenge 3 Command History

You're going to type a lot of commands, and typing everything from scratch can be annoying. Luckily, the shell saves a history of every command you invoke.

You can scroll through those saved commands with the up/down arrow keys, and we'll practice that in this challenge. This challenge will inject the flag into your history. Bring up a terminal, hit the up arrow, and grab it! In other challenges, the history will contain the log of the commands you've run, so if you need to run a similar command again, you can use the arrow keys to scroll through and find it

## Solution:

-I pressed the upwards arrow key on my keyboard<br>
-The flag appeared on my terminal to be grabbed and thats what I did<br>

### Commands run:

```sh
`up` arrow key to scroll to previous command
hacker@hello~command-history:~$ the flag is pwn.college{QNBfhOym3W6fuqruW5d-Qrd9rCP.0lNzEzNxwyNzAzNzEzW}
```

## Flag:

`
pwn.college{QNBfhOym3W6fuqruW5d-Qrd9rCP.0lNzEzNxwyNzAzNzEzW}
`

### Notes:

-In this challenge I learnt that the shell saves the previous commands that we invoked or typed in the past<br>
-We can navigate through them using the up/down arrow keys<br>
-This is helpful as if we have to repeat some commands in a program then we can just access the old one in our history using up and down keys<br>
-This will save us alot of time<br>

  


