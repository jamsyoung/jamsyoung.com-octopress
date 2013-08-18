---
layout: post
title: "Need A Wordpress Development Environment?"
date: 2013-08-05 23:19
comments: true
categories: wordpress vagrant virtualbox LEMP
---

If you are like me, you get tired of having to reconfigure your development
machine everytime you switch projects.  PHP is neat and all, but I hardly
ever mess with it anymore, so when I came across the need to run a Wordpress
instance on my local dev machine, I didn't have anything installed anymore.
No PHP or MySQL, and I really didn't feel like taking the risk of totally
breaking what I do have running.

[Vagrant][0] and [Virtualbox][1] to the rescue!  With these working together it
is pretty simple to get an Ubuntu VM running whatever is needed while still
allowing me to write the code in [Sublime][2] on my MBP.  I threw it up on
Github so everyone can quickly spin up a Wordpress development environment.

<https://github.com/jamsyoung/vagrant-lemp>

**8/28/2013**
Update! This has been made more generic to just be a Vagrant LEMP environment.
You can still do Wordpress development on it, but the repository is not
specific to only Wordpress anymore.


[0]: http://www.vagrantup.com
[1]: https://www.virtualbox.org
[2]: http://www.sublimetext.com/2
