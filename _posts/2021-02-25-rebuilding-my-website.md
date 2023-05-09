---
title: "Rebuilding the Site and a Retrospective on the Wild Web"
author: {{site.author}}
last_modified_at: 2021-02-25
categories: [tech]
---

## Why

As someone that is relatively privacy conscious the idea of using my website as an alternative to social media has been developing in the back of my head for a while now.
Going back to the "wild west" of the internet and not relying on any platform to post my own stuff feels strangely refreshing, considering that it is a very old way of using the internet.
One day I was helping a friend start his own jekyll blog and this inspired me to finally bite the bullet and rebuild it.
I wanted to make the layout much simpler, and not rely on a theme for custom styling.
I also wanted to make some new sections to accommodate the type of content one might like to post on social media like images and short *"microblogs"*

## How

I have been using the [minimal mistakes theme](https://mmistakes.github.io/minimal-mistakes/) on my site for quite some time now and although it does a great job of looking good and having plenty of functionality it is anything but "minimal".
I wanted to use a much simpler theme or make my own theme.
I ended up not using a theme and doing all the styling myself.
for the style I was quite inspired by the excellent site [tilde town](tilde.town)

Since I struggled getting jekyll and ruby to work on my windows machine I started with the [jekyll base](https://github.com/danielmcgraw/Jekyll-Base) repository and removed the theme from ``_config.yml``.
I started with a simple main page that just lists all my blog posts chronologically and slowly added more categories and a nav bar etc.
[This cheatsheet](https://gist.github.com/magicznyleszek/9803727) proved useful in figuring out some of the more complicated liquid syntax.
One of the things I struggled with most was excluding the micro blog posts from the main blog page since I would like to be able to post more often and more freely without it cluttering up the section that contained longer more "serious" blog posts.

## Join Me

If you are reading this and feel like the idea interests you too, I urge you to start your own website.
It can be a fun way to learn a few new skills and use some of your creativity.
If your needs are simpler than mine you can even host plain html pages for free (without having to deal with jekyll) on [neocities](https://neocities.org/).
[github pages](https://pages.github.com/) will also let you host plain html but the community over on neocities is much more suited to this style of website.

Please send me a link to your site if you were inspired by this!
