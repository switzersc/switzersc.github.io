---
layout: post
title: in pursuit of making SDKs suck less
date: 2015-03-16 23:50 MST
---

This is a follow-up from [a previous post](http://shelbyswitzer.com/blog/2014/10/01/sdks-suck/) on SDKs being crap. My points in that post still stand for the most part, because, well, most SDKs suck. But being in the business of designing and building APIs, I can't escape them, and soon I'll have to be building and maintaining them at [notion](http://getnotion.com).  In other words, for me, the question is no longer why do I have to keep using SDKs that suck,<a href="#footnote1" name="footnote1anc"><sup>1</sup></a> but how do I make them *not* suck?

My main gripes with SDKs are that they tend to be incomplete (e.g. I end up having to just make an HTTP request because the SDK doesn't provide a method to wrap that request), poorly documented, or just one more layer adding complexity between me and an API.<a href="#footnote2" name="footnote2anc"><sup>2</sup></a> Also, from the point of view of the provider (a start-up provider at that), each SDK is one more library to maintain - and who's got time for that? I would love to spend half my time writing articles and documentation to help educate developers on how to interact directly and easily with an API using HTTP, but ultimately, if I want to make things easier for devs (who also don't have much time), sure, education is part of that,<a href="#footnote3" name="footnote3anc"><sup>3</sup></a> but so is giving them the tools to do amazing things faster and more reliably.<a href="#footnote4" name="footnote4anc"><sup>4</sup></a>

So how can I make an SDK that helps more than hurts?<a href="#footnote5" name="footnote5anc"><sup>5</sup></a> How do I make an SDK that not only makes my API more accessible, but more *manageable*? Can an SDK *enrich* the experience of using an API?

The number one thing first and foremost must be maintainability.<a href="#footnote6" name="footnote6anc"><sup>6</sup></a> This is a really loaded word here. It means that I as the provider should not have to exert a ton of effort to fix bugs, keep it up to date with API patches or different versions, etc. It also means that client devs shouldn't have to put in a load of work just to use it (or figure out how to use it) or debug problems. Practically, and perhaps somewhat obviously, this means making sure your SDKs are open-sourced<a href="#footnote7" name="footnote7anc"><sup>7</sup></a>, well-documented, and really not more complex than a simple wrapper around your API. 

But what I'm really excited about is the potential of SDKs to help consumers with exploiting hypermedia to explore and keep up with changes in the API. Until hypermedia evolves and starts to see more adoption by client developers, SDKs offer a great opportunity to leverage hypermedia and get hypermedia into the mainstream, while increasing maintainability. Maintainability, because the SDK can expose the API and its resources through the links given in responses or through the API spec (following apis.json or json.schema) so the provider as to do less hard-coding, but also because of [awesome developments](http://blog.apiary.io/2015/02/17/Utilising-API-Blueprint-in-API-Clients/) in the ability to generate hypermedia clients directly from your API documentation spec -- meaning all you have to do is keep up with your documentation.<a href="#footnote8" name="footnote8anc"><sup>8</sup></a> 

I'll be working on implementing some hypermedia SDKs in the near future and writing about my failures and successes, but in the meantime, check out these cool projects and resources:

* [Hyperclient](https://github.com/codegram/hyperclient)
* [HyperResource](https://github.com/gamache/hyperresource) and the [paper](http://petegamache.com/wsrest2014-gamache.pdf)
* [The Hypermedia Project](https://github.com/the-hypermedia-project)
* Mike Amundsen's ["Implementing Hypermedia Clients: It's Not Rocket Science"](https://mediaspace.msu.edu/media/Implementing+Hypermedia+Clients:+It%27s+Not+Rocket+Science/1_ip29lntc)
* Rob Zazueta's API and Hypermedia version of ["stop planning and start building"](http://www.mashery.com/blog/stop-talking-about-hypermedia-and-rest-start-building-adaptable-apis) - because flexibility, adaptability, and maintainability are the real aims here


<div class="footnote-block"></div>
<div id="footnote1">
<a href="#footnote1anc" name="footnote1sym">1</a> Not that I've used SDKs since I wrote that post, mind you. 
</div>
<div id="footnote2">
<a href="#footnote2anc" name="footnote2sym">2</a> See further discussion <a href="https://github.com/apicraft/detroit2014/wiki/Just-API-or-client-SDK-to-help-developers-with-API-adoption" target="_blank">here</a>.
</div>
<div id="footnote3">
<a href="#footnote3anc" name="footnote3sym">3</a> Not to mention witty and <i>utterly</i> convincing blog posts by yours truly.
</div>
<div id="footnote4">
<a href="#footnote4anc" name="footnote4sym">4</a> What? You mean I'm building software for <i>other people</i>?
</div>
<div id="footnote5">
<a href="#footnote5anc" name="footnote5sym">5</a> Read: helps way more. Actually, read: helps and doesn't hurt at all.
</div>
<div id="footnote6">
<a href="#footnote6anc" name="footnote5sym">6</a> Can you tell I'm trying to avoid explicitly writing a numbered list? Is it working? If you think so, tweet <a href="https://twitter.com/switzerly" target="_blank">@switzerly</a> to give me mad props; otherwise, you can keep your thoughts to yourself.
</div>
<div id="footnote7">
<a href="#footnote7anc" name="footnote7sym">7</a> So I can offload all the bug-fixing and README-ing to other people.
</div>
<div id="footnote8">
<a href="#footnote8anc" name="footnote8sym">8</a> And, of course, documentation should be at the top of your priorities anyway.
</div>
<div class="footnote-block"></div>