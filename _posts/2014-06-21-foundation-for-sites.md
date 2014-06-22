---
title: Foundation for Sites
author: Jon Cuevas
layout: post
permalink: /foundation-for-sites/
excerpt: "Just updated Archon Digital to Foundation 5.3 or now known as 'Foundation for Sites'."
featured: false
featured_image: /assets/images/Foundation-for-Sites.png
bg_color: 'rgba(0, 0, 0, .8);'
text_color: light
categories:
  - Images
format: image
comments: true
---
<div class="panel">
  <div class="row">
    <div class="large-6 large-push-6 columns">
      <img src="{{ site.baseurl }}/assets/images/Foundation-for-Sites.png" alt=""><hr>    
    </div>
    <div class="large-6 large-pull-6 columns">
      <p class="lead">I just finished updating my newly-minted, Jekyll-powered Archon Digital to <del>Foundation 5.3</del>, errr, <strong><a href="http://zurb.com/article/1316/foundation-strike-5-3-strike-for-sites">Foundation for Sites</a></strong> as how Zurb wants to call it now, and all I can say is, it is one brilliant piece of work. The people at Zurb have always kept busy working on better ways to iterate their products, so that us users of the framework can focus our attention on making our best ideas a reality.</p>
    </div>
  </div>  
</div>

<div class="row">
  <div class="large-12 columns">
    <h3>What's new?</h3>
    <p>The framework has come a long way since I first encountered it two years ago. It is now one of the most active open source projects on Github and the community supporting it is growing everyday. I've used Foundation since version 3.0 and have used it for all my projects since. Foundation 5.3 fixed a lot of bugs and added new components as seen on the <a href="http://foundation.zurb.com/docs/changelog.html">changelog</a>. I immediately went to work and checked out the new features and tested them here on this post. See them below.</p>    
  </div>
</div>

<div class="row">

  <div class="large-8 columns">

    <h3>Icon Bars</h3> 
    <p>The new Icon Bar component can be implemented to allow a user to navigate an app more quickly. The Icon Bar can be deployed either horizontally or vertically.</p>
    <div class="icon-bar six-up">
      <a class="item">
        <img src="{{ site.baseurl }}/assets/images/footer-foundation-retina.png">
        <label>One</label>
      </a>
      <a class="item">
        <img src="{{ site.baseurl }}/assets/images/footer-foundation-retina.png">
        <label>Two</label>
      </a>
      <a class="item">
        <img src="{{ site.baseurl }}/assets/images/footer-foundation-retina.png">
        <label>Three</label>
      </a>
      <a class="item">
        <img src="{{ site.baseurl }}/assets/images/footer-foundation-retina.png">
        <label>Four</label>
      </a>
      <a class="item">
        <img src="{{ site.baseurl }}/assets/images/footer-foundation-retina.png">
        <label>Five</label>
      </a>
      <a class="item">
        <img src="{{ site.baseurl }}/assets/images/footer-foundation-retina.png">
        <label>Six</label>
      </a>
    </div>

    <h3>Vertical Range Sliders</h3>
    <div class="row">
      <div class="large-1 large-push-1 columns">
        <div class="range-slider vertical-range" data-slider data-options="vertical: true; display_selector: #sliderOutput;">
          <span class="range-slider-handle"></span>
          <span class="range-slider-active-segment"></span>
          <input type="hidden">
        </div>      
      </div>

      <div class="large-9 columns">
        
        <p>Slide the slider to change this value <strong><span id="sliderOutput"></span></strong>. Isn't that amazing?</p>
        <p>Foundation's Range Sliders allows you to drag a handle to select a specific value from a range.</p>
      </div>
    </div>    

    <h3>Switches</h3>
    <div class="row">

      <div class="large-1 large-push-1 columns">
        <div class="switch">
          <input id="exampleCheckboxSwitch" type="checkbox">
          <label for="exampleCheckboxSwitch"></label>
        </div> 

        <!-- Using radio buttons – each switch turns off the other two -->
        <div class="switch small">
          <input id="exampleRadioSwitch1" type="radio" checked name="testGroup">
          <label for="exampleRadioSwitch1"></label>
        </div> 

        <div class="switch radius">
          <input id="exampleRadioSwitch2" type="radio" name="testGroup">
          <label for="exampleRadioSwitch2"></label>
        </div> 

        <div class="switch round large">
          <input id="exampleRadioSwitch3" type="radio" name="testGroup">
          <label for="exampleRadioSwitch3"></label>
        </div>      
      </div>

      <div class="large-9 columns">
          <p>New Switches component is a toggle element that allows for an Off and On state upon tapping or clicking. I find it amazing that these only require simple checkbox inputs or radio buttons to function.</p>
      </div>  
    </div>
  </div>

  <div class="large-4 columns">
    <div class="panel callout">
      <h4>Foundation Resources for your projects</h4>
      <p>For those interested in using Foundation framework, you can download one of the bloilerplate projects below to jumpstart your own Foundation-based project.</p>
      <ul>
        <li><a href="http://madmimi.github.io/angular-foundation/">Angular Foundation</a></li>
        <li><a href="http://picotto-wp.urbanjonathan.com/">WordPress: Picotto by Jonathan Urban</a></li>
        <li><a href="https://github.com/olefredrik/foundationpress/">WordPress: FoundationPress by Ole Fredrik Lie</a></li>
        <li><a href="http://jointswp.com/">WordPress: JointsWP by Jeremy Englert</a></li>
        <li><a href="https://github.com/penibelst/jekyll-noita">Jekyll: Noita by Anatol Broder using Foundation 5</a></li>
        <li><a href="https://github.com/timothyasp/pyrocms-theme-foundation">PyroCMS: PyroYeti by Timothy Asp</a></li>
        <li><a href="http://waterlee.jakesharp.co/">Magento: Waterlee Boilerplat by Jake Sharp</a></li>
      </ul>
      <p>Let me know if you want your Foundation 5 based project to be listed here. Just send me a link in the comments section at the end of this post.</p>
    </div>
  </div>

</div>

Updating my site was as simple as running the "bower update" command in my assets folder, everthing went smooth and I did not encounter any problems. I can easily use components of the latest version on any part of my site whenever there is a need to.

Foundation would always be my first choice whenever starting a new Project. You should also check out their post on **[Foundation for Apps][3]** which they will soon launch.

<hr>


[1]: http://foundation.zurb.com/docs/changelog.html
[2]: http://zurb.com/article/1316/foundation-strike-5-3-strike-for-sites
[3]: http://zurb.com/article/1312/the-next-foundation