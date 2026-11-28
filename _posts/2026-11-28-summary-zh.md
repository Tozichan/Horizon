---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 70 条内容中筛选出 16 条重要资讯。

---

**科技新闻**
1. [OpenSec 披露 Linux nfsd 9.8 分预认证漏洞](#item-tech-news-1) ⭐️ 9.0/10
2. [Cacti 未修补零日漏洞公开 PoC，可远程执行代码](#item-tech-news-2) ⭐️ 8.0/10
3. [谷歌 DeepCrossAttention 称模型质量相当、速度最高提升 3 倍](#item-tech-news-3) ⭐️ 7.0/10
4. [WebRTC 信用卡盗刷脚本现身热门购物网站](#item-tech-news-4) ⭐️ 7.0/10
5. [多州总检察长起诉 SpaceX，要求阻止 Grok 生成儿童性虐待与报复性色情图像](#item-tech-news-5) ⭐️ 7.0/10
6. [Convex 技能插件被指未经告知上传用户应用创意](#item-tech-news-6) ⭐️ 7.0/10
7. [美空军 Cloud One 云平台据报遭入侵](#item-tech-news-7) ⭐️ 7.0/10
8. [Drupal 警告新漏洞可致网站被接管并已被利用](#item-tech-news-8) ⭐️ 7.0/10
9. [黑客借 AI 工具 Artex 攻击 CIA 等美国情报机构](#item-tech-news-9) ⭐️ 7.0/10
10. [Anthropic 系统卡披露暗中削弱模型研发请求，约占 0.03% 流量](#item-tech-news-10) ⭐️ 7.0/10
11. [《我的世界》基岩版资源包漏洞影响 26.52 至 26.63，26.65 已修复](#item-tech-news-11) ⭐️ 7.0/10
12. [微软拟以 Windows 内置驱动取代部分第三方驱动](#item-tech-news-12) ⭐️ 7.0/10

**财经新闻**
1. [国常会部署稳市：优化中央汇金类“平准基金”功能](#item-finance-news-1) ⭐️ 8.0/10
2. [央行下调大额存单起购门槛：个人降至 10 万元](#item-finance-news-2) ⭐️ 8.0/10
3. [蜜雪冰城 5 亿元入股 DeepSeek 新一轮融资](#item-finance-news-3) ⭐️ 7.0/10
4. [市场监管总局约谈雅迪、台铃、爱玛等 15 家电动自行车企业](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenSec 披露 Linux nfsd 9.8 分预认证漏洞](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec 披露了 Linux 内核 NFS 服务器 nfsd 的预认证堆溢出漏洞 CVE-2026-99362，CVSS 评分 9.8。攻击者无需登录，只需向 tcp/2049 发送一条连接即可越界写入内核堆，进而获得 root shell。该漏洞自 2014 年的 Linux 3.16 起存在，影响启用 NFSv4.1 或 4.2 的主机，波及文件服务器、NAS 和集群存储节点。修复已在 6.12.117、6.18.61、7.3.2 和 7.4-rc1 中发布，需升级内核并重启；无法立即升级的环境可通过防火墙限制 tcp/2049 访问。CVE 于 2026 年 11 月 20 日公开。

telegram · zaihuapd · 11月27日 12:57

**「背景」** 该漏洞位于 Linux 内核 nfsd 的 NFSv4.1/4.2 会话回复缓存中，攻击者可在任何认证之前通过构造 COMPOUND 请求触发堆越界写（CWE-787），因此只要主机可达 TCP 2049 端口即暴露风险。外部漏洞记录显示，CVE-2026-99362 于 2026 年 11 月 19 日发布，内核 CNA 给出 9.8 分、Red Hat 给出 9.4 分；Red Hat 同时指出其默认配置不启用内核 nfsd，攻击面因此受限。

**「影响与处置」** 运行启用 NFSv4.1 或 4.2 的 nfsd 的文件服务器、NAS 和集群存储节点均受影响，且攻击无需任何凭据。管理员应升级到 6.12.117、6.18.61、7.3.2 或 7.4-rc1 并重启内核；暂时无法升级时，应通过防火墙限制对 tcp/2049 的访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://computingforgeeks.com/nfs2root-cve-2026-99362/">NFS2ROOT (CVE-2026-99362): Check, Patch, Mitigate ...</a></li>
<li><a href="https://app.opencve.io/cve/CVE-2026-99362">CVE-2026-99362 - Vulnerability Details - OpenCVE</a></li>

</ul>
</details>

**标签**: `#linux-kernel`, `#security-vulnerability`, `#nfs`, `#remote-exploit`, `#kernel-patching`

---

<a id="item-tech-news-2"></a>
### [Cacti 未修补零日漏洞公开 PoC，可远程执行代码](https://www.bleepingcomputer.com/news/security/unpatched-cacti-zero-day-with-public-poc-gives-remote-code-execution/) ⭐️ 8.0/10

Cacti 网络监控平台存在一个尚未修补的零日漏洞，并已有公开的概念验证（PoC）利用代码。该漏洞允许未认证攻击者在受影响的服务器上执行命令，即未认证远程代码执行。目前披露信息未说明受影响版本、根本原因或缓解措施，也尚无官方补丁。

rss · BleepingComputer · 11月27日 17:06

**「背景」** Cacti 是开源的网络性能与故障监控框架，此前已出现过未认证漏洞：据 Ionix 威胁中心记录，CVE-2026-39938 为影响 1.2.30 及之前所有版本的未认证本地文件包含漏洞（CVSS 9.8），可远程利用且无需凭据或用户交互。本次公开的零日 PoC 则针对 Cacti 1.2.31，在启用访客访问（guest access）时可实现未认证命令执行，截至 11 月尚无补丁或 CVE 编号。

**「影响与应对」** 运行 Cacti 的监控服务器若暴露在可被攻击者访问的网络中，可能面临未认证的远程命令执行风险。由于补丁尚未发布，管理员需关注官方后续公告，并考虑限制 Cacti 实例的网络暴露面作为临时缓解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ionix.io/threat-center/cve-2026-39938/">CVE-2026-39938 – Unauthenticated LFI / Remote Code Execution ...</a></li>
<li><a href="https://windowsforum.com/news/cacti-4http2shell-zero-day-poc-enables-rce-via-guest-access-mitigation-guide.454357/">Cacti 4HTTP2SHELL Zero-Day PoC Enables RCE via Guest Access ...</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#cacti`, `#remote-code-execution`, `#open-source`

---

<a id="item-tech-news-3"></a>
### [谷歌 DeepCrossAttention 称模型质量相当、速度最高提升 3 倍](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 7.0/10

谷歌研究团队发布博客文章《Supercharging Transformer Residual Connections》，介绍一种名为 DeepCrossAttention 的 Transformer 残差连接方法，声称在模型质量相当的情况下最高可快 3 倍。该说法来自谷歌研究自身的博客表述，所给材料未包含基准测试方法、具体模型规模或独立验证，因此速度提升幅度目前仍属厂商主张而非已证实结果。

hackernews · ComputedCamp995 · 11月27日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50672565)

**「背景」** DeepCrossAttention（DCA）由 Google 研究人员提出，相关论文已发表于 ICML 2025，作者包括 M. Heddes、A. Javanmard、K. Axiotis 等人。该工作针对传统残差连接“简单相加各层输出、可能稀释关键信息”的问题，改用带可学习权重的路由方式增强 transformer 的残差学习。Google Research 博客于 2026 年 11 月 23 日发布了这一方法的介绍。

**「对实践者的影响」** 若该结论在复现中成立，关注训练或推理效率的 Transformer 开发者可能需要评估将残差连接替换为 DeepCrossAttention 的可行性；但在缺少基准细节和第三方验证前，不宜据此调整生产配置。

**「社区讨论」** 有评论者批评博客图表使用折线图连接不同方法，认为这些方法之间没有时间或其他连续关系，应改用柱状图。另有评论者追问该方法能否与 MTP、Dflash 等已有加速手段叠加，并提到 Densenet 的相似思路，但这些均为个人观点与疑问，未提供验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections</a></li>
<li><a href="https://arxiv.org/html/2502.06785">DeepCrossAttention : Supercharging Transformer Residual ...</a></li>
<li><a href="https://scholar.google.com/citations?user=SZpFJqIAAAAJ&amp;hl=en">Google - Cited by 399 - Machine Learning - Data Mining - Algorithms</a></li>

</ul>
</details>

**标签**: `#transformers`, `#deep-learning`, `#model-efficiency`, `#google-research`, `#attention-mechanisms`

---

<a id="item-tech-news-4"></a>
### [WebRTC 信用卡盗刷脚本现身热门购物网站](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

InfoHawk 于 11 月 27 日发布报告称，在热门购物网站上发现了利用 WebRTC 的信用卡盗刷（skimming）脚本。报告将这一活动与黑色星期五购物季联系起来，但现有材料未提供受影响网站名单、脚本样本数量或已确认的受害者数据。评论者指出，WebRTC 本身并非关键，它只是较少被监控，同样的手法用普通 HTTP 请求也能实现。

hackernews · scanr · 11月27日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50668145)

**「背景」** 网页盗刷（web skimming，常以 Magecart 之名归类）指攻击者在电商结账页面注入恶意脚本，在用户输入时窃取银行卡数据。2026 年 1 月已有报道称，一轮 Magecart 活动针对与 AmEx、Diners Club、Mastercard 等主要支付网络相关的在线结账页面窃取卡数据。此次报道的不同之处在于，被注入的脚本借助 WebRTC 传输数据，而非此前更常见的 HTTP 请求方式。

**「影响与应对」** 对电商站点而言，风险主要来自页面嵌入的第三方脚本：评论者 afavour 认为，只要站点引入第三方脚本就始终存在被注入的风险，因此站点方需要审计并限制第三方脚本的加载范围。对用户而言，广告与脚本拦截被视为降低暴露面的手段之一，但这只是缓解措施，并不能替代站点侧的脚本管控。

**「社区讨论」** 评论者 afavour 认为，问题与 WebRTC 的技术能力无关，而是它较少被监控，攻击者只针对移动设备也是因为更难检测；jszymborski 则以此作为不为此感到愧疚地拦截广告的理由。另有评论者 snickerer 主张浏览器不应允许陌生代码在本地执行，s\_u\_d\_o 建议广告提供商对广告做沙箱隔离、禁止客户端执行 JS，\_\_MatrixMan\_\_ 则质疑支付为何仍依赖对称密钥。这些均为个人观点，并非已证实的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aviatrix.ai/threat-research-center/web-skimming-campaign-magecart-2026/">2026 Magecart Web Skimming Campaign Compromises Payment Data</a></li>
<li><a href="https://www.malwarebytes.com/blog/news/2026/01/online-shoppers-at-risk-as-magecart-skimming-hits-major-payment-networks">Online shoppers at risk as Magecart skimming hits major ...</a></li>

</ul>
</details>

**标签**: `#web security`, `#credit card skimming`, `#WebRTC`, `#third-party scripts`, `#e-commerce`

---

<a id="item-tech-news-5"></a>
### [多州总检察长起诉 SpaceX，要求阻止 Grok 生成儿童性虐待与报复性色情图像](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 7.0/10

弗吉尼亚州总检察长 Jay Jones 与另一州总检察长 Rayfield 联合对 SpaceX 提起诉讼，指控其旗下 xAI 的 Grok 生成儿童性剥削图像和非自愿私密图像。诉状将 SpaceX 列为 xAI 与 X 的母公司，要求法院制止相关图像生成行为。目前公开信息仅来自州总检察长办公室的新闻稿，诉讼的具体诉求、涉及州数量及法院受理进展尚未在现有材料中说明。

hackernews · DeepLogin · 11月27日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=50670855)

**「背景」** 弗吉尼亚州总检察长 Jay Jones 与俄勒冈州总检察长 Dan Rayfield 于本周一（据 CNBC 报道为 11 月 23 日）对 SpaceX 及其子公司 xAI、X 提起消费者保护诉讼，指控其就数据安全误导公众，并借 Grok 的“spicy mode”生成和传播非自愿性化图像牟利。两州寻求民事罚款和禁令，要求停止 Grok 与 X 生成、分发此类图像。

**「对平台与用户的影响」** 该诉讼针对的是 SpaceX 作为 xAI 母公司的责任，而非 Grok 用户个人；若法院受理并推进，可能迫使平台在图像生成环节增加年龄与同意核验等限制。外部报道显示，2026 年 8 月第七巡回上诉法院曾依据 Ashcroft v. Free Speech Coalition 判例裁定，不涉及真实儿童的 AI 生成儿童性虐待材料受第一修正案保护，这使本案中针对生成内容的诉求面临宪法层面的不确定性；涉及真实人物的非自愿私密图像则不在该保护范围内。

**「社区讨论」** 有评论者质疑 Grok 此前是否已被各平台广泛禁止生成此类内容，并追问用户是否需要刻意“诱导”才能触发。另有评论者认为应追究实际生成图像的人，而非仅起诉公司。还有评论者提出，最高法院已裁定个人使用 AI 制作儿童性虐待材料属于受保护言论，但该豁免不适用于描绘真实儿童的情形，其对报复性色情的适用性则存疑；上述法律解读均为评论者个人说法，未经本条目核实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.oag.state.va.us/media-center/news-releases/jay-jones/3164-media-clips-attorney-general-jay-jones-holds-x-accountable-for-child-exploitation-and-non-consensual-images">MEDIA CLIPS: Attorney General Jay Jones Holds X Accountable ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/23/oregon-virginia-spacex-grok-deepfake-lawsuits.html">SpaceX sued by 2 states over AI deepfake porn, Grok ... - CNBC</a></li>
<li><a href="https://billygraham.org/decision-magazine/articles/federal-court-says-ai-child-sex-abuse-images-are-constitutionally-protected">Court Says AI Child Sex Abuse Images Are Constitutionally ...</a></li>
<li><a href="https://www.foxnews.com/politics/appeals-court-delivers-unsettling-ruling-supreme-court-left-no-choice">AI-generated CSAM possession protected by First Amendment ...</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#content moderation`, `#AI regulation`, `#generative AI`, `#legal`

---

<a id="item-tech-news-6"></a>
### [Convex 技能插件被指未经告知上传用户应用创意](https://github.com/convex/convex-backend-skill/issues/64) ⭐️ 7.0/10

一名用户在 Convex 的 GitHub 仓库提交 issue，指控其技能插件在未告知用户的情况下，将用户的应用创意发送到远程服务器。Convex CEO Jamie 在评论中回应称，该插件中的提示词上传功能用于支撑 Convex 的“quickstart”功能，是已关闭的端到端 vibe-coding 产品 Convex Chef 的继任者，用于引导项目初始化。目前该指控主要来自 issue 提交者，具体上传范围与用户告知机制尚未有独立核实。

hackernews · MickyTheMouse · 11月27日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50669765)

**「背景」** Convex 是一个用于构建和托管软件的全栈平台，提供数据与代码托管以及供开发者构建应用或驱动应用内功能的 AI 网关。据 Convex CEO 在讨论中说明，该插件中的提示词上传功能服务于 Convex 的“quickstart”特性，而这一特性是已关闭的端到端 AI 应用生成产品 Convex Chef 的继任者。

**「影响」** 使用该技能插件的开发者需要留意：其输入的应用描述可能被发送至 Convex 服务器，而现有信息未说明是否提供明确告知或选择退出机制。在 Convex 公布具体的数据处理说明前，涉及敏感或未公开创意的开发者应谨慎使用该功能。

**「社区讨论」** 有评论者认为长期来看自托管开放权重模型更可靠；也有人指出提示词注入比模型自主发起恶意工具调用更常见，但未认定此次事件属于恶意行为。另有评论将讨论引向对 AI 工具信任与数据处理的关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://chef.convex.dev/">chef . convex .dev</a></li>
<li><a href="https://github.com/convex/chef">GitHub - convex / chef : The only AI app builder that knows backend</a></li>

</ul>
</details>

**标签**: `#privacy`, `#ai-tooling`, `#developer-tools`, `#data-handling`, `#open-source`

---

<a id="item-tech-news-7"></a>
### [美空军 Cloud One 云平台据报遭入侵](https://www.bleepingcomputer.com/news/security/us-air-force-cloud-platform-reportedly-hacked-in-latest-federal-breach/) ⭐️ 7.0/10

据 BleepingComputer 报道，黑客据称入侵了美国空军的 Cloud One 计算平台。报道称，这起事件是近期针对美国政府机构的一系列网络攻击的一部分，涉及联邦调查局、中央情报局和财政部。目前报道仅给出简短摘要，未披露攻击手法、入侵时间、受影响系统范围或数据损失等具体技术细节，且事件仍以“据报”表述，尚未得到独立证实。

rss · BleepingComputer · 11月27日 15:09

**「背景」** 据《卫报》和天空新闻援引知情人士的报道，此次入侵发生在近期的升级工作期间，并已对 Cloud One 平台造成干扰；该平台承载敏感的战术、人事和后勤数据。这些报道还称，此次事件是近期针对美国联邦机构的一系列网络事件之一，此前已有 FBI、CIA、国土安全部和财政部等机构受影响。

**「潜在影响」** 据路透社援引三名知情人士报道，此次入侵可能危及 Cloud One 上大量敏感的战术、人事和后勤数据；消息人士将该平台描述为美军最大的云平台之一，并称此次泄露“非常严重”。由于报道仍使用“据称”措辞，且美国空军仅表示会持续采取保护措施，尚未确认具体受影响系统或数据范围，相关用户和依赖该平台的应用方目前无法据此判断自身暴露程度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/27/hackers-breach-us-air-force-cloud-computing">Hackers reportedly breach US air force ’s flagship cloud computing...</a></li>
<li><a href="https://www.youtube.com/watch?v=JythiSaX7K0">After FBI , CIA , US Air Force Hacked, Who Is Attacking ... - YouTube</a></li>
<li><a href="https://news.sky.com/story/us-air-forces-cloud-computing-platform-hacked-13617163">US Air Force &#x27;s cloud computing platform hacked | Sky News</a></li>
<li><a href="https://nypost.com/2026/11/27/us-news/hackers-breach-us-air-force-flagship-cloud-one-computing-platform/">Hackers breach US Air Force flagship Cloud One computing platform</a></li>
<li><a href="https://www.zerohedge.com/technology/hackers-breach-usafs-critical-cloud-one-platform-insiders-warn-its-big-deal">Hackers Breach USAF&#x27;s Critical Cloud One Platform As... | ZeroHedge</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#cloud-security`, `#government-breach`, `#US-Air-Force`, `#incident-report`

---

<a id="item-tech-news-8"></a>
### [Drupal 警告新漏洞可致网站被接管并已被利用](https://www.bleepingcomputer.com/news/security/drupal-warns-of-new-access-bypass-flaw-exploited-in-attacks/) ⭐️ 7.0/10

Drupal 安全团队警告称，攻击者正在利用一个可让未修补网站被入侵并接管的第二个严重漏洞。该警告由 BleepingComputer 于 2026 年 11 月 27 日报道，但现有信息仅为简短摘要，未披露漏洞的技术细节、受影响版本或缓解措施。报道未说明该漏洞是否已有官方补丁，也未给出独立验证的利用规模。

rss · BleepingComputer · 11月27日 10:10

**「背景」** Drupal 安全团队此前已发布 SA-CORE-2026-017，指出核心自带的 install.php 安装程序在特定条件下可被用于尝试重新安装 Drupal，进而导致站点接管或远程代码执行；该公告称最早在 2026 年 11 月 19 日 19:00 UTC 已收到在运行站点上被利用的报告。同一批修复还涉及被评为中等严重（14/25）的 SA-CORE-2026-018 组件链问题，影响相同版本。此次报道的是继上述漏洞之后出现的第二个正被积极利用的严重漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.drupal.org/security">Security advisories | Drupal.org</a></li>
<li><a href="https://www.drupal.org/sa-core-2026-017">Drupal core - Highly critical - Remote code execution - SA ...</a></li>
<li><a href="https://docs.pantheon.io/release-notes/2026/11/drupal-core-security-release">Drupal core security releases fix a critical remote code ...</a></li>

</ul>
</details>

**标签**: `#security`, `#drupal`, `#vulnerability`, `#open-source`, `#web`

---

<a id="item-tech-news-9"></a>
### [黑客借 AI 工具 Artex 攻击 CIA 等美国情报机构](https://www.forbes.com/sites/the-wiretap/2026/11/25/us-government-under-ai-cyberattack) ⭐️ 7.0/10

《纽约时报》报道称，黑客攻击了美国中央情报局、国家地理空间情报局和国家情报总监办公室，攻击过程中使用了名为 Artex 的 AI 工具。Artex 可整合多个开源 AI 模型来测试网络和计算机防御；一名中国开发者今年早些时候发布了该工具，此后它被用于多起攻击，包括针对欧盟的一起，该开发者已将其从自己的 GitHub 账号删除。报道称此次攻击看起来不算严重，影响的是非机密侦察数据；今年早些时候 FBI 曾警告，网络罪犯和间谍正在广泛使用 Artex。上述信息来自单一来源的转述，细节有限。

telegram · zaihuapd · 11月27日 10:42

**「背景」** 美国联邦调查局（FBI）此前已就 Artex 发出警告：这是一个开源、由大语言模型驱动的自主渗透测试框架，威胁行为者将其武器化，用于自动化网络入侵的多个阶段。据 TechCrunch 和 BleepingComputer 报道，FBI 在 2026 年 11 月中旬表示，该工具曾被用于攻击一家美国 IT 巨头和韩国金融业，并在不到三小时内攻破网络。

**「影响与关注点」** 对防御方而言，Artex 这类整合多个开源模型的工具降低了发起网络探测的门槛，安全团队需要把针对 AI 辅助侦察的检测纳入防护范围。报道同时指出，此次事件的影响限于非机密侦察数据，尚未显示机密系统受损。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ic3.gov/CSA/2026/261113.pdf">Threat Overview of ARTEX Autonomous Penetration Testing Framework</a></li>
<li><a href="https://techcrunch.com/2026/11/16/fbi-says-artex-ai-open-source-hacking-tool-used-to-breach-networks-in-under-three-hours/">FBI says Artex AI open source hacking tool used to breach ...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/fbi-warns-artex-ai-hacking-tool-is-powering-global-cyberattacks/">FBI warns ARTEX AI hacking tool is powering global cyberattacks</a></li>

</ul>
</details>

**标签**: `#AI security`, `#cybersecurity`, `#offensive AI`, `#government`, `#open-source models`

---

<a id="item-tech-news-10"></a>
### [Anthropic 系统卡披露暗中削弱模型研发请求，约占 0.03% 流量](https://news.ycombinator.com/item?id=50664325) ⭐️ 7.0/10

Anthropic 在 6 月发布的 Claude Mythos 5 与 Fable 5 系统卡中写明，对于旨在开发前沿大模型的请求，Claude 会暗中降低回答质量，手段包括改写提示、引导向量和参数高效微调。这类干预不会像安全类拦截那样回退到其他模型，用户无法察觉。Anthropic 估算其影响约 0.03% 的流量、不到 0.1% 的组织，涉及预训练流水线、分布式训练和加速器设计等任务，多数编码工作不受影响。该披露本周因开发者讨论重新受到关注；上述信息来自 Telegram 对 Hacker News 讨论的转述，具体模型版本等细节未在现有材料中独立核实。

telegram · zaihuapd · 11月27日 13:42

**「背景」** Anthropic 通过系统卡（system card）记录 Claude 模型的能力、安全评估与部署决策，这类文档是其发布流程的一部分。据 2026 年 6 月的一篇报道，相关模型卡已写明 Anthropic 加入了限制 Claude 在“面向前沿大模型开发”的请求上发挥效果的干预措施，并列举预训练流水线、分布式训练基础设施和机器学习加速器设计为例。本次讨论重新聚焦的正是这份既有披露，而非新增的干预措施。

**「对开发者的影响」** 使用 Claude 开发竞品模型本就违反 Anthropic 服务条款，而系统卡披露的机制意味着相关请求不会收到明确拒绝，而是得到被静默削弱的回答。依赖 Claude 进行训练基础设施或加速器设计工作的开发者，可能难以判断输出质量下降是自身问题还是平台干预所致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/system-cards">Model system cards \ Anthropic</a></li>
<li><a href="https://ai-digest.liziran.com/en/digest/2026-06-11-anthropic-built-most-capable-model-then-wired-three-ways">Anthropic Built Its Most Capable Model , Then Wired In Three Ways to...</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#model safety`, `#Anthropic`, `#developer trust`, `#LLM`

---

<a id="item-tech-news-11"></a>
### [《我的世界》基岩版资源包漏洞影响 26.52 至 26.63，26.65 已修复](https://www.zaikei.co.jp/article/20261119/878386.html) ⭐️ 7.0/10

《我的世界》基岩版存在资源包漏洞：带有 content.zipe 文件的资源包可以改动游戏界面框架 Ore UI 的文件并运行隐藏脚本。附加组件开发者 8Crafter 于 11 月 15 日在 Reddit 公开该问题，称已确认影响 26.52 至 26.63 版本，更早版本也可能受影响，覆盖 PC、手机和主机，Java 版不受影响。玩家加入服务器或 Realm 时若开启资源包自动下载，无需手动安装就可能收到问题文件；8Crafter 列举的利用方式包括删除全部存档、获取玩家 IP，在 Windows 上特定条件下还能无提示打开任意 URI，并启动资源包内的批处理文件下载恶意软件。Mojang 已在 26.65 版修复该问题。

telegram · zaihuapd · 11月27日 18:04

**「背景」** 该漏洞由附加组件开发者 8Crafter 于 11 月 15 日在 Reddit 公开，据外部报道，Mojang 随后在 11 月 17 日发布基岩版热修复 26.65 修复此问题。问题根源在于名为 content.zipe 的文件可获取对 Ore UI 的写入权限，而 Ore UI 是驱动基岩版几乎所有菜单界面的 TypeScript 与 React 界面框架。

**「影响与应对」** 使用 26.52 至 26.63 版本基岩版的玩家，尤其是开启服务器或 Realm 资源包自动下载的用户，应升级到 26.65 或更高版本。AxmBro 发布的 Windows 只读检测工具可以查找资源包中的 content.zipe 文件，但无法判定资源包是否恶意，因此不能替代版本升级。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.minehour.com/en/blog/minecraft-bedrock-26-65-fixes-flaw-in-resource-packs">Minecraft Bedrock 26.65 fixes flaw in resource packs</a></li>
<li><a href="https://kaimux.com/forum/project/minecraft-insights/minecraft-bedrock-26-65-resource-pack-fix.1063">Minecraft Bedrock 26.65: the resource pack security fix | KAIMUX</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#minecraft`, `#gaming`, `#resource-packs`

---

<a id="item-tech-news-12"></a>
### [微软拟以 Windows 内置驱动取代部分第三方驱动](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 7.0/10

微软在 Ignite 2026 大会上确认，正在为整类硬件开发新的 Windows 内置驱动，以减少进入系统内核的第三方代码。打印机是首批重点，近期推出的 Windows Ready Print 模式用于取代旧式第三方打印驱动。Windows 产品经理 Mehmet Kucukgoz 表示，SoundWire、SDCA 等音频类驱动将很快成为 Windows 内置组件，I3C 总线、USB 以太网和 MIPI 摄像头类驱动也在开发中。微软同时推出驱动质量倡议（DQI），提升驱动可靠性、质量和安全标准，并鼓励第三方开发者及 OEM 尽量采用内置驱动。

telegram · zaihuapd · 11月28日 02:09

**「背景」** 微软将这一调整与驱动稳定性问题直接挂钩：据其说法，单个驱动故障就可能导致整台 PC 崩溃，因此计划尽可能用自家驱动替换打印机、音频和摄像头等类别的第三方驱动，以减少崩溃和攻击面。此次 Ignite 2026 的确认延续了这一方向，并把范围扩展到 I3C 总线、USB 以太网和 MIPI 摄像头等更多硬件类别。

**「影响」** 对驱动开发者和 OEM 而言，这一方向意味着部分定制驱动可能被系统内置功能替代，其定制驱动也需符合 DQI 的质量与安全要求。不过报道未披露各驱动类别的具体时间表和迁移方式，相关影响仍待微软进一步说明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.windowslatest.com/2026/11/24/microsoft-admits-one-failed-driver-can-bring-down-your-pc-so-its-replacing-the-ones-for-printers-audio-and-cameras-with-its-own-wherever-it-can-on-windows-11-promising-fewer-crashes-and-attack/">Microsoft admits one failed driver can bring down your PC, so ...</a></li>
<li><a href="https://finance.biggo.com/news/780e9526-5af6-4c4b-8b8d-f810046e41fa">Microsoft Looks to Replace Most Third-Party Drivers With ...</a></li>

</ul>
</details>

**标签**: `#windows`, `#device-drivers`, `#microsoft`, `#kernel-security`, `#hardware`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [国常会部署稳市：优化中央汇金类“平准基金”功能](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 8.0/10

国务院常务会议 11 月 27 日提出，加力发挥“国家队”稳市作用，进一步优化中央汇金公司的类“平准基金”功能，并提供充足流动性保障；会议同时要求推动上市公司加大分红回购力度，完善保险、企业年金、社保基金等中长期资金入市支持引导政策。

telegram · zaihuapd · 11月27日 05:35

**「背景」** 中央汇金公司是国有独资投资机构，长期在股市异常波动时增持银行股和交易型开放式指数基金（ETF）以稳定市场，因此被市场称为“国家队”主力。此次国常会提出优化其类“平准基金”功能，有专家解读为这一机制正从危机应对转向常态化安排。

**「影响」** 若相关部署落地，保险资金、企业年金和社保基金等中长期资金入市渠道有望获得更多政策引导，上市公司股东则可能因分红回购要求加强而受到影响；目前会议仅提出方向，未公布具体规模或实施时间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.eastmoney.com/a/202611273941634358.html">如何理解 国 常会对资本 市 场的最新定调？ 专 家 解读来了 _ 东方财富网</a></li>

</ul>
</details>

**标签**: `#China policy`, `#capital markets`, `#Central Huijin`, `#market stabilization`, `#long-term funds`

---

<a id="item-finance-news-2"></a>
### [央行下调大额存单起购门槛：个人降至 10 万元](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 8.0/10

中国人民银行 11 月 27 日公布《大额存单管理办法》，将个人投资人认购起点从原来的 20 万元下调至不低于 10 万元，机构投资人从 1000 万元下调至不低于 500 万元，新规自 2027 年 3 月 21 日起施行。

telegram · zaihuapd · 11月27日 11:36

**「背景」** 大额存单是银行面向个人和机构发行、利率通常高于普通定期存款的存款凭证；此前执行的 2015 年暂行办法规定个人起点 20 万元、机构起点 1000 万元，此次两个门槛均下调一半，同时废止 2015 年办法和 2016 年第 13 号公告。

**「影响」** 门槛降低后，资金在 10 万元以上的个人储户可参与此前需 20 万元才能购买的大额存单；同日发布的《人民币存贷款利率管理规定》要求金融机构自主确定存贷款利率、不得以高息揽储等不正当手段吸收存款，两项规定均自 2027 年 3 月 21 日起施行。

**标签**: `#central bank regulation`, `#deposits`, `#interest rates`, `#China banking`, `#personal finance`

---

<a id="item-finance-news-3"></a>
### [蜜雪冰城 5 亿元入股 DeepSeek 新一轮融资](https://m.sohu.com/a/1107027659_115479) ⭐️ 7.0/10

据报道，DeepSeek 已完成第二轮融资，规模在 1000 亿至 1055 亿元之间，投后估值约 6155 亿元；新增 31 家出资人，蜜雪冰城股份有限公司认缴 5 亿元，该笔资金经砺思资本管理的天津砺思星深基金投入。上述数字来自搜狐网报道，尚未见 DeepSeek 或蜜雪冰城官方确认。

telegram · zaihuapd · 11月27日 06:33

**「背景」** 据此前报道，DeepSeek 首轮融资于今年 4 月启动、6 月完成交割，以超 3500 亿元估值募资 500 亿元；第二轮融资 7 月中旬启动后曾于 7 月底暂停，后重启。蜜雪冰城此次 5 亿元通过砺思资本管理的天津砺思星深基金投入，该基金 11 月初完成 75.2 亿元募集，共有 40 名有限合伙人参与。

**「影响」** 若融资消息属实，蜜雪冰城将以 5 亿元、通过砺思资本管理的基金间接持有 DeepSeek 少数股权，其风险敞口相对蜜雪 2025 年 335.6 亿元营收和约 58.9 亿元归母净利较为有限。该交易目前仅见于媒体报道，尚未获公司或 DeepSeek 官方确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://post.smzdm.com/p/aom07rr7/">DeepSeek 估 值 5000 亿 重启 融 资 ，自建智算中心并涨价_IT...</a></li>
<li><a href="https://www.php.cn/faq/2947867.html">消息称 DeepSeek 重启 第 二 轮 500 亿 元 融 资 投 前 估 值 升至 5000...</a></li>
<li><a href="https://www.chinaventure.com.cn/news/78-20261108-393950.html">梁文锋攒了一个老乡局 | 投中网</a></li>
<li><a href="https://finance.sina.com.cn/stock/hkstock/ggscyd/2026-10-22/doc-iniwamip5161974.shtml">DeepSeek据报完成约1000亿元人民币融资 宁德时代和腾讯参投</a></li>
<li><a href="https://www.sohu.com/a/1095692217_128469">DeepSeek融资1055亿，投后估值6155亿！_中国电信_模型_投资方</a></li>
<li><a href="https://finance.sina.com.cn/roll/2026-10-30/doc-iniwyncw5551924.shtml">DeepSeek 投资人曝光：腾讯、宁德时代、长鑫、中芯国际、vivo、美团、...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI financing`, `#private markets`, `#corporate investment`, `#China tech`

---

<a id="item-finance-news-4"></a>
### [市场监管总局约谈雅迪、台铃、爱玛等 15 家电动自行车企业](https://www.news.cn/20261127/0c8c665ce70c417b9263b39fa8a519f0/c.html?hl=zh-CN) ⭐️ 7.0/10

11 月 27 日，国家市场监管总局集中约谈雅迪、台铃、爱玛、九号、小牛等 15 家电动自行车企业。监管人员在 CCC 认证全覆盖飞行检查中发现，部分企业存在质量保证能力欠缺、产品一致性管控不严、违反强制性国家标准出厂销售不合格产品等问题，约谈要求企业限期整改并召回确认存在缺陷的产品。

telegram · zaihuapd · 11月27日 12:06

**「背景」** CCC 认证是中国强制性产品认证制度，电动自行车须通过该认证方可出厂销售；此次约谈源于监管部门对该认证开展的突击式全覆盖检查。

**「影响」** 被约谈企业须执行“一车一池一充一码”规定，并在售后环节不得推诿责任、误导消费者无牌上路，或以“证书很快恢复”为由拒绝退车，这直接关系到已购车消费者的退换和召回权益。

**标签**: `#regulation`, `#electric bicycles`, `#consumer safety`, `#China manufacturing`, `#product recalls`

---