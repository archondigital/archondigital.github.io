---
title: How to Disable Disqus & Google Adsense when running Jekyll on localhost.
author: Jon Cuevas
layout: post
permalink: /articles/disable-adsense-disqus-jekyll-localhost/
excerpt: "When I migrated my WordPress website to Jekyll, one of the things that I forgot to do was disable Disqus comments and Google Adsense on my localhost when running Jekyll locally."
keywords: "Google Adsense, Disqus Comments, Disqus, Adsense, Jekyll, localhost, disable Adsense, disable Disqus"
featured_image: /assets/images/articles/disqus-localhost.jpg
featured_image_thumb: /assets/images/articles/disqus-localhost-800.jpg
background_position: top center
bg_color: 'rgba(0, 0, 0, .9);'
text_color: light
comments: true

---
<div class="offgrid-right"><p>{% include adzone01.html %}</p></div>

<p class="lead">
When I migrated my <a href="http://archon.digital/articles/wordpress-to-jekyll/">WordPress website to Jekyll</a>, one of the things that I forgot to do was disable Disqus comments and Google Adsense on my localhost when running Jekyll locally. It was one of those things that I used to do from PHP when I was still on WordPress.
</p>

This had me end up with a lot of ```http://localhost:4000/…``` URLs on my Disqus account and something that I’d periodically clean whenever I find myself being OCD. I would find it hard to resist not deleting these mupltiple invalid posts on my disqus and I'd end up checking on it more and wasting more time. This was not a critical problem but it was something that wouldn't go away and was always bothering me.

<div class="offgrid-left">
	<img src="/assets/images/articles/disqus-localhost-800.jpg">
	<p class="caption">Replacing the disqus_shortname variable with a test account allows you to still preview disqus comments even when on localhost without generating "http://localhost:4000/" errors.</p>
</div>

Though the Disqus issue is more of a nuisance than a critical one, the same cannot be said for Adsense.

With ad impressions running from localhost, you run the risk of getting your Adsense account banned since it may appear to Google as simulated impressions which is a violation of their terms of use.

This prompted me to scout around for an elegant solution and that is how I came across this post from [Michael Parker][2]{:target="_blank"} on how he [disabled Disqus when running Jekyll on localhost][3]{:target="_blank"} using a second configuration file.

Apparently, Jekyll supports multiple config files running, something I just recently learned while browsing through this post and reading up on [Jekyll documentation][4]{:target="_blank"}. This same principle applies for when you want to disable Google Adsense.

Following the example from the blog post above, I added the following to my _config.yml:

```enable_disqus: true``` and ```enable_adsense: true```

I then created a _config_dev.yml where I added the two lines but this time I set the value as false:

```enable_disqus: false``` and ```enable_adsense: false```

On the include file, comments.html where I place the universal disqus code I then added the following conditional statement to the disqus_shortname variable:

<script src="https://gist.github.com/archondigital/6f649f1e455380e92269.js"></script>

This allows me to still load Disqus on localhost but using a 'testing' account instead of my real account.

Now for Adsense, I applied the same but replaced the Adsense code with a placeholder banner ad when running on localhost.
	
<script src="https://gist.github.com/archondigital/c03c0ea45f7969d1c7ea.js"></script>

I can now preview my site on localhost without violating Google Adsense terms but at the same time be able to see how it would appear when in production.

This is the command that I run when running Jekyll on my local machine.

```
jekyll serve --baseurl --drafts --cfig=_config.yml,_config_dev.yml
```

The second config file overrides the first one which results in Disqus and Adsense when running on localhost. 

Hopefully, Jekyll would have a more official solution to this in the future.



[1]: http://archon.digital/articles/wordpress-to-jekyll/
[2]: http://omgitsmgp.com/
[3]: http://omgitsmgp.com/2013/08/29/disqus-and-jekyll-on-localhost/
[4]: http://jekyllrb.com/docs/configuration/#build-command-options