---
title: Pipes
layout: default
previous: io_redirection
next: the_unix_system
---

Pipes are really cool, you can output one command into the input of another
using `|`.

To learn pipes we will learn a new command, `grep`.  `grep` is used to search
for certain strings. Example:

    dave@[datadyne]:~/$ ls
    bin/      how to raid/  pythonweb/  scripts/   unix/            wireless/
    code/     mpd.conf      rotate.sh   script.sh  update.sh        www
    file.txt  opt           sabres/     temp/      viridianplayer/
    dave@[datadyne]:~/$ ls | grep script
    scripts/
    script.sh

I first ran ls by itself, and then in the second command I piped ls to grep and
searched for "script".  As you can see there were 2 matches, the directory and
the file because they both contain the word "script" in them.
