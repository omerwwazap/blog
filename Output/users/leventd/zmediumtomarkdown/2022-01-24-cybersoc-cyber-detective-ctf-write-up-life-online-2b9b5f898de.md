---
title: "CyberSoc | Cyber Detective CTF Write Up — Life Online"
author: "Levent Durdalı"
date: 2022-01-24T14:32:55.920+0000
last_modified_at: 2022-01-31T16:45:03.045+0000
categories: ""
tags: ["osint","ctf","quiz","investigation"]
description: "OSINT-focused CTF Challenges. OSINT in Twitter, Stego, Crypto and more"
image:
  path: /assets/2b9b5f898de/1*wiQPHzWoG3UZYs54JYz3ww.png
---

### CyberSoc \| Cyber Detective CTF Write Up — Life Online

[Cyber Detective CTF](https://ctf.cybersoc.wales/) is an OSINT\-focused CTF created by the Cyber Society at Cardiff University\. There are 40 challenges across 3 categories: General Knowledge, **Life Online** and Evidence Investigation\.

**Life Online** Progress: 11/12 \(11/11\)


> Note: **leaveamessage** can't be solved as the twitter account need for the question is suspended and I can’t seem to find any archives of the profile\. 




### Let’s start


![Question 1 — voteforme](assets/2b9b5f898de/1*oK5a4w2fAFhq_-SXSdsC3A.png)

Question 1 — voteforme


![Hello James](assets/2b9b5f898de/1*wiQPHzWoG3UZYs54JYz3ww.png)

Hello James

Lets scroll down to see if we can anything about a political party?


![James could to be a Democrat](assets/2b9b5f898de/1*jjr0TLx46XIgRHmka2OxpQ.png)

James could to be a Democrat


![Question 2 — growingup](assets/2b9b5f898de/1*0qqXW5u2Jl1xiwykSxlroA.png)

Question 2 — growingup

His other tweets doesn't have any information so it's probably the thing in his bio


![This abomination](assets/2b9b5f898de/1*FDAaGazoItkqr3Fs71IGFg.png)

This abomination

So I found this by googling “///push\.asking\.barn” apparently it’s from a site called [what3words](https://what3words.com/push.asking.barn) \. If you couldn't find it by google, check his tweets carefully apparently he tweeted about this\. Oh an the answer is York\.


![Hello York](assets/2b9b5f898de/1*3Djhonm4e6MZ9NHPUqCLHw.png)

Hello York


![Question 3— choochoo, Okey?](assets/2b9b5f898de/1*qBLIoUsBJGGqrLdxycVnMg.png)

Question 3— choochoo, Okey?

James posted a train station saying getting off this afternoon so it highly likely that this is the city he work at\.


![Cardiff](assets/2b9b5f898de/1*TU62vR1U4ZoVcTTftecOvw.png)

Cardiff

Yes it was\. Cardiff


![Question 4 — suntan](assets/2b9b5f898de/1*DCoU4G3KcZK4TBO5XOlKzQ.png)

Question 4 — suntan

So, we need to find Sarah first\. Since I don't remember seeing Sarah in James’s tweets I started checking James Likes, and boom found her\.


![Nice Place](assets/2b9b5f898de/1*og4VXBLL966vPkephNiYXw.png)

Nice Place

Simple reverse image search brings, Elizabeth Quay which is in Perth, Australia\.


![Nice Place](assets/2b9b5f898de/1*KI6dEYfLXlOJ66PuEwpFqg.png)

Nice Place


![Question 5 — wagthetail](assets/2b9b5f898de/1*lJ8PJ2an3DVKifwVdFYynA.png)

Question 5 — wagthetail

First place I looked was her bio and found some coordinate for Buster’s favorite place \(probably her dog\)


![I too should do a postgrad](assets/2b9b5f898de/1*kjqSum1joRtKaeYUmcKRgQ.png)

I too should do a postgrad

IT’s 2 Bridge St, **Brecon** LD3 8AH, UK\. according to google\.


![Nice](assets/2b9b5f898de/1*eAAoEq8hNCQEtxrZ-1E2cA.png)

Nice


![Question 6 — narcissism](assets/2b9b5f898de/1*-6-0A_BdRIBmae53-msSRA.png)

Question 6 — narcissism

So I found this George guy from James “Replies” page


![Happy George](assets/2b9b5f898de/1*chWF06UkmjT7pxo-0wyl7A.png)

Happy George

I first tried the Code in the tweet above but it didn't work, so back to searching\.


![Oh you silly boy](assets/2b9b5f898de/1*MGqbCVkKhXwn4pFRXckiWw.png)

Oh you silly boy

This looks awful like “Base64” encoding\. Decoding it with my personal favorite tools\. [https://gchq\.github\.io/CyberChef/](https://gchq.github.io/CyberChef/) and [https://www\.dcode\.fr/cipher\-identifier](https://www.dcode.fr/cipher-identifier) \(this identifier is amazing\) Okey, let’s use dCode even though I'm %100 sure that's Base64\.


![dCode also believes this is Base64 encoding\. Yey](assets/2b9b5f898de/1*IwtXv_SYQ7BVujjNR5OGRA.png)

dCode also believes this is Base64 encoding\. Yey


![Cool password\.](assets/2b9b5f898de/1*JRXFewdgb_PXsiGBGrAuZg.png)

Cool password\.


![Question 7— proppedup](assets/2b9b5f898de/1*Bi5LUxMGsdUK9qouuof_UQ.png)

Question 7— proppedup

I haven’t seen any desks in James or Sarah’s tweets so let's look at Georges tweets\.


![Hmm\. Okey](assets/2b9b5f898de/1*5IImSW2LHcgxZ2701coCXg.png)

Hmm\. Okey

Well we found another person of interest\. Yey for us\. Anyways the answer is: **brown grey**


![Question 8 — bluengreen](assets/2b9b5f898de/1*4LlNDItyENm6sasxjo8V_Q.png)

Question 8 — bluengreen

To be honest this took me way to long, like more than 15 minutes\. To solve this you go here,


![So very sad](assets/2b9b5f898de/1*ek-ncCjJut2oZc1fp0piJw.png)

So very sad

You see that very small black **“u”** looking character behind the avatar, well here it is\. Oh and that's the answer\.


![Yeah me too :\(](assets/2b9b5f898de/1*seCkCkNLnrbXAittxuwdkQ.png)

Yeah me too :\(


![Question 9 — clockingout](assets/2b9b5f898de/1*bjDsB3bwKGoPL3OnXS9Khw.png)

Question 9 — clockingout

So I tried so much stuff here and at first I couldn't find it\. AFter I finnesd this section of the ctf and came back\. The first thing I noticed was, this tweet\.


![](assets/2b9b5f898de/1*1RjqbVo6LjnlKLhbWGJ_mg.png)


As you can see, James actually gave us everything we needed to solve this question\. With this tweet, we know how long he works and the time he got off work\.

So, is it simply “1:00 AM minus 8 hours of work = Answer” Not quite, because Twitter actually shows 1:00AM for **MY local time** not UK Time, and since I’m not in the UK Time zone, I’LL need to do some adjustments\.

Using sites like [timebie](http://www.timebie.com/timezone/istanbullondon.php) , we can see that 1:00AM my local time is 10:00PM UK Time\(previuoıs day\) \. So, minus 8 hours of work is gives us 5:00PM my local time which is **2:00PM UK Time\. The answer is 2:00**


![Question 10 — meme](assets/2b9b5f898de/1*EjmzWGW8krUMeN12n7Sqpg.png)

Question 10 — meme

So I already found the meme with a code in it so I just tried that and it worked\. \(You can see it couple question above\)


![Question 11 — partytime](assets/2b9b5f898de/1*KDtLMrJCvMkqei_XRb501A.png)

Question 11 — partytime

So since I don’t remember any address from James, Sarah and George let's check Pearce’s tweets,


![Nice](assets/2b9b5f898de/1*Hnd16XkP6UmvfBf5ASzBgg.png)

Nice

Opened Google maps and found the routes, C1, 57, 58 and 52


![Nice](assets/2b9b5f898de/1*gcTp8afQTqj_7_aGFCFwcA.png)

Nice

Tried **57** first and it worked\.


![Question 12— leaveamessage](assets/2b9b5f898de/1*cXmu7gIo_CH8rb-UUwHA5w.png)

Question 12— leaveamessage

Looking at the tweet below we haven’t seen Sophjones77 so lets check that account\.


![**Where did you go jenmp7, where?**](assets/2b9b5f898de/1*3uzJedHufsTb3zRBmyIRGg.png)

**Where did you go jenmp7, where?**


![So sad](assets/2b9b5f898de/1*ZysFOjLzqcnW6n7O_FZBFw.png)

So sad

Uhm, okey that's very sad\. Let’s look elsewhere\.


![](assets/2b9b5f898de/1*CcLcoSbidhHcLzl0LUwCWg.png)



![](assets/2b9b5f898de/1*Vtld0zThQBhzQxVpa4Pazw.png)


Found these guys, but I can’t be sure they’re related in anyway\.

So after searching for a while I found a previous write\-up about this question\. And yes **Sophjones77** was the correct account but since it's suspended I can't solve that question\.


![](assets/2b9b5f898de/1*km2W9v8SvbVytfdtqCr0vQ.png)



![**Sophjones77**](assets/2b9b5f898de/1*pUqUVHzMUZ6EmeZYlOBG8Q.png)

**Sophjones77**

Okey well since I have no way of solving the last question\. I’ll have to end this category for the CTF\.

But, before I end, the final category, **General Knowledge** is super basic stuff like “what does OSINT and HTTPS stand for” So, I won’t add them here\. But hey I still finished them :\)


![heheh\. Nice\.](assets/2b9b5f898de/1*8BWK29X2vw2_Nhtj5RgTMQ.png)

heheh\. Nice\.

Anyhow the first category was very fun to solve hope the next one is too\. After I finish the **Evidence Investigation category** i’ll try out this CTF [https://investigator\.cybersoc\.wales](https://investigator.cybersoc.wales/)



_[Post](https://medium.com/@leventd/cybersoc-cyber-detective-ctf-write-up-life-online-2b9b5f898de) converted from Medium by [ZMediumToMarkdown](https://github.com/ZhgChgLi/ZMediumToMarkdown)._
