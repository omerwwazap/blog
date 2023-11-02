---
layout: post
title: "CyberSoc | Cyber Detective CTF Write Up — Evidence Investigation"
date: 2022-01-27 12:00 +0200
categories: [Cyber Security, Walkthroughs]
tags: [English, CyberSoc]     # TAG names should always be lowercase
img_path: /images/2022CyberSoc1
image:
  path: /0.png
---

[Cyber Detective CTF](https://ctf.cybersoc.wales/) is an OSINT-focused CTF created by the Cyber Society at Cardiff University. There are 40 challenges across 3 categories: General Knowledge, Life Online and **Evidence Investigation**.

**Evidence Investigation** Progress: 18/18 — Fully Complete

# Let's start[^1]

![Question 1 — dvla](/1.png) _Question 1 — dvla_

Here is the image,

![That's definitely a Ford Focus or KA](/2.png) _That's definitely a Ford Focus or KA_

Well, since I already know the Brand and Model of the car. I started searching the plate. I googled the plate and clicked the first [site](https://www.regit.cars/car/cy10hhb/interested).

![Yey, I guessed the Ford car part :)](/3.png) _Yey, I guessed the Ford Kar part :)_

> Answer: Ford June
{: .prompt-tip }

## Question 2 — connectionrefused

![Question 2 — connectionrefused](/4.png)

So I tried opening the site, but it failed, so since it says it was accessible 4 years ago, let's go to [web.archive.org](http://web.archive.org) . Here there were multiple snap-shots, so I checked them all. One of them leads to the answer.

| ![Image](/5.png) | ![Doctor Who?](/6.png) |

<p style="text-align: center;"> Doctor Who?</p>

> Answer: IceCTF{Th3y’11_n3v4r_f1|\|d_m4h_fl3g_1n_th3_p45t}
{: .prompt-tip }

## Question 3 — chemtrails

![Question 3 — chemtrails](/7.png)

Here is the image,

![Cool](/0.png) _Cool_

Simply search online barcode scanner/orc opened the first [link,](https://online-barcode-reader.inliteresearch.com/) and boom.

![Nice](/XNyaGLX0wQI7HmHRUcHO5Q.png) _Nice_

> Answer: SEAT NUMBER: 22B
{: .prompt-tip }

## Question 4 — bigbrother

![Question 4 — bigbrother](/dnmTKXFT5kpewu6sAaaMsA.png)

So, the IP doesn't work, or it was not active when I checked it. Because of this found an old write up and took the image to solve it :(

![I wished I could see it myself.](/F7JDoEu-xDgofjWfHWhi8g.png)

I wished I could see it myself.

It's definitely Europe. I was going to crop the image but got lazy and started reverse image search.

![Thanks, [Yandex](https://yandex.com/images/search?rpt=imageview&url=https%3A%2F%2Favatars.mds.yandex.net%2Fget-images-cbir%2F1648143%2FpBDJWCb6iXip-QaIijkbwA7400%2Forig&cbir_id=1648143%2FpBDJWCb6iXip-QaIijkbwA7400)](/zUenrfWtgB_IPkTpKZpcaQ.png)

Thanks, [Yandex](https://yandex.com/images/search?rpt=imageview&url=https%3A%2F%2Favatars.mds.yandex.net%2Fget-images-cbir%2F1648143%2FpBDJWCb6iXip-QaIijkbwA7400%2Forig&cbir_id=1648143%2FpBDJWCb6iXip-QaIijkbwA7400)

> Answer: Belgium
{: .prompt-tip }

## Question 5 — balencethebooks

![Question 5 — balencethebooks](/VIMonLXIBXTFhC0F9q8Wrw.png)

As a non-British person, this was very weird to solve. I searched TECHNOLOGY SERVICES LIMITED and started clicking all the links. Then found this bizarre [site](https://find-and-update.company-information.service.gov.uk/company/01867162) . Fake Government site? I don't know. `find-and-update.company-information.service.gov.uk` Just look at that domain. Wow

![Hmm](/-3o_OJe0QJ1vdPbKkj_4DA.png) _Hmm_

Anyhow, at this point, I'm still aimlessly clicking things…. Then I saw "Filing History", huh. Okay, that could be nice.

![Nice](/zmobQF7HS7GfT64FreAm9g.png) _Nice_

So, again started clicking on all the links that sad **"full accounts"** Here's a peek.

![Cool stuff](/1xnu-dYod6UWUVvyf-hCZg.png) _Cool stuff_

Then, I started trying all the numbers that were labelled **"Cash at Bank"** Eventually, I got it right, but I have no know idea which document or column ı used :(

> Answer: Cash at Bank
{: .prompt-tip }

## Question 6 — readyfortakeoff

![Question 6 — readyfortakeoff](/h4co19jqbhwLp80DAScUgA.png)

Here is the Image that they gave,

![Bornholm Airport](/4_86rcCBqhwh4oXbvt48Bg.jpeg) _Bornholm Airport_

So, I solved this purely by chance. My original idea was to find a free, archival flight history site. But all the free sites let you search a couple of months back. So I figured since these flight times should be mostly the same on different dates. I simply tried every first flight time of arrival at destination. The sites I used were,

- [https://airportinfo.live/arrivals/rnn/airport-ronne-bornholm-ronne](https://airportinfo.live/arrivals/rnn/airport-ronne-bornholm-ronne)
- [https://www.radarbox.com/data/airports/EKRN?tab=departures](https://www.radarbox.com/data/airports/EKRN?tab=departures)
- [https://www.flightstats.com/v2/flight-tracker/departures/RNN/?year=2022&month=1&date=25&hour=6](https://www.flightstats.com/v2/flight-tracker/departures/RNN/?year=2022&month=1&date=25&hour=6)

And I found the answer on my 4th try, the earliest departure time I saw was 06:15, and according to that flight data, it arrived at its intended destination at 06:55, which was the answer.

> Answer: 06:55
{: .prompt-tip }

## Question 7 — inplainsight

![Question 7 — inplainsight](/3en4uaPZ8LIgYeu8aFfNvw.png)

Firstly the link doesn't work, so I have to find my own tool for this. I used my trusted site for this one [https://aperisolve.fr/](https://aperisolve.fr/) but couldn't find the text, so I skipped this question.

![Question 8— gunpowder](/gxhIdOOf2_iwqTXGhhVuuQ.png)

## Question 8— gunpowder

The link doesn't work, sadly, so here is the image,

![Nice](/ETHS44yBXLfns2TwSpreDQ.png) _Nice_

So the first thing I checked wasn't the loft name but that tower silhouette. I opened a random [blog](https://art-facts.com/famous-towers-in-the-world/) about the most famous towers in the world. And found that CN Tower seems like a close match. So let's search Toronto.

![Cool](/q-SXNiv7qbw3rzPmQp9lcw.png) _Cool_

So there are a few weird results, but [result](https://www.google.com/maps/search/birchmount+lofts+Toronto/@43.7438623,-79.3225952,13z) s 1, 2, 5 and 8 are on the same road. Which is **Birchmount Rd.** this is our answer.

![Cool](/P4NWVqms5mA5gax8VLnL_w.png) _Cool_

> Answer: Birchmount Rd
{: .prompt-tip }

## Question 9 — sos

![Question 9 — sos](/Xmcwe0c-PKCgVRaxNy-UYQ.png)

Here is the text,

![Image](/utrA784VhyM6rKhgLSLulA.png)

Well, that's just Morse code (used [dCode](https://www.dcode.fr/morse-code) )

![GOLDENEAGLE is our answer](/tk_E6HjPV_ssr-RuIch0Dg.png)

> Answer: GOLDENEAGLE
{: .prompt-tip }

## Question 10 — rollingeyes, Wow that's long

![Question 10 — rollingeyes, Wow that's long](/CwGa63BTfGcnGRr6KpTkxA.png)

Here is the image,

![That's probably Britain](/JbjN71b42ixG13Pi_3129Q.jpeg) _That's probably Britain_

I simply searched Poppy-n-pals pet care service, and the first result was correct.

![yey](/-FN0zdcdvyN9Uls1fsEt1w.png) _yey_

I don't get how we are supposed to solve this one, but my thought process was this: Check the rode in the dead centre of the image. And that road is Amherst Cres,

![Pure Luck](/To892MIzSNaAEI3mvBelDQ.png) _Pure Luck_

The first random place I picked has this dude, and I immediately tried it, and it worked.

> Answer: Amherst Cres
{: .prompt-tip }

## Question 11 — proofinthesignal

![Question 11 — proofinthesignal](/AOGm4BUTpZ034IuE1DxT7g.png)

Well, I already knew about Wifi mapping sites, so I just used [Wiggle](https://www.wigle.net/) ,

| ![Image](/yjNoYo3Xfbj9DGnqhQAzSA.png) | ![Wiggle -> Bristol](/wneMLLxFM3Fe0GqJ2AAuPw.png) |

<p style="text-align: center;"> Wiggle -> Bristol</p>

From the map on the right, we can find two "jammy" markers on St Marks Road.

> Answer: jammy
{: .prompt-tip }

## Question 12 — undercover

![Question 12 — undercover](/Cg-mbvZMc_UPHY3d2zxdGA.png)

I'm going to be honest this was the dumbest question yet, or I'm very dumb can't decide. I tried lots of tools to analyze this given blank pdf file.

Can be seen here,

![NOT EMPTY lol](/bKU32rf8HJ3tE46pA2N07g.png) _NOT EMPTY lol_

After a while got bored and started randomly clicking on the blank page until something was selected.

![White text inside the PDF](/2eM0jyPMhHQhtiEz6zfyVQ.png) _White text inside the PDF_

The text was Lock Code: 956445

> Answer: 956445
{: .prompt-tip }

## Question 13 — defrauded, So long wow

![Question 13 — defrauded, So long wow](/e3iaaXxv_d7pU4LKPy-jxQ.png)

Here is the given pdf file,

![Hmm](/NgJIwCV0vmgoL2Pr4WfILw.png) _Hmm_

Well, this one is probably the most straightforward question yet. Z-Zip said the file was modified in 2012, but the pdf said it was 2020. So I just used 13/05/2012, and it worked.

![yey 7-Zip](/xoEC7A8t96zQvgsaeYDN2g.png) _yey 7-Zip_

> Answer: 13/05/2012
{: .prompt-tip }

## Question 14 — photophile

![Question 14 — photophile](/CZidDSfC8GMfOkjpnMOX4w.png)

This question is about EXIF, using my trusted EXIF [site](https://exifdata.com/exif.php) . We can see a Motorola Moto G3 Camera took this photo.

![Nice](/g6MvMFoX3taKz_9atK-aJQ.png) _Nice_

> Answer: Motorola Moto G3
{: .prompt-tip }

## Question 15 — xorrelase, Cool Question

![Question 15 — xorrelase, Cool Question](/o3vMEIzOjBzJvrYNFR5o7A.png)

So, as an engineer, I know what XOR is, and since I also know how to use [CyberChef](https://gchq.github.io/CyberChef/CyberChef_v9.32.3.zip) , this was an easy question.

![XOR Brute Force Panel](/VAhpB3JqLVGpmsoiQ-T2KQ.png) _XOR Brute Force Panel_

This XOR panel brute forces XOR combinations and give a list.

![Key=1c](/A5fxZln94T293NRCcBOEEQ.png) _Key=1c_

As you can see, the answer is MyStrongWiFi54.

> Answer: MyStrongWiFi54
{: .prompt-tip }

## Question 16 — mothertongue, Cool question

![Question 16 — mothertongue, Cool question](/-uNAULMbJwuGNmlXjjwVYw.png)

Here is the given text,

![Arabic maybe?](/pk5ENlU-UdX3gsEtpkVQ-g.png) _Arabic maybe?_

Well, It's not Arabic. It's Pashto. Very interesting. But that's not the answer. Hmm, weird. Then, I saw multiple different texts. Here are some,

| ![Image](/5grrIv_-Wet1T3YClVtuag.png) | ![Image](/9ru1L_OK4HRb97uHH63gUQ.png) |
| ![Image](/BsJ8g37wvt6rpdWCBw4A.png) | ![Nice](/-nUPa1h6iydMbxtY5mqPqg.png) |

<p style="text-align: center;">Nice</p>

After this, I figured there must be some special word for the answer. After painfully removing Pashto, these 6 sentences were left, and the last one is the answer. It translates to **Clouds.**

![These ones](/0QuUD5b6ZTyxdF88220KZg.png) _These ones_

> Answer: Clouds
{: .prompt-tip }

## Question 17— hostiletakeover, So long

![Question 17— hostiletakeover, So long](/dSODQED68yq1QJ9PEa8CzA.png)

Here is the given PDF file,

![Hmm](/ntQBPBYH7DQW5BzP6Qm9PA.png) _Hmm_

Well, after googling Land Registry, I came to this site

![Hmm](/sy0BUdlJ9hquVrlIzD62dg.png) _Hmm_

It wasn't really helpful, or I couldn't use it, I don't know. After this, I found this other page from the sites search function.

![Hmm](/bs53jNrFoLud70CG8bNzog.png) _Hmm_

That site leads to this search engine,

![Image](/8Fqdj7VNVW_fDO1k7WG9rA.png)

Here I set the amount paid to £20.000.00, don't ask why. And set the dates to match the date given in the Bank Statement (1 month before is September), but I couldn't be sure if this would be correct so, I set the end date as 31 October just to be sure. In the end, this gave me about 70 answers.

Time to learn Welsh city names, I guess. I'll skip this part, but in the end, there were two possible answers, so I tried them both. Tesco was the answer.

| ![Image](/XbOC6YRDvbuqYYH-0WRQ.png) | ![Cool Site](/mWX3qIm0J11OgCm2lBjpVA.png)|

<p style="text-align: center;">Cool Site</p>

I have to say. This question was very hard.

> Answer: Tesco
{: .prompt-tip }

## The last question

### Question 18 — bitcoinbuster, Longest Question

![Image](/9B3_czCnA9RAEGVHXFhFFw.png)

![Question 18 — bitcoinbuster, Longest question wow](/R_9DxiYfywjzj_ubrDYLPw.png)

Here is the given HTML file,

![Cool](/3aSysE0sDxWxw9EsodzLjw.png) _Cool_

So let's open all the links and set the dates to 1st Feb 2020. Here is one as an [example](https://finance.yahoo.com/quote/BTC-USD/history?period1=1580515200&period2=1580515200&interval=1d&filter=history&frequency=1d&includeAdjustedClose=true) ,

![Buy High, Sell Low :)](/I9oIfPhpQ6Ajp9eroaDcWA.png) _Buy High, Sell Low :)_

> Note: the site uses the same query so just copied this query for every currency xxxxxxxxxx/history?period1=1580515200&period2=1580515200&interval=1d&filter=history&frequency=1d&includeAdjustedClose=true
{: .prompt-warning }

Now, multiply every currency's Open price with 3.581074451254057 to see if it makes any nice numbers :)

![Yey](/EEEaLfrXImmc_dTUbpwkwg.png) _Yey_

AUD (Australian Dollar)was the answer, as seen above.

> Answer: Australia
{: .prompt-tip }

---

**Well, that was the end of Cyber Detective CTF. Completion 39/40**

Thank you, Cyber Society of Cardiff University, for this amazing CTF. Since I finished this one, I'll be doing [Cyber Investigator CTF](https://investigator.cybersoc.wales/) in the future.

[^1]: [First published in my Medium](https://medium.com/@leventd/cybersoc-cyber-detective-ctf-write-up-evidence-investigation-935971c5542d)
