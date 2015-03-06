---
layout: post
title: document early, document more
date: 2015-03-06 12:00 MST
redirect_from:
    - blog/2015/03/06/documentation
---

Recently at work, we were discussing risk management for start-ups — specifically, for [our start-up](http://getnotion.com). When each of us laid out what we saw as our risks on the whiteboard, a couple things became apparent. First, there were a ton of risks. What if one of our supply-chain partners had to delay? What if a tool we decided on at an earlier stage got too expensive, or turned out not to be the right one? What about all the extra hands we were foreseeing we would need — in marketing, customer service, engineering? What if — knock on wood — one of us got hit by a bus?

But another thing that kept coming up as we discussed ways to mitigate these risks was documentation. When we grow our support team, how will we train them quickly enough to be effective when we need them? By having a robust, searchable knowledge-base for reference. If we suddenly have to find a back-up manufacturer or supplier, how can we get the new partner up and running immediately to stay on schedule? By providing them with detailed documentation of our process and specifications. If one of our small team leaves unexpectedly, the more documentation about their work that we have, the faster and more seamlessly someone will be able to fill their shoes. It went on and on. By the end of the meeting, it was clear that **documentation was one of the biggest risk mitigators that we could actually do something about today.**

Obviously, "documentation" doesn't have a very exciting ring to it.<a href="#footnote1" name="footnote1anc"><sup>1</sup></a> Plus, there are people who would argue that documentation is at odds with the whole agile process<a href="#footnote2" name="footnote2anc"><sup>2</sup></a> — which, to some degree, we follow in our office. One of the trains of thought behind agile is that you move fast and iterate often, leaving no time for documentation, especially because whatever you’re documenting today may very well change in the next sprint two weeks from now. I understand this argument, but I think it's completely wrong.

Let me explain how I came to this opinion:

After our risk management meeting, I made it a personal goal that before I would `git commit` a piece of work, I would take a moment to look over my code, think about it at a high level, and try to identify areas that might not be totally self-explanatory to someone who hadn’t written the code -- and add documentation. Don’t get me wrong —- I totally believe in the idea that good code should be as transparent and well-communicated as possible in terms of small, well-named methods, clear organization, etc. —- but even when code is good, it can still take a lot of time for an outsider (i.e. anyone who didn’t write it) to get a solid feel for what the code is doing and how it is structured, especially if there are many classes or modules involved. So I started adding small comments here and there, maybe just at the top of a class or a method, briefly identifying the purpose, how it fit into the architecture, and/or why I did it that way, particularly if it took me a few tries or refactorings to get to the current state. 

I’m not gonna lie -- I’m still getting used to this. I’m still finding the balance between useful comments/documentation and unnecessary ones. I sometimes forget about my goal altogether, when I’m on a roll, feeling pressured, or caffeine-deficient. But I’ve already come away with some very clear benefits to this:

1. **Documentation helps me think at a higher level about my work, and helps me write better code.** When I start adding a comment to a method or class, I start to ask myself, is there actually a way I could’ve coded this to make it clearer or simpler? Why did I choose to write this or structure this in such a way? Making myself have an internal dialogue about all of this is especially beneficial when working on a small start-up team, when we don’t have a lot of time or capacity to discuss code at a detailed level or perform thorough team code reviews.<a href="#footnote3" name="footnote3anc"><sup>3</sup></a> It increases code quality and accountability without sacrificing much time - mine or other developers’. 

2. **Documentation early on brings clarity to an entire project’s development.** When I began putting together our public API’s documentation and dev portal, I knew that I wanted the docs to be open-sourced and for anyone in our dev community to be able to clone the repo and contribute to the docs or add their own tutorials. After I made the first iteration of our docs, I immediately wrote up the README on how to install and setup and begin contributing, instead of waiting until we actually wanted to launch the dev portal. I did this so that other people on my team would be able to contribute and deploy the docs without me, but it also helped me realize some aspects of the whole Jekyll-GithubPages-Bower-Grunt setup that were overly complicated and needed to be simplified. Keeping the documentation in mind while I was working on it was very helpful too — because it meant that I was constantly thinking, how can I make this as easy as possible for another developer not on my team to add their own tutorial, and how can I explain our setup easily? It’s given me a lot of clarity on how to structure this project and not over-engineer a simple documentation site.

3. **Documentation saves time.** If I keep our internal API docs up to date as I make changes, it adds maybe five minutes to my day. That saves me time tomorrow when the mobile developer needs to find out how to format a request — he can just check out the docs instead of interrupting my jam session at my desk to ask me. And for me, answering questions unrelated to what I’m currently working on isn’t just taxing on time - it’s taxing on my mental capacity for the day because I have to context-switch, and doing that multiple times in a few hours really kills my productivity.<a href="#footnote4" name="footnote4anc"><sup>4</sup></a>

So since I’ve started this, and as my company as a whole has been working increasingly to document our processes and the discussions we have, I’ve realized that **documentation doesn’t take time — it just takes discipline.** All it takes is making yourself incorporate it into your daily routine, and it becomes habit. It’s just like in boxing: if I start out going fast and paying little attention to form, sure, I might feel like I’m throwing stronger punches, but I’m not actually getting better. If I take a bit of extra time from the beginning to go slow and make sure I’m practicing good technique and thinking about what I’m doing, and keep that technique in mind as I get faster and faster, then after a few months I’ll be miles ahead of where I’d be if I just cared about hitting hard and moving fast.<a href="#footnote5" name="footnote5anc"><sup>5</sup></a>


<div class="footnote-block"></div>

<div id="footnote1">
<a href="#footnote1anc" name="footnote1sym">1</a> Unless, of course, you're into APIs, in which case you could discuss documentation all day.
</div>
<div id="footnote2">
<a href="#footnote2anc" name="footnote2sym">2</a> <a href="http://www.infoq.com/news/2014/01/documentation-agile-how-much" target="_blank">http://www.infoq.com/news/2014/01/documentation-agile-how-much </a>
</div>
<div id="footnote3">
<a href="#footnote3anc" name="footnote3sym">3</a> Or, ahem, when the software team is only 2 people.
</div>
<div id="footnote4">
<a href="#footnote4anc" name="footnote4sym">4</a> Check out <a href="http://www.petrikainulainen.net/software-development/processes/the-cost-of-context-switching/" target="_blank" >this blog post</a> and <a href="http://www.infoq.com/articles/multitasking-problems " target="_blank" >this article</a>.
</div>
<div id="footnote5">
<a href="#footnote5anc" name="footnote5sym">5</a> Yeah, I totally just made a reference to how I'm starting boxer circuit training, cuz I'm that baller and I'm gonna get that ripped.
</div>

<div class="footnote-block"></div>