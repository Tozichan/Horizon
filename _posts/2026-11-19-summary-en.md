---
layout: default
title: "Horizon Summary: 2026-11-19 (EN)"
date: 2026-11-19
lang: en
---

> From 71 items, 15 important content pieces were selected

---

**Technology News**
1. [Xint discloses NGINX2Root chain: five nginx flaws to host root](#item-tech-news-1) ⭐️ 9.0/10
2. [Google Releases Gemini 4 Neon Model](#item-tech-news-2) ⭐️ 9.0/10
3. [Ruby Discloses Memory-Corruption Bugs in Regexp and String Case Conversion](#item-tech-news-3) ⭐️ 8.0/10
4. [Anthropic Reportedly Prices IPO at $83 a Share](#item-tech-news-4) ⭐️ 8.0/10
5. [Microsoft Agent Framework PyPI package hit by credential-stealing compromise](#item-tech-news-5) ⭐️ 8.0/10
6. [Microsoft Announces Seven New Models at Ignite 2026](#item-tech-news-6) ⭐️ 7.0/10
7. [Quad9 Leaves France Over DNS Blocking Orders](#item-tech-news-7) ⭐️ 7.0/10
8. [LLM Agents for Reverse Engineering, With Limits](#item-tech-news-8) ⭐️ 7.0/10
9. [Google DeepMind&\#x27;s Genie 4 announced as available](#item-tech-news-9) ⭐️ 7.0/10
10. [OpenAI details using its models for chip design](#item-tech-news-10) ⭐️ 7.0/10
11. [Apache Patches Actively Exploited Roller RCE Flaw](#item-tech-news-11) ⭐️ 7.0/10
12. [Voyager 1 Reaches One Light-Day From Earth After 49 Years](#item-tech-news-12) ⭐️ 7.0/10
13. [US Weighs Requiring Firms to Disclose Chinese AI Use](#item-tech-news-13) ⭐️ 7.0/10

**Financial News**
1. [Tencent Q3: AI spending surges, free cash flow turns negative](#item-finance-news-1) ⭐️ 7.0/10
2. [China and South Korea announce substantive conclusion of FTA services and investment talks](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Xint discloses NGINX2Root chain: five nginx flaws to host root](https://nginx2root.com/) ⭐️ 9.0/10

Xint publicly disclosed NGINX2Root, a chain of five nginx vulnerabilities plus a Linux kernel flaw that, combined, can take an unauthenticated nginx visitor to host root. The key link, CVE-2026-123007, is an HTTP/2 flow-control memory-corruption bug that allows command execution inside an nginx worker without authentication. nginx 1.30.7 and 1.31.9, released November 18, fix 10 CVEs; Rapid7 has published a proof of concept, and no in-the-wild exploitation has been reported. The disclosure advises disabling external HTTP/2 where upgrading is not possible.

telegram · zaihuapd · Nov 18, 16:21

**「Background」** CVE-2026-123007 is an HTTP/2 flow-control memory-corruption flaw \(CWE-191, integer underflow\) rated 9.2 Critical, which Rapid7 describes as permitting remote code execution in the nginx worker context; Ubuntu&\#x27;s advisory notes it is a data-plane issue with no control-plane exposure. The chain matters because the worker compromise is only the first step, with a separate Linux kernel flaw used to escalate to host root.

**「Impact」** Operators running nginx with HTTP/2 enabled should upgrade to 1.30.7 or 1.31.9; the source states that those unable to upgrade should disable external HTTP/2, which removes the unauthenticated worker-level entry point described for CVE-2026-123007. A commenter notes HTTP/2 is not enabled by default in nginx and cites W3Techs data that about 12% of servers use it, so exposure depends on configuration rather than every nginx deployment.

**「Community discussion」** Commenters noted that the fix appeared in the open-source repository about a week before the coordinated release, with a commit message crediting Xint.io, and argued that a public advisory to disable HTTP/2 during that window would have been warranted. Others pointed out that HTTP/2 is not enabled by default in nginx and is used by roughly 12% of servers, while one commenter claimed the exploit requires about 128 GB of HTTP/2 traffic and specific CPU instructions, calling it a non-issue.

<details><summary>References</summary>
<ul>
<li><a href="https://ubuntu.com/security/CVE-2026-123007">CVE - 2026 - 123007 | Ubuntu</a></li>
<li><a href="https://www.rapid7.com/blog/post/ve-cve-2026-123007-critical-nginx-http-2-integer-underflow-leads-to-rce-fixed/">Rapid7 discloses a critical vulnerability affecting NGINX HTTP / 2 that...</a></li>
<li><a href="https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities">Unauthenticated Remote Code Execution in NGINX ... | Wiz Blog</a></li>

</ul>
</details>

**Tags**: `#nginx`, `#vulnerability disclosure`, `#remote code execution`, `#HTTP/2`, `#security`

---

<a id="item-tech-news-2"></a>
### [Google Releases Gemini 4 Neon Model](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) ⭐️ 9.0/10

Google released Gemini 4 Neon, a frontier model aimed at complex software engineering, knowledge work, and research workflows, available to developers, enterprises, and Google AI Pro/Ultra subscribers. Google lists pricing at $3 per million input tokens \($0.15 cached\) and $15 per million output tokens, with a 1M-token context window. The company claims Neon ranks first on the Artificial Analysis coding agent index \(58.6\), third on its intelligence index at the xhigh setting \(61\), and scores 65.2% on Terminal-Bench 4.1, with default high-setting cost per task 32% lower than Carbon. These are vendor-published benchmark and pricing figures relayed in a brief secondary summary, not independently verified results.

telegram · zaihuapd · Nov 19, 02:00

**「Background」** Gemini 4 Neon joins an existing Gemini 4 family that already includes Gemini 4 Carbon, which the source treats as the comparison baseline for cost and positioning. According to Artificial Analysis, Neon is priced at $3/$15 per million input/output tokens, 50% above Carbon&\#x27;s currently discounted $2/$10 rate \(which ends November 30\) and 25% below Carbon&\#x27;s standard $4/$20, and it adds an xhigh effort level introduced in the recent Hydrogen release. The source&\#x27;s claim that Neon&\#x27;s default high tier cuts per-task cost 32% versus Carbon is a vendor comparison rather than an independently measured result.

**「Impact」** Developers choosing between Gemini models face a trade-off: commenters note that although Neon scores higher overall, Google still positions Carbon as its long-horizon model, with Carbon reportedly scoring higher on research-scale evaluations such as CritPt. Teams should therefore match model choice to task type rather than defaulting to the newest release.

**「Community Discussion」** Commenters criticized the proliferation of model names \(Neon, Carbon, Sol, Astra, Opus, and others\) as hard to map to use cases, and one asked whether Google&\#x27;s naming scheme encodes model size class. Others reported that Neon is served on OpenRouter at about 127 tokens per second versus 46 for Carbon, which one commenter found surprising given Neon&\#x27;s positioning, while another argued that benchmarks do not capture the perceived quality gap versus Anthropic&\#x27;s Opus 5.5.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/articles/gemini-4-neon-intelligence-gain">Google continues to accelerate its release cadence with ...</a></li>

</ul>
</details>

**Tags**: `#google`, `#gemini`, `#llm-release`, `#software-engineering`, `#benchmarks`

---

<a id="item-tech-news-3"></a>
### [Ruby Discloses Memory-Corruption Bugs in Regexp and String Case Conversion](https://www.ruby-lang.org/en/news/2026/11/18/multiple-vulnerabilities-in-regexp-and-string/) ⭐️ 8.0/10

Ruby published a security advisory on 2026-11-18 covering multiple memory-corruption vulnerabilities in its Regexp handling and String case conversion. The advisory credits Stephan Lipp of Ada Logics and Anthropic for reporting at least one of the issues, according to a commenter citing the linked GitHub security advisory. The source provides no affected version list, patch versions, or severity ratings, so the scope of fixed releases is not established here. The disclosure is a patch advisory rather than a report of a new capability.

hackernews · runesoerensen · Nov 18, 23:52 · [Discussion](https://news.ycombinator.com/item?id=50554038)

**「Background」** Ruby&\#x27;s advisory covers seven vulnerabilities in its regular expression engine and string case conversion, and the project released Ruby 4.0.10, 3.4.13 and 3.3.14 to fix them. One flaw, GHSA-87fm-7w84-j2px, is an integer overflow in case conversion that causes a heap-based buffer overflow; Ruby says it is aware of proofs of concept showing remote code execution in some scenarios. A separate issue involves converting a crafted regular expression to a string, which may allow information disclosure or remote code execution in applications that compile attacker-controlled patterns.

**「Impact」** Because the flaws are C-level memory-corruption bugs, Ruby deployments that process untrusted strings or regular expressions should treat the advisory as requiring a prompt upgrade once fixed versions are identified. Commenters demonstrated that case conversion on crafted input can produce incorrect buffer sizes, which is the kind of condition that can lead to out-of-bounds writes rather than a simple exception.

**「Community Discussion」** Commenters dissected specific mechanics: tptacek described a Windows-1252 upcasing path where a trailing German sharp &\#x27;s&\#x27; \(ß\) expands to &quot;SS&quot; while the buffer check appears to advance one character at a time, and pentestercrab posted a Shift\_JIS downcase example with a 4,294,967,302-byte string that produced anomalous output on an unfixed version. rvz argued that autonomous AI models finding such bugs in established software shows memory-unsafe languages are exposed, and raised the prospect of attackers using non-disclosing models at scale; these are opinions and interpretations, not confirmed findings.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ruby-lang.org/en/news/2026/11/18/multiple-vulnerabilities-in-regexp-and-string/">Security advisories: multiple vulnerabilities in Regexp and ...</a></li>
<li><a href="https://seclists.org/oss-sec/2026/q4/782">Ruby: multiple vulnerabilities in Regexp and String case ...</a></li>
<li><a href="https://www.openwall.com/lists/oss-security/2026/11/19/1">oss-security - Ruby: multiple vulnerabilities in Regexp and ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#ruby`, `#memory-safety`, `#vulnerability-disclosure`, `#ai-assisted-security`

---

<a id="item-tech-news-4"></a>
### [Anthropic Reportedly Prices IPO at $83 a Share](https://techcrunch.com/2026/11/18/anthropic-reportedly-prices-ipo-at-83-a-share-above-projected-range/) ⭐️ 8.0/10

Anthropic reportedly priced its IPO at $83 per share, above its projected range, according to TechCrunch. The report says the offering values the company at $1.5 trillion on a fully diluted basis. The supplied source is a brief report and the pricing is described as reported rather than confirmed by the company, so the figures remain unverified here.

rss · TechCrunch AI · Nov 18, 22:11

**「Background」** The $83 price came in above earlier estimates of $80, and Bloomberg reported last week that the shares were oversubscribed by as much as 6x, according to Yahoo Finance&\#x27;s live coverage. ZeroHedge reported that at $83, buyers are paying 18.4x a cited run rate on a fully diluted basis \(13.4x on shares outstanding\).

<details><summary>References</summary>
<ul>
<li><a href="https://www.zerohedge.com/markets/anthropic-prices-83-raises-record-94-billion-its-own-chip-suppliers-holding-floor">Anthropic IPO Prices At $ 83 , Raises A Record $107... | ZeroHedge</a></li>
<li><a href="https://finance.yahoo.com/technology/live/anthropic-ipo-live-company-said-to-price-stock-at-83-begin-trading-thursday-212656452.html">Anthropic IPO live: Company said to price stock at $ 83 , begin trading...</a></li>

</ul>
</details>

**Tags**: `#anthropic`, `#ipo`, `#ai-industry`, `#tech-business`

---

<a id="item-tech-news-5"></a>
### [Microsoft Agent Framework PyPI package hit by credential-stealing compromise](https://www.bleepingcomputer.com/news/security/microsofts-agent-framework-pypi-package-compromised-to-steal-credentials/) ⭐️ 8.0/10

Microsoft&\#x27;s official Agent Framework Python package on PyPI was compromised, with attackers publishing two malicious versions intended to steal cloud credentials and other sensitive data from developers&\#x27; systems. The report identifies the package and the credential-theft intent but does not specify the malicious version numbers, the attack vector, or remediation steps. Developers with the package in their dependency trees should treat any installed copy as potentially untrusted until Microsoft or PyPI publishes affected versions and guidance.

rss · BleepingComputer · Nov 18, 16:58

**「Background」** Microsoft&\#x27;s Agent Framework is a Python package for building AI agents and multi-agent applications, distributed through PyPI. According to SecurityWeek, the malicious versions were published on November 17, 2026, and could expose cloud and CI/CD credentials of users who installed them; Chainguard reports it detected and blocked the attack. The supplied excerpt does not describe the attack vector or remediation steps.

**「Impact」** Because the compromised package is an official Microsoft release distributed through PyPI, any project that pulled the affected versions could expose cloud credentials and other secrets from the developer&\#x27;s machine or build environment. Until affected version numbers and a fix are published, teams should audit lockfiles and CI logs for installs of the Agent Framework package and rotate any credentials that may have been present in those environments.

<details><summary>References</summary>
<ul>
<li><a href="https://www.chainguard.dev/unchained/microsoft-agent-framework-compromised-on-pypi-november-2026">Microsoft agent-framework compromised on PyPI: 1.26.1 and 1. ...</a></li>
<li><a href="https://www.securityweek.com/microsoft-agent-framework-releases-poisoned-with-credential-stealer/">Microsoft Agent Framework Releases Poisoned With Credential ...</a></li>

</ul>
</details>

**Tags**: `#supply-chain-security`, `#pypi`, `#ai-agents`, `#credential-theft`, `#microsoft`

---

<a id="item-tech-news-6"></a>
### [Microsoft Announces Seven New Models at Ignite 2026](https://microsoft.ai/news/microsoft-ignite-2026/) ⭐️ 7.0/10

Microsoft announced seven new AI models at Ignite 2026, positioning them around scalable price-performance. The announcement itself carries no detailed technical specifications in the supplied material, so the concrete capabilities, parameter counts, licensing terms, and availability remain unverified beyond the vendor&\#x27;s framing. A commenter who says they tested MAI Code 2 reports it has been &quot;quite good&quot; for their usual work and roughly on par with Opus or Sol, though this is one user&\#x27;s impression rather than an independently measured benchmark.

hackernews · gmays · Nov 18, 16:08 · [Discussion](https://news.ycombinator.com/item?id=50548021)

**「Background」** Microsoft&\#x27;s Ignite 2026 announcement introduced the seven models as a family, with Microsoft claiming MAI Code 2 reaches 98% of GPT-6.1 Sol&\#x27;s coding quality at about 40% of the price and MAI Cyber 2 Flash beats GPT-6 Astra&\#x27;s quality at under 2% of the cost per task on the CyberGym-E2E benchmark. Microsoft also announced the Maia 200 AI accelerator and a program allowing customers to license MAI model weights and run them in their own environments, which is the context for the community debate over open-weight strategy.

**「Why It Matters」** For teams choosing models on cost, the announcement adds another claimed price-performance option, but the absence of published benchmarks or licensing details in the supplied material means buyers cannot yet verify the comparison against Anthropic or OpenAI models. One commenter argues Microsoft should release some models as open source or open weight to secure market share, framing closed distribution as a competitive risk.

**「Community Reaction」** Commenters split between hands-on praise and skepticism: one reported positive results testing MAI Code 2 and credited Microsoft for building from scratch, while others questioned the keynote&\#x27;s depth and argued the models need open-weight distribution to gain traction. A separate thread debated whether cheaper competing models undermine Anthropic&\#x27;s pricing ahead of its IPO, which is an opinion about market dynamics rather than a confirmed fact.

<details><summary>References</summary>
<ul>
<li><a href="https://microsoft.ai/news/microsoft-ignite-2026/">Seven new world-class models at scalable price-performance ...</a></li>
<li><a href="https://microsoft.ai/news/microsoft-ignite-2026-mai-keynote/">Microsoft Ignite 2026: MAI keynote transcript | Microsoft AI</a></li>
<li><a href="https://www.linkedin.com/pulse/microsoft-ignite-2026-seven-new-mai-models-chip-your-own-ivana-tilca-hxyef">Microsoft Ignite 2026: Seven New MAI Models, a New Chip, and ...</a></li>

</ul>
</details>

**Tags**: `#AI models`, `#Microsoft`, `#price-performance`, `#model competition`, `#open source`

---

<a id="item-tech-news-7"></a>
### [Quad9 Leaves France Over DNS Blocking Orders](https://techstackups.com/articles/quad9-leaves-france-dns-blocking/) ⭐️ 7.0/10

An opinion piece on techstackups.com argues that DNS resolvers are the wrong mechanism for enforcing anti-piracy blocking, using Quad9&\#x27;s withdrawal from France as its framing case. The supplied material contains only the article title and reader comments, so the specific court orders, dates, and terms of Quad9&\#x27;s exit cannot be verified here. Commenters link to Quad9&\#x27;s and Cloudflare&\#x27;s own blog posts on the withdrawal, but those pages were not supplied as source content.

hackernews · ritzaco · Nov 18, 13:18 · [Discussion](https://news.ycombinator.com/item?id=50545958)

**「Background」** Quad9 is a global public recursive DNS resolver that blocks domains associated with malware and phishing. The French case stems from a court order obtained by beIN Sports requiring DNS-level blocking of piracy-related domains; rather than comply, Quad9 announced it would stop serving users in France, with the withdrawal reported for November 24, 2026. Cloudflare characterized the French court&\#x27;s penalty order against Quad9 as the culmination of rightsholder efforts to mandate DNS-level blocking.

**「Why It Matters」** The debate centers on whether French judges were correctly applying a flawed law or overreaching, a distinction commenter skrebbel says much coverage of the decision fails to make. That question determines whether pressure for change should target courts or lawmakers, and it bears directly on whether resolver operators elsewhere can expect similar blocking demands.

**「Community Reaction」** Commenters split on the root cause: trentnix argues any anti-piracy measure short of prosecution is a backdoor to suppressing speech, while skrebbel asks whether the fault lies with judges or the law they interpreted. bemttevi contends enforcement is futile without a better legal viewing experience, citing per-movie DRM-free downloads as an example, and AppalachianEng argues commercial AI training on copyrighted works goes unprosecuted while individuals are targeted.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad 9 - Wikipedia</a></li>
<li><a href="https://techstackups.com/articles/quad9-leaves-france-dns-blocking/">Quad 9 Is Leaving France : Why DNS Resolvers Are... | Tech Stackups</a></li>
<li><a href="https://blog.cloudflare.com/quad9-withdrawal-from-france/">Quad 9 ’s withdrawal from France : A canary in the coal... | Cloudflare Blog</a></li>

</ul>
</details>

**Tags**: `#DNS`, `#internet-policy`, `#censorship`, `#piracy`, `#network-infrastructure`

---

<a id="item-tech-news-8"></a>
### [LLM Agents for Reverse Engineering, With Limits](https://www.slowchronicle.com/posts/llm-assisted-reverse-engineering) ⭐️ 7.0/10

A blog post and accompanying Hacker News discussion examine how LLM agents can assist reverse engineering, focusing on techniques that stop models from guessing and on the limits of that approach for harder targets. The author describes a variation of the scientific method that forces the agent to run definitive experiments, which reportedly breaks the guessing loops that stall it. The discussion is practitioner-level rather than a product release: no specific tool, version, or benchmark result is announced, and the post is a personal write-up rather than an independently measured capability claim.

hackernews · ioma8 · Nov 18, 22:29 · [Discussion](https://news.ycombinator.com/item?id=50553225)

**「Context」** Reverse engineering typically requires forming hypotheses about unknown code or binaries and testing them against observed behavior. The post applies that loop to LLM agents, arguing that without an enforced experiment step the model tends to guess and retry rather than resolve uncertainty.

**「Practical takeaway」** Commenters report that guessing loops are the main annoyance when reverse engineering with Claude, mostly Opus 4.8 due to restrictions on newer models, and that on harder or larger targets the agent must be repeatedly told to stop guessing. One commenter with no reverse-engineering experience said they successfully reverse engineered an abandoned audio effects plugin and a discontinued DSP instrument using this approach.

**「Debate」** One commenter argues the process is what matters because it builds skills and the final result brings satisfaction, and that using AI for reverse engineering delivers neither. Another reports using Codex to unlock premium features in Android apps and reimplement their functionality offline, while a third raises liability questions about shipping agent-generated code that may infringe software patents.

**Tags**: `#reverse-engineering`, `#LLM-agents`, `#AI-assisted-development`, `#software-engineering`, `#community-discussion`

---

<a id="item-tech-news-9"></a>
### [Google DeepMind&\#x27;s Genie 4 announced as available](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/) ⭐️ 7.0/10

Google DeepMind announced that Genie 4, the next version of its generative world model, is now available, according to a post on Google&\#x27;s blog. The supplied item contains no technical details, benchmarks, or release specifics from the announcement itself. Community comments indicate access is described as limited to &quot;Eligible Google AI Ultra subscribers,&quot; with at least one user reporting that their account still shows Genie 3 rather than Genie 4 and uncertainty over whether the gap is regional or a documentation lag. The scope of availability and the model&\#x27;s capabilities therefore remain unconfirmed by the available evidence.

hackernews · leumon · Nov 18, 18:49 · [Discussion](https://news.ycombinator.com/item?id=50550415)

**「Background」** Genie 4 follows earlier DeepMind world-model releases, including Genie 3, which commenters say Google&\#x27;s AI Ultra subscription currently lists. External coverage describes Genie 4 as a natively multimodal world model announced October 27, 2026, adding real-time interactive simulation with native audio, physics, and natural human motion, with steering powered by Gemini models. The supplied item itself contains no technical details or benchmarks, so those capabilities remain vendor claims rather than independently verified results.

**「Access and compatibility」** For prospective users, the practical question is eligibility: a commenter reports that a Google Workspace account could not obtain an AI Ultra subscription and that a personal account still displayed Genie 3, leaving unclear whether Genie 4 is region-restricted or simply not yet reflected in account pages. Users planning to rely on Genie 4 should verify their subscription tier and region before assuming access.

**「Community discussion」** Commenters focused less on the model itself than on access and purpose: one described difficulty determining how to pay Google for the product and whether UK availability differs from the US-only rollout of an earlier Genie version, while another questioned whether DeepMind&\#x27;s output can become profitable. Others discussed whether generative world models could eventually serve as game engines, and one commenter said their main reaction to such releases is not wanting the technology at all.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/">Genie 4 : A new generation of world simulation — Google DeepMind</a></li>
<li><a href="https://genie4.art/">Genie 4 — Google DeepMind &#x27;s Real-Time World Model , Explained</a></li>
<li><a href="https://digg.com/tech/8q57gd3x">Google DeepMind unveils Genie 4 , an AI world model promising...</a></li>

</ul>
</details>

**Tags**: `#generative-ai`, `#world-models`, `#google-deepmind`, `#ai-products`, `#game-engines`

---

<a id="item-tech-news-10"></a>
### [OpenAI details using its models for chip design](https://openai.com/index/advancing-chip-design-with-our-models/) ⭐️ 7.0/10

OpenAI published an account of applying its models to chip design, including work on a chip named Jalapeño. The announcement is a vendor description rather than a released tool or independently measured result, and the supplied material discloses few technical specifics about the models, the design flow, or the resulting hardware. Commenters noted that the post does not appear to share the RISC-V designs it discusses.

hackernews · vighneshiyer · Nov 18, 17:45 · [Discussion](https://news.ycombinator.com/item?id=50549493)

**「Background」** OpenAI&\#x27;s post describes its models optimizing circuits in its own Jalapeño silicon and improving RISC-V core designs, with coverage of the announcement reporting gains of up to 14% PPA versus baselines and work extending to AMD GPU RTL. The item itself is a vendor announcement with limited disclosed technical detail, so the specific methodology and the extent to which designs are shared remain unclear.

**「Impact」** Because the post does not release the RISC-V designs or the models used, engineers cannot reproduce or build on the reported chip-design work from this announcement alone; practitioners interested in the approach would need the underlying artifacts to evaluate it.

**「Community discussion」** One commenter reported treating chip design as a software problem, having an agent write code to generate circuits and automate the EDA flow and then babysit multi-hour simulation runs, while noting that only a small fraction of the design is RTL and the bulk is analog. Others questioned whether the RISC-V designs are being shared and argued that AI companies are increasingly competing with their own customers while withholding models.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/advancing-chip-design-with-our-models/">Advancing chip design with OpenAI models</a></li>
<li><a href="https://explainx.ai/blog/openai-amd-jalapeno-chip-design-astra-ppa-november-2026">OpenAI AMD Chip Design: 14% PPA in 5 Months (Nov 2026 ...</a></li>

</ul>
</details>

**Tags**: `#chip-design`, `#EDA`, `#LLM-agents`, `#RISC-V`, `#AI-industry`

---

<a id="item-tech-news-11"></a>
### [Apache Patches Actively Exploited Roller RCE Flaw](https://www.bleepingcomputer.com/news/security/apache-warns-of-roller-rce-vulnerability-exploited-in-attacks/) ⭐️ 7.0/10

Apache has released security updates for a critical remote code execution vulnerability in Apache Roller that threat actors are actively exploiting to gain code execution on vulnerable servers. The source does not specify the affected or fixed versions, the vulnerability&\#x27;s CVE identifier, or the technical nature of the flaw. Administrators running Roller should treat the update as urgent given the confirmed in-the-wild exploitation, but should consult Apache&\#x27;s advisory for version and mitigation details.

rss · BleepingComputer · Nov 18, 10:35

**「Background」** Apache Roller is an open-source, Java-based blogging platform. The flaw is tracked as CVE-2026-129448 \(CVSS 9.8\) and stems from unauthenticated deserialization in the XML-RPC endpoint, which can lead to remote code execution; Rapid7 notes it is the same vulnerability as CVE-2026-82384, which listed only Roller 6.1.5 as affected. Apache recommends upgrading to Roller 6.1.6 or later, which disables the extension types and rejects XML-RPC requests when that feature is disabled.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/critical-apache-roller-rce-flaw-under.html">Critical Apache Roller RCE Flaw Under Active Exploitation, No ...</a></li>
<li><a href="https://www.rapid7.com/db/vulnerabilities/cve-2026-129448/">CVE-2026-129448: Apache Software Foundation Apache Roller ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#apache`, `#remote-code-execution`, `#open-source`

---

<a id="item-tech-news-12"></a>
### [Voyager 1 Reaches One Light-Day From Earth After 49 Years](https://www.cnn.com/2026/11/18/science/voyager-1-light-day) ⭐️ 7.0/10

Voyager 1 became the first human-made object to reach roughly one light-day from Earth, crossing about 26 billion kilometers at 5:16 a.m. ET on November 18, roughly 49 years after launch. Radio signals now take 24 hours to reach the probe, and NASA says round-trip communication takes about two days. Two science instruments remain operational, and NASA recently adjusted the spacecraft&\#x27;s power supply to save an estimated 10 watts, which it expects to extend the mission by about two and a half years.

telegram · zaihuapd · Nov 18, 14:41

**「Background」** Voyager 1 launched in 1977 and crossed into interstellar space in 2012, making it the most distant spacecraft in operation. Its power comes from radioisotope thermoelectric generators, which lose output each year as the plutonium decays, so NASA has progressively shut down instruments and heaters to keep the probe running.

**「Impact」** Because commands and data now require a two-day round trip, mission operators must plan and troubleshoot Voyager 1 activities with far less real-time control than for closer spacecraft. The roughly 10-watt power saving is NASA&\#x27;s stated basis for the projected two-and-a-half-year extension, so the added operating time depends on that estimate holding.

**Tags**: `#space`, `#voyager`, `#nasa`, `#engineering`, `#science`

---

<a id="item-tech-news-13"></a>
### [US Weighs Requiring Firms to Disclose Chinese AI Use](https://www.reuters.com/world/china/trump-administration-weighs-forcing-us-firms-disclose-chinese-ai-use-2026-11-18/) ⭐️ 7.0/10

The Trump administration is reportedly considering requiring US companies to publicly disclose their use of Chinese AI models, with the Treasury Department and the White House Office of Science and Technology Policy having discussed the proposal. The approach aims to discourage reliance on cheaper Chinese open-weight models through public naming rather than imposing new restrictions. Airbnb, which uses Alibaba&\#x27;s Qwen to support customer service, is cited as an example of a company that would have to post such disclosures on its website if the plan takes effect. It remains unclear whether the proposal has internal government support or will enter a formal legislative process.

telegram · zaihuapd · Nov 19, 02:30

**「Background」** The proposal is framed as an alternative to new restrictions: rather than banning Chinese AI models, it would use public disclosure to discourage US firms from relying on them. The source cites Airbnb&\#x27;s use of Alibaba&\#x27;s Qwen for customer service as an example of the kind of deployment that could require a public notice on the company&\#x27;s website. The Treasury Department and the White House Office of Science and Technology Policy have discussed the idea, but it remains unclear whether it has internal support or will enter a formal legislative process.

**「Impact」** If adopted, the requirement would affect US companies running Chinese open-weight models in production, such as Airbnb&\#x27;s use of Qwen for customer service, by obliging them to publish that use on their websites. Because the proposal is still under discussion and lacks a confirmed legislative path, companies face uncertainty rather than an immediate compliance obligation.

**Tags**: `#AI policy`, `#China AI`, `#open-weight models`, `#AI regulation`, `#industry news`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Tencent Q3: AI spending surges, free cash flow turns negative](https://api3.cls.cn/share/article/2537922?os=android&amp;amp;sv=8.8.5&amp;amp;app=cailianpress&amp;amp;selected=) ⭐️ 7.0/10

Tencent reported 2026 third-quarter revenue of 207.3 billion yuan, up 8% year on year and below market expectations, while net profit rose 0.8% to 63.6 billion yuan. Capital expenditure reached 81.43 billion yuan, far above the 55.4 billion yuan market estimate, and quarterly free cash flow was negative 69.1 billion yuan.

telegram · zaihuapd · Nov 18, 09:20

**「Background」** WorkBuddy is Tencent&\#x27;s AI agent desktop workspace that plans and executes office tasks such as documents, spreadsheets and presentations from natural-language requests, according to Tencent&\#x27;s product documentation. Tencent said the negative free cash flow reflected net cash from operations of 2.6 billion yuan offset by 65.1 billion yuan of capital expenditure payments, among other items, per a Caixin-affiliated report cited by Tencent News.

**「Impact」** The capex overshoot and negative free cash flow signal that Tencent is directing substantially more cash into AI infrastructure than analysts had expected, a shift relevant to investors weighing the company&\#x27;s spending against near-flat profit growth.

<details><summary>References</summary>
<ul>
<li><a href="https://www.workbuddy.cn/docs/workbuddy/Overview">WorkBuddy 简介 | WorkBuddy - AI Agent 办公新范式</a></li>
<li><a href="https://news.qq.com/rain/a/20261118A0D07X00">腾讯控股：第三季度录得负自由现金流691亿元 资本开支付款651亿元_腾...</a></li>
<li><a href="https://finance.eastmoney.com/a/202611183934218485.html">腾讯三季度资本开支升至814亿元，大额算力预付款拖累自由现金流腾讯三...</a></li>

</ul>
</details>

**Tags**: `#Tencent`, `#earnings`, `#AI capex`, `#free cash flow`, `#China tech`

---

<a id="item-finance-news-2"></a>
### [China and South Korea announce substantive conclusion of FTA services and investment talks](https://x.com/Jaemyung_Lee/status/2122988472994791476) ⭐️ 7.0/10

On November 18, China and South Korea announced the substantive conclusion of follow-up negotiations under their free trade agreement on services and investment. China committed to most-favored-nation treatment for South Korean films and games and to wider opening in tourism, legal, construction, and finance, according to a Yonhap report relayed on social media; some technical items remain to be settled at the working level.

telegram · zaihuapd · Nov 18, 10:02

**「Background」** The China–South Korea free trade agreement took effect in 2015, and follow-up talks on services and investment began in March 2018; the two sides restarted the process in January 2025 after a four-year pause, according to Lianhe Zaobao.

<details><summary>References</summary>
<ul>
<li><a href="https://www.zaobao.com.sg/realtime/china/story20250116-5743403">时隔四 年 韩 中 重 启 自 贸 协 定 服 贸 投 资 后 续 谈 判 | 联合早报</a></li>
<li><a href="https://t.me/zaobao_news/162157">联合早报 即时报道 – Telegram</a></li>

</ul>
</details>

**Tags**: `#China-South Korea FTA`, `#trade policy`, `#services and investment`, `#media and entertainment`, `#market opening`

---