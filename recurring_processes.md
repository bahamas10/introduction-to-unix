---
title: Recurring Processes
layout: default
previous: init
next: more_advanced_bash
---

Cron is used for processes that need to be repeated.  Say you wanted to execute
our script that says hello at 3 minutes passed the hour, every hour, this is
where cron helps us.  To view your 'cron table' run the command `crontab`.  This
will present you with a blank document most likely, it is up to you to fill in
the cron table.  To make this script execute 3 minutes passed the hour enter
this in.

    3 * * * * "$HOME/script.sh" >> "$HOME/file.txt"
