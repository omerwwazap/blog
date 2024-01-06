---
layout: post
title: "Identity Theft in the Era of Advanced AI"
date: 2024-01-06 01:53 +0200
categories: [Artificial Intelligence]
tags: [English, AI, Ideas]     # TAG names should always be lowercase
img_path: /images/2024TheftIDAI
image:
  path: /0.png
  alt: From mage.space and @emmanuel_2m's Aitana2
---

## Art of Deception

Identity theft is on the brink of a startling surge, and distinguishing authenticity from deception is becoming increasingly challenging.

Take a look at these images[^1],[^2],[^3];

| ![Image](/1.jpeg) | ![Image](/2.jpg) | ![Image](/6.jpeg) |

*Can you tell if they're authentic or fake?*

Well, all of these images are AI generated, image designed to trick first-level verification systems, a staple in many financial institutions and KYC protocols.

Now lets look at what this reddit user did

The first image was created by a reddit user **u/*harsh*** and was shared on **r/StableDiffusion**. The rest are thanks to u/*harsh*'s inspiration.

| ![Image](/3.jpeg) | ![Image](/5.png) |

## Workflow - Fully Open Source[^4]

### 1. Face Generation with LoRAs

LoRAs, or Low-Rank Adaptations, are a technique used in AI image generation, particularly with models like Stable Diffusion. They serve as a way to fine-tune these models by introducing new concepts or styles into the generation process. This makes them useful for generating images with particular styles or subjects with greater fidelity. You can checkout [civitai](https://civitai.com/) for some examples.

- LoRA Examples
  - [DreamShaper XL](https://civitai.com/models/112902/dreamshaper-xl)
  - [OmnigenXL](https://civitai.com/models/203014/omnigenxl-nsfw-and-sfw)
  - [LRM - Liangyiu's Realistic Mix](https://civitai.com/models/81304/lrm-liangyius-realistic-mix)

Begin by generating a set of faces without using LoRAs. To enhance the chosen image, apply a combination of LoRAs.
For instanse, mix a lower quality face LoRA you've trained with a small proportion (around 0.3) of a high-quality celebrity LoRA.
This blend can significantly improve the variety and quality of the outputs.

### 2. Refining the Face

Reuse the seed from your chosen image and refine the face with the combined LoRAs and a control net. The control net allows for more detailed adjustments.

### 3. Adding Text to a Card

- Generate an image of blank paper using Stable Diffusion.
- Write the desired text on a physically textured paper.
- In Photoshop, overlay this paper as a 'hard light' layer over the generated blank paper, and clean up as needed.

Alternatively one can use tools like [Calligrapher AI](https://www.calligrapher.ai/) for automatic generation.

> These images that you just saw were created on this week *06.01.2024*, the picture below[^5] is from **11.02.2023**. Incredible advancement in under three months.
{: .prompt-info }

![Image](/7.jpeg)

## Future Threats

**The threat is clear: criminals are poised to exploit open-source models to craft flawless deepfakes of someone real or to create entire new personas for fraud.**

However, the real issue isn't just identity theft, it's a problem thats going to cause massive headaches for everyone involved, from normal people to politicians. *Once this level of quality translates to video generation, we'll face an unparalleled crisis.*

> Even **dead** politicians are affected. The Flemish Christian Democrat Party, the CD&V used AI to bring their former PM back to life. [Twitter (X) Post here](https://twitter.com/cdenv/status/1732479890178412877).
> [More info on VRT.be](https://www.vrt.be/vrtnws/en/2023/12/07/_the-beast-is-back-christian-democrats-bring-former-pm-back-to/)
{: .prompt-warning }

Imagine a simalar fabricated picture or a video depicting your abduction sent to your parents, demanding ransom, all courtesy of AI technology. 👍

![Image](/8.png) *I'ts not all bad 😅*

Banks might need to promptly bolster their security protocols and regulations to combat this threat, assuming they haven't already done so.

As normal people, we might have to assume everything is fake by default. Much like the dilemma of deepfakes with revenge porn. And have figure out a way to verify the contents for authenticity.

## Thats Not All

Imagine adding a fabricated or a cloned -your- voice to all the things mentioned above.

Prof. Ethan Mollick has an simple but amazing demonstration for this.[^6]

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">This is a completely fake video of me. The AI (HeyGen) used 30 seconds of me talking to a webcam and 30 seconds of my voice, and now I have an avatar that I can make say anything. Don&#39;t trust your own eyes.<br><br>Its not perfect, but a two minute recording would yield better results. <a href="https://t.co/HkIooCo6Zu">pic.twitter.com/HkIooCo6Zu</a></p>&mdash; Ethan Mollick (@emollick) <a href="https://twitter.com/emollick/status/1743146951749533897?ref_src=twsrc%5Etfw">January 5, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

> Click on the tweet to see the full thread. He explains and shows the original images and voices with the fabricated/generated content.
> More info from Ethan, [A quick and sobering guide to cloning yourself](https://www.oneusefulthing.org/p/a-quick-and-sobering-guide-to-cloning) and [AI is Already Altering the Truth](https://www.oneusefulthing.org/i/140341342/ai-is-already-altering-the-truth) 
{: .prompt-tip }

A similar thread on how to create fabricated videos and voice was shared by @LinusEkenstam, [Make an Instant AI Avatars (Clones) for free](https://twitter.com/LinusEkenstam/status/1728069915301581080) and [Animate-Anyone](https://twitter.com/LinusEkenstam/status/1730356019182829571)

### AI Influencer's

I'm not going to explains this, its something you should know

- [theClueless AI](https://www.theclueless.ai/models) - Company
  - [Aitana Lopez](https://www.theclueless.ai/project/aitana-lopez)
    - [Hey Story](https://twitter.com/heyronir/status/1730818748981158299)
  - [Maia Lima](https://www.theclueless.ai/project/maia-lima-2)
  - [@limaiaaa](https://www.instagram.com/limaiaaa/)
- [@lilmiquela](https://www.instagram.com/lilmiquela/?hl=en) - Only on Instagram

> Want to create it your on AI Influencer? Read This!!! by [@emmanuel_2m](https://twitter.com/emmanuel_2m)
> 
> - [How to build your on AI #influencers in 30 minutes](https://twitter.com/emmanuel_2m/status/1743178167710552566)
> - [Creating with LoRA](https://twitter.com/emmanuel_2m/status/1743178187126030345)
> - [An AI character made with Scenario](https://twitter.com/emmanuel_2m/status/1738358988193092085)
> - [Character consistency](https://twitter.com/emmanuel_2m/status/1743613492521791842)
{: .prompt-tip }

Comment form the dude that invented LoRA (Low-Rank Adaptations), Simo Ryu. [Little did I realize year later thousands of deepfake waifu LoRAs would be flooding on the web...](https://twitter.com/cloneofsimo/status/1743291012276179240)

## We Already See its Problems

The imminent impact of AI on identity verification processes in Know-Your-Customer systems is undeniable. As AI progresses, it becomes easier and more economical to replicate someone's likeness and identity markers, often acquired from data breaches. Consequently, infiltrating accounts, stealing funds, compromising data, and damaging brands will become simpler for malicious actors. And it's already started;

- [AI deepfakes are getting better at spoofing KYC verification — Binance exec](https://cointelegraph.com/news/binance-rise-in-deepfake-customer-checks-verification)
- [New North America Fraud Statistics: Forced Verification and AI/Deepfake Cases Multiply at Alarming Rates](https://finance.yahoo.com/news/north-america-fraud-statistics-forced-130500823.html)
- [Liveness tests used by banks to verify ID are ‘extremely vulnerable’ to deepfake attacks](https://www.theverge.com/2022/5/18/23092964/deepfake-attack-facial-recognition-liveness-test-banks-sensity-report)
- [How Underground Groups Use Stolen Identities and Deepfakes](https://www.trendmicro.com/en_us/research/22/i/how-underground-groups-use-stolen-identities-and-deepfakes.html)

Just a short while ago, deceiving these systems was a formidable challenge. However, with the advancement of deepfakes and AI-generated personas, breaching these security measures is increasingly within reach.

The landscape of security and authenticity is rapidly shifting, and the window for relying on video verification systems may be closing sooner than we think.

[^1]: [I want to join in and have taken it a little further.](https://www.reddit.com/r/StableDiffusion/comments/18zt733/i_want_to_join_in_and_have_taken_it_a_little/)
[^2]: [First verification post got taken down. Here is another one.](https://www.reddit.com/r/StableDiffusion/comments/18yf5dk/first_verification_post_got_taken_down_here_is/)
[^3]: [If you've been following along, this is a 3rd and last post. First 2 got removed. This is the culmination of all I've learned in the past 24 hours](https://www.reddit.com/r/StableDiffusion/comments/18yq5r4/if_youve_been_following_along_this_is_a_3rd_and/)
[^4]: [Workflow for Generation](https://www.reddit.com/r/StableDiffusion/comments/18yq5r4/comment/kgco82f/)
[^5]: [AI Notkilleveryoneism Memes - @AISafetyMemes](https://twitter.com/AISafetyMemes/status/1743241432482119823/photo/1)
[^6]: [This is a completely fake video of me @emollick](https://twitter.com/emollick/status/1743146951749533897)
