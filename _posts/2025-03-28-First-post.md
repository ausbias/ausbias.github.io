---
layout: post
title:  "The AusBIAS Logo"
date:   2025-03-28
categories: [news, updates]
author: Lachlan Whitehead
bsky: "https://bsky.app/profile/drlachie.bsky.social"
---

### What's a society without a logo? 

When we first decided we needed a website, the first question was obviously: what should our logo be. 

At first I wanted something quickly, and took the obvious route of paying homage (shamelessly plagiarising) the GloBIAS Logo:

![Globias Logo](/assets/images/globias_logo.png){: height="200" }

In a fit of ... what's the opposite of creatitvity... I created this monstrosity: 
![Original Ausbias Logo](/assets/images/old_logo_DoNotUse.png){: height="150" }


My thoughts were: 

- change the colours to "Aussie it up a bit" 
- highlight the bottom right, where we usually appear on a map of the world. 


After all this, I decided it was best to actually ask permission from the GloBIAS organising committee and, while flattered, they were somewhat concerned about protecting their brand now that they're a legal entity. This was entirely justified so back to the drawing board for me.

Next I looked at the Neubias logo: 

![Neubias Logo](/assets/images/neubias_logo.png){: height="200" }

Well I liked the look of the network there, so that's where I started tinkering. 

I liked the idea of the ![napari logo](https://napari.org/dev/naps/5-new-logo.html) being completely defined in python, so thought I could follow their lead. First - I found a csv file with the latitude and longitude of the major cities in Australia, including their populations. Then wrote a script to put a propotionally population sized dot on each and connect them with lines.

![Australia with striaght lines connecting population centers](/assets/images/straight_lines.png){: height="300" }

That was cool and all, but as I had scaled the cities to the population, why not do the same with the lines? 

![Getting closer](/assets/images/scale_lines.png){: height="300" }

I still wasn't happy so decided to curve the lines, and add a colour map: 

![Almost there...](/assets/images/almost_final.png){: height="300" }

That was it. Thought to make it more abstract I'd remove the coastline, had a design-minded friend (thanks Michael) help chose a font and the rest is (extremely recent) history:

![Ausbias Final Logo](/assets/images/banner_logo.png){: height="300" }

If you want to generate the logo yourself, all the code is in [our github](https://github.com/ausbias/ausbias.github.io/tree/main/logo_stuff)! 

Fun trivia: the logo initially included Geelong, but not Canberra. It was pointed out that while we do have members who work and reside in Geelong, missing our nation's capital was perhaps sub-optimal. 
