---
layout: post
title: "Logging to Notification Center and Growl From Node Applications"
date: 2013-10-20 14:42
comments: true
categories: node javascript
---

I wrote a small [NodeJS][node] library that combines the [growl][growl] and
[terminal-notifier][terminal-notifier] npm packages into a single call that can
be used to quickly add notifications to a node appliction with support for OS X,
Windows and Linux. For systems that do not support the OS X Notification Center
or Growl, the notification will go to `console.log()`.  This is cleverly named
`log-notify`.  Check it out: <https://npmjs.org/package/log-notify>.

_OS X 10.8.x Notification Center_  
![](http://new.tinygrab.com/d34460e816c9911aabc9cebaa92ac8c13910a39faa.png)

_Ubuntu 13.04_  
![](http://new.tinygrab.com/d34460e816c07e0856758e7746df470467713d2696.png)




[dust-compiler]: https://npmjs.org/package/dust-compiler
[growl]: https://npmjs.org/package/growl
[node]: http://nodejs.org/
[terminal-notifier]: https://npmjs.org/package/terminal-notifier
