---
title: I/O Redirection
layout: default
previous: scripts
next: pipes
---

I/O Redirection is a cool thing with bash, you can choose where you want the
output of a command or script to go.  For example try this:

    dave@[datadyne]:~/$ echo "hello" > file.txt
    dave@[datadyne]:~/$ cat file.txt
    hello

Recall that `cat` prints the contents of a file.  We can also do that with a
script, try this:

    dave@[datadyne]:~/$ bash script.sh &gt; file.txt
    dave@[datadyne]:~/$ cat file.txt
    Hello Dave, you are 21 years old!

As you can see the scripts output was written to file.txt, but the last thing
written to it is gone! That's because the > operator will wipe out anything
in the file when you use it. If you want to concatenate it with the file, use
the >> operator.

    dave@[datadyne]:~/$ bash script.sh > file.txt
    dave@[datadyne]:~/$ cat file.txt
    Hello Dave, you are 21 years old!
    dave@[datadyne]:~/$ bash script.sh >> file.txt
    dave@[datadyne]:~/$ cat file.txt
    Hello Dave, you are 21 years old!
    Hello Dave, you are 21 years old!

This was printed twice because it was appended to the file.
