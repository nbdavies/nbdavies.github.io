---
layout: post
title: "Total Update!"
---
My intentions for regularly updating this blog have so far not turned into reality. There have been some other things going on. So here's a rapid-fire update on various fronts:

### Coding

For the Open Elections project, Wisconsin hasn't had any elections lately, but we noticed that the website went down in August, and parts of the site are down still. It was an occasion for the folks leading that project to reassess how it's presented online. Some of my effort since then has been prototyping what an alternative site could look like. I plan to post more about that later.

I've also been helping a Wisconsin assembly candidate get her website going. I didn't have much experience with Wordpress going into it, so it's been educational for me, as well as good practice in design. Is it exemplary? Next-level? Not yet. But it's helping a challenger establish a competitive web presence against the incumbent.

I also switched my band's site (gentlebrontosaurus.com) over to a Jekyll/Github Pages stack like this one. The concept of pulling content from Facebook and Twitter dynamically wasn't reliable in practice. Events didn't show up consistently. The newsfeed wasn't very useful. The Facebook API version I'd used was going to be deprecated soon. Also the SSL certificate had expired, and it seemed like Heroku was going to charge for maintenance of that. Since the site didn't really need a database or API keys behind it anymore, moving to a static site made sense. 

I also fixed a couple things I'd noticed wrong with the page. YouTube embeds were loading Google Ads and Analytics scripts that caused errors. For the social icons, an `a` tag with an `object` inside it for SVG content no longer made the `object` clickable. 

The downside of this stack is that I had the site written in Slim, and I had to convert it all to HTML. There is a Jekyll plugin for Slim support, but it doesn't work with more recent Jekyll versions. More to the point, Github Pages only supports certain Jekyll plugins, and that one isn't in the list. Nor is HAML.

### Travel

My partner and I went on a trip to Catalonia. It was my third time there, her first. We spent about 5 days in Barcelona and about 5 days biking in the Girona region, mostly following the Vies Verdes and/or Pirinexus route. Though our itinerary didn't go entirely according to plan. I intend to write more about that.

I wasn't intending to plan another trip right away. But now biking season's essentially over for winter (for me anyway), and for some reason I started looking at river valleys in the Alps. Now I think I've got a sweet itinerary plotted out, ready to go for next summer

### Writing

I'm about 80% through the rewrite of "A City Divided" (I guess I've been calling it). Apparently that's twice where I was as of July. I tried to really push through on that in November but didn't hit my stride until near the end.

Now I switch back to "The Enthrallers" for a little while. I have a first draft of the next chapter to revise. 

Then maybe I switch back, get through that last 20%, and get ready to start querying. That's what the December holidays are for, right? That might be over-ambitious.

### Otherwise

I had my first physical in a long while. It didn't tell me anything I didn't already know, which is probably a good thing.

I bought a coffee roasting machine. The Whirley-Pop just wasn't cutting it. It made awful grating noises and the mechanism would jam up all the time, and the results were suffering. It feels a little less DIY to use a roasting machine, but this isn't a "set it and forget it" kind of machine. You still actively monitor and adjust multiple variables as it roasts the beans. The results are already better and a lot more consistent.

Recently I played Disco Elysium, which I enjoyed a ton and highly recommend. It's a detective RPG, and the core mechanic is that you walk around a town talking to people. Something you learn in conversation might allow you to go back to someone you already talked to and unlock more dialog options. But also party to these conversations are various voices inside the protagonist's head. Things like empathy and rhetoric, and much weirder impulses. Those are also the skills you level up in. The dialog--internal and external--is often hilarious.
