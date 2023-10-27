---
layout: post
title: Lets Defend Challenge&#58; Shellshock Attack
date: 2023-10-25 12:00 +0200
categories: [Cyber Security, Walkthroughs]
tags: [English, Letsdefend]     # TAG names should always be lowercase
img_path: /images/LetsDefendCH3
image:
  path: /dfir_crocodile.jpeg
  alt: Let's Defend Shellshock Attack Challenge.
---

# Shellshock Attack [^1]

**What is Shellshock attack?**
Shellshock is a family of security bugs in the Unix Bash shell. It was first disclosed on September 24, 2014, and could enable an attacker to cause Bash to execute arbitrary commands and gain unauthorized access to many Internet-facing services, such as web servers, that use Bash to process requests[^2]

## Solving the challenge

We need a program to open PCAP files. I’ll be using Wireshark again.

## *Q1: What is the server operating system?*

At a quick glance we can see packets with the headers “500 Internal Errors”. This will likely have some clues regarding its OS.

![PCAP](/1.png)

Checking the decoded text, we can see:

![PCAP](/2.png)

> Answer: Ubuntu
{: .prompt-tip }

## *Q2: What is the application server and version running on the target system?*

We can see this in the previous question.

> Answer: Apache/2.2.22
{: .prompt-tip }

## *Q3: What is the exact command that the attacker wants to run on the target server?*

I quickly checked these packets due to the obvious name “/exploitable.cgi”

![PCAP](/3.png)

Inside the packets we can see this decoded text.

![PCAP](/4.png)

> Answer: /bin/ping -c1 10.246.50.2
{: .prompt-tip }

[^1]: This is challenge can be found [here](https://app.letsdefend.io/challenge/shellshock-attack).
[^2]: [Article on ShelShock](https://en.wikipedia.org/wiki/Shellshock_%28software_bug%29)