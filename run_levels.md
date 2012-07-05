---
title: Run Levels
layout: default
previous: processes
next: init
---

When the computer first turns on, it enters different run levels when the
computer runs a Unix system.

The run levels on a standard Linux System are:

0: Shutdown

1: Single User

2: Multi User no Networking

3: Multi User with Networking (typical for servers)

4: User Define

5: Multi User with Networking and GUI

6: Reboot

A computer starts at run level 0 when it is off.  When the user turns it on it
will go from 1-5 for a desktop computer, or 1-3 on a server.  When the user
tells the computer to reboot it goes into run level 6.

You can use the `init` command (as root) to change the run level, though this is
seldom necessary.
