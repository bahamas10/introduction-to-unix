---
title: init
layout: default
previous: run_levels
next: recurring_processes
---

Init is the owner of all processes (pid 1), if it dies, then the computer will
shutdown.

Init starts when your computer starts, and doesn't go down until the computer
does.  Mac will have launchd instead of init, but the idea is still the
same.
