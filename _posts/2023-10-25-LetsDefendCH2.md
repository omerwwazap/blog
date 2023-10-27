---
layout: post
title: Lets Defend Challenge&#58; Port Scan Activity
date: 2023-10-25 12:00 +0200
categories: [Cyber Security, Walkthroughs]
tags: [English, Letsdefend]     # TAG names should always be lowercase
img_path: /images/LetsDefendCH2
image:
  path: /pirate_eye.jpeg
  alt: Let's Defend Port Scan Activity Challenge.
---

# Port Scan Activity [^1]

First, we have to download a program similar to Wireshark to open the PCAP file.

## *Q1: Which automated scan tool did attacker use for web reconnaissance?*

There multiple IP addresses that seems to be doing something. My best guess for identifying the attacker is to check the ports. If they are trying to connect to various related or unrelated ports than that’s our attacker. IP 10.42.42.253 appears to be probing some interesting ports, such as 74, 554, and 389. More interestingly, these connections all have the RST flag, indicating that they are not fully connecting but merely checking if the server is responsive.

![PCAP](/1.png)

> Answer: 10.42.42.253
{: .prompt-tip }

## *Q2: What is the IP address found as a result of the scan?*

Seeing this question and knowing that there are three visible IP addresses suggests that there is a successful connection hidden somewhere in the logs.

Some quick Googling on how to use Wireshark's filter function led me to this filter query, “tcp.flags.ack==1” but this also included RST flags.

So, I had to modify the query to this: `“(tcp.flags.ack==1) && (tcp.flags.reset==0)”`.

![PCAP](/2.png)

Here, you can see that the only IP address with the ACK flag is 10.42.42.50.

> Answer: 10.42.42.50
{: .prompt-tip }

## *Q3: What is the MAC address of the Apple system it finds?*

This can be found by checking the Ethernet II section of the packets.  

![PCAP](/3.png)

Or we can search the string “Apple” since Wireshark automatically resolves MAC address as seen above.

![PCAP](/4.png)

> Answer: 00:16:cb:92:6e:dc
{: .prompt-tip }

## *Q4: What is the IP address of the detected Windows system?*

It took a lot of time for some reason, but after I found a packet with the name “SMBSERVER”, I knew I had found the answer, as SMB is a Windows protocol.

![PCAP](/5.png)

You can also search for the query 'Microsoft' to find packets related to this, but that didn’t come to mind when I solved this question.

Another way to solve this is to look at NetBIOS packets (NBNS) since it’s also is a Windows only protocol.

> Answer: 10.42.42.50
{: .prompt-tip }

[^1]: This is challenge can be found [here](https://app.letsdefend.io/challenge/port-scan-activity).
