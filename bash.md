---
title: Bash
layout: default
previous: getting_started
next: terminal
---

If you have terminal open, you are now looking at a black screen with a
blinking cursor, and the program that just loaded (most likely) is Bash.  Bash is
a program that opens in a terminal, and is the default on most Linux
distributions.  It should look something like this:

    dave@[dataDyne]~$

If you click the terminal and press enter a bunch of times you'll notice the
line that you see repeats itself: this recurring text is called the prompt (it
_prompts_ the user for input).  In my example you see the name `dave`,
which is my username on the system.  You also see `dataDyne`, this is my
computers hostname, or the name of the specific machine I'm logged into.  You
then see `~`, which is a shortcut path that leads to my users home directory.
Lastly you see '$': that sign means that my user is a typical user, and not
root.  Root is the administrator account of the computer that has full
privileges to everything on the system.  Root will have `#` instead of `$`.

Bash is simply a program that accepts input, processes it, and supplies output.
This type of program is referred to as a shell; the `sh` in bash actually
stands for shell.  This tutorial will show you how to navigate, understand,
modify, and control your computer using bash as a shell.
