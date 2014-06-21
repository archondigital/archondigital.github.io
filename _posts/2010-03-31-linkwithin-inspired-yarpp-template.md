---
title: LinkWithin-Inspired YARPP Template
author: Jon Cuevas
layout: post
permalink: /linkwithin-inspired-yarpp-template-854/
comments: true
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

<pre class="brush: php; title: ; notranslate" title="">&lt;!--?php /* Example template Author: Archon Digital (Jonathan Cuevas) {{ site.baseurl }}/ */ ?--&gt;&lt;/pre&gt;
&lt;h3&gt;Possibly Related Posts&lt;/h3&gt;
&lt;pre&gt;
&lt;!--?php if ($related_query---&gt;have_posts()):?&gt;&lt;/pre&gt;
&nbsp;
&lt;ul class="related-posts"&gt;
&lt;ul class="related-posts"&gt;
	&lt;li&gt;&lt;!--?php $postimageurl = get_post_meta($post---&gt;ID, 'thumbnail', true); if ($postimageurl) { ?&gt;

 &lt;a title="Permanent Link to &lt;?php the_title(); ?&gt;" href="&lt;?php the_permalink(); ?&gt;" rel="bookmark"&gt;&lt;img src="&lt;?php bloginfo('stylesheet_directory'); ?&gt;/timthumb.php?src=&lt;?php echo $postimageurl; ?&gt;&h=100&w=100&zc=1&q=100" alt="&lt;?php the_title(); ?&gt;" width="100" height="100" /&gt;&lt;/a&gt;

 &lt;!--?php } else { ?--&gt;

 &lt;a title="Permanent Link to &lt;?php the_title(); ?&gt;" href="&lt;?php the_permalink(); ?&gt;" rel="bookmark"&gt;&lt;img src="&lt;?php bloginfo('stylesheet_directory'); ?&gt;/timthumb.php?src=&lt;?php bloginfo('stylesheet_directory'); ?&gt;/default.jpg&h=100&w=100&zc=1&q=100" alt="&lt;?php the_title(); ?&gt;" width="100" height="100" /&gt;&lt;/a&gt;

 &lt;!--?php } ?--&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/ul&gt;
&nbsp;
&lt;pre&gt;
&lt;!--?php else: ?--&gt;

No related posts.

&lt;!--?php endif; ?--&gt;

</pre>

## Copy the CSS

Add the following css to your theme's stylesheet or [download text file here][8].

<pre class="brush: css; title: ; notranslate" title="">ul.related-posts {

	float: left;

	list-style-type: none;

	margin: 0px;

	padding: 0px;

}

.related-posts li {

	list-style-type: none;

	float: left;

	width: 100px;

	padding-right: 8px;

	padding-left: 8px;

	font-size: 12px;

	line-height: 18px;

}

.related-posts img{

	width: 100px;

	padding: 1px;

	border: 1px solid #CCC;

}

</pre>

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
 [8]: http://archondigital.com/downloads/yarpp-custom-css.txt
 [9]: http://archondigital.com/assets/images/legacy/v5/yarpp.jpg
 [10]: http://archondigital.com/assets/images/legacy/v5/yarpp2.jpg