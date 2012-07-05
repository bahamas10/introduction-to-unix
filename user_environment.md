---
title: User Environment
layout: default
previous: file_permissions
next: environmental_variables
---

The environment is created when the user loads bash.  When bash is loaded it
loads a list of all of the commands you can run, and variables that are set for
the user to see.

To see some of the variables that are set we first need to learn how to print
stuff to the screen, to do this we need `echo`.  Use it like this:

    dave@[datadyne]:~/$ echo Hello World
    Hello World
