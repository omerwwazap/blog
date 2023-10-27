---
layout: post
title: Who Throws Away Canvassed Satellite Images? - OSINT Challenge 8 with Overpass Turbo
date: 2022-02-2 19:06 +0200
categories: [OSINT, Geolocation]
tags: [English, overpassturbo]     # TAG names should always be lowercase
img_path: /images/2022OSINTCH8
image:
  path: /0.jpeg
  alt: Who Throws Away Canvassed Satellite Images?
---

# OSINT with Overpass Turbo

On Jan 16, 2022, Quiztime (contributor @trbrtc) shared a new OSINT quiz with us. The objective was simple but cool. We had to figure out the location of these satellite images. So let's try to Locate the place. Please refer to the embedded link below for the original post:

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Here’s a <a href="https://twitter.com/hashtag/SundayQuiz?src=hash&amp;ref_src=twsrc%5Etfw">#SundayQuiz</a> for <a href="https://twitter.com/quiztime?ref_src=twsrc%5Etfw">@quiztime</a>. Someone at a New York City government building apparently threw away these canvassed satellite images. Who can find the locations they show? <a href="https://t.co/z9n1GUJmzd">pic.twitter.com/z9n1GUJmzd</a></p>&mdash; Christiaan Triebert (@trbrtc) <a href="https://twitter.com/trbrtc/status/1482793938989858819?ref_src=twsrc%5Etfw">January 16, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Don't read any further if you'd like to test your geolocation skills. Open the picture and give it a try. Don't scroll further down as I will be discussing how I found it and since I just started this hobby, ill probably be doing the long way around :)

> Note: At the very end, I try to find the second picture with Overpasss Turbo
{: .prompt-info }

Lastly, English is not my native language. So, I apologies for any mistakes that I might do.

> When I solved this Challenge, ChatGPT or similar tools were not available. So I had to manually code. 
> Thanks to ChatGPT you don't have to this anymore. Simply ask for what you want and till give you code and most of the time ill work right out the gate. Sometimes you might have tweak it a bit.
{: .prompt-danger }

## Warning spoilers ahead

As I always do, I started by doing a reverse image search (Google Lens and Yandex Image). Both results tell me that this is, in fact, Aerial Imagery, not Satellite Imagery (I knew something was off )

![Image](/1.webp) _Cool_

At this point, having found no matches on Yandex, Google or Bing, I thought of using **[Overpass Turbo](https://overpass-turbo.eu/)**, an API for **[OpenStreetMap](https://www.openstreetmap.org/)**. You can read this fantastic blog post from [NixIntel](https://nixintel.info/) on how to use it here (for Part-2). But first, I'll try to solve this without Overpass Turbo.

Anyway, let's start. Since the photos seemed like they were decently developed places, I searched "**Lake**" on all majorly populated areas in New York, as seen below,

![Image](/2.webp) _New York, New York_

If you are wondering why I'm checking New York, please read the quiz tweet. About 5 minutes later, I came across this Lake called **Indian Lake**.

![Image](/3.webp) _So many Lakes…_

And since I'm checking almost each lake one by one, when I zoomed in here, [I found the place](https://goo.gl/maps/c2G212xpCnUkzc2o7) I was looking for. (By the way, I'm not checking every lake there is, only the ones that have some river connected to it)

![Image](/4.webp) _Yey found it._

Okay, cool, I found the first image. So let's look at the other picture,

![Image](/5.webp) _Second Image_

While not, I'm not sure, I believe we can see some railways here (marked in orange), and the blue line should be a river. So, assuming this image is not incredibly old, and those railways are still intact, we can find this place by searching Train Stops/Depots, etc. And with a gut feeling, I started exploring places close to where I found the first image. (Normally, Overpass Turbo would make our life's so much easier, but I won't use it for now.)

Oh, and you might be asking, why would that mean there is a stop/depot? Well, it doesn't, but the right side of the image seems like an Industrial place, so I'm assuming there is a depot/stop near there.

![Image](/6.webp) _Orange Box marks our first image location — lake._

So, after I searched for "**Train**", I directly went to the nearest Train Station, "**Bordentown Station**" but it wasn't populated enough so, since they all should logically be connected, I went to "[Hamilton Station](https://goo.gl/maps/bSRZKbtiGhJ127xg7)" while following the line to see if it split anywhere.

![Image](/7.webp) _Cool_

Okay so, this place is more populated, but it isn't right. Having no great Ideas, I simply followed the railway. A couple of clicks later, I found the second place.

| ![Image](/8.webp) | ![Image](/9.webp) |

<p style="text-align: center;"> Cool it matches </p>

I was wrong about the long orange line (the one I marked) being a railway, but I correctly guessed that the orange box marker was a railway. (Now that I that think about it, both of them being railways was very stupid, lol)

| ![Image](/10.webp) | ![Image](/11.webp) |

<p style="text-align: center;"> The long orange line was, in fact, a Highway </p>

> Side Note: Even though Google, Yandex, and I assumed this to be an Ariel image, it still could be a satellite image.
> I will try to find the possible date these photos were taken some other time.
{: .prompt-info }

## Using Overpass Turbo

So since we know the place we are searching for is close to New York, we move the map to create a search area (by default, the visible map is the search area).

![Image](/12.webp) _Center New York on the map._

Okay, time for some codding. I had to read like 20 minutes worth of API documents, then realized that I could just [modify this query](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_API_by_Example#Banks_far_away_from_police_stations) to solve this question. Here are the documents I used,

- [Key:waterway](https://wiki.openstreetmap.org/wiki/Key:waterway?uselang=en-GB)
- [Banks far away from police stations](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_API_by_Example#Banks_far_away_from_police_stations)

After making the relevant changes to that Bank Query,

<script src="https://gist.github.com/omerwwazap/2d185957b0623c21f967c049a8f2a2ca.js"></script>
<p style="text-align: center;"> My Railways near Rivers Query</p>

Using that query gives this,

![Image](/13.webp) _Whoa it worked_

![Image](/14.webp) _OOO Cool_

![Image](/15.webp) _O0O Cool, it worked_

I have to say [Overpass Turbo](https://overpass-turbo.eu/), OpenStreetMap API is a fantastic tool but seems hard to learn. I'll try to use more from now on.

**Thank you, [Quiztime](https://twitter.com/quiztime), for the questions. I'll be randomly picking questions from your Twitter and solving them from now on.**
