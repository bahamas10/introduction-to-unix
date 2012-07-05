---
title: The Filesystem
layout: default
previous: terminal
next: navigation
---

The Filesystem on Unix machines is very straight-forward.  There is a root
folder simply called '/', and any file or folder that exists on the machine
exists within the root folder (often call 'slash' or 'the root directory').
Inside the root directory you will find typical folders that will exists on most
Unix-based machines.

* /bin -- This folder contains normal executable (binary) files that are needed
  on the system to perform basic tasks, like navigation and file
  creation/deletion.
* /usr -- This folder contains files that are not necessary, but are helpful
  for the user.  There is a /usr/bin folder that has executable files that
  aren't necessary for the system to operate, but are very handy for the user
* /sbin -- This folder contains executable files that are to be used by the
  _s_uper user.  Commands in here typically do administrative things like
  control network interfaces, etc.
* /etc -- This folder typically contains configuration files for programs that
  are installed on the computer.
* /var -- This contains _var_ious files used by the operating system.  For
  example, /var/log contains all of the logs that the system generates.
* /dev -- This contains _dev_ices that the system uses.  This confuses
  most people at first, but the computer talks to your devices as if they are
  files (for the most part).  /dev/usb0 is the typical name of a usb stick when
  you plug it into your computer.
* /home -- This is where a users home directory goes.  If you come from windows
  this is comparable to C:\Documents and Settings\ or C:\Users
* /tmp -- This is a folder for temporary files that can be used by all users on
  the computer
* /mnt -- This is where mounted devices should go.  If you plug in a usb stick,
  the computer has to mount it before it can write to it, so you can mount it
  to /mnt/usbstick for example (this is different than /dev/usb0).
* /lib -- Shared libraries the comptuer uses.  This is for programs installed
  on the system that need to share resources (such as functions).
* /proc -- This is a filesystem that the computer uses to communicate with
  various aspects of itself... this is a tricky subject so i'll just leave this
  [link here][proc] if you are interested in learning more.

Note: /proc is very different across different Unix-based operating systems.

You don't need to memorize this! Use this page as a reference... But if you
start using Unix or Linux you'll find that you do memorize this without
much effort.

The part of the file system that we will be dealing with for the most part is
the users home directory, which is typically located at /home/$USER.  In the
prompt if you recall there was a '~' character that symbolized my home
directory.  From the prompt you can run this command and it will tell you the
path of your home directory

    dave@[datadyne]:~/$ pwd
    /home/dave

Bash recognizes ~ as a shortcut to the current users home directory, which for
me is /home/dave.

That's all for the filesystem for right now, so let's move on to navigating
the filesystem.

[proc]: http://en.wikipedia.org/wiki/Procfs
