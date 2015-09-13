---
layout: page
title: Archives
permalink: /archives/
---

<!-- modified snippet taken from http://reyhan.org/2013/03/jekyll-archive-without-plugins.html -->
<h3>2015</h3>
{%for post in site.posts %}
{% unless post.next %}
<ul class="this no-bullet">
  {% else %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
  {% if year != nyear %}
</ul>
<h3>{{ post.date | date: '%Y' }}</h3>
<ul class="past no-bullet">
  {% endif %}
  {% endunless %}
  <li><time class="meta" style="display:inline-block;width:3.25rem;">{{ post.date | date:"%d %b" }}:</time> <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>