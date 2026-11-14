---
layout: default
title: "Horizon Summary: 2026-11-14 (EN)"
date: 2026-11-14
lang: en
---

> From 62 items, 13 important content pieces were selected

---

**Technology News**
1. [Report claims Nvidia CEO Jensen Huang resigned over alleged affair with Chinese spy](#item-tech-news-1) ⭐️ 8.0/10
2. [TorchTitan Trains 1T-Parameter MoE on 384 GH200 GPUs](#item-tech-news-2) ⭐️ 8.0/10
3. [Hobbyist SDR Setup Transcribes Entire Airband Live](#item-tech-news-3) ⭐️ 7.0/10
4. [Amazon plans &quot;World Product Graph&quot; to index web shopping data](#item-tech-news-4) ⭐️ 7.0/10
5. [ChatGPT Wallet lets OpenAI&\#x27;s Dots agents make purchases](#item-tech-news-5) ⭐️ 7.0/10
6. [Jensen Huang&\#x27;s Departure Said to Cut AI Startup Funding](#item-tech-news-6) ⭐️ 7.0/10
7. [Report: China&\#x27;s Top AI Models Trained on Banned Nvidia Chips](#item-tech-news-7) ⭐️ 7.0/10
8. [Check Point Gateways Hit by PHP2Shell Attacks Deploying ESXi Wiper](#item-tech-news-8) ⭐️ 7.0/10
9. [ICML 2027 Adds Two-Stage Review and Reviewer Quotas](#item-tech-news-9) ⭐️ 7.0/10
10. [Shanghai investigation faults ethics and consent in gene-editing death](#item-tech-news-10) ⭐️ 7.0/10
11. [Python 早期贡献者 Tim Peters 去世，享年 74 岁](#item-tech-news-11) ⭐️ 7.0/10
12. [DeepSeek 开放应用 API，支持服务端工具调用](#item-tech-news-12) ⭐️ 7.0/10
13. [SpaceX 裁撤约 60 名 Grok Imagine 研发人员](#item-tech-news-13) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Report claims Nvidia CEO Jensen Huang resigned over alleged affair with Chinese spy](https://techcrunch.com/2026/11/13/nvidia-ceo-jensen-huangs-affair-with-alleged-chinese-spy-a-timeline/) ⭐️ 8.0/10

A TechCrunch report dated November 13, 2026 states that Nvidia CEO Jensen Huang has resigned following an affair, and raises possible national-security ramifications given the U.S.-China race to build advanced AI infrastructure. The supplied source is a single-sentence summary with no named sourcing, timeline details, or corroboration, so the resignation and the alleged espionage connection remain unverified claims rather than confirmed events. No Nvidia statement, regulatory filing, or independent confirmation is included in the material provided.

rss · TechCrunch AI · Nov 13, 15:58

**「Background」** Nvidia&\#x27;s board announced Huang&\#x27;s resignation on November 12, 2026, appointing CFO Colette Kress as interim CEO until a permanent successor is named, according to The Guardian. The New York Times reported that the board said it would investigate after Huang admitted the affair, and that Huang also had a relationship with Kimberly Powell, Nvidia&\#x27;s vice president of health care, who reports to him. The BBC reported that Huang has agreed to appear before Congress following the resignation.

**「Impact」** The source provides no details on succession, interim leadership, or operational continuity at Nvidia, so the concrete consequences for customers and developers relying on Nvidia&\#x27;s AI hardware cannot be established from the supplied material. A separate AP report cited in search results describes competitors seeking to exploit uncertainty around the chip giant, but that is external commentary rather than a verified operational effect.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/12/nvidia-ceo-jensen-huang-resigns">Jensen Huang resigns as Nvidia CEO after alleged affairs</a></li>
<li><a href="https://www.nytimes.com/live/2026/11/12/business/nvidia-jensen-huang-resigns">Nvidia Updates: Huang ’s Resignation Reverberates Through...</a></li>
<li><a href="https://www.bbc.com/news/live/c6zjry11v8w1t">Huang agrees to appear before Congress, US lawmakers... - BBC News</a></li>
<li><a href="https://apnews.com/article/nvidia-jensen-china-ai-chips-1b7431af84c9d78773c277672a9486f3">Jensen Huang&#x27;s departure as Nvidia CEO may dampen mood around ...</a></li>

</ul>
</details>

**Tags**: `#nvidia`, `#ai-industry`, `#us-china-tech`, `#national-security`, `#corporate-leadership`

---

<a id="item-tech-news-2"></a>
### [TorchTitan Trains 1T-Parameter MoE on 384 GH200 GPUs](https://www.reddit.com/r/MachineLearning/comments/1xvce5h/scaling_to_1t_moe_on_torchtitan_p/) ⭐️ 8.0/10

A practitioner report describes training a ~1T-parameter mixture-of-experts model with TorchTitan at ~1,300 tokens/s per GPU on 384 GH200 GPUs, a 14X improvement over the starting point. The setup uses 384-way FSDP plus 4-way expert parallelism kept inside each node, skipping pipeline parallelism to avoid long steps. Reported gains include 4X from full activation checkpointing, a drop in optimizer step time from 42 s to ~2 s after moving Newton-Schulz to the GPU, and 21% throughput from fixing allocator retries. The author notes the router load-balancing trade-off is still under evaluation and that the write-up is a practitioner experience report, not a peer-reviewed result.

reddit · r/MachineLearning · /u/f14-bertolotti · Nov 13, 16:28

**「Context」** TorchTitan is PyTorch&\#x27;s native training stack for large-scale models, composing FSDP, tensor, pipeline, context, and expert parallelism in one codebase. A December 2025 PyTorch blog post described efficient MoE pre-training with TorchTitan on 1,000 AMD GPUs, framing it as a reusable recipe from early experiments to full-scale runs. This report extends that line to a ~1T-parameter MoE on 384 GH200 GPUs, adding parallelism trade-offs and optimizer changes.

**「Impact」** Teams training large MoE models on Hopper-class clusters with slower inter-node links can apply the reported techniques directly: full activation checkpointing, offloading checkpoint activations to Grace over the C2C link, Muon instead of Adam, and FlexShard expert sharding to keep Newton-Schulz local. The author reports these changes raised throughput from a baseline step of 84 seconds, 68 of which were network wait, to ~1,300 tokens/s per GPU on 384 GH200s, a 14X improvement. Two fixes depend on TorchTitan/FSDP2 internals: GPU-side Newton-Schulz for host-offloaded parameters and the private \`unshard\_async\_op\` flag, which the author says is becoming a public API, so others may need to wait for that exposure or patch it themselves.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/pytorch/torchtitan">GitHub - pytorch/torchtitan: A PyTorch native platform for ...</a></li>
<li><a href="https://pytorch.org/blog/efficient-moe-pre-training-at-scale-with-torchtitan/">Efficient MoE Pre-training at Scale on 1K AMD GPUs ... - PyTorch</a></li>

</ul>
</details>

**Tags**: `#large-language-models`, `#mixture-of-experts`, `#distributed-training`, `#pytorch`, `#gpu-scaling`

---

<a id="item-tech-news-3"></a>
### [Hobbyist SDR Setup Transcribes Entire Airband Live](https://orcasairband.com/) ⭐️ 7.0/10

A hobbyist project at orcasairband.com streams live airband monitoring and transcription from an ETTUS B210 software-defined radio attached to a machine with dual RTX 4090 GPUs. The author describes a CUDA polyphase channelizer that takes the entire airband, splits it into channels on the GPU, demodulates each, detects transmissions, discards data transmissions, and transcribes the audio. The site was demonstrated during a real ground stop affecting Victoria and Orcas, and the author posted raw, unedited transcripts generated at the time of posting, including a 2143Z Victoria Ground transmission on 126.400 and a 2151Z Vancouver Centre exchange on 134.800. This is a personal project rather than a shipped product, and the transcripts are presented as-is without independent verification.

hackernews · mmaunder · Nov 13, 22:04 · [Discussion](https://news.ycombinator.com/item?id=50490593)

**「Background」** The project uses an Ettus USRP B210, a single-board software-defined radio with continuous coverage from 70 MHz to 6 GHz, to capture the airband. A GPU-based polyphase channelizer then splits the wideband capture into individual channels for demodulation and transcription, an approach similar to earlier research that used GPUs to channelize full-band radio traffic in real time. The demonstration coincided with a ground stop affecting departures, which the FAA describes as holding aircraft on the ground while managing those already airborne.

**「Practical takeaway」** The project shows that a single wideband SDR plus consumer GPUs can channelize, demodulate, and transcribe the full airband in real time, a workflow that previously required dedicated per-frequency receivers or narrower tuning. Anyone relying on the transcripts should treat them as unverified: the author notes weak signals and unintelligible passages, and commenters reported that many transmissions were hard to understand.

**「Community reaction」** Commenters found the ground-stop context compelling: one quoted a 14:03 exchange on the stream in which a pilot asked to confirm a ground stop into Vancouver and was told nothing was departing to land there. Another reader said many transmissions were garbled and that they could understand barely half of what was said, while expressing admiration for the controllers and pilots who work with such audio. A separate commenter compared the approach to an earlier hobby project that decodes ships&\#x27; DSC signals from public KiwiSDR receivers and uses timing differences across receivers to triangulate positions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ettus.com/all-products/ub210-kit/">USRP B 210 USB Software Defined Radio ( SDR ) - Ettus Research</a></li>
<li><a href="https://www.pure.ed.ac.uk/ws/files/148736420/medcomnet2020.pdf">One GPU to Snoop Them All: a Full- Band</a></li>
<li><a href="https://www.newsmax.com/us/faa-ground-stop-spreads-to-international-flights/2026/11/13/id/1276264/">FAA Ground Stop Spreads to International Flights | Newsmax.com</a></li>

</ul>
</details>

**Tags**: `#software-defined-radio`, `#GPU-computing`, `#signal-processing`, `#speech-transcription`, `#hobbyist-engineering`

---

<a id="item-tech-news-4"></a>
### [Amazon plans &quot;World Product Graph&quot; to index web shopping data](https://www.theverge.com/tech/1033697/amazon-world-product-graph-ai-search) ⭐️ 7.0/10

Amazon reportedly plans a project called the &quot;World Product Graph&quot; to build a vault of data on products sold anywhere online, including items Amazon does not sell, and surface that information through its own site, according to Reuters reporting cited by The Verge. The stated aim is to keep shoppers from leaving Amazon to research products on Reddit or Google, and to make Amazon the likely destination even for products sold elsewhere. The same logic extends to AI shopping agents: if Amazon holds the largest stockpile of shopping data, agents may rely on its product index over others. The report describes a plan rather than a shipped capability, and the available excerpt does not detail technical architecture, timelines, or availability.

rss · The Verge · Nov 13, 23:49

**「Background」** Amazon&\#x27;s reported plan follows a broader contest over AI shopping agents, which The Verge has previously reported are being blocked by retailers including Amazon, The RealReal, Target, and Meta. According to Reuters&\#x27; reporting, the World Product Graph would serve at least one other function: countering alternative AI shopping agents. Amazon has disputed the characterization of the internal document, saying it is an outdated brainstorm, and no launch has been confirmed.

**「Impact」** If built as described, the index would position Amazon as an intermediary for product data beyond its own catalog, which matters to retailers whose listings could be surfaced through Amazon and to developers building AI shopping agents that may depend on such an index. The report does not specify access terms, so compatibility and usage conditions for third parties remain unknown.

<details><summary>References</summary>
<ul>
<li><a href="https://www.reuters.com/business/media-telecom/amazons-plan-own-worlds-product-data-fight-ai-shopping-agents-2026-11-13/">Amazon’s plan to own the world’s product data and fight AI ...</a></li>
<li><a href="https://explainx.ai/blog/amazon-world-product-graph-reuters-ai-shopping-agents-draft-memo-claimed-vs-verified-2026">Amazon World Product Graph: What Reuters Found vs Confirmed ...</a></li>

</ul>
</details>

**Tags**: `#AI search`, `#e-commerce`, `#product data`, `#Amazon`, `#AI agents`

---

<a id="item-tech-news-5"></a>
### [ChatGPT Wallet lets OpenAI&\#x27;s Dots agents make purchases](https://www.theverge.com/ai-artificial-intelligence/1033425/openai-chatgpt-wallet) ⭐️ 7.0/10

OpenAI is rolling out ChatGPT Wallet starting November 13 for ChatGPT Pro subscribers in the US who are 18 or older, have a US billing address, and use eligible US-issued American Express, Chase, Mastercard, or Visa cards. After adding a card, Dots agents can buy items in response to prompts, but each purchase requires a check-in and a biometric security check such as Face ID or a fingerprint scan before checkout. The wallet uses payment tokens issued by the card networks in place of the user&\#x27;s real card number, according to the Telegram summary. The Verge&\#x27;s supplied content is truncated, so full terms and limits are not available.

rss · The Verge · Nov 13, 20:45

**「Background」** ChatGPT Wallet builds on OpenAI&\#x27;s Dots agent platform, which the company launched earlier in 2026 as always-on agents that work toward user-set goals in ChatGPT, each with its own cloud computer and app integrations. The wallet gives those agents a payment method, but purchases still require per-transaction user approval and biometric verification.

**「Impact」** Eligible Pro subscribers can now delegate purchases to Dots agents, but the per-purchase biometric approval means agents cannot complete checkouts unattended. Users outside the US, on other ChatGPT plans, or with cards from issuers not listed are excluded from this rollout.

<details><summary>References</summary>
<ul>
<li><a href="https://supergok.com/openai-dots/">OpenAI Dots Bring Always-On AI Agents to ChatGPT</a></li>
<li><a href="https://www.dragapp.com/blog/openai-dots/">OpenAI Dots and Email: What a Dot Can Do With Your Inbox ( 2026 )</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#OpenAI`, `#agentic commerce`, `#payments`, `#AI industry`

---

<a id="item-tech-news-6"></a>
### [Jensen Huang&\#x27;s Departure Said to Cut AI Startup Funding](https://techcrunch.com/2026/11/13/jensen-huangs-departure-blasts-big-hole-in-ai-startup-funding-vcs-and-founders-say/) ⭐️ 7.0/10

Nvidia&\#x27;s investment in AI startups, described as tens of billions of dollars under Jensen Huang, is reportedly ending with his departure, according to TechCrunch. Founders and venture capitalists cited in the report expect smaller checks and lower valuations as a result. The item provides no figures for the investment total, no named sources, and no confirmation from Nvidia, so the scale and timing of any funding change remain unverified.

rss · TechCrunch AI · Nov 13, 22:43

**「Background」** Nvidia&\#x27;s startup investing under Huang was substantial: the company held $48 billion in stakes across 229 private companies, including OpenAI and Anthropic, as of the end of July, according to The New York Times. TechCrunch separately reported that Huang&\#x27;s resignation raised questions about Nvidia&\#x27;s commitment to open-source AI, including its Hugging Face acquisition and open-weight models.

**「Impact」** If the reported change holds, AI startups that counted on Nvidia as an investor would face tighter funding and lower valuations, and founders would need to line up alternative backers. Because the report lacks confirmed figures or company statements, the size of that gap is not yet established.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/13/technology/jensen-huang-silicon-valley-start-ups.html">Jensen Huang ’s Resignation From Nvidia Worries the A . I . Start - Up ...</a></li>
<li><a href="https://techcrunch.com/2026/11/12/jensen-huangs-exit-puts-nvidias-support-for-open-source-in-question/">Jensen Huang ’s exit puts Nvidia ’s support for open... | TechCrunch</a></li>

</ul>
</details>

**Tags**: `#AI startups`, `#venture capital`, `#Nvidia`, `#industry news`, `#funding`

---

<a id="item-tech-news-7"></a>
### [Report: China&\#x27;s Top AI Models Trained on Banned Nvidia Chips](https://techcrunch.com/2026/11/13/export-banned-nvidia-chips-are-behind-chinas-most-powerful-ai-models-uh-oh-jensen/) ⭐️ 7.0/10

New research reportedly indicates that China&\#x27;s most advanced AI models were trained on Nvidia chips covered by export bans, according to a TechCrunch report. The source provides only a one-sentence summary of the research, with no details on methodology, which specific chips or models were involved, or how the finding was established. The claim therefore remains unverified from the supplied material, and it is unclear whether the research has been published or independently reviewed.

rss · TechCrunch AI · Nov 13, 18:40

**「Background」** The item provides no details on the research&\#x27;s methodology, the specific chips involved, or how the models were identified. Earlier reporting cited in search results described U.S. scrutiny of Chinese AI firms&\#x27; access to advanced Nvidia chips, including a July 2026 accusation by a White House official that Moonshot AI had accessed banned Nvidia chips and August 2026 reporting that Chinese firms were tapping Nvidia computing power overseas, prompting lawmakers to weigh closing a cloud-access gap.

**「Impact」** The finding, if confirmed, would suggest that U.S. export controls have not kept banned Nvidia hardware out of the training pipelines behind China&\#x27;s leading models. It also bears on enforcement debates beyond direct shipments: earlier reporting described Chinese AI firms accessing advanced Nvidia compute through overseas subsidiaries and cloud access, gaps U.S. lawmakers have weighed closing. The source provides no methodology or chip specifics, so the scale of any circumvention remains unverified.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/07/23/moonshot-kimi-nvidia-ai-chips-export-ban.html">China&#x27;s Moonshot AI accessed banned Nvidia chips, U.S ... - CNBC</a></li>
<li><a href="https://www.cnbc.com/2026/08/19/china-ai-nvidia-chips-us-export-controls.html">China AI firms tap Nvidia power overseas as U.S ... - CNBC</a></li>
<li><a href="https://www.cnbc.com/2026/08/19/china-ai-nvidia-chips-us-export-controls.html">China AI firms tap Nvidia power overseas as U.S ... - CNBC</a></li>
<li><a href="https://www.cnbc.com/2026/05/31/us-takes-step-to-halt-nvidia-ai-chip-shipments-to-chinese-firms-outside-china.html">U.S. takes step to halt Nvidia AI chip shipments to Chinese ...</a></li>

</ul>
</details>

**Tags**: `#AI hardware`, `#export controls`, `#Nvidia`, `#China AI`, `#AI policy`

---

<a id="item-tech-news-8"></a>
### [Check Point Gateways Hit by PHP2Shell Attacks Deploying ESXi Wiper](https://www.bleepingcomputer.com/news/security/check-point-gateways-hacked-via-php2shell-to-deploy-vmware-esxi-wiper/) ⭐️ 7.0/10

Check Point Software released emergency hotfixes for a high-severity flaw in Security Gateway devices that attackers have exploited since late October to gain root privileges and establish persistence. According to BleepingComputer, vulnerable gateways were targeted in PHP2Shell attack chains that deployed data-wiping malware on VMware ESXi hosts. The report does not specify affected firmware versions, the vulnerability identifier, or whether exploitation was observed in the wild beyond the described campaign. The hotfixes are the vendor&\#x27;s response; the source does not state how widely they have been applied.

rss · BleepingComputer · Nov 13, 16:21

**「Background」** Check Point released emergency hotfixes for CVE-2026-123039, a high-severity flaw it said had been exploited since late October to gain root privileges and establish persistence on vulnerable Security Gateways. According to Check Point, the PHP2Shell flaws provided initial access, after which attackers escalated privileges through the DynamicCLI interface \(CVE-2026-123039\) and deployed PHP web shells, the TSGA backdoor, and its embedded TSProxy networking component.

**「Operational impact」** Defenders should treat Check Point Security Gateway appliances as compromised until patched and verified, since the reported chain moves laterally to VMware ESXi hosts over SSH using the vpxuser service account and runs a Linux ELF wiper named destroy\_v6 that recursively deletes all files regardless of extension. That means ESXi hosts reachable from a compromised gateway may need credential review and integrity checks, not just gateway hotfixing.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/check-point-patches-zero-day-that-lets-hackers-get-root-access/">Check Point warns of zero-day flaw exploited for root access</a></li>
<li><a href="https://thehackernews.com/2026/11/hackers-exploit-php2shell-flaws-in.html">Hackers Exploit PHP 2 Shell Flaws in Check Point Gateways to Deploy...</a></li>
<li><a href="https://thehackernews.com/2026/11/hackers-exploit-php2shell-flaws-in.html">Hackers Exploit PHP2Shell Flaws in Check Point Gateways to Deploy...</a></li>

</ul>
</details>

**Tags**: `#security`, `#malware`, `#VMware ESXi`, `#Check Point`, `#vulnerability exploitation`

---

<a id="item-tech-news-9"></a>
### [ICML 2027 Adds Two-Stage Review and Reviewer Quotas](https://www.reddit.com/r/MachineLearning/comments/1xvkxbj/icml_2027_changes_d/) ⭐️ 7.0/10

ICML 2027&\#x27;s call for papers introduces a two-stage review process in which an area chair decides whether a paper proceeds to full review, and any proposed first-stage rejection must be confirmed by a senior area chair, with authors receiving a short justification by February 23. The policy also caps participation at 20 submissions per person, requires every paper to name a reciprocal reviewer from its author list \(with a maximum of 6 papers per reviewer\), and obliges anyone with 3 or more submissions to serve on the program committee. Non-compliant papers may be desk rejected, and each author may be on at most one paper that has no eligible reciprocal reviewer among its authors. These details come from a Reddit user&\#x27;s reading of the CFP rather than an official announcement.

reddit · r/MachineLearning · /u/Gravitist · Nov 13, 21:53

**「Background」** The ICML 2027 call for papers introduces reciprocal reviewing, a model in which authors commit to reviewing as a condition of submission. IJCAI 2027&\#x27;s main-track call describes the same reciprocal-reviewing requirement as a way to keep the review process sustainable and timely. ICML&\#x27;s 2026 peer-review FAQ also notes that nominations from that cycle will be passed to the ICML 2027 program chairs.

**「Who is affected」** Authors with heavy submission volumes now face a direct trade-off between paper count and reviewing duty, and papers listing coauthors who cannot review—such as undergraduates, interns, or researchers outside the field—consume the single no-eligible-reviewer allowance. Because non-compliance can trigger desk rejection, submitting teams should confirm reviewer eligibility and program committee obligations before the deadline.

<details><summary>References</summary>
<ul>
<li><a href="https://icml.cc/Conferences/2026/PeerReviewFAQ">ICML 2026 Peer Review FAQ</a></li>
<li><a href="https://2027.ijcai.org/ijcai-2027-call-for-papers-main-track/">IJCAI 2027 Call for papers (Main Track) – IJCAI 2027</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#peer-review`, `#conference-policy`, `#icml`, `#research-community`

---

<a id="item-tech-news-10"></a>
### [Shanghai investigation faults ethics and consent in gene-editing death](https://mp.weixin.qq.com/s/p0iC3tcI1yr10EBl2NjUvg) ⭐️ 7.0/10

Shanghai authorities investigating a customized gene-editing therapy given to a child with Snijders Blok-Campeau syndrome found deficiencies in preclinical research, ethics review, and informed consent, and said some personnel accepted about 1.06 million yuan from the family. The child died in March 2025 from thrombotic microangiopathy after the injection, and a paper on the case was published in Nature in February 2026, according to the Xinhua relay. The investigation resulted in the dismissal of Qiu and Yang and a five-year disqualification, while the involved institutions were summoned for rectification and received administrative penalties. The account comes from a brief Telegram relay of Xinhua and could not be independently verified from the supplied material.

telegram · zaihuapd · Nov 13, 09:24

**「Background」** The case centers on a paper published in Nature in February 2026 by a team led by neuroscientist Zilong Qiu of Shanghai Jiao Tong University School of Medicine, describing preclinical work for a gene-editing treatment for Snijders Blok-Campeau syndrome. Reporting in July 2026 by Science and Retraction Watch disclosed that a young girl had died after receiving the experimental therapy, prompting journal and university investigations. The Shanghai investigation now concludes that the preclinical research, ethics review, and informed consent were deficient, and that staff accepted about 1.06 million yuan from the family.

**「Impact」** The findings tie the case&\#x27;s failure to specific procedural gaps—preclinical work, ethics review, and consent—and to payments from the family, giving regulators a documented basis for institutional penalties and a five-year ban on the named personnel. Researchers and institutions offering customized therapies for rare diseases face heightened scrutiny of ethics approval and consent documentation, though the source does not specify new rules or broader policy changes.

<details><summary>References</summary>
<ul>
<li><a href="https://retractionwatch.com/2026/07/30/nature-university-china-investigations-gene-editing-death-science/">Journal, university investigations launched into gene-editing ...</a></li>
<li><a href="https://www.livescience.com/health/genetics/6-year-old-in-china-dies-after-experimental-treatment-investigation-finds-raising-questions-about-the-countrys-gene-therapy-regulations">An experimental gene therapy killed a 6-year-old girl in ...</a></li>

</ul>
</details>

**Tags**: `#gene-editing`, `#research-ethics`, `#biotech-regulation`, `#clinical-trials`, `#China`

---

<a id="item-tech-news-11"></a>
### [Python 早期贡献者 Tim Peters 去世，享年 74 岁](https://x.com/Itsfoss/status/2120957452937998716) ⭐️ 7.0/10

Python 创造者 Guido van Rossum 宣布，早期 Python 贡献者 Tim Peters 去世，享年 74 岁。Peters 是 Python 的第二位真实用户，撰写了《Python 之禅》（PEP 20），并开发了 Timsort 排序算法。他还在 Python 软件基金会董事会任职 13 年。该消息来自一条简短的社交媒体转发，未提供死因或其他细节。

telegram · zaihuapd · Nov 13, 09:55

**「Background」** Timsort, the hybrid sorting algorithm Peters created, was adopted as Python&\#x27;s default list-sorting algorithm and has also been used in other language runtimes. PEP 20, the Zen of Python, is a set of aphorisms written by Peters in June 1999 that summarizes the language&\#x27;s design philosophy and is accessible in Python via \`import this\`.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tim_Peters_%28software_engineer%29">Tim Peters (software engineer) - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/Tim_Peters_%28software_engineer%29">Tim Peters (software engineer) — Grokipedia</a></li>

</ul>
</details>

**Tags**: `#python`, `#open-source`, `#community`, `#algorithms`, `#obituary`

---

<a id="item-tech-news-12"></a>
### [DeepSeek 开放应用 API，支持服务端工具调用](https://mp.weixin.qq.com/s/78KBHc4-4N5b2vfL9SkutQ) ⭐️ 7.0/10

DeepSeek 发布了一套应用 API，开发者只需在现有 API 中开启相应参数，即可获得深度思考搜索、文件输入、链接阅读和语音等对话能力，工具调用与上下文拼接由服务端自动完成。据该 Telegram 帖子称，V4.1-Flash 模型已在三个接口中支持这些能力，Search、Fetch、OCR、ASR 和 TTS 也可单独调用。DeepSeek 还开源了一个前端聊天演示，可导入历史对话，并提供了托管体验地址。该帖子未说明定价、速率限制或确切的接口名称，因此这些细节仍未确认。

telegram · zaihuapd · Nov 13, 14:27

**「Background」** DeepSeek&\#x27;s API documentation lists Search, Fetch, OCR, ASR, and TTS as standalone APIs for custom workflows, and the same docs page references the DeepSeek-V4.1-Flash-1017 model. The new application API builds on that existing model and tool set by letting developers enable the bundled capabilities through parameters in the original API rather than calling each service separately.

**「影响」** 开发者现在可以通过现有 API 参数获得搜索、抓取、OCR 和语音能力，而无需自行编排这些工具；需要单独控制某一能力的团队则可以直接调用对应的独立接口。开源聊天演示还提供了一个可本地部署的参考前端，可导入历史对话。

<details><summary>References</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/news/news261113/">The full DeepSeek App experience, now via API | DeepSeek API Docs</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#API`, `#LLM tooling`, `#open source`, `#speech/OCR`

---

<a id="item-tech-news-13"></a>
### [SpaceX 裁撤约 60 名 Grok Imagine 研发人员](https://weibo.com/1642634100/RreMyi69Y) ⭐️ 7.0/10

据新浪科技经 Telegram 频道转述的报道，SpaceX 上周裁撤了 Grok Imagine 约 60 名研发人员，仅留少量人员维持这款视频与图像生成工具的基本运转。产品目前仍可正常使用，但专职团队解散后前景不明。报道称，SpaceX 今年 2 月以价值 2500 亿美元股票收购 xAI 后，重心转向 AI 代码工具与 GrokBot 智能体，8 月又以 600 亿美元收购 AI 代码初创公司 Cursor。上述裁员人数与收购金额均来自单一聚合来源，尚无 SpaceX 或 xAI 的公开确认。

telegram · zaihuapd · Nov 13, 15:00

**「Background」** The reported layoffs follow SpaceX&\#x27;s acquisition of xAI in February and its $60 billion purchase of AI coding startup Cursor in August, moves that shifted the company&\#x27;s focus toward coding tools and agents. External reports also describe Grok Bot&\#x27;s costs as &quot;unsustainably high&quot; and note that xAI was acquired by SpaceX in February.

**「影响」** 对 Grok Imagine 用户而言，工具眼下仍可使用，但仅靠少量人员维护意味着功能更新与问题修复可能放缓；依赖该工具进行视频和图像生成的开发者应评估替代方案。

<details><summary>References</summary>
<ul>
<li><a href="https://www.forbes.com/sites/siladityaray/2026/11/02/musk-says-grok-bots-costs-were-unsustainably-high-weeks-after-touting-rapid-growth/">Elon Musk Says Grok Bot Costs Were ‘Unsustainably High’ Amid...</a></li>
<li><a href="https://www.nbcnews.com/tech/tech-news/musks-ai-chatbot-grok-xai-making-sexual-deepfakes-imagine-rcna265855">Musk’s AI chatbot Grok is still making sexual deepfakes</a></li>

</ul>
</details>

**Tags**: `#AI industry`, `#layoffs`, `#Grok Imagine`, `#xAI`, `#generative media`

---