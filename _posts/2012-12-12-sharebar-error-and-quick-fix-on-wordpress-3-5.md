---
published: true
post_title: Sharebar error and quick fix on WordPress 3.5
author: Jon Cuevas
layout: post
permalink: /sharebar-error-and-quick-fix-on-wordpress-3-5-1717/
comments: true
tags: [WordPress, Web Development, Coding]
---
I ran into some problems with the Sharebar plugin immediately after upgrading to WordPress 3.5. All my posts where [Sharebar][1] is active were displaying the following error code.

<pre class="brush: php; published: true
post_title: ; notranslate" title="">Warning: Missing argument 2 for wpdb::prepare(), called in /&lt;path&gt;/wp-content/plugins/sharebar/sharebar.php on line 112 and defined in /&lt;path&gt;/wp-includes/wp-db.php on line 990
</pre>

<div class="alignleft">
</div>

This got me scrambling for whatever quick fix I could find because I use this plugin on a number of sites and I fear that having them display an error message with the path of my WordPress installation exposed would be a security risk.

Disabling the plugin while waiting for an update was not an option for me because some of the sites I run rely on this plugin a lot and I can't afford to have it deactivated even for a brief period. Besides that, I'm the sort who's always looking forward to getting my hands dirty fixing stuff on my own. After running a quick search on Google, I found this in the [WordPress.org forums][2] and one of the users, [e3mobile][3], contributed a fix which worked for all my sites using Sharebar.

e3mobile, suggested editing the file sharebar.php located in the Sharebar folder inside wp-plugins.

On Line 112 look for;[  
][2]

<pre class="brush: php; first-line: 112; published: true
post_title: ; notranslate" title="">$results =$wpdb-&gt;get_results($wpdb-&gt;prepare("SELECT * FROM ".$wpdb-&gt;prefix."sharebar WHERE enabled=1 ORDER BY position, id ASC")); $str .= "\n";&lt;/a&gt;
</pre>

and replace it with this;

<pre class="brush: php; first-line: 112; published: true
post_title: ; notranslate" title="">$results =$wpdb-&gt;get_results($wpdb-&gt;prepare("SELECT * FROM ".$wpdb-&gt;prefix."sharebar WHERE enabled=1 ORDER BY position, id ASC", null)); $str .= "\n";
</pre>

Then on line 124, look for this;

<pre class="brush: php; first-line: 124; published: true
post_title: ; notranslate" title="">$results = $wpdb-&gt;get_results($wpdb-&gt;prepare("SELECT * FROM ".$wpdb-&gt;prefix."sharebar WHERE enabled=1 ORDER BY position, id ASC")); $str .= "\n";
</pre>

and replace it with this;

<pre class="brush: php; first-line: 124; published: true
post_title: ; notranslate" title="">$results = $wpdb-&gt;get_results($wpdb-&gt;prepare("SELECT * FROM ".$wpdb-&gt;prefix."sharebar WHERE enabled=1 ORDER BY position, id ASC", null)); $str .= "\n";
</pre>

Hope this helps, I'm no PHP expert, but I just want to share this now because this is what worked for me which you might want to implement while waiting for the plugin author to release an update.

 [1]: http://devgrow.com/sharebar-wordpress-plugin/
 [2]: http://wordpress.org/support/topic/error-with-wordpress-35
 [3]: http://wordpress.org/support/profile/e3mobile