---
layout: default
title: "Horizon Summary: 2026-11-11 (EN)"
date: 2026-11-11
lang: en
---

> From 69 items, 16 important content pieces were selected

---

**Technology News**
1. [Voltage Glitching Unlocks A100 Features on a Mining Card](#item-tech-news-1) ⭐️ 8.0/10
2. [Google DeepMind unveils AlphaGenome 2 for cell-type DNA effects](#item-tech-news-2) ⭐️ 8.0/10
3. [Guide to Storing SSH Keys in the macOS Secure Enclave](#item-tech-news-3) ⭐️ 7.0/10
4. [Linear Programming Explored as a Tool for Weight-Space Model Editing](#item-tech-news-4) ⭐️ 7.0/10
5. [New York&\#x27;s AI safety law takes effect, targeting OpenAI and Anthropic](#item-tech-news-5) ⭐️ 7.0/10
6. [Google adds two specialized TPUs for confidential training and memory](#item-tech-news-6) ⭐️ 7.0/10
7. [Railway Breach Exposes Credentials, Fuels $740,000 in Fraudulent AI Charges](#item-tech-news-7) ⭐️ 7.0/10
8. [Hackers Used Qubole&\#x27;s AWS IAM Credentials to Breach Customer Clouds](#item-tech-news-8) ⭐️ 7.0/10
9. [Critical Xen Orchestra Auth Bypass Actively Exploited](#item-tech-news-9) ⭐️ 7.0/10
10. [Binance warns iOS flaw could expose wallet secrets](#item-tech-news-10) ⭐️ 7.0/10
11. [Alibaba Previews Qwen4-Max on Its Token Plan](#item-tech-news-11) ⭐️ 7.0/10
12. [AMD&\#x27;s Mext AI memory tiering moves cold pages to NVMe flash](#item-tech-news-12) ⭐️ 7.0/10
13. [Report alleges Alice Huang helped move 240,000 Nvidia GPUs to China](#item-tech-news-13) ⭐️ 7.0/10

**Financial News**
1. [China Ends 90-Day Grace Period for Offshore Trust Income Tax](#item-finance-news-1) ⭐️ 8.0/10
2. [FCC Approves SpaceX&\#x27;s 800 MHz Spectrum Purchase](#item-finance-news-2) ⭐️ 7.0/10
3. [Stripe Announces OpenRouter Joins the Company](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Voltage Glitching Unlocks A100 Features on a Mining Card](https://blog.kate.land/posts/using-voltage-glitching-to-unlock-the-a100/) ⭐️ 8.0/10

A blog post by kate.land describes using voltage glitching to re-enable A100-class capabilities on a mining card, according to the post&\#x27;s account as summarized for Hacker News. The write-up is a hands-on hardware-hacking report on a single card rather than a general-purpose tool or a vendor-sanctioned modification, and no independent verification of the result is provided in the supplied material. The post drew substantial discussion about why such capabilities are fused off in the first place.

hackernews · lae · Nov 11, 10:48 · [Discussion](https://news.ycombinator.com/item?id=50451903)

**「Background」** The card in question is Nvidia&\#x27;s CMP 170HX, a GA100-based mining product sold with most of the die&\#x27;s memory and compute resources fused off. Voltage fault injection attacks work by briefly disturbing a chip&\#x27;s supply voltage to induce faults that can bypass or alter security and configuration logic, in this case the fuses that disable those resources. Independent write-ups of the post describe the result as an effective A100-80G with roughly 120–126 SMs exposed and about 1.2x the throughput of a retail A100, though these are secondary accounts rather than the source itself.

**「Impact」** For hardware and security engineers, the post illustrates that fuses used to segment GPU products can be bypassed with physical fault injection, which matters to anyone assessing whether disabled features are truly unrecoverable. The technique is described for one specific card and is not presented as a repeatable procedure for other models.

**「Community Discussion」** Commenters debated why the capabilities were disabled: amelius argued the more likely explanation is fabrication faults that made a full A100 unviable, while mr\_roboto called deliberately limiting functional hardware for market segmentation morally repugnant. roger\_ said they had bought these cards and planned to try the method, and SillyUsername wished a similar approach existed for older Tesla P100 and P4 cards.

<details><summary>References</summary>
<ul>
<li><a href="https://news.lavx.hu/article/kate-uses-voltage-glitching-to-turn-a-cmp-170hx-mining-card-into-an-a100-class-gpu">Kate uses voltage glitching to turn a CMP 170HX mining card ...</a></li>
<li><a href="https://todayforai.com/en/items/art-2770d0dd-6ab">Voltage Glitching Unlocks CMP Mining Card Into 80GB A100</a></li>

</ul>
</details>

**Tags**: `#hardware-hacking`, `#voltage-glitching`, `#gpu`, `#nvidia`, `#security`

---

<a id="item-tech-news-2"></a>
### [Google DeepMind unveils AlphaGenome 2 for cell-type DNA effects](https://www.theverge.com/ai-artificial-intelligence/1031524/google-deepmind-alphagenome-2-genetic-ai-model) ⭐️ 8.0/10

Google DeepMind has unveiled AlphaGenome 2, a successor to its AlphaGenome model for predicting how changes in DNA affect different cell types. The Verge reports that the model is intended to give scientists a more detailed view of how cell types switch genes on and off, a problem it links to understanding disease causes and potential treatments. The supplied article is a brief teaser: it provides no benchmarks, validation results, technical specifications, or release and availability details, so the model&\#x27;s actual capabilities remain unverified.

rss · The Verge · Nov 11, 15:00

**「Background」** AlphaGenome 2 succeeds DeepMind&\#x27;s original AlphaGenome, which the company described in June 2025 as achieving state-of-the-art performance on genomic prediction benchmarks, including predicting whether a genetic variant would raise or lower a gene&\#x27;s expression or alter its splicing. A January 2026 Nature paper described that model as taking 1-Mb DNA sequences as input and predicting functional genomic tracks at single-base resolution across multiple modalities. The new version is presented as a successor to that model; the supplied source does not detail what specifically changed in its architecture, training data, or performance.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/alphagenome-ai-for-better-understanding-the-genome/">AlphaGenome: AI for better understanding the genome</a></li>
<li><a href="https://www.nature.com/articles/s41586-025-10014-0">Advancing regulatory variant effect prediction with AlphaGenome</a></li>

</ul>
</details>

**Tags**: `#genomics`, `#AI for science`, `#Google DeepMind`, `#machine learning`, `#biotechnology`

---

<a id="item-tech-news-3"></a>
### [Guide to Storing SSH Keys in the macOS Secure Enclave](https://gatezh.com/posts/macos-secure-enclave-ssh-keys/) ⭐️ 7.0/10

A blog post by gatezh describes a practical method for storing SSH private keys in the macOS Secure Enclave, with the author noting in the comments that he ultimately chose the third-party app Secretive because he could not tolerate the Touch ID prompt shown by the native approach. The post is a how-to guide rather than a product release, and no source content was supplied, so specific commands, macOS versions, and compatibility conditions cannot be verified here. Commenters report using Secretive across multiple machines and for Git commit signing, while others describe preferring YubiKeys for vendor-independent, portable, and backup-friendly key storage.

hackernews · js2 · Nov 11, 04:28 · [Discussion](https://news.ycombinator.com/item?id=50449748)

**「Background」** The macOS Secure Enclave is an isolated coprocessor that can hold private keys in hardware so they cannot be exported, but it supports only the P-256 elliptic curve, which constrains which SSH key types can be stored this way. Third-party tools such as Secretive wrap this capability to manage Secure Enclave-backed SSH keys, and the article&\#x27;s author says he ultimately chose Secretive over the native approach because of the Touch ID prompt behavior.

**「Practical Trade-offs」** For practitioners, the thread highlights a concrete trade-off: Secure Enclave-backed keys tie key use to a specific Mac and its biometric prompt, whereas commenters who need portable backups or cross-machine use report relying on YubiKeys instead. One commenter also describes a macOS upgrade breaking WireGuard&\#x27;s keychain-stored keys with error -25300, after which the app deleted profiles it considered orphaned, a caution about depending on keychain-backed key storage.

**「Community Discussion」** Several commenters report long-term satisfaction with Secretive, including one who uses it for Git commit signing with a separate interaction-requiring key while keeping other keys for servers. Others argue for hardware tokens independent of the machine vendor, citing backup and physical portability as reasons they chose YubiKeys over the Secure Enclave.

<details><summary>References</summary>
<ul>
<li><a href="https://popov.wtf/secure-ssh-keys-with-secure-enclave-on-macos">Secure SSH Keys with Secure Enclave on macOS | Pavel Popov</a></li>
<li><a href="https://sesamedisk.com/protecting-ssh-keys-with-macos-secure-enclave/">Protecting SSH Keys with macOS Secure Enclave - Sesame Disk</a></li>

</ul>
</details>

**Tags**: `#security`, `#ssh`, `#macos`, `#hardware-security`, `#open-source`

---

<a id="item-tech-news-4"></a>
### [Linear Programming Explored as a Tool for Weight-Space Model Editing](https://nathan.rs/posts/weight-space-lp/) ⭐️ 7.0/10

A technical blog post examines whether linear programming \(LP\) can be used for weight-space programming of models, framing weight edits as linear constraints such as eliminating one behavior while preserving another. The post offers concrete discussion of constraints and solver guidance, but the evidence is limited to the author&\#x27;s analysis rather than a shipped tool or independently measured result. Hacker News commenters debated how this relates to model-editing claims and whether such optimization belongs in training.

hackernews · emschwartz · Nov 11, 12:30 · [Discussion](https://news.ycombinator.com/item?id=50452655)

**「Background」** The post follows a November 2, 2026 blog post by four MIT CSAIL researchers claiming that GPT-6 Astra could natively read and write neural-network weights without gradient descent or a training loop, and that editing 0.016% of Qwen3.5-0.8B&\#x27;s weights raised MATH-500 from 7.9% to 48.1% in author-run tests. The LP analysis examines whether such weight edits can instead be framed as constrained optimization problems solved with linear-programming solvers.

**「Impact」** For practitioners interested in model editing, the post&\#x27;s framing suggests LP solvers could serve as a guided tool for weight edits rather than a replacement for training, though the approach remains unverified beyond the blog post.

**「Community Discussion」** Commenters offered differing interpretations: jsw97 suggested LP solvers could make weight-editing methods more effective when given constraints, while ultimatefan1 argued recent headlines overstated frontier models&\#x27; ability to directly manipulate weights, since they are trained on tokens and task completion rather than weights. dansitu said the simplicity of the approach suggests it should happen during training via regularization, and rbnafo welcomed a return to numerical analysis over reliance on LLMs.

<details><summary>References</summary>
<ul>
<li><a href="https://kingy.ai/blog/weight-space-programming-ai-agent-model-weights/">Weight-Space Programming: GPT-6 Astra Edits Qwen - kingy.ai</a></li>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights: MATH-500 7.9% to 48.1% ...</a></li>
<li><a href="https://www.datacamp.com/blog/weight-space-programming">Weight-Space Programming: How LLMs Edit Network Weights</a></li>

</ul>
</details>

**Tags**: `#linear programming`, `#model editing`, `#weight-space optimization`, `#machine learning`, `#numerical methods`

---

<a id="item-tech-news-5"></a>
### [New York&\#x27;s AI safety law takes effect, targeting OpenAI and Anthropic](https://techcrunch.com/2026/11/10/openai-anthropic-face-new-oversight-as-new-yorks-ai-safety-law-takes-effect/) ⭐️ 7.0/10

New York is preparing to enforce a sweeping AI safety law that requires major developers such as OpenAI and Anthropic to register, disclose their safety practices, and report critical incidents, with fines as the stated penalty for noncompliance. The supplied report does not specify which developers fall within scope, the registration thresholds, the size of the fines, or the enforcement timeline, so the law&\#x27;s precise reach and obligations remain unclear from this account. The measure is described as taking effect, but the source does not indicate whether any company has yet registered or disclosed under it.

rss · TechCrunch AI · Nov 10, 20:52

**「Background」** The law&\#x27;s passage followed a contested political fight: a Fortune report from June 2026 said OpenAI&\#x27;s backers spent $7.6 million in a Manhattan primary against Alex Bores, the sponsor of what it described as New York&\#x27;s toughest AI safety law, while Anthropic spent $10 million to support him. The current source does not specify the law&\#x27;s scope, thresholds, penalties, or compliance timeline.

**「Impact」** Large frontier developers face additional requirements and assessments intended to fund state oversight, according to external coverage of the law. Companies in scope should prepare registration filings, safety-plan documentation, and incident-reporting procedures before enforcement begins, since the supplied source does not specify thresholds, penalties, or deadlines.

<details><summary>References</summary>
<ul>
<li><a href="https://fortune.com/2026/06/17/bores-openai-anthropic-manhattan-primary-ai-regulation/">OpenAI &#x27;s backers spent $7.6 million to destroy a state... | Fortune</a></li>
<li><a href="https://www.multistate.ai/updates/vol-83-new-york-ai-safety-law-raise-act">New York AI Safety Law : RAISE Act Changes — multistate. ai</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#AI safety`, `#policy`, `#OpenAI`, `#Anthropic`

---

<a id="item-tech-news-6"></a>
### [Google adds two specialized TPUs for confidential training and memory](https://techcrunch.com/2026/11/10/google-broadens-its-ai-hardware-portfolio-with-two-new-specialized-chips/) ⭐️ 7.0/10

Google announced two new tensor processing units \(TPUs\) that extend its AI chip lineup to additional use cases, including confidential model training and greater memory capacity. The announcement names no chip models, specifications, benchmarks, pricing, or availability dates, and the supplied material does not indicate whether the chips are shipping or only planned. The details come from a brief summary rather than independent testing.

rss · TechCrunch AI · Nov 10, 15:54

**「Background」** Google designs its own TPUs to power AI workloads in its cloud rather than relying solely on third-party chips. At Hot Chips 2026, Google discussed its eighth-generation TPU family, including the TPU 8t for training and the TPU 8i for inference, according to ServeTheHome. The new variants extend that lineup to confidential model training and higher-memory use cases.

<details><summary>References</summary>
<ul>
<li><a href="https://www.servethehome.com/googles-tpuv8s-for-training-and-inference-at-hot-chips-2026/">Google’s TPUv8s for Training and Inference at Hot Chips 2026</a></li>

</ul>
</details>

**Tags**: `#AI hardware`, `#TPU`, `#Google`, `#confidential computing`, `#AI infrastructure`

---

<a id="item-tech-news-7"></a>
### [Railway Breach Exposes Credentials, Fuels $740,000 in Fraudulent AI Charges](https://www.bleepingcomputer.com/news/apple/railway-breach-leads-to-740-000-in-fraudulent-ai-charges/) ⭐️ 7.0/10

Cloud hosting provider Railway reported that attackers exploited vulnerabilities in its infrastructure to steal customer authentication secrets and generate roughly $740,000 in fraudulent AI usage. The incident may have exposed credentials for up to 100,000 workspaces. The figures come from Railway&\#x27;s own incident report, and the source does not specify which vulnerabilities were involved, when the breach occurred, or whether the fraudulent charges were absorbed or passed on to customers.

rss · BleepingComputer · Nov 10, 22:20

**「Background」** Railway is a cloud platform for deploying web apps, servers, and databases, offering automatic scaling, monitoring, and security features. The incident centers on stolen customer authentication secrets being used to run up AI compute charges, rather than on a flaw in the AI models themselves.

**「Impact」** Because stolen authentication secrets could grant access to affected workspaces, Railway customers should treat credentials stored in or connected to the platform as potentially compromised and rotate them. The case also shows that stolen cloud credentials can be converted directly into AI compute costs, so teams should monitor AI usage and spending for anomalies rather than relying only on access controls.

<details><summary>References</summary>
<ul>
<li><a href="https://railway.com/">Railway | The all-in-one intelligent cloud provider</a></li>

</ul>
</details>

**Tags**: `#security`, `#cloud-infrastructure`, `#ai-compute`, `#credential-theft`, `#incident-report`

---

<a id="item-tech-news-8"></a>
### [Hackers Used Qubole&\#x27;s AWS IAM Credentials to Breach Customer Clouds](https://www.bleepingcomputer.com/news/security/hackers-exploit-trusted-aws-access-to-breach-multiple-cloud-environments/) ⭐️ 7.0/10

A threat actor used compromised IAM credentials tied to Qubole&\#x27;s AWS account to access and exfiltrate data from multiple customers&\#x27; AWS environments, according to BleepingComputer. The report describes a cross-tenant breach in which trusted access granted to the big data platform was abused rather than broken into directly. The supplied excerpt does not name affected customers, the number of environments reached, the data taken, or a timeline, and it does not describe remediation steps or AWS&\#x27;s response.

rss · BleepingComputer · Nov 10, 19:31

**「Background」** Qubole is a big data platform that runs workloads in customers&\#x27; own AWS accounts, so its IAM credentials can carry permissions across those environments. SecurityWeek reports that the same leaked Qubole credentials were used to steal data from more than a dozen organizations, including credentials, secrets, and files.

**「Impact」** The incident points to a specific risk for organizations that grant third-party platforms IAM roles into their own AWS accounts: a compromise on the vendor side can extend to every customer that trusted it. The source does not detail which permissions were involved or whether affected customers have been notified, so the practical scope of credential rotation or access review is not established by the available evidence.

<details><summary>References</summary>
<ul>
<li><a href="https://www.securityweek.com/over-a-dozen-organizations-hit-in-qubole-supply-chain-attack/">Over a Dozen Organizations Hit in Qubole Supply... - SecurityWeek</a></li>

</ul>
</details>

**Tags**: `#cloud security`, `#AWS`, `#IAM`, `#data breach`, `#supply chain`

---

<a id="item-tech-news-9"></a>
### [Critical Xen Orchestra Auth Bypass Actively Exploited](https://www.bleepingcomputer.com/news/security/critical-xen-orchestra-auth-bypass-flaw-exploited-to-hijack-vm-servers/) ⭐️ 7.0/10

A critical authentication bypass vulnerability in Xen Orchestra is being actively exploited in attacks that can grant administrator privileges and allow takeover of XCP-ng virtualization hosts, according to BleepingComputer. The report does not specify the affected versions, the vulnerability&\#x27;s mechanism, or whether a patch is available. The exploitation is described as ongoing, so the flaw should be treated as a live risk rather than a theoretical one.

rss · BleepingComputer · Nov 10, 16:17

**「Background」** Xen Orchestra is the web-based management interface for XCP-ng and Citrix Hypervisor \(formerly XenServer\), so a login bypass there exposes the virtualization hosts it administers. The flaw is tracked as CVE-2024-55555 with a CVSSv3.1 score of 9.8, and it lets unauthenticated remote attackers bypass the login mechanism entirely and obtain administrative privileges, according to a remediation guide cited in coverage of the exploitation.

**「Impact」** Because successful exploitation yields administrator access, operators running Xen Orchestra to manage XCP-ng hosts should treat exposed management interfaces as potentially compromised and restrict access until they can confirm their version&\#x27;s patch status. The source provides no version or patch details, so affected administrators will need to check vendor advisories directly.

<details><summary>References</summary>
<ul>
<li><a href="https://securityarsenal.com/blog/xen-orchestra-authentication-bypass-cve-2024-55555-detection-and-remediation-guide-for-xcp-ng-infrastructure">Xen Orchestra Authentication Bypass (CVE-2024-55555 ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#virtualization`, `#Xen Orchestra`, `#XCP-ng`

---

<a id="item-tech-news-10"></a>
### [Binance warns iOS flaw could expose wallet secrets](https://www.bleepingcomputer.com/news/security/binance-warns-of-ios-flaw-that-could-leak-crypto-wallet-secrets/) ⭐️ 7.0/10

Binance is warning that a vulnerability in Apple&\#x27;s iOS 26.7.1, 27.0.1, and 27.2 could allow third-party apps to read private files stored by other apps, including cryptocurrency seed phrases, secret keys, and login credentials. The advisory names the affected iOS versions but, in the available excerpt, does not describe the underlying flaw, an exploit path, or a fix. It is a vendor warning rather than an independently confirmed or measured result.

rss · BleepingComputer · Nov 10, 15:59

**「Background」** Binance&\#x27;s November 10 warning names the flaw &quot;worse\_query&quot; and says it lets malicious apps read files belonging to other apps on affected iOS versions. The advisory identifies iOS 26.7.1, 27.0.1, and 27.2 as affected, with seed phrases, private keys, and login details cited as data at risk. The supplied reports do not describe the underlying technical mechanism or state whether Apple has released a fix.

**「Impact」** Users on the affected iOS versions should update to iOS 27.2.1, which a report says Apple released to address the flaw; Binance&\#x27;s warning covers 26.7.1, 27.0.1, and 27.2. Until patched, wallet apps relying on iOS file isolation to protect seed phrases and credentials cannot assume other installed apps are unable to read that data.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/ios-flaw-expose-crypto-wallet/">Binance Warns iPhone Users of Major iOS Flaw That May Expose ...</a></li>
<li><a href="https://cryptonews.com/news/binance-ios-worse-query-iphone-duo-18pro-security-flaw/">iPhone Duo Under Attack? Binance Flags iOS Security Flaw</a></li>
<li><a href="https://happycoin.news/en/apple-i-google-zakryli-uyazvimosti-a-binance-predupredila-ob-atakah-na-seed-frazy-v-ios/">Apple , Google, and Binance have secured crypto wallet owners...</a></li>

</ul>
</details>

**Tags**: `#security`, `#iOS`, `#vulnerability`, `#cryptocurrency`, `#mobile`

---

<a id="item-tech-news-11"></a>
### [Alibaba Previews Qwen4-Max on Its Token Plan](https://mp.weixin.qq.com/s/J_zbVHa2R3mmY5KD4v3-bw) ⭐️ 7.0/10

Alibaba has teased its Qwen4 model family and launched a Qwen4-Max preview on its Token Plan, according to a brief promotional post. The company claims deeper knowledge understanding, more three-dimensional world perception, and further advances in coding and agentic capabilities, but the post provides no benchmarks, technical specifications, or independent verification. The preview is available at a limited-time discount of up to 90% off, and Alibaba says Qoder, the Qwen App, and QwenStudio have already integrated the new model.

telegram · zaihuapd · Nov 11, 02:35

**「Background」** Alibaba&\#x27;s Qwen team had previously released Qwen3.8-Flash-Next, an open-weight multimodal model described as previewing the architecture planned for the Qwen 4 family, with 125 billion parameters. The Qwen4-Max preview is positioned as the flagship of the Qwen 4 series, optimized for complex programming and agent tasks, and is available only through Alibaba&\#x27;s Token Plan rather than as a downloadable model.

**「What It Means for Users」** Developers and users of Qoder, the Qwen App, and QwenStudio can already access Qwen4-Max through those products, while others can try it via the Token Plan during the promotional discount period. Because the capability claims are vendor-sourced and unbenchmarked, teams should validate performance on their own workloads before relying on the preview in production.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kucoin.com/news/flash/aliyun-launches-qwen4-max-preview-focused-on-complex-programming">Aliyun Launches Qwen 4 - Max Preview Focused on Complex... | KuCoin</a></li>
<li><a href="https://www.youtube.com/watch?v=Ie-k0mGntDA">It&#x27;s Here: Qwen 4 Max Preview (No 27B Yet) - YouTube</a></li>
<li><a href="https://ask.yugatech.com/general/qwen3-8-flash-next-previews-the-qwen4-architecture-with-125b-parameters/">Qwen3.8-Flash-Next Previews The Qwen 4 Architecture With...</a></li>

</ul>
</details>

**Tags**: `#llm`, `#qwen`, `#alibaba`, `#model-release`, `#ai-agents`

---

<a id="item-tech-news-12"></a>
### [AMD&\#x27;s Mext AI memory tiering moves cold pages to NVMe flash](https://www.theregister.com/systems/2026/11/11/amd-where-were-going-we-dont-need-as-much-dram/5308953) ⭐️ 7.0/10

AMD is commercializing technology from its Mext acquisition as software that uses an AI model to transparently page memory between DRAM and cheaper NVMe flash, moving cold pages without the operating system or applications noticing. AMD claims that replacing half of a server&\#x27;s DRAM with flash retains up to 99% of performance and estimates enterprise server costs could fall by as much as 83%. The Mext license must be purchased together with Epyc servers, and the performance and cost figures are AMD&\#x27;s own claims rather than independently measured results.

telegram · zaihuapd · Nov 11, 11:15

**「Background」** AMD acquired MEXT, a startup whose software makes NAND flash appear as DRAM to the operating system through memory tiering, in June 2026. AMD said at the time that it planned to integrate MEXT&\#x27;s technology across its data center portfolio. The current item describes that technology being packaged as a software product licensed alongside Epyc server purchases.

**「Impact」** Organizations sizing Epyc servers would need to buy the Mext license alongside the hardware to use the tiering, so the claimed savings depend on AMD&\#x27;s estimates holding in their workloads; the source provides no independent benchmarks or details on which workloads were tested.

<details><summary>References</summary>
<ul>
<li><a href="https://www.amd.com/en/blogs/2026/amd-acquires-mext-for-memory-optimization.html">AMD Acquires MEXT to Advance Memory Optimization</a></li>
<li><a href="https://www.tomshardware.com/pc-components/cpus/amd-takes-over-mext-to-address-growing-memory-constraints-in-the-data-center-memory-tiering-technology-enables-flash-to-appear-as-dram-to-applications">AMD takes over MEXT for memory tiering tech that enables ...</a></li>
<li><a href="https://www.amd.com/en/products/software/mext.html">AMD MEXT Predictive Memory Software</a></li>

</ul>
</details>

**Tags**: `#memory-tiering`, `#AMD`, `#server-hardware`, `#AI-for-systems`, `#NVMe`

---

<a id="item-tech-news-13"></a>
### [Report alleges Alice Huang helped move 240,000 Nvidia GPUs to China](https://www.tomshardware.com/tech-industry/policy/alice-huang-reportedly-instrumental-in-securing-over-usd7-5-billion-of-nvidia-ai-gpu-imports-during-three-year-relationship-with-jensen-huang-helped-move-240-000-banned-chips-into-china-mostly-h100-and-h200) ⭐️ 7.0/10

An investigation by The Information, summarized by Tom&\#x27;s Hardware, alleges that Alice Huang used a relationship with Nvidia CEO Jensen Huang to help move roughly 240,000 restricted Nvidia AI GPUs into China, mostly H100 and H200 models. The report puts the value of the AI GPU imports at about $7.5 billion and names Shanghai Century Litong and Singapore&\#x27;s Megaspeed among the companies involved. These are allegations from a secondhand summary of the investigation, not confirmed findings, and the supplied material gives no primary sourcing detail.

telegram · zaihuapd · Nov 11, 14:41

**「Background」** The US has restricted exports of advanced Nvidia AI accelerators such as the H100 and H200 to China, making the chips subject to licensing controls rather than freely exportable. The Information&\#x27;s investigation, relayed by Reuters and Tom&\#x27;s Hardware, alleges that Alice Huang used ties to Nvidia to secure supplies when orders for restricted chips stalled, moving roughly 240,000 H100, H200 and some A100 chips into China. These remain allegations from the reporting, not confirmed findings.

**「Why it matters」** If substantiated, the alleged volume would represent a large diversion of export-restricted AI accelerators, a concern for suppliers and regulators tracking whether H100 and H200 chips reach China despite controls. The report does not establish how the shipments were routed or whether any enforcement action has followed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theinformation.com/articles/jensen-huangs-yearslong-ties-alice-huang-enabled-nvidia-chip-sales-china">How Jensen Huang’s Yearslong Ties to Alice Huang Enabled $7 ...</a></li>
<li><a href="https://www.reuters.com/world/china/nvidia-ceos-affair-aided-75-billion-chip-shipments-china-information-reports-2026-11-10/">Nvidia faces deepening scrutiny over China chip ties, CEO ...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/policy/alice-huang-reportedly-instrumental-in-securing-over-usd7-5-billion-of-nvidia-ai-gpu-imports-during-three-year-relationship-with-jensen-huang-helped-move-240-000-banned-chips-into-china-mostly-h100-and-h200">Alice Huang reportedly instrumental in securing over $7.5 ...</a></li>

</ul>
</details>

**Tags**: `#nvidia`, `#export-controls`, `#ai-hardware`, `#supply-chain`, `#investigative-reporting`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China Ends 90-Day Grace Period for Offshore Trust Income Tax](https://www.news.cn/20261111/9bcce99c779b4a6197ff45bbbc3e4c50/c.html) ⭐️ 8.0/10

China&\#x27;s tax authority said on November 11 that the 90-day transition period for taxing offshore trust income ended with more than RMB 160 billion in personal income tax declared, including over RMB 120 billion collected in October, which lifted national personal income tax revenue by nearly 90% that month.

telegram · zaihuapd · Nov 11, 10:35

**「Background」** A July 24, 2026 notice from the Ministry of Finance and the tax authority said taxpayers who declared and paid within the 90-day window would not owe late fees; officials now say those who did not declare, or declared inaccurately, will be pressed to pay with late fees and face audits if they still do not comply.

**「Impact」** The collections affect wealthy individuals holding offshore trusts and give a one-off boost to October fiscal revenue, though the source does not say how much of the total reflects new declarations versus shifted timing.

**Tags**: `#offshore trusts`, `#personal income tax`, `#tax enforcement`, `#fiscal revenue`, `#China policy`

---

<a id="item-finance-news-2"></a>
### [FCC Approves SpaceX&\#x27;s 800 MHz Spectrum Purchase](https://wap.cj.sina.cn/7x24/5206981) ⭐️ 7.0/10

The U.S. Federal Communications Commission approved SpaceX&\#x27;s application to acquire 800 MHz spectrum nationwide through a deal with Grain Management, covering 546 paired licenses and nearly the entire U.S. population. Verizon, AT&amp;T and T-Mobile declined to give SpaceX access to their networks.

telegram · zaihuapd · Nov 11, 02:14

**「Background」** Grain Management announced a definitive agreement in October 2026 to sell its nationwide 800 MHz spectrum portfolio to SpaceX, and the FCC&\#x27;s Wireless Telecommunications Bureau then opened the transfer applications for the licenses. The 800 MHz band is low-frequency spectrum that carries signals well through walls and works with nearly all smartphones.

**「Impact」** The approval gives SpaceX low-band airwaves that can reach indoors and work with nearly all smartphones, potentially letting its Starlink mobile service compete with Verizon, AT&amp;T and T-Mobile without renting their networks.

<details><summary>References</summary>
<ul>
<li><a href="https://graingp.com/grain-management-announces-definitive-agreement-to-sell-nationwide-800-mhz-spectrum-portfolio-to-spacex/">Grain Management Announces Definitive Agreement to Sell ...</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/DA-26-1218A1.pdf">DA 26-1218 TRANSFER OF CONTROL OF 800 MHZ SPECTRUM LICENSES ...</a></li>
<li><a href="https://sxcontent9668.azureedge.us/cms-assets/assets/FCC_Narrative_10_8_26_f63e78e026.pdf">Draft PIS and Description of the Transaction (Grain 800 MHz ...</a></li>
<li><a href="https://wccftech.com/spacex-grabs-a-piece-of-the-800-mhz-spectrum-that-would-allow-starlink-mobile-to-work-indoors-sidestepping-att-t-mobile-and-verizon-after-they-refused-to-partner/">SpaceX Grabs A Piece Of The 800 MHz Spectrum That ... - Wccftech</a></li>
<li><a href="https://arstechnica.com/tech-policy/2026/10/starlink-spectrum-deal-boosts-musk-plan-to-beat-att-t-mobile-and-verizon/">Starlink spectrum deal boosts Musk plan to beat AT&amp;T, T ...</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#FCC`, `#spectrum`, `#telecom`, `#regulation`

---

<a id="item-finance-news-3"></a>
### [Stripe Announces OpenRouter Joins the Company](https://x.com/stripe/status/2120240651778355306) ⭐️ 7.0/10

Stripe announced that OpenRouter has joined the company, saying the two will build economic infrastructure for AI and help businesses explore new models and optimize token routing and usage. The announcement gave no deal terms, valuation, or purchase price.

telegram · zaihuapd · Nov 11, 09:45

**「Background」** OpenRouter is an AI gateway that lets developers access models from multiple providers through one interface; it had raised $113 million at a $1.3 billion valuation before this deal, according to reports cited in search results. Stripe&\#x27;s own newsroom post says it agreed to acquire OpenRouter, while the reported $7 billion price tag comes from third-party coverage rather than the announcement.

**「Impact」** Businesses that use OpenRouter to route requests across AI models now face uncertainty about whether its pricing, model access, or service terms will change under Stripe ownership, though no such changes were announced.

<details><summary>References</summary>
<ul>
<li><a href="https://finelo.com/blog/stripe-openrouter-acquisition-2026">Stripe Acquires OpenRouter | Understand the AI Deal | Finelo</a></li>
<li><a href="https://news.google.com/stories/CAAqNggKIjBDQklTSGpvSmMzUnZjbmt0TXpZd1NoRUtEd2lWaG9IcEVSRnRHVm80Y0YtM1NpZ0FQAQ?hl=en-US&amp;gl=US&amp;ceid=US:en">Stripe acquires artificial intelligence startup OpenRouter - Overview</a></li>
<li><a href="https://laava.nl/en/news/openrouter-model-routing-enterprise-ai-runtime">OpenRouter &#x27;s funding shows why model routing belongs in the AI ...</a></li>

</ul>
</details>

**Tags**: `#acquisition`, `#Stripe`, `#OpenRouter`, `#AI infrastructure`, `#fintech`

---