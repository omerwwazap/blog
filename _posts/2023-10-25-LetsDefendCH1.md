---
layout: post
title: Lets Defend Challenge&#58; Investigate Web Attack
date: 2023-10-25 12:00 +0200
categories: [Cyber Security, Walkthroughs]
tags: [English, Letsdefend]     # TAG names should always be lowercase
img_path: /images/LetsDefendCH1/
image:
  path: /webAttack.png
  alt: Let's Defend Investigate Web Attack Challenge.
---

# Investigate Web Attack [^1]

## Solving the challenge

First, we have to download the log file and open it with any text editor you have. I have Notepad++ and Visual Studio Code. Let’s go with VSCode as it has color linting, so it’ll be easier to see.

## *Q1: Which automated scan tool did attacker use for web reconnaissance?*

Checking the logs, the first ~40 logs seem to be normal requests from a Mozilla client using MacOS.

![Logs](/First40Logs.png)

After line 40, we start seeing a new user agent, called “Nikto”. If you're not familiar with it, a quick Google search shows you that Nikto is an open-source vulnerability scanner.

![Logs](/NiktoLogs.png)

Meaning we've found the answer to the first question. It should be noted that that I've never used Nikto, so it’s going to be interesting going forward. As a side note after a Google search, I found bWAPP stands for “buggy web application” which is cool, I guess.

> Answer: Nikto
{: .prompt-tip }

## *Q2: After web reconnaissance activity, which technique did attacker use for directory listing discovery?*

![Logs](/NiktoLogs2.png)

Looking at this, we see that the attacker is trying to find something with changing file extension. My immediate thought was they were trying to upload a file and were testing if there were any “Unrestricted File Uploads” available but when I tried that I get the **“Oops, wrong answer!”** error.

So, checked the hint page. It said “directory ____ ____”.

So, I started searching for different vulnerabilities about Directories.

![Logs](/DirTesting1.png)

![Logs](/DirTesting2.png)

I also saw these parts, but they didn't provide any additional information. After a while I started trying various different vulnerability names and eventually found it.

> Answer: directory brute force
{: .prompt-tip }

## *Q3: What is the third attack type after directory listing discovery?*

Looking at these logs,

![Logs](/Discovery1.png)

![Logs](/Discovery2.png)

It seems like the attacker is testing random endpoints within the same timeframe. My immediate thought was that they were doing and brute force attack. So, I just simply tried this as the answer and it worked. 

> Answer: brute force
{: .prompt-tip }

### Some Notes

![Logs](/ChangeinUserAgent.png)

*In full honesty Q2 and Q3 seems very odd.* But I realize now that I was initially looking at the wrong thing. The directory brute force attempts begin when the user agent changes to MSIE6 (meaning Internet Explorer 6) When you realize this, it makes much more sense.

![Logs](/DirBruteForce.png)

![Logs](/DirBruteForce2.png)

Meaning I solved Q2 and Q3 by pure chance, but at least now I understand the questions.

## *Q4: Is the third attack success?*

Fastest way to test this is to check POST requests, so let's do that.

![Logs](/PostReq.png)

After the last brute force attempt, you find that the next log is;

```log
"GET /bWAPP/portal.php HTTP/1.1"
```

Meaning it worked and they successfully logged in.

> Answer: Yes
{: .prompt-tip }

## *Q5: What is the name of fourth attack?*

```php
phpi.php?message=%22%22;%20system(%27whoami%27)
phpi.php?message=%22%22;%20system(%27net%20user%27)
phpi.php?message=%22%22;%20system(%27net%20share%27)
phpi.php?message=%22%22;%20system(%27net%20user%20hacker%20Asd123!!%20/add%27) 
phpi.php?message=%22%22;%20system(%27net%20user%20hacker%20Asd123!!%20/add%27) 
```

Here, we can see that after logging in, the attacker is trying to execute different system commands. This is commonly known as a Code Injection Attack.

**Note: %27 represents an apostrophe character, and %20 represents a space character.**

> Answer: Code Injection
{: .prompt-tip }

## *Q6: What is the first payload for 4rd attack?*

As seen in the previous question, the first payload is 'whoami'.

> Answer: whoami
{: .prompt-tip }

## *Q7: Is there any persistency clue for the victim machine in the log file? If yes, what is the related payload?*

The answer is YES. Because the 'net user' command is used to add, remove, and make changes to user accounts. The command used was;

```shell
net user hacker Asd123!! /add
```

This means that they added a user named 'hacker' with the password 'Asd123!!!' to the system.

> Answer: %27net%20user%20hacker%20Asd123!!%20/add%27
{: .prompt-tip }

[^1]: This is challenge can be found [here](https://app.letsdefend.io/challenge/investigate-web-attack).
