---
layout: default
title: "Horizon Summary: 2026-11-21 (EN)"
date: 2026-11-21
lang: en
---

> From 58 items, 17 important content pieces were selected

---

**Technology News**
1. [Levent Alpöge Claims Generalized Riemann Hypothesis Proof](#item-tech-news-1) ⭐️ 9.0/10
2. [GitHub Repo Claims Finite-Time Blow-Up for Unforced Navier–Stokes](#item-tech-news-2) ⭐️ 9.0/10
3. [Hackers Use AI Pentesting Tool Cairn to Find Zero-Day](#item-tech-news-3) ⭐️ 8.0/10
4. [KVM 漏洞允许虚拟机读取 AMD 主机内存](#item-tech-news-4) ⭐️ 8.0/10
5. [TSMC Pauses 16nm-and-Below Orders From Chinese Firms](#item-tech-news-5) ⭐️ 8.0/10
6. [Paper Claims Language Models Can Rewrite Their Own Weights Without Gradients](#item-tech-news-6) ⭐️ 7.0/10
7. [Inkling 2 Mini: Open-Weights Looped Transformer Model](#item-tech-news-7) ⭐️ 7.0/10
8. [Signal Moves to Limit AI Agents Capturing Mobile Data](#item-tech-news-8) ⭐️ 7.0/10
9. [Blog recounts vibecoding an inference chip with AI](#item-tech-news-9) ⭐️ 7.0/10
10. [Bell Canada Reports &\#x27;Agentic&\#x27; Hacker Stole Enterprise Data](#item-tech-news-10) ⭐️ 7.0/10
11. [F5 Issues Emergency Patches for Five Critical BIG-IP Flaws](#item-tech-news-11) ⭐️ 7.0/10
12. [US Tightens Chip Exports as India Expands AI Compute](#item-tech-news-12) ⭐️ 7.0/10
13. [Apple reportedly developing its own AI agent for late 2027](#item-tech-news-13) ⭐️ 7.0/10
14. [OpenAI adds background mode for long API requests](#item-tech-news-14) ⭐️ 7.0/10
15. [Cursor Weighs Phasing Out Chinese Open-Weight AI Models](#item-tech-news-15) ⭐️ 7.0/10
16. [OpenAI 称反蒸馏防御将推理链提取成功率降至 0.2%](#item-tech-news-16) ⭐️ 7.0/10

**Financial News**
1. [Trump Proposes &\#x27;Huge Tax&\#x27; on US Firms Building AI Data Centers Abroad](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Levent Alpöge Claims Generalized Riemann Hypothesis Proof](https://alpo.ge/remark.pdf) ⭐️ 9.0/10

Anthropic mathematician Levent Alpöge has posted a document on his website claiming a proof of the Generalized Riemann Hypothesis, reportedly developed with help from Claude and accompanied by a very large Lean formalization. The claim has not been independently verified, and Anthropic has not commented on or involved itself in the announcement, according to The Verge. A separate, fully human proof has also been circulated, and MIT&\#x27;s Andrew Sutherland is running verification checks that were still in progress as of 2026-11-20 22:05 UTC. The formalization is reported to be roughly 1.3 GB and about 15 million lines of Lean code.

hackernews · iamronaldo · Nov 20, 14:16 · [Discussion](https://news.ycombinator.com/item?id=50574968)

**「Background」** The Riemann hypothesis, posed in 1859, concerns the distribution of prime numbers and remains unproven; the Generalized Riemann Hypothesis extends the same conjecture to a broader class of zeta and L-functions. Alpöge&\#x27;s claim, posted on November 20, 2026, reportedly rests on a large Lean formalization distributed as 14 file parts, alongside a separate human proof attributed to Alessandro Masullo. Independent verification had not been completed at the time of the reports.

**「Verification status」** MIT mathematician Andrew Sutherland has published verification results for the Lean formalization, reporting that the published Lean source compiles without errors and that the five headline theorems check out, with remaining checks still in progress as of the page&\#x27;s last update. Sutherland characterized the result as &quot;a human triumph&quot; while noting that substantial work remains to understand the mathematical details, so the claim should be treated as machine-checked in part rather than fully digested or independently confirmed in the conventional mathematical sense.

**「Community Reaction」** Commenters noted the scale of the Lean artifact, with one describing a 1.3 GB, ~15-million-line proof split across 14 downloadable parts, and another pointing to a separate human proof posted on a math blog. One commenter cited Sutherland&\#x27;s ongoing verification page as reason to believe the proof is correct, while others debated the broader implications of AI-driven mathematics and recalled Terence Tao&\#x27;s earlier skepticism that current AI could make progress on the Riemann hypothesis.

<details><summary>References</summary>
<ul>
<li><a href="https://www.scientificamerican.com/article/anthropic-mathematician-claims-to-prove-riemann-hypothesis-most-famous-problem-in-all-of-math/">Anthropic mathematician claims to prove Riemann hypothesis , most...</a></li>
<li><a href="https://www.nacionale.com/en/articles/has-riemann-hypothesis-been-proved-levent-alpoge-claude-anthropic-claim-lean">Riemann hypothesis proof claimed with Claude , unverified</a></li>
<li><a href="https://kingy.ai/blog/levent-alpoge-claude-riemann-hypothesis-proof/">Levent Alpöge claims a Riemann hypothesis proof with Claude</a></li>
<li><a href="https://math.mit.edu/~drew/grh/">RH Lean proof: verification files - MIT Mathematics</a></li>
<li><a href="https://www.nacionale.com/en/articles/what-is-lean-proof-assistant-riemann-hypothesis-alpoge-claude-explained">Lean, the proof checker the Riemann claim rests on</a></li>
<li><a href="https://agihunt.info/en/p/1a1faf8de7f20b49cf336059c5b">MIT&#x27;s Sutherland Verifies Riemann Hypothesis… · AGI Hunt</a></li>

</ul>
</details>

**Tags**: `#mathematics`, `#formal-verification`, `#Lean`, `#AI-research`, `#research-claims`

---

<a id="item-tech-news-2"></a>
### [GitHub Repo Claims Finite-Time Blow-Up for Unforced Navier–Stokes](https://github.com/tristanbuckmaster/navier-stokes/) ⭐️ 9.0/10

A GitHub repository attributed to Tristan Buckmaster claims a finite-time blow-up result for the unforced Navier–Stokes equations. The supplied metadata contains no paper, proof, or verification details, so the claim remains unconfirmed; if valid, a blow-up for the unforced equations would bear directly on the Navier–Stokes existence and smoothness Millennium Prize problem. Hacker News commenters framed it as distinct from a prior forced-equation result, which they said relied on a carefully designed external force.

hackernews · trotro · Nov 20, 15:34 · [Discussion](https://news.ycombinator.com/item?id=50576232)

**「Background」** The Navier–Stokes existence and smoothness problem is one of the Clay Mathematics Institute&\#x27;s Millennium Prize problems, asking whether smooth initial data in three dimensions always yields smooth solutions for all time. The repository&\#x27;s claim concerns the unforced equations, meaning no external force is applied, which community commenters contrasted with an earlier OpenAI result that reportedly used a designed external force. External reporting describes the work as by Tristan Buckmaster and Levent Alpöge and says it rests on an approximate self-similar profile checked by interval arithmetic, but the supplied metadata provides no verification of the claim.

**「Impact」** Because the repository supplies no verifiable proof detail in the supplied material, the practical consequence is that researchers cannot yet treat the unforced blow-up claim as established or build on it. Commenters distinguish it from OpenAI&\#x27;s earlier result, which they say used a carefully designed external force, making this unforced version more physically relevant if it holds. Verification would matter for numerical simulation, since a genuine blow-up would indicate where smooth solutions break down rather than where a simulation merely becomes unstable.

**「Community Discussion」** Commenters debated the claim&\#x27;s significance relative to other same-day results, with one calling the combination of a generalized Riemann Hypothesis claim and unforced Navier–Stokes a record day for mathematics. Others discussed whether a numerical simulation could show the blow-up in real time to build intuition, and one commenter referenced unverified rumors about an Anthropic Millennium Prize result affecting credit for the work.

<details><summary>References</summary>
<ul>
<li><a href="https://officechai.com/ai/tristan-buckmaster-levent-alpoge-claim-proof-of-navier-stokes-millennium-prize-problem-without-forcing/">Tristan Buckmaster, Levent Alpöge Claim Proof Of Navier ...</a></li>
<li><a href="https://aixiv.online/abs/2611.02204">[2611.02204] Finite-time blow-up for the Navier–Stokes ...</a></li>
<li>Did OpenAI solve the wrong Navier-Stokes problem?</li>
<li>[PDF] Finite Time Blowup for Navier–Stokes - OpenAI</li>

</ul>
</details>

**Tags**: `#navier-stokes`, `#mathematics`, `#fluid-dynamics`, `#research`, `#millennium-prize`

---

<a id="item-tech-news-3"></a>
### [Hackers Use AI Pentesting Tool Cairn to Find Zero-Day](https://www.bleepingcomputer.com/news/security/hackers-use-autonomous-ai-tool-cairn-to-find-zero-day-take-over-server/) ⭐️ 8.0/10

Threat actors reportedly used Cairn, an open-source autonomous AI penetration-testing framework, to discover a previously unknown vulnerability in a medical imaging application and take over a server. The supplied report is a brief excerpt and does not specify the application, the vulnerability class, the affected versions, or how the compromise was carried out. The claim is attributed to the reporting rather than to an independently verified technical analysis, so the exploit details and the extent of Cairn&\#x27;s role remain unconfirmed.

rss · BleepingComputer · Nov 20, 17:30

**「What Cairn is」** Cairn is an open-source, multi-agent penetration-testing framework released under the AGPL-3.0 license that dispatches autonomous AI &quot;workers&quot; against a defined target to map infrastructure and probe for weaknesses. The reported incident is notable because the same tooling designed for authorized security testing was allegedly turned against a medical imaging application to find a previously unknown flaw.

**「Impact」** The reported use of Cairn to find and exploit a zero-day in a medical imaging application suggests defenders of internet-facing healthcare software should treat autonomous AI pentesting tools as a realistic attack path, not just a research curiosity. Because Cairn is open source, the same framework is available to both authorized testers and attackers, so organizations running such applications may need to prioritize patching and exposure review. The supplied source does not identify the affected product, version, or patch status, so no specific remediation can be confirmed from this report alone.

<details><summary>References</summary>
<ul>
<li><a href="https://futuretweets.com/cairn-ai-pentesting-panels-hijacked-2026/">Cairn AI Pentesting Panels Hijacked: 17 Hit [2026]</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-use-autonomous-ai-tool-cairn-to-find-zero-day-take-over-server/">Hackers use autonomous AI tool Cairn to find zero-day, take ...</a></li>
<li><a href="https://aviatrix.ai/threat-research-center/chinese-nexus-cairn-ai-agents-zero-day-2026/">Chinese-Nexus Cairn AI Agents Discover Zero-Day in 2026 ...</a></li>

</ul>
</details>

**Tags**: `#AI security`, `#zero-day`, `#penetration testing`, `#open source`, `#vulnerability research`

---

<a id="item-tech-news-4"></a>
### [KVM 漏洞允许虚拟机读取 AMD 主机内存](https://thehackernews.com/2026/11/new-linux-kvm-flaw-cve-2026-99312-lets.html) ⭐️ 8.0/10

Linux 内核 KVM 中的 CVE-2026-99312 允许虚拟机在启用嵌套虚拟化时读取 AMD 主机内存。研究人员在 DigitalOcean 上从虚拟机内读取到约 127 GB 主机内存。上游修复已于 11 月 18 日随稳定内核 7.3.5 等发布，但 Debian、Ubuntu 等发行版内核尚未修复。在补丁到位前，可关闭嵌套虚拟化作为缓解措施。

telegram · zaihuapd · Nov 20, 14:23

**「Background」** KVM is the Linux kernel&\#x27;s hypervisor module, and nested virtualization lets a guest VM itself run hypervisors, which expands the code paths that must correctly isolate guest state from the host. According to a Red Hat advisory, CVE-2026-99312 stems from KVM failing to reset the Memory Management Unit context when emulating an INIT processor reset while nested virtualization is active, allowing memory corruption or denial of service. The reported DigitalOcean result of reading roughly 127 GB of host RAM is a researcher demonstration, not an independently reproduced measurement.

**「影响」** 在 AMD 主机上运行嵌套虚拟化的基础设施运营方应检查其内核版本，并在发行版补丁可用前考虑禁用嵌套虚拟化，因为未修复的客户机可能读取主机内存。

<details><summary>References</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99312">CVE-2026-99312 - Red Hat Customer Portal</a></li>
<li><a href="https://dev.to/etairos/cve-2026-99312-linux-kvm-flaw-let-a-guest-vm-read-127-gb-of-host-memory-on-amd-hosts-4460">CVE-2026-99312: Linux KVM Flaw Let a Guest VM Read 127 GB of ...</a></li>

</ul>
</details>

**Tags**: `#linux-kernel`, `#kvm`, `#vulnerability`, `#virtualization`, `#security`

---

<a id="item-tech-news-5"></a>
### [TSMC Pauses 16nm-and-Below Orders From Chinese Firms](https://appleinsider.com/articles/26/11/20/apple-supplier-tsmc-cuts-off-china-chip-orders-amid-tighter-export-controls) ⭐️ 8.0/10

TSMC has notified customers that it is pausing orders for 16nm-and-below advanced process nodes from Chinese companies. Under tightened U.S. semiconductor export rules, TSMC may not supply these nodes without a prior U.S. export license or exemption, leaving Chinese firms limited to older processes such as 28nm and 40nm and unable to use the high-bandwidth memory needed for AI data centers. Previously TSMC could itself assess whether a customer&\#x27;s design qualified for an exemption; now customers must apply in advance. The U.S. approved list includes Apple, AMD, and Nvidia, with no Chinese companies listed, and TSMC said it will comply with the new rules.

telegram · zaihuapd · Nov 21, 02:01

**「Background」** The pause follows a U.S. Commerce Department rule that took effect on November 19, 2026, which removed routes for chip designers in certain country groups to use advanced foundry processes without U.S. authorization, according to Reuters reporting cited by Effectstory. Under the prior arrangement, TSMC could itself assess whether a customer&\#x27;s design qualified for an exemption; the new rule requires customers to obtain U.S. export licenses in advance.

**「Impact」** Chinese chip designers that relied on TSMC&\#x27;s 16nm-and-below nodes must now obtain a U.S. license or exemption before ordering, or shift designs to 28nm and 40nm processes, which the report says cannot support the high-bandwidth memory used in AI data centers.

<details><summary>References</summary>
<ul>
<li><a href="https://effectstory.com/en/articles/tsmc-halts-china-16nm-orders-new-us-chip-rule">TSMC reportedly halts China chip orders at 16nm and below</a></li>
<li><a href="https://aistockwire.com/blog/tsmc-tsm-halts-china-chip-orders-16nm-us-foundry-rule-november-2026">TSMC (TSM) halts some Chinese chip orders under new US rule</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#export-controls`, `#TSMC`, `#AI-hardware`, `#supply-chain`

---

<a id="item-tech-news-6"></a>
### [Paper Claims Language Models Can Rewrite Their Own Weights Without Gradients](https://arxiv.org/abs/2611.21885) ⭐️ 7.0/10

A research paper posted to arXiv claims that, for the first time, a language model rewrites its own weights through its own reasoning and improves, with no gradients and no training. According to the abstract-style description, the model tests its edits on practice problems and submits only what works, with accuracy rising across eight consecutive sessions. The supplied material contains no methodology, benchmarks, or independent verification, so the result should be treated as a vendor-style claim rather than a confirmed capability.

hackernews · lwhsiao · Nov 20, 16:29 · [Discussion](https://news.ycombinator.com/item?id=50577265)

**「Prior work on weight editing」** The paper&\#x27;s claim sits alongside earlier work on editing model weights without gradient descent. Weight-space programming describes a general-purpose LLM reading and directly writing another neural network&\#x27;s weights without a training loop, and a November 2026 MIT paper reported using GPT-6 Astra to change only 0.016% of a Qwen3.5-0.8B model&\#x27;s weights to improve math performance. Google Research&\#x27;s Sleep framework separately updates numerical weights during an offline phase using self-generated practice examples. Commenters cite both lines of work when questioning how much of the new result is novel.

**「Why it matters」** If the claim holds, it would let a deployed model modify itself without a training pipeline, which raises direct questions about how such edits are audited or rolled back. Commenters also flag a safety concern: an autonomous model could in principle use weight edits to suppress activations associated with safety and alignment, so any practical use would need controls on what edits are permitted and logged.

**「Community pushback」** Commenters questioned the novelty and the framing of &quot;no training&quot;: Toutouxc argued the described loop of testing edits and keeping only what works sounds a lot like training, while aesthesia noted the only observed self-improvement was shortening reasoning traces to avoid token limits, similar to a prior weight-space programming result. gavinray pointed to Google&\#x27;s SLEEP framework, which updates weights offline using self-generated practice examples, as earlier work covering similar ground.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/">The sleep framework : A new way for LLMs to retain knowledge in...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Weight-space_programming">Weight-space programming - Wikipedia</a></li>
<li><a href="https://x.com/i/trending/2117328869283840499">MIT Shows GPT-6 Astra Edits Neural Network Weights Directly</a></li>
<li><a href="https://www.mindstudio.ai/blog/gpt-5-astra-weight-space-programming">Can AI Edit Another Model&#x27;s Weights? Inside the MIT ...</a></li>

</ul>
</details>

**Tags**: `#language-models`, `#self-modification`, `#ai-safety`, `#research`, `#weight-editing`

---

<a id="item-tech-news-7"></a>
### [Inkling 2 Mini: Open-Weights Looped Transformer Model](https://thinkingmachines.ai/news/inkling-2-mini/) ⭐️ 7.0/10

Thinking Machines released Inkling 2 Mini, an open-weights model built on a looped transformer architecture and trained end-to-end in nvfp4. The release targets local use, and commenters report running it through llama.cpp: one measured about 27 tokens/s decode on a Ryzen 395 with Vulkan, another about 10 tokens/s on a 32GB M1 Pro MacBook at q4. These are early community anecdotes and vendor benchmark claims, not independently verified results; the team said it had not exhaustively tested some aspects of the nvfp4 training.

hackernews · jasondavies · Nov 20, 20:12 · [Discussion](https://news.ycombinator.com/item?id=50581260)

**「Background」** Inkling 2 Mini is Thinking Machines Lab&\#x27;s open-weights model, and its architecture is a modified looped transformer in which layers 6–17 are looped three times, according to Unsloth&\#x27;s local-run guide. Thinking Machines also reports that most of the model&\#x27;s weights were trained and are deployed natively in NVFP4, with the last four layers in MXFP8, and that a DSpark drafter is included. These details explain why the release drew attention from local-inference users: the looped design and low-precision training are the features commenters cite when comparing it with larger models.

**「Impact」** Local users running the model in llama.cpp need several unmerged PRs \(32694, 32657, 32429, 32704\), and one commenter reported a small patch to src/llama-graph.cpp yielding roughly a 30% speed boost, so expect to apply fixes before judging throughput.

**「Community Discussion」** Commenters called the reported parity with a Qwen3.8-27B-class model notable for a looped architecture and predicted more open models will adopt looping, while one raised open questions about safety and interpretability at this level of availability. Another framed the efficiency focus as a product of resource constraints rather than a deliberate design trend.

<details><summary>References</summary>
<ul>
<li>Introducing Inkling 2 Mini - Thinking Machines Lab</li>
<li>Welcome Inkling 2 Mini, Cutting-edge Performance for your Local Setup</li>
<li>Inkling 2 Mini - Run Locally Guide | Unsloth Documentation</li>

</ul>
</details>

**Tags**: `#machine learning`, `#open weights`, `#local inference`, `#transformer architecture`, `#llama.cpp`

---

<a id="item-tech-news-8"></a>
### [Signal Moves to Limit AI Agents Capturing Mobile Data](https://signal.org/blog/protecting-your-privacy/) ⭐️ 7.0/10

Signal published a blog post describing efforts to restrict AI agents on mobile operating systems from capturing user data, including Signal chats. The post says Signal is &quot;cautiously optimistic&quot; about progress, according to a commenter who summarized it, but the supplied material does not include the technical mechanism, affected platforms, or a release timeline. The item therefore reflects an announced direction rather than a demonstrated, shipped capability.

hackernews · dotcoma · Nov 20, 09:42 · [Discussion](https://news.ycombinator.com/item?id=50572348)

**「Background」** Signal&\#x27;s post frames OS-integrated AI agents as a threat at the application layer, arguing that without &quot;common-sense remedies&quot; independent developers cannot protect sensitive data. Coverage of the post describes Signal as warning about AI agents built into computer and smartphone operating systems and rolling out screenshot blocks in response.

**「Why it matters」** The concern raised in discussion is that even users without an AI app installed can leak chats if a contact runs one, so protection depends on OS-level controls rather than Signal alone. Commenters also asked Signal to publish its forensics findings so smaller app developers could reuse them, and one noted that screenshot blocking already affects Windows users who want to capture chats.

**「Community reaction」** Commenters broadly welcomed the direction but pressed for more: one cited a Meredith Whittaker interview describing Signal&\#x27;s struggle to keep AI apps out of chats, another asked for a public, collaborative write-up of the forensics investigation, and a third argued users should be warned about spyware and pointed to GrapheneOS or Linux. A separate thread criticized Signal&\#x27;s captcha-heavy spam protection as breaking new-contact setup over VPNs, which one commenter said pushes journalists and sources to other apps.

<details><summary>References</summary>
<ul>
<li><a href="https://signal.org/blog/protecting-your-privacy/">Signal is Serious About Protecting Your Privacy</a></li>
<li><a href="https://gizmodo.com/signal-is-fighting-to-keep-ai-agents-out-of-your-private-messages-2000843160">Signal Is Fighting to Keep AI Agents Out of Your ... - Gizmodo</a></li>
<li><a href="https://www.inc.com/aaron-mok/signal-blocks-screenshots-ai-agents-privacy/91440348">Signal Blocks Screenshots Over AI Agent Risks - Inc.com</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#security`, `#mobile-os`, `#ai-agents`, `#signal`

---

<a id="item-tech-news-9"></a>
### [Blog recounts vibecoding an inference chip with AI](https://ankitg.me/blog/vibecoding-inference-chip/) ⭐️ 7.0/10

A blog post by Ankit Gupta describes an attempt to &quot;vibecode&quot; an inference chip with AI assistance, according to the Hacker News submission. The post is a first-person account of using LLM tooling for hardware design rather than a shipped chip or independently measured result. Commenters focused on FPGA feasibility and economics, the reported $10k+ token cost, and the need for automated verification when delegating large tasks to models.

hackernews · ankitvgupta · Nov 20, 18:15 · [Discussion](https://news.ycombinator.com/item?id=50579297)

**「Context」** The post is a first-person account of using AI coding assistants to design an inference chip, a task that normally requires specialized hardware-design expertise. The community discussion frames the attempt against existing constraints: FPGAs are cited as a route to bespoke fast chips but face fab-capacity and economic limits at scale, and one commenter notes that each chip needs its own tailored software and inference stack, which is expensive and difficult to build.

**「Practical Impact」** The project&\#x27;s reported $10k+ token spend, noted in the discussion, makes this approach impractical as a routine design method for most individuals, though it may be viable for organizations already paying for large-scale model usage. Commenters also stressed that automated verification indicators matter when delegating large hardware-design tasks to models, suggesting that checking AI-generated RTL or chip logic is the binding constraint rather than generation itself.

**「Community discussion」** One commenter recalled being told that FPGAs face fab-capacity constraints that make scaling bespoke inference hardware economically difficult, though they could not recall whether the cause was technical or capacity-related. Another called the project fun but said spending $10k+ in tokens on a curiosity is excessive, while a third argued that automated indicators matter more than model intelligence when giving AI large tasks.

<details><summary>References</summary>
<ul>
<li>Simon Willison&#x27;s Weblog</li>

</ul>
</details>

**Tags**: `#ai-assisted-coding`, `#hardware-design`, `#inference-chips`, `#fpga`, `#llm-tooling`

---

<a id="item-tech-news-10"></a>
### [Bell Canada Reports &\#x27;Agentic&\#x27; Hacker Stole Enterprise Data](https://www.bleepingcomputer.com/news/security/bell-canada-says-agentic-hacker-stole-enterprise-customer-data/) ⭐️ 7.0/10

Bell Canada confirmed that an &quot;agentic&quot; threat actor breached its systems on November 17, 2026, and stole enterprise customer data. The stolen information includes data from a system used to order and provision telecommunications circuits. The supplied excerpt provides no further technical detail on the attack mechanics, the scope of affected customers, or how the actor was identified as agentic.

rss · BleepingComputer · Nov 20, 18:51

**「Background」** Bell Canada&\#x27;s disclosure describes the intruder as an &quot;agentic&quot; threat actor, a term used for attackers that direct AI agents to carry out intrusion steps rather than relying solely on manual operations. The breach affected a system used to order and provision telecommunications circuits, according to the company&\#x27;s confirmation. The supplied reports do not detail how the agents were used, what data was taken, or how many customers were affected.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/bell-canada-says-agentic-hacker-stole-enterprise-customer-data/">Bell Canada says &#x27;agentic&#x27; hacker stole enterprise customer data</a></li>
<li><a href="https://www.scworld.com/brief/bell-canada-confirms-data-breach-involving-agentic-threat-actor">Bell Canada confirms data breach involving agentic threat actor</a></li>
<li><a href="https://www.theglobeandmail.com/business/article-bell-cybersecurity-incident-customer-data/">Bell says enterprise customer data was stolen in ‘agentic ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#AI agents`, `#data breach`, `#telecom`

---

<a id="item-tech-news-11"></a>
### [F5 Issues Emergency Patches for Five Critical BIG-IP Flaws](https://www.bleepingcomputer.com/news/security/f5-releases-emergency-patches-for-critical-big-ip-rce-flaws/) ⭐️ 7.0/10

F5 has released emergency patches for five critical vulnerabilities in its BIG-IP product line, warning that attackers could exploit them to achieve remote code execution or cause denial-of-service conditions. The company urged customers to apply the fixes, though the available excerpt does not specify affected versions, CVE identifiers, or exploitation status. The flaws are described as critical, but no independently measured severity scores or proof-of-exploitation details were provided in the source.

rss · BleepingComputer · Nov 20, 10:57

**「Background」** F5&\#x27;s November 2026 security update covers 12 BIG-IP and BIG-IQ flaws, including unauthenticated Traffic Management Microkernel \(TMM\) crashes that may allow remote code execution, according to a third-party alert summary. The emergency patches reported here are out-of-band fixes for BIG-IP Access Policy Manager \(APM\) and BIG-IP iRule, five of which carry a 9.8 Critical severity rating.

**「Impact」** Organizations running BIG-IP appliances should treat the patches as urgent and verify which of their deployed versions are affected before applying updates, since the flaws allow both remote code execution and DoS. The source does not state whether the vulnerabilities are being actively exploited, so administrators should consult F5&\#x27;s advisory for version-specific guidance.

<details><summary>References</summary>
<ul>
<li><a href="https://threatlistpro.com/alerts/f5-big-ip-november-2026-security-update">F5 BIG-IP Vulnerabilities November 2026: 12 CVEs and Fixes</a></li>
<li><a href="https://www.networkworld.com/article/4251676/f5-scrambles-to-fix-more-critical-big-ip-security-flaws.html">F5 scrambles to fix more critical BIG-IP security flaws</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerabilities`, `#patching`, `#networking`, `#F5 BIG-IP`

---

<a id="item-tech-news-12"></a>
### [US Tightens Chip Exports as India Expands AI Compute](https://www.bloomberg.com/news/articles/2026-11-20/nvidia-scandal-fallout-india-ai-yotta-ambani-adani-am-intelligence-e2e-networks) ⭐️ 7.0/10

The US has tightened export controls on advanced chips to Malaysia, Thailand, and Singapore, and India&\#x27;s AI sector sees an opening to absorb the displaced demand. Yotta says it will add roughly 100,000 GPUs over the next year, an increase of about 10% over India&\#x27;s current compute capacity. India currently hosts 153 data centers, ranking 14th globally, while Reliance has committed up to $110 billion and Adani $100 billion to AI infrastructure, though the sector has long been held back by compute shortages and limited capital. The figures come from a brief digest of a Bloomberg report and are stated plans rather than independently verified deployments.

telegram · zaihuapd · Nov 20, 07:31

**「Background」** The US has been tightening controls on advanced AI chip exports, with Southeast Asian transshipment hubs such as Malaysia and Singapore becoming a focus because Nvidia hardware has been routed through them to reach restricted buyers. Reporting cited in search results describes ByteDance deploying 36,000 Nvidia B200 chips in Malaysia through Southeast Asian cloud providers, and Nvidia chips being placed in Malaysian data centers via a Singapore-based intermediary. India&\#x27;s AI buildout, by contrast, has been constrained by limited domestic compute infrastructure and capital, which is the gap the new GPU and data-center commitments are meant to address.

**「Impact」** For Indian AI operators, the announced capacity depends on GPU supply that US export rules could constrain, since the same tightening that redirects demand toward India also limits access to advanced chips. Yotta&\#x27;s planned ~100,000 GPUs would add roughly 10% to India&\#x27;s existing compute, a modest increment relative to the $210 billion in combined Reliance and Adani commitments, which target multi-gigawatt data centers over multi-year horizons rather than near-term availability.

<details><summary>References</summary>
<ul>
<li><a href="https://abhs.in/blog/bytedance-36000-nvidia-b200-chips-malaysia-us-export-controls-2026">ByteDance Routes 36,000 Nvidia B200 Chips Through Malaysia to...</a></li>
<li><a href="https://www.moonofalabama.org/2026/11/nvidia-knifes-are-out-for-jensen-huang-spy-allegations-fanciful.html/comment-page-2">Nvidia – Knives Are Out For Jensen Huang – Spy Allegations Fanciful...</a></li>
<li><a href="https://www.adani.com/newsroom/media-releases/adani-commits-usd-100-bn-to-sovereign-ai-infrastructure">Adani Commits USD 100 Bn to Sovereign AI Infrastructure</a></li>
<li><a href="https://economictimes.indiatimes.com/tech/artificial-intelligence/reliance-puts-110-billion-on-table-joins-adani-tata-in-big-ticket-ai-buildout/articleshow/128589413.cms">Reliance puts $110 billion on table, joins Adani &amp; Tata in ...</a></li>
<li><a href="https://bharatbusinessindex.com/blog/indias-210-billion-ai-data-centre-boom-2026-reliance-110b-adani-100b-the-race-to-become-the-worlds-ai-infrastructure-hub">India&#x27;s $210 Billion AI Data Centre Boom 2026: Reliance $110B ...</a></li>

</ul>
</details>

**Tags**: `#chip-export-controls`, `#ai-infrastructure`, `#india`, `#gpu-compute`, `#semiconductors`

---

<a id="item-tech-news-13"></a>
### [Apple reportedly developing its own AI agent for late 2027](https://www.bloomberg.com/news/articles/2026-11-19/apple-is-working-on-ai-agent-for-device-control-apps-browsing-and-coding) ⭐️ 7.0/10

Bloomberg, citing job postings Apple added this week, reports that Apple is recruiting a senior engineering manager to lead development of a &quot;proactive AI agent&quot; that could write code, browse the web, and operate apps on the user&\#x27;s behalf. The project is described as early-stage, with a launch targeted as early as late 2027. The same report says macOS 27.3 adds a warning screen that raises the number of steps a third-party agent needs to obtain Mac control permissions from 4 to 14. These are reported plans and job-posting evidence, not a shipped product or independently verified capability.

telegram · zaihuapd · Nov 20, 08:59

**「背景」** 彭博的报道依据是苹果本周新增的招聘信息，其中高级工程经理一职被描述为负责开发能像人一样使用电脑、浏览网页并跨应用工作的 AI 智能体。报道同时提到，Meta Muse、OpenAI 等公司已推出同类智能体，而苹果在 macOS 27.3 中新增警告页，使第三方智能体获取 Mac 控制权限的步骤从 4 步增至 14 步。

**「Impact」** If the macOS 27.3 change ships as described, developers building third-party agents for the Mac would face a longer, warning-gated permission flow, while Apple&\#x27;s own agent would be positioned as a first-party alternative. The late-2027 target means no near-term compatibility or migration action is warranted yet.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bloomberg.com/opinion/articles/2026-11-20/an-apple-agent-is-something-to-fear-for-ai-rivals">An Apple Agent Is Something to Fear for AI Rivals - Bloomberg</a></li>
<li><a href="https://thenextweb.com/news/apple-ai-agent-job-listing-computer-use-bloomberg">Apple is building an AI agent that codes and controls apps ...</a></li>

</ul>
</details>

**Tags**: `#apple`, `#ai-agents`, `#macos`, `#platform-policy`, `#industry-news`

---

<a id="item-tech-news-14"></a>
### [OpenAI adds background mode for long API requests](https://developers.openai.com/api/docs/guides/background) ⭐️ 7.0/10

OpenAI has reportedly introduced a background mode that runs long-running API requests asynchronously: setting \`background: true\` and choosing a 2h or 8h window via \`background\_options.completion\_window\` yields token rates 30% and 40% below standard pricing, respectively, while the default \`soonest\` setting carries no discount. The discounted mode is said to be in public beta on GPT-6.2 Astra, GPT-6.2 Sol, GPT-6.1 Terra and GPT-6 Luna. The report also states that background mode temporarily stores response data even when \`store\` is false or zero data retention is enabled. This comes from a single Telegram summary without independent verification, and the model names could not be confirmed from the supplied material.

telegram · zaihuapd · Nov 20, 11:15

**「Background context」** OpenAI&\#x27;s Responses API already supported background mode for asynchronous requests, but its completion window defaulted to \`soonest\`, which carried no token discount. The new option lets developers explicitly select a 2h or 8h target window in exchange for lower per-token rates, with the discounted windows now in public beta.

**「Impact」** Developers building long-running workloads would need to weigh the 30–40% token discount against the temporary storage of response data, which the report says applies regardless of the \`store\` setting or zero data retention. Teams with strict data-handling requirements should confirm that behavior before routing sensitive requests through background mode.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.openai.com/api/docs/guides/background">Background mode | OpenAI API</a></li>
<li><a href="https://community.openai.com/t/reduce-costs-using-background-mode-with-completion-windows/1418130">Reduce costs using Background Mode with completion windows</a></li>

</ul>
</details>

**Tags**: `#openai`, `#api`, `#async-processing`, `#pricing`, `#llm-infrastructure`

---

<a id="item-tech-news-15"></a>
### [Cursor Weighs Phasing Out Chinese Open-Weight AI Models](https://www.cnbc.com/2026/11/20/cursor-chinese-ai-models-geopolitical-risk.html) ⭐️ 7.0/10

Cursor, the AI coding platform described in the report as SpaceX-owned, said it is considering phasing out Chinese-developed open-weight models, citing &quot;geopolitical risk.&quot; Its Composer 2 coding model is reportedly built on Moonshot AI&\#x27;s Kimi K2.5. The position follows a report from the US House Homeland Security Committee and the Select Committee on China, which recommends a &quot;US national open-weight plan&quot; and, building on an executive order barring DeepSeek from federal systems, calls for banning Chinese-developed AI models from federal systems. The source is a brief secondary summary, so the timing, scope, and finality of any Cursor change remain unconfirmed.

telegram · zaihuapd · Nov 20, 16:13

**「Background」** Cursor&\#x27;s Composer 2 coding model was built by continued pretraining on Kimi K2.5, the open-weight checkpoint from Beijing-based Moonshot AI, a detail developers discovered in the code rather than from Cursor&\#x27;s launch materials. SpaceX acquired Cursor&\#x27;s maker, Anysphere, in an all-stock deal that closed in August 2026 after being announced in June, placing the coding platform inside SpaceX&\#x27;s AI unit.

**「Impact」** If Cursor proceeds, developers using its Composer 2 coding model would lose a model built on Moonshot&\#x27;s Kimi K2.5 and would need to migrate to alternative models. The cited congressional report&\#x27;s recommendation to bar Chinese-developed AI models from federal systems signals that similar scrutiny could extend to other US organizations deploying Chinese open-weight models, so teams should track which upstream models their tools depend on.

<details><summary>References</summary>
<ul>
<li><a href="https://techjournal.org/spacex-acquires-cursor-60-billion">SpaceX Buys Cursor for $60B: Deal Closed (2026 Update)</a></li>
<li><a href="https://aimagazine.com/news/cursor-the-ai-coding-agent-spacex-bought-in-a-us-60bn-deal">Cursor: The AI Coding Agent SpaceX Bought in a US$60bn Deal</a></li>
<li><a href="https://www.linkedin.com/pulse/openais-cursor-cutoff-touches-five-percent-traffic-henning-steier-y9a2e">OpenAI&#x27;s Cursor cutoff touches five percent of traffic</a></li>
<li><a href="https://medium.com/synthetic-futures/20-month-cursor-is-running-a-free-chinese-model-i-tested-it-directly-and-saved-340-d2cc746e2d40">$20/Month Cursor Is Running a Free Chinese Model ... | Medium</a></li>
<li><a href="https://www.cryptopolitan.com/doordash-use-of-chinese-ai-model-draws-house-security-probe/">DoorDash use of Chinese AI model draws House security probe</a></li>
<li><a href="https://aiinasia.com/asean/us-house-open-weight-model-audit-southeast-asia-buyers-asean-deep-dive-2026-08-03">Washington Is Auditing Who Runs Chinese Models , and… | AI in Asia</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#open-weight models`, `#AI coding tools`, `#geopolitics`, `#open source`

---

<a id="item-tech-news-16"></a>
### [OpenAI 称反蒸馏防御将推理链提取成功率降至 0.2%](https://openai.com/index/combatting-adversarial-distillation/) ⭐️ 7.0/10

OpenAI 于 11 月 20 日发布文章，介绍针对“对抗性蒸馏”的防御措施，称 GPT-6.2 Astra 与 Sol 已加强对推理链的保护。OpenAI 表示，在红队测试中，提取历史请求推理的成功率从 54.0% 降至 0.2%。这些数字是 OpenAI 自述的红队测试结果，并非独立验证的测量值；来源摘要未说明测试方法或模型访问条件。OpenAI 还称，今年每周对数千至数万个蒸馏账号采取执法，并曾就 DeepSeek 疑似蒸馏行为向国会汇报。

telegram · zaihuapd · Nov 21, 01:30

**「Background」** OpenAI&\#x27;s post frames the change as a defense against adversarial distillation, in which an attacker tries to recover a model&\#x27;s protected reasoning from an earlier request rather than training on ordinary outputs. The 54.0% baseline comes from an internal adaptive red-team evaluation against GPT-6 Astra with its original protections, so the drop to 0.2% is a vendor-reported comparison between model generations, not an independent measurement.

**「影响」** 对于依赖模型输出构建蒸馏数据集或评估推理行为的开发者而言，OpenAI 的声明意味着针对 GPT-6.2 Astra 与 Sol 的提取尝试可能面临显著更低的成功率，且相关账号可能被执法。由于来源未说明防御的具体机制或适用范围，开发者不应假定这些保护同样适用于其他模型或访问方式。

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/combatting-adversarial-distillation/">Combatting adversarial distillation - OpenAI</a></li>
<li><a href="https://www.unite.ai/openai-strengthens-gpt-6-2-astra-against-reasoning-extraction/">OpenAI Strengthens GPT-6.2 Astra Against Reasoning Extraction</a></li>

</ul>
</details>

**Tags**: `#AI security`, `#model distillation`, `#OpenAI`, `#red teaming`, `#LLM`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Trump Proposes &\#x27;Huge Tax&\#x27; on US Firms Building AI Data Centers Abroad](https://apnews.com/article/trump-artificial-intelligence-data-centers-f1ac03b73d13445400eeed8631d9d879) ⭐️ 7.0/10

At a White House press conference on November 20, President Trump said he plans to impose a &quot;huge tax&quot; on US tech companies that build AI data centers overseas, aiming to keep those facilities in the US and preserve AI competitiveness with China. He said the plan had not yet been shared with officials inside his administration, and no rate, scope, or legislative path was given.

telegram · zaihuapd · Nov 21, 03:26

**「Background」** Trump&\#x27;s remarks follow data centers becoming a central issue in the midterm elections earlier in November, when many Democratic candidates promised tougher regulation on their construction, and come as tech giants including Meta and Google have entered agreements to build data centers overseas.

**「Potential impact」** If enacted, the tax would directly affect major US tech companies that build AI data centers abroad, such as Meta and Google, which have already signed agreements to build data centers overseas \(tool-2-1\). The proposal remains an announced intention with no rate, scope, or legislative path specified.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.co.uk/news/articles/cmde1lw9y54ko">Trump threatens ban on US firms building AI data centres overseas</a></li>
<li><a href="https://www.bbc.com/news/articles/cmde1lw9y54ko">Trump threatens ban on US firms building AI data centres overseas</a></li>
<li><a href="https://www.bbc.com/news/articles/cmde1lw9y54ko">Trump threatens ban on US firms building AI data centres overseas</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#US policy`, `#taxation`, `#data centers`, `#US-China tech competition`

---