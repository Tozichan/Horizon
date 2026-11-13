---
layout: default
title: "Horizon Summary: 2026-11-13 (EN)"
date: 2026-11-13
lang: en
---

> From 84 items, 20 important content pieces were selected

---

**Technology News**
1. [Telegram Post Claims Jensen Huang Resigned as NVIDIA CEO](#item-tech-news-1) ⭐️ 10.0/10
2. [Rust 1.100 Stabilizes Never Type, Custom Allocators, and Cargo Cooldowns](#item-tech-news-2) ⭐️ 8.0/10
3. [Researcher Chains 22-Year-Old Postgres Type Confusion into RCE](#item-tech-news-3) ⭐️ 8.0/10
4. [Google Releases Gemini 4 Hydrogen Model](#item-tech-news-4) ⭐️ 8.0/10
5. [Apache HTTP Server Patches Critical HTTP/2 RCE Flaw](#item-tech-news-5) ⭐️ 8.0/10
6. [UMAP 0.6 adds new initialization and optimizers, with opt-in defaults](#item-tech-news-6) ⭐️ 8.0/10
7. [Gemma 3 Encodes Spatial Maps That Its Answers Don&\#x27;t Use](#item-tech-news-7) ⭐️ 8.0/10
8. [AMD&\#x27;s Mike Clark Discusses Zen 6 in Chips and Cheese Interview](#item-tech-news-8) ⭐️ 7.0/10
9. [Apple&\#x27;s Foundation Models framework adds on-device and Private Cloud Compute access](#item-tech-news-9) ⭐️ 7.0/10
10. [Open-source project runs 16B LLMs on sub-1GB devices](#item-tech-news-10) ⭐️ 7.0/10
11. [Developer Builds Custom App to Replace Embroidery Machine Subscription](#item-tech-news-11) ⭐️ 7.0/10
12. [Fireworks AI Breach Exposes Notion Users&\#x27; Chat Transcripts](#item-tech-news-12) ⭐️ 7.0/10
13. [Hackers Used 4,837 Compromised GitHub Accounts to Steal Cloud Credentials](#item-tech-news-13) ⭐️ 7.0/10
14. [N-able N-central zero-day &quot;4EverAble2Shell&quot; exploited to mine crypto](#item-tech-news-14) ⭐️ 7.0/10
15. [Researcher Releases Windows SignDrop Zero-Day Exploit for SYSTEM Access](#item-tech-news-15) ⭐️ 7.0/10
16. [Independent audit finds TRIBE v2 lacks retinotopy and tonotopy but shows MT+ motion selectivity](#item-tech-news-16) ⭐️ 7.0/10
17. [US Commerce Department to finalize rule closing remote AI chip access for Chinese firms](#item-tech-news-17) ⭐️ 7.0/10
18. [Apple details Secure Exclaves for audio/video privacy](#item-tech-news-18) ⭐️ 7.0/10
19. [Telegram Widgets 被指存在沙箱逃逸远程代码执行漏洞](#item-tech-news-19) ⭐️ 7.0/10

**Financial News**
1. [China Approves Eli Lilly&\#x27;s Oral Weight-Loss Drug, a First for the Country](#item-finance-news-1) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Telegram Post Claims Jensen Huang Resigned as NVIDIA CEO](https://nvidianews.nvidia.com/news/nvidia-announces-ceo-transition) ⭐️ 10.0/10

A Telegram post attributed to an NVIDIA newsroom URL claims Jensen Huang has resigned as president, CEO, and director effective immediately, with CFO Colette Kress named interim CEO while continuing as CFO and a board search for a permanent successor underway. The post also says the board appointed Harvey C. Jones as its first chair and that operations, customer commitments, and the product roadmap are unaffected, with Q3 results still due November 17. The claim is not corroborated within the supplied material: it rests on a single Telegram post, and the accompanying links and RSS snippets are unverified excerpts rather than confirmed reporting. The post also includes an unrelated political remark about Tim Cook that is not part of the corporate announcement.

telegram · zaihuapd · Nov 12, 13:52

**「Background」** NVIDIA&\#x27;s board announced the transition in a press release dated Nov. 12, 2026, stating that Jensen Huang resigned as President, CEO, and board member effective immediately, with CFO Colette Kress named interim CEO and Harvey C. Jones appointed the company&\#x27;s first board chair. Reuters reported that Huang had a relationship with a second employee, and the source material also links the resignation to questions about export-control compliance and the company&\#x27;s open-source AI commitments.

**「Why verification matters here」** If accurate, the change would put an interim CEO in charge of the central supplier of AI accelerators during an active export-control dispute, and the post&\#x27;s own claim that the November 17 earnings date is unchanged would be the near-term checkpoint to watch. Readers should treat the resignation as unconfirmed until NVIDIA&\#x27;s newsroom or a major wire service publishes the announcement directly.

**「Commenter reactions」** Hacker News commenters largely debated motives rather than confirming the event: one argued the timing and the leak&\#x27;s beneficiaries deserve scrutiny, another said a visible CEO&\#x27;s perceived stability matters to the AI economy, and a third speculated that export-ban compliance, not the reported affair, is the real issue. Others floated theories about open-model strategy and competition with other AI chip designers; these are opinions, not established facts.

<details><summary>References</summary>
<ul>
<li><a href="https://investor.nvidia.com/news/press-release-details/2026/NVIDIA-Announces-CEO-Transition/">NVIDIA Corporation - NVIDIA Announces CEO Transition</a></li>
<li><a href="https://www.reuters.com/business/retail-consumer/nvidia-ceo-jensen-huang-step-down-big-blow-ai-boom-2026-11-12/">Nvidia CEO Jensen Huang resigns in blow to AI boom he helped ...</a></li>

</ul>
</details>

**Tags**: `#nvidia`, `#leadership-change`, `#ai-hardware`, `#semiconductors`, `#industry-news`

---

<a id="item-tech-news-2"></a>
### [Rust 1.100 Stabilizes Never Type, Custom Allocators, and Cargo Cooldowns](https://blog.rust-lang.org/2026/11/12/Rust-1.100.0/) ⭐️ 8.0/10

Rust 1.100 ships a large batch of stabilizations, including the never type and custom allocators, according to the release announcement and community discussion. Cargo gains dependency cooldowns via RFC 3923: when configured, the resolver ignores versions published more recently than the configured minimum age unless they are already in Cargo.lock. Cargo now also reports unused dependencies by default \(with \`cargo::unused\_dependencies\` set to \`warn\`\), and \`cargo install\` uses the lockfile in the .crate tarball by default, making \`--locked\` a no-op. Commenters note additional stabilized APIs not covered in the blog post, such as \`bool::toggle\(\)\`, \`Box::map\(\)\`, and \`str::trim\_prefix\(\)\`/\`trim\_suffix\(\)\`.

hackernews · mbStavola · Nov 12, 18:39 · [Discussion](https://news.ycombinator.com/item?id=50472038)

**「Background」** Rust ships on a six-week release train, with each numbered version bundling stabilizations of features that previously required nightly-only flags. Cargo&\#x27;s dependency cooldowns, introduced in 1.100.0, implement RFC 3923: when configured, the resolver skips crate versions published more recently than the configured minimum age unless they already appear in Cargo.lock. The same release adds a built-in unused-dependency check through the cargo::unused\_dependencies lint.

**「Impact for Rust Users」** Projects that enable the minimum publish age setting will see Cargo resolve to older crate versions unless a newer one is already pinned in Cargo.lock, which changes how fresh releases enter dependency graphs. The unused-dependency warning is on by default, so builds may surface new warnings, and scripts relying on \`cargo install --locked\` should note it no longer changes behavior.

**「Community Reaction」** Commenters welcomed the release, singling out the never type, custom allocators, dependency cooldowns, and unused-dependency warnings as favorites, and one noted that several stabilized APIs went unmentioned in the blog post. A dissenting commenter asked whether compiler performance improved, citing long compile times and large temporary file buildup requiring frequent \`cargo clean\`.

<details><summary>References</summary>
<ul>
<li><a href="https://releases.rs/docs/1.100.0/">1.100.0 | Rust Changelogs - releases.rs</a></li>
<li><a href="https://doc.rust-lang.org/nightly/releases.html">Rust Release Notes</a></li>

</ul>
</details>

**Tags**: `#rust`, `#programming-languages`, `#cargo`, `#open-source`, `#compilers`

---

<a id="item-tech-news-3"></a>
### [Researcher Chains 22-Year-Old Postgres Type Confusion into RCE](https://mehmetince.net/part-3-6-how-i-ended-up-turning-a-22-year-old-postgresql-type-confusion-primitive-into-rce-cve-2026-6460/) ⭐️ 8.0/10

A security researcher published a write-up describing how a 22-year-old PostgreSQL type-confusion primitive was chained into remote code execution, tracked as CVE-2026-6460. The attack requires an authenticated database account, and the researcher documents the path from that primitive to full server compromise. The post is a technical research account rather than a vendor advisory, and no patch version or affected release range is stated in the supplied material.

hackernews · ozirus · Nov 12, 18:22 · [Discussion](https://news.ycombinator.com/item?id=50471761)

**「Background」** PostgreSQL&\#x27;s internal Datum representation pairs a value with a separate type identifier, and the researcher&\#x27;s write-up traces the type-confusion primitive to that long-standing design. The fix landed as CVE-2026-6460, described by PostgreSQL as type confusion after ALTER ... SET DATA TYPE that lets an object creator execute arbitrary code as the operating system user running the database; the researcher&\#x27;s post says it introduces composite attribute versioning and was part of a release containing 52 new CVEs, six tied to this article.

**「Who is affected」** Because exploitation starts from an authenticated database session, the practical risk is highest for multi-tenant or shared PostgreSQL deployments where one tenant&\#x27;s database credentials should not grant control of the whole server. Operators of such setups should treat database-account isolation as a security boundary and watch for a vendor fix, since the supplied material does not identify a patched version.

**「RCE or privilege escalation?」** Commenters including logophobia and jmuguy argued the attack is better described as privilege escalation than RCE, since it requires authenticated database access and mainly matters for multi-tenant databases. Others, such as igbanam and sailfast, praised the author for documenting the research path and PostgreSQL internals, while amluto questioned the internal Datum design that keeps a type id separate from its value.

<details><summary>References</summary>
<ul>
<li><a href="https://www.postgresql.org/support/security/CVE-2026-6460/">PostgreSQL : CVE - 2026 - 6460 : PostgreSQL type confusion after...</a></li>
<li><a href="https://mehmetince.net/part-3-6-how-i-ended-up-turning-a-22-year-old-postgresql-type-confusion-primitive-into-rce-cve-2026-6460/">Part 3/6 | How I Ended Up Turning a 22-Year-Old PostgreSQL ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#postgresql`, `#vulnerability-research`, `#database-internals`, `#exploitation`

---

<a id="item-tech-news-4"></a>
### [Google Releases Gemini 4 Hydrogen Model](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-hydrogen/) ⭐️ 8.0/10

Google introduced Gemini 4 Hydrogen, a new flagship-generation model aimed at fast execution for everyday coding and agentic workflows, and made it available to developers, enterprises, and general users. Google lists a flat price of $1.50 per million input tokens and $7.50 per million output tokens. The company claims it is 2.5x faster than Gemini 3.8 Flash, that its Terminal-Bench 4.1 score rose from 18.2% to 57%, and that its default tier beats Argon on the Artificial Analysis index. These are vendor claims; the supplied material does not include independent measurements.

hackernews · dvaplima · Nov 12, 18:01 · [Discussion](https://news.ycombinator.com/item?id=50471431)

**「Background」** Gemini 4 Hydrogen replaces Gemini 3.8 Flash, the model it is benchmarked against: Google reports Terminal-Bench 4.1 rising from 18.2% to 57% and a 2.5x speed improvement over 3.8 Flash. Google&\#x27;s blog describes Hydrogen as a fast, cost-efficient model for agentic workflows, priced flat across its 1 million-token context window at $1.50 per million input tokens and $7.50 per million output tokens. A separate report describes an Orchestrator that pairs Carbon&\#x27;s reasoning with Hydrogen&\#x27;s faster execution while using 24% less quota.

**「Impact」** Commenters report that Gemini 3.8 Flash was replaced by &quot;4 Hydrogen&quot; immediately in the interface, so users comparing models now face a new name with no obvious ordering. One commenter notes the new model is priced the same as undiscounted 3.8 Flash and well above what users currently pay for 3.8 Flash, 3.5 Flash Lite, or older Gemini models, raising the question of whether Google is dropping its fast-and-cheap tier.

**「Community Discussion」** The main debate concerns naming: one commenter argues that element names work for separate products but not for models meant to be compared, and that &quot;Hydrogen&quot; intuitively sounds stronger than &quot;Argon.&quot; Another infers from the low atomic weight, Search availability, and 2.5x speed claim that Hydrogen is an entry-level replacement for 3.5 Flash Lite, and questions the higher pricing. Separate complaints describe account suspensions for command-line use and glitches in the Gemini iPhone app.

<details><summary>References</summary>
<ul>
<li><a href="https://interestingengineering.com/ai-robotics/google-gemini-4-hydrogen-coding-benchmark">Google launches Gemini 4 Hydrogen for faster coding and agentic...</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-hydrogen/">Introducing Gemini 4 Hydrogen for Agentic Workflows</a></li>

</ul>
</details>

**Tags**: `#AI models`, `#Google Gemini`, `#LLM`, `#model pricing`, `#AI industry`

---

<a id="item-tech-news-5"></a>
### [Apache HTTP Server Patches Critical HTTP/2 RCE Flaw](https://www.bleepingcomputer.com/news/security/apache-http-server-patches-critical-http-2-remote-code-execution-flaw/) ⭐️ 8.0/10

Apache HTTP Server has released a patch for a critical vulnerability in its HTTP/2 module that could allow an unauthenticated attacker to achieve remote code execution. The flaw affects servers running the HTTP/2 component, and the fix is available now. The supplied report does not specify affected version numbers, the exact exploitation mechanism, or whether exploitation has been observed in the wild, so operators should consult Apache&\#x27;s advisory for version and mitigation details.

rss · BleepingComputer · Nov 12, 19:12

**「Background」** The flaw is tracked as CVE-2026-119618 and affects the mod\_http2 module, which implements HTTP/2 support in Apache HTTP Server. Red Hat&\#x27;s Product Security team rated it Critical and reported that public research demonstrated a reliable exploit against a default-configured server with mod\_http2 enabled, allowing arbitrary command execution.

**「Impact」** Operators of affected Apache HTTP Server installations should upgrade to version 2.4.71 or later, which addresses the race condition in \`assign\_headers\(\)\` in \`mod\_http2\` \(CVE-2026-119618\). Because the flaw is exploitable by unauthenticated attackers, servers exposing HTTP/2 should be prioritized for patching; a detection-only scanner is also available for triaging whether an owned install remains vulnerable.

<details><summary>References</summary>
<ul>
<li><a href="https://access.redhat.com/security/vulnerabilities/RHSB-2026-017">RHSB-2026-017 Remote Code Execution - Apache HTTP Server (CVE ...</a></li>
<li><a href="https://access.redhat.com/security/cve/cve-2026-119618">CVE-2026-119618 - Red Hat Customer Portal</a></li>
<li><a href="https://www.wiz.io/blog/cve-2026-119618-rce-apache-http-server-vulnerability">Critical RCE Vulnerability in Apache HTTP Server ... | Wiz Blog</a></li>
<li><a href="https://github.com/foxcornlab/apache-httpd-scanner">GitHub - foxcornlab/ apache -httpd-scanner: Detection-only triage for...</a></li>
<li><a href="https://www.enigma-global.com/cert-alerts/13712">Critical RCE Vulnerability in Apache HTTP Server : Everything You...</a></li>

</ul>
</details>

**Tags**: `#security`, `#apache`, `#http2`, `#vulnerability`, `#remote-code-execution`

---

<a id="item-tech-news-6"></a>
### [UMAP 0.6 adds new initialization and optimizers, with opt-in defaults](https://www.reddit.com/r/MachineLearning/comments/1xudaah/umap_06_new_initialization_new_optimizers_and/) ⭐️ 8.0/10

UMAP 0.6 ships a new recursive initialization, new optimizers, and a nearest-neighbor search the author says is about 4x faster through better use of PyNNDescent. The author reports that on 3 million arXiv papers the release finishes in under 5 minutes, while a seeded UMAP 0.5 run takes 52 minutes and is single-threaded; UMAP 0.6 runs are reproducible with a fixed seed across all cores. The new initialization and optimizers are opt-in via compatibility\_layout=False because they change output, and the author says future versions will make them the default. Install with pip install -U umap-learn or from conda-forge.

reddit · r/MachineLearning · /u/lmcinnes · Nov 12, 13:51

**「Background」** UMAP is a widely used open-source dimensionality-reduction library, installed as \`umap-learn\`, that builds low-dimensional layouts from a nearest-neighbor graph. Its earlier 0.5 release relied on spectral or PCA initialization and, per the author, ran seeded layouts single-threaded. The 0.6 release changes both the initialization and optimizer, but the new behavior is opt-in via \`compatibility\_layout=False\` because it alters output.

**「What it means for users」** Users who want the speed and quality gains must explicitly set compatibility\_layout=False, which changes results and therefore breaks reproducibility against existing 0.5 pipelines; leaving it unset preserves the older behavior. The author attributes the fidelity gains at million scale to hard-negative mining and better handling of high repulsion strengths, and asks users to report how the opt-in path performs.

**Tags**: `#umap`, `#dimensionality-reduction`, `#machine-learning`, `#open-source`, `#performance`

---

<a id="item-tech-news-7"></a>
### [Gemma 3 Encodes Spatial Maps That Its Answers Don&\#x27;t Use](https://www.reddit.com/r/MachineLearning/comments/1xuqs9d/gemma_3_builds_a_linearly_decodable_spatial_map/) ⭐️ 8.0/10

An independent, preregistered study of Gemma 3 12B and 27B reports that linear probes can recover every object&\#x27;s position from text-only layout descriptions such as &quot;A is 3 north of B, C is 2 east of A,&quot; including positions that require combining two sentences, with R² of 0.74. However, ablating that spatial map costs no more than erasing random directions, indicating the model&\#x27;s answers do not read it. The authors instead find a per-sentence 2-D code that distributed alignment search \(DAS\) recovers at 72% and 83% \(versus 0% for random\), which behaves like a switch rather than a coordinate. Reading answers directly off the unused map outperforms the model on chain questions, 80% versus 73%. The findings are self-reported by the author, with a linked paper, code, and demo.

reddit · r/MachineLearning · /u/Cristhian-AI-Math · Nov 12, 22:29

**「Background」** Gemma 3 is Google&\#x27;s open-weight model family, and the 12B and 27B sizes examined here are the larger variants in that lineup. Google&\#x27;s release notes also list Gemma Scope 2, an interpretability suite for Gemma 3 models, indicating that tooling for probing these models&\#x27; internal representations exists. The study&\#x27;s method—linear probes and ablation on internal activations—is a standard interpretability approach for testing whether a representation is both readable and actually used.

**「Impact」** The dissociation suggests that probe accuracy alone is insufficient evidence that a model uses an internal representation, so interpretability work on spatial or structured reasoning should pair probing with causal ablations or DAS before drawing conclusions about mechanism. The reported 80% versus 73% gap also implies that decoding from the unused map can outperform the model itself on chain questions, a concrete target for follow-up replication.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.google.dev/gemma/docs/releases">Gemma releases - Google AI for Developers</a></li>

</ul>
</details>

**Tags**: `#interpretability`, `#large language models`, `#spatial reasoning`, `#probing`, `#Gemma`

---

<a id="item-tech-news-8"></a>
### [AMD&\#x27;s Mike Clark Discusses Zen 6 in Chips and Cheese Interview](https://chipsandcheese.com/p/talking-zen-6-with-mike-clark-at) ⭐️ 7.0/10

Chips and Cheese published an in-depth interview with AMD&\#x27;s Mike Clark about Zen 6. The supplied material provides only the interview&\#x27;s title and a brief reader comment, so the specific architectural claims, product details, and any timelines discussed cannot be verified from the available source. The item is a design discussion rather than a product announcement.

hackernews · dverlaeckt80 · Nov 12, 14:12 · [Discussion](https://news.ycombinator.com/item?id=50467460)

**「Context」** Zen 6 is AMD&\#x27;s successor to the Zen 5 core family, and the interview frames it as an evolution of Zen 5 with expanded out-of-order structures and iterative improvements, while also covering how the Zen 6 and Zen 6c variants differ. AMD chief architect Mike Clark described five design goals for the family, including a major core performance increase, fuller use of the dense design style for throughput, better AI capability for agentic workloads, a lower-latency operating point, and expanded confidential computing.

**「Community reaction」** One commenter, koutakun, called the article interesting and said it is very rare to see CPU designers go into this much depth. That is a reader&\#x27;s opinion about the interview&\#x27;s level of detail, not an assessment of the technical claims.

<details><summary>References</summary>
<ul>
<li><a href="https://chipsandcheese.com/p/talking-zen-6-with-mike-clark-at">Talking Zen 6 with Mike Clark at AMD In-Depth</a></li>
<li><a href="https://www.techpowerup.com/review/amd-zen-6-technical-deep-dive/4.html">AMD Zen 6 Technical Deep Dive - Zen 6 Core Architecture ...</a></li>
<li><a href="https://chipsandcheese.com/p/amds-zen-6-family-feeding-the-beast">AMD’s Zen 6 Family: Feeding the Beast - by George Cozma</a></li>

</ul>
</details>

**Tags**: `#hardware`, `#cpu-architecture`, `#amd-zen`, `#chips-and-cheese`, `#semiconductor`

---

<a id="item-tech-news-9"></a>
### [Apple&\#x27;s Foundation Models framework adds on-device and Private Cloud Compute access](https://developer.apple.com/foundation-models-framework/) ⭐️ 7.0/10

Apple&\#x27;s Foundation Models framework gives developers access to on-device models and Apple&\#x27;s Private Cloud Compute \(PCC\) from their apps. According to a commenter quoting Apple&\#x27;s developer documentation, developers enrolled in the App Store Small Business Program with fewer than two million first-time App Store downloads can use PCC with no cloud API cost, where Apple Intelligence is available, and can test PCC features via TestFlight or ad hoc distribution. The source page itself provided no content, so the framework&\#x27;s exact API surface and release status are not established here. Community reports describe practical use, but eligibility and entitlement details remain partly unconfirmed.

hackernews · kermatt · Nov 12, 21:13 · [Discussion](https://news.ycombinator.com/item?id=50474361)

**「Background」** Apple&\#x27;s Foundation Models framework lets apps use the on-device models behind Apple Intelligence, and Apple says any app can tap into them at no cost per request, with features working offline. Apple&\#x27;s WWDC 2026 session on the framework covers access to Private Cloud Compute, integration of third-party and open-source models, and vision capabilities. Because the framework is a native macOS/iOS framework rather than downloadable model weights, tools built around conventional model files, such as Ollama, have requested a dedicated Apple backend to support it.

**「Impact」** For eligible developers, PCC access reportedly carries no cloud API cost, which changes the economics of shipping model-backed features compared with paying per-token cloud APIs. Developers outside the stated eligibility conditions, or in regions without Apple Intelligence, may not get the same access, and one commenter said they believe special entitlements are currently limited to Siri&\#x27;s desktop app and still needs to verify this.

**「Community discussion」** Commenters reported mixed practical experience: one said they have used Foundation Models in an app called Noodle and liked working with it, while another said local models run capably on an M1 with 8GB of RAM. Others noted that Anthropic&\#x27;s Claude already supports App Attest for authentication and questioned whether the framework had received an update, since the linked page appeared unchanged.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.apple.com/videos/play/wwdc2026/241/">What’s new in the Foundation Models framework ... - Apple Developer</a></li>
<li><a href="https://github.com/ollama/ollama/issues/19116">Feature request: Native support for Apple Foundation Models ...</a></li>
<li><a href="https://www.apple.com/apple-intelligence/">Apple Intelligence and Siri - Apple</a></li>

</ul>
</details>

**Tags**: `#apple`, `#foundation-models`, `#on-device-ai`, `#private-cloud-compute`, `#ios-development`

---

<a id="item-tech-news-10"></a>
### [Open-source project runs 16B LLMs on sub-1GB devices](https://github.com/hyperionaidev/smolmaxxing/) ⭐️ 7.0/10

An open-source project called smolmaxxing, started by author mrashad74 at their AI company, reports running 16B-parameter models on an iPad Air 1st generation and a Xiaomi TV box, both with less than 1GB of usable memory. The effort relies on custom kernels and modified models, with the kernels, results, and modified models published on GitHub and Hugging Face for reproduction. These are self-reported, early-stage claims that have not been independently verified, and no source content was supplied beyond the author&\#x27;s description.

hackernews · mrashad74 · Nov 12, 15:23 · [Discussion](https://news.ycombinator.com/item?id=50468888)

**「Background」** The project builds on llama.cpp, the widely used open-source LLM inference engine, but requires a patched build: the project&\#x27;s README states that stock llama.cpp cannot load its published model files. Its earlier experiment was a 260K-parameter story model, so the current claim of 16B models on sub-1GB devices is a much larger step that the author reports without independent verification.

**「What it means for developers」** Because the kernels and modified models are published, developers can attempt to reproduce the results on their own low-memory hardware rather than relying on the author&\#x27;s benchmarks. The author is soliciting more challenging target devices, so the practical value depends on whether independent reproductions confirm the reported speeds.

**「Community reaction」** Commenters welcomed the trend toward small local models: nico said a locally trained 6.5M-parameter model now handles reasoning and multi-step tasks, while cjdell described experimenting with tiny models for agentic tool calling on older 2GB–11GB GPUs and said tool-calling output has improved. Farmadupe2 argued that writing an inference engine is now largely a matter of compute and that modern coding agents can handle much of the porting work, making sourcing old hardware and granting SSH access the harder part.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/hyperionaidev/smolmaxxing/">GitHub - hyperionaidev / smolmaxxing : maxxing the ability to run...</a></li>

</ul>
</details>

**Tags**: `#LLM inference`, `#edge computing`, `#open source`, `#model optimization`, `#hardware`

---

<a id="item-tech-news-11"></a>
### [Developer Builds Custom App to Replace Embroidery Machine Subscription](https://github.com/simpsoka/zigzag) ⭐️ 7.0/10

A developer published a GitHub project called zigzag, a custom app for controlling a $300 embroidery machine that otherwise required a subscription. The Hacker News post links to the author&\#x27;s X thread rather than detailed technical documentation, so the supplied material does not specify the machine model, the subscription terms, or how the app communicates with the hardware. The project is presented as a working replacement for vendor software, but its scope and compatibility are not independently verified here.

hackernews · simpsoka · Nov 12, 17:02 · [Discussion](https://news.ycombinator.com/item?id=50470488)

**「Background」** The project joins a broader effort to keep older embroidery machines usable after vendor software and media become scarce. A December 2024 write-up documented reverse engineering the Brother PE-150, whose out-of-box workflow depended on CompactFlash cards and proprietary software that cost more than the machine itself. The new app targets a different machine and replaces a subscription requirement rather than obsolete media.

**「Impact」** Owners of the affected machine may be able to keep using it without paying for vendor software, though the supplied material does not confirm which models or firmware versions the app supports. Anyone relying on it should verify compatibility with their own machine before assuming the subscription can be dropped.

**「Community Discussion」** Commenters framed the project as part of a broader effort to revive abandoned or subscription-locked hardware: one described a friend&\#x27;s replacement motherboard for the Brother PE-150 that adds USB control, and another pointed to InkStitch, an Inkscape plugin for exporting SVG designs to embroidery file formats. One commenter speculated that an LLM did much of the implementation work, which is an assumption rather than a confirmed fact.

<details><summary>References</summary>
<ul>
<li><a href="https://owentrueblood.com/blog/2024/12/10/reverse-engineering-the-brother-pe-150-embroidery-machine/">Reverse Engineering the Brother PE-150 Embroidery Machine</a></li>

</ul>
</details>

**Tags**: `#reverse-engineering`, `#hardware-hacking`, `#subscription-lock-in`, `#open-source`, `#embedded-systems`

---

<a id="item-tech-news-12"></a>
### [Fireworks AI Breach Exposes Notion Users&\#x27; Chat Transcripts](https://techcrunch.com/2026/11/12/cyberattack-on-fireworks-ai-allowed-hackers-to-access-notion-customers-chat-transcripts/) ⭐️ 7.0/10

A cyberattack on AI inference provider Fireworks AI reportedly allowed hackers to access chat transcripts belonging to Notion customers, according to TechCrunch. The report describes this as Fireworks&\#x27; second data breach in as many months. The available account does not specify the number of affected users, the attack vector, or whether the exposure has been contained, so the full scope remains unconfirmed.

rss · TechCrunch AI · Nov 12, 15:02

**「Background」** Fireworks AI is an AI inference provider that Notion used to power its Notion AI &quot;Insights&quot; feature. According to TechCrunch, Notion said on November 3 that it disconnected its systems from Fireworks, deleted the data stored there, and stopped all connectivity between the two, and it confirmed this week that hackers took chat transcripts of Notion AI customers who used Insights. The report describes this as Fireworks&\#x27; second data breach in as many months, though the supplied material gives no details on the earlier incident or on the root cause of this one.

**「Why It Matters」** The incident points to third-party AI inference providers as a path to customer data held by downstream applications, meaning Notion users&\#x27; exposure stems from a vendor relationship rather than Notion&\#x27;s own systems. Organizations routing chat data through external model providers should verify what transcript retention and access controls those providers apply.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/12/cyberattack-on-fireworks-ai-allowed-hackers-to-access-notion-customers-chat-transcripts/">Cyberattack on Fireworks AI allowed hackers to access Notion ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#data breach`, `#AI infrastructure`, `#privacy`

---

<a id="item-tech-news-13"></a>
### [Hackers Used 4,837 Compromised GitHub Accounts to Steal Cloud Credentials](https://www.bleepingcomputer.com/news/security/hackers-compromise-4-800-github-accounts-to-steal-cloud-credentials/) ⭐️ 7.0/10

A campaign tracked as &quot;wfx-loot&quot; used 4,837 compromised GitHub accounts to probe 61,764 repositories, open pull requests, and push malware designed to steal secrets, according to BleepingComputer. The reported goal was harvesting cloud credentials. The source describes the activity as an ongoing campaign rather than a patched or resolved incident, and it does not specify which cloud providers, credential types, or organizations were affected.

rss · BleepingComputer · Nov 12, 22:25

**「Prior context」** The wfx-loot campaign follows earlier attacks that hijacked developer accounts to inject secret-stealing workflows into GitHub repositories. The Cloud Security Alliance research note identifies GhostAction, first discovered in September 2025 and resurfacing in waves in August and October 2026, as the campaign&\#x27;s most direct predecessor.

**「Impact」** Because the reported vector is malicious pull requests and pushed code, maintainers of repositories targeted by these accounts should treat unexpected contributions as untrusted and review them before merging. Any credentials exposed to code from those pull requests should be rotated, since the stated objective was cloud-credential theft.

<details><summary>References</summary>
<ul>
<li><a href="https://labs.cloudsecurityalliance.org/research/csa-research-note-wfx-github-ci-secret-stealer-20261112-csa/">The wfx Campaign: Hijacked GitHub Accounts Harvest CI Secrets</a></li>

</ul>
</details>

**Tags**: `#security`, `#github`, `#supply-chain`, `#cloud-credentials`, `#malware`

---

<a id="item-tech-news-14"></a>
### [N-able N-central zero-day &quot;4EverAble2Shell&quot; exploited to mine crypto](https://www.bleepingcomputer.com/news/security/new-n-able-4everable2shell-zero-day-exploited-hours-after-poc-released/) ⭐️ 7.0/10

A newly disclosed zero-day in N-able N-central, dubbed &quot;4EverAble2Shell,&quot; is being actively exploited to compromise servers and deploy cryptocurrency miners. Researchers report at least 21 affected systems, including 19 running N-able&\#x27;s latest security update, indicating the patch does not block the attacks. The vulnerability was exploited within hours of a proof-of-concept being released. The source does not specify affected N-central versions or a fix timeline.

rss · BleepingComputer · Nov 12, 19:51

**「Background」** N-able N-central is a remote monitoring and management platform that IT service providers use to administer customer endpoints and servers, which makes a server-side flaw in it a potential path to many downstream networks. According to a researcher cited in coverage of the exploit, 4EverAble2Shell can let an unauthenticated attacker run commands with root privileges on an N-central server, but the attack requires the Legacy API to be enabled.

**「Impact」** Because 19 of the 21 reported victims were on the latest security update, administrators running current N-central builds should not assume patching alone protects them and should monitor for cryptomining activity and signs of compromise.

<details><summary>References</summary>
<ul>
<li><a href="https://dzen.ru/a/avYbekQwLEe5MMt5">Эксплойт 4 EverAble 2 Shell может позволить... | Дзен | Дзен | Статьи</a></li>

</ul>
</details>

**Tags**: `#security`, `#zero-day`, `#vulnerability`, `#N-able N-central`, `#cryptomining`

---

<a id="item-tech-news-15"></a>
### [Researcher Releases Windows SignDrop Zero-Day Exploit for SYSTEM Access](https://www.bleepingcomputer.com/news/security/new-windows-signdrop-zero-day-gives-hackers-system-privileges/) ⭐️ 7.0/10

Security researcher Abdelhamid Naceri, also known as Nightmare Eclipse, has released a Windows zero-day exploit that can grant attackers SYSTEM privileges, according to a brief BleepingComputer report. The supplied account does not specify the vulnerability mechanism, affected Windows versions, or any available mitigation, so the exploit&\#x27;s practical reach and novelty remain unverified. The disclosure is a researcher-published proof of concept rather than a confirmed in-the-wild attack or a vendor patch.

rss · BleepingComputer · Nov 12, 16:04

**「Background」** The exploit was posted as a proof-of-concept on GitHub on November 10, 2026, by researcher Abdelhamid Naceri, who also uses the handles Nightmare Eclipse and MSNightmare. Reporting on the release describes SignDrop as abusing CLFS file-creation logic, with Naceri quoted as saying Microsoft&\#x27;s implementation is &quot;done properly&quot; but that the underlying logic allows abuse. The supplied source material does not specify which Windows versions are affected or whether a patch or mitigation exists.

**「Impact」** Because the exploit requires only standard user access and no Microsoft fix is available, affected organizations should treat local privilege escalation to SYSTEM as a live risk until a patch ships. External coverage reports that the flaw lies in Windows CLFS log authentication and that the exploit could potentially be used to disable antivirus and EDR tooling, so defenders may want to monitor for CLFS abuse rather than rely on endpoint protection alone.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/windows-signdrop-zero-day-exploit/">Windows SignDrop 0-Day Exploit Lets Attackers Gain SYSTEM ...</a></li>
<li><a href="https://osintsights.com/windows-zero-day-exploit-signdrop-grants-hackers-system-privileges">Windows Zero-Day Exploit SignDrop Grants Hackers SYSTEM ...</a></li>
<li><a href="https://threatdefence.com/article/windows-signdrop-clfs-zero-day-privilege-escalation-hunting">Windows SignDrop CLFS Zero-Day: Mitigation and Hunting</a></li>
<li><a href="https://thehackernews.com/2026/11/new-signdrop-zero-day-exploit-turns.html">New SignDrop Zero-Day Exploit Turns Windows CLFS Security ...</a></li>
<li><a href="https://dailysecurityreview.com/resources/signdrop-windows-clfs-zero-day-exploit-published-no-patch/">SignDrop Windows CLFS Zero-Day Exploit Published, No Patch</a></li>

</ul>
</details>

**Tags**: `#windows`, `#zero-day`, `#privilege-escalation`, `#security`, `#exploit`

---

<a id="item-tech-news-16"></a>
### [Independent audit finds TRIBE v2 lacks retinotopy and tonotopy but shows MT+ motion selectivity](https://www.reddit.com/r/MachineLearning/comments/1xuillf/does_metas_brainresponse_model_tribe_v2_actually/) ⭐️ 7.0/10

A Reddit author reports independently probing Meta&\#x27;s TRIBE v2 fMRI-prediction model with classic topographic mapping stimuli and finding no retinotopic map \(d=0.05, not significant\) and no tonotopic map \(ρ=-0.07, not significant, even with loudness controlled\). Motion selectivity was strong and localized to MT+ \(d=4.31, 52x enrichment over chance\). The author also reports that an apparent eccentricity effect became significant and &quot;correct&quot; only under three stimulus-geometry controls, which they interpret as an image-statistics confound rather than a positional code. The post is a self-funded solo project with linked code and paper, not peer-reviewed, and the claims are unverified.

reddit · r/MachineLearning · /u/Own\_Tank1283 · Nov 12, 17:16

**「Background」** TRIBE v2 is Meta&\#x27;s open-sourced multimodal foundation model that predicts high-resolution human fMRI activity from video, audio, or language, as external coverage of the release describes. The Reddit author&\#x27;s audit targets a gap in that model&\#x27;s published evaluation: the paper reportedly did not test whether the model reproduces classic topographic maps, and its methods section states that video features are spatially averaged before prediction, which would remove the position information such maps depend on.

**「Impact」** The author notes that TRIBE v2&\#x27;s own paper never tested these topographic maps and that its methods section says video features are spatially averaged before prediction, which the author argues should destroy position information. Readers evaluating TRIBE v2 for spatially resolved predictions should treat its position-related outputs as unvalidated until the audit&\#x27;s code and results are independently reproduced.

<details><summary>References</summary>
<ul>
<li><a href="https://www.marketingembeddings.com/marketing-embeddings/from-attention-to-neural-prediction">From Attention to Neural Prediction — Marketing Embeddings</a></li>
<li><a href="https://www.builderhustle.com/p/meta-tribe-v2-iphone-fold-ai-gym-hacker-youtube-partner">Meta TRIBE v 2 , iPhone Fold Rumors, AI Gym Hacker &amp; YouTube...</a></li>

</ul>
</details>

**Tags**: `#neuroscience`, `#fMRI`, `#model-evaluation`, `#representation-learning`, `#reproducibility`

---

<a id="item-tech-news-17"></a>
### [US Commerce Department to finalize rule closing remote AI chip access for Chinese firms](https://www.theinformation.com/articles/commerce-department-finalizing-long-awaited-ai-remote-access-rule) ⭐️ 7.0/10

The US Commerce Department is finalizing a rule that would block Chinese AI companies from remotely using advanced AI chips through overseas data centers, with publication possible as early as this month, according to The Information. The controls would extend existing semiconductor export restrictions to Malaysia, Singapore, Thailand and four other countries, aiming to close remote-access and chip-smuggling gaps. The department is still consulting other government agencies before finalizing the text, so the rule has not yet been issued. The White House had previously asked Congress to legislate that the Commerce Department write this rule, and Nvidia reportedly lobbied against closing the remote-access gap, arguing US AI infrastructure needs to win globally.

telegram · zaihuapd · Nov 12, 03:42

**「Background」** The reported rule targets a gap left by earlier US policy: according to Tech Times, the Commerce Department&\#x27;s 2026 decision to rescind the Biden-era &quot;know your customer&quot; provision left data centers in Thailand, Singapore, Malaysia and Japan able to provision Nvidia GPU access to Chinese AI companies without verifying the ultimate user. The new rule would extend existing Bureau of Industry and Security semiconductor controls to seven additional countries, including Malaysia, Singapore and Thailand, and reportedly add them to a license list requiring end-user reporting.

**「Impact」** If finalized as described, the rule would extend licensing requirements beyond physical chip shipments to remote compute access, affecting Chinese AI developers that rely on data centers in the seven named Southeast Asian countries and the operators of those facilities. Because the rule is not yet published, its exact scope, effective date and any exemptions remain unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techtimes.com/articles/325957/20260829/commerce-drafts-ai-chip-rule-loophole-it-created-rescinding-biden-know-your-customer.htm">Commerce Drafts AI Chip Rule for Loophole It Created by ...</a></li>
<li><a href="https://biz.chosun.com/en/en-international/2026/11/12/M2ICNVHJPVCFLJDLAGG5IP4VDE/">US to widen AI chip export controls to seven nations, curb ...</a></li>

</ul>
</details>

**Tags**: `#export controls`, `#AI chips`, `#semiconductor policy`, `#data centers`, `#US-China tech`

---

<a id="item-tech-news-18"></a>
### [Apple details Secure Exclaves for audio/video privacy](https://security.apple.com/blog/secure-exclaves/) ⭐️ 7.0/10

Apple published a blog post on November 12 detailing Secure Exclaves, an architecture that processes audio and video in an isolated secure environment so the main system and apps receive only necessary recognition results rather than raw data. Apple says the technology is already used in HomeView face and sound recognition and in the iPhone 18 Pro privacy indicator. On the iPhone 18 Pro, dedicated hardware verifies the microphone indicator dot&\#x27;s color, brightness, and visibility before audio is allowed into the main system, and Apple requires the dot to stay displayed throughout relevant Siri audio sessions for at least three seconds to prevent it from being obscured or spoofed. The item is a brief secondary summary of Apple&\#x27;s post, so the iPhone 18 Pro specifics could not be independently verified from the supplied content.

telegram · zaihuapd · Nov 12, 09:13

**「Background」** Apple&\#x27;s Secure Exclaves build on a kernel-level compartmentalization effort reported earlier, in which sensitive services run in a separate Secure Kernel so that compromising one service does not grant access to the entire kernel address space. Unlike the older Secure Enclave, Apple has argued the exclave design is robust enough to secure a range of features, including HomeView face and sound recognition. The new blog post details how that architecture is now applied to audio/video processing and to hardware-verified recording indicators.

**「Impact」** For developers, the design means apps in ambient-sensing modes get recognition outputs instead of raw audio or video, and audio capture on the iPhone 18 Pro is gated by a hardware check of the indicator. The stated three-second minimum display requirement for Siri audio sessions is a condition app and Siri integration behavior would need to respect.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theregister.com/security/2025/03/08/how-apple-rearranged-its-xnu-kernel-with-security-exclaves/1352740">How Apple rearranged its XNU kernel with security exclaves</a></li>
<li><a href="https://www.wired.com/story/apples-homeview-tries-face-authentication-without-faceid/">Apple ’s HomeView Tries Face Authentication Without FaceID | WIRED</a></li>

</ul>
</details>

**Tags**: `#apple`, `#security-architecture`, `#privacy`, `#hardware-security`, `#audio-video`

---

<a id="item-tech-news-19"></a>
### [Telegram Widgets 被指存在沙箱逃逸远程代码执行漏洞](https://x.com/telegram/status/2120502876728680765?a=qTsR6dLMSgt3RHbYYO0&amp;amp;s=46) ⭐️ 7.0/10

一则社交媒体安全提醒称，Telegram Widgets 的客户端沙箱存在漏洞，可被用于远程代码执行。Telegram Widgets 是 Telegram 在 2026 年 11 月 9 日发布的 Bot API 10.4 中引入的功能，允许机器人在聊天消息内嵌入 HTML、CSS 和 JavaScript 以构建交互式界面。该提醒称 Telegram 官方表示已修复，但发帖者称群友在部分设备的最新版本上测试后仍可利用该漏洞。该提醒建议用户不要点击来路不明的机器人，并暂时不要升级到支持 Telegram Widgets 的版本；这些说法来自一条简短帖子，未提供受影响版本、漏洞细节或独立验证。

telegram · zaihuapd · Nov 13, 01:02

**「Background」** Telegram introduced Widgets in Bot API 10.4 on November 9, 2026, letting bots embed self-contained HTML, CSS, and JavaScript documents of up to 4 KB compressed and 32 KB uncompressed directly in chat messages. Telegram&\#x27;s widget-sandbox project describes the runtime as a no-network sandbox for this inline HTML. The advisory&\#x27;s claim of a sandbox escape therefore concerns the isolation layer that is supposed to contain that bot-supplied JavaScript.

**「影响与建议」** 如果该漏洞确实存在，风险集中在运行 Widget 内 JavaScript 的 Telegram 客户端：恶意机器人可在聊天消息中投递利用代码，因此用户应避免与不熟悉的机器人交互。发帖者称官方修复在部分设备上不完整，这意味着仅升级客户端未必能消除风险，在获得更明确的受影响版本信息前，用户需自行权衡是否启用或升级支持 Widgets 的版本。

<details><summary>References</summary>
<ul>
<li><a href="https://dev.to/marylyn_roundy_e32b126c99/telegram-widgets-bot-api-104-interactive-cards-inside-chat-messages-with-a-working-example-46j9">Telegram widgets (Bot API 10.4): interactive cards inside ...</a></li>
<li><a href="https://core.telegram.org/bots/api">Telegram Bot API</a></li>
<li><a href="https://github.com/TelegramMessenger/widget-sandbox">GitHub - TelegramMessenger/ widget - sandbox · GitHub</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#telegram`, `#sandbox`, `#javascript`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China Approves Eli Lilly&\#x27;s Oral Weight-Loss Drug, a First for the Country](https://www.reuters.com/business/healthcare-pharmaceuticals/china-approves-eli-lillys-weight-loss-pill-orforglipron-2026-11-12/) ⭐️ 7.0/10

China&\#x27;s National Medical Products Administration approved Eli Lilly&\#x27;s once-daily oral GLP-1 weight-loss drug orforglipron \(brand name Muyouda\) on November 12 as a Class 1 new drug, making it the country&\#x27;s first approved oral GLP-1 treatment for adults who are obese or overweight with at least one weight-related condition. Pricing and launch timing were not disclosed, and the drug&\#x27;s type 2 diabetes indication is still under review.

telegram · zaihuapd · Nov 12, 10:09

**「Background」** Orforglipron is Eli Lilly&\#x27;s once-daily oral GLP-1 drug; in company-reported Phase 3 trials it produced average weight loss of up to about 12% \(roughly 27 pounds\), according to Medscape and Healthline. China&\#x27;s obesity-drug market is already crowded with weekly injectable GLP-1 treatments from Novo Nordisk, Pfizer and Innovent, and analysts expect intensifying price competition as more products and generics arrive.

**「Impact」** The approval gives Chinese patients a pill alternative to the weekly injections sold by Novo Nordisk, Pfizer and Innovent, though how much market share it takes will depend on the undisclosed price and launch date.

<details><summary>References</summary>
<ul>
<li><a href="https://www.healthline.com/health-news/orforglipron-eli-lilly-weight-loss-pill">Lilly ’s New Oral GLP - 1 Orforglipron Led to 12% Weight Loss in Trials</a></li>
<li><a href="https://www.linkedin.com/pulse/attain-1-orforglipron-achieves-up-12-weight-loss-phase-3-obesity-inrme">ATTAIN- 1 : Orforglipron Achieves Up to 12% Weight Loss in Phase...</a></li>
<li><a href="https://www.medscape.com/viewarticle/top-line-results-positive-lillys-oral-glp-1-orforglipron-2025a100098n">Topline Results Positive for Lilly ’s Oral Orforglipron</a></li>
<li><a href="https://global.chinadaily.com.cn/a/202604/02/WS69ce1a08a310d6866eb416e6.html">Price war looms in China&#x27;s booming weight-loss drug market</a></li>
<li><a href="https://www.lek.com/sites/default/files/insights/pdf-attachments/winning-smart-glp-china.pdf">The Race is On: Winning Smart in the Intensifying GLP-1 ...</a></li>

</ul>
</details>

**Tags**: `#pharmaceuticals`, `#regulatory approval`, `#GLP-1 obesity drugs`, `#Eli Lilly`, `#China healthcare`

---