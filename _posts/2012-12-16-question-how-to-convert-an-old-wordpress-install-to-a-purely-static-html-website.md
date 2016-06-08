---
published: true
post_title: 'Question: How to convert WordPress install to a static HTML website'
author: Jon Cuevas
excerpt: "When I redesigned my site two years ago, I decided to archive my old WordPress installation as a way to clean up all the bloat it accumulated from years of installing plugins, themes and custom scripts. The most logical decision for me was to just start with a fresh WordPress install  and retire my old installation under a subfolder. Archiving my site also required me to manually put dozens of 301 redirects to allow search engines and old backlinks to still find their way into my blog."
layout: post
permalink: /question-how-to-convert-an-old-wordpress-install-to-a-purely-static-html-website-1737/
comments: true
tags: [WordPress, HTML, Jekyll, Web Development]
---

<div class="row">
	<div class="large-6 columns">
		<p class="lead">This post is not a how-to article, I merely want to find out what is the best way to convert a WordPress install to a static HTML website. I was about to write an aside which turned out to be pretty long for an aside so it evolved into an actual post.</p>

		<p>When I redesigned my site two years ago, I decided to archive my old WordPress installation as a way to clean up all the bloat it accumulated from years of installing plugins, themes and custom scripts. The most logical decision for me was to just start with a fresh WordPress install  and retire my old installation under a subfolder. Archiving my site also required me to manually put dozens of 301 redirects to allow search engines and old backlinks to still find their way into my blog.		</p>
	</div>

	<div class="large-6 columns">
		<img class="alignnone" title="convert wordpress to static html" alt="convert wordpress to static html" src="{{ site.baseurl }}/assets/images/legacy/code.jpg" />		
	</div>	
</div>

Fast forward two years, and I now have this chore of updating both my the current Archon Digital and its old version. This setup was also the main culprit of an [error after a Jetpack upgrade][1], which cost me a week and a half of lost stats.

I Google'd up and tried [Really Static][2] and [WP Static HTML Output Plugin][3] and still ran into a problem of not  having all my content from being converted automatically, scripts like timthumb wouldn't work, stylesheets missing, etc...

I want to change that by converting everything to a clean, static HTML or PHP version without the WordPress CMS part.

Any ideas, anyone?


 [1]: http://archondigital.com/lost-all-my-stats-after-jetpack-upgrade-1650/
 [2]: http://wordpress.org/extend/plugins/really-static/
 [3]: http://wordpress.org/extend/plugins/static-html-output-plugin/