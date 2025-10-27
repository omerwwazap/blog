---
layout: post
title: Simply GeoEstimation — OSINT Challenge 13
date: 2022-05-14 12:00 +0200
categories: [OSINT, Geolocation]
tags: [English, Academic]     # TAG names should always be lowercase
img_path: /images/2022GeoEstimation
image:
  path: /0.webp
  alt: Simply GeoEstimation
---

# OSINT with GeoEstimation

On Dec 20, 2021, OSINT Dojo shared an OSINT quiz with us. The objective was simple. We had to determine where the photo was taken and their final destination. Please refer to the embedded link below for the original post:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">As my hands were a bit busy at the time, Mrs. Win took the photo for this week&#39;s <a href="https://twitter.com/hashtag/OSINT?src=hash&amp;ref_src=twsrc%5Etfw">#OSINT</a> challenge. See if you can answer the following questions:<br><br>Lat/Long where the photo was taken<br>Our final destination <a href="https://t.co/eGws2uz7fH">pic.twitter.com/eGws2uz7fH</a></p>&mdash; OSINT Dojo (@OSINTDojo) <a href="https://twitter.com/OSINTDojo/status/1472933510696484869?ref_src=twsrc%5Etfw">December 20, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

Don’t read any further if you’d like to test your geolocation skills. Open the picture and give it a try. Don’t scroll further down as I will be discussing how I found it and since I just started this hobby, I’ll probably be doing this the long way around :)

> Lastly, English is not my native language. So, I apologise for any mistakes that I might make.

## Warning spoilers ahead

Since I knew reverse image won’t bring me anything useful, I used the first tool that got me into Geolocation. A tool/research called **Geoestimation** (more information can be found here **[GeoEstimation](https://github.com/TIBHannover/GeoEstimation)** Using that tool, I found some crucial information.

![Image](/0.webp) _Hmm_

Interestingly the tool believes it’s in Washington, USA.

![Image](/1.webp) _3 possible locations_

The tool is confident in that marked location but also has other guesses. So we should check the others as well. All those locations are marked in Google Maps below.

![Image](/2.webp) _Google Maps — [Link](https://www.google.com/maps/@47.5808552,-121.0431343,11z)_

So let’s check the roads close to the marked locations. And since the road in the image is curving very aggressively, we should be able to check every road here incredibly fast.

Also, the road seems to be a Highway, so we don’t need to check all the streets here.

![Image](/3.webp) _First Location to check_

But no roads here seem like the one on the image,

![Image](/4.webp) _Sad_

The second location to check,

![Image](/5.webp) _Google Maps — [Link](https://www.google.com/maps/@47.7275882,-121.1192223,12.75z)_

So let’s check the red markers I put. (The blue marker was too far away from the original location.)

WHOA. We actually found it. The lowest marked place on the image was the correct location.

![Image](/6.webp) _Cool — Link_

As you can see, we found the location.

![Image](/7.webp) _Yey_

> The location: 47.71668013192945, -121.12567364527123
{: .prompt-tip }

As a recap, I couldn’t have solved this question without the [Geoestimation](https://github.com/TIBHannover/GeoEstimation) (more information can be found here GeoEstimation) tool. Thanks to it, I found the general location, and the rest was basic resigning.

Thank you, [OSINTDojo](https://www.osintdojo.com/), for the questions. I’ll be randomly picking questions from your Twitter and solving them from now on.
