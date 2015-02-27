---
layout: post
title: APIs for IoT
date: 2015-02-25 22:00 MST
---

A couple weeks ago I wrote a [post on Notion's blog](http://notion.is/blog/2015/02/11/apis-for-iot-what-matters/) about
APIs for the Internet of Things -- specifically, three major points I'm thinking about a lot as we design the API, iterate on it,
and plan for scaling. 

The tl;dr:<a href="#footnote1" name="footnote1anc"><sup>1</sup></a>

* **Reliability**: IoT devices are part of our daily life and we rely on them for more than watching youtube or getting our work done.
APIs handling IoT information should be reliable -- redundant, persistent, and well-logged.

* **Real-time**: We tend to care about events from our devices when they happen, not thirty minutes later. At Notion, we're
implementing webhooks for real-time connectivity, but you could also use WebSockets to augment your API functionality.

* **Integration-ready**: Connected devices are even more useful when they're connected to each other and to other programs
or apps we use. Their APIs need to be built with integration in mind, to make this process easier and faster.

Read more in the whole post!
[http://notion.is/blog/2015/02/11/apis-for-iot-what-matters/](http://notion.is/blog/2015/02/11/apis-for-iot-what-matters/)

<div class="footnote-block"></div>

<div id="footnote1">
<a href="#footnote1anc" name="footnote1sym">1</a> Whoops, I realize this is actually a rather long "tl;dr." 
</div>

<div class="footnote-block"></div>