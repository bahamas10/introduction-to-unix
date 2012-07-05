---
title: File Permissions
layout: default
previous: different_users
next: user_environment
---

For each file and directory in Unix there are specific permissions and an owner
set.  Every file has to be owned by somebody, so whoever creates a file or
creates a folder owns that file or folder.  To start off we are going to add
another switch to `ls` to allow us to see the owner of the file, and the
permissions.

* `ls -l` -- This tells ls to give a _l_ong listing, displaying information about each file

Running this in my home directory yields.

    dave@[datadyne]:~/$ ls -l
    total 64
    drwxr-xr-x 2 dave dave  4096 2010-10-04 09:33 bin/
    drwxr-xr-x 3 dave dave  4096 2009-10-27 13:15 code/
    drwxr-xr-x 2 dave dave  4096 2009-10-27 13:07 how to raid/
    -rw-r----- 1 dave dave 12433 2010-07-28 23:57 mpd.conf
    lrwxrwxrwx 1 dave dave     5 2010-07-31 11:38 opt -> /opt//
    drwxr-xr-x 2 dave dave  4096 2010-08-25 16:43 pythonweb/
    -rwx------ 1 dave dave   501 2010-05-19 16:29 rotate.sh
    drwxr-xr-x 2 dave dave  4096 2010-10-04 09:38 sabres/
    drwxr-xr-x 8 dave dave  4096 2010-07-23 09:20 scripts/
    drwxr-xr-x 2 dave dave  4096 2010-06-09 17:44 temp/
    drwxr-xr-x 2 dave dave  4096 2010-10-06 17:42 unix/
    -rwxr-xr-x 1 dave dave  2464 2010-07-13 15:25 update.sh
    drwxr-xr-x 6 dave dave  4096 2010-09-23 21:51 viridianplayer/
    drwxr-xr-x 4 dave dave  4096 2010-08-04 20:03 wireless/
    lrwxrwxrwx 1 dave dave     9 2010-07-31 11:38 www -> /var/www//

This is a lot of information to look at, but if we look at it column by column
it's not bad.  The first line just tells us how many files/folders are in the
directory (it counts hidden files too).  The next lines after that show us each
file and information about them.  The first part shows the permissions on the
files.  The second and third part show the username who owns it, and the group
to which it's in.  The next column is the file size.  The next 2 columns show
the modified time of the file, and the last line shows the filename.

You can set permissions on the file for the files owner, people in the group
that the file is in, and everybody.  A standard default permission is 755 which
means the owner has read write and execute, and everybody else can only read
and execute.
