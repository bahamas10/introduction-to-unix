---
title: Intro
layout: default
next: getting_started
---

Welcome to _An Introduction to Unix_! This website aims to give people, with
little or no knowledge of Unix, a good foundation in the fundamentals of Unix.

This guide starts with the basics to give a good overall view, and then gets
more precise by seeing how to work directly with a Unix machine.  Commands will
be taught throughout this guide that will deal directly with the current
section, and examples of all commands will be shown.

To start off, whenever you see something in a black text-box-looking block,
this signifies code, or a command.  If it is a command it will typically be
shown like this:

    $ command

In that example, `command` is a command that could be run directly on the Unix
machine (if this is confusing don't worry, it will become clear in the first 2
sections).

Code, on the other hand, will always start with a 'shebang', or 'hashbang',
which looks like a # sign (hash) followed by an exclamation mark ! (bang).
Code will look like this:

{% highlight bash %}
#!/bin/bash
a=4
b=6
echo $((a+b))
{% endhighlight %}

The 'shebang' in that example is '#!/bin/bash', and that lets you know that
what you are seeing is code, and coincidentally tells the computer that this
file, if it is executed, should be executed using /bin/bash.

That's it for the intro to this guide, to get started click the link below this
line to the right that says 'Getting Started', or click the corresponding like
on the side menu.
