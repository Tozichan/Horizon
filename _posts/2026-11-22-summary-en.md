---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 42 items, 10 important content pieces were selected

---

**Technology News**
1. [Claimed Lean formalization of Riemann Hypothesis reported certified](#item-tech-news-1) ⭐️ 10.0/10
2. [Microsoft previews RDMA over USB4 for multi-PC local AI inference on Windows](#item-tech-news-2) ⭐️ 8.0/10
3. [OpenRouter 警告 MiniMax 模型提示词疑遭第三方读取](#item-tech-news-3) ⭐️ 8.0/10
4. [Zhejiang University reports first on-hardware QRAM demonstration](#item-tech-news-4) ⭐️ 8.0/10
5. [Daraxonrasib First-Line Data: 8.2% Complete Responses in 61 Patients](#item-tech-news-5) ⭐️ 8.0/10
6. [Blogger Traces Monitor USB Hub to 75% Download Speed Loss](#item-tech-news-6) ⭐️ 7.0/10
7. [FBI and USDA reportedly breached in separate cyberattacks](#item-tech-news-7) ⭐️ 7.0/10
8. [Microsoft Warns Entra Connect Health Flaw Exploited for Tenant Data](#item-tech-news-8) ⭐️ 7.0/10
9. [Tesla begins overseas rollout of FSD v15](#item-tech-news-9) ⭐️ 7.0/10

**Financial News**
1. [Trump Proposes &\#x27;Huge Tax&\#x27; on U.S. Firms Building AI Data Centers Abroad](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Claimed Lean formalization of Riemann Hypothesis reported certified](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 10.0/10

A Telegram post reports that Levent Alpöge released a Lean formalization of the Riemann Hypothesis on 2026-11-20, comprising roughly 17 million lines of code. The post says Lean FRO and the Mathlib Initiative jointly certified on 2026-11-21 that the statement and proof are correct, that the statement matches Mathlib&\#x27;s RiemannHypothesis, that the codebase compiles without errors, and that multiple independent proof checkers validated the proof. The evidence supplied is a single forwarded post citing a Lean community blog URL, with no independent corroboration, so the claim should be treated with caution despite its potential significance.

telegram · zaihuapd · Nov 21, 16:48

**「Background」** The Riemann Hypothesis, unproven since Riemann posed it in 1859, concerns the non-trivial zeros of the Riemann zeta function and is one of mathematics&\#x27; best-known open problems. Lean is an interactive theorem prover in which proofs are checked mechanically by a small kernel, and Mathlib is its large community-maintained library of formalized mathematics; a formalization is therefore only meaningful if its statement matches the intended theorem and the code compiles without errors. External coverage reports that Levent Alpöge, an Anthropic mathematician, announced on November 20, 2026 a claimed proof of the Riemann Hypothesis and the Generalized Riemann Hypothesis for Dirichlet L-functions, formalized in Lean without assumptions, pending peer verification.

**「Verification caveat」** Because the certification rests on a forwarded post rather than an independently reviewed announcement, readers should check the linked Lean community blog and the Lean FRO and Mathlib Initiative statements directly before relying on the result. If confirmed, the proof&\#x27;s validity would depend on the correctness of the multiple independent checkers cited, not on any single kernel.

**「Community reaction」** Commenters debated how much assurance the independent checkers provide: one argued that a bug would now have to affect every kernel, including those with self-consistency proofs, while another noted that a fake Collatz refutation previously passed one such checker and questioned how independent they really are. Others credited Alpöge for eliciting the result from Claude and discussed whether the formalization covers a large portion of modern mathematics.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unite.ai/levent-alpoges-unverified-riemann-claim-puts-claudes-lean-code-in-focus/">Levent Alpöge’s Unverified Riemann Claim Puts Claude’s Lean ...</a></li>
<li><a href="https://stateofproof.org/paper-watch/paper-2026-11-20-a-claimed-proof-of-the-riemann-hypothesis">A Claimed Proof of the Riemann Hypothesis — Paper Watch ...</a></li>
<li><a href="https://english.mathrubhumi.com/technology/levent-alpoge-riemann-hypothesis-proof-claude-lean-code-2026-iyc9lobg">Levent Alpöge Claims Riemann Hypothesis Proof With Claude ...</a></li>

</ul>
</details>

**Tags**: `#formal-verification`, `#lean`, `#mathematics`, `#riemann-hypothesis`, `#mathlib`

---

<a id="item-tech-news-2"></a>
### [Microsoft previews RDMA over USB4 for multi-PC local AI inference on Windows](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

Microsoft released a Windows developer preview of RDMA over USB4 that lets multiple PCs share memory and GPU compute over ordinary USB4 links to run a single local AI model, without dedicated network cards or switches. In a demonstration, three AMD Ryzen AI Max+ 395 systems ran a 4-bit quantized Qwen3-235B-A22B model at roughly 18.5 tokens per second. The preview is being distributed through Windows Insider, so it is an announced developer capability rather than a generally shipped feature.

telegram · zaihuapd · Nov 21, 06:13

**「Background」** RDMA \(Remote Direct Memory Access\) lets one machine read and write another&\#x27;s memory directly, bypassing the CPU-heavy networking stack; Windows already exposes it through the NetworkDirect API used with datacenter RDMA adapters. Microsoft&\#x27;s preview applies that same API to USB4 links between PCs, so a compatible inference framework can spread one model across their combined memory and GPU compute without dedicated networking hardware.

**「Impact」** Developers testing the preview will need USB4-equipped PCs and Windows Insider builds, and should treat the ~18.5 token/s figure as a vendor demonstration rather than a general performance guarantee. The approach offers an alternative to dedicated networking hardware for pooling memory and GPU resources across machines.

<details><summary>References</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/microsoftusbblog/introducing-rdma-over-usb4%C2%AE-on-windows-run-larger-local-ai-models-across-pcs/4574602">Introducing RDMA over USB 4 ® on Windows : run larger local AI ...</a></li>
<li><a href="https://www.guru3d.com/story/microsoft-previews-usb4-links-that-let-windows-pcs-pool-memory-and-gpu-resources/">Microsoft previews USB 4 links that let Windows PCs pool memory ...</a></li>

</ul>
</details>

**Tags**: `#RDMA`, `#USB4`, `#local AI inference`, `#Windows`, `#distributed computing`

---

<a id="item-tech-news-3"></a>
### [OpenRouter 警告 MiniMax 模型提示词疑遭第三方读取](https://news.ycombinator.com/item?id=50585962) ⭐️ 8.0/10

OpenRouter 通过邮件通知用户，发往 MiniMax 模型的请求内容可能已被第三方读取。安全研究者在 2026 年 7 月至 10 月间向 MiniMax 模型发送含测试 URL 的提示词，第三方在 40 到 130 小时后访问了这些 URL。OpenRouter 将问题归因于 MiniMax 及其转发方 AtlasCloud、Novita、StreamLake，已下架相关端点的「零数据保留」标签，并建议涉及敏感凭证的用户更换 API Key 和密码。OpenRouter 官网暂未公布相关消息，上述细节来自一份简短的二手摘要，尚未获得独立确认。

telegram · zaihuapd · Nov 21, 06:53

**「Context」** OpenRouter routes requests to third-party inference providers and had labeled some MiniMax endpoints as offering &quot;zero data retention.&quot; The reported incident concerns whether that label held: a researcher&\#x27;s test URLs embedded in prompts sent between July and October 2026 were later fetched by a third party, according to secondary coverage of OpenRouter&\#x27;s notice.

**「影响与建议」** 通过 OpenRouter 向 MiniMax 模型发送过敏感数据的用户应视为提示词可能已外泄，并按 OpenRouter 建议轮换 API Key 和相关密码。依赖「零数据保留」标签判断合规性的用户需注意，受影响端点已不再带有该标签，此前基于该标签的数据处理假设不再成立。

<details><summary>References</summary>
<ul>
<li><a href="https://www.privacyaffairs.com/openrouter-minimax-prompts/">OpenRouter: MiniMax Prompts May Have Been Read by Others</a></li>
<li><a href="https://startupfortune.com/openrouter-warns-minimax-prompts-may-have-been-read-by-a-third-party/">OpenRouter warns MiniMax prompts may have been read by a ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#privacy`, `#llm-inference`, `#openrouter`, `#minimax`

---

<a id="item-tech-news-4"></a>
### [Zhejiang University reports first on-hardware QRAM demonstration](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 8.0/10

A Zhejiang University team reports running a quantum random access memory \(QRAM\) prototype on its own superconducting chip, &quot;Tianmu-2,&quot; which the team describes as the first real-hardware QRAM demonstration. The prototype retrieved 4-bit and 8-bit data with 80.9% and 60.4% accuracy, respectively, according to a paper published in Nature Physics. The team also reports more than 30% lower circuit depth than an unoptimized approach and says it verified local noise resilience in the architecture for the first time. The results come from a brief financial-news report and have not been independently verified from the supplied material; the accuracy figures indicate early-stage performance. The team says its next step is scaling up QRAM research.

telegram · zaihuapd · Nov 21, 08:31

**「Background」** QRAM is a proposed quantum memory architecture that lets a quantum computer address stored data in superposition, a capability needed for many quantum algorithms that rely on fast random access to classical or quantum data. The Zhejiang University work was carried out on &quot;Tianmu-2,&quot; a 125-qubit superconducting processor developed in the researchers&\#x27; lab at the university, according to a separate report on the team&\#x27;s hardware.

**「Impact」** The 60.4% accuracy for 8-bit retrieval suggests the prototype is not yet reliable enough for general use, so any follow-on work would likely focus on error rates and scaling before QRAM can serve as practical quantum memory. The reported circuit-depth reduction and local noise resilience are architecture-level claims that would need independent replication to guide hardware design choices.

<details><summary>References</summary>
<ul>
<li><a href="https://phys.org/news/2026-11-quantum-teleportation-method-weaker-entanglement.html">Quantum teleportation method uses weaker entanglement to transfer...</a></li>

</ul>
</details>

**Tags**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#hardware`, `#research`

---

<a id="item-tech-news-5"></a>
### [Daraxonrasib First-Line Data: 8.2% Complete Responses in 61 Patients](https://event.eortc.org/ena2026/2026/11/20/metastatic-pancreatic-cancer-responds-well-to-initial-treatment/) ⭐️ 8.0/10

Late-breaking data presented at ENA 2026 in Barcelona on November 20 reported that daraxonrasib, an oral RAS\(ON\) multi-selective inhibitor, combined with gemcitabine/nab-paclitaxel produced a confirmed objective response rate of 60.7% and complete responses in 8.2% \(about 1 in 12\) of 61 previously untreated metastatic pancreatic ductal adenocarcinoma patients. Patients received 200 mg once daily; disease control rate was 90.2%, median progression-free survival 12.8 months, 12-month overall survival 76.6%, and median follow-up 18.3 months. The investigators cautioned that this is a single-arm Phase I/II study without a chemotherapy control arm, and that efficacy comparisons must await the ongoing Phase III trial. The drug was approved by the FDA on August 26 under the brand name RASONQUE for previously treated patients, based on the Phase III RMC-302 trial showing median overall survival of 13.2 versus 6.7 months.

telegram · zaihuapd · Nov 21, 11:24

**「Background」** Daraxonrasib is an oral RAS\(ON\) multi-selective inhibitor that targets active-state RAS across multiple KRAS/NRAS mutations, rather than a single G12C variant. The source reports that the FDA approved it on August 26, 2026 under the brand name RASONQUE for previously treated patients, based on the Phase III RMC-302 trial, which showed median overall survival of 13.2 versus 6.7 months; external coverage describes the pivotal study as RASolute 302, a randomized Phase 3 trial. The new ENA 2026 report extends testing to first-line use combined with gemcitabine/nab-paclitaxel.

**「Impact」** The source notes that historical chemotherapy benchmarks put 1-year survival at 22%–48% \(35% in MPACT, 48% for mFOLFIRINOX\), so the 76.6% 12-month rate should not be described as clearly superior to chemotherapy until the randomized Phase III data are available. Daraxonrasib&\#x27;s mechanism differs from single-target G12C drugs: it acts on active-state RAS and covers multiple KRAS/NRAS mutations.

<details><summary>References</summary>
<ul>
<li>Rasonque (daraxonrasib): FDA approval, pivotal trial and safety - 2 Minute Medicine</li>
<li>FDA approves RASONQUE (daraxonrasib) the first broad RAS-targeted medicine in metastatic pancreatic cancer - Medical Update Online</li>

</ul>
</details>

**Tags**: `#biomedical-ai`, `#drug-discovery`, `#clinical-trials`, `#oncology`, `#RAS-inhibitors`

---

<a id="item-tech-news-6"></a>
### [Blogger Traces Monitor USB Hub to 75% Download Speed Loss](https://blog.tymscar.com/posts/studiodisplayethernet/) ⭐️ 7.0/10

A blogger investigating slow downloads found that a monitor&\#x27;s built-in USB hub was throttling Ethernet throughput by roughly 75%. The root cause was extra latency introduced by routing the connection through the monitor: the laptop could not acknowledge packets quickly enough, a buffer on the Ethernet adapter filled, and packets were dropped. Switching to a different adapter that required less frequent acknowledgement resolved the problem. The finding is a single-user troubleshooting account, not an independently measured or vendor-confirmed result.

hackernews · soheilpro · Nov 21, 10:36 · [Discussion](https://news.ycombinator.com/item?id=50587875)

**「Why It Matters」** USB hubs and docks add latency to attached network adapters, and TCP throughput depends on timely acknowledgements; when round-trip time grows, a fixed-size adapter buffer can overflow and drop packets. This makes the failure look like a bandwidth cap rather than a latency problem, which is why it can be hard to diagnose.

**「Practical Takeaway」** Users seeing unexplained throughput loss on a docked or hub-connected Ethernet adapter should test the adapter connected directly rather than through the monitor or dock, and compare adapters, since the blogger&\#x27;s fix came from an adapter with different acknowledgement behavior rather than from the monitor itself.

**「Community Reaction」** One commenter argued the post is better described as a USB network switch problem, since the monitor is incidental. Another summarized the mechanism for readers who missed it: added latency caused slow acknowledgements, buffer fill, and packet drops, with a different adapter fixing it. A separate commenter reported a similar year-long issue with a MacBook and Thunderbolt dock, saying enabling flow control was good enough.

**Tags**: `#networking`, `#usb`, `#troubleshooting`, `#hardware`, `#performance`

---

<a id="item-tech-news-7"></a>
### [FBI and USDA reportedly breached in separate cyberattacks](https://www.theverge.com/tech/1039543/fbi-usda-hacked) ⭐️ 7.0/10

The FBI and USDA were reportedly hacked, according to reporting cited by The Verge. CNN reported that the FBI breach is the second in the last few months and targeted the National Crime Information Center \(NCIC\), the database federal, state, and local law enforcement use to share warrants and missing persons information; President Donald Trump confirmed the hack in a Fox News interview. NBC first reported the USDA breach, and Reuters reported that a payments database is the known extent of that intrusion so far, with former officials warning the scope could be wider. The reports do not specify the attackers, the method, or the full extent of either breach.

rss · The Verge · Nov 21, 17:42

**「Background」** The NCIC is the nationwide database federal, state, and local law enforcement use to share records such as warrants, missing-persons reports, and background checks. The source describes the reported FBI intrusion as the second such attack on the agency in the last few months, but it does not identify the earlier incident or say whether the two breaches are connected.

**「Impact」** The USDA breach reportedly reached a payments database used to pay farmers, and search results describe farmer payments and loan services being disrupted while staff reset database passwords across multiple systems. The FBI incident is said to involve NCIC, the shared law-enforcement database for warrants and missing-persons records, so agencies relying on it face a potential integrity and availability concern; the source does not specify whether NCIC data was accessed or altered.

<details><summary>References</summary>
<ul>
<li><a href="https://www.newsmax.com/newsfront/fbi-national-crime-information-center-kash-patel/2026/11/21/id/1277111/">FBI Probes Apparent Breach of National Crime Database</a></li>
<li><a href="https://www.cnn.com/2026/11/20/politics/fbi-hacked-again-target-crime-database">The FBI was hacked again, this time the breach... | CNN Politics</a></li>
<li>7News DC on X: &quot;Hackers allegedly accessed a U.S. Department of Agriculture (USDA ...</li>
<li>BREAKING: USDA HIT BY CYBERSECURITY INCIDENT — CRITICAL SYSTEMS SHUT DOWN, FARMER PAYMENTS AND LOAN SERVICES DISRUPTED By John A. Patrick Jr.</li>
<li>BREAKING: USDA Cybersecurity Breach Takes Critical Farm Financial Systems Offline</li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#government`, `#data breach`, `#FBI`, `#USDA`

---

<a id="item-tech-news-8"></a>
### [Microsoft Warns Entra Connect Health Flaw Exploited for Tenant Data](https://www.bleepingcomputer.com/news/security/microsoft-entra-connect-health-flaw-exploited-to-steal-tenant-data/) ⭐️ 7.0/10

Microsoft is warning organizations that attackers exploited a vulnerability in its Entra Connect Health service to gain unauthorized access to administrator email addresses and tenant configuration information. The company described the incident as a data breach affecting tenant data. The available report does not specify the vulnerability&\#x27;s technical details, affected versions, or a remediation timeline.

rss · BleepingComputer · Nov 21, 18:01

**「Background」** Entra Connect Health is Microsoft&\#x27;s monitoring service for on-premises identity infrastructure tied to Entra ID, so a flaw there sits in the path between local directory sync and cloud tenant administration. The source excerpt does not specify the vulnerability type, affected versions, or when exploitation began, so the technical mechanism remains undisclosed in the supplied material.

<details><summary>References</summary>
<ul>
<li><a href="https://windowsforum.com/news/microsoft-entra-connect-health-api-flaw-exposed-admin-emails-and-tenant-data.453553/">Microsoft Entra Connect Health API Flaw Exposed Admin Emails ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#microsoft`, `#cloud-identity`, `#data-breach`

---

<a id="item-tech-news-9"></a>
### [Tesla begins overseas rollout of FSD v15](https://x.com/Tesla/status/2124222447855743019) ⭐️ 7.0/10

Tesla announced the overseas rollout of FSD v15, claiming that handling of safety-critical scenarios improves by up to 25x. The update adds a &quot;Tesla Reality View&quot; interface that overlays camera footage and the FSD driving plan on the in-car screen, with full-screen, map, and split-screen views plus a quiet mode. It also overlays navigation cues such as turns, softens and fades the turn-signal chime, and refines speed control around potholes, debris, schools, and bad weather. The 25x figure is a vendor claim from a brief social post and has not been independently verified.

telegram · zaihuapd · Nov 22, 00:03

**「Background」** FSD v15 is a major-version update to Tesla&\#x27;s supervised Full Self-Driving software, following the v14 line that preceded it. Coverage of the rollout describes the release as targeting long-standing weaknesses such as sign reading, potholes, and school-zone speeds, alongside the new Reality View visualization.

**「Impact」** Owners receiving v15 will see a new visualization layer and changed in-cabin alerts, so drivers accustomed to the previous interface and turn-signal sound should expect a different display and audio experience after updating.

<details><summary>References</summary>
<ul>
<li><a href="https://teslanorth.com/2026/11/21/tesla-fsd-v15-first-rollout-reality-view/">Tesla Starts Rolling Out FSD v15 With a New Reality View</a></li>
<li><a href="https://electrek.co/2026/11/21/tesla-fsd-v15-rollout-25x-safety-reality-view/">Tesla launches FSD v15, targets its biggest weaknesses, from ...</a></li>

</ul>
</details>

**Tags**: `#autonomous-driving`, `#tesla-fsd`, `#ai-systems`, `#software-release`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Trump Proposes &\#x27;Huge Tax&\#x27; on U.S. Firms Building AI Data Centers Abroad](https://apnews.com/article/trump-artificial-intelligence-data-centers-f1ac03b73d13445400eeed8631d9d879) ⭐️ 7.0/10

At a White House press conference on November 20, President Trump said he plans to impose a &quot;huge tax&quot; on U.S. tech companies that build AI data centers overseas, aiming to keep those projects in the U.S. and maintain AI competitiveness against China. He said he had not yet told officials within his administration about the plan, and no rate, scope, or timeline has been announced.

telegram · zaihuapd · Nov 21, 03:26

**「Background」** Trump made the remarks at a White House press conference on November 20, framing the proposed tax as a way to keep AI data-center investment in the U.S. and maintain an edge over China. The proposal has no announced rate, scope, or timeline, and Trump said he had not yet told officials inside his administration about it.

**「Who would be affected」** If enacted, the tax would directly affect large U.S. tech companies that site AI data centers abroad, raising the cost of overseas projects relative to building in the U.S. The proposal is an announced intention with no rate, scope, or timeline, and Trump said he had not told internal officials, so it is not yet policy.

<details><summary>References</summary>
<ul>
<li><a href="https://www.reuters.com/technology/trump-says-us-penalize-firms-building-data-centers-abroad-2026-11-20/">Trump says US to penalize firms building data centers abroad</a></li>
<li><a href="https://www.politico.com/news/2026/11/20/trump-overseas-data-center-tax-01178999">Trump says he’ll tax companies building data centers outside US</a></li>
<li><a href="https://www.newsweek.com/trump-tax-us-data-centers-overseas-12748825">Trump Threatens Massive Tax on US Data Centers Built Overseas ...</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#tax policy`, `#US-China tech competition`, `#data centers`, `#technology regulation`

---