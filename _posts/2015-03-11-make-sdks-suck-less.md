---
layout: post
title: how to make SDKs suck less
date: 2015-03-11 17:00 MST
---

This is a follow-up from [a previous post](http://shelbyswitzer.com/blog/2014/10/01/sdks-suck/) on SDKs being crap. My points in that post still stand for the most part, because, well, most SDKs suck. But being in the business of designing and building APIs, I can't escape them, and soon I'll even have to be building and maintaining them at [notion](http://getnotion.com).  In other words, for me, the question is no longer why do I have to keep using SDKs that suck, but how do I make them *not* suck?

My main gripes with SDKs are that they tend to be incomplete (e.g. I end up having to just make an HTTP request because the SDK doesn't provide a method to do wrap that request), poorly documented, or just one more layer adding complexity between me and an API. An S