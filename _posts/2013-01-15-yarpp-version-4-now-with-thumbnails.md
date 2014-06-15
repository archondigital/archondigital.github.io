---
title: YARPP version 4 now with thumbnails
author: Jon Cuevas
layout: post
permalink: /yarpp-version-4-now-with-thumbnails-1835/
custom_css:
  - 
custom_fonts:
  - 
custom_columns:
  - 
feature_front_queue:
  - 1
dsq_thread_id:
  - 1025557622
categories:
  - Articles
  - Wordpress
---
**Yet Another Related Post Plugin** now offers a built-in thumbnail template option that takes advantage of WordPress&#8217; own post thumbnails function and can be enabled without requiring any extra PHP programming. All your options are now conveniently located on the settings page. This latest feature eliminates the need for a custom template similar to the [Linkwithin-inspired YARPP template][1] that I published way back in March 2010.

YARPP now also allows you to edit directly on your theme&#8217;s CSS file to customize the styling. The HTML output of the plugin now comes wrapped in distinct classes that would make it easier to narrow down to which element you want to tweak via CSS. The interface of the settings page is also sleeker and simpler to use and by default only displays the most basic of options which would be enough for most users. The more advanced users can easily enable the other options by choosing which panels you want to display as you normally would via the Screen Options button in the WordPress backend. There are more changes outlined in this release but most of these can be seen on the [Changelog][2] of the plugin&#8217;s download page.

### <img class="alignnone" alt="YARPP version 4 now with thumbnails" src="http://archondigital.com/wp-content/uploads/Screen-Shot-2013-01-14-at-3.59.45-PM.png" />

I&#8217;ve been using **YARPP** on older versions of **[Archon Digital][3]** and on other websites that I run but decided to ditch it along with dozens of other plugins when I last revamped my site back in October 2011. Reasons for that were not really related to YARPP, but was more on trying out new things and starting afresh. Then fast forward to November 2012, I installed YARPP 3.6 beta 5 and tested it for a few days on a local installation and then forgot about it until this weekend. At present, after two days of having [Yet Another Related Post Plugin][4]&#8216;s latest version back on my site, I can immediately notice the increased amount of traffic and some improvement on my blog&#8217;s bounce rates.

### Goodbye Timthumb.

You no longer need to use Timthumb to generate thumbnails which was the case in my previous **YARPP** post, and which also proved quite difficult to install for some users. I experienced this first hand when I received a lot of queries and comments asking for assistance in getting Timthumb to work on their WordPress installations after publishing that [post on using Timthumb on YARPP][1]. Calls for support on issues such as write permissions, typos and other Timthumb-related problems, most of which were unique to each person&#8217;s hosting environment, kept pouring in to my inbox and comments section for more than a year after published the article.

Also, based on my experience on several sites, using Timthumb together with YARPP consumes quite a lot of resources. This may not be optimal for the average blogger that relies on entry-level shared hosting. And don&#8217;t get me started on the Timthumb exploit that had me suddenly patch several dozens of websites in the past. The exploit has since been fixed, and I continue to use it on other websites, but since WordPress introduced post_thumbnails, and also now when employing a device-agnostic design workflow, I gradually moved away from using Timthumb altogether.

### Custom YARPP templates.

What I really like about [YARPP][5] is that it allows me to develop my own template should I chose to do so. Version 4 of the plugin allows for a wide range customizations that can range from a few simple lines of CSS, to custom functions that you can further extend as you develop your WordPress website. Right now, I&#8217;m going through the plugin&#8217;s code and documentation to help me come up with other ways that I can implement YARPP on other websites that I run.

### YARPP is old school, the awesome kind of old school.

This plugin has been around long enough that most WordPress users already know about the benefits that comes with having it around.

Now don&#8217;t get me wrong, it&#8217;s not all bells and whistles that we&#8217;re discussing here, YARPP, like other WordPress plugins if not properly setup, can consume quite a lot of RAM and CPU cycles which is most noticeable when deployed on a shared hosting environment. But that doesn&#8217;t mean you cannot run it on cheap shared hosting with a server stack that&#8217;s overloaded with websites aside from not being properly optimized. You can always install WP-Supercache or any other caching solution for a quick fix. Fortunately, I have a good setup on [**my host that doesn&#8217;t suck**][6] (my host uses a combination of NGINX and Apache), so I barely notice anything and can let the plugin run with minimal amount of tweaking.

To date, I still find it to be the best related posts plugin for WordPress. **[YARPP][5]** is so useful to me that I consider it as a &#8220;fire-and-forget&#8221; plugin that I can deploy on a website and literally forget about for a long period of time. There were several instances where I would only check on YARPP&#8217;s settings once after an install and would come back to it only after a year or two, or even after three years. Now how&#8217;s that for a reliable plugin?

 [1]: http://archondigital.com/linkwithin-inspired-yarpp-template-854/
 [2]: http://wordpress.org/extend/plugins/yet-another-related-posts-plugin/changelog/
 [3]: http://archondigital.com
 [4]: http://mitcho.com/code/yarpp/
 [5]: http://archondigital.com/topic/yarpp/
 [6]: http://archondigital.com/webfaction-hosting-sucks-1005/