---
title: Webfaction, Hosting that Sucks
author: Jon Cuevas
excerpt: "After 10 months of hosting under Webfaction, I'd like to give some insight and clarify a few points on as to why Webfaction sucks."
layout: post
permalink: /webfaction-hosting-sucks-1005/
keywords: "Archon Digital, Webfaction Sucks, Webfaction Hosting, Hosting that sucks, webfaction doesn't suck"
featured_image: /assets/images/legacy/v5/webfaction.jpg
bg_color: 'rgba(0, 0, 0, .8);'
text_color: light
comments: true
---

<p class="lead">
After 10 months of hosting Archon Digital with these guys, I'd have to say <a href="http://archon.digital/webfaction-hosting-sucks-1005/">Webfaction Sucks</a> because I cannot find anything negative to say about it. Go ahead and try to Google that keyword <strong>Webfaction Sucks</strong> as you'd find almost nothing negative being said about my current web host. That in itself is pretty self-explanatory and if you would try searching for Bluehost Sucks or Dreamhost Sucks or for any other host you'd find thousands of complaints from unhappy customers.<!--more-->
</p>

<div class="offgrid-left">
	<img class="size-full wp-image-1010 aligncenter" title="Webfaction, Hosting that Sucks" alt="Webfaction, Hosting that Sucks" src="{{ site.baseurl }}/assets/images/legacy/v5/webfaction.jpg" width="618" height="480" />
	<p class="caption">Screenshot of Webfaction's website, circa 2010.</p>
</div>

Not all hosting companies are perfect and the biggest problem I had with Webfaction, which lasted for a few days, was a routing issue I had where I could not connect via SSH or FTP to Webfaction's data center (The Planet). It turns out [my ISP was to blame][2] for the routing problems. Which I believe got fixed when I sent e-mails directly to their engineers after doing a whois on the IP addresses and sending e-mails to the technical people concerned. **Thank you tech guys at Smart** for getting this sorted out as it would never have gotten sorted under normal circumstances. Again throughout this ordeal Webfaction's support staff supported me all the way. This is even after the fact that they were aware that my problems were an external issue not related to them.

Another thing that makes **Webfaction suck less** than other hosting companies is that they are using a combination of **Nginx** and **Apache**, which for a year I was attempting to do by myself when Archon Digital was still under [Slicehost][3]. Moving **Archon Digital** to **Webfaction** took out the burden and stress of running my own bare server at a much lower cost and still achieve the configuration (nginx-apache) that I've always wanted to implement. Webfaction serves static content using **Nginx** and dynamic content using **Apache**. If you combine that with **W3 Total Cache** or **WP Supercache** where your content gets served by super fast **Nginx** as static content, you'd end up with a pretty fast loading site.

You can take a tour of Webfaction by watching the video clip below.

The control panel is different from the cpanel that is commonly found with shared hosting and it does take a bit of getting used to when you're new to it. Following a few short tutorials anyone serious about hosting their site would be up to speed with the ins and outs of Webfaction's control panel. There is no fantastico, which I never really cared to bother with before, but Webfaction has its own app installer which is pretty straightforward and easy to use.

Adding additional domains, applications, websites and tinkering with DNS overrides for MX records and TXT or CNAME changes is very easy and to the point. Those who are into getting their hands dirty can login via SSH and code away as if they are on a VPS account.

Servers are not full to the brim and Webfaction gives you the option of charging you for overages in case you go over your bandwidth limit. Most shared hosting companies would rather take down your account under such circumstances.

Lousy web hosts make more money off smaller hosting accounts which have low-traffic blogs that don't ever get too much bandwidth usage. **Webfaction sucks** as it **does not** promise you unlimited this or unlimited that and it clearly defines what it offers without any surprises in fine print. They even provide a 60-day money-back guarantee if in case you are not satisfied at all.

Now if you are convinced that **Webfaction doesn't suck at all** and would wish to sign up and **help me out** in the process, you can follow the affiliate link and [help Archon Digital complete his goal of World Domination][4].


[1]: http://archon.digital/webfaction-hosting-sucks-1005/
[2]: http://archon.digital/v5/internet/isp/smartbro/blame-it-on-my-isp-smart-bro/
[3]: http://archon.digital/v5/internet/hosting/a-new-slice-of-life-slicehost/
[4]: http://www.webfaction.com/signup?affiliate=archondigital
