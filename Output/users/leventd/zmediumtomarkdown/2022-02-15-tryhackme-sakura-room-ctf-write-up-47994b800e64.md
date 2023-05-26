---
title: "TryHackMe Sakura Room CTF Write-Up"
author: "Levent Durdalı"
date: 2022-02-15T14:33:18.984+0000
last_modified_at: 2022-02-15T14:33:18.984+0000
categories: ""
tags: ["ctf-writeup","challenge","osint","tryhackme","ctf"]
description: "My wired, unexplainable urge to get OSINT Dojo's Student Rank Badge has led me to this CTF, and now that I'm here, I realize that I can get…"
image:
  path: /assets/47994b800e64/0*ZZ58Lm0_V6jBxcK8.png
---

### TryHackMe Sakura Room CTF Write\-Up

My wired, unexplainable urge to get [OSINT Dojo's Student Rank Badge](https://www.osintdojo.com/ranks/) has led me to this CTF, and now that I'm here, I realize that I can get another badge as well\.


> _Small Note before we start, English is not my native language\. So, I apologise for any mistakes that I might do\._ 






![**All of this is for you, Sakura Badge\.**](assets/47994b800e64/0*ZZ58Lm0_V6jBxcK8.png)

**All of this is for you, Sakura Badge\.**

So, the OSINT Dojo's [**Sakura Room**](https://tryhackme.com/room/sakura) on [TryHackMe](https://tryhackme.com/) is designed to test many different OSINT skills and techniques\. And it really did\.

If you'd like to test your skills, then don't read any further\. Open the CTF/Room and give it a try\. Don't scroll further down as I will be discussing how I completed it\.
### Let's Start

Task 1 is an introduction, so I'll skip it\.
### **Task 2: TIP\-OFF**

**Objective:** Find the attackers username\. \(Don't ask what an attacker is\. Just read the [Task\. It really is fun](https://tryhackme.com/room/sakura) \. \) oh, and we are given this [link](https://raw.githubusercontent.com/OsintDojo/public/3f178408909bc1aae7ea2f51126984a8813b0901/sakurapwnedletter.svg) that had this image\.


![Very nice image\.](assets/47994b800e64/1*RZlUSvflkI_khIHrOH0VGA.png)

Very nice image\.

Normally every time I'm given an image from a CTF or Quiz, I immediately go to [Aperi'solve](https://aperisolve.fr/) , an online platform that performs steganography analysis\. But looking at the link, I realized that this image was an SVG\. So my trusted site doesn't work\. But then I saw that the image was on GitHub, and as a Software Developer myself, I thought, let's press F12\. \(Don't sue me, please 😉\)


![Whoa](assets/47994b800e64/1*bDStcvF3urr2Rpb9fZT8Kw.png)

Whoa

Immediately, that one line stood out, that's an operating system directory and /home/XXXX is the username\. For our Task, the answer is **SakuraSnowAngelAiko**
### **Task 3: RECONNAISSANCE**

**Objective:** Find the attackers email address and their full real name\.

Since we have a username, let's search that on google,


![Off\. Google gave two other write\-ups\.](assets/47994b800e64/1*XjVrimjQl-PYyb8J4sLTCA.png)

Off\. Google gave two other write\-ups\.

Here we can see two crucial pieces of information\. GitHub and LinkedIn\. Let's check them out\. But I wonder why the LinkedIn result came up? Was it because of other people solving the CTF? I'll be on the lookout for some other clues that could lead me to LinkedIn\.


![[GitHub Account](https://github.com/sakurasnowangelaiko)](assets/47994b800e64/1*kEsiOK2XSo9RCOr6mavOlw.png)

[GitHub Account](https://github.com/sakurasnowangelaiko)

We can see a repo called PGP\. You know what that means? It means that we'll likely find a public key inside\. If you don't know what PGP is, I recommend [Protonmails Blog](https://protonmail.com/blog/what-is-pgp-encryption/) \.


![Yep, I was correct\.](assets/47994b800e64/1*hvdPVwWJnSRkN6DckfO6cA.png)

Yep, I was correct\.

Okay, now, we have to decode this key and extract the mail address\. You can use built\-in tools on your operating system to do this\. But I found an online tool that does this\. This tool\. [https://cirw\.in/gpg\-decoder/](https://cirw.in/gpg-decoder/)


![This is the relevant part\.](assets/47994b800e64/1*ifUPmGzjoP8ae2UWdvCfcQ.png)

This is the relevant part\.

Answer,
- Name: Aiko Abe \(From LinkedIn\)
- Email: SakuraSnowAngel83@protonmail\.com

### **Task 4:** UNVEIL

**Objective:** Find the attacker's cryptocurrency wallet address, their choice of crypto and which pool paid them on January 23, 2021\.

The Instruction states, "It seems the cybercriminal is aware that we are onto them\. As we were investigating into their Github account we observed indicators that the account owner had already begun editing and deleting information in order to throw us off their trail\."

Hmm, cool, let's check some commit history and review the code\. :\(


![[GitHub Account](https://github.com/sakurasnowangelaiko)](assets/47994b800e64/1*kEsiOK2XSo9RCOr6mavOlw.png)

[GitHub Account](https://github.com/sakurasnowangelaiko)

The repos, cpuminer, Mailpile, xmrig are all active opensource projects, so I doubt it's there\. Before I check that IO repo, let's open the **Repositories Tab** since it states there are 9 repos, a whole 4 more repos than we currently see\.


![Repositories Tab](assets/47994b800e64/1*gv20w5KVXY27BymoXl4EZw.png)

Repositories Tab

Oh, a repo called ETH, Ethereum probably\. That repo has only one line of code\.


![](assets/47994b800e64/1*HcxBSCicmyKu41ED7xFt5A.png)


Since the Instructions stated that they deleted some stuff, let's check the commit history\.


![Yep](assets/47994b800e64/1*WIy8oCt0TxCxZ0CChKlr2Q.png)

Yep

The deleted code, `stratum://0xa102397dbeeBeFD8cD2F73A89122fCdB53abB6ef.Aiko:pswd@eu1.ethermine.org:4444` Having zero knowledge about mining, I searched these strings on google\. I started with the long 0xa… one because that felt important :\)

That led me to [etherscan\.io](https://etherscan.io/txs?a=0xa102397dbeeBeFD8cD2F73A89122fCdB53abB6ef) , some kind of transaction recording site\. \(I think\) Oh, and that string apparently is the wallet address\.


![Cool site\.](assets/47994b800e64/1*0zJtRHEa6eM5PpGvk1u-Nw.png)

Cool site\.

From here, we can answer every question that was asked\. Payment Pool and From probably means the same thing\. And we can easily see that these transactions are for Ethereum\. The Payment Pool for January 23, 2021, can be seen below\. And there are some Tether marked transactions in the value column\. So we can say that this person used Ethereum and Tether\.


![](assets/47994b800e64/1*XVNrnJNtHzZdBfyLvy_vBw.png)


Answer,
- Wallet address: 0xa102397dbeeBeFD8cD2F73A89122fCdB53abB6ef
- Choice of crypto: Mostly **Ethereum** and a couple of **Tether**
- Payment Pool\(January 23, 2021\): Ethermine

### **Task 5:** TAUNT

**Objective:** Find the attacker's current Twitter handle, URL for the location where the attacker saved their WiFi SSIDs and passwords, BSSID for the attacker's Home WiFi\.

We are given this picture to work with,


![Cool](assets/47994b800e64/0*VxiZNUwCgWfYjk9i.png)

Cool

Let's search for that Twitter handle,


![](assets/47994b800e64/1*7YeYCgrk89Hb3MNjHl5zTg.png)


Whoa, 4 of the top 5 results give me the answer\. Let's check it out and find some relevant information\.


![The main image is cropped — To check it, [click here](https://twitter.com/SakuraLoverAiko/status/1353157336538386432/photo/1) \.](assets/47994b800e64/1*NuPC7K4wyBiPP8y6lh5fZw.png)

The main image is cropped — To check it, [click here](https://twitter.com/SakuraLoverAiko/status/1353157336538386432/photo/1) \.

Okay, I have never heard of this Dark Web site, but apparently, we have to find that \.onion site\. So I started searching different keyword combinations **"Deep Search onion", "Search Paste onion"** etc\. eventually, I found a [site linking](https://deepweblinks.net/pastebin/) to another site called **"DeepPaste, a new extensive site\. Paste, chat and links\."** \(FYI, the link was wrong, I found the real link from DuckDuckGo\)

Okay, it's time to download Tor Browser and check it out\.


![Cool Site\.](assets/47994b800e64/1*ouSNIuDgKzzKmxfvLU6e2w.png)

Cool Site\.

From here, we can see multiple WiFi Names, SSIDS and Passwords\. But the question wants a BSSID \(basically the mac address\) \. To find this, we have to check an amazing site called [wigle\.net](https://wigle.net/) \(almost all CTF's use this site, lol\) \. I opened a free account just to use the advanced search option, and trust me\. It's worth it\.


![Query for DK1F\-G](assets/47994b800e64/1*KZ9pU_AHXLTEumX_37Z_-A.png)

Query for DK1F\-G

Excellent, we have a match\. The Net ID is our BSSID\.

Answer,
- Current Twitter Handle: **SakuraLoverAiko**
- URL for the WiFi SSIDs and Passwords: `depasteon6cqgrykzrgya52xglohg5ovyuyhte3ll7hzix7h5ldfqsyd😎onion/show😎php?md5=0a5c6e136a98a60b8a21643ce8c15a74`
- BSSID: 84:AF:EC:34:FC:F8

### **Task 6:** HOMEBOUND

**Objective:** Location closest to the picture they posted before the flight, the last layover airport, What lake can be seen in the map they posted and 
What city does the attacker considers home?

Let's search her Twitter, and what do you know? I found something\.


![[Link](https://twitter.com/SakuraLoverAiko/status/1353471045148110848)](assets/47994b800e64/1*4Qgm0txsV04-gpoJ5ohV3Q.png)

[Link](https://twitter.com/SakuraLoverAiko/status/1353471045148110848)

I was about just about to get it to my Geolocation mindset \(Nah, not really\), but I saw that white thing in the background,


![Cool](assets/47994b800e64/1*24Zi5jjNOTYUiGrucBKbhw.png)

Cool

Oh, that's DC, USA, the Monument\. Cool\. And according to google, the closest airport to the monument is the **Ronald Reagan Washington National Airport \(DCA\) \.**

Let's move on to the Layover part\. She posted this image,


![Hmm okay\.](assets/47994b800e64/1*51V6dagconlggD14qkbF_w.png)

Hmm okay\.

Since this is a First Class Lounge and people love posting pictures, I can safely say Google Lens or Yandex can find this instantly,


![Yep](assets/47994b800e64/1*5u8rl1JhPGCJhl_XV38iCw.png)

Yep

Like I thought, google gave two exact matches, and those photos say that this is the **Japan Airlines Sakura Lounge at Haneda Airport \(HND\) \.**

The lake question is now straightforward to solve, probably, I don't know\.


![](assets/47994b800e64/1*n7mfxGodGVa85Oyqf31mdw.png)


Assuming that is japan and Yep, an exact match\. So\. \. \. That lake is [**Lake Inawashiro**](https://goo.gl/maps/6ooEJXdu7FwoZ25z5) **\.**


![Yep Matchers perfectly](assets/47994b800e64/1*rcdDTbu96zyAixHTgWsJpA.png)

Yep Matchers perfectly

And for the last question…\. We have to find their home city, and I am confident that we actually found this already\. The WiFi list we found has an entry called " **City Free WiFi",** and that city is **"HIROSAKI\_Free\_Wi\-Fi"\.**


![](assets/47994b800e64/1*BIkkIWWoZHsHFJrW5y9LAg.png)


Answer,
- Closest Airport before posting the photo: **DCA**
- Layover Airport: **HND**
- Lake seen from the map: **Lake Inawashiro**
- Attackers Home City: **Hirosaki**


And that's it\. I finished the Sakura CTF\. I already finished [TryHacMe's OhSINT](https://tryhackme.com/room/ohsint) room but didn't have the time to write a post about it\. So I'll write that next week, maybe\. Stay tuned for more\.


![Leaderboard — Rank 9](assets/47994b800e64/1*a20uSQ-O4DJbVC7hJTCeCQ.png)

Leaderboard — Rank 9

Thank you to [OSINTDojo](https://twitter.com/OSINTDojo) for such a fantastic room\! I learned a lot and had a lot of fun researching and learning new techniques\.



_[Post](https://medium.com/@leventd/tryhackme-sakura-room-ctf-write-up-47994b800e64) converted from Medium by [ZMediumToMarkdown](https://github.com/ZhgChgLi/ZMediumToMarkdown)._
