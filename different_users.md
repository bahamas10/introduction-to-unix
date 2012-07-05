---
title: Different Users
layout: default
previous: file_types
next: file_permissions
---

On the Unix machine there can be multiple users, and because of the way that
Unix is designed multiple users can be logged in at the same time.  To see
this we will use the following commands.

* `users` -- to see who's on the machine
* `w` -- to see who's on the machine and what they are doing
* `cat` -- we will use this to view a file

First we can run `users`, and this will show how many users are logged on. If a
persons name shows up more than once it means they have more than one session
open.

    dave@[datadyne]:~/$ users
    dave dave dave dave

As you can see I have 4 terminals open on this machine. Once you learn how to
use a command line interface (which is what terminal is) it's hard to want to
use anything else because of the level of increased productivity it allows.

    dave@[datadyne]:~/$ w
    18:08:22 up 14 days, 13:42,  4 users,  load average: 0.01, 0.03, 0.00
    USER     TTY      FROM              LOGIN@   IDLE   JCPU   PCPU WHAT
    dave     pts/0    129.21.81.15     17:22   13:22   0.24s  0.24s -bash
    dave     pts/1    129.21.25.56:S.0 22Sep10  2days  2:18   2:18  weechat-curses
    dave     pts/2    129.21.25.56:S.1 22Sep10  2days  6.33s  6.07s python
    dave     pts/3    129.21.25.56:S.2 23Sep10  0.00s  1.74s  0.01s w

This shows a lot more, this shows what program is running on all of the
terminals.  As you can see this particular machine has 4 users on (all me), and
has been up for about 14 days.  On the 4 terminals, I'm running bash in one,
weechat-curses in another, python in another, and one ran 'w' to get the output
that you are seeing.  The programs I'm running are not important, what is
important is that anyone on the machine can see what programs you are using
with the `w` command.

Finally we are going to use `cat` to view the contents of the file.  To use `cat`
is simple, we will it like this.

    dave@[datadyne]:~/$ cat /etc/passwd

`cat` will dump the contents of a file right on the terminal, so in this case it
will dump the contents of `/etc/passwd`.  This file in particular shows all of
the users (along with more information) that exists on the computer.

For security purposes I will not show the output of this command, but hopefully
this will teach you how to use the command.
