---
layout: post
title: "Tools I use: VIM"
category: english
tags: vim tools
---

<p class="original_post codegenome">
This was originally posted here: <a href="http://www.codegenome.com/en/blog/posts/tools-we-use-vim" target="_blank">Code Genome's blog</a>. This is a redacted version, more personal.
</p>

![2ret-vim image](http://benjamin.thouret.com/images/my_copyright/2ret-vim.png)

A big part of creating Web Applications is to write code. I spend a lot of time in text editor and therefore it has to be an extension of myself. We each have our own preference at Code Genome. Some like to use [textmate](http://macromates.com/), while others prefer [emacs](http://www.gnu.org/software/emacs/) or a full IDE like [RubyMine](http://www.jetbrains.com/ruby/).

I personally prefer using [VIM](http://www.vim.org/), as it allows me to:

- consistently use the same development and system administration environment, whether it be on a Mac OS or Unix system;
- minimize the use of the mouse, which greatly improves my focus and productivity;
- efficiently edit and navigate my source code.

VIM has a steep learning curve. Based on personal experience, it can be very intimidating at first. I know first hand, as I have failed a couple of times prior to switching from textmate. Thankfully, one day you eventually get the right [tutorials](https://github.com/benichu/2ret-vim/blob/master/README.md#tutorials) and [VIM configuration (.vimrc)](https://github.com/benichu/2ret-vim/blob/master/.vimrc) and before long, you find yourself navigating better through your files, and you start to remember more and more shortcuts and keys.

Today, I would like to share my VIM setup. It’s easy to install with this one liner command:

{% highlight bash %}
  $ curl http://2ret.com/vim -L -o - | sh
{% endhighlight %}

It’s still a work in progress considering some details need to be ironed-out, but I am quite happy with it and am using this as my work setup. The distribution’s [README is available on github](https://github.com/benichu/2ret-vim/blob/master/README.md), do not hesitate to check it out...
