# CLI 101 - Introduction to command-line interfaces with Bash

## Introduction

This course introduces you to command-line interfaces and Bash. In this course you will learn how to complete basic operations with a terminal.

## Setup

You will need access to a Bash terminal. On MacOS, be sure to install iTerm2. On Linux, look for a program called `terminal` or something similar.

Once you have an open terminal, it's almost time to start entering your first commands. But first, just a tiny bit of background.

First of all, what is this terminal and what is Bash?

### The terminal and Bash
You might have heard all kinds of names for 'the terminal'. For example: `console`, `command-line`, `cli`, `command-line interface` or `terminal`. When people use any of these names, they ususaly refer to working with a terminal program, like you just started.

What people mean when they say they are working through a terminal is that they are typing commands into their terminal program. Most terminals by default accept so called 'Bash commands'; Bash is basically a programming language which you can use to instruct a computer (as with any programming language).

The most basic Bash/terminal operations consist of just one single command. An example would be the `pwd` command.

>Go ahead, enter `pwd` into your terminal and press enter, see what happens.

What's important to realise is that whenever you enter 'commands', you are basically telling your computer to run a program.

Let's take the `pwd` example from before. 
Whenever you type `pwd` into your terminal and press enter, what you are really doing is telling the computer: run the program `pwd` now. 
The `pwd` program then starts, does it's thing (in the case of `pwd` it show's the path of the directory you are in) and then the program ends. 
Afterwards you can enter a new 'command', or better; like you just learned: enter a new program for the computer to run. 

Obviously it is possible to run more than one program at once, not just that, some programs require you type more than just their name to execute them. This first course focusses on showing you your first command-line programs to look and move around a file system and perform some operations on (eg: do stuff to) files.

## Programs
You already used `pwd`; notice what the directory path looks like. If you used a computer or a web browser before, you probably already know how paths work. When navigating your computer with Bash, paths work very much like they would in a web browser or in a graphical file browser. 

Now look up the following programs and what they do:

```
pwd
ls
cd
cat
touch
mv
cp
rm
mkdir
rmdir
man
```

### Quiz

1: How do you show hidden files with `ls`?

2: With which of the programs can you rename a file?

## . and ..
While you where using `ls -a` you might have noticed that every directory contains `.` and `..`.

Find out what they do.

## ~, / and the tab button
### ~
Whenever you open up a terminal, you usualy start in your `home` directory. You can use the `~` (tilde) as a shortcut to your home directory.

To instantly jump to your home directory from anywhere run:
```
cd ~
```
To have a look at the file `somefile.txt` in your home directory:
```
cat ~/somefile.txt
```

### /
Much like `~` is a shortcut to your home directory, `/` can be seen as a 'shortcut' to the `root` directory: the starting point of your filesystem, or `/`.

### The tab button
While you are entering commands into a command-line you can use the `tab` button to autocomplete your entries.

Start typing your command and press `tab`, bash will try to complete your entry as best as it can. This is best illustrated with a simple example.

#### Example

You are in the directory `/somedir/`

In this directory are 3 files: `text_a.txt`, `text_b.txt`, and `somefile.py`.

You want to use `cat` on thee files.

You start typing:
```
cat t
```
Press `tab`
You will see:
```
cat text_
```
That's because bash does not know wheter you mean `text_a.txt` or `text_b.txt`, but both start with `text_`, and you entered `cat t` before you pressed `tab`, so these 2 where the only files that matched.

Press `tab` a second time to see all possible options.

Fill in an `a` and press `tab` again and bash will fully autocomplete your command.
```
cat text_a.txt
```

Typing `cat s` and pressing `tab` will instantly autocomplete to:
```
cat somefile.py
```
Because that is the only file that starts with an `s`.

### Test

Using the programs mentioned in this course, recreate the example from above. 

Create a new directory called `somedir` and inside of this new directory, create the 3 files mentioned in the example.

Remember, you can look up where you are and you can look up what's inside of the directory you are in.

If you make a mistake (for example, a typo), you can use a program to remove, rename or move a file

Now follow along with the example.

Remember, if `cat` does not show any output, it is because you (probably) left the files empty.

```
   Copyright 2018 Opensource Academy

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```
