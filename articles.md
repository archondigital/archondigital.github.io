---
layout: page
title: Articles
permalink: /articles/
---

<div class="posts">
  
	<div class="row">
		<div class="large-8 columns">
			{% for post in site.posts %}
				<article>
					<h2><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
					<span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
					<p>{{ post.excerpt }}</p>
				</article>

			{% endfor %}
		</div>

		<div class="large-4 columns">
			<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
		</div>
	</div>

</div>

  
