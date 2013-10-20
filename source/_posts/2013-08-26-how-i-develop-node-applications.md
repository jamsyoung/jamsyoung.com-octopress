---
layout: post
title: "How I Develop Node Applications"
date: 2013-08-26 20:55
comments: true
categories: node javascript
---

**Part 1**

There is no right way or wrong way to develop a node application.  Well, there 
is a wrong way, but you won't do it wrong for long, hopefully.  Being a software
developer, you have chosen this life because you are constantly striving for the
best, most efficient way to develop.  If you are doing it a wrong way, it is
just because you haven't rewritten it again, and again, and again. That's what
we all do, we refactor over and over until we run out of time.

This is what I am currently doing.  I didn't do this in the past, and I will 
change it in the future.

<!-- more -->

## The Development Environment
Mac OS X.  Yes, I use Linux and Windows as well, but when walking into a room 
with every computer imaginable, I am going to grab the newest MBP and get to
work.

Ok, I have my MBP, now for all the software.  Install Xcode, just so I can get
Command Line Tools.  This is going to give you all the command line goodness,
specifically git, make, gcc, blah, blah, blah.  Its all there, and you
are going to use it either directly or indirectly at some point.

Next [Sublime Text 2][0] with a small handful of packages.  Yeah, I will list
those sometime later.  Between vim and subl, you will probably never edit a file
with anything else.  Maybe that is just me though.


## Dotfiles
I have lots of them, you can get them all from [mydotfiles][1].

Those aren't the only dotfiles to use though. There are individual project
dotfiles you will want to add to each project you work on.  This is what I am
currently putting in my node projects.

- [.editorconfig][2] - This will insure that you have consistent settings for
  all files.  This is particularly useful for projects that have more than just
  you working on it.

- [.jshintrc][3] - If its a JavaScript file, use [JSHint][4] on it.  It doesn't
  really matter what settings you use, just as long as they are settings that
  you can justify and live with.

- [.travis.yml][5] - Free CI in the cloud.  Sweet.

- .gitignore - Standard part of GIT. Source control is good.  I have used just
  about everything in the past.  GIT is all I use now.

- .npmignore - You don't need everything in your published npm packages.


## Unit Tests
[Mocha][6] and [Chai][7] FTW!  Throw in [Grunt][8] with some [blanket][9] code
coverage and you are set.  I should write a whole series of articles on how to
use TDD and BDD.


## Functional Tests
I'll admit, I haven't settled on my favorite yet.  I am all over the place here.
Java based [Selenium][10], [Casper][11] on [Phantom][12], [Arrow][13] on 
Selenium or Phantom, [Zombie][14], others!  I just don't know yet.  I have done
work in all of the above and they all fit the bill.

(Ok, I haven't used Zombie yet, but I plan too!)

Stay tuned for Part 2 where I dive into more details.




[0]: http://www.sublimetext.com/2
[1]: https://github.com/jamsyoung/mydotfiles
[2]: http://editorconfig.org
[3]: https://gist.github.com/jamsyoung/6343880
[4]: http://jshint.com/docs
[5]: https://travis-ci.org
[6]: http://visionmedia.github.io/mocha/
[7]: http://chaijs.com
[8]: http://gruntjs.com
[9]: http://blanketjs.org
[10]: http://docs.seleniumhq.org
[11]: http://casperjs.org
[12]: http://phantomjs.org
[13]: https://github.com/yahoo/arrow
[14]: http://zombie.labnotes.org
