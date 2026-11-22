---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 52 items, 8 important content pieces were selected

---

**Technology News**
1. [Claim of Lean-verified Riemann Hypothesis proof remains unconfirmed](#item-tech-news-1) ⭐️ 10.0/10
2. [OpenRouter Discloses Data-Processing Incidents at Inference Providers](#item-tech-news-2) ⭐️ 7.0/10
3. [FBI and USDA reportedly breached in separate cyberattacks](#item-tech-news-3) ⭐️ 7.0/10
4. [Microsoft Entra Connect Health Flaw Exploited in Tenant Data Breach](#item-tech-news-4) ⭐️ 7.0/10
5. [Tesla begins overseas rollout of FSD v15](#item-tech-news-5) ⭐️ 7.0/10

**Financial News**
1. [US Tech Selloff Prompts Emergency Market Measures in Asia](#item-finance-news-1) ⭐️ 8.0/10
2. [FT: Person tied to Cambodia&\#x27;s Prince Group alleged to have helped smuggle Nvidia chips into China](#item-finance-news-2) ⭐️ 7.0/10
3. [China Asks U.S. to Withdraw Phone Number Access Limits](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Claim of Lean-verified Riemann Hypothesis proof remains unconfirmed](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 10.0/10

A Telegram post claims that on November 20, 2026, Levent Alpöge released a Lean formalization of the Riemann Hypothesis comprising roughly 17 million lines of code, and that on November 21 the Lean FRO and Mathlib Initiative jointly certified both the statement and proof as correct. The post further asserts that the community confirmed the statement matches Mathlib&\#x27;s RiemannHypothesis, that the codebase compiles without errors, and that multiple independent proof checkers validated the proof. These are extraordinary claims resting on a single Telegram-sourced post; they should be treated as unverified until the linked Lean community blog post and independent confirmations are checked.

telegram · zaihuapd · Nov 21, 16:48

**「Background」** The claim centers on Levent Alpöge, who said on November 20, 2026 that he believed he and Claude had found a proof of the Riemann hypothesis along with a method resolving the Generalized Riemann Hypothesis, and released Lean code without independent validation of the completed argument, according to Unite.AI. Coverage of the release describes a 175,187-file Lean archive and an &quot;8-hour reversal&quot; following the initial announcement. The current item&\#x27;s certification by Lean FRO and Mathlib is a separate, later claim that the supplied external reports do not confirm.

**「Impact」** If confirmed, the result would be a landmark for both mathematics and formal verification, but until the Lean community blog post and independent checker results are verified, readers should not treat the Riemann Hypothesis as proven or rely on the claimed certification.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unite.ai/levent-alpoges-unverified-riemann-claim-puts-claudes-lean-code-in-focus/">Levent Alpöge’s Unverified Riemann Claim Puts Claude’s Lean ...</a></li>
<li><a href="https://dev.to/kursatyz/17-million-lines-of-lean-code-and-an-8-hour-reversal-levent-alpoge-claude-and-the-riemann-42e7">17 Million Lines of Lean Code and an 8-Hour Reversal: Levent ...</a></li>
<li><a href="https://casrai.org/news/anthropic-levent-alpoge-claude-lean-riemann-hypothesis-claim-2026">175,000-File Lean Riemann Hypothesis Proof Claim — CASRAI</a></li>

</ul>
</details>

**Tags**: `#formal-verification`, `#lean`, `#mathematics`, `#riemann-hypothesis`, `#unverified-claim`

---

<a id="item-tech-news-2"></a>
### [OpenRouter Discloses Data-Processing Incidents at Inference Providers](https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/) ⭐️ 7.0/10

OpenRouter published an announcement disclosing data-processing incidents involving inference providers on its platform. The post does not appear to specify which providers were involved, what data was exposed, or how many users were affected, and no source text was available for this summary. OpenRouter&\#x27;s stated response is described in community discussion as &quot;a few first steps&quot; that lack enforcement power, so the disclosure should be read as an announced remediation plan rather than a verified fix.

hackernews · sdko · Nov 22, 02:14 · [Discussion](https://news.ycombinator.com/item?id=50595554)

**「Background」** OpenRouter is an inference routing service that forwards prompts to third-party providers, and its Zero Data Retention \(ZDR\) setting is meant to signal that prompts and responses are not stored. According to coverage of the announcement, OpenRouter off-boarded three providers and removed 125 endpoints from ZDR eligibility after canary-token research found some providers did not uphold their stated data policies; the findings did not indicate a breach of OpenRouter itself.

**「Impact」** Users of OpenRouter&\#x27;s routing service cannot assume that a provider&\#x27;s zero-data-retention terms reflect what happens downstream: one commenter reported being affected by a single prompt and said the core problem was providers forwarding prompts to an upstream vendor \(MiniMax\) rather than serving inference themselves. That commenter responded by restricting OpenRouter settings to a manually approved list of providers instead of allowing automatic routing.

**「Community Discussion」** Commenters split on the disclosure: one said the breadth of exposures ended their consideration of moving to OpenRouter, arguing there are no due-diligence or guardrails on which providers it markets, while another welcomed the move but argued the strongest zero-data-retention guarantee is a direct agreement with the inference provider, which smaller customers cannot obtain. A third commenter said the incident reinforces that companies&\#x27; privacy promises should not be trusted, and another speculated that cheap decision models may function as honeypots for data acquisition, an opinion offered without evidence.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/">Data Processing Incidents on Inference Providers - openrouter.ai</a></li>
<li><a href="https://openrouter.ai/blog/">Blog — OpenRouter Blog</a></li>
<li><a href="https://www.unite.ai/openrouter-cuts-three-providers-after-ai-prompt-exposure-findings/">OpenRouter Cuts Three Providers After AI Prompt Exposure ...</a></li>

</ul>
</details>

**Tags**: `#ai-inference`, `#privacy`, `#openrouter`, `#llm-infrastructure`, `#data-processing`

---

<a id="item-tech-news-3"></a>
### [FBI and USDA reportedly breached in separate cyberattacks](https://www.theverge.com/tech/1039543/fbi-usda-hacked) ⭐️ 7.0/10

On Friday, November 21, 2026, it was reported that both the FBI and the US Department of Agriculture were hacked. CNN reported that the FBI breach targeted the National Crime Information Center \(NCIC\), the database federal, state, and local law enforcement use to share warrants and missing persons information, and that it was the agency&\#x27;s second such attack in recent months; President Donald Trump confirmed the hack in a Fox News interview. NBC first reported the USDA breach, and Reuters reported that a payments database is the known extent of that intrusion so far, with former officials warning the scope may be broader. The reports rely on secondary sourcing and provide few technical details about attack vectors or confirmed impact.

rss · The Verge · Nov 21, 17:42

**「Prior context」** The National Crime Information Center \(NCIC\) is the FBI&\#x27;s original information-sharing system, connecting local and national law enforcement data on criminal subjects, suspected terrorists, and missing persons, including children. In September, the FBI said it was investigating an apparent breach by a cyber group that claimed it had stolen sensitive information on the bureau&\#x27;s 38,000 employees, according to Al Jazeera.

**「Impact」** Because the reported FBI intrusion targeted the National Crime Information Center, the affected system is the shared database federal, state, and local law enforcement use for warrants and missing-persons records, so any confirmed compromise could affect agencies beyond the FBI itself. The USDA breach is reported to extend at least to a payments database, though former officials cited by Reuters warned the known extent may not be the full scope. Neither report establishes how the intrusions occurred or whether data was exfiltrated.

<details><summary>References</summary>
<ul>
<li><a href="https://www.axios.com/2026/11/21/fbi-hack-personal-records-ncic">Latest hack of FBI puts personal records at risk</a></li>
<li><a href="https://www.aljazeera.com/news/2026/11/21/fbi-national-crime-database-suffers-suspected-breach-reports">FBI national crime database suffers suspected breach ... | Al Jazeera</a></li>
<li><a href="https://www.theguardian.com/us-news/2026/nov/21/usda-fbi-outages-cyber-attack">USDA , FBI breached by hackers amid spate of tech... | The Guardian</a></li>
<li><a href="https://www.zerohedge.com/technology/fbi-probes-suspected-hack-critical-nationwide-crime-database-cyber-pandemic-fears-mount">FBI Probes Suspected Hack Of Critical Nationwide Crime Database As...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#government`, `#data breach`, `#law enforcement`

---

<a id="item-tech-news-4"></a>
### [Microsoft Entra Connect Health Flaw Exploited in Tenant Data Breach](https://www.bleepingcomputer.com/news/security/microsoft-entra-connect-health-flaw-exploited-to-steal-tenant-data/) ⭐️ 7.0/10

Microsoft is warning organizations that attackers exploited a vulnerability in its Entra Connect Health service to gain unauthorized access to administrator email addresses and tenant configuration information. The company described the incident as a data breach affecting tenant data. The available report does not specify the vulnerability&\#x27;s technical details, affected versions, or a remediation timeline.

rss · BleepingComputer · Nov 21, 18:01

**「Background」** Microsoft Entra Connect Health is a monitoring service for hybrid identity deployments that sync on-premises Active Directory with Microsoft Entra ID. According to a report on the incident, Microsoft said it addressed the vulnerability, which had allowed unauthorized read-only access to certain tenant-level contact and configuration metadata.

<details><summary>References</summary>
<ul>
<li><a href="https://thepeninsulaqatar.com/article/22/11/2026/microsoft-addresses-security-vulnerability-in-entra-connect-health">Microsoft addresses security vulnerability in Entra Connect Health</a></li>
<li><a href="https://learn.microsoft.com/en-us/entra/identity/hybrid/connect/reference-connect-health-faq">Microsoft Entra Connect Health FAQ - Azure... | Microsoft Learn</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#microsoft`, `#cloud`, `#identity`

---

<a id="item-tech-news-5"></a>
### [Tesla begins overseas rollout of FSD v15](https://x.com/Tesla/status/2124222447855743019) ⭐️ 7.0/10

Tesla announced on X that it has begun rolling out FSD v15 overseas. The company claims the update improves handling of safety-critical scenarios by 25x, though this figure is a vendor claim and has not been independently verified. The release also adds a &quot;Tesla Reality View&quot; interface that overlays camera footage and the FSD driving plan on the in-car screen, with full-screen, map, and split-screen views plus a quiet mode. Navigation turn prompts can be overlaid on the display, turn-signal chimes are softer and fade gradually, and the update refines driving over potholes and debris and speed control near schools and in bad weather.

telegram · zaihuapd · Nov 22, 00:03

**「Background」** FSD v15 is the next major release of Tesla&\#x27;s end-to-end driving software, and Tesla&\#x27;s own announcement frames it as an upgrade to &quot;every part of the end-to-end driving network.&quot; The 25x safety figure is a Tesla claim rather than an independently measured result, and the source does not specify the baseline or methodology behind it. The new Reality View builds on the existing in-car visualization by rendering a live, movable view of the car&\#x27;s surroundings and FSD&\#x27;s planned path.

**「Impact」** Drivers receiving the update will see a new visualization layer and revised in-cabin alerts, so the changes affect the interface and driving behavior rather than only the underlying model. Because the 25x safety figure comes from Tesla and no independent measurement was provided, users should treat it as an unverified claim until third-party testing is available.

<details><summary>References</summary>
<ul>
<li><a href="https://techau.com.au/tesla-fsd-v15-is-rolling-out-with-new-reality-view-dramatic-capability-improvements/">Tesla FSD V 15 is rolling out with new Reality View ... | techAU</a></li>
<li><a href="https://www.youtube.com/watch?v=eNBqkc7V1nU">Introducing Tesla Self-Driving V 15 - YouTube</a></li>
<li><a href="https://gizmodo.com/its-like-gta-musk-touts-video-game-like-update-to-tesla-fsd-2000843584">Tesla Adds GTA-Like Update to FSD</a></li>

</ul>
</details>

**Tags**: `#autonomous driving`, `#Tesla FSD`, `#AI systems`, `#software release`, `#computer vision`

---

## Financial News

<a id="item-finance-news-1"></a>
### [US Tech Selloff Prompts Emergency Market Measures in Asia](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

US AI tech stocks sold off sharply on Friday, with the Nasdaq falling 5.28% in a single day and the Philadelphia Semiconductor Index dropping nearly 11%, according to the report. In response, mainland China, South Korea, and Taiwan announced market-stabilization measures, including margin and short-selling rule changes.

telegram · zaihuapd · Nov 22, 13:24

**「Background」** The selloff followed an earlier AI-led US tech decline on Nov. 5, 2026, when the Nasdaq fell about 5% and the Philadelphia Semiconductor Index dropped as much as 11.9% before closing down 9.9%, according to the Financial Times. China&\#x27;s three main stock exchanges said the margin requirement for stock purchases on credit would fall to 80% from 100%, effective Nov. 30, Reuters and Bloomberg reported.

**「Impact」** Taiwan&\#x27;s ban on short-selling below the previous close, effective November 23, and its higher 150% margin requirement for stock lending directly affect short sellers and securities lenders there, while South Korea&\#x27;s three-month easing of daily buyback order limits from November 24 affects listed companies and their repurchase plans.

<details><summary>References</summary>
<ul>
<li><a href="https://www.foxbusiness.com/markets/stocks-nov-5-2026">Nasdaq tumbles 5%, Dow plunges more than 1,800... | Fox Business</a></li>
<li><a href="https://www.ft.com/content/7c6ceb4f-d7b1-49ec-9047-0e2e4cd2615c?syn-25a6b1a6=1">US midterms 2026 reaction as it happened: Global stocks tumble as...</a></li>
<li><a href="https://www.reuters.com/world/chinese-exchanges-ease-margin-trading-requirements-aid-stock-markets-2026-11-22/">Chinese exchanges ease margin trading requirements to aid ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-22/china-lowers-margin-requirement-to-80-to-boost-stock-liquidity">China Lowers Margin Requirement to 80% to Boost Stock Liquidity</a></li>
<li><a href="https://en.sedaily.com/world/2026/11/22/china-eases-margin-rules-after-tech-selloff-wipes-out-17">China Eases Margin Rules After Tech Selloff Wipes Out $1.7 ...</a></li>

</ul>
</details>

**Tags**: `#US tech selloff`, `#market stabilization policy`, `#short-selling rules`, `#Asian equities`, `#margin requirements`

---

<a id="item-finance-news-2"></a>
### [FT: Person tied to Cambodia&\#x27;s Prince Group alleged to have helped smuggle Nvidia chips into China](https://www.ft.com/content/f3ad8a81-3890-4a8a-8853-ff0a94b08ba9?syn-25a6b1a6=1) ⭐️ 7.0/10

The Financial Times, citing people familiar with the matter, reported that Hu Xiaowei, described by the U.S. Treasury as the &quot;number two&quot; figure at Cambodia&\#x27;s Prince Group, is alleged to have helped move Nvidia chips into China. The report cites trade data showing about $4.6 billion in declared imports by Megaspeed&\#x27;s Malaysian subsidiary between December 2024 and December 2025, with some chips said to have reached China&\#x27;s black market; Prince Group denied the allegations.

telegram · zaihuapd · Nov 22, 04:34

**「Background」** The US Treasury sanctioned nine individuals and 26 entities linked to Cambodia&\#x27;s Prince Group in June 2026, describing it as a transnational criminal organization; the State Department says its members run cyber-enabled fraud from scam compounds in Southeast Asia \(tool-1-2, tool-1-1\). Megaspeed, the Malaysian subsidiary named in the report, has separately been accused of breaching US export controls to divert Nvidia chips into China \(tool-2-3\).

**「Impact」** The allegations point to a channel through which export-controlled Nvidia chips may reach China despite U.S. restrictions, a concern U.S. lawmakers have already raised in debates over semiconductor export policy. The figures are based on anonymous sourcing and trade declarations, and the group denies the claims, so the scale of any diversion remains unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.state.gov/releases/office-of-the-spokesman/2026/11/dismantling-the-prince-group-transnational-criminal-organization/">Dismantling the Prince Group Transnational Criminal ...</a></li>
<li><a href="https://www.state.gov/releases/office-of-the-spokesman/2026/06/dismantling-prince-group-transnational-criminal-organization-and-huione-group/">Dismantling Prince Group Transnational Criminal Organization ...</a></li>
<li><a href="https://www.dw.com/en/megaspeed-and-the-battle-to-go-high-end-nvidia-chips-into-china/a-79909129">Megaspeed : Nvidia partner at the center of the spy affair</a></li>
<li><a href="https://epoch.ai/publications/chip-smuggling">Diversion and resale: estimating compute smuggling to China</a></li>
<li><a href="https://www.congress.gov/crs_external_products/R/PDF/R48642/R48642.5.pdf">U.S. Export Controls and China: Advanced Semiconductors</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#export controls`, `#Nvidia`, `#smuggling`, `#China trade`

---

<a id="item-finance-news-3"></a>
### [China Asks U.S. to Withdraw Phone Number Access Limits](https://www.bloomberg.com/news/articles/2026-11-22/china-objects-to-us-curbs-on-telecoms-access-to-phone-numbers) ⭐️ 7.0/10

China&\#x27;s Commerce Ministry on November 22 urged the U.S. to withdraw a measure barring China Mobile, China Telecom and China Unicom from directly obtaining U.S. phone numbers, saying it violates non-discrimination and fair competition principles. The FCC voted on November 19 to tighten security requirements for voice-over-internet providers seeking direct access to U.S. numbers, adding national security certification to block entities, equipment and services on its Covered List.

telegram · zaihuapd · Nov 22, 06:44

**「Background」** The FCC voted on November 19 to tighten security requirements for providers seeking direct access to U.S. phone numbers, adding national-security certification intended to keep entities on its Covered List off U.S. networks. The FCC has previously moved against Chinese carriers, including China Mobile International in 2019 and China Telecom in 2020, according to a Yahoo News report.

**「Impact」** The dispute affects the three largest Chinese state-owned carriers and their ability to connect calls directly to U.S. numbers; the Commerce Ministry said the measures are pushing the two countries toward decoupling in telecom, communications and testing certification, and that China will take necessary steps to protect its interests.

<details><summary>References</summary>
<ul>
<li><a href="https://sg.news.yahoo.com/fcc-seeks-bar-hong-kong-093000777.html">FCC seeks to bar Hong Kong Telecom carrier from operating in US</a></li>

</ul>
</details>

**Tags**: `#telecom regulation`, `#US-China relations`, `#FCC`, `#state-owned carriers`, `#trade policy`

---