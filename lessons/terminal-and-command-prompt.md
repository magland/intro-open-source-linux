# The terminal and command prompt

Don’t fret… the terminal is your friend… as an open source software developer, you will soon grow to feel at home in the terminal. In this lesson you will learn to open a terminal, use some basic commands, and learn some crucial shortcuts. We will also touch upon the notions of files and directories.

## How to open a terminal

Depending on your flavor of Linux, opening a terminal may be as easy as pressing [ctrl]+t, or it may be as difficult as spending hours of fruitless searching. I recommend that you try pressing [ctrl]+t (that is holding down the [ctrl] key and then pressing the letter “t”). If that opens a window that looks something like one of the following then you are in business!

FIG: examples of terminal windows

But on some systems, that common shortcut is not registered. If that is the case for you, then you will need to click around the desktop a bit searching for something called ‘terminal’. Once you find it, then I recommend you figure out how to configure a keyboard shortcut to launch this program. Do a google search if you get stuck.

## It’s like texting with the computer

Using the terminal is like having a text conversation with your computer. Except, the computer always responds immediately, often doesn’t understand you, and is never forgiving about even the slightest spelling errors. You type in a message (or command), press enter, and then you get a response in the form of text from the computer. Try typing in random messages into the terminal to see what responses you can get. Don’t worry, you probably won’t do any harm. Worst case, close the terminal and open a new one.

## The command prompt, current directory, and the `cd` command

You have probably noticed that the terminal indicates when you are allowed to enter a new command by showing a command prompt. This usually (but not always) displays your current working directory (more about that later) followed by some special characters indicating that you may now enter a command. For example, in my terminal, I see the following

```
[insert command prompt]
```

indicating that my current directory is `/home/magland`. Of all the directories (or folders) on my file system, this is the current directory or the directory that I am now in. If you have multiple terminal windows open, then each has its own current directory. 

There is a very important command that allows you to change the current directory. It is called `cd` and stands for change directory. For example, the following will change to the `/tmp` directory:

```
cd /tmp
```

Try it and you should see the command prompt change to reflect the new current directory. You can always get back to the default (or home) directory by just typing

```
cd
```

On many systems your home directory will be `/home/[username]` where `[username]` is name you used when you logged on to your computer.

## Files, directories, and the `ls` command

You are probably already familiar with folders (aka directories) and files, but let’s formalize it anyway. Some information on your computer is stored in memory (or RAM), but that information disappears whenever you restart your computer. Other persistent information (that survives even a reboot) is stored in the filesystem, also known as on the disk, or on the hard drive of your computer. The filesystem is organized hierarchically into directories and files.

What’s the relationship between files and directories? It’s easy. Files hold data (like documents, pictures, music, and programs), and directories contain files and other directories. For example, `/home/magland` is a directory (not a file) and you can visualize the contents of that directory by typing `ls` (short for list):

```
[show results]
```

Here [*] and [*] are files, and `Downloads` and [*] are other directories contained inside `/home/magland`.

You can think of the terminal as a text adventure game! The current directory is like the room you are currently in, and when you type `ls` you can see what’s inside the room (the files) and where you are allowed to go from there (the directories). To change to the `Downloads` directory and see what’s in that room (directory), type

```
cd Downloads
ls -l
```

Note that by putting in the `-l` option we get more details about the files, such as their sizes and permissions (we’ll talk more about permissions in a different lesson).

## Cancelling a command and using the clipboard

Suppose you execute a command, and the computer takes a long time to respond, or perhaps the program you start is designed to run until interrupted. It is very important to know how to cancel or interrupt such a program… you press [ctrl]+c (I think the “c” stands for cancel, but I am not sure). Here’s an example of a command that will run for a long time, so you can practice cancelling it:

```
ping github.com
```

You might be surprised that the keyboard shortut to cancel a program, [ctrl]+c, is the same as what is typically used to copy text into the clipboard! If you are not familiar with the notion of ‘clipboard’, please read about it [here]. Obviously, [ctrl]+c does not work for copying selected text from the terminal. Instead you can (usually) either use [ctrl]+[shift]+c or right-click the terminal window to get a context menu. Similarly, the correct way to paste text into the terminal is usually [ctrl]+[shift]+v (rather than just [ctrl]+v). Incidentally, it took me 20 years to learn that trick, so I thought I would tell you about it early on in your life. (You are very welcome.)

Spend some time practicing selecting text in the terminal with your mouse, copying it, and pasting it into the command prompt. One important thing to realize is that if the text you are pasting contains line breaks (i.e., is multiple lines of text) then the terminal will automatically execute your commands, even without you pressing [enter]! Just something to be careful about.

## Tab completion

One of the crucial features (or shortcuts) of the command prompt is tab completion. Here’s how it works. If you are typing a command, the name of a program, file, or directory, just press the [tab] key and the system will (if possible) complete the word you are typing! If there is more than one option, then just press the tab key a second time and you’ll see a list of possibilties.

For example, got to your home directory (enter `cd`) and then try

```
cd Down[tab]
```
If you have directory called Downloads, then the system will complete your word. This is very important, not only for saving time, but also for avoiding spelling errors, or for just for figuring out what are your options. As mentioned, it works not only for files and directories, but also for programs and commands. Try typing

```
ne[tab][tab]
```
You should see a list of all available commands starting with the letters “ne”. Try exploring with tab completion! It can be really fun!

## Command history (repeating commands)

The other most useful feature to be aware of in the terminal is the [up] and [down] arrows for retrieving previously executed commands. The best way to learn how to use this is to just try the [up] and [down] arrows at the command prompt. Cool, eh? This is particularly useful if you want to run a modified version of a previous command, by finding the command using the [up] arrow and then using [backspace] or [left] and [right] arrows for replacing portions of the command.

## Proficiency tests

* Demonstrate that you can open a terminal window and type in commands
* Define the following: the command prompt, the current working directory.
* Show how to change directories, and to change back to the home directory.
* Demonstrate that you can navigate around the file system, exploring where the different files are.
* Explain how to cancel a command that is taking too long to execute.
* Explain what the clipboard is and how to copy and paste text in the terminal.
* List the most important UNIX commands to be aware of.
* Explain how to use the most important UNIX commands (listed above).
* Explain how tab completion works, and demonstrate that you know how to use it.
* Demonstrate how to retrieve and modify previously executed commands.
