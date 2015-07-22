---
layout: post
title: API versioning doesn't matter
date: 2015-07-22 08:00 MST
---

Let's face it: you will at some point have to introduce breaking changes to your API. Most of us plan for this, and try to mitigate the consequences, by versioning. There are loads of ways people out there are versioning -- introducing a new subversion with every minor change, bundling changes into major version releases, using content negotiation to manage different versions of resources, etc --  and people bicker to no end about the best way to do this. But if one thing is becoming clear,<a href="#footnote1" name="footnote1anc"><sup>1</sup></a> it's that the way you version your API doesn't matter -- **the way you communicate does.**

**Good communication with your consumers is the key to easing transition to and adoption of new iterations of your API, and this means:**

* Be transparent about how you are going to version (or not version) your API from the beginning. 
* Let your consumers<a href="#footnote2" name="footnote2anc"><sup>2</sup></a> know well in advance what changes you're about to introduce (and maybe even say why!). 
* Keep older versions around long enough for transitions and communicate a lot about deprecation -- and even keep tabs on who is still using those older versions so that you can communicate with them directly about getting them up to speed with your latest API. 
* Be active in any open source communities maintaining libraries for or using your APIs, at least to open issues letting them know the details of upcoming changes. 

For those of us shouting **"Hypermedia! Hypermedia!"** as an alternative to versioning, or at least as a helpful hand in the process: yes, the goal of hypermedia and RESTful architecture is to allow systems to evolve after they are already deployed gracefully, so that the API exposes new behavior through hypermedia and clients execute this on the fly.<a href="#footnote3" name="footnote3anc"><sup>3</sup></a> This would be *awesome* -- if our clients are actually written to consume hypermedia like this. But the fact is, most clients aren't, and even if hypermedia practices were mainstream, if you have an open API, you have no clue who your consumers are and/or how they're consuming your API. If you make changes to a resource and expect hypermedia clients to be able to keep up, you're ignoring any devs out there who might not be using hypermedia clients. If you communicate about these changes in advance, at least those folks will have a chance to prepare and catch up. 

You're never going to keep all of your API consumers happy:<a href="#footnote4" name="footnote4anc"><sup>4</sup></a> you're going to break things, you're going to expect they consume your API in specific ways or for specific purposes, and you're going to be wrong. **The only way to minimize breakage and maintain happiness in your community is transparency and proactive communication.**

<div class="footnote-block"></div>
<div id="footnote1">
	<a href="#footnote1anc" name="footnote1sym">1</a> From my experiencs consuming APIs and preparing to launch one into the dev community, as well as from the APIstrat discussion on versioning at the most recent [Gluecon](http://gluecon.com/). That discussion was packed with people trying to figure out how to version gracefully, and it all came down to how you communicate with your consumers. 
</div>
<div id="footnote2">
<a href="#footnote2anc" name="footnote2sym">2</a> Internal or external dev community, API partners -- whoever is on the other end.
</div>

<div id="footnote3">
<a href="#footnote3anc" name="footnote3sym">3</a> http://www.infoq.com/articles/roy-fielding-on-versioning
</div>

<div id="footnote4">
<a href="#footnote4anc" name="footnote4sym">4</a> Unless you're the only one consuming your API, and even then, I don't know about you but I frequently am annoyed by decisions made by an earlier me.
</div>
<div class="footnote-block"></div>