---
layout: default
title: "Horizon Summary: 2026-11-15 (EN)"
date: 2026-11-15
lang: en
---

> From 52 items, 11 important content pieces were selected

---

**Technology News**
1. [SpaceX catches Starship booster to close out Flight 15](#item-tech-news-1) ⭐️ 8.0/10
2. [Lovable apps exposed passport data and 200K+ private messages](#item-tech-news-2) ⭐️ 8.0/10
3. [Asian Governments React to Nvidia CEO Jensen Huang&\#x27;s Exit](#item-tech-news-3) ⭐️ 8.0/10
4. [Show HN: DeepSeek V3 inference reimplemented in ~200 lines of JAX](#item-tech-news-4) ⭐️ 7.0/10
5. [Project Zero to shorten vulnerability disclosure to 60 then 30 days](#item-tech-news-5) ⭐️ 7.0/10
6. [PyPI&\#x27;s Redesigned Project Pages Now Show Security and Provenance Signals](#item-tech-news-6) ⭐️ 7.0/10
7. [Cursor Confirms Breach Behind Malicious Claude Code Extension](#item-tech-news-7) ⭐️ 7.0/10
8. [Google designer runs Windows 11 24H2 on foldable iPhone via Gemini-assisted project](#item-tech-news-8) ⭐️ 7.0/10
9. [Cloudflare open-sources Kitesurf, a stateless browser for AI agents](#item-tech-news-9) ⭐️ 7.0/10
10. [Tesla Cybercab terms require $299 monthly subscription to operate](#item-tech-news-10) ⭐️ 7.0/10

**Financial News**
1. [Anthropic IPO Reportedly Bars Mainland China and Hong Kong Investors](#item-finance-news-1) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [SpaceX catches Starship booster to close out Flight 15](https://www.spacex.com/launches/starship-flight-15) ⭐️ 8.0/10

SpaceX caught the Starship booster at the end of Flight 15, according to the company&\#x27;s launch page and a post on X. The source material is limited to those links and a short video, so it does not specify the catch mechanism, booster identity, flight profile, or whether the ship itself was recovered. The company presents the catch as a step toward fully reusable launch vehicles; no independent measurement or cost figure accompanies the claim.

hackernews · ls612 · Nov 14, 21:22 · [Discussion](https://news.ycombinator.com/item?id=50500963)

**「Background」** SpaceX&\#x27;s Flight 15 launched from Starbase, Texas, on November 13, 2026, but the planned tower catch of the Super Heavy booster was waved off, and the booster instead splashed down in the Gulf of Mexico; SpaceX later said it was investigating a guidance issue behind the aborted chopsticks landing. Flight 15 was also described as the first attempt to catch the Ship upper stage with the chopsticks, which is the catch the source reports as successful.

**「Why it matters」** A successful booster catch is the prerequisite for reusing the booster rather than expending it, which is the cost lever SpaceX is pursuing. Commenters note that the next tests would be catching both stages and re-flying the same vehicles, and that the heat shield&\#x27;s performance remains the open question for ship reuse.

**「Community discussion」** Commenters framed Starship as a corrected Space Shuttle: a reusable booster without solid rocket boosters and a stack mounted on top rather than beside the orbiter. Others cautioned that the payoff depends on the heat shield holding up and on re-flying the same ships, and one commenter said it is still unclear what final mass fraction to orbit will be, arguing that a fully reusable vehicle beats a partially reusable one such as Falcon 9.

<details><summary>References</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=RHY66XujZ90">Blastoff! SpaceX Starship launches to orbit on Flight 15 , booster ...</a></li>
<li><a href="https://www.space.com/space-exploration/launches-spacecraft/spacex-says-starship-flight-15-booster-aborted-chopsticks-landing-catch-after-launch-due-to-guidance-issue-video">SpaceX still investigating why Starship Flight 15 booster ... | Space</a></li>
<li><a href="https://www.zerohedge.com/technology/watch-live-spacex-targets-historic-starship-booster-double-chopsticks-catch">Elon Musk&#x27;s &#x27;Mechazilla&#x27; Catches Starship Rocket In... | ZeroHedg...</a></li>

</ul>
</details>

**Tags**: `#spaceflight`, `#reusable-rockets`, `#spacex`, `#engineering-milestone`

---

<a id="item-tech-news-2"></a>
### [Lovable apps exposed passport data and 200K+ private messages](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

Security researchers at Crissy Field reported that apps built with Lovable exposed sensitive user data, including passport details and more than 200,000 private messages, because of insufficient Row-Level Security. Lovable&\#x27;s Head of Security, Igor Andri, said in comments that insufficient RLS was the root cause and that the company scans every app automatically before publishing, offers a deeper SAST scan free to all users, and lets users apply fixes, enable auto-fix, or block publishing when findings appear. The report describes a specific incident rather than an independently measured audit of Lovable&\#x27;s scanning, and the vendor&\#x27;s account of its safeguards is a company claim.

hackernews · armcat · Nov 14, 17:43 · [Discussion](https://news.ycombinator.com/item?id=50499017)

**「Background」** Supabase&\#x27;s Data API auto-exposes tables in the public schema, and Row-Level Security policies determine which rows clients can read; misconfigured or missing policies leave data open to anyone with the project&\#x27;s public API key. Supabase announced a change effective October 30, 2026, under which new tables in existing projects are no longer auto-granted to the Data API, but external reports say existing tables keep their current grants and RLS behavior, so previously open tables stay open.

**「Why it matters」** The exposure points to a practical risk for people building on AI code generators backed by Supabase: if RLS policies are missing or misconfigured, data can be reachable through ordinary browser network calls without sophisticated hacking, as commenters noted. Builders should verify RLS on every table and test access with unauthenticated and low-privilege requests before publishing.

**「Community debate」** Commenters split on responsibility: one argued Supabase bears much of the blame because its permissive defaults were a deliberate onboarding tradeoff, and said reports suggest existing projects may still use those defaults despite a claimed October 30 fix. Others said AI-generated apps are especially exposed because they are numerous, easy to probe, and opaque to end users.

<details><summary>References</summary>
<ul>
<li><a href="https://www.getleakpatrol.com/supabase-october-30-change.html">Supabase&#x27;s October 30 change: what it fixes for your app&#x27;s ...</a></li>
<li><a href="https://dev.to/fixloopdev/supabase-oct-30-why-new-tables-get-42501-and-how-to-fix-grants-rls-2i8k">Supabase Oct 30: why new tables get 42501 (and how to fix ...</a></li>
<li><a href="https://dev.to/dave_thomas_18311ddb9c409/supabases-oct-30-change-what-breaks-what-doesnt-and-the-quick-fix-to-avoid-bg4">Supabase&#x27;s Oct 30 change: what breaks, what doesn&#x27;t, and the ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#AI code generation`, `#Supabase`, `#row-level security`, `#data exposure`

---

<a id="item-tech-news-3"></a>
### [Asian Governments React to Nvidia CEO Jensen Huang&\#x27;s Exit](https://techcrunch.com/2026/11/14/asian-governments-react-to-nvidia-ceo-jensen-huangs-exit/) ⭐️ 8.0/10

Asian governments are reportedly responding to the exit of Nvidia CEO Jensen Huang, according to TechCrunch. Some governments moved to confirm chip supply commitments, while others said they were monitoring the impact on local projects or addressing ongoing investigations. The report does not name the governments involved, describe the circumstances of Huang&\#x27;s departure, or specify the commitments and investigations in question.

rss · TechCrunch AI · Nov 14, 16:34

**「Background」** Jensen Huang resigned as Nvidia&\#x27;s chief executive two days before this report, after disclosures of extramarital affairs, including one involving a suspected Chinese spy, according to Reuters and The Guardian. He was replaced on an interim basis, leaving the chipmaker&\#x27;s leadership unsettled as governments assess their exposure.

**「Impact」** Governments that moved to confirm chip supply commitments signal they are treating Nvidia&\#x27;s supply chain as a continuity risk tied to Huang&\#x27;s departure, though the source does not name which governments or what commitments were made. The reported monitoring of local projects and ongoing investigations means organizations relying on Nvidia hardware in those markets face uncertainty about project timelines and regulatory scrutiny until details are confirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/12/nvidia-ceo-jensen-huang-resigns">Jensen Huang resigns as Nvidia CEO after alleged affairs</a></li>
<li><a href="https://www.reuters.com/business/retail-consumer/nvidia-ceo-jensen-huang-step-down-big-blow-ai-boom-2026-11-12/">Nvidia CEO Jensen Huang resigns in blow to AI boom he helped ...</a></li>
<li><a href="https://techcrunch.com/2026/11/14/asian-governments-react-to-nvidia-ceo-jensen-huangs-exit/">Asian governments react to Nvidia CEO Jensen Huang ’s exit</a></li>

</ul>
</details>

**Tags**: `#nvidia`, `#semiconductors`, `#ai-hardware`, `#tech-industry`, `#government-policy`

---

<a id="item-tech-news-4"></a>
### [Show HN: DeepSeek V3 inference reimplemented in ~200 lines of JAX](https://github.com/Vaibhaav-Tiwari/deepseek-v3-jax) ⭐️ 7.0/10

A Show HN project by VaibhaavTiwari reimplements DeepSeek V3 inference in roughly 200 lines of pure JAX, published as a GitHub repository. The item provides little technical detail beyond the link, so the implementation&\#x27;s completeness and fidelity to the original model are not independently verified. Commenters report it running end-to-end on AMD hardware via ROCm, which the author&\#x27;s framing presents as a working capability rather than a benchmarked result.

hackernews · VaibhaavTiwari · Nov 14, 15:04 · [Discussion](https://news.ycombinator.com/item?id=50497589)

**「Background」** DeepSeek V3 is an open-weight model with 684B parameters, released by DeepSeek under a free and open-source software license since January 2025. The Show HN project reimplements inference for that model from scratch in JAX rather than using DeepSeek&\#x27;s own code, which is why commenters treat it as a learning artifact.

**「Practical impact」** For developers without CUDA GPUs, the reported ROCm path is the concrete draw: one commenter says it was the first project to run end-to-end on an RX 7600 XT 16GB under Fedora, after setting HSA\_OVERRIDE\_GFX\_VERSION=11.0.0 because JAX&\#x27;s plugin rejects the gfx1102 target. That suggests a usable starting point for local JAX experimentation on that card, though the setup requires environment-variable workarounds and the claim comes from a single user report.

**「Community reaction」** Commenters largely framed the project as a learning resource, with several saying they plan to recreate it to build intuition about inference. One user asked for a roadmap for developers comfortable with Java and Python but new to model internals; no such roadmap was supplied in the comments.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V3">deepseek -ai/ DeepSeek - V 3 · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#jax`, `#deepseek`, `#model-inference`, `#open-source`, `#rocm`

---

<a id="item-tech-news-5"></a>
### [Project Zero to shorten vulnerability disclosure to 60 then 30 days](https://projectzero.google/2026/11/disclosure-policy.html) ⭐️ 7.0/10

Google Project Zero announced a staged tightening of its vulnerability disclosure policy: it keeps a &quot;Full 90&quot; window, disclosing bugs 90 days after reporting them to the vendor, then moves to &quot;Full 60&quot; on February 2, 2027, and to &quot;Full 30&quot; on January 3, 2028. The change is an announced plan rather than a shipped capability, and the supplied material provides only the headline and comment excerpts, with no detail on exceptions, grace periods, or how the policy interacts with vendor patch deadlines.

hackernews · hacb · Nov 14, 11:13 · [Discussion](https://news.ycombinator.com/item?id=50496051)

**「Prior disclosure policy」** Since 2021, Project Zero has operated under a &quot;90 + 30&quot; policy: vendors got up to 90 days to remediate a vulnerability, plus an extra 30 days of &quot;soak time&quot; for patch rollout, according to the project&\#x27;s own policy post. The new schedule replaces that grace period with a single fixed window that shrinks in stages, and the project attributes the change to AI-assisted vulnerability discovery and exploitation altering the threat landscape.

**「Impact on maintainers」** The shorter windows put pressure on vendors and open-source projects to patch within 30 days by 2028; one commenter argued Ubuntu would need far more time than that, suggesting slower-moving distributions may struggle to meet the schedule.

**「Community debate」** Commenters debated whether the compressed timeline is feasible for vendors and open-source projects, with one arguing for immediate release on the grounds that nothing else compels a reported company to fix a bug. Another raised a separate concern that bug-hunting companies should give vendors comparable access to the products used to find flaws, warning that disclosure pressure could otherwise be used to push adoption of specific AI tools.

<details><summary>References</summary>
<ul>
<li><a href="https://projectzero.google/2026/11/disclosure-policy.html">Policy and Disclosure: 2026 Edition - Project Zero</a></li>
<li><a href="https://projectzero.google/vulnerability-disclosure-policy.html">Vulnerability Disclosure Policy - Project Zero</a></li>

</ul>
</details>

**Tags**: `#vulnerability-disclosure`, `#security`, `#open-source`, `#google`, `#policy`

---

<a id="item-tech-news-6"></a>
### [PyPI&\#x27;s Redesigned Project Pages Now Show Security and Provenance Signals](https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/) ⭐️ 7.0/10

PyPI has made its redesigned project pages live, with the files section now surfacing provenance information alongside package downloads. Community examples show the difference: the dlt project&\#x27;s files page carries no provenance, while datasette&\#x27;s does. The change is a UI and trust-signal update rather than a new signing mechanism, and commenters note that trusted publishing still lacks support for reusable workflows.

hackernews · rbanffy · Nov 14, 15:40 · [Discussion](https://news.ycombinator.com/item?id=50497892)

**「Background」** PyPI&\#x27;s provenance signals build on Trusted Publishing, which PyPI designed and implemented with Trail of Bits as a more secure way to upload packages without long-lived API tokens, and on Sigstore-based attestations that record how and where a package was built. The new pages surface those existing attestation records rather than introducing a new signing mechanism.

**「Impact」** Developers checking a package&\#x27;s files page can now see whether a release carries provenance, giving them a visible signal when deciding whether to install or audit a dependency. Commenters caution that this indicates whether a formerly benign project&\#x27;s PyPI entry was tampered with, not whether the project itself is malicious.

**「Community Discussion」** Commenters debated whether tying trust to centralized cloud identity providers promotes lock-in, with one calling the approach &quot;a bit anti-pythonic.&quot; Others welcomed keyless, short-lived signatures and hoped third-party CI/CD services would add secure OIDC handling so developers aren&\#x27;t pushed toward GitHub Actions or GitLab, and one asked for trusted publishing to support reusable workflows.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.trailofbits.com/2024/11/14/attestations-a-new-generation-of-signatures-on-pypi/">Attestations : A new generation of signatures on PyPI - The Trail of...</a></li>
<li><a href="https://www.pyblog.in/programming/python/pypi-security-in-2026-trusted-publishing-sigstore-and-whats-next/">PyPI Security 2026: Trusted Publishing and Sigstore Guide</a></li>

</ul>
</details>

**Tags**: `#supply-chain-security`, `#pypi`, `#package-management`, `#provenance`, `#open-source`

---

<a id="item-tech-news-7"></a>
### [Cursor Confirms Breach Behind Malicious Claude Code Extension](https://www.bleepingcomputer.com/news/security/cursor-confirms-security-breach-led-to-malicious-claude-code-extension/) ⭐️ 7.0/10

Cursor confirmed a security breach in which attackers used credentials stolen from AI infrastructure provider Fireworks AI to distribute a malicious Claude Code extension through Cursor&\#x27;s marketplace. The supplied report does not specify the attack vector, the extension&\#x27;s behavior, how long it was available, or remediation steps. The confirmation establishes that the marketplace listing was tied to stolen third-party credentials, but the technical details remain undisclosed in the available excerpt.

rss · BleepingComputer · Nov 14, 17:27

**「Background」** Cursor&\#x27;s incident update, published November 13, 2026, traced the breach to a Cursor-issued access key that Fireworks AI had exposed. According to reporting on that update, the attacker used the key to copy historical coding-agent traces and credentials, then reached select software tools used by Cursor to distribute malicious Claude Code extension builds.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/cursor-data-breach/">Cursor Reveals How a Leaked Fireworks AI Key Led to a ...</a></li>
<li><a href="https://www.unite.ai/cursor-traces-breach-to-access-key-exposed-by-fireworks-ai/">Cursor Traces Breach to Access Key Exposed by Fireworks AI</a></li>

</ul>
</details>

**Tags**: `#security`, `#supply-chain`, `#AI coding tools`, `#Cursor`, `#Claude Code`

---

<a id="item-tech-news-8"></a>
### [Google designer runs Windows 11 24H2 on foldable iPhone via Gemini-assisted project](https://www.windowslatest.com/2026/11/14/windows-11-can-run-on-apples-foldable-iphone-and-googles-ai-boss-proved-it-using-gemini-years-after-microsoft-gave-up-on-windows-phones/) ⭐️ 7.0/10

Ammaar Reshi, a product design lead for Google AI Studio, reportedly used Gemini 4 Carbon to get Windows 11 24H2 running locally on Apple&\#x27;s foldable iPhone, which the source calls the &quot;iPhone Duo,&quot; and published a video of the demonstration. The work relies on an open-source project called WindowsiOS, which requires no jailbreak and runs ARM64 code through JIT-based translation, with support for some legacy applications via Microsoft&\#x27;s Prism. The image is about 12 GB and requires an Apple Silicon Mac and development tools. These details come from a single report and the demonstration has not been independently verified.

telegram · zaihuapd · Nov 14, 06:52

**「Background」** Windows on ARM normally requires native ARM64 builds of Windows and drivers written for the specific device. Projects that run Windows on non-Windows hardware instead rely on translation layers, and Apple&\#x27;s iPhone hardware has no official Windows support. The source describes WindowsiOS as an open-source, JIT-based ARM64 translation project that runs without jailbreaking and can use Microsoft&\#x27;s Prism to run some legacy apps; the reported 12 GB image requires an Apple Silicon Mac and development tools to prepare.

**「Practical limits」** Because the setup needs an Apple Silicon Mac and developer tooling, this is a proof-of-concept rather than something ordinary iPhone owners can install. Anyone attempting to reproduce it should expect a roughly 12 GB image and JIT-based translation, which may limit compatibility with traditional Windows applications.

**Tags**: `#Windows on ARM`, `#emulation`, `#Apple hardware`, `#Gemini`, `#open source`

---

<a id="item-tech-news-9"></a>
### [Cloudflare open-sources Kitesurf, a stateless browser for AI agents](https://www.phoronix.com/news/Cloudflare-Kitesurf-Open-Source) ⭐️ 7.0/10

Cloudflare has open-sourced Kitesurf under the Apache 2.0 license, a stateless browser aimed at AI agents. Built on Cloudflare Workers, it parses HTML, handles CSS, and executes JavaScript without a browser container. Cloudflare says the goal is a lightweight, efficient browser that uses less CPU and memory than Chromium and scales on demand across the global Workers network; the code is published on GitHub. The lower resource use and scaling claims are Cloudflare&\#x27;s own, not independently measured results.

telegram · zaihuapd · Nov 14, 09:33

**「Background」** Cloudflare&\#x27;s August 6, 2026 blog post and changelog introduced Kitesurf as a stateless, agent-first browser running entirely on Workers, offered free while in beta. The current release makes the code available under Apache 2.0 on GitHub, moving it from a hosted beta service to an open-source project.

**「Impact」** Developers building agent workloads on Workers can run page parsing and JavaScript execution without provisioning a Chromium container, which matters for deployments where per-request CPU and memory limits apply. Because Kitesurf is not a full browser engine, teams should verify that its HTML, CSS, and JavaScript coverage fits their target sites before replacing container-based browsing.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.cloudflare.com/kitesurf/">Introducing Kitesurf: The agent-first browser that runs in V8 ...</a></li>
<li><a href="https://developers.cloudflare.com/changelog/post/2026-08-06-kitesurf/">Introducing Kitesurf, an agent-first browser on Browser Run</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#Cloudflare Workers`, `#open source`, `#browser infrastructure`, `#web rendering`

---

<a id="item-tech-news-10"></a>
### [Tesla Cybercab terms require $299 monthly subscription to operate](https://www.tesla.com/configurator/api/v4/terms?category=autonomy_subs&amp;amp;locale=en_US&amp;amp;model=cc&amp;amp;saleType=Sale) ⭐️ 7.0/10

Tesla&\#x27;s published Cybercab autonomy subscription terms, as reported by a Telegram channel citing Electrek and Reuters, set the vehicle price at $29,990 and require a $299 monthly subscription for the car to run at all. Tesla may change the price with one month&\#x27;s notice, and can suspend or cancel the subscription for non-payment or misuse; three accumulated warnings reportedly disable autonomous driving for a week. The terms also restrict operation to designated areas and bar unauthorized use on ride-hailing, delivery, or rental platforms. The item is a short secondary summary without primary verification, so the terms should be treated as reported rather than independently confirmed.

telegram · zaihuapd · Nov 15, 01:10

**「Background」** Tesla&\#x27;s Cybercab is the company&\#x27;s purpose-built robotaxi, distinct from the Model Y vehicles it also uses for robotaxi service. The source notes that both the Cybercab and robotaxi Model Y run the same AI4 hardware and autonomous-driving software, while the FSD feature sold to ordinary owners still requires human supervision.

**「Impact」** For prospective owners, the effective cost of the vehicle is the $29,990 purchase price plus $299 per month indefinitely, and the car&\#x27;s usability depends on continued payment and compliance with Tesla&\#x27;s terms. The reported ban on unauthorized ride-hailing, delivery, or rental use also limits owners who might have expected to earn income with the vehicle.

**Tags**: `#autonomous driving`, `#Tesla`, `#subscription pricing`, `#robotaxi`, `#tech industry`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Anthropic IPO Reportedly Bars Mainland China and Hong Kong Investors](https://m.economictimes.com/markets/us-stocks/news/anthropic-ipo-share-orders-from-china-are-said-to-be-rebuffed/articleshow/135809948.cms) ⭐️ 8.0/10

Anthropic&\#x27;s IPO is reportedly not accepting orders from mainland Chinese and Hong Kong investors, with unnamed sources linking the restriction to ITAR export controls. The offering is set to price on November 18 and list the next day under ticker ANT, targeting a $1.4 trillion valuation and raising up to $90.4 billion, according to the report.

telegram · zaihuapd · Nov 14, 10:18

**「Background」** Anthropic, the developer of the Claude AI models, made its IPO filing public with the US Securities and Exchange Commission on October 26, 2026, after lining up investor meetings earlier in the year. The reported restriction on mainland Chinese and Hong Kong orders is tied to ITAR, the US International Traffic in Arms Regulations that govern exports of defense-related technology.

**「Impact」** The report says some of that demand is being routed through British Virgin Islands trusts, SPVs and swap structures, with orders reportedly about six times the shares available; Goldman Sachs and Morgan Stanley are leading the underwriting.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/07/15/anthropic-ipo-banks-investor-meetings.html">Anthropic moves closer to IPO as bankers line up investor meetings</a></li>
<li><a href="https://www.fxstreet.com/news/anthropic-ipo-filing-reveals-rapid-growth-as-investors-weigh-an-80-billion-loss-202610270748">Anthropic IPO filing reveals rapid growth as investors weigh an $80...</a></li>

</ul>
</details>

**Tags**: `#IPO`, `#Anthropic`, `#export controls`, `#cross-border investment`, `#capital markets`

---