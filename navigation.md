---
title: Navigation
layout: default
previous: the_filesystem
next: creating_files
---

Now that you know how the filesystem is laid out, you might be asking "that's
great, but what can I do from terminal?".  We are going to learn some useful
commands to navigate the filesystem.  The commands are:

* `pwd` -- display the present working directory
* `cd`  -- change directory
* `ls`  -- list the files in the directory

It's important to remember that at all times in the bash shell, you are inside
a directory. You are always inside a directory in bash.  The `pwd` command is
used to show which directory you are currently in.  Assuming you are using
bash, this should be your home directory.

Let's see what's in your home directory. Try typing `ls` and pressing enter.
This will list all of the files and folders in the current directory.

    dave@[datadyne]:~/$ ls
    bin/   how to raid/  opt         rotate.sh  scripts/  update.sh        wireless/
    code/  mpd.conf      pythonweb/  sabres/    temp/     viridianplayer/  www

My home folder has a lot of files in it, this is because anything I'm working
on gets stored in my home directory.  As you can see in my example the folders
have a / at the right of them, and the files don't.  If this doesn't show up
for you try typing `ls -p` without the single quotes, and it should.  I'll talk
more about this later, but you gave the program `ls` the `p` switch, or the `p`
option, which tells it to change the way it acts.  Most programs have
options, and the letters for each program for their options can vary.

Let's move up on level.  To do this we need to take advantage of the fact that
there are 2 special directories that exists inside every directory.  These 2
special directories are `..` and `.`.  These are special because they are
relative.  `.` represents the current directory that you are in, and `..`
represents the parent folder of your current folder.  If you wanted to
reference a file called `words.txt` in the current directory, you could call it
`words.txt` or `./words.txt`, the computer will see them as the same thing.
But we want to go up a level, so we will type `cd ..`.  This will change our
directory to `..`, which moves us up one level.  We started in /home/dave, and
after the command we will be in /home.

    dave@[datadyne]:~/$ cd ..
    dave@[datadyne]:/home/$ pwd
    /home

Now that we are in /home we can run ls to see what folders exist in here.

    dave@[datadyne]:/home/$ ls
    dave/

You can see that inside /home, only a folder called dave exists (the folder we
were just in!)

Now that you have some navigation commands down, let's move on to creating files.
