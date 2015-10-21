---
title: How to load Clearing Lightbox using a URI hash on Foundation 5.
author: Jon Cuevas
layout: post
permalink: /articles/load-clearing-lightbox-uri-hash-foundation/
excerpt: "Using URI hash instead of query strings to load Foundation 5's Clearing Lightbox or modals"
keywords: "URI hash, Clearing Lightbox, Foundation 5, Foundation for websites, Responsive, jQuery, Street Photography, Flickr, 500px"
featured_image: /assets/images/articles/hash-foundation-clearing.jpg
featured_image_thumb: /assets/images/articles/hash-foundation-clearing.jpg
background_position: top center
bg_color: 'rgba(12, 78, 103, .9);'
text_color: light
comments: true
tags: [Foundation, Web Development, HTML5, Coding]
---
<div class="offgrid-right"><p>{% include adzone01.html %}</p></div>

<p class="lead">
I want to share how I made the <strong>Clearing Lightbox</strong> feature of Foundation 5 to be triggered by adding a location hash in your URI. The idea is to be able to share a page and, by adding a hash, have it load with the gallery already open when sharing photos or other media. I made the changes last night and will start to use this when sharing photos.
</p>

### What hash? Can this get you in trouble?

It's not that kind of hash, and it's not the kind that can [break the internet][2]{:target="_blank"} too. Let me try to explain this in plain english. Originally, a URI hash or location hash, is actually used for quick navigation to an anchor on a section within an HTML page, like when navigating to the ```#top``` of the page or to ```#footnotes```. A URI location hash is whatever follows after a # sign in the URI: Ex. in the address ```http://archon.digital.com/#about```, the ```#about``` is the hash, hence the term hashtags being used these days. Query strings are normally used in these cases but in here let's explore using hashes instead.

### Why use a URI hash instead of a query string?

As I just mentioned above, query strings are normally used for this purpose, but a URI hash is just another way, and in my opinion, a more elegant way to trigger JavaScript/AJAX on pages that have dynamic content to be bookmarkable (read: sharable on social media) and can also trigger events like firing up a [gallery][1]{:target="_blank"} or modal just by adding the hash to the URI. It can be used in the same way as query strings, but without triggering a new page request. The action happens client-side and allows data or content in the URI to be displayed or manipulated by JavaScript without ever reloading the page. And in case javascript is turned off or is blocked from loading, everything degrades gracefully and what you get is a working anchor to a section of your HTML page.

<div class="offgrid-left">
	<script src="https://gist.github.com/archondigital/c9a9902a8d96ad68e013.js"></script>
	<p class="caption">Loading this script right after loading Foundation would allow you to fire up Clearing just by adding a hash on your address.</p>
</div>

### The Script

Add the script shown on the screen right after the ```$(document).foundation();``` script for loading Foundation. You can change the ID and the hash to whatever you want and also position the anchor anywhere on the page. Loading a URL with the hash on your browser would then load the page with Clearing already open.

A live example of this can be seen by navigating to [this image post][3]{:target="_blank"}. You can apply this to any WordPress theme, on Jekyll or on static sites that use Foundation 5 and has [Clearing Lightbox][1]{:target="_blank"} enabled.


### Why would you want to do this?

One of the reasons why I wanted to be able to load Clearing Lightbox on opening a page is for when I share photos of my street photography on various forums. By the way, my photos are crap. But I would want to be able to share photos without distracting the people who would click through with my site by removing, or in this case, covering all the branding on my site. What users would see is just an opened up modal or lightbox that would show the entire image on a black background.

This would allow me to display my photo without any other distractions for the user and at the same time allow me to measure this interaction on my Google Analytics account. It's like using a third-party, image sharing service minus the third-party.

Usually people on online communities would share images through Flickr, 500px or Imgur or on any other free or paid online service. I don't see anything wrong with using these free image sharing services, but being a person with my own website, I am more inclined to share from my own site without relying on third-party services to be able to do just that. I would use my site as the primary source and from there just link to third-party services like Flickr or Instagram as a secondary resource.

Remember, Flickr, Instagram and all these image sharing platforms are all online services that may come and go at some point or their terms may simply allow them to remove your data in the future. Having your own infrastructure in place gives you the liberty of doing whatever you want with your content and data. It's not for everyone, but if you have the capability, then it would make more sense to do things your way.

[1]: http://foundation.zurb.com/docs/components/clearing.html
[2]: http://isolani.co.uk/blog/javascript/BreakingTheWebWithHashBangs
[3]: {{ site.baseurl }}/articles/pineapple/#photo

