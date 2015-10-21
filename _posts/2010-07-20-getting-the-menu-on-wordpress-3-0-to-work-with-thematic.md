---
title: Getting the Menu on WordPress 3.0 to Work with Thematic
author: Jon Cuevas
excerpt: 'One of the best new feature to come out of WordPress 3.0 is the menu editor. This drag-&-drop approach enables you to create custom navigation without being limited to the page or category hierarchy.'
layout: post
permalink: /getting-the-menu-on-wordpress-3-0-to-work-with-thematic-1044/
featured_image: /assets/images/legacy/v5/wordpress-menu.gif
bg_color: 'rgba(0, 0, 0, .8);'
text_color: light
categories:
  - Wordpress
tags: [WordPress, Web Development]
---
<div class="alignleft">
</div>

One of the best new feature to come out of WordPress 3.0 is the menu editor. This drag-&-drop approach enables you to create custom navigation without being limited to the page or category hierarchy. Being able to add external links and categories to the menu, I am now able to produce a fully customized navigation solution for my projects with relative ease.<!--more-->

<span class="attention">Update: The latest version of <a href="http://themeshaper.com/thematic/">Thematic</a> now fully supports the WP 3.0 menus</span>

Ever since I updated to version 3.0 of WordPress, I&#8217;ve been wanting to get the new menu feature to work with Thematic. For several days I tried but failed miserably at every attempt. Now thanks to <a title="Theo Ribeiro – Photographer" href="http://theoribeiro.com/" rel="home">Theo Ribeiro</a>, who posted about this on the [Themeshaper forums][1]after following [this post from thematic4you][2], I was able to implement it on projects where I use Thematic.<figure class="figure alignnone">

[<img class="size-full wp-image-1079" title="wordpress-menu" src="{{ site.baseurl }}/assets/images/legacy/v5/wordpress-menu.gif" alt="" width="589" height="425" />][3]<figcaption>The new WordPress menus allow you to easily drag-&-drop menu items</figcaption></figure> 
Copying the following code into your Thematic child theme&#8217;s functions.php will allow you to get the menu to work on Thematic.

<span class="attention">Update: updated the snippet from what <a href="http://theoribeiro.com/">Theo Ribeiro</a> just suggested from the comments below</span>

<pre class="brush: php; title: ; notranslate" title="">// We Register the a new menu for the theme called "Primary Menu"
function register_primary_menu() {
register_nav_menu( 'primary-menu', __( 'Primary Menu' ) );
}
add_action( 'init', 'register_primary_menu' );&lt;/code&gt;

&lt;code&gt;function change_menu_type() {
return 'wp_nav_menu';
}
add_filter( 'thematic_menu_type', 'change_menu_type' );

</pre>

I made only one minor change by following the comment thread on the Themeshaper forums which allowed the navigation to work perfectly. Reading up on [Function Reference/wp nav menu][4] on the WordPress codex will also help get you up to speed on how the menu system works.

 [1]: http://themeshaper.com/forums/topic/a-better-way-to-use-the-new-menu-in-wordpress-30-final-version
 [2]: http://programming.thematic4you.com/2010/03/how-to-test-wp_nav_menu-with-thematic/
 [3]: {{ site.baseurl }}/assets/images/legacy/v5/wordpress-menu.gif
 [4]: http://codex.wordpress.org/Function_Reference/wp_nav_menu