---
title: "CyberSoc | Cyber Detective CTF Write Up — Evidence Investigation"
author: "Levent Durdalı"
date: 2022-01-27T02:32:23.929+0000
last_modified_at: 2022-02-14T15:16:31.926+0000
categories: ""
tags: ["osint","ctf","quiz","investigation"]
description: "OSINT-focused CTF Challenges. OSINT in Goverment, Stego, Crypto multiple languages, WIFI, EXIF and more"
image:
  path: /assets/935971c5542d/1*BULOYIeo6R7QIIqXY0H0aA.png
---

### CyberSoc \| Cyber Detective CTF Write Up — Evidence Investigation

[Cyber Detective CTF](https://ctf.cybersoc.wales/) is an OSINT\-focused CTF created by the Cyber Society at Cardiff University\. There are 40 challenges across 3 categories: General Knowledge, Life Online and **Evidence Investigation** \.

**Evidence Investigation** Progress: 18/18 — Fully Complete


> Lastly, English is not my native language\. So, I apologise for any mistakes that I might do\. 




### Let's start


![Question 1 — dvla](assets/935971c5542d/1*nVte2nd0j6aOHUkmiSWf2w.png)

Question 1 — dvla

Here is the image,


![That's definitely a Ford Focus or KA](assets/935971c5542d/1*j0pIC-HmxBfXMHs3oDuTfw.png)

That's definitely a Ford Focus or KA

Well, since I already know the Brand and Model of the car\. I started searching the plate\. I googled the plate and clicked the first [site](https://www.regit.cars/car/cy10hhb/interested) \.


![Yey, I guessed the Ford Kar part :\)](assets/935971c5542d/1*OCTb61WmUWLwfqj8OGU4rw.png)

Yey, I guessed the Ford Kar part :\)


![Question 2 — connectionrefused](assets/935971c5542d/1*Hx59omOnVJGQOHt8DNXO6g.png)

Question 2 — connectionrefused

So I tried opening the site, but it failed, so since it says it was accessible 4 years ago, let's go to [web\.archive\.org](http://web.archive.org) \. Here there were multiple snap\-shots, so I checked them all\. One of them leads to the answer\.


![](assets/935971c5542d/1*DNCO2DD_-iFnJHNNPEYXPg.png)



![Doctor Who?](assets/935971c5542d/1*lxqa4tpkDxvKxVPr3w7UHw.png)

Doctor Who?


![Question 3 — chemtrails](assets/935971c5542d/1*Oi3ZkOPIJzNA0n9HxzcEVw.png)

Question 3 — chemtrails

Here is the image,


![Cool](assets/935971c5542d/1*BULOYIeo6R7QIIqXY0H0aA.png)

Cool

Simply search online barcode scanner/orc opened the first [link,](https://online-barcode-reader.inliteresearch.com/) and boom\.


![Nice](assets/935971c5542d/1*XNyaGLX0wQI7HmHRUcHO5Q.png)

Nice


![Question 4 — bigbrother](assets/935971c5542d/1*dnmTKXFT5kpewu6sAaaMsA.png)

Question 4 — bigbrother

So, the IP doesn't work, or it was not active when I checked it\. Because of this found an old write up and took the image to solve it :\(


![I wished I could see it myself\.](assets/935971c5542d/1*F7JDoEu-xDgofjWfHWhi8g.png)

I wished I could see it myself\.

It's definitely Europe\. I was going to crop the image but got lazy and started reverse image search\.


![Thanks, [Yandex](https://yandex.com/images/search?rpt=imageview&url=https%3A%2F%2Favatars.mds.yandex.net%2Fget-images-cbir%2F1648143%2FpBDJWCb6iXip-QaIijkbwA7400%2Forig&cbir_id=1648143%2FpBDJWCb6iXip-QaIijkbwA7400)](assets/935971c5542d/1*zUenrfWtgB_IPkTpKZpcaQ.png)

Thanks, [Yandex](https://yandex.com/images/search?rpt=imageview&url=https%3A%2F%2Favatars.mds.yandex.net%2Fget-images-cbir%2F1648143%2FpBDJWCb6iXip-QaIijkbwA7400%2Forig&cbir_id=1648143%2FpBDJWCb6iXip-QaIijkbwA7400)

It's Belgium\.


![Question 5 — balencethebooks](assets/935971c5542d/1*VIMonLXIBXTFhC0F9q8Wrw.png)

Question 5 — balencethebooks

As a non\-British person, this was very weird to solve\. I searched TECHNOLOGY SERVICES LIMITED and started clicking all the links\. Then found this bizarre [site](https://find-and-update.company-information.service.gov.uk/company/01867162) \. Fake Government site? I don't know\. `find-and-update.company-information.service.gov.uk` Just look at that domain\. Wow


![Hmm](assets/935971c5542d/1*-3o_OJe0QJ1vdPbKkj_4DA.png)

Hmm

Anyhow, at this point, I'm still aimlessly clicking things…\. Then I saw "Filing History", huh\. Okay, that could be nice\.


![Nice](assets/935971c5542d/1*zmobQF7HS7GfT64FreAm9g.png)

Nice

So, again started clicking on all the links that sad **"full accounts"\.** Here's a peek\.


![Cool stuff](assets/935971c5542d/1*1xnu-dYod6UWUVvyf-hCZg.png)

Cool stuff

Then, I started trying all the numbers that were labelled **"Cash at Bank"\.** Eventually, I got it right, but I have no know idea which document or column ı used :\(


![Question 6 — readyfortakeoff](assets/935971c5542d/1*h4co19jqbhwLp80DAScUgA.png)

Question 6 — readyfortakeoff

Here is the Image that they gave,


![Bornholm Airport](assets/935971c5542d/1*4_86rcCBqhwh4oXbvt48Bg.jpeg)

Bornholm Airport

So, I solved this purely by chance\. My original idea was to find a free, archival flight history site\. But all the free sites let you search a couple of months back\. So I figured since these flight times should be mostly the same on different dates\. I simply tried every first flight time of arrival at destination\. The sites I used were,
- [https://airportinfo\.live/arrivals/rnn/airport\-ronne\-bornholm\-ronne](https://airportinfo.live/arrivals/rnn/airport-ronne-bornholm-ronne)
- [https://www\.radarbox\.com/data/airports/EKRN?tab=departures](https://www.radarbox.com/data/airports/EKRN?tab=departures)
- [https://www\.flightstats\.com/v2/flight\-tracker/departures/RNN/?year=2022&month=1&date=25&hour=6](https://www.flightstats.com/v2/flight-tracker/departures/RNN/?year=2022&month=1&date=25&hour=6)


And I found the answer on my 4th try, the earliest departure time I saw was 06:15, and according to that flight data, it arrived at its intended destination at 06:55, which was the answer\.


![Question 7 — inplainsight](assets/935971c5542d/1*3en4uaPZ8LIgYeu8aFfNvw.png)

Question 7 — inplainsight

Firstly the link doesn't work, so I have to find my own tool for this\. I used my trusted site for this one [https://aperisolve\.fr/](https://aperisolve.fr/) but couldn't find the text, so I tried another tool\.


![Question 8— gunpowder](assets/935971c5542d/1*gxhIdOOf2_iwqTXGhhVuuQ.png)

Question 8— gunpowder

The link doesn't work, sadly, so here is the image,


![Nice](assets/935971c5542d/1*ETHS44yBXLfns2TwSpreDQ.png)

Nice

So the first thing I checked wasn't the loft name but that tower silhouette\. I opened a random [blog](https://art-facts.com/famous-towers-in-the-world/) about the most famous towers in the world\. And found that CN Tower seems like a close match\. So let's search Toronto\.


![Cool](assets/935971c5542d/1*q-SXNiv7qbw3rzPmQp9lcw.png)

Cool

So there are a few weird results, but [result](https://www.google.com/maps/search/birchmount+lofts+Toronto/@43.7438623,-79.3225952,13z) s 1, 2, 5 and 8 are on the same road\. Which is **Birchmount Rd\.** this is our answer\.


![Cool](assets/935971c5542d/1*P4NWVqms5mA5gax8VLnL_w.png)

Cool


![Question 9 — sos](assets/935971c5542d/1*Xmcwe0c-PKCgVRaxNy-UYQ.png)

Question 9 — sos

Here is the text,


![Medium's text formatting is terrible](assets/935971c5542d/1*utrA784VhyM6rKhgLSLulA.png)

Medium's text formatting is terrible

Well, that's just Morse code \(used [dCode](https://www.dcode.fr/morse-code) \)


![GOLDENEAGLE is our answer](assets/935971c5542d/1*tk_E6HjPV_ssr-RuIch0Dg.png)

GOLDENEAGLE is our answer


![Question 10 — rollingeyes, Wow that's long](assets/935971c5542d/1*CwGa63BTfGcnGRr6KpTkxA.png)

Question 10 — rollingeyes, Wow that's long

Here is the image,


![That's probably Britain](assets/935971c5542d/1*JbjN71b42ixG13Pi_3129Q.jpeg)

That's probably Britain

I simply searched Poppy\-n\-pals pet care service, and the first result was correct\.


![yey](assets/935971c5542d/1*-FN0zdcdvyN9Uls1fsEt1w.png)

yey

I don't get how we are supposed to solve this one, but my thought process was this: Check the rode in the dead centre of the image\. And that road is Amherst Cres,


![Pure Luck](assets/935971c5542d/1*To892MIzSNaAEI3mvBelDQ.png)

Pure Luck

The first random place I picked has this dude, and I immediately tried it, and it worked\.


![Question 11 — proofinthesignal](assets/935971c5542d/1*AOGm4BUTpZ034IuE1DxT7g.png)

Question 11 — proofinthesignal

Well, I already knew about Wifi mapping sites, so I just used [Wiggle](https://www.wigle.net/) ,


![](assets/935971c5542d/1*yjNoYo3Xfbj9DGnqhQAzSA.png)



![Wiggle \-> Bristol](assets/935971c5542d/1*wneMLLxFM3Fe0GqJ2AAuPw.png)

Wiggle \-> Bristol

From the map on the right, we can find two "jammy" markers on St Marks Road\.


![Question 12 — undercover](assets/935971c5542d/1*Cg-mbvZMc_UPHY3d2zxdGA.png)

Question 12 — undercover

I'm going to be honest this was the dumbest question yet, or I'm very dumb can't decide\. I tried lots of tools to analyze this given blank pdf file\.

Can be seen here,


![NOT EMPTY lol](assets/935971c5542d/1*bKU32rf8HJ3tE46pA2N07g.png)

NOT EMPTY lol

After a while got bored and started randomly clicking on the blank page until something was selected\.


![White text inside the PDF](assets/935971c5542d/1*2eM0jyPMhHQhtiEz6zfyVQ.png)

White text inside the PDF

The text was Lock Code: 956445


![Question 13 — defrauded, So long wow](assets/935971c5542d/1*e3iaaXxv_d7pU4LKPy-jxQ.png)

Question 13 — defrauded, So long wow

Here is the given pdf file,


![Hmm](assets/935971c5542d/1*NgJIwCV0vmgoL2Pr4WfILw.png)

Hmm

Well, this one is probably the most straightforward question yet\. Z\-Zip said the file was modified in 2012, but the pdf said it was 2020\. So I just used 13/05/2012, and it worked\.


![yey 7\-Zip](assets/935971c5542d/1*xoEC7A8t96zQvgsaeYDN2g.png)

yey 7\-Zip


![Question 14 — photophile](assets/935971c5542d/1*CZidDSfC8GMfOkjpnMOX4w.png)

Question 14 — photophile

This question is about EXIF, using my trusted EXIF [site](https://exifdata.com/exif.php) \. We can see a Motorola Moto G3 Camera took this photo\.


![Nice](assets/935971c5542d/1*g6MvMFoX3taKz_9atK-aJQ.png)

Nice


![Question 15 — xorrelase, Cool Question](assets/935971c5542d/1*o3vMEIzOjBzJvrYNFR5o7A.png)

Question 15 — xorrelase, Cool Question

So, as an engineer, I know what XOR is, and since I also know how to use [CyberChef](https://gchq.github.io/CyberChef/CyberChef_v9.32.3.zip) , this was an easy question\.


![XOR Brute Force Panel](assets/935971c5542d/1*VAhpB3JqLVGpmsoiQ-T2KQ.png)

XOR Brute Force Panel

This XOR panel brute forces XOR combinations and give a list\.


![Key=1c](assets/935971c5542d/1*A5fxZln94T293NRCcBOEEQ.png)

Key=1c

As you can see, the answer is MyStrongWiFi54\.


![Question 16 — mothertongue, Cool question](assets/935971c5542d/1*-uNAULMbJwuGNmlXjjwVYw.png)

Question 16 — mothertongue, Cool question

Here is the given text,


![Arabic maybe?](assets/935971c5542d/1*pk5ENlU-UdX3gsEtpkVQ-g.png)

Arabic maybe?

Well, It's not Arabic\. It's Pashto\. Very interesting\. But that's not the answer\. Hmm, weird\. Then, I saw multiple different texts\. Here are some,


![](assets/935971c5542d/1*5grrIv_-Wet1T3YClVtuag.png)



![](assets/935971c5542d/1*9ru1L_OK4HRb97uHH63gUQ.png)



![](assets/935971c5542d/1*BsJ8g37wvt6rpd1_WCBw4A.png)



![Nice](assets/935971c5542d/1*-nUPa1h6iydMbxtY5mqPqg.png)

Nice

After this, I figured there must be some special word for the answer\. After painfully removing Pashto, these 6 sentences were left, and the last one is the answer\. It translates to **Clouds\.**


![These ones](assets/935971c5542d/1*0QuUD5b6ZTyxdF88220KZg.png)

These ones


![Question 17— hostiletakeover, So long](assets/935971c5542d/1*dSODQED68yq1QJ9PEa8CzA.png)

Question 17— hostiletakeover, So long

Here is the given PDF file,


![Hmm](assets/935971c5542d/1*ntQBPBYH7DQW5BzP6Qm9PA.png)

Hmm

Well, after googling Land Registry, I came to this site


![Hmm](assets/935971c5542d/1*sy0BUdlJ9hquVrlIzD62dg.png)

Hmm

It wasn't really helpful, or I couldn't use it, I don't know\. After this, I found this other page from the sites search function\.


![Hmm](assets/935971c5542d/1*bs53jNrFoLud70CG8bNzog.png)

Hmm

That site leads to this search engine,


![](assets/935971c5542d/1*8Fqdj7VNVW_fDO1k7WG9rA.png)


Here I set the amount paid to £20\.000\.00, don't ask why\. And set the dates to match the date given in the Bank Statement \(1 month before is September\), but I couldn't be sure if this would be correct so, I set the end date as 31 October just to be sure\. In the end, this gave me about 70 answers\.

Time to learn Welsh city names, I guess\. I'll skip this part, but in the end, there were two possible answers, so I tried them both\. Tesco was the answer\.


![](assets/935971c5542d/1*X1_bOC6YRDvbuqYYH-0WRQ.png)



![Cool Site](assets/935971c5542d/1*mWX3qIm0J11OgCm2lBjpVA.png)

Cool Site

I have to say\. This question was very hard\.
### The last question


![](assets/935971c5542d/1*9B3_czCnA9RAEGVHXFhFFw.png)



![Question 18 — bitcoinbuster, Longest question wow](assets/935971c5542d/1*R_9DxiYfywjzj_ubrDYLPw.png)

Question 18 — bitcoinbuster, Longest question wow

Here is the given HTML file,


![Cool](assets/935971c5542d/1*3aSysE0sDxWxw9EsodzLjw.png)

Cool

So let's open all the links and set the dates to 1st Feb 2020\. Here is one as an [example](https://finance.yahoo.com/quote/BTC-USD/history?period1=1580515200&period2=1580515200&interval=1d&filter=history&frequency=1d&includeAdjustedClose=true) ,


![Buy High, Sell Low :\)](assets/935971c5542d/1*I9oIfPhpQ6Ajp9eroaDcWA.png)

Buy High, Sell Low :\)


> Note: the site uses the same query so just copied this query for every currency xxxxxxxxxx/history?period1=1580515200&period2=1580515200&interval=1d&filter=history&frequency=1d&includeAdjustedClose=true 





Now, multiply every currency's Open price with 3\.581074451254057 to see if it makes any nice numbers :\)


![Yey](assets/935971c5542d/1*EEEaLfrXImmc_dTUbpwkwg.png)

Yey

AUD \(Australian Dollar\)was the answer, as seen above\.

Well, that was the end of **Cyber Detective CTF\. Completion 39/40**

Thank you, Cyber Society of Cardiff University, for this amazing CTF\. Since I finished this one, I'll be doing [Cyber Investigator CTF](https://investigator.cybersoc.wales/) in the future\.



_[Post](https://medium.com/@leventd/cybersoc-cyber-detective-ctf-write-up-evidence-investigation-935971c5542d) converted from Medium by [ZMediumToMarkdown](https://github.com/ZhgChgLi/ZMediumToMarkdown)._
