# jamsyoung.com
An Octopress Blog


## Quick usage summary:
- Generate updated source

        $ rake generate

- Watch sources for changes and regenerate

        $ rake watch

- Preview changes at [http://localhost:4000][0]

        $ rake preview

- Deploy

        $ rake deploy

- Make a new post

        $ rake new_post["title"]

- Make a new page

        $ rake new_page["page-name"]
        $ rake new_page["page-name/custom.html"]



* * *



## What is Octopress?
Octopress is [Jekyll][1] blogging at its finest.

1. **Octopress sports a clean responsive theme** written in semantic HTML5,
   focused on readability and friendliness toward mobile devices.

2. **Code blogging is easy and beautiful.** Embed code (with [Solarized][2]
   styling) in your posts from gists, jsFiddle or from your filesystem.

3. **Third party integration is simple** with built-in support for Pinboard,
   Delicious, GitHub Repositories, Disqus Comments and Google Analytics.

4. **It's easy to use.** A collection of rake tasks simplifies development and
   makes deploying a cinch.

5. **Ships with great plug-ins** some original and others from the Jekyll
   community &mdash; tested and improved.


## Documentation

Check out [Octopress.org][3] for guides and documentation.


## Contributing

[![Build Status](https://travis-ci.org/imathis/octopress.png?branch=master)][4]

We love to see people contributing to Octopress, whether it's a bug report,
feature suggestion or a pull request. At the moment, we try to keep the core
slick and lean, focusing on basic blogging needs, so some of your suggestions
might not find their way into Octopress. For those ideas, we started a
[list of 3rd party plug-ins][5], where you can link your own Octopress plug-in
repositories. For the future, we're thinking about ways to easier add them them
into our main releases.


## License
(The MIT License)

Copyright © 2009-2013 Brandon Mathis

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the ‘Software’), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


#### If you want to be awesome.
- Proudly display the 'Powered by Octopress' credit in the footer.

- Add your site to the Wiki so we can watch the community grow.



[0]: http://localhost:4000
[1]: https://github.com/mojombo/jekyll
[2]: http://ethanschoonover.com/solarized
[3]: http://octopress.org/docs
[4]: https://travis-ci.org/imathis/octopress
[5]: https://github.com/imathis/octopress/wiki/3rd-party-plugins
