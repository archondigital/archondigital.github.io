---
title: LinkWithin-Inspired YARPP Template
author: Jon Cuevas
layout: post
permalink: /articles/linkwithin-inspired-yarpp-template/
comments: true
tags: [WordPress, YARPP, Linkwithin, Web Development, Coding]
disqus_identifier: 933359197
---
Archon Digital has created a **simple custom template for YARPP** that would allow it to display post **thumbnails** on related posts, similar to how **LinkWithin** displays relevant articles.

<!--more-->

## LinkWithin-Inspired YARPP Template with thumbnails using Timthumb

Yesterday, after reading a forum entry on CMF about LinkWithin, I immediately went and installed it on my site just to test and see if it worked as discussed by the forum members. The plugin seemed fine with the only two issues I have is that Linkwithin has a link back to it's own site and on top of that, it wasn't being distributed on WordPress.org.

For those of you like me, who are not at ease on using plugins not found on WordPress.org's repository of open source plugins, Archon Digital created a cutomized template for [**Yet Another Related Post Plugin**][1] or **YARPP** by [mitcho (Michael 芳貴 Erlewine)][2]. Since version 3.0, the YARPP plugin allows custom templates as <a href="http://mitcho.com/blog/projects/yarpp-3-templates/" target="_blank">described in this post</a>.

I've been using **YARPP** for such a long time now that I actually just forgot about it and ignored it altogether. All this time I knew there were ways to customize the template and style it with CSS but for some reason, since the plugin just worked well for me, I left it like the way it was when I first installed it.

It seems a major part of what makes the **Linkwithin plugin** perform so well on blogs is that it displays your related posts along with thumbnails using their own proprietary way of weighing which posts are relevant. To achieve something similar I had to create a template that uses timthumb.php to generate the thumbnails for me using a custom field I am already using extensively on my blog.<figure class="figure alignnone">

[<img class="size-full wp-image-862 " title="LinkWithin-Inspired YARPP Template with thumbnails using Timthumb" alt="LinkWithin-Inspired YARPP Template with thumbnails using Timthumb" src="{{ site.baseurl }}/assets/images/legacy/v5/yarpp-linkwithin.jpg" width="590" height="228" />][3]<figcaption>A sample of how the custom YARPP template looks</figcaption></figure> 
**Timthumb** was an image-resize script created for [Mimbo Pro][4] and was eventually released by [Darren Hoyt][5] as open source. It is for me one of the best scripts or plugins created to help theme authors to simplify the generation of post thumbnails. Archon Digital uses the timthumb script extensively on this site.

<span class="Apple-style-span" style="font-weight: bold; color: #000000;">Requirements</span>

*   **YARPP**. In case you haven't yet, install the plugin [YARPP][6] and set the Display options to display using a custom template file as seen on the image below.
*   **Timthumb**. Download the [timthumb][7] script. Copy it to your existing theme folder.
*   **Cache folder**. create a folder called *cache* inside your existing theme folder and set the permissions to 755 or 777 via your ftp software.
*   **Default image**. create an image and save it as *default.jpg* and upload it to your existing theme folder. This will be the default image in case your post still has no thumbnail assigned to it.

## Create a custom PHP file "yarpp-template-post-thumbnail.php"

Copy and paste the following code to notepad or any text editor and the save file as "yarpp-template-post-thumbnail.php" inside your current theme folder

<script src="https://gist.github.com/archondigital/558ea6840798c60fb9c5.js"></script>

## Copy the CSS

Add the following css to your theme's stylesheet or [download text file here][8].

<script src="https://gist.github.com/archondigital/b22f4f008b71e065ed08.js"></script>

## Set your YARPP options

Go to your YARPP options panel and follow as illustrated below<figure>

[<img class="alignnone size-full wp-image-857" title="LinkWithin-Inspired YARPP Template with thumbnails using Timthumb" alt="LinkWithin-Inspired YARPP Template with thumbnails using Timthumb" src="{{ site.baseurl }}/assets/images/legacy/v5/yarpp.jpg" width="520" height="426" />][9]</figure> 
## Timthumb and custom fields

The template file has refers to a custom field called *thumbnail* for the timthumb script to work. The thumbnail custom field would require your image's full URL as its value.<figure>

[<img class="alignnone size-full wp-image-859" title="LinkWithin-Inspired YARPP Template with thumbnails using Timthumb" alt="LinkWithin-Inspired YARPP Template with thumbnails using Timthumb" src="{{ site.baseurl }}/assets/images/legacy/v5/yarpp2.jpg" width="590" height="370" />][10]</figure> 
In case you are already using timthumb on your theme then you will only have to edit the template file to match your own custom field. Simply edit the word &#8216;thumbnail' on line 9 of the template (see image above).

**<span style="font-weight: normal;">Still, <a href="http://www.linkwithin.com/learn"><strong>Linkwithin</strong></a> is a great and effective plugin for bloggers who want a significant improvement on their bounce rates and to those who would want a good related post plugin for WordPress. Definitely, </span><span style="font-weight: normal;">YARPP is better </span><span style="font-weight: normal;">but I think Blogger users would find LinkWithin more useful as it greatly increases the interactivity and it's very simple to implement.</span>**

 [1]: http://mitcho.com/code/yarpp/
 [2]: http://mitcho.com/
 [3]: {{ site.baseurl }}/assets/images/legacy/v5/yarpp-linkwithin.jpg
 [4]: http://www.darrenhoyt.com/2008/03/12/mimbo-pro-magazine-theme-released/
 [5]: http://www.darrenhoyt.com/2008/04/02/timthumb-php-script-released/
 [6]: http://wordpress.org/extend/plugins/yet-another-related-posts-plugin/
 [7]: http://timthumb.googlecode.com/svn/trunk/timthumb.php
 [8]: https://gist.github.com/archondigital/b22f4f008b71e065ed08
 [9]: http://archondigital.com/assets/images/legacy/v5/yarpp.jpg
 [10]: http://archondigital.com/assets/images/legacy/v5/yarpp2.jpg