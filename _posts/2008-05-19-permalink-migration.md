---
published: true
post_title: Permalink Migration on WordPress
author: Jon Cuevas
layout: post
permalink: /v5/permalink-migration-142/
featured_image: /assets/images/legacy/v5/blanktheme-lead.jpg
bg_color: 'rgba(0, 0, 0, .8);'
text_color: light
categories:
  - Articles
  - Wordpress
tags: [WordPress, Web Development, Coding]
disqus_identifier: 933414660
---
{% include snippet-disclaimer-old-post.html %}

It has been one of those things you knew you had to do but was near the bottom of your very long to-do list. But after a few days of thinking it over and browsing the web and eventually looking for the right plugins, I managed to migrate my permalink structure to a more keyword rich, SEO friendly layout.<!--more-->

My old permalink structure was the date based */%year%/%monthnum%/%day%/%postname%/* which I still find to be useful for proper chronological organization of one&#8217;s journal or news items but I also find my new permalink structure */%category%/%postname%/* to be more keyword rich and easier for both humans and bots.

## The Plugin

I am now using [Permalink Redirect][1] by [Scott Yang][2] to help me simplify the process of migrating permalinks. The plugin worked like a charm. I tested how the plugin would handle backlinks using the old permalink structure and everything redirected properly to the new permalink structure without any noticeable delay.

## Small Hiccup

There was only one problem I encountered while migrating my permalink structure and that was which category name will be used. By default, WordPress would use the category name with the lowest ID if incase you have multiple categories per post. My theme makes use of different categories as well as some temporary categories which I use as a switch to place posts on the four special feature sections of my theme.

The answer to this minor problem was [sCategory Permalink][3], a plugin by [Dmytro Shteflyuk][4] which allows you to tick which category your post will use for your permalink structure. It works by making use of a custom permalink option *%scategory%* (take note of the extra &#8220;s&#8221; before the category word).<figure>

<img class="aligncenter" src="http://archon-digital.com/images/scategory.jpg" alt="" /></figure> 
## There is Always a Better Way

What I really wanted was to somehow write a few lines of code on my vhost file on Nginx so redirection would be done on the webserver and not through PHP. For me this is the ideal setup as it puts less load on your server. I also have enough documentation to configure this for Apache but not for Nginx. The next few days were spent looking around for answers, which included several forum postings and reading a lot of Nginx documentation. I gave up after a week so I was left with the plugin option instead but still open to learning how to do it through Nginx but for now I would settle for the plugin.

A person&#8217;s quest for knowledge can only be limited by himself and not by anything else. For now this setup works well for me but I know there is better way of doing things.

### Other Related Articles

<a title="Permanent Link: Migrating your WordPress Permalinks Structure" href="http://www.cravingtech.com/migrating-your-wordpress-permalinks.html" rel="bookmark">Migrating your WordPress Permalinks Structure</a> by Michael Aulia

 [1]: http://scott.yang.id.au/code/permalink-redirect/
 [2]: http://scott.yang.id.au/
 [3]: http://kpumuk.info/projects/wordpress-plugins/scategory-permalink/
 [4]: http://kpumuk.info/