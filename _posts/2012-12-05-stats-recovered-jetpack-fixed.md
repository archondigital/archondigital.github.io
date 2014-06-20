---
title: Stats recovered, Jetpack fixed
author: Jon Cuevas
layout: post
permalink: /stats-recovered-jetpack-fixed-1664/
custom_css:
  - 
custom_fonts:
  - 
custom_columns:
  - 
dsq_thread_id:
  - 959343096
categories:
  - Updates
  - Wordpress
---
<figure><img class="alignleft" title="screenshot of Jetpack website" src="{{ site.baseurl }}/assets/images/legacy/v5/Screen-Shot-2012-12-02-at-9.54.48-PM.png" alt="" width="324" height="229" /></figure> 
In my previous post, I wrote about how I suddenly lost several years worth of statistics after upgrading Jetpack on [Archon Digital][1]. Today, I got my stats back after support people from WordPress sorted my problem for me.

I received an email yesterday from a WordPress Happiness engineer named Valerie who apologized for time it took for my support request to get answered and was informed that they have located the source of the problem and have asked one of their engineers give the problem a look. This afternoon, I received an email with instructions on how to recover my old statistics along with some information on what caused the problem.

Apparently, an archive of a [previous version][2] of my site caused the issue. In the past, using WP-Stats, you&#8217;d be able to choose from a drop-down list, which site you&#8217;d want your stats to keep a record of. When I updated plugins on my archive site and installed Jetpack almost a year ago, I never realized this would become a problem. This probably explains why a week ago, when I had to &#8220;reconnect&#8221; my Jetpack on my WordPress for iOS app, the stats got reset.

The solution was simply to disconnect Jetpack from my archive site and disconnect then reconnect Jetpack on my existing site. Problem solved, my stats are all back. Thank you WordPress, I can now continue to gloat over my rather pathetic set of statistics and draw up more evil plans for [world domination][1].

 [1]: {{ site.baseurl }}
 [2]: {{ site.baseurl }}/v5/