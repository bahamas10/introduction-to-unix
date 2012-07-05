---
title: Avoiding Common Mistakes
layout: default
previous: loops
---

This section is in here for 2 reasons.  It will save you a LOT of trouble,
and it's my biggest bash related pet peeve.

When people are learning bash they often want to iterate over a list of files
in a directory, so they take this approach:

{% highlight bash %}
#!/bin/bash
for file in $(ls); do
    echo "$file"
done
{% endhighlight %}

The problem is that this will fail if a file has a space in its name or a
newline character (this is possible!).  The correct way to do this is to used a
bash extension called a glob.  A glob is like a wildcard

{% highlight bash %}
for file in *; do
    echo "$file"
done
{% endhighlight %}

This approach will properly delimit file names.

More information about that can be found here
[http://mywiki.wooledge.org/ParsingLs](http://mywiki.wooledge.org/ParsingLs)
