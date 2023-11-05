---
layout: post
title: "[Work In Progress] Bypassing DLP's - The Analog Gap"
date: 2023-11-03 01:53 +0200
categories: [Cyber Security, Systems]
tags: [English, Ideas]     # TAG names should always be lowercase
img_path: /images/2023DLP1
image:
  path: /0.webp
  alt: Bypassing DLP's - Novel Methods
---

Data leakage is a serious threat to organizations, as it can lead to significant financial losses and compromised security. Almost all organizations have implemented data leakage prevention (DLP) measures to prevent both outsiders and insiders from gaining unauthorized access to data.

The main thing about DLP measures are that they are mainly focused on insiders as a risk (my opinion) and secondly and outside actor that gained access to some systems. My main reasoning for saying insider risk is simple; It is much more harder to detect and prevent data breaches when its done by employees that have rightful access to that data.

One crucial point to understand is that if an employee wants to steal data, they will always find a way to do so, regardless of the obstacles and preventative measures. Thats why my idea/goal of having an DLP is to extremely difficult for them.

## Basics of DLPs and CASB

There are so many documents you can read about DLP and CASB so I'll skip the detailed explanation and give you and analogy.

**DLP** is like a security guard for your data. It helps make sure your sensitive information doesn't accidentally or intentionally leave your company without permission. It watches over your data, like personal information or confidential documents, and stops them from being shared where they shouldn't be, like sending a top-secret file to the wrong person.

**CASB (Cloud Access Security Broker)** is like a security manager for your cloud-based files. It helps your company control and protect the data you store in services like Google Drive or Dropbox. It checks who's using your data, what they're doing with it, and makes sure everyone follows the rules to keep your data secure in the cloud. It's your safety net when using online storage services.

Now thats out of the way. What did I mean by its always possible to bypass DLP? Here is all the ways you can!!! 🚀

## Ways for bypassing DLP's

### 1 - Cameras

Think about it if you open your phone or camera and take a picture of your screen and send it to someone who's going to know. The answer is no one!
It's the same with taking notes or remembering what they see.

#### Solutions

1. Sorry but your are out of luck! the most cost effective way to solve this is to simply ban cameras from the room computers are in. This is standard practice for classified military/intelligence environments. But if you are not in that environment you simple can't. If the data they are stealing is text based they'll need some OCR and they'll have it in writing too.
2. There are some ways which kind of help deter people but still doesn't work it you do OCR and do nnt immediately post the data.
   1. Watermarking applications and software that you are using with and a unique ID that identifies the content, the current date, the viewer email or the IP address used to access content. Problem with this would that it can be photoshoped out before the photo/video is published.
3. **Only way to actually combat this is fo what Gaming Companies are doing**
   - [Tracking leaks on NDA beta Xbox 360s by embedding serial number on-screen](https://news.ycombinator.com/item?id=18643987)
   - [Tweet from Xbox Developer](https://i.redd.it/pdkwdh92rh321.png)[^1]

As a fun note check what Gaming Companies are doing to find game leakers from Computer ScreenShots

| ![Image](/1.png) | ![Image](/2.png) |

<p style="text-align: center;"> Download and Try an Photo Forensics Application </p>

Also another fun topic to read is [Machine Identification Code](https://en.wikipedia.org/wiki/Machine_Identification_Code). ) It's a unique identifier associated with a particular computer or device. It can however act as a finger print for uniq ID's such as the computer name that printed, data, time etc. These are primarily used in classified military/intelligence/government environments. Also its one of the reasons why you need cyan/yellow even if you only print a black and white document. [Also check this Decoding Tool for MIC code.](https://github.com/dfd-tud/deda)

When it comes to physical printing security there even more ways here is a small lis,

- [UV Printing](https://www.nexeimpressions.com/en/uv-security-ink/) just like UV markings in money.
- [MicroText or Microprinting](https://en.wikipedia.org/wiki/Microprinting) 1 point size, readable only with a magnifying glass.[^2]
- InfraRed text - Printed text that is only visible in the dark, with an infrared camera.[^2]

### 2 - Capture Cards and Monitors

#### Solutions



### 3 - Wifi Enabled Hard Drives

Check this list of [Wifi Enabled Hard Drives](https://www.techradar.com/news/best-wireless-drives) as you can see there are many HDD/SSD's with WiFi capabilities. You know what that means! You can connect the wifi drive to the work computer and then access it with another computer via the browsers(through its wifi portal). Now you might be thinking DLP's can stop file transfers to USB's. It's true but one thing to note is that there are in company process where you can ask for access to USB transfers, for legitimate purposes. The thing is that most of the organizations don't check what kind of USB/HDD/SSDs they are giving access to. So its still possible.

#### Solutions

1. Track and analyze the usage of USB drives in your organization along with details on who accessed each device for what, when, and from where.
2. Restrict users from moving business-critical data to USB devices by blocking file copy actions to limit the possibility of a data leak.
3. Scan the data being transferred to USB storage devices to detect or block the transfer of sensitive or confidential information.
4. Think of solutions for creating a white list of USB disks for company given USB/HDD/SSDs and do not allow personal use when granting permission.

But yes this is harders to do than the others one

### 4 - Forms of Stenography

There probably even more but these were the one that came to my mind in a 5 min brainstorming session.

## Info on Side-Channel Attacks

[^1]: [Tweet from Xbox Developer](http://web.archive.org/web/20181211013030/https://twitter.com/cullend/status/1071884772064944128)
[^2]: [Xerox® Speciality Imaging: Fraud Deterrent Technology](https://www.xerox.com/tr-tr/dijital-baski/fraud-deterrent-technology)
