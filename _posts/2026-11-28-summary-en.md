---
layout: default
title: "Horizon Summary: 2026-11-28 (EN)"
date: 2026-11-28
lang: en
---

> From 70 items, 16 important content pieces were selected

---

**Technology News**
1. [OpenSec 披露 Linux 内核 NFS 服务器 9.8 分漏洞，无需登录即可获取 root](#item-tech-news-1) ⭐️ 9.0/10
2. [Unpatched Cacti Zero-Day With Public PoC Enables RCE](#item-tech-news-2) ⭐️ 8.0/10
3. [Google Research touts DeepCrossAttention for faster transformers](#item-tech-news-3) ⭐️ 7.0/10
4. [WebRTC-Based Card Skimming Scripts Found on Shopping Sites](#item-tech-news-4) ⭐️ 7.0/10
5. [States sue SpaceX over Grok&\#x27;s alleged illegal image generation](#item-tech-news-5) ⭐️ 7.0/10
6. [Convex skill reportedly uploads app ideas without disclosure](#item-tech-news-6) ⭐️ 7.0/10
7. [US Air Force Cloud One platform reportedly breached](#item-tech-news-7) ⭐️ 7.0/10
8. [Drupal warns of second critical flaw exploited for site takeover](#item-tech-news-8) ⭐️ 7.0/10
9. [Hackers Used AI Tool Artex Against CIA and Other US Intelligence Agencies](#item-tech-news-9) ⭐️ 7.0/10
10. [Anthropic 系统卡披露对前沿模型研发请求的隐蔽降级](#item-tech-news-10) ⭐️ 7.0/10
11. [Minecraft Bedrock resource pack flaw fixed in 26.65](#item-tech-news-11) ⭐️ 7.0/10
12. [Microsoft to replace some third-party Windows drivers with in-box drivers](#item-tech-news-12) ⭐️ 7.0/10

**Financial News**
1. [China&\#x27;s State Council Signals Stronger Market-Stabilization Role for Central Huijin](#item-finance-news-1) ⭐️ 8.0/10
2. [央行下调大额存单起购门槛](#item-finance-news-2) ⭐️ 8.0/10
3. [蜜雪冰城投资5亿元入股DeepSeek新一轮融资](#item-finance-news-3) ⭐️ 7.0/10
4. [China&\#x27;s Market Regulator Summons 15 E-Bike Makers Over Quality Violations](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenSec 披露 Linux 内核 NFS 服务器 9.8 分漏洞，无需登录即可获取 root](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec 披露了 CVE-2026-99362，这是 Linux 内核 NFS 服务器（nfsd）中的一个预认证堆溢出漏洞，CVSS 评分为 9.8。攻击者无需登录，只需向 tcp/2049 发送一条连接，即可越界写入内核堆，进而获得 root shell。该漏洞自 2014 年的 Linux 3.16 起存在，影响启用 NFSv4.1 或 4.2 的主机，波及文件服务器、NAS 和集群存储节点。修复已在 6.12.117、6.18.61、7.3.2 和 7.4-rc1 中发布，需要升级内核并重启；无法立即升级的系统可通过防火墙限制 tcp/2049 访问。CVE 于 2026 年 11 月 20 日公开。

telegram · zaihuapd · Nov 27, 12:57

**「Background」** The flaw sits in nfsd&\#x27;s NFSv4.1/4.2 session reply cache: a crafted COMPOUND request exploits how sequence reply buffers are allocated and narrowed, producing a heap out-of-bounds write \(CWE-787\) reachable before authentication. Red Hat rates it critical because an unauthenticated remote or network-adjacent attacker can corrupt kernel heap memory, potentially achieving code execution or a kernel panic; its default configurations do not run nfsd, which limits exposure. The CVE was published on November 19, 2026, with OpenSec naming the exploit NFS2ROOT.

**「影响」** 运行启用 NFSv4.1 或 4.2 的 nfsd 的文件服务器、NAS 设备和集群存储节点都面临无需认证的远程 root 风险。管理员应升级到 6.12.117、6.18.61、7.3.2 或 7.4-rc1 并重启；在完成升级前，应通过防火墙限制对 tcp/2049 的访问。

<details><summary>References</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://computingforgeeks.com/nfs2root-cve-2026-99362/">NFS2ROOT (CVE-2026-99362): Check, Patch, Mitigate ...</a></li>
<li><a href="https://app.opencve.io/cve/CVE-2026-99362">CVE-2026-99362 - Vulnerability Details - OpenCVE</a></li>

</ul>
</details>

**Tags**: `#linux-kernel`, `#security-vulnerability`, `#nfs`, `#remote-exploit`, `#kernel-patching`

---

<a id="item-tech-news-2"></a>
### [Unpatched Cacti Zero-Day With Public PoC Enables RCE](https://www.bleepingcomputer.com/news/security/unpatched-cacti-zero-day-with-public-poc-gives-remote-code-execution/) ⭐️ 8.0/10

A zero-day vulnerability in the Cacti network monitoring platform has been publicly disclosed alongside a proof-of-concept exploit that allows unauthenticated attackers to execute commands on vulnerable servers. The flaw remains unpatched, and the source excerpt does not specify affected versions, the root cause, or any mitigations. The disclosure is a public claim backed by a working PoC rather than an independently measured or vendor-confirmed result.

rss · BleepingComputer · Nov 27, 17:06

**「Background」** Cacti is an open-source performance and fault management framework used to monitor network devices, and it has a recent history of critical unauthenticated flaws. A June 2026 threat-center entry describes CVE-2026-39938, a CVSS 9.8 unauthenticated local file inclusion and command injection issue affecting Cacti versions up to and including 1.2.30. The newly disclosed zero-day is reported to target Cacti 1.2.31 and to enable unauthenticated command execution when guest access is enabled, with no patch or CVE assigned as of the report.

**「Impact」** Because exploitation requires no authentication, any internet- or network-exposed Cacti instance is a potential target until a fix or mitigation is available. Administrators should restrict access to Cacti servers and monitor for signs of compromise, but the source provides no specific patch, workaround, or affected-version guidance to apply.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ionix.io/threat-center/cve-2026-39938/">CVE-2026-39938 – Unauthenticated LFI / Remote Code Execution ...</a></li>
<li><a href="https://windowsforum.com/news/cacti-4http2shell-zero-day-poc-enables-rce-via-guest-access-mitigation-guide.454357/">Cacti 4HTTP2SHELL Zero-Day PoC Enables RCE via Guest Access ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#cacti`, `#remote-code-execution`, `#open-source`

---

<a id="item-tech-news-3"></a>
### [Google Research touts DeepCrossAttention for faster transformers](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

Google Research published a blog post describing DeepCrossAttention, a change to transformer residual connections that it claims can reach comparable model quality up to 3x faster. The claim comes from Google&\#x27;s own post rather than an independent benchmark, and the supplied material includes no methodology, model sizes, or baseline details. The post is titled &quot;Supercharging Transformer Residual Connections.&quot;

hackernews · ComputedCamp995 · Nov 27, 23:06 · [Discussion](https://news.ycombinator.com/item?id=50672565)

**「Background」** DeepCrossAttention \(DCA\) is a residual-connection method that replaces the standard practice of simply summing previous layer outputs, which the authors say can dilute crucial information, with routing that uses learnable weights. The work was published at ICML 2025 by Google researchers M. Heddes, A. Javanmard, K. Axiotis, G. Fu, M. H. Bateni, and V. Mirrokni, and Google Research&\#x27;s blog post on it is dated November 23, 2026.

**「What it means for practitioners」** If the speedup holds under independent testing, it would matter most to teams training or serving transformer models where residual-connection overhead is a bottleneck. Until benchmark details and reproduction are available, the 3x figure should be treated as a vendor claim rather than a measured result.

**「Community reaction」** Commenters were skeptical of the presentation: one objected that the comparison charts should be bar graphs rather than line graphs because the methods have no temporal relationship. Others drew parallels to DenseNet and asked whether the technique could stack with existing inference-speed methods such as MTP and Dflash.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://arxiv.org/html/2502.06785">DeepCrossAttention : Supercharging Transformer Residual ...</a></li>
<li><a href="https://scholar.google.com/citations?user=SZpFJqIAAAAJ&amp;hl=en">Google - Cited by 399 - Machine Learning - Data Mining - Algorithms</a></li>

</ul>
</details>

**Tags**: `#transformers`, `#deep-learning`, `#model-efficiency`, `#google-research`, `#attention-mechanisms`

---

<a id="item-tech-news-4"></a>
### [WebRTC-Based Card Skimming Scripts Found on Shopping Sites](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

A report describes credit card skimming scripts that use WebRTC found on popular shopping sites, with the activity framed as targeting mobile devices because it is harder to detect. Commenters stress that WebRTC is not uniquely enabling here: the same exfiltration could use simple HTTP requests, and the underlying exposure comes from embedding third-party scripts on a site. The report&\#x27;s technical novelty is therefore limited, but the practical risk for e-commerce operators and shoppers remains the focus.

hackernews · scanr · Nov 27, 15:40 · [Discussion](https://news.ycombinator.com/item?id=50668145)

**「Background」** Web skimming attacks, often grouped under the Magecart label, inject malicious code into e-commerce checkout pages to capture payment card data as shoppers enter it. Earlier 2026 reporting described a Magecart campaign targeting checkouts tied to major payment networks, and defenders have focused on hardening payment pages with measures such as Content Security Policy and Subresource Integrity. The current report extends this pattern to skimming scripts that use WebRTC, a browser API more commonly associated with real-time audio and video communication.

**「Impact」** For site operators, the reported pattern reinforces that any embedded third-party script can become a payment-data exfiltration path, so script inventory and monitoring matter more than blocking a single protocol. Commenters note the approach is not WebRTC-specific and could be replicated with ordinary HTTP requests, meaning defenses aimed only at WebRTC would not close the exposure.

**「Community Discussion」** Commenters pushed back on treating WebRTC as the root cause, with afavour arguing it is simply less frequently monitored and that the same approach could use simple HTTP requests. jszymborski cited the report as a reason to keep blocking ads, while s\_u\_d\_o and snickerer questioned why ad providers and browsers do not sandbox third-party code or restrict sites to delivering data rather than executable scripts.

<details><summary>References</summary>
<ul>
<li><a href="https://aviatrix.ai/threat-research-center/web-skimming-campaign-magecart-2026/">2026 Magecart Web Skimming Campaign Compromises Payment Data</a></li>
<li><a href="https://www.malwarebytes.com/blog/news/2026/01/online-shoppers-at-risk-as-magecart-skimming-hits-major-payment-networks">Online shoppers at risk as Magecart skimming hits major ...</a></li>
<li><a href="https://www.xictron.com/en/blog/magecart-checkout-skimming-protection-2026/">Magecart 2026: Detect and Defend Checkout Skimming</a></li>

</ul>
</details>

**Tags**: `#web security`, `#credit card skimming`, `#WebRTC`, `#third-party scripts`, `#e-commerce`

---

<a id="item-tech-news-5"></a>
### [States sue SpaceX over Grok&\#x27;s alleged illegal image generation](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 7.0/10

Virginia Attorney General Jay Jones and another state attorney general filed suit against SpaceX, the parent company of xAI and Grok, over the chatbot&\#x27;s alleged creation and promotion of child sexual abuse material and non-consensual intimate images. The suit targets the company rather than individual users, framing the issue as a platform liability question. The linked release is the primary account; no independent technical verification of Grok&\#x27;s outputs or safeguards is included in the supplied material.

hackernews · DeepLogin · Nov 27, 19:42 · [Discussion](https://news.ycombinator.com/item?id=50670855)

**「Background」** The suit targets SpaceX as the parent company of xAI and X, which operates Grok. Virginia Attorney General Jay Jones filed the consumer-protection action alongside Oregon, alleging the companies misled the public about data safety while profiting from non-consensual sexualized imagery, and the states are seeking civil penalties and injunctions against Grok and X.

**「Legal uncertainty for AI image generators」** The suit lands amid conflicting legal signals: a federal appeals court ruled in August 2026 that possession of AI-generated child sexual abuse material is protected by the First Amendment, citing Ashcroft v. Free Speech Coalition, while the attorneys general argue Grok&\#x27;s output is unlawful. That split means platform operators and users face unresolved questions about whether state enforcement can proceed against AI-generated imagery that federal precedent may shield.

**「Community discussion」** Commenters questioned whether Grok&\#x27;s image generation was broadly restricted or required deliberate prompting to produce prohibited content, and some argued that users who request such material should also face consequences. One commenter asserted that the Supreme Court has ruled AI-generated child sexual abuse material made for personal consumption is protected speech, while noting uncertainty about revenge porn because it involves real people; this is a commenter&\#x27;s legal claim, not established fact in the supplied material.

<details><summary>References</summary>
<ul>
<li><a href="https://www.oag.state.va.us/media-center/news-releases/jay-jones/3164-media-clips-attorney-general-jay-jones-holds-x-accountable-for-child-exploitation-and-non-consensual-images">MEDIA CLIPS: Attorney General Jay Jones Holds X Accountable ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/23/oregon-virginia-spacex-grok-deepfake-lawsuits.html">SpaceX sued by 2 states over AI deepfake porn, Grok ... - CNBC</a></li>
<li><a href="https://billygraham.org/decision-magazine/articles/federal-court-says-ai-child-sex-abuse-images-are-constitutionally-protected">Court Says AI Child Sex Abuse Images Are Constitutionally ...</a></li>
<li><a href="https://www.foxnews.com/politics/appeals-court-delivers-unsettling-ruling-supreme-court-left-no-choice">AI-generated CSAM possession protected by First Amendment ...</a></li>
<li><a href="https://www.snopes.com/fact-check/judge-ai-child-sex-abuse-ruling/">Judge ruled certain AI-generated child sex abuse material is ...</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#content moderation`, `#AI regulation`, `#generative AI`, `#legal`

---

<a id="item-tech-news-6"></a>
### [Convex skill reportedly uploads app ideas without disclosure](https://github.com/convex/convex-backend-skill/issues/64) ⭐️ 7.0/10

A GitHub issue on the convex-backend-skill repository alleges that Convex&\#x27;s skill plugin sends users&\#x27; app ideas to a remote server without informing them. Convex CEO Jamie responded in the thread, saying the prompt upload powers the Convex &quot;quickstart&quot; feature, which he described as the successor to the recently shut-down Convex Chef vibe-coding product. The source provides no technical details on what data is transmitted, where it is stored, or whether users can opt out, and the claim remains an allegation from the issue rather than an independently verified finding.

hackernews · MickyTheMouse · Nov 27, 18:02 · [Discussion](https://news.ycombinator.com/item?id=50669765)

**「Background」** Convex Chef was an AI app builder that generated full-stack applications on top of Convex&\#x27;s reactive database, and its GitHub repository described it as &quot;the only AI app builder that knows backend.&quot; In the issue thread, Convex CEO Jamie said the company recently shut Chef down and that the prompt upload in the plugin now powers Convex&\#x27;s &quot;quickstart&quot; feature, which he called Chef&\#x27;s &quot;spiritual successor.&quot; That makes the disputed upload part of a successor product rather than the discontinued Chef itself.

**「Why it matters」** Developers using the skill plugin may be sharing proprietary app concepts with Convex&\#x27;s servers without knowing it, which matters for anyone working under confidentiality constraints or evaluating self-hosted alternatives. The thread does not establish whether the upload can be disabled or what retention applies, so users concerned about prompt handling have no confirmed mitigation from the supplied material.

**「Community reaction」** Commenters debated trust in AI tooling: one argued that self-hosted open-weight models are the long-term answer, while another noted that prompt injection is far more common than models making malicious tool calls on their own, without claiming this case was malicious. A separate commenter questioned why the author of an unrelated front-page post was also promoting a personal media page in the issue thread.

<details><summary>References</summary>
<ul>
<li><a href="https://chef.convex.dev/">chef . convex .dev</a></li>
<li><a href="https://github.com/convex/chef">GitHub - convex / chef : The only AI app builder that knows backend</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#ai-tooling`, `#developer-tools`, `#data-handling`, `#open-source`

---

<a id="item-tech-news-7"></a>
### [US Air Force Cloud One platform reportedly breached](https://www.bleepingcomputer.com/news/security/us-air-force-cloud-platform-reportedly-hacked-in-latest-federal-breach/) ⭐️ 7.0/10

Hackers have reportedly breached the US Air Force&\#x27;s Cloud One computing platform, according to BleepingComputer. The report places the incident within a recent wave of cyberattacks said to affect US government agencies, including the FBI, CIA, and Treasury Department. The available account is a brief excerpt that does not identify the attackers, the affected systems or data, or how access was obtained, and the breach is described as reported rather than confirmed. No technical details or official confirmation were provided in the supplied material.

rss · BleepingComputer · Nov 27, 15:09

**「Context」** Cloud One is described in reporting as the Air Force&\#x27;s flagship cloud computing platform, and the reported intrusion was discovered within the past month during upgrade work, according to Reuters reporting cited in secondary coverage. The breach follows reports of other federal compromises, including a CIA database and incidents affecting the FBI, Department of Homeland Security, at least two spy agencies, and the Treasury. The supplied source does not specify the attackers, the data accessed, or whether the intrusion has been contained.

**「Impact」** The reported breach could expose sensitive tactical, personnel, and logistics data hosted on Cloud One, according to people familiar with the matter cited by Reuters. Cloud One consolidates Air Force IT infrastructure across Microsoft, Amazon, Oracle, and Alphabet cloud services, so any compromise could affect dozens of military applications rather than a single system. The Air Force said it continuously takes prudent measures to protect its information, systems, and mission capabilities, but the reported breach remains unverified and no technical details on affected systems or data have been disclosed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/27/hackers-breach-us-air-force-cloud-computing">Hackers reportedly breach US air force ’s flagship cloud computing...</a></li>
<li><a href="https://www.youtube.com/watch?v=JythiSaX7K0">After FBI , CIA , US Air Force Hacked, Who Is Attacking ... - YouTube</a></li>
<li><a href="https://news.sky.com/story/us-air-forces-cloud-computing-platform-hacked-13617163">US Air Force &#x27;s cloud computing platform hacked | Sky News</a></li>
<li><a href="https://southfront.press/hackers-breach-u-s-air-forces-flagship-cloud-network/">Hackers Breach U.S. Air Force ’s Flagship Cloud Network</a></li>
<li><a href="https://nypost.com/2026/11/27/us-news/hackers-breach-us-air-force-flagship-cloud-one-computing-platform/">Hackers breach US Air Force flagship Cloud One computing platform</a></li>
<li><a href="https://www.zerohedge.com/technology/hackers-breach-usafs-critical-cloud-one-platform-insiders-warn-its-big-deal">Hackers Breach USAF&#x27;s Critical Cloud One Platform As... | ZeroHedge</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#cloud-security`, `#government-breach`, `#US-Air-Force`, `#incident-report`

---

<a id="item-tech-news-8"></a>
### [Drupal warns of second critical flaw exploited for site takeover](https://www.bleepingcomputer.com/news/security/drupal-warns-of-new-access-bypass-flaw-exploited-in-attacks/) ⭐️ 7.0/10

Drupal&\#x27;s security team says attackers are actively exploiting a second critical vulnerability that allows them to breach and hijack unpatched websites. The available report does not specify the affected Drupal versions, the technical nature of the flaw, or the mitigations Drupal recommends, so administrators should consult Drupal&\#x27;s official security advisory for those details before acting. The exploitation is described as ongoing, not merely theoretical.

rss · BleepingComputer · Nov 27, 10:10

**「Background」** Drupal&\#x27;s security team had already disclosed a highly critical core vulnerability, SA-CORE-2026-017, on November 18, 2026, warning that the bundled install.php could let an attacker attempt to reinstall Drupal and achieve site takeover or remote code execution; it later reported exploitation on live sites as early as November 19, 2026. A related advisory, SA-CORE-2026-018, covers a gadget chain rated moderately critical \(14/25\) affecting the same versions. The current warning concerns a second critical flaw, but the supplied excerpt does not identify its advisory ID, affected versions, or fix.

<details><summary>References</summary>
<ul>
<li><a href="https://www.drupal.org/security">Security advisories | Drupal.org</a></li>
<li><a href="https://www.drupal.org/sa-core-2026-017">Drupal core - Highly critical - Remote code execution - SA ...</a></li>
<li><a href="https://docs.pantheon.io/release-notes/2026/11/drupal-core-security-release">Drupal core security releases fix a critical remote code ...</a></li>

</ul>
</details>

**Tags**: `#security`, `#drupal`, `#vulnerability`, `#open-source`, `#web`

---

<a id="item-tech-news-9"></a>
### [Hackers Used AI Tool Artex Against CIA and Other US Intelligence Agencies](https://www.forbes.com/sites/the-wiretap/2026/11/25/us-government-under-ai-cyberattack) ⭐️ 7.0/10

The New York Times reported that hackers targeted the CIA, the National Geospatial-Intelligence Agency, and the Office of the Director of National Intelligence, with an AI tool assisting the attack. The tool, called Artex, aggregates multiple open-source AI models to test network and computer defenses; a Chinese developer released it earlier this year and has since deleted it from his GitHub account after it was used in several attacks, including one against the European Union. The reported impact appears limited to non-classified reconnaissance data, and the FBI had earlier warned that cybercriminals and spies were widely using Artex. The account comes from a single Telegram summary of NYT and Forbes reporting, so details remain thin.

telegram · zaihuapd · Nov 27, 10:42

**「Background」** The FBI issued a flash advisory in mid-November 2026 describing ARTEX as an open-source, LLM-driven agentic platform that threat actors have weaponized to automate multiple phases of intrusions, and it warned the tool was used against a U.S. IT company and South Korean financial targets. The current report extends that warning to U.S. intelligence agencies, including the CIA, the National Geospatial-Intelligence Agency, and the Office of the Director of National Intelligence, and says the tool&\#x27;s developer has since removed it from GitHub.

**「Impact」** The reported targeting of non-classified reconnaissance data suggests the intrusion did not reach classified systems, but the FBI&\#x27;s earlier warning indicates Artex is already circulating among criminals and spies. The developer&\#x27;s removal of Artex from GitHub does not necessarily prevent copies from remaining in use.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ic3.gov/CSA/2026/261113.pdf">Threat Overview of ARTEX Autonomous Penetration Testing Framework</a></li>
<li><a href="https://techcrunch.com/2026/11/16/fbi-says-artex-ai-open-source-hacking-tool-used-to-breach-networks-in-under-three-hours/">FBI says Artex AI open source hacking tool used to breach ...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/fbi-warns-artex-ai-hacking-tool-is-powering-global-cyberattacks/">FBI warns ARTEX AI hacking tool is powering global cyberattacks</a></li>

</ul>
</details>

**Tags**: `#AI security`, `#cybersecurity`, `#offensive AI`, `#government`, `#open-source models`

---

<a id="item-tech-news-10"></a>
### [Anthropic 系统卡披露对前沿模型研发请求的隐蔽降级](https://news.ycombinator.com/item?id=50664325) ⭐️ 7.0/10

Anthropic 的 Claude Mythos 5 与 Fable 5 系统卡（今年 6 月发布）写明，针对开发前沿模型的请求会被暗中削弱回答效果，手段包括改写提示、引导向量和参数高效微调。Anthropic 估算这类干预影响约 0.03% 的流量和不到 0.1% 的组织，涉及预训练流水线、分布式训练和加速器设计等任务，多数编码工作不受影响。与安全类拦截不同，用户无法察觉，也不会回退到其他模型。该披露本周因开发者讨论重新受到关注；上述细节来自二手转述，模型名称与版本未在原始材料中核实。

telegram · zaihuapd · Nov 27, 13:42

**「Context」** Anthropic publishes system cards documenting each Claude model&\#x27;s capabilities, safety evaluations, and deployment decisions. The disclosure in question comes from the system cards for Claude Mythos 5 and Fable 5, released in June, which state that Anthropic added interventions limiting Claude&\#x27;s effectiveness on requests targeting frontier LLM development, citing pretraining pipelines, distributed training infrastructure, and ML accelerator design as examples. The item says the cards drew renewed developer attention this week.

**「影响」** 使用 Claude 进行预训练流水线、分布式训练或加速器设计相关工作的开发者，可能收到质量被静默降低的回答，且不会收到拦截提示或模型回退，因此难以判断输出是否被干预。Anthropic 称用 Claude 开发竞品模型本就违反服务条款，这为上述干预提供了政策依据。

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/system-cards">Model system cards \ Anthropic</a></li>
<li><a href="https://ai-digest.liziran.com/en/digest/2026-06-11-anthropic-built-most-capable-model-then-wired-three-ways">Anthropic Built Its Most Capable Model , Then Wired In Three Ways to...</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#model safety`, `#Anthropic`, `#developer trust`, `#LLM`

---

<a id="item-tech-news-11"></a>
### [Minecraft Bedrock resource pack flaw fixed in 26.65](https://www.zaikei.co.jp/article/20261119/878386.html) ⭐️ 7.0/10

A Minecraft Bedrock resource pack flaw let packs containing a content.zipe file modify files in the Ore UI interface framework and run hidden scripts. Add-on developer 8Crafter disclosed the issue on Reddit on November 15, saying it was confirmed in versions 26.52 through 26.63 and that earlier versions may also be affected; it covers PC, mobile, and console, while Java Edition is unaffected. Players joining a server or Realm with automatic resource pack downloads enabled could receive the problematic files without installing anything manually. Mojang fixed the issue in version 26.65.

telegram · zaihuapd · Nov 27, 18:04

**「Background」** Minecraft Bedrock resource packs are user-supplied content bundles that the game can download automatically when a player joins a server or Realm, which is how a malicious pack could reach players without manual installation. According to external reports, add-on developer 8Crafter disclosed the issue on Reddit around November 14–15, 2026, and Mojang released hotfix 26.65 on November 17, 2026, addressing the flaw in the Ore UI interface framework.

**「Impact」** 8Crafter listed possible exploits including deleting all saves, obtaining the player&\#x27;s IP, silently opening arbitrary URIs under certain conditions on Windows, and launching batch files inside the resource pack to download malware. AxmBro released a Windows read-only detection tool that can find content.zipe files but cannot determine whether a resource pack is malicious.

<details><summary>References</summary>
<ul>
<li><a href="https://www.minehour.com/en/blog/minecraft-bedrock-26-65-fixes-flaw-in-resource-packs">Minecraft Bedrock 26.65 fixes flaw in resource packs</a></li>
<li><a href="https://kaimux.com/forum/project/minecraft-insights/minecraft-bedrock-26-65-resource-pack-fix.1063">Minecraft Bedrock 26.65: the resource pack security fix | KAIMUX</a></li>
<li><a href="https://www.techtimes.com/articles/330961/20261117/mojang-patches-bedrock-after-community-discovers-resource-packs-could-execute-malicious-code.htm">Minecraft Bedrock Had a Hidden Malware Flaw - Tech Times</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#minecraft`, `#gaming`, `#resource-packs`

---

<a id="item-tech-news-12"></a>
### [Microsoft to replace some third-party Windows drivers with in-box drivers](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 7.0/10

Microsoft confirmed at Ignite 2026 that it is developing new in-box Windows drivers for entire hardware classes, aiming to reduce third-party code entering the kernel. Printing is the first focus, with the recently introduced Windows Ready Print mode intended to replace legacy third-party print drivers. Windows product manager Mehmet Kucukgoz said SoundWire and SDCA audio drivers will soon become built-in Windows components, while I3C bus, USB Ethernet, and MIPI camera drivers are also in development. Microsoft also introduced a Driver Quality Initiative \(DQI\) at its Windows Hardware Engineering conference to raise driver reliability, quality, and security standards and to encourage third-party developers and OEMs to use built-in drivers where possible.

telegram · zaihuapd · Nov 28, 02:09

**「Background」** Windows device drivers traditionally ship as third-party kernel-mode code supplied by hardware vendors, so a single faulty driver can crash the whole system. Microsoft has framed the in-box driver push as a response to that reliability and attack-surface problem, saying one failed driver can bring down a PC.

**「Impact」** Driver developers and OEMs face pressure to shift custom drivers toward Microsoft&\#x27;s in-box components, and existing third-party print drivers are the first category affected by the Ready Print replacement. The source gives no implementation details, timelines, or migration guidance, so the practical scope of replacement remains unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.windowslatest.com/2026/11/24/microsoft-admits-one-failed-driver-can-bring-down-your-pc-so-its-replacing-the-ones-for-printers-audio-and-cameras-with-its-own-wherever-it-can-on-windows-11-promising-fewer-crashes-and-attack/">Microsoft admits one failed driver can bring down your PC, so ...</a></li>

</ul>
</details>

**Tags**: `#windows`, `#device-drivers`, `#microsoft`, `#kernel-security`, `#hardware`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s State Council Signals Stronger Market-Stabilization Role for Central Huijin](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 8.0/10

At a State Council executive meeting on Nov 27 chaired by Premier Li Qiang, China&\#x27;s government called for stepping up the &quot;national team&\#x27;s&quot; market-stabilization role and optimizing Central Huijin&\#x27;s quasi-&quot;stabilization fund&quot; function, alongside measures to encourage more dividends and buybacks and to guide long-term funds such as insurance, enterprise annuity and social security money into the stock market. The meeting gave no specific figures or implementation timeline.

telegram · zaihuapd · Nov 27, 05:35

**「Background」** Central Huijin is a state-owned investment company that acts as the main vehicle for the &quot;national team&quot; of state funds buying stocks to support prices. An expert quoted by Eastmoney said the meeting&\#x27;s wording signals China&\#x27;s quasi-stabilization-fund mechanism is shifting from crisis response toward a more regular role \(tool-1-2\).

**「Impact」** The directive signals that state-backed buyers such as Central Huijin could play a larger role in supporting share prices, a potential cushion for investors in Chinese equities, though the announcement sets direction rather than concrete funding or rules.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.eastmoney.com/a/202611273941634358.html">如何理解 国 常会对资本 市 场的最新定调？ 专 家 解读来了 _ 东方财富网</a></li>

</ul>
</details>

**Tags**: `#China policy`, `#capital markets`, `#Central Huijin`, `#market stabilization`, `#long-term funds`

---

<a id="item-finance-news-2"></a>
### [央行下调大额存单起购门槛](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 8.0/10

中国人民银行11月27日公布《大额存单管理办法》，将个人投资人认购起点从20万元降至不低于10万元，机构投资人从1000万元降至不低于500万元，两项门槛均减半，自2027年3月21日起施行。

telegram · zaihuapd · Nov 27, 11:36

**「背景」** 新办法同时废止2015年《大额存单管理暂行办法》和2016年第13号公告；同日央行还发布《人民币存贷款利率管理规定》，同样自2027年3月21日起施行，要求金融机构自主确定存贷款利率，不得通过高息揽储等不正当手段吸收存款。

**「影响」** 门槛下调后，资金不足20万元的个人储户也能购买大额存单，而银行在吸收存款时须遵守不得以高息揽储的新规。

**Tags**: `#central bank regulation`, `#deposits`, `#interest rates`, `#China banking`, `#personal finance`

---

<a id="item-finance-news-3"></a>
### [蜜雪冰城投资5亿元入股DeepSeek新一轮融资](https://m.sohu.com/a/1107027659_115479) ⭐️ 7.0/10

据报道，DeepSeek已完成第二轮融资，规模在1000亿至1055亿元之间，投后估值约6155亿元；新增31家出资人中包括蜜雪冰城股份有限公司，其认缴5亿元。该消息来自搜狐网经Telegram转述的报道，尚无官方确认。

telegram · zaihuapd · Nov 27, 06:33

**「Background」** DeepSeek&\#x27;s first round closed in June at a valuation above 3500亿元, raising 500亿元, according to earlier reports \(tool-1-3\). Its second round was reportedly launched in mid-July, paused in late July, and later restarted \(tool-1-2\). The 砺思-managed fund through which 蜜雪冰城 invested, 天津砺思星深, closed at 75.2亿元 with 40 limited partners \(tool-2-1, tool-2-2\).

**「Impact」** The reported round, if confirmed, would rank among China&\#x27;s largest private financings and, per media reports, is intended to pave the way for a DeepSeek IPO. Mixue&\#x27;s 5亿元 commitment is small relative to its 2025 revenue of 335.6亿元, so the stake is unlikely to materially change its own finances.

<details><summary>References</summary>
<ul>
<li><a href="https://post.smzdm.com/p/aom07rr7/">DeepSeek 估 值 5000 亿 重启 融 资 ，自建智算中心并涨价_IT...</a></li>
<li><a href="https://www.php.cn/faq/2947867.html">消息称 DeepSeek 重启 第 二 轮 500 亿 元 融 资 投 前 估 值 升至 5000...</a></li>
<li><a href="https://www.cls.cn/detail/2525279">75 . 2 亿 元 、40名LP， 砺 思 又拿到了DeepSeek投 资 份额</a></li>
<li><a href="https://www.chinaventure.com.cn/news/78-20261108-393950.html">梁文锋攒了一个老乡局 | 投中网</a></li>
<li><a href="https://finance.sina.com.cn/stock/hkstock/ggscyd/2026-10-22/doc-iniwamip5161974.shtml">DeepSeek据报完成约1000亿元人民币融资 宁德时代和腾讯参投</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#AI financing`, `#private markets`, `#corporate investment`, `#China tech`

---

<a id="item-finance-news-4"></a>
### [China&\#x27;s Market Regulator Summons 15 E-Bike Makers Over Quality Violations](https://www.news.cn/20261127/0c8c665ce70c417b9263b39fa8a519f0/c.html?hl=zh-CN) ⭐️ 7.0/10

On November 27, China&\#x27;s State Administration for Market Regulation held a collective regulatory meeting with 15 electric bicycle companies, including Yadea, Tailg, Aima, Ninebot, and Niu, after spot checks found quality-control gaps, weak product-consistency controls, and non-compliant products sold under mandatory national standards. The regulator ordered the companies to rectify the problems, enforce the &quot;one vehicle, one battery, one charger, one code&quot; standard, and immediately recall products confirmed to be defective.

telegram · zaihuapd · Nov 27, 12:06

**「Background」** The meeting followed a full-coverage &quot;flying inspection&quot; of CCC certification, China&\#x27;s mandatory product certification system, which uncovered the violations; the session was a supervisory warning rather than a formal penalty.

**「Impact」** The companies were told not to shift responsibility to buyers, mislead consumers into riding unregistered vehicles, push discounted returns, or refuse returns on the grounds that certification will &quot;soon be restored,&quot; which directly affects owners seeking refunds or recalls.

**Tags**: `#regulation`, `#electric bicycles`, `#consumer safety`, `#China manufacturing`, `#product recalls`

---