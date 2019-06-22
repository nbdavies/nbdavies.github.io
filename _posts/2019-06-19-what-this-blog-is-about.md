---
layout: post
title: "What This Blog is About"
---
If I'm ever going to declare my intentions for this blog, this is probably the most sensible time to do that. 

### Why start a blog? 

I've been thinking about starting this blog just as a way to digest ideas. Solidify things I've learned, relate things I've observed, put forward hypotheses, organize uncollected thoughts on a subject. A place to put down things I don't want to keep carrying.

As much as I enjoy writing fiction, I think writing of any type strengthens your skills, and writing outside my typical narrative prose is probably a good idea. Also a blog is allegedly a good thing for people in different industries to have. Like web development, for example. Or publishing.

The posts can be about anything. Culinary experiments, music theory, what I'm writing, web development, biking, politics, books/games/movies I've experienced lately. 

Disclaimer: In no way do I claim to be an authority on anything. If I get something wrong, or if I miss an important point, let me know! The best I can do is post what I know at any given time, and try to build on that.

### What's under the hood?

I spend time during the day working on a complex application. So redesigning a personal website is also nice change of pace, and a fun way to try out new frameworks and tools.

On one extreme, there's something like Medium, or traditional Wordpress, where I'd be completely abstracted from what ends up on the page. Those services typically involve preset themes, and some kind of WYSIWYG editor that winds up introducing a lot of garbage HTML. And the resulting site may come with someone else's brand attached.

On the other extreme, there's starting completely from scratch: creating a website and blog by setting up a database with tables for posts, etc., and making a lot of decisions about how to present the database concepts in the browser. To mix wheel metaphors, that approach also seems within my wheelhouse, but it also seemed like it'd be reinventing the wheel.

In the middle, there are a lot of things in the vague, unofficial category of "open source blogs". I took a brief, shallow dive into these before getting a bit overwhelmed. Some that stood out were:
* Wordpress (the .org, not to be confused with the .com)
* Nikola
* Bolt
* Poet
* Postleaf
* Anchor
* Hexo
* Jekyll

I decided to start with Jekyll for now. I tried it out briefly once, about three years ago, but didn't spend much time with it. I like the idea of not having a database involved at all, which ought to make for a fast page load and allow for more hosting options, like GitHub pages. I might come back and try out some of these other options at some point.

I was intrigued (and still am) by the idea of [serverless pre-rendering](https://zeit.co/blog/serverless-pre-rendering). It looks like the approach described there would periodically (hourly or daily for instance) run a function to make an API request to wherever your content lives, and rebuild your static site using that up-to-date content. I don't need that complexity right now, but it might be worth coming back to.

Another option would be to store your content in whatever preferred "elsewhere" you want to use, and have the visitor's browser request it and insert it into the page. That would necessarily involve giving the browser access get that content. But if your content management layer can say "everyone can look, only you can touch", then that shouldn't be a problem.

These options would definitely be more attractive if it were easier to get content out of the lingua franca of content management, Google Docs. Perusing Google's API specs, it looks like you can get the .docx content, or you can traverse the structure of the document field by field. Through the Google Docs UI, you can "publish" a document, which makes it available in HTML form (e.g. biggest headings become h1 tags). The HTML version can contain artifacts--though perhaps not on the scale you would get from Wordpress. But I'm not certain that through the API you can effectively get the HMTL representation of a Google Doc, or even what it's "published" ID/URL would be.
