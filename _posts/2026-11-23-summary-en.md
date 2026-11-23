---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 51 items, 6 important content pieces were selected

---

**Technology News**
1. [OpenAI Explores Perplexity as a Measure of Model Intelligence](#item-tech-news-1) ⭐️ 7.0/10
2. [GL.iNet Confirms Cloud Flaw Exploited to Infect Routers and KVM Devices](#item-tech-news-2) ⭐️ 7.0/10
3. [Google builds simulated internet to test Chrome AI agent](#item-tech-news-3) ⭐️ 7.0/10

**Financial News**
1. [US Tech Selloff Triggers Emergency Market Measures Across Asia](#item-finance-news-1) ⭐️ 8.0/10
2. [China Asks US to Withdraw Phone Number Access Limits](#item-finance-news-2) ⭐️ 7.0/10
3. [Ant Group Leads $100M Round in China&\#x27;s Simplexity Robotics at $1.6B Valuation](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI Explores Perplexity as a Measure of Model Intelligence](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI published an article titled &quot;Perplexity and Intelligence&quot; examining how perplexity relates to model intelligence. The supplied material contains only the title, URL, and community comments, so the article&\#x27;s specific claims, data, and any reported results cannot be verified. Commenters describe the piece as presenting a clear trend linking cross-entropy loss to capability, with one reader calling it a simple benchmark compared with more convoluted evaluations. The discussion also references a chart of base models, including a claim that Microsoft&\#x27;s MAI-2 Base reports a log-perplexity of 0.819 on OpenAI&\#x27;s evaluation set.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**「Background」** Perplexity here is the standard language-modeling metric: the degree of surprise a model shows when predicting each next token, equal to vocabulary size for a uniform random predictor and 1 for perfect prediction. OpenAI&\#x27;s post, by Chief Scientist Jakub Pachocki, argues for using perplexity \(equivalently, cross-entropy loss\) as a shared metric across model developers to inform common safety standards.

**「Impact」** For ML practitioners, the discussion points to perplexity on a shared held-out set as a comparatively simple comparison metric across base models, which could make cross-vendor pre-training progress easier to compare than bespoke benchmarks. The reported MAI-2 Base figure is a vendor claim relayed in a comment, not an independently verified result, and the article&\#x27;s own methodology is not available in the supplied material.

**「Community Discussion」** Commenters debated the underlying concept: one noted the article never defines perplexity and supplied the standard definition \(degree of surprise predicting the next token, bounded between 1 and vocabulary size\), while another argued that prediction-as-compression makes the perplexity–intelligence link unsurprising and cited a 2008 paper. A third commenter said they were surprised cross-entropy loss still tracks capability given the rise of RL, and asked what happened with GPT-4.5 and whether o1 marked the start of true reasoning models.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Perplexity_AI">Perplexity AI - Wikipedia</a></li>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#language-models`, `#perplexity`, `#model-evaluation`, `#openai`

---

<a id="item-tech-news-2"></a>
### [GL.iNet Confirms Cloud Flaw Exploited to Infect Routers and KVM Devices](https://www.bleepingcomputer.com/news/security/hackers-exploit-glinet-cloud-flaw-to-infect-routers-kvm-devices/) ⭐️ 7.0/10

GL.iNet has confirmed that attackers exploited a vulnerability in its cloud remote management services to install custom malware on customers&\#x27; routers and KVM devices. Some affected users reported backdoors and reverse shells that gave remote access to infected devices. The source excerpt does not specify the affected firmware or service versions, the vulnerability&\#x27;s technical mechanism, or a patch or mitigation timeline, so the scope of exposure and remediation status remain unclear.

rss · BleepingComputer · Nov 22, 18:45

**「Background」** GL.iNet&\#x27;s own security notice, dated November 20, 2026, states that the company identified the vulnerability in its cloud remote management services that day and that an unauthorized party exploited it to access and install malicious software on some routers and KVM devices. The flaw therefore sits in the cloud-based remote management layer rather than in the device firmware itself, which is why the vendor&\#x27;s notice covers both router and KVM product lines.

**「Impact」** Because the flaw sits in GL.iNet&\#x27;s cloud remote management service rather than a single device model, owners of affected routers and KVM devices should treat internet-exposed management access as potentially compromised and check devices for unauthorized access until GL.iNet publishes remediation guidance.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20">GL.iNet Security Notice 2026-11-20</a></li>
<li><a href="https://forum.gl-inet.com/t/2026-11-20-gl-inet-security-notice-goodcloud-kvm-routers/73056">2026-11-20: GL.iNet Security Notice - GoodCloud / KVM / Routers</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#routers`, `#embedded-systems`, `#cloud`

---

<a id="item-tech-news-3"></a>
### [Google builds simulated internet to test Chrome AI agent](https://www.landian.news/archives/128701.html) ⭐️ 7.0/10

Google has reportedly built a simulated internet environment called Mirror Dimension to test Chrome&\#x27;s AI agent in isolation, according to a brief Landian News report relayed via Telegram. The environment is said to contain thousands of simulated websites, with each engineer testing in a separate isolated setup and more than 1,000 test cases run daily. The tests reportedly cover the agent opening sites, searching and browsing, logging in, adding items to carts, and completing tasks, with a focus on defending against prompt injection and other attacks from malicious web pages. The item is a secondary report without primary sourcing, so the scale figures and security details remain unverified.

telegram · zaihuapd · Nov 23, 01:30

**「Background」** Google&\#x27;s security blog describes Mirror Dimension as a synthetic version of the web used to test Chrome&\#x27;s &quot;auto browse&quot; agent in realistic online environments without exposing the real internet to risk. The setup is intended to let engineers evaluate agent behavior, including defenses against prompt injection from malicious pages, before such browsing capabilities reach users.

**「Impact」** If confirmed, the approach points to a testing requirement for browser-based AI agents: because such agents act on page content, malicious pages can attempt prompt injection, so isolated simulated environments rather than live sites would be needed to exercise login, purchase, and task-completion flows safely. The report does not indicate whether Mirror Dimension or its test tooling will be released publicly.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/security/mirror-dimension-for-agents/">Mirror Dimension for Agents: Evaluating Browser-Use Agents ...</a></li>
<li><a href="https://explainx.ai/blog/google-mirror-dimension-synthetic-web-chrome-auto-browse-agents-prompt-injection-testing-2026">Google Mirror Dimension: Fake Web for Chrome AI Agents ...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#browser automation`, `#prompt injection`, `#AI security`, `#testing infrastructure`

---

## Financial News

<a id="item-finance-news-1"></a>
### [US Tech Selloff Triggers Emergency Market Measures Across Asia](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

US tech stocks fell sharply on Friday, with the Nasdaq down 5.28% in a single day and the Philadelphia Semiconductor Index down nearly 11%, prompting same-week emergency stabilization measures in mainland China, South Korea, and Taiwan. The measures include mainland China lowering the minimum margin requirement to 80%, South Korea easing daily share buyback limits from November 24 for three months, and Taiwan banning short-selling below the previous close from November 23 and raising short-sale margin from 130% to 150%.

telegram · zaihuapd · Nov 22, 13:24

**「Background」** The selloff was concentrated in AI-related technology shares, and the policy responses target trading rules that can amplify price swings, such as margin financing and short-selling.

**「Impact」** The rule changes directly affect investors and brokers in mainland China, South Korea, and Taiwan by altering the cost and availability of margin trading and short-selling during the volatility.

**Tags**: `#US tech selloff`, `#market stabilization policy`, `#short-selling rules`, `#Asian equities`, `#margin requirements`

---

<a id="item-finance-news-2"></a>
### [China Asks US to Withdraw Phone Number Access Limits](https://www.bloomberg.com/news/articles/2026-11-22/china-objects-to-us-curbs-on-telecoms-access-to-phone-numbers) ⭐️ 7.0/10

China&\#x27;s Commerce Ministry on November 22 urged the US to withdraw a measure barring China Mobile, China Telecom and China Unicom from directly obtaining US phone numbers, saying it violates non-discrimination and fair competition principles. The FCC voted on November 19 to tighten security requirements for voice-over-internet providers seeking direct access to US numbers, adding national security certification to block entities, equipment and services on its Covered List.

telegram · zaihuapd · Nov 22, 06:44

**「Background」** The FCC voted on November 19, 2026 to tighten security requirements for voice-over-internet providers seeking direct access to US numbers, adding national-security certification aimed at keeping entities on its Covered List off US networks. The US regulator had already denied China Mobile&\#x27;s US service application in 2019 and revoked China Telecom&\#x27;s and China Unicom&\#x27;s authorizations in 2021 and 2022, according to Inside Towers.

**「Impact」** The dispute affects the three Chinese carriers and cross-border calling services between the US and China, with Beijing warning the measures are pushing the two countries toward decoupling in telecom, communications and testing certification.

<details><summary>References</summary>
<ul>
<li><a href="https://www.jpost.com/international/article-915665">China slams US FCC ban on direct phone number access for...</a></li>
<li><a href="https://www.foxbusiness.com/politics/fcc-bans-chinese-firms-direct-access-us-phone-numbers-bid-curb-robocalls">FCC regulators bar Chinese telecom giants from direct number access</a></li>
<li><a href="https://insidetowers.com/congress-subpoenas-three-china-telecoms/">Congress Subpoenas Three China Telecoms - Inside Towers</a></li>

</ul>
</details>

**Tags**: `#telecom regulation`, `#US-China relations`, `#FCC`, `#China carriers`, `#trade policy`

---

<a id="item-finance-news-3"></a>
### [Ant Group Leads $100M Round in China&\#x27;s Simplexity Robotics at $1.6B Valuation](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

Bloomberg reports that Chinese embodied-AI company Simplexity Robotics raised a $100 million pre-A round led by Ant Group at a $1.6 billion post-money valuation, with existing investors Alibaba, Tencent, HongShan and BlueRun participating; chairman and co-founder Wang Kai confirmed the deal to Bloomberg.

telegram · zaihuapd · Nov 23, 02:02

**「Background」** Simplexity Robotics was founded in Hangzhou in July 2025 by former Li Auto executives and disclosed in March that it had completed five funding rounds totaling 2 billion yuan within six months of launch, at a post-money valuation already above $1 billion.

**「Who this affects」** The funding gives Simplexity more capital to compete with established Chinese humanoid-robot makers such as Unitree and UBTech, a market where China accounted for about 97% of global humanoid-robot shipments, according to Bloomberg.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gasgoo.com/robot/news/70449505-%E7%90%86%E6%83%B3%E5%89%8D%E9%AB%98%E7%AE%A1%E5%81%9A%E6%9C%BA%E5%99%A8%E4%BA%BA-%E5%8D%8A%E5%B9%B4%E8%9E%8D%E4%BA%8620%E4%BA%BF-%E6%80%8E%E4%B9%88%E5%81%9A%E5%88%B0%E7%9A%84/">理 想 前高管做机器人，半年 融 了20亿，怎么做到的？ | 盖世 汽 车</a></li>
<li><a href="https://www.linkedin.com/posts/caproasia_china-robot-startup-simplexity-robotics-raised-activity-7438465152846385152-3W35">China Robot Startup Simplexity Robotics Raised $290 Million...</a></li>
<li><a href="https://equalocean.com/news/2026030921780">Five Rounds, RMB 2B: Simplexity Robotics Emerges... | EqualOcean</a></li>
<li><a href="https://www.thenovtech.com/p/a-robot-just-ran-100-meters-in-886">Beijing&#x27;s Robot Week: Sprint Records, IPOs, and 97 % Market</a></li>
<li><a href="https://www.workoptional.ai/p/china-builds-the-body-america-builds-the-brain-8c09">China Builds the Body. America Builds the Brain.</a></li>

</ul>
</details>

**Tags**: `#embodied AI`, `#humanoid robotics`, `#venture funding`, `#China tech`, `#Ant Group`

---