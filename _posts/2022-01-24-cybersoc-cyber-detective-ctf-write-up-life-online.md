---
layout: post
title: "CyberSoc | Cyber Detective CTF Write Up — Life Online"
date: 2022-01-24 12:00 +0200
categories: [Cyber Security, Walkthroughs]
tags: [English, CyberSoc]     # TAG names should always be lowercase
img_path: /images/2022CyberSoc2
image:
  path: /wiQPHzWoG3UZYs54JYz3ww.png
---

[Cyber Detective CTF](https://ctf.cybersoc.wales/) is an OSINT-focused CTF created by the Cyber Society at Cardiff University. There are 40 challenges across 3 categories: General Knowledge, **Life Online** and Evidence Investigation.

**Life Online** Progress: 11/12 (11/11)

> Note: **leaveamessage** can't be solved as the twitter account need for the question is suspended and I can’t seem to find any archives of the profile.
{: .prompt-info }

# Let’s start[^1]

## Question 1 — voteforme

![Question 1 — voteforme](/oK5a4w2fAFhq_-SXSdsC3A.png)

![Hello James](/wiQPHzWoG3UZYs54JYz3ww.png) _Hello James_

Lets scroll down to see if we can anything about a political party?

![James could to be a Democrat](/jjr0TLx46XIgRHmka2OxpQ.png) _James could to be a Democrat_

> Answer: Democrat
{: .prompt-tip }

## Question 2 — growingup

![Question 2 — growingup](/0qqXW5u2Jl1xiwykSxlroA.png)

His other tweets doesn't have any information so it's probably the thing in his bio

![This abomination](/FDAaGazoItkqr3Fs71IGFg.png) _This abomination_

So I found this by googling “///push.asking.barn” apparently it’s from a site called [what3words](https://what3words.com/push.asking.barn) . If you couldn't find it by google, check his tweets carefully apparently he tweeted about this. Oh an the answer is York.

> Answer: York
{: .prompt-tip }

![Hello York](/3Djhonm4e6MZ9NHPUqCLHw.png) _Hello York_

## Question 3— choochoo, Okey?

![Question 3— choochoo, Okey?](/qBLIoUsBJGGqrLdxycVnMg.png)

James posted a train station saying getting off this afternoon so it highly likely that this is the city he work at.

![Cardiff](/TU62vR1U4ZoVcTTftecOvw.png) _Cardiff_

Yes it was. Cardiff

> Answer: Cardiff
{: .prompt-tip }

## Question 4 — suntan

![Question 4 — suntan](/DCoU4G3KcZK4TBO5XOlKzQ.png)

So, we need to find Sarah first. Since I don't remember seeing Sarah in James’s tweets I started checking James Likes, and boom found her.

![Nice Place](/og4VXBLL966vPkephNiYXw.png) _Nice Place_

Simple reverse image search brings, Elizabeth Quay which is in Perth, Australia.

![Nice Place](/KI6dEYfLXlOJ66PuEwpFqg.png) _Nice Place_

> Answer: Pert
{: .prompt-tip }

## Question 5 — wagthetail

![Question 5 — wagthetail](/lJ8PJ2an3DVKifwVdFYynA.png)

First place I looked was her bio and found some coordinate for Buster’s favorite place (probably her dog)

![I too should do a postgrad](/kjqSum1joRtKaeYUmcKRgQ.png) _I too should do a postgrad_

IT’s 2 Bridge St, **Brecon** LD3 8AH, UK. according to google.

![Nice](/eAAoEq8hNCQEtxrZ-1E2cA.png) _Nice_

> Answer: Brecon
{: .prompt-tip }

## Question 6 — narcissism

![Question 6 — narcissism](/6-0A_BdRIBmae53-msSRA.png)

So I found this George guy from James “Replies” page

![Happy George](/chWF06UkmjT7pxo-0wyl7A.png) _Happy George_

I first tried the Code in the tweet above but it didn't work, so back to searching.

![Oh you silly boy](/MGqbCVkKhXwn4pFRXckiWw.png) _Oh you silly boy_

This looks awful like “Base64” encoding. Decoding it with my personal favorite tools. [https://gchq.github.io/CyberChef/](https://gchq.github.io/CyberChef/) and [https://www.dcode.fr/cipher-identifier](https://www.dcode.fr/cipher-identifier) (this identifier is amazing) Okey, let’s use dCode even though I'm %100 sure that's Base64.

![dCode also believes this is Base64 encoding. Yey](/IwtXv_SYQ7BVujjNR5OGRA.png)

dCode also believes this is Base64 encoding. Yey

![Cool password.](/JRXFewdgb_PXsiGBGrAuZg.png) _Cool password._

> Answer: imamazing123
{: .prompt-tip }

## Question 7— proppedup

![Question 7— proppedup](/Bi5LUxMGsdUK9qouuof_UQ.png)

I haven’t seen any desks in James or Sarah’s tweets so let's look at Georges tweets.

![Hmm. Okey](/5IImSW2LHcgxZ2701coCXg.png) _Hmm. Okey_

Well we found another person of interest. Yey for us. Anyways the answer is: **brown grey**

> Answer: Brown Silver
{: .prompt-tip }

## Question 8 — bluengreen

![Question 8 — bluengreen](/4LlNDItyENm6sasxjo8V_Q.png)

To be honest this took me way to long, like more than 15 minutes. To solve this you go here,

![So very sad](/ek-ncCjJut2oZc1fp0piJw.png) _So very sad_

You see that very small black **“u”** looking character behind the avatar, well here it is. Oh and that's the answer.

![Yeah me too :(](/seCkCkNLnrbXAittxuwdkQ.png) _Yeah me too :(_

> Answer: icanseeyou
{: .prompt-tip }

## Question 9 — clockingout

![Question 9 — clockingout](/bjDsB3bwKGoPL3OnXS9Khw.png)

So I tried so much stuff here and at first I couldn't find it. After I finnesd this section of the ctf and came back. The first thing I noticed was, this tweet.

![Image](/1RjqbVo6LjnlKLhbWGJ_mg.png)

As you can see, James actually gave us everything we needed to solve this question. With this tweet, we know how long he works and the time he got off work.

So, is it simply “1:00 AM minus 8 hours of work = Answer” Not quite, because Twitter actually shows 1:00AM for **MY local time** not UK Time, and since I’m not in the UK Time zone, I’LL need to do some adjustments.

Using sites like [timebie](http://www.timebie.com/timezone/istanbullondon.php) , we can see that 1:00AM my local time is 10:00PM UK Time(previuoıs day) . So, minus 8 hours of work is gives us 5:00PM my local time which is **2:00PM UK Time. The answer is 2:00**

> Answer: 2:00
{: .prompt-tip }

## Question 10 — meme

![Question 10 — meme](/EjmzWGW8krUMeN12n7Sqpg.png)

So I already found the meme with a code in it so I just tried that and it worked. (You can see it couple question above)

> Answer: CTF3404X71
{: .prompt-tip }

## Question 11 — partytime

![Question 11 — partytime](/KDtLMrJCvMkqei_XRb501A.png)

So since I don’t remember any address from James, Sarah and George let's check Pearce’s tweets,

![Nice](/Hnd16XkP6UmvfBf5ASzBgg.png) _Nice_

Opened Google maps and found the routes, C1, 57, 58 and 52

![Nice](/gcTp8afQTqj_7_aGFCFwcA.png) _Nice_

Tried **57** first and it worked.

> Answer: 57
{: .prompt-tip }

## Question 12— leaveamessage

![Question 12— leaveamessage](/cXmu7gIo_CH8rb-UUwHA5w.png)

Looking at the tweet below we haven’t seen Sophjones77 so lets check that account.

![**Where did you go jenmp7, where?**](/3uzJedHufsTb3zRBmyIRGg.png)

**Where did you go jenmp7, where?**

![So sad](/ZysFOjLzqcnW6n7O_FZBFw.png) _So sad_

Uhm, okey that's very sad. Let’s look elsewhere.

| ![Image](/Vtld0zThQBhzQxVpa4Pazw.png) | ![Image](/CcLcoSbidhHcLzl0LUwCWg.png) |

Found these guys, but I can’t be sure they’re related in anyway.

So after searching for a while I found a previous write-up about this question. And yes **Sophjones77** was the correct account but since it's suspended I can't solve that question.

| ![Image](/km2W9v8SvbVytfdtqCr0vQ.png) | ![**Sophjones77**](/pUqUVHzMUZ6EmeZYlOBG8Q.png) |

<p style="text-align: center;">**Sophjones77**</p>

Okey well since I have no way of solving the last question. I’ll have to end this category for the CTF.

But, before I end, the final category, **General Knowledge** is super basic stuff like “what does OSINT and HTTPS stand for” So, I won’t add them here. But hey I still finished them :)

![heheh. Nice.](/8BWK29X2vw2_Nhtj5RgTMQ.png) _heheh. Nice._

Anyhow the first category was very fun to solve hope the next one is too. After I finish the **Evidence Investigation category** i’ll try out this CTF [https://investigator.cybersoc.wales](https://investigator.cybersoc.wales/)

[^1]: [First published in my Medium](https://medium.com/@leventd/cybersoc-cyber-detective-ctf-write-up-life-online-2b9b5f898de)
