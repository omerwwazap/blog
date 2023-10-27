---
layout: post
title: Security Risks of Public Artificial Intelligence Tools
date: 2023-10-27 22:53 +0200
categories: [Cyber Security, General, Artificial Intelligence]
tags: [English, AI , LLM]     # TAG names should always be lowercase
img_path: /images/LLMRisks
pin: true
image:
  path: /NewHumans.jpg
  alt: Large Language Models takes over the world.
---

# Security Risks for Enterprises

ChatGPT, Bard, PaLM, Copilot, and other Generative AI (GenAI) or Large Language Models (LLMs) have revolutionized our work and life but they come with significant risks. In this article, we'll look into the complex landscape of LLM-related challenges, including biases, misuse,ethical concerns, and the potential threats they pose to secure systems and information integrity.

I'll go over these in an easy to understand manner with bullet points, real examples and hypothetical problems.

## Major Risk 1 - Leakage of Sensitive Information

In very simple terms use of "Public" LLM's may result in unauthorized access to sensitive information, intellectual property, source code and any other data deemed sensitive. This could happen in a number of ways, here are some;

- *Some LLMs are capable of learning from past user queries.* This could directly cause the possibility of generating sensitive information.
  - This a major risk as an individual may not mis-judge the sensitivity of their query to the LLM.
  - Also the initial query may not be sensitive but given enough use from one or multiple individuals will eventually lead the data to become sensitive information.
- *Most LLMs are run and maintain by public/private entities.* While some LLM providers say otherwise there is the possibility of the entered queries being visible to these entities.
- Security Breachers, Data Leakage are Software/API Vulnerabilities of LLM platforms will always be matter of utmost concern.
- Share of training data or outputs with other third party actors.
  - This is very simalar to another current problem with data privacy, where entities give/sell user information to other entities.

### Example Scenarios

#### *Hypothetical Misuse Scenario*

Imagine a government worker working with some sensitive information ... **To Be Added.**

#### *Real Examples*

Public LLMs platform’s own systems and infrastructure may not  be secure, OpenAI had a breach very recently where users got access to other user queries.
For more information look, [Here](https://www.pluralsight.com/blog/security-professional/chatgpt-data-breach), [Here](https://www.washingtonpost.com/technology/2023/07/13/ftc-openai-chatgpt-sam-altman-lina-khan/) and [Here](https://www.searchenginejournal.com/massive-leak-of-chatgpt-credentials-over-100000-accounts-affected/489801/)

## Major Risk 2 - Misinformation, Bias and Hallucination

> Hallucinations: Are confident responses from LLMs that appears plausible but not factual. Its a major problem when you consider how confident the answers are.
{: .prompt-info }

- Current generation LLMs are known to output incorrect, inaccurate and misleading information. Even though most answers given by LLMs now start with some form of a disclaimer stating that they are not entirety knowledgeable and are not an authority on the matter. **The outputs are explain with such confidence that any reader could be mislead.**

- Training on biased data may also lead to discrimination, to potential damage to reputation and possible legal repercussions.
  - Any form of communication without assessing the accuracy of the given output may lead to publications of incorrect statements and information.
  - This also includes all forms of research and development.

- Intentional disinformation and broader campaigns by APTs.
  - Malicious actors can **Poisoning Training Data**, which can lead to anything from disinformation, bias or incorrect knowledge.[^1]

- *Potential for Offensive or Inappropriate Responses.* There is a risk of LLMs being manipulated to generate hate speech or offensive content, since LLMs lack the contextual understanding.[^2]
  - This can occur when an LLM is trained on biased or discriminatory datasets. The result can be producing text promoting harm, discrimination, or hate
  - Noted that all LLMs providers are hard working to eliminate this.

### *Real Example of Mistakes*

![Bing Aı](/BingAILogic.png)

As seen in the image, simple problems that require physical understanding of the world are not accurate.

### *Real Example of Inaccurate Information*

- A Lawyer from USA asked ChatGPT for examples of cases that supported an argument they were try to make.[^3],[^4]

![chatgpt-lawyer](/chatgpt-lawyer-screenshot-1.jpg)
![chatgpt-lawyer](/chatgpt-lawyer-screenshot-3.jpg)

- ChatGPT invented several supporting cases and full details for those cases.
- When asked about its authenticity it even verifies that they are in fact real cases.

### *Reals Example of Hallucinations*

For more information about Hallucinations [check here](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)).

*By Google's Bard*[^5]

