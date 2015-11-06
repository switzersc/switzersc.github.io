---
layout: post
title: API-first & Native Apps for Start-ups
date: 2015-11-05 20:00 MST
---

I have an Android, and that means that I'm typically the last to get the coolest new apps or to be able to use the latest IoT devices -- because they all start with iOS first. It makes me wonder why many of these companies don't start with a responsive web app first, and do native apps later -- that way, they'll be able to support all platforms out the gate. There are some obvious restrictions to web apps, like not having quite the same access to the platform's hardware and not being able to easily pass wifi credentials to an external device: for example, if you buy a bridge or hub for your smart home system and it needs to connect to the wifi, as far as I know, the best user experience requires a native app so that your phone's wifi settings can be passed seamlessly through the app to the device.<a href="#footnote1" name="footnote1anc"><sup>1</sup></a>

But it also occurred to me that building native-first is by default explicitly and intentionally building API-first.<a href="#footnote2" name="footnote2anc"><sup>2</sup></a> Done right, API-first architecture yeilds so many benefits for a start-up. Firstly, it provides an immediately high level of flexibility: the number of platforms you can build for becomes infinite, since all you need is to develop another client that consumes your already-built API. If all your business logic is centralized on your API instead of implemented client-side, then it becomes even easier to build new clients, because you're not porting around your business logic to different code bases and desperately trying to keep things consistent.  Furthermore, if you're implementing a hypermedia API,<a href="#footnote3" name="footnote3anc"><sup>3</sup></a> building and maintaining new clients becomes even easier. In contrast, if you had originally created a monolothic web app, you will later need to do double the work to create an API and then native clients to consume that API.<a href="#footnote4" name="footnote4anc"><sup>4</sup></a>

API-first design for start-ups also has major business implications. We're increasingly immersed in the (API economy)[http://www.forbes.com/sites/ciocentral/2012/08/29/welcome-to-the-api-economy/], and most start-ups without an API are missing the boat. By missing the boat, I mean they're missing huge opportunities to expand into new markets, develop B2B partnerships, and make their service even more relevant and connected.<a href="#footnote5" name="footnote5anc"><sup>5</sup></a> By starting out with an API, start-ups are one step closer to having an open API -- even if that means open to any third party dev or only open to enterprise partners.


<div class="footnote-block"></div>
<div id="footnote1">
	<a href="#footnote1anc" name="footnote1sym">1</a> If I'm wrong on this and you can do this easily with a web app on mobile as well, please let me know!
</div>
<div id="footnote2">
<a href="#footnote2anc" name="footnote2sym">2</a> Or if it's not, it should be. 
</div>

<div id="footnote3">
<a href="#footnote3anc" name="footnote3sym">3</a> http://apievangelist.com/2014/01/07/what-is-a-hypermedia-api/
</div>

<div id="footnote4">
<a href="#footnote4anc" name="footnote4sym">4</a> Although yes, it's becoming increasingly common to build web apps that use APIs, e.g. a purely JavaScript front-end consuming a Rails API. 
</div>
<div class="footnote-block"></div>

<div id="footnote5">
<a href="#footnote5anc" name="footnote5sym">5</a> http://www.3scale.net/api-economy/
</div>
<div class="footnote-block"></div>
