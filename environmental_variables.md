---
title: Environmental Variables
layout: default
previous: user_environment
next: bashrc
---

`echo` is pretty self explanatory.  If you want to print a variable you need to
start the variable name with a $.  Some built in variables are $USER, $HOME,
and $PWD.  Uppercase variable names are reserved for constant variables, and
variables set for you automatically are called environmental variables.

    dave@[datadyne]:~/$ echo "Hello $USER, your home directory is $HOME, and the current directory is $PWD, the PWD variable is identical to the out of the pwd command"
    Hello dave, your home directory is /home/dave, and the current directory is /home/dave, the PWD variable is identical to the out of the pwd command

In that example we can see three environmental variables being printed.
