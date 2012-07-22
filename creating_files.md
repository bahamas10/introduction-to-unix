---
title: Creating Files
layout: default
previous: navigation
next: home_dir_and_hidden_files
---


To create files and folders on a unix system you will need the following commands:

* `mkdir` -- Create a directory
* `touch` -- Create a file (indirectly)
* `rm` -- Remove a file
* `mv` -- Move a folder (and rename)

Let's go back to your home directory, so type `cd ~`.

Now let's make a folder called unix, to do this run this command

    dave@[datadyne]:~/$ mkdir unix

Now let's go into the folder and make 2 files called file1 and file2 (original i know.)

    dave@[datadyne]:~/$ cd unix
    dave@[datadyne]:~/unix/$ touch file1
    dave@[datadyne]:~/unix/$ touch file2
    dave@[datadyne]:~/unix/$ ls
    file1        file2

Assuming everything went as planned you should see 2 files in the output of `ls`.
Touch also allows multiple file names on the same lines. When something comes
as a parameter to a command (file1 is the parameter we sent to touch) it is
called the programs arguments.  We could have done this instead.

    dave@[datadyne]:~/$ touch file1 file2

That would have had the same effect. Now we can rename file2 to file3, to do
this we can use `mv`.  And then, just for fun, let's delete those files.

    dave@[datadyne]:~/$ mv file2 file3
    dave@[datadyne]:~/$ rm file1 file3

We don't rm file2 because it has been moved to file3.  Now let's move back to
the home directory and remove the directory unix.

    dave@[datadyne]:~/$ rmdir unix

`rmdir` I threw in as a bonus command, it only works if the directory you are
trying to remove is empty, otherwise you would have to use `rm -r unix`.  BE
VERY CAREFUL WITH `rm`, you can remove a lot of files with it in one command, and
there is no undo or Recycling Bin.
