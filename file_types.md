---
title: File Types
layout: default
previous: home_directory_and_hidden_files
next: different_users
---

The file extensions in Unix are treated differently than in Windows.  Windows
uses the extension (ie: .exe) to know what kind of file it is, but Unix can
look into the file to figure out what kind of file it's dealing with.
Extensions are still used in Unix and are great for the user to see, but they
are not necessary.

In the first page I showed a basic script with a 'shebang' that said
`#!/bin/bash`.  The computer would look at that shebang to determine what kind of
file it is.  To verify this you can use the 'file' command.

    dave@[datadyne]:~/$ file update.sh
    update.sh: Bourne-Again shell script text executable

Bourne-Again SHell... BASH.  It's a bash script, the file command did not look
at the .sh part of the name, only the shebang in the file.
