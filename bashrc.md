---
title: bashrc
layout: default
previous: environmental_variables
next: advanced_bash
---

The `.bashrc` file is a hidden file that is in your home folder by default, and
is executed every time bash is loaded.  This allows you to set your own
environmental variables for your bash session.  For
example, this might be inside a .bashrc file.

{% highlight bash %}
VAR1=5
VAR2="Hello"
{% endhighlight %}

Now every time you load bash, `$VAR1` will hold 5 and `$VAR2` will hold "Hello"
(without quotes).  This can be useful for a variety of reasons.

Something more useful would be to set aliases in the `.bashrc` for commonly used
commands.  If you recall from earlier, the output of my ls command had '/' at
the end of directories, I used an alias for that.

{% highlight bash %}
alias ls='ls -p'
{% endhighlight %}

This sets the command `ls` to actually execute `ls -p` when called. The slashes will be seen
at the end of directories in the listing.