![Google's Bard](/BardOfficialDemo.jpeg)

Google's Bard AI promo gets one detail wrong: James Webb Space Telescope *did not* take the first pictures of a planet outside our own solar system. The model returns three bullet points with the final being factually incorrect.

As per NASA, the 1st picture of a planet outside the Milky Way was taken by European Southern Observatory’s Very Large Telescope(VLT), 19 years before in 2004 way before NASA's JWST![^6]

*By ChatGPT*

![ChatGPT](/ChatGPT_hallucination.png)

Here, ChatGPT summarizes a non-existent New York Times article based on a fake URL.
Though this degree of hallucinations dose not happen anymore thanks new improvements. We see more and more subtle hallucinations like Bards JWST answer.

## Major Risk 3 - Transparency, Data Privacy, Confidentiality

- Lack of Transparency
  - LLM generated text often lacks transparency in its origin and the underlying decision process.
  - This causes concerns regarding accountability and it becomes challenging to attribute responsibility or evaluate the reliability of the generated content.
- Privacy and Data Security
  - Data that is sent to external servers for processing for example.
    - What are the implications of protecting sensitive information, particularly confidential or personal data.
    - For example, assume sensitive information is transmitted to an LLM server for language translation without adequate security measures. In that case, it can expose the data to potential breaches or unauthorized access.

## Major Risk 4 - Compliance as a Risk

- Before using LLMs all stakeholders should verify any relevant Regulations and Polices.
  - GDPR (EU), PIPEDA (CA), CCPA (USA), European Union AI Act, National New Generation of AI Standardization Guidance" (China)
    - Inputting sensitive information could inadvertently trigger violations of data protection regulations.
  - Global Partnership on Artificial Intelligence, UNICRI Centre for AI and Robotics
  - etc.
- LLMs have been reported to have used contact created by others (with ot without explicit concent)
  - If outputs are directly used it may lead to Copyright and Ownership issues.

## Other Risk Amplifiers for LLMs

- **Difficulty in detecting AI-generated content**, its becoming increasingly harder to trace, monitor and regulate AI generated content.
- Specialized LLMs for companies/governments becomes the **single collection point for company/government data**.
  - If an entity comprises an LLMs data set there isn't much need for them to search for anything else.
- **Fake News**
  - LLMs can generate text resembling human-written content they can even mimic writing/explanation styles of people.
  - As such LLMs pose a significant risk in the creation of false or misleading information, leading to misinformation and fake news.
  - eg: Creating social media posts that mimic authentic sources or people.
- **Outdated Information**
  - LLMs gather information from datasets that reflect the state of knowledge at the time they were developed. As such, the answers generated by LLMs may become outdated or inaccurate as knowledge evolves.

## Way Forward

- Awareness, Education and Guidance for the use of Public LLMs for personal and work use.
  - Given by Enterprise Security teams.
  - Some form of an Acceptable Use Policy.
- Establishing in house private LLMs systems.
- Technical controls for monitoring and regulating use in side the company.[^7]
  - Having some for Secure/Safe Operating Policy for these systems.

## Other Risks

From my perspective these are the majors risks LLMs how ever these are not even close to the full extend of problems that arises with rise of AI. To name a few headlines;

### Data Input Related Risks

- Unauthorized disclosure.
- Entry of confidential/sensitive information.

### System Security Related Risks

- Supply Chain Risks.
- Software/API Vulnerabilities.
- Breaches / Data Leakage.

## Further Reading for more Risks

- [OWASP Top 10 for Large Language Model Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [Why Red Teams Play a Central Role in Helping Organizations Secure AI Systems](https://services.google.com/fh/files/blogs/google_ai_red_team_digital_final.pdf)
- [Unveiling LLM Vulnerabilities: 6 Key Risks and How to Stay Secure](https://medium.com/wix-engineering/unveiling-llm-vulnerabilities-6-key-risks-and-how-to-stay-secure-a91df5d77195)
- [NCSC - ChatGPT and large language models: what's the risk?](https://www.ncsc.gov.uk/blog-post/chatgpt-and-large-language-models-whats-the-risk)
- [Risks of Large Language Models: A comprehensive guide](https://deepchecks.com/risks-of-large-language-models/)

---
References

[^1]: [OWASP Top 10 for Large Language Model Applications - LLM03: Training Data Poisoning](https://owasp.org/www-project-top-10-for-large-language-model-applications/Archive/0_1_vulns/Training_Data_Poisoning.html)
[^2]: [OWASP Top 10 for Large Language Model Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - **Parts about Prevention**
[^3]: [New York lawyers sanctioned for using fake ChatGPT cases in legal brief](https://www.reuters.com/legal/new-york-lawyers-sanctioned-using-fake-chatgpt-cases-legal-brief-2023-06-22/)
[^4]: [Lawyer cites fake cases invented by ChatGPT, judge is not amused](https://simonwillison.net/2023/May/27/lawyer-chatgpt/) - Images
[^5]: [Googles Promo Tweet](https://x.com/Google/status/1622710355775393793?s=20)
[^6]: [2M1207 b - First image of an exoplanet ](https://go.nasa.gov/3YCFI1f)
[^7]: [GPT-4 Technical Report](https://cdn.openai.com/papers/gpt-4.pdf) - Check Section 6. Risks and Mitigation
