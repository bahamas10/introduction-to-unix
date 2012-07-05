---
title: Process
layout: default
previous: the_unix_system
next: run_levels
---

Every program that runs in Unix is a process, and because of that has its own
process id, which is a way for the system to uniquely reference it.

To view the processes running on the system we need the `ps` command, and we are
going to give it some switches to allow us to see all of the processes that are
running.  I have shortened the output to be able to show it on this site.

    dave@[daveeddy]:/var/www/dev/$ ps aux
    USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
    root         1  0.0  0.0  23680  1744 ?        Ss   Sep29   0:00 /sbin/init
    root         2  0.0  0.0      0     0 ?        S    Sep29   0:00 [kthreadd]
    root         3  0.0  0.0      0     0 ?        S    Sep29   0:00 [migration/0]
    root         4  0.0  0.0      0     0 ?        S    Sep29   0:00 [ksoftirqd/0]
    root         5  0.0  0.0      0     0 ?        S    Sep29   0:00 [watchdog/0]
    root         6  0.0  0.0      0     0 ?        S    Sep29   0:00 [migration/1]
    root         7  0.0  0.0      0     0 ?        S    Sep29   0:00 [ksoftirqd/1]
    root         8  0.0  0.0      0     0 ?        S    Sep29   0:00 [watchdog/1]
    root         9  0.0  0.0      0     0 ?        S    Sep29   0:00 [migration/2]
    root        10  0.0  0.0      0     0 ?        S    Sep29   0:00 [ksoftirqd/2]
    root        11  0.0  0.0      0     0 ?        S    Sep29   0:00 [watchdog/2]
    root        12  0.0  0.0      0     0 ?        S    Sep29   0:00 [migration/3]
    root        13  0.0  0.0      0     0 ?        S    Sep29   0:00 [ksoftirqd/3]
    root        14  0.0  0.0      0     0 ?        S    Sep29   0:00 [watchdog/3]

The owner of the process is on the far left, the id is next to it, and the
process itself is on the right side.

The owner of all processes is init, and it has a process id (pid) of 1, which
it will always have, and we will talk about it in a later section.
