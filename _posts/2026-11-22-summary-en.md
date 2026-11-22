---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 53 items, 9 important content pieces were selected

---

**Technology News**
1. [Telegram post claims Lean-verified Riemann Hypothesis proof](#item-tech-news-1) ⭐️ 10.0/10
2. [OpenRouter Discloses Data-Processing Incidents at Inference Providers](#item-tech-news-2) ⭐️ 7.0/10
3. [Blog Claims Anthropic&\#x27;s 2028 Power Mix Is 87% Gas, 11% Coal](#item-tech-news-3) ⭐️ 7.0/10
4. [FBI and USDA reportedly hacked, with NCIC database targeted](#item-tech-news-4) ⭐️ 7.0/10
5. [Rackspace Spot Breach Exposed Customer Kubernetes Secrets](#item-tech-news-5) ⭐️ 7.0/10
6. [Microsoft Entra Connect Health Flaw Exploited in Tenant Data Breach](#item-tech-news-6) ⭐️ 7.0/10

**Financial News**
1. [US Tech Selloff Prompts Emergency Market Measures in Asia](#item-finance-news-1) ⭐️ 9.0/10
2. [FT Report Alleges Nvidia Chip Smuggling Network Linked to Cambodia&\#x27;s Prince Group](#item-finance-news-2) ⭐️ 7.0/10
3. [China Asks US to Withdraw Phone Number Access Limits](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Telegram post claims Lean-verified Riemann Hypothesis proof](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 10.0/10

A Telegram post claims that on November 20, 2026, Levent Alpöge published a Lean formalization of the Riemann Hypothesis comprising roughly 17 million lines of code, and that on November 21 the Lean FRO and Mathlib Initiative jointly certified both the statement and proof as correct. The post further asserts that the community confirmed the statement matches Mathlib&\#x27;s RiemannHypothesis, that the codebase compiles without errors, and that multiple independent proof checkers validated the proof. These claims come from a single Telegram channel and cite a future-dated event; they have not been independently confirmed here and should be treated with strong caution.

telegram · zaihuapd · Nov 21, 16:48

**「Background」** The claim centers on Levent Alpöge, an Anthropic researcher who said on November 20, 2026, that he believed he and Claude had found a proof of the Riemann Hypothesis and a method resolving the Generalized Riemann Hypothesis, releasing a personal Lean archive. External coverage describes that archive as roughly 175,187 files and reports MIT kernel checks, while a note on Alpöge&\#x27;s website frames the result as a claimed proof found with Claude. The Riemann Hypothesis is a long-standing open conjecture about the zeros of the Riemann zeta function, and Lean is an interactive theorem prover in which a formalization can be machine-checked.

**「Why verification matters」** If confirmed, the claim&\#x27;s decisive details would be the consistency of the formal statement with Mathlib&\#x27;s existing RiemannHypothesis definition and successful checking by independent verifiers, since a Lean proof only establishes what its encoded statement says. Readers should await confirmation from the Lean FRO, Mathlib, or the cited Lean community blog before relying on the result.

<details><summary>References</summary>
<ul>
<li><a href="https://www.unite.ai/levent-alpoges-unverified-riemann-claim-puts-claudes-lean-code-in-focus/">Levent Alpöge’s Unverified Riemann Claim Puts Claude’s Lean ...</a></li>
<li><a href="https://casrai.org/news/anthropic-levent-alpoge-claude-lean-riemann-hypothesis-claim-2026">175,000-File Lean Riemann Hypothesis Proof Claim — CASRAI</a></li>
<li><a href="https://lean4.dev/proofs/riemann-hypothesis-claim">The Riemann Hypothesis: a claimed proof, delivered in Lean</a></li>

</ul>
</details>

**Tags**: `#formal-verification`, `#lean`, `#mathematics`, `#riemann-hypothesis`, `#mathlib`

---

<a id="item-tech-news-2"></a>
### [OpenRouter Discloses Data-Processing Incidents at Inference Providers](https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/) ⭐️ 7.0/10

OpenRouter published an announcement disclosing data-processing incidents among its inference providers. The disclosure prompted discussion of how OpenRouter vets providers, what its zero-data-retention \(ZDR\) agreements actually cover, and whether providers forward prompts to upstream services. The source item provides no further technical detail on the incidents themselves, such as which providers were involved, how many prompts were affected, or what remediation was taken.

hackernews · sdko · Nov 22, 02:14 · [Discussion](https://news.ycombinator.com/item?id=50595554)

**「Context」** OpenRouter is a unified API platform that routes requests across many third-party inference providers behind a single interface. The incident disclosure states that OpenRouter off-boarded three providers and removed 125 endpoints from Zero Data Retention eligibility following its investigations, according to the announcement page.

**「What It Means for Users」** One commenter reported being affected by a single prompt and said the incident led them to restrict OpenRouter routing to a manually selected set of providers rather than allowing automatic routing. Another said the disclosure ended their consideration of moving to OpenRouter for an upcoming external AI renewal, citing a lack of visible due diligence and guardrails on provider marketing and classification. These are individual reactions, not verified outcomes of the incidents.

**「Community Reaction」** Commenters debated provider trust: one argued that the best ZDR protection is a direct agreement with the inference provider, while acknowledging that smaller organizations cannot afford that and still must trust provider claims even after auditing security documentation. Another raised concern that some OpenRouter providers forward prompts to an upstream service \(naming MiniMax\) instead of running inference themselves, and a further commenter speculated that cheap decision models could serve as data-collection honeypots, an unverified suspicion rather than a documented finding.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/">Data Processing Incidents on Inference Providers</a></li>
<li><a href="https://downdetector.com/status/openrouter/">OpenRouter down? Current problems and outages | US</a></li>

</ul>
</details>

**Tags**: `#AI privacy`, `#inference providers`, `#OpenRouter`, `#data processing`, `#LLM infrastructure`

---

<a id="item-tech-news-3"></a>
### [Blog Claims Anthropic&\#x27;s 2028 Power Mix Is 87% Gas, 11% Coal](https://betterdatacenterproject.com/2026/11/16/how-ai-is-powered-a-breakdown-of-byop-and-grid-power/) ⭐️ 7.0/10

A post on the Better Data Center Project blog, discussed on Hacker News, projects that Anthropic&\#x27;s data-center energy mix in 2028 will be 87% natural gas and 11% coal. The figures come from a single blog&\#x27;s breakdown of bring-your-own-power and grid sourcing rather than from Anthropic or an independent measurement, and no source content was available to verify the methodology. The claim is a forward-looking projection, not a shipped or reported operating result.

hackernews · happosai · Nov 22, 08:57 · [Discussion](https://news.ycombinator.com/item?id=50597612)

**「Background」** AI data centers require constant power around the clock, which makes their electricity sourcing a distinct infrastructure problem rather than a simple computing cost. Anthropic has already struck a $3.4bn deal to generate gas-fired power for its data centers, according to the Financial Times, so the blog&\#x27;s 2028 projection extends an existing reliance on gas rather than introducing a new one.

**「Why the mix matters」** If the projection holds, the large gas and coal share would tie a major AI model provider&\#x27;s 2028 operations to fossil-fuel generation, making the sourcing choices of data-center operators and their power partners the main lever on those emissions. Readers should treat the percentages as an unverified estimate until Anthropic or an independent assessment publishes actual sourcing data.

**「Debate in the comments」** Commenters split between calls for regulation to price externalities \(sollewitt\) and arguments that model providers already face strong cost incentives to reduce power use \(softwaredoug\). Others disputed the scale of AI energy demand and whether providers are doing enough, with lousken arguing that if individuals can source renewables, Anthropic can too; these are opinions rather than verified findings.

<details><summary>References</summary>
<ul>
<li><a href="https://www.technologyreview.com/2025/05/20/1116327/ai-energy-usage-climate-footprint-big-tech/">We did the math on AI’s energy footprint. | MIT Technology Review</a></li>
<li><a href="https://www.ft.com/content/a6c43402-719e-4295-ae5f-541edb0aeb29?syn-25a6b1a6=1">‘Bold but sane’: what we learnt from Anthropic ’s 240,000-word IPO filing</a></li>

</ul>
</details>

**Tags**: `#ai-infrastructure`, `#data-centers`, `#energy`, `#climate`, `#industry-analysis`

---

<a id="item-tech-news-4"></a>
### [FBI and USDA reportedly hacked, with NCIC database targeted](https://www.theverge.com/tech/1039543/fbi-usda-hacked) ⭐️ 7.0/10

Reports on Friday said both the FBI and the USDA were hacked. CNN reported the FBI breach is the second such attack on the agency in recent months and targeted the National Crime Information Center, the system federal, state, and local law enforcement use to share warrants and missing persons data; President Donald Trump confirmed the FBI hack in a Fox News interview. NBC first reported the USDA breach, and Reuters reported that a payments database is the known extent of that intrusion so far, with former officials warning it may be broader. The accounts are based on secondary reporting and do not establish how the intrusions occurred, who was responsible, or how many records were affected.

rss · The Verge · Nov 21, 17:42

**「Background」** The National Crime Information Center \(NCIC\) is the FBI-run database that federal, state, and local law enforcement use to share records such as warrants and missing-persons reports. According to CNN&\#x27;s reporting cited by The Verge, the reported FBI breach is the second such attack on the agency in the last few months, with this one targeting the NCIC. The USDA breach was first reported by NBC News, which reported that the known extent of that intrusion was a payments database.

**「Impact」** The reported USDA intrusion reached the system used to send payments to farmers, according to NBC News reporting cited by Reuters and ABC News, while the FBI breach reportedly targeted the NCIC database that federal, state, and local law enforcement use to share warrants and missing-persons records. The extent of the USDA intrusion beyond the payments database is not established; former officials cited by Reuters warned the known scope may not be complete.

<details><summary>References</summary>
<ul>
<li><a href="https://nypost.com/2026/11/20/us-news/hackers-reportedly-breach-fbi-crime-database-the-2nd-time-the-bureau-was-targeted-in-months/">Hackers reportedly breach FBI crime database — the 2nd time the...</a></li>
<li><a href="https://www.theguardian.com/us-news/2026/nov/21/usda-fbi-outages-cyber-attack">USDA, FBI breached by hackers amid spate of tech outages ...</a></li>
<li><a href="https://www.reuters.com/legal/litigation/us-department-agriculture-breached-by-hackers-this-week-nbc-news-reports-2026-11-20/">Hackers breached US Department of Agriculture, NBC News ...</a></li>
<li><a href="https://abcnews.com/GMA/Food/new-government-report-sparks-concern-potential-cyberattack-us/story?id=138316014">USDA hit with cyberattack: Sources - ABC News</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#government`, `#data breach`, `#law enforcement`

---

<a id="item-tech-news-5"></a>
### [Rackspace Spot Breach Exposed Customer Kubernetes Secrets](https://www.bleepingcomputer.com/news/security/rackspace-spot-breach-let-hackers-access-customer-kubernetes-secrets/) ⭐️ 7.0/10

Rackspace warned customers that attackers breached its Rackspace Spot cloud platform using compromised credentials. According to the disclosure, the intruders deployed unauthorized workloads and accessed Kubernetes secrets in customer clusters. The supplied report does not specify how many customers or clusters were affected, when the breach occurred, or what remediation steps Rackspace has taken.

rss · BleepingComputer · Nov 21, 22:59

**「Background」** Rackspace Spot is a managed Kubernetes offering in which the provider operates the control plane and underlying infrastructure for customer clusters. Kubernetes Secrets are the standard object for storing sensitive data such as credentials and tokens inside a cluster, so access to them can expose the applications and services those secrets protect. The source does not specify how the credentials were compromised or which customers were affected.

**「Impact」** Affected Rackspace Spot customers should treat Kubernetes secrets in their clusters as potentially compromised and rotate credentials, since attackers could read Secrets, create pods, and list nodes. An extended outage of the Spot administration console also temporarily prevented customers from managing clusters and rotating credentials, delaying cleanup.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/rackspace-spot-breach-let-hackers-access-customer-kubernetes-secrets/">Rackspace Spot breach let hackers access customer Kubernetes ...</a></li>
<li><a href="https://securityelites.com/news/rackspace-spot-breach-kubernetes-secrets-exposed/">Rackspace Spot Breach Exposed Kubernetes Secrets</a></li>

</ul>
</details>

**Tags**: `#cloud security`, `#kubernetes`, `#security breach`, `#rackspace`, `#infrastructure`

---

<a id="item-tech-news-6"></a>
### [Microsoft Entra Connect Health Flaw Exploited in Tenant Data Breach](https://www.bleepingcomputer.com/news/security/microsoft-entra-connect-health-flaw-exploited-to-steal-tenant-data/) ⭐️ 7.0/10

Microsoft is warning organizations that attackers exploited a vulnerability in its Entra Connect Health service to gain unauthorized access to administrator email addresses and tenant configuration information. The disclosure describes an actively exploited flaw resulting in a data breach, but the available excerpt does not specify the vulnerability type, affected versions, or a patch. Microsoft has not, in the supplied material, detailed mitigation steps or the scope of affected tenants.

rss · BleepingComputer · Nov 21, 18:01

**「Background」** Entra Connect Health is a Microsoft service that monitors and reports on the health of Entra Connect, the tool organizations use to synchronize on-premises Active Directory identities into Microsoft Entra ID. A separate report states that Microsoft has addressed the vulnerability, which it described as resulting in unauthorized read-only access to certain tenant-level contact and configuration metadata.

<details><summary>References</summary>
<ul>
<li><a href="https://thepeninsulaqatar.com/article/22/11/2026/microsoft-addresses-security-vulnerability-in-entra-connect-health">Microsoft addresses security vulnerability in Entra Connect Health</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#microsoft`, `#identity`, `#data-breach`

---

## Financial News

<a id="item-finance-news-1"></a>
### [US Tech Selloff Prompts Emergency Market Measures in Asia](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 9.0/10

US tech stocks fell sharply on Friday, with the Nasdaq down 5.28% in one day and the Philadelphia Semiconductor Index down nearly 11%, prompting emergency market-stabilization measures in mainland China, South Korea, and Taiwan. Mainland China lowered its minimum margin requirement to 80%, South Korea eased daily share-buyback limits for three months starting November 24, and Taiwan banned short-selling below the previous close from November 23 and raised its short-selling margin requirement from 130% to 150%.

telegram · zaihuapd · Nov 22, 13:24

**「Background」** The selloff follows a broader slide in chip stocks: the Philadelphia Semiconductor Index fell 10.7% on Nov. 20 and was down 43% from its June high, according to a Nov. 21 report cited by tool-1-2.

**「Impact」** The emergency measures directly affect investors and listed companies in mainland China, South Korea and Taiwan: lower margin requirements in mainland China allow more leveraged buying, while Taiwan&\#x27;s higher margin ratio and short-selling ban curb bearish bets and raise costs for short sellers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.guancha.cn/GuoJi%C2%B7ZhanLue/2026_11_21_909399.shtml">AI恐慌爆发，华尔街震荡，美国科技股 跌 入熊市</a></li>

</ul>
</details>

**Tags**: `#US tech selloff`, `#market volatility`, `#market stabilization policy`, `#short-selling rules`, `#Asian equities`

---

<a id="item-finance-news-2"></a>
### [FT Report Alleges Nvidia Chip Smuggling Network Linked to Cambodia&\#x27;s Prince Group](https://www.ft.com/content/f3ad8a81-3890-4a8a-8853-ff0a94b08ba9?syn-25a6b1a6=1) ⭐️ 7.0/10

The Financial Times, citing people familiar with the matter, reported that Hu Xiaowei, described by the U.S. Treasury as the &quot;number two&quot; figure at Cambodia&\#x27;s Prince Group, is alleged to have helped move Nvidia chips into China. The report cited trade data showing a Megaspeed Malaysian subsidiary declared about $4.6 billion in imports between December 2024 and December 2025, with some chips allegedly reaching China&\#x27;s black market; Prince Group denied the claims.

telegram · zaihuapd · Nov 22, 04:34

**「Background」** The U.S. Treasury sanctioned Hu Xiaowei in June 2026, describing him as the &quot;second-in-command&quot; of Cambodia&\#x27;s Prince Group, which Washington labels a transnational criminal organization \(tool-1-2, tool-1-3\). The allegations also center on Megaspeed, a Singapore-based cloud computing provider that media reports have suspected of involvement in Nvidia chip smuggling, amid U.S. export controls that restrict China&\#x27;s access to advanced semiconductors \(tool-2-1, tool-2-2\).

**「Impact」** The allegations, if substantiated, would point to a route around U.S. export controls on advanced chips reaching China, a focus for semiconductor and trade-policy watchers; the details rest on unnamed sources and company denials.

<details><summary>References</summary>
<ul>
<li><a href="https://home.treasury.gov/news/press-releases/sb0538">Treasury Further Dismantles Overseas Scam Operations ...</a></li>
<li><a href="https://www.state.gov/releases/office-of-the-spokesman/2026/06/dismantling-prince-group-transnational-criminal-organization-and-huione-group/">Dismantling Prince Group Transnational Criminal Organization ...</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/megaspeed-built-network-singapore-malaysia-024836098.html?fr=sycsrp_catchall">How Megaspeed built a network in Singapore and Malaysia to ...</a></li>
<li><a href="https://www.cnn.com/2026/11/14/tech/china-megaspeed-nvidia-scandal-hnk-intl">How the Nvidia scandal lifted the curtain on a loophole that ...</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#export controls`, `#Nvidia`, `#smuggling`, `#China`

---

<a id="item-finance-news-3"></a>
### [China Asks US to Withdraw Phone Number Access Limits](https://www.bloomberg.com/news/articles/2026-11-22/china-objects-to-us-curbs-on-telecoms-access-to-phone-numbers) ⭐️ 7.0/10

China&\#x27;s Commerce Ministry on November 22 urged the US to withdraw a measure that bars China Mobile, China Telecom and China Unicom from directly obtaining US phone numbers, saying it violates non-discrimination and fair-competition principles. The FCC voted on November 19 to tighten national-security requirements on voice-over-internet providers seeking direct access to US numbers, adding a national-security certification aimed at keeping entities, equipment and services on its Covered List off US networks.

telegram · zaihuapd · Nov 22, 06:44

**「Background」** On November 19, 2026, the FCC voted to require interconnected VoIP providers seeking direct access to US phone numbers to meet new national-security certifications, aimed at keeping equipment and services on its Covered List off US networks. The FCC has previously revoked US operating authority from China Telecom Americas \(2021\) and China Unicom Americas \(2022\).

**「Impact」** The FCC measure directly affects China Mobile, China Telecom and China Unicom, which would lose direct access to US phone numbers; the commerce ministry said it will take necessary measures to protect China&\#x27;s interests, leaving open the possibility of further bilateral telecom restrictions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.reuters.com/world/fcc-votes-ban-chinese-telecoms-direct-access-us-phone-numbers-2026-11-19/">FCC votes to ban Chinese telecoms from direct access to US ...</a></li>
<li><a href="https://www.fcc.gov/document/fcc-cracks-down-bad-actors-access-us-phone-numbers-0">FCC Cracks Down on Bad Actors&#x27; Access to U.S. Phone Numbers</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/DOC-427320A1.pdf">FCC Cracks Down on Bad Actors’ Access to U.S. Phone Numbers</a></li>
<li><a href="https://www.fcc.gov/document/china-telecom-americas-order-revocation-and-termination">China Telecom Americas Order on Revocation and Termination</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/FCC-22-9A1.pdf">Federal Communications Commission FCC 22-9 Before the Federal ...</a></li>
<li><a href="https://www.fcc.gov/document/china-unicom-americas-order-revocation">China Unicom Americas Order on Revocation | Federal ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-22/china-objects-to-us-curbs-on-telecoms-access-to-phone-numbers">China Objects to US Curbs on Telecoms’ Access to Phone ...</a></li>
<li><a href="https://www.reuters.com/world/china-opposes-us-fcc-ban-chinese-telecoms-direct-access-us-phone-numbers-2026-11-22/">China opposes US FCC ban on Chinese telecoms&#x27; direct access ...</a></li>
<li><a href="https://www.nst.com.my/business/economy/2026/11/1583171/china-slams-malicious-us-ban-telecom-firms-phone-number-access">China slams &#x27;malicious&#x27; US ban on telecom firms&#x27; phone number ...</a></li>

</ul>
</details>

**Tags**: `#telecom regulation`, `#US-China relations`, `#FCC`, `#national security`, `#telecommunications`

---