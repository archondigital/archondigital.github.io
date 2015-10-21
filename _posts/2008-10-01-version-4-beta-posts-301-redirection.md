---
title: Version 4 Beta, Posts and 301 Redirection
author: Archon Digital
excerpt: "Almost Done. Finally, after three months of finding spare time to sit down on and actually execute my design.Transferring per-post with 301 redirects on a new URL and permalink structure is tiring but fun."
layout: post
permalink: /v5/studio/wordpress/themes/version-4-beta-posts-301-redirection/
featured_image: /assets/images/legacy/v5/site-screenshot.jpg
bg_color: 'rgba(0, 0, 0, .8);'
text_color: light
categories:
  - Themes
tags: [Design, Wordpress, Web Development]
comments: true
---
{% include snippet-disclaimer-old-post.html %}

<div class="offgrid-left">
	<img src="/assets/images/legacy/v5/site-screenshot.jpg">
	<p class="caption">Screenshot of version 4.0</p>
</div>

<p class="lead">So far I'm happy with what I came up with and I'll be sticking and improving this design for some time.</p>

<!--more-->

### It has been a while since I've had this much fun

Migrating all my posts to a new permalink structure and redirecting each of my older posts took me a lot of time. Figuring it out took a few weeks of looking for solutions and almost decided to pay someone for the job. Eventually, I found a very simple plugin called [Permanent Redirector WordPress Plugin][1] for wordpress redirecting each post by creating a custom field containing the URL which you want to use for the 301 redirects.

### I can't express myself well

At first I was actually trying to redirect manually using regular expressions directly on the server block on my vhost file in nginx. That would've been the most practical way but sadly I suck at it.

### Tidying Up

In the next few days I'd be finishing and polishing everything I need for the site. The other sections are still being worked on and being tested on a local Ubuntu box before I upload.

[1]: http://www.taragana.com/products/free-wordpress-plugins/permanent-redirector