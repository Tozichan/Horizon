---
layout: default
title: "Horizon Summary: 2026-11-26 (EN)"
date: 2026-11-26
lang: en
---

> From 74 items, 13 important content pieces were selected

---

**Technology News**
1. [1Password Discloses Breach via Hacked Employee GitHub Account](#item-tech-news-1) ⭐️ 8.0/10
2. [Shorter Lean verification of GRH posted to GitHub](#item-tech-news-2) ⭐️ 8.0/10
3. [NFS2root: 12-year-old pre-auth remote root in Linux NFS server](#item-tech-news-3) ⭐️ 8.0/10
4. [FCC approves SpaceX&\#x27;s Starmind plan for up to 1 million AI satellites](#item-tech-news-4) ⭐️ 8.0/10
5. [Minecraft Java Edition RCE Flaw Affects Versions 1.20.5 and Later](#item-tech-news-5) ⭐️ 8.0/10
6. [Hacker News debate on AI and a claimed matrix multiplication breakthrough](#item-tech-news-6) ⭐️ 7.0/10
7. [Italy and Switzerland warn of autonomous AI-driven cyberattacks](#item-tech-news-7) ⭐️ 7.0/10
8. [Drupal Confirms Active Exploitation of Critical RCE Flaw](#item-tech-news-8) ⭐️ 7.0/10
9. [OpenAI Bets on Cybersecurity as a Business Larger Than Coding](#item-tech-news-9) ⭐️ 7.0/10
10. [Tencent open-sources GGUF quantized weights for 224B Hy4 flash](#item-tech-news-10) ⭐️ 7.0/10
11. [三星与 SK 海力士据报通过交叉许可采用长江存储 Xtacking 技术](#item-tech-news-11) ⭐️ 7.0/10

**Financial News**
1. [US Commerce Department reportedly pressured Intel to hand over 10% stake](#item-finance-news-1) ⭐️ 8.0/10
2. [US Plans New Tariffs on China, EU and 12 Other Trading Partners](#item-finance-news-2) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [1Password Discloses Breach via Hacked Employee GitHub Account](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password disclosed a November 2026 security incident in which an attacker compromised an employee&\#x27;s corporate GitHub account and used it to access source code and push malicious code to backend services, resulting in the download of some customer account information. According to the source account, the exposed data includes names, email addresses, account identifiers, and account creation and last-login times; customer vaults and their contents were not affected. 1Password began investigating signs of the GitHub account compromise on November 19, has not disclosed how many users were affected, and says it disabled the account, rotated or revoked potentially exposed internal credentials, and strengthened verification codes for invitation and recovery emails. The company says users do not need to change their accounts but should be alert to phishing.

hackernews · lxhrstn · Nov 25, 17:18 · [Discussion](https://news.ycombinator.com/item?id=50644817)

**「Background」** 1Password&\#x27;s disclosure centers on an employee&\#x27;s corporate GitHub account, which the attacker used to reach source code and push malicious code to backend services. The company says it began investigating indications of that account compromise on November 19, 2026, and that customer vaults and their contents were not affected, though names, email addresses, account identifiers, and account creation and last-login times were exposed. 1Password has not disclosed how many users were affected; it says it disabled the involved account, rotated or revoked potentially exposed internal credentials, and strengthened verification codes for invitation and recovery emails.

**「What Users Should Do」** Because the exposed fields include email addresses and account identifiers, affected users are a natural target for follow-on phishing, and the source says 1Password is advising vigilance rather than account changes. The disclosure does not state whether branch protection or other controls on the compromised GitHub account were missing or bypassed, leaving the code-push path itself unexplained.

**「Community Reaction」** Commenter tptacek argued that compromised employee laptops leading to code pushed to production is the standard pattern behind SaaS breaches, with the odds rising as headcount grows, while noting 1Password&\#x27;s worst case is mitigated by its encryption model. ChrisHardie, a longtime user who keeps a local-only vault, said the incident reinforces his concern that malicious code pushed to production could eventually place an attacker between a user and their data. qixxiq reported receiving a high-quality phishing email containing personal details and a fake vault-sharing link, and ctidd criticized the announcement for not addressing whether branch protection rules were missing or bypassed.

<details><summary>References</summary>
<ul>
<li>Update on a security incident involving 1Password&#x27;s backend systems.</li>
<li>1Password Discloses GitHub Account Breach Exposing Limited Customer Data</li>
<li>1Password posted an update on its Nov 19 security incident. An attacker got into an employee&#x27;s ... - Threads</li>

</ul>
</details>

**Tags**: `#security`, `#supply-chain`, `#saas`, `#password-managers`, `#phishing`

---

<a id="item-tech-news-2"></a>
### [Shorter Lean verification of GRH posted to GitHub](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

A GitHub repository by lsernau hosts a much shorter Lean formalization of the Generalized Riemann Hypothesis, attributed in the item to Anthropic&\#x27;s work. Commenters describe the readable version as roughly 300k lines with a clear split between &quot;known math&quot; and &quot;new math&quot; and human-readable documentation, and one commenter cites a reduction from about 17 million lines to about 76k lines. The supplied evidence does not include the repository&\#x27;s own documentation or independent verification, so the line counts and the attribution to Anthropic remain community-reported rather than confirmed here.

hackernews · nb-t · Nov 25, 21:48 · [Discussion](https://news.ycombinator.com/item?id=50648050)

**「Background」** The Generalized Riemann Hypothesis extends the Riemann Hypothesis, which concerns the locations of the nontrivial zeros of the Riemann zeta function, to a broader class of L-functions. The earlier AI-assisted proof attributed to Anthropic was released as roughly 17 million lines of Lean code and, as of November 2026 reporting, remained unconfirmed. The new repository is presented as a much shorter, more readable Lean formalization of that same work.

**「Impact」** For formal-verification and AI-assisted-proof readers, the reported reduction from roughly 17 million to about 76,000 lines, with a documented split between known and new mathematics, makes the formalization more tractable to inspect and digest. The supplied evidence does not show independent verification of the Lean proof or a human-readable mathematical exposition, so the artifact should be treated as a readability improvement rather than confirmation of the underlying result.

**「Community discussion」** Commenters welcomed the clearer known-versus-new math separation and documentation as aids to digesting the proof, and one linked a Lean Zulip discussion thread. Others debated whether the shorter proof answers a prior concern from Terence Tao that huge proofs without insight are a problem, and one commenter said they would still like a conventional mathematical paper explaining the core argument.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Riemann_hypothesis">Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://phys.org/news/2026-11-sacred-mathematics-riemann-hypothesis-ai.html">&#x27;The sacred object in mathematics&#x27;: The Riemann hypothesis , AI and...</a></li>
<li><a href="https://www.npr.org/2026/11/21/g-s1-154922/anthropic-worker-claims-to-have-solved-a-holy-grail-of-math-problems-with-the-help-of-ai">Anthropic worker claims to have solved a Holy Grail of math... : NPR</a></li>

</ul>
</details>

**Tags**: `#formal-verification`, `#lean`, `#mathematics`, `#ai-assisted-proofs`, `#open-source`

---

<a id="item-tech-news-3"></a>
### [NFS2root: 12-year-old pre-auth remote root in Linux NFS server](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

A blog post describes a pre-auth remote root vulnerability in the Linux kernel&\#x27;s NFS server that reportedly went unnoticed for 12 years. According to the write-up and community discussion, the flaw affects NFS 4.1 and 4.2 and was patched upstream months before the post. No proof-of-concept exploit has been published, and the post&\#x27;s practical mitigation is to disable those protocol versions by writing &quot;-4.1 -4.2&quot; to /proc/fs/nfsd/versions, a change that reverts on reboot.

hackernews · dm · Nov 25, 20:35 · [Discussion](https://news.ycombinator.com/item?id=50647161)

**「Background」** The Linux kernel&\#x27;s in-kernel NFS server \(nfsd\) listens on port 2049 and, when NFSv4.1 or 4.2 is enabled, handles client requests before any user authentication occurs. The OpenSec write-up frames CVE-2026-99362 as a pre-auth remote root flaw in that server code path, which is why the practical mitigation discussed is restricting the enabled protocol versions rather than relying on export-level access controls.

**「Mitigation and exposure」** Administrators running NFS 4.1 or 4.2 on kernels without the upstream fix can disable those versions via /proc/fs/nfsd/versions, but the setting is temporary and must be reapplied after reboot. Commenters note that NFS is rarely exposed to the public internet, which limits real-world exposure, though the pre-auth nature of the flaw means any reachable server is at risk.

**「Community reaction」** Commenters emphasized that no PoC has been posted and that the bug was patched upstream months ago, tempering concern. One commenter shared a working XDP-based firewall rule for blocking the traffic, while another suggested checking whether clients actually use NFS 4.1 or 4.2 before disabling them.

<details><summary>References</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS 2 ROOT ( CVE - 2026 - 99362 ): pre - auth root in Linux nfsd | OpenSec</a></li>

</ul>
</details>

**Tags**: `#linux-kernel`, `#nfs`, `#security-vulnerability`, `#remote-code-execution`, `#mitigation`

---

<a id="item-tech-news-4"></a>
### [FCC approves SpaceX&\#x27;s Starmind plan for up to 1 million AI satellites](https://www.theverge.com/science/1042278/spacex-fcc-starmind-ai-space-data-centers) ⭐️ 8.0/10

The FCC authorized SpaceX to deploy up to 1 million AI chip-equipped satellites for its &quot;Starmind&quot; in-orbit data processing network, calling it the first US approval of a space data center constellation. Satellites would operate at altitudes between 500 and 1002 km, with the first satellite required in service by 2033 and the full constellation operating by 2040. The authorization carries conditions including communications backup, periodic progress reports, and a detailed orbital debris mitigation plan, and the FCC rejected objections from Amazon, Viasat, and the American Astronomical Society. The FCC deferred SpaceX&\#x27;s request to dispose of satellites above 600 km in &quot;graveyard&quot; orbits rather than deorbiting them.

rss · The Verge · Nov 25, 17:44

**「Background」** Starmind is a planned constellation of solar-powered, AI data-center satellites that SpaceX has been developing as of 2026, with its first satellite design designated AI1. The FCC&\#x27;s November 25 approval covers satellites operating at altitudes between 500 and 1002 km, and the agency said it enables deployment &quot;at unprecedented scale.&quot;

**「Impact」** SpaceX must place at least one Starmind satellite in orbit by 2033 and reach the full 1 million-satellite constellation by 2040, with the FCC also requiring communications backup, periodic progress filings, and a detailed orbital-debris mitigation plan. The FCC deferred SpaceX&\#x27;s request to dispose of satellites above 600 km in &quot;graveyard&quot; orbits, leaving that disposal question unresolved. The agency rejected objections from Amazon, Viasat, and the American Astronomical Society, so competing operators and astronomers have no relief from this authorization.

**「Community discussion」** No community comments were available for this item.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Starmind_%28satellite%29">Starmind (satellite) - Wikipedia</a></li>
<li><a href="https://www.satellitetoday.com/connectivity/2026/11/25/fcc-approves-spacexs-1-million-satellite-orbital-data-center-constellation/">FCC Approves SpaceX’s 1-Million Satellite Orbital Data Center ...</a></li>

</ul>
</details>

**Tags**: `#space-computing`, `#AI-infrastructure`, `#satellites`, `#regulation`, `#SpaceX`

---

<a id="item-tech-news-5"></a>
### [Minecraft Java Edition RCE Flaw Affects Versions 1.20.5 and Later](https://github.com/bikini/minecraft2shell) ⭐️ 8.0/10

A publicly disclosed vulnerability, minecraft2shell, published on November 22, shows that a crafted TrueType font in a server resource pack can trigger a native out-of-bounds write in FreeType 2.14.3 and earlier, leading to arbitrary code execution on Java Edition 26.3 Windows clients. Affected versions are 1.20.5 through 1.21.10 and the 26.1–26.4 snapshots; 1.20.4 and earlier and Bedrock Edition are not affected. Mojang still ships lwjgl-freetype 3.4.3 and has no patch available, while a community fix, m2sfix 1.0.0, released November 24, disables hinting via a Java agent or mod. The submitter advises not adding resource packs until a fix lands, setting multiplayer server resource-pack permissions to &quot;disabled,&quot; or installing the community mod.

telegram · zaihuapd · Nov 25, 12:46

**「Background」** The flaw sits in FreeType, the font-rendering library Minecraft&\#x27;s Java client uses through LWJGL&\#x27;s lwjgl-freetype binding. The public minecraft2shell write-up describes how a crafted TrueType font in a server resource pack drives a native out-of-bounds write in FreeType 2.14.3 and earlier, which the researchers say can be turned into code execution on the Windows client. Because the vulnerable component is the bundled native library rather than Minecraft&\#x27;s own Java code, the community fix \(m2sfix 1.0.0\) works by disabling font hinting through a Java agent or mod rather than by patching the game itself.

**「Impact」** Until Mojang ships a fix, server operators and players should disable server resource packs or install the community workaround, since a malicious pack can execute code on the client. The workaround project notes that versions before 1.20.5 never call FreeType, so its hooks have no effect there, and it describes itself as a temporary measure that may produce false positives and false negatives. One external post claims Mojang has since updated the bundled library and that restarting the official launcher pulls the fix, but this is not confirmed by the source item or the workaround repository, which still lists lwjgl-freetype 3.4.3 as of its latest release.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/bikini/minecraft2shell">GitHub - bikini/ minecraft 2 shell : Minecraft to native RCE · GitHub</a></li>
<li><a href="https://github.com/sunrisemc-tw/minecraft2shell-fix">GitHub - sunrisemc-tw/minecraft2shell-fix: Client-side ...</a></li>
<li><a href="https://github.com/sunrisemc-tw/minecraft2shell-fix/releases">Releases · sunrisemc-tw/minecraft2shell-fix · GitHub</a></li>
<li><a href="https://x.com/grok/status/2125304105769791940">Grok on X: &quot;It&#x27;s the Minecraft2Shell RCE. A bug in the ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#minecraft`, `#freetype`, `#open-source`

---

<a id="item-tech-news-6"></a>
### [Hacker News debate on AI and a claimed matrix multiplication breakthrough](https://scottaaronson.blog/?p=10379) ⭐️ 7.0/10

A Hacker News thread with roughly 1,100 points and 960 comments reacted to a Scott Aaronson blog post and a linked paper titled &quot;The matrix multiplication exponent is nine fourths.&quot; The supplied material is largely a link plus comment excerpts, so the paper&\#x27;s technical claims and any role AI played in producing them cannot be verified from the evidence here. The discussion centered on whether AI&\#x27;s apparent strength in axiomatic mathematics implies comparable progress in other sciences.

hackernews · Kotlopou · Nov 25, 19:11 · [Discussion](https://news.ycombinator.com/item?id=50646108)

**「Background」** Matrix multiplication&\#x27;s computational cost is conventionally described by the exponent ω, where multiplying two n×n matrices takes on the order of n^ω operations; the long-standing goal has been to push ω down from the naive value of 3. A preprint dated November 24, 2026, posted in OpenAI&\#x27;s math repository, claims ω equals exactly 9/4 \(2.25\) over every field, combining an upper bound with a matching lower bound for formal arithmetic circuits, according to a summary of the paper. The Hacker News discussion also points to a separate thread on the same paper.

**「Community debate」** Commenters disagreed over how far mathematical results generalize: jsLavaGoat argued that AI skill at &quot;analytic a priori&quot; work like axiomatic math does not imply it will solve other fields or pose the risks imagined in science fiction. utopiah asked how much of the result would have been possible with Lean, MathLib, and computing power alone, without LLMs, suggesting the groundwork may predate current AI tools. Nevermark argued that humans are biologically poorly equipped to register the scale of change being described.

<details><summary>References</summary>
<ul>
<li><a href="https://raw.githubusercontent.com/openai/math/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf">The matrix multiplication exponent is nine fourths</a></li>
<li><a href="https://aiweekly.co/alerts/openai-claims-matrix-multiplication-exponent-is-exactly-94">OpenAI claims matrix multiplication exponent is exactly 9/4</a></li>

</ul>
</details>

**Tags**: `#AI`, `#mathematics`, `#matrix multiplication`, `#scientific progress`, `#community discussion`

---

<a id="item-tech-news-7"></a>
### [Italy and Switzerland warn of autonomous AI-driven cyberattacks](https://www.bleepingcomputer.com/news/security/italy-and-switzerland-warn-of-autonomous-ai-driven-cyberattacks/) ⭐️ 7.0/10

Swiss and Italian cybersecurity agencies have issued a warning about automated cyberattacks powered by AI agents that target organizations in the critical infrastructure sector. The supplied excerpt does not name the specific agencies, describe the attack techniques, or specify which organizations or countries were affected. It also does not indicate whether the warning follows observed incidents or is a precautionary advisory, so the scope and severity of the threat remain unverified.

rss · BleepingComputer · Nov 25, 19:39

**「Background」** The warnings follow Switzerland&\#x27;s National Cyber Security Center confirming its first cases of AI-assisted cyberattacks against organizations in the country, affecting companies and critical infrastructure operators across at least two sectors. Threat research accounts describe the attacks as using multi-agent frameworks that autonomously chained vulnerabilities and misconfigurations, though these details come from a secondary summary rather than the agencies&\#x27; own advisories.

**「Impact」** The warning gives critical-infrastructure operators in Italy and Switzerland a concrete reason to treat AI agents as an active attack vector rather than a theoretical one. Because such agents can read files, call APIs, execute code, and chain actions without human approval at each step, defenders may need to monitor and constrain autonomous tool use inside their environments, not just block conventional malware. The excerpt does not specify which sectors, organizations, or attack techniques were observed, so the practical scope of the warning remains unverified.

<details><summary>References</summary>
<ul>
<li><a href="https://aviatrix.ai/threat-research-center/italy-switzerland-autonomous-ai-driven-cyberattacks-2026/">Italy &amp; Switzerland Warn of Autonomous AI Cyberattacks on ...</a></li>
<li><a href="https://cybersecuritynews.com/switzerland-ai-agent-cyberattacks/">Switzerland Confirms First AI-Agent Cyberattacks That ...</a></li>
<li><a href="https://jetico.com/blog/agentic-ai-security-risks-enisas-warning-and-the-hugging-face-incident/">Agentic AI Security Risks: ENISA&#x27;s Warning &amp; the Hugging... - Jetico</a></li>

</ul>
</details>

**Tags**: `#AI security`, `#cybersecurity`, `#autonomous agents`, `#critical infrastructure`

---

<a id="item-tech-news-8"></a>
### [Drupal Confirms Active Exploitation of Critical RCE Flaw](https://www.bleepingcomputer.com/news/security/hackers-now-exploit-critical-drupal-rce-flaw-to-hijack-sites/) ⭐️ 7.0/10

The Drupal security team has confirmed that a critical remote code execution vulnerability allowing attackers to hijack unpatched sites is being actively exploited in the wild, with exploitation observed since at least Thursday. The source excerpt does not identify the affected Drupal versions, the vulnerable component, or a patch release, so operators should consult Drupal&\#x27;s official security advisory for the specific fix and affected releases. The confirmation of active exploitation is a vendor statement; no independent measurement of the scale of attacks was provided.

rss · BleepingComputer · Nov 25, 10:10

**「Background」** Drupal&\#x27;s security team had disclosed a separate critical flaw, tracked as CVE-2026-132165 and rated 18 out of 25 on the project&\#x27;s risk scale, which could enable site takeover or remote code execution under uncommon configurations, according to The Hacker News. The current report concerns active exploitation of a critical Drupal RCE vulnerability, but the supplied excerpt does not state whether it is the same CVE or a different one.

**「Impact」** Because exploitation is confirmed rather than theoretical, sites running unpatched Drupal installations are exposed to full site takeover, and administrators should apply the vendor&\#x27;s fix promptly and check for signs of compromise rather than waiting for further details.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/drupal-patches-critical-installer-flaw.html">Drupal Patches Critical Installer Flaw That Could Give...</a></li>

</ul>
</details>

**Tags**: `#security`, `#drupal`, `#vulnerability`, `#remote-code-execution`, `#web-security`

---

<a id="item-tech-news-9"></a>
### [OpenAI Bets on Cybersecurity as a Business Larger Than Coding](https://www.theinformation.com/newsletters/ai-agenda/openais-roadmap-making-cyber-bigger-coding-remains-blurry) ⭐️ 7.0/10

OpenAI is positioning cybersecurity as a potential growth engine that could exceed its coding business. CFO Sarah Friar said external estimates putting the cybersecurity market above $300 billion are still far too low, and President Greg Brockman said cybersecurity will become a larger business segment for OpenAI than coding. The company has released GPT-6 Cyber for security research and is expanding its Daybreak trusted-access program, which as of September covered thousands of verified defenders and about 2,000 approved organizations and workspaces, supporting vulnerability discovery, codebase analysis, and binary reverse engineering. The report notes that competition with Anthropic and Google and the path to scaled commercialization remain unclear, and the market-size and business-comparison claims are company assertions.

telegram · zaihuapd · Nov 25, 04:51

**「Background」** OpenAI&\#x27;s Daybreak program is its Trusted Access for Cyber offering, which grants qualified enterprise customers and security practitioners approved access to OpenAI models for authorized security work. According to OpenAI&\#x27;s documentation, Daybreak is split into Blue and Red tiers, with Blue aimed at defensive workflows and Red at advanced, authorized testing. The current report describes Daybreak as having expanded to thousands of verified defenders and roughly 2,000 approved organizations and workspaces by September, alongside the GPT-6 Cyber model for security research.

**「Impact」** Security teams seeking access to GPT-6 Cyber must go through Daybreak&\#x27;s verification and approval process rather than gaining open access, so organizations outside the roughly 2,000 approved workspaces cannot yet use the capability. The report does not specify pricing, general availability, or compatibility details.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity</a></li>
<li><a href="https://help.openai.com/en/articles/20001258-openai-daybreak-trusted-access-for-cyber-overview">OpenAI Daybreak - Trusted Access for Cyber overview</a></li>
<li><a href="https://openai.com/business/solutions/cybersecurity/">AI for Cybersecurity Teams | OpenAI</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#cybersecurity`, `#AI security`, `#business strategy`, `#trusted access`

---

<a id="item-tech-news-10"></a>
### [Tencent open-sources GGUF quantized weights for 224B Hy4 flash](https://mp.weixin.qq.com/s/o0xxShVQX6g2UllrrEv1WQ) ⭐️ 7.0/10

Tencent Hunyuan released GGUF quantized weights for its 224B-parameter Hy4 flash model through its AngelSlim model-compression toolkit. The original weights are about 410.27GiB, while the smallest IQ2-AH variant is 125.73GiB, roughly 30% of the original, and is reported to run on a 64 GB Mac mini using the Strata offload framework. The source cites 89 tokens per second at 10K context on a 48 GB VRAM device, and 47 tokens per second at 32K context for the Q3\_K version on an M5 Max with 128 GB. It also reports that Q3\_K scores within 0.4 points of the original model on benchmarks including DeepSWE v1.1; these figures come from the brief announcement and were not independently verified.

telegram · zaihuapd · Nov 25, 09:29

**「Background」** Hy4 flash is Tencent Hunyuan&\#x27;s roughly 220B-parameter model with about 12B active parameters and a 1M-token context window, and its weights are published on Hugging Face. Tencent distributes AngelSlim, the Hunyuan AI Infra team&\#x27;s model-compression toolkit, which produced the GGUF files referenced in this release. The new item concerns quantized GGUF variants of that already-open model rather than a new base model.

**「Practical effect」** The release gives local-deployment users a quantized path to a 224B model, but the 64 GB Mac mini claim depends on the Strata offload framework rather than fitting the weights in memory, so users should expect offloading overhead and should check that their inference stack supports Strata before relying on the smallest IQ2-AH variant.

<details><summary>References</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=85Gm68lK0sI">Tencent Hy 4 Flash Is Out. Time to Ditch Qwen 3.8 Flash ... - YouTube</a></li>
<li><a href="https://huggingface.co/tencent/Hy4-flash">tencent / Hy 4 - flash · Hugging Face</a></li>
<li><a href="https://github.com/Tencent/AngelSlim">GitHub - Tencent / AngelSlim : Model compression toolkit engineered...</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#quantization`, `#LLM inference`, `#local deployment`, `#Tencent Hunyuan`

---

<a id="item-tech-news-11"></a>
### [三星与 SK 海力士据报通过交叉许可采用长江存储 Xtacking 技术](https://tech.ifeng.com/c/8yLRPKxQy4L) ⭐️ 7.0/10

据报道，三星电子和 SK 海力士已通过交叉许可协议，同意在 3D NAND 闪存中采用长江存储 Xtacking 堆叠技术的部分内容。Xtacking 将存储单元与控制电路（CMOS）分别制作在两片晶圆上，再通过键合工艺合二为一，使两部分能够独立生产和优化。三星、SK 海力士和长江存储三方均拒绝置评，因此该协议的具体范围、许可条款和量产时间尚不明确。

telegram · zaihuapd · Nov 25, 14:33

**「Background」** Xtacking separates a 3D NAND chip&\#x27;s memory array and its CMOS control logic onto two wafers that are then bonded together, allowing each part to be manufactured and optimized independently. According to the source, an Omdia senior analyst said this lets a manufacturer produce the memory array itself while outsourcing the logic circuitry to a foundry, gaining access to more advanced process nodes. Reports citing Nikkei Asia say Samsung and SK hynix reached cross-licensing deals with YMTC covering elements of Xtacking, with TechPowerUp noting both companies are pushing NAND to hundreds of layers and running into single-wafer limits.

**「潜在影响」** 据 Omdia 高级分析师的说法，这种分离式架构允许厂商自行生产存储阵列，并将逻辑电路交由晶圆代工厂制造，从而使用更先进的制程。若协议属实，三星和 SK 海力士可在其 3D NAND 路线中引入晶圆键合方案，但实际采用程度仍取决于未公开的许可细节。

<details><summary>References</summary>
<ul>
<li><a href="https://www.trendforce.com/news/2026/11/25/news-sk-hynix-reportedly-joins-samsung-in-licensing-ymtcs-xtacking-technology-as-nand-race-heats-up/">[News] SK hynix Reportedly Joins Samsung in Licensing YMTC’s ...</a></li>
<li><a href="https://www.techpowerup.com/355199/samsung-and-sk-hynix-to-license-ymtcs-xtacking-technology">Samsung and SK hynix to License YMTC&#x27;s Xtacking Technology</a></li>
<li><a href="https://sammyguru.com/samsung-sk-hynix-ymtc-xtacking-nand-technology/">Samsung and SK hynix Want to License YMTC&#x27;s Xtacking Technology</a></li>

</ul>
</details>

**Tags**: `#3D NAND`, `#semiconductor manufacturing`, `#hybrid bonding`, `#YMTC`, `#memory hardware`

---

## Financial News

<a id="item-finance-news-1"></a>
### [US Commerce Department reportedly pressured Intel to hand over 10% stake](https://www.wired.com/story/inside-trumps-demands-to-another-chips-ceo/) ⭐️ 8.0/10

Court filings cited by WIRED say US Commerce Department lawyers told Intel&\#x27;s CFO in August 2025 that a request for a 10% government equity stake was not a negotiation, warning of unpredictable consequences if the board refused; Intel&\#x27;s board handed over the shares days later. President Trump then said the US government &quot;fully owns and controls&quot; 10% of Intel without paying for it, and the stake is now valued at about $11 billion.

telegram · zaihuapd · Nov 25, 13:25

**「Background」** The reported pressure came during President Donald Trump&\#x27;s second term, which began in January 2025 \(tool-2-1\). The New York Times reported in November 2025 that the administration was taking stakes in private companies including Intel, describing the practice as unusual and showing no sign of slowing \(tool-2-2\).

**「Impact」** Intel shareholders face dilution from a 10% government stake acquired without payment, while other chipmakers receiving federal support may now face similar equity demands, according to analysts cited by NPR.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Second_presidency_of_Donald_Trump">Second presidency of Donald Trump - Wikipedia</a></li>
<li><a href="https://www.nytimes.com/2025/11/25/us/politics/trump-intel-steel-minerals-china.html">Trump Administration Is Taking Billions in Stakes in Firms Like Intel ...</a></li>
<li><a href="https://www.npr.org/2025/09/06/nx-s1-5530190/government-stake-intel-ai-competition-china">The U.S. government is taking a stake in Intel . It&#x27;s rare — and... : NPR</a></li>
<li><a href="https://www.ainvest.com/news/trump-policy-shifts-reshaping-chip-investment-incentives-navigating-high-stakes-semiconductor-landscape-2508/">Trump&#x27;s Policy Shifts and the Reshaping of U.S. Chip Investment...</a></li>

</ul>
</details>

**Tags**: `#semiconductor industry`, `#US industrial policy`, `#Intel`, `#government equity stake`, `#corporate governance`

---

<a id="item-finance-news-2"></a>
### [US Plans New Tariffs on China, EU and 12 Other Trading Partners](https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html) ⭐️ 8.0/10

The US government is reportedly preparing country-specific tariffs under Section 301 of the 1974 Trade Act on 14 trading partners, including China, the EU, Japan and India, aimed at manufacturing overcapacity. China would face an additional 20% on top of the existing 25% tariffs, with a possible rise to 40% if it does not comply with the October 2025 trade truce reached in Busan, South Korea, according to a CNBC report relayed on Telegram.

telegram · zaihuapd · Nov 25, 13:59

**「Background」** The proposal follows a Section 301 investigation that the U.S. Trade Representative self-initiated in March 2026 into structural excess manufacturing capacity across 16 economies, with findings now issued for 14 of them. The possible 40% rate on China is tied to the October 2025 Busan trade truce between Trump and Xi, which the source says China must comply with.

**「Who could be affected」** If enacted, the proposed tariffs would raise import costs for US businesses and consumers buying goods from China, the EU, Japan, India and the other listed partners, with Chinese goods facing the steepest stacked rate. The proposal does not yet specify product scope or effective dates, so the size of the price effect remains unclear.

<details><summary>References</summary>
<ul>
<li><a href="https://kpmg.com/us/en/taxnewsflash/news/2026/11/tnf-ustr-findings-and-proposed-section-301-tariffs-on-14-economies-relating-to-structural-excess-capacity-and-production-in-manufacturing-sectors.html">USTR findings and proposed Section 301 tariffs on 14 ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Busan_Summit">Busan Summit - Wikipedia</a></li>
<li><a href="https://www.cfr.org/articles/united-states-and-china-agree-trade-truce">United States and China Agree to Trade Truce | Council on ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html">U . S . unveils new Section 301 tariffs targeting China , EU and others</a></li>

</ul>
</details>

**Tags**: `#trade policy`, `#tariffs`, `#Section 301`, `#US-China trade`, `#manufacturing`

---