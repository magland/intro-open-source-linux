# UNIX commands

In this lesson you will learn how to use the most common programs or commands in the terminal (aka at the command prompt). It is worth taking the time to practice these basic techniques so that you become comfortable with probing and manipulating your Linux system.

In a previous lesson, we already talked about two crucial commands: `cd` and `ls`. If you are not familiar with those, or don’t feel comfortable inside the terminal, go back and study.

## Displaying file content

The next commands to learn are: `echo`, `cat`, `more`, and `tail`.

The `echo` command just repeats back the string (or text) that you give it. For example, try,

```
echo “I said a-boom-chick-a-boom”
```

There are many ways this can be useful. For example, enter the following to create a new file with some text in it.

```
echo “This is the content of the first text file I ever made in the terminal!” > first_file.txt
```

Rather than repeating the string, the output of `echo` gets redirected to that new file. Use the `ls` command to verify that the new file got created. Now we can use `cat` to verify that the contents of the new file are as expected:

```
cat first_file.txt
```

You should see the text that we `echo`d into the file. That’s what the `cat` command does… it echoes back the contents of a file. Is this fun?? Let’s put some more text in:

```
echo “This is some more text” >> first_file.txt
```

Notice that we used a double-redirect `>>` which causes the file to be appended rather than rewritten (that means the new text was added on to the end of the file). Check out the new file content using the `cat` command again.

If the file gets too big, then we won’t want to use `cat` because it will give us TMI. For example, try

```
cat [file in large file here]
```

That file is so big that you might need to press [ctrl]+c to cancel the program. In such cases you will instead want to use one of the commands `more` or `tail`

```
more [filename]
tail [filename] 
```

The first command (`more`) allows you to see the first part of the file and then press keys to scroll through the file. The second command (`tail`) is convenient if you need to see just the end of the file.

## Getting help for UNIX commands

Most UNIX commands have many, many options, or different ways to run them. For example, we saw the “-l” flag for the `ls` command changes the behavior. Another example is
```
[give another example]
```

There are several methods for getting help for UNIX commands, to see which options are available and how to use them. The old-fashioned way is to use the `man` command (stands for manual). For example,

```
man echo 
```

However, you can usually get a more practical summary using the `--help` option:

```
echo --help
```

## Proficiency tests

Demonstrate your proficiency in the following commands:
`cd`, `ls`
`echo`, `cat`, `more`, `tail`
`cp`, `mv`, `rm`

## Other important terminal commands

In addition to `ls` and `cd`, here are some other important commands (also known as UNIX commands) you should be aware of. Try out the examples and 

[Talk about file paths somewhere]

## Running scripts and programs from the command line

You are probably used to starting programs (on your computer or mobile device) by clicking on icons. (Sometimes those icons might even start bouncing up and down while the program is starting up.) As a software developer, it is important that you learn how to run programs from the command line.

Explain why it is important to know how to launch programs from the command line rather than just clicking on icons.
