---
layout: post
title: "Command Line Reporting"
date: 2007-04-29 21:49
comments: true
categories:
---

I find myself dealing with lots of log files that need to be parsed on the fly.
Here are some of the harder-to-remember-yet-very-useful ones that I find myself
copy/pasting all the time.

{% codeblock Various Bash commands lang:bash %}
$ listysftclog 200709* | grep att/v4 | perl -ne 'if(/(yihupg[^|]*)/){print $1."n";}' | sort -r | uniq -c

$ cat ~/ysftc.log | grep att/v4 | perl -ne 'if(/beacon.choice~([^|]*)/){print $1."n";}' | sed 's/&/&/' | sort | uniq -c | sort -nr

$ cat ~/ysftc.log | grep att/v4 | grep choice.php | grep result~200 | wc -l

$ cat ~/ysftc.log | grep att/v4 | grep result~200 | cut -f10 -d| | sort | uniq | wc -l

$ cat /home/y/logs/ysftc/ysftc.log | grep att/v4 | perl -ne 'if(/choiceua([^|]*)/){print $1."n";}' | sort | uniq -c | sort -nr

$ cat /home/y/logs/ysftc/ysftc.log | grep att/v4 | perl -ne 'if(/choiceua([^|]*)/){print $1."n";}' | grep Windows | wc -l

$ cat /home/y/logs/ysftc/ysftc.log | grep att/v4 | perl -ne 'if(/choiceua([^|]*)/){print $1."n";}' | grep Mac | wc -l


$ cat ~/ysftc.log | grep att/v4 | perl -ne 'if(/beacon.choice~([^|]*)/){print $1."n";}' | sed 's/&/&/' | sort | uniq -c | sort -nr
 23 AT&T Yahoo! Online Protection
 13 Parental Controls
 11 AT&T Yahoo! Messenger
 11 AT&T Yahoo! Browser
 11 AT&T Toolbar
  6 Connection Manager
  2 AT&T Pop-Up Blocker
  1 AT&T Security Suite SM
{% endcodeblock %}
