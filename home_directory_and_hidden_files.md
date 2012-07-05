---
title: Home Directory and Hidden Files
layout: default
previous: creating_files
next: file_types
---

Hidden files in Unix are made hidden by starting them with a period.  Most programs
on Unix allow the user to set up their own custom preferences, and these
settings are typically stored in the home directory, but they are hidden to not annoy the
user and clutter the folder visibly.  To view these files we need to use `ls
-a` which will show all files in the directory.  If you do this in your home
directory you can see that their are most likely a lot of hidden files.  You
can edit them if you would like, but most of the time you don't need to edit
them directly (unless you are on a server machine and not a desktop).

Other than not showing up with a normal `ls`, there is nothing at all
different between a normal file and a hidden file.
