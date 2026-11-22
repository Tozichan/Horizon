---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 42 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [黎曼猜想 Lean 形式化证明获社区认证](#item-tech-news-1) ⭐️ 10.0/10
2. [微软发布 RDMA over USB4 开发者预览，多台 PC 可合跑一个本地 AI 模型](#item-tech-news-2) ⭐️ 8.0/10
3. [OpenRouter 警告 MiniMax 模型提示词疑遭第三方读取](#item-tech-news-3) ⭐️ 8.0/10
4. [浙江大学在超导芯片上首次真机实现 QRAM](#item-tech-news-4) ⭐️ 8.0/10
5. [胰腺癌口服药 daraxonrasib 一线早期数据：确认缓解率 60.7%](#item-tech-news-5) ⭐️ 8.0/10
6. [显示器内置 USB 网卡为何把下载速度砍掉 75%](#item-tech-news-6) ⭐️ 7.0/10
7. [FBI 与 USDA 据报遭黑客入侵，FBI 目标为 NCIC 数据库](#item-tech-news-7) ⭐️ 7.0/10
8. [微软 Entra Connect Health 漏洞遭利用，租户数据被窃](#item-tech-news-8) ⭐️ 7.0/10
9. [特斯拉海外推送 FSD v15，新增 Reality View 可视化界面](#item-tech-news-9) ⭐️ 7.0/10

**财经新闻**
1. [特朗普提议对海外建 AI 数据中心的美国公司征“巨额税款”](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [黎曼猜想 Lean 形式化证明获社区认证](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 10.0/10

据 Telegram 转发消息，Levent Alpöge 于 2026 年 11 月 20 日发布黎曼猜想的 Lean 形式化证明，代码库约 1700 万行。次日，Lean FRO 与 Mathlib Initiative 联合声明称，社区已确认该命题与 Mathlib 的 RiemannHypothesis 一致、代码库可无错编译，且多个独立证明检查器验证了证明有效。上述内容目前仅来自单一转发帖及其引用的博客链接，尚无独立信源佐证，应视为待核实的声明而非已确认的数学结论。

telegram · zaihuapd · 11月21日 16:48

**「背景」** 黎曼猜想是数学界最著名的未解问题之一，其形式化验证依赖 Lean 定理证明器及 Mathlib 数学库。据外部报道，Levent Alpöge 于 2026 年 11 月 20 日宣布与 Claude 合作得到黎曼猜想及 Dirichlet L 函数广义黎曼猜想的证明，并称已在 Lean 中无假设地完成形式化，但相关结果当时仍待同行验证。

**「影响与待核实点」** 若认证属实，该结果将同时影响数学与形式化验证两个领域：数学界需评估证明的实质内容，Lean 用户则需关注该代码库与 Mathlib 的兼容性及编译成本。由于 1700 万行的规模远超常规项目，独立复现编译与检查本身即是一项门槛较高的工作，在第三方复核完成前不宜将其当作已确立的定理。

**「社区讨论」** 有评论者认为，由于存在多个语言、多个内核的独立实现及各自的一致性证明，证明因内核缺陷而失效的可能性已很小；也有人提醒，过去曾出现伪造的 Collatz 反例通过某个所谓独立检查器的情况，因此检查器之间的独立性可能被高估。另有评论指出，此次工作据称形式化了大量现代数学内容，其意义不止于黎曼猜想本身，并强调 Alpöge 在引导模型完成该工作中的关键作用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unite.ai/levent-alpoges-unverified-riemann-claim-puts-claudes-lean-code-in-focus/">Levent Alpöge’s Unverified Riemann Claim Puts Claude’s Lean ...</a></li>
<li><a href="https://stateofproof.org/paper-watch/paper-2026-11-20-a-claimed-proof-of-the-riemann-hypothesis">A Claimed Proof of the Riemann Hypothesis — Paper Watch ...</a></li>
<li><a href="https://english.mathrubhumi.com/technology/levent-alpoge-riemann-hypothesis-proof-claude-lean-code-2026-iyc9lobg">Levent Alpöge Claims Riemann Hypothesis Proof With Claude ...</a></li>

</ul>
</details>

**标签**: `#formal-verification`, `#lean`, `#mathematics`, `#riemann-hypothesis`, `#mathlib`

---

<a id="item-tech-news-2"></a>
### [微软发布 RDMA over USB4 开发者预览，多台 PC 可合跑一个本地 AI 模型](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

微软发布了 Windows 平台的 RDMA over USB4 开发者预览，允许多台 PC 通过普通 USB4 连接共享内存与 GPU 算力，共同运行同一个本地 AI 大模型，无需专用网卡或交换机。微软给出的演示中，三台搭载 AMD Ryzen AI Max+ 395 的机器以 4-bit 量化运行 Qwen3-235B-A22B，速度约为 18.5 token/s。该功能将通过 Windows Insider 推送，目前仍是开发者预览而非正式产品。

telegram · zaihuapd · 11月21日 06:13

**「背景」** RDMA（远程直接内存访问）此前主要用于数据中心，通过专用网卡让一台机器直接读写另一台机器的内存，绕过常规网络协议栈。微软此次把这一能力搬到消费级 USB4 接口上，并复用 Windows 已有的 NetworkDirect API，使兼容的推理框架能把单个模型分布到多台 PC 的内存与 GPU 上。

**「影响与限制」** 对希望本地运行超出单机显存容量的大模型的用户，这一方案提供了用现有 USB4 接口拼接多台机器的路径，而不必采购专用网络硬件。但当前仅为开发者预览，实际可用性取决于 Windows Insider 推送范围以及各设备 USB4 实现与驱动的兼容情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/microsoftusbblog/introducing-rdma-over-usb4%C2%AE-on-windows-run-larger-local-ai-models-across-pcs/4574602">Introducing RDMA over USB 4 ® on Windows : run larger local AI ...</a></li>
<li><a href="https://www.guru3d.com/story/microsoft-previews-usb4-links-that-let-windows-pcs-pool-memory-and-gpu-resources/">Microsoft previews USB 4 links that let Windows PCs pool memory ...</a></li>

</ul>
</details>

**标签**: `#RDMA`, `#USB4`, `#local AI inference`, `#Windows`, `#distributed computing`

---

<a id="item-tech-news-3"></a>
### [OpenRouter 警告 MiniMax 模型提示词疑遭第三方读取](https://news.ycombinator.com/item?id=50585962) ⭐️ 8.0/10

OpenRouter 通过邮件通知用户，发往 MiniMax 模型的请求内容可能已被第三方读取。安全研究者在 2026 年 7 至 10 月向 MiniMax 模型发送含测试 URL 的提示词，第三方在 40 到 130 小时后访问了这些 URL。OpenRouter 将问题归因于 MiniMax 及其转发方 AtlasCloud、Novita、StreamLake，已下架相关端点的「零数据保留」标签，并建议涉及敏感凭证的用户更换 API Key 和密码。OpenRouter 官网暂未公布相关消息，上述细节来自一份简短的二手摘要，尚未获得独立确认。

telegram · zaihuapd · 11月21日 06:53

**「背景」** OpenRouter 是聚合多家模型与推理端点的路由服务，用户选择端点时往往依赖其标注的数据保留政策。此次事件中，安全研究者用植入提示词的测试 URL 作为“金丝雀”链接，在 2026 年 7 至 10 月间向 MiniMax 模型发送，随后观察到第三方在 40 到 130 小时后访问这些链接，从而暴露出提示词可能被转发方读取的问题。

**「影响与应对」** 通过 OpenRouter 向 MiniMax 模型发送过敏感数据（如密钥、密码或内部 URL）的用户，应按通知建议轮换 API Key 和密码。依赖「零数据保留」标签判断合规性的用户需注意，相关端点已不再带有该标签，不能再据此假定请求内容不会被留存或外泄。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://startupfortune.com/openrouter-warns-minimax-prompts-may-have-been-read-by-a-third-party/">OpenRouter warns MiniMax prompts may have been read by a ...</a></li>

</ul>
</details>

**标签**: `#security`, `#privacy`, `#llm-inference`, `#openrouter`, `#minimax`

---

<a id="item-tech-news-4"></a>
### [浙江大学在超导芯片上首次真机实现 QRAM](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 8.0/10

浙江大学团队报告在自主制备的超导量子芯片「天目 2 号」上首次于真机实现量子随机存储器（QRAM），成果发表于《自然·物理》。芯片上运行的原型可调取 4 位和 8 位数据，准确率分别为 80.9% 和 60.4%，线路深度较未优化方案降低 30% 以上，并首次验证该架构具备局部抗噪特性。团队表示下一步将推进 QRAM 的规模化研究。上述结果来自论文与团队表述，尚属早期原型性能，准确率数据也反映出当前水平有限。

telegram · zaihuapd · 11月21日 08:31

**「背景」** 量子随机存储器（QRAM）旨在让量子计算机以叠加态寻址经典或量子数据，是许多量子算法的关键组件，但此前多停留在理论或小规模线路方案阶段。据工具结果，浙江大学团队使用的「天目 2 号」是该校实验室研发的 125 比特超导量子处理器，本次 QRAM 原型即在该芯片上运行。

**「实际影响」** 对量子计算研究者而言，这一原型提供了在超导硬件上验证 QRAM 架构的实测数据，但 8 位数据调取仅 60.4% 的准确率意味着该方案距离可用于实际量子算法的可靠存储仍有明显差距，后续工作需优先提升保真度与规模。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://phys.org/news/2026-11-quantum-teleportation-method-weaker-entanglement.html">Quantum teleportation method uses weaker entanglement to transfer...</a></li>

</ul>
</details>

**标签**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#hardware`, `#research`

---

<a id="item-tech-news-5"></a>
### [胰腺癌口服药 daraxonrasib 一线早期数据：确认缓解率 60.7%](https://event.eortc.org/ena2026/2026/11/20/metastatic-pancreatic-cancer-responds-well-to-initial-treatment/) ⭐️ 8.0/10

11 月 20 日，在西班牙巴塞罗那举行的 EORTC-NCI-AACR（ENA 2026）大会上，daraxonrasib 一线联合化疗的早期数据以 late-breaking 口头报告形式公布：61 例既往未治疗的转移性胰腺导管腺癌患者每日口服 200 mg，联合吉西他滨/白蛋白紫杉醇，确认客观缓解率为 60.7%，完全缓解率为 8.2%（约十二分之一），疾病控制率为 90.2%，中位无进展生存期为 12.8 个月，12 个月总生存率为 76.6%，中位随访时间为 18.3 个月。研究者强调，这是单臂 I/II 期研究，没有化疗对照组，疗效对比仍需正在进行的 III 期试验验证。

telegram · zaihuapd · 11月21日 11:24

**「背景」** daraxonrasib 是一种口服 RAS\(ON\) 多选择性抑制剂，作用于活跃态 RAS 并覆盖多种 KRAS/NRAS 突变，而非仅针对单一 G12C 突变。据来源，该药已于 8 月 26 日获 FDA 批准（商品名 RASONQUE），用于既往治疗后的转移性胰腺癌患者，批准依据是 III 期 RMC-302 试验中位总生存 13.2 个月对 6.7 个月的结果；外部报道将该关键试验称为 RASolute 302。此次 ENA 2026 公布的是同一药物在未经治疗患者中联合化疗的单臂 I/II 期数据，与已获批的后线适应症属于不同治疗阶段。

**「解读注意」** 化疗的历史参照区间为 1 年生存率 22%–48%（MPACT 试验 35%，mFOLFIRINOX 48%），因此不宜简单断言该结果“远高于化疗”。机制上，daraxonrasib 是口服 RAS\(ON\) 多选择性抑制剂，作用于活跃态 RAS，覆盖多种 KRAS/NRAS 突变，并非单一 G12C 靶向药；该药已于 8 月 26 日获 FDA 批准（商品名 RASONQUE），用于既往治疗后的患者，依据是 III 期 RMC-302 试验：中位总生存期为 13.2 个月，对照组为 6.7 个月。

<details><summary>参考链接</summary>
<ul>
<li>Rasonque (daraxonrasib): FDA approval, pivotal trial and safety - 2 Minute Medicine</li>
<li>FDA approves RASONQUE (daraxonrasib) the first broad RAS-targeted medicine in metastatic pancreatic cancer - Medical Update Online</li>

</ul>
</details>

**标签**: `#biomedical-ai`, `#drug-discovery`, `#clinical-trials`, `#oncology`, `#RAS-inhibitors`

---

<a id="item-tech-news-6"></a>
### [显示器内置 USB 网卡为何把下载速度砍掉 75%](https://blog.tymscar.com/posts/studiodisplayethernet/) ⭐️ 7.0/10

一位博主排查发现，显示器内置 USB 集线器上的以太网适配器会把下载速度压低约 75%。根因是数据经显示器转发后额外增加的延迟，使笔记本无法及时确认数据包，适配器缓冲区被填满后开始丢包。换用对确认频率要求更低的适配器后问题消失。这是单个用户的排查记录，而非厂商声明或独立测量结果。

hackernews · soheilpro · 11月21日 10:36 · [社区讨论](https://news.ycombinator.com/item?id=50587875)

**「背景」** 许多显示器自带 USB 集线器，用户常把以太网适配器接在上面以节省接口。这条链路比直连多经过一层 USB 转发，会引入额外延迟，而 TCP 依赖及时返回的确认包来维持吞吐。

**「影响」** 遇到类似速度异常的 USB 网卡用户，可先尝试把适配器直接插到电脑或改用对确认频率要求更低的型号，而不是先怀疑宽带线路。

**「社区讨论」** 有评论认为更准确的标题应是“我的 USB 网络交换机拖慢了下载速度”，显示器本身并不关键；另有评论指出不少读者误解了原文，问题实质是延迟导致确认不及时、缓冲区溢出丢包。还有用户表示自己在 MacBook 加雷雳扩展坞上遇到同样问题已一年多，启用流控后勉强可用。

**标签**: `#networking`, `#usb`, `#troubleshooting`, `#hardware`, `#performance`

---

<a id="item-tech-news-7"></a>
### [FBI 与 USDA 据报遭黑客入侵，FBI 目标为 NCIC 数据库](https://www.theverge.com/tech/1039543/fbi-usda-hacked) ⭐️ 7.0/10

据媒体报道，美国联邦调查局（FBI）和美国农业部（USDA）于周五被曝遭到黑客入侵。CNN 报道称，这是 FBI 近几个月内第二次遭攻击，此次目标为全国犯罪信息中心（NCIC）数据库，该数据库供联邦、州和地方执法机构共享通缉令、失踪人员等信息；特朗普总统随后在接受 Fox News 采访时证实了此次入侵。NBC 最先报道了 USDA 被入侵一事，路透社援引报道称目前已知的入侵范围是支付数据库，但前官员警告实际影响可能更大。上述信息均来自媒体转述，报道未披露攻击者身份、入侵手法或受影响数据的具体规模。

rss · The Verge · 11月21日 17:42

**「背景」** NCIC 是美国联邦、州和地方执法机构共享通缉令、失踪人口及背景核查等信息的全国性数据库，也是此次报道所称 FBI 遭入侵的目标。据 CNN 援引两名了解调查情况的人士报道，FBI 正在调查这起疑似入侵事件；相关报道均将事件描述为“疑似”或“据报”，调查结论尚未公布。

**「实际影响」** 据搜索结果报道，USDA 的支付系统遭到入侵，导致用于向农民付款的系统被访问，关键系统被关闭，农民付款和贷款服务受到干扰；技术人员还被要求重置多个系统的数据库密码，进而引发更多应用下线。FBI 方面，此次被指针对 NCIC 数据库，该库用于联邦、州和地方执法机构共享通缉令和失踪人员等信息，但现有报道未说明数据是否被读取或篡改。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.newsmax.com/newsfront/fbi-national-crime-information-center-kash-patel/2026/11/21/id/1277111/">FBI Probes Apparent Breach of National Crime Database</a></li>
<li><a href="https://www.cnn.com/2026/11/20/politics/fbi-hacked-again-target-crime-database">The FBI was hacked again, this time the breach... | CNN Politics</a></li>
<li>7News DC on X: &quot;Hackers allegedly accessed a U.S. Department of Agriculture (USDA ...</li>
<li>BREAKING: USDA HIT BY CYBERSECURITY INCIDENT — CRITICAL SYSTEMS SHUT DOWN, FARMER PAYMENTS AND LOAN SERVICES DISRUPTED By John A. Patrick Jr.</li>
<li>BREAKING: USDA Cybersecurity Breach Takes Critical Farm Financial Systems Offline</li>

</ul>
</details>

**标签**: `#cybersecurity`, `#government`, `#data breach`, `#FBI`, `#USDA`

---

<a id="item-tech-news-8"></a>
### [微软 Entra Connect Health 漏洞遭利用，租户数据被窃](https://www.bleepingcomputer.com/news/security/microsoft-entra-connect-health-flaw-exploited-to-steal-tenant-data/) ⭐️ 7.0/10

微软警告称，攻击者利用 Entra Connect Health 服务中的一个漏洞，未经授权访问了管理员电子邮件地址和租户配置信息，构成一次数据泄露。微软将此事定性为已遭实际利用的漏洞，但现有报道未披露漏洞的技术细节、受影响的租户数量或修复状态。

rss · BleepingComputer · 11月21日 18:01

**「背景」** Entra Connect Health 是微软用于监控本地身份基础设施与 Entra ID 之间同步状态的混合身份监控服务，因此其接口一旦被滥用，暴露的往往是租户层面的管理信息。本次事件中，攻击者利用该服务的漏洞读取了管理员及技术联系人的电子邮件地址和租户配置数据，微软已就此向部分客户发出通知。

**「影响」** 使用 Entra Connect Health 的组织应假定其管理员邮箱地址和租户配置信息可能已暴露，并据此排查异常访问、加强管理员账户防护。由于报道未说明漏洞是否已修复，相关租户需关注微软后续公告以确认处置措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/microsoft-entra-connect-health-flaw/">Hackers Exploit Microsoft Entra Connect Health Flaw to Access ...</a></li>
<li><a href="https://windowsforum.com/news/microsoft-entra-connect-health-api-flaw-exposed-admin-emails-and-tenant-data.453553/">Microsoft Entra Connect Health API Flaw Exposed Admin Emails ...</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#microsoft`, `#cloud-identity`, `#data-breach`

---

<a id="item-tech-news-9"></a>
### [特斯拉海外推送 FSD v15，新增 Reality View 可视化界面](https://x.com/Tesla/status/2124222447855743019) ⭐️ 7.0/10

特斯拉已在海外开始推送 FSD v15。官方称本次更新将安全关键场景的处理能力提升至 25 倍，并新增“Tesla Reality View”可视化界面，可在车机屏幕上叠加摄像头画面与 FSD 行驶规划，支持全屏、地图或分屏视图及安静模式。导航可将转弯等信息叠加显示，转向灯提示音更轻柔并逐渐减弱；更新还优化了坑洼、碎片等路况的行驶体验，以及学校和恶劣天气下的速度控制。上述性能提升为特斯拉的官方说法，来源未提供独立验证或具体测试条件。

telegram · zaihuapd · 11月22日 00:03

**「背景」** FSD 是特斯拉的高级驾驶辅助软件，此前版本已具备导航辅助驾驶和可视化界面等能力。据多家特斯拉媒体报道，v15 是首个面向客户推送的版本，重点针对标志识别、坑洼路面和学校区域限速等此前被指出的薄弱环节，并新增 Reality View 可视化界面。

**「用户影响」** 已收到推送的海外车主可在车机上使用新的可视化界面与导航叠加提示，但“25 倍”安全提升目前仅为厂商声明，尚无第三方数据佐证，实际效果需以独立测试或监管评估为准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://teslanorth.com/2026/11/21/tesla-fsd-v15-first-rollout-reality-view/">Tesla Starts Rolling Out FSD v15 With a New Reality View</a></li>
<li><a href="https://electrek.co/2026/11/21/tesla-fsd-v15-rollout-25x-safety-reality-view/">Tesla launches FSD v15, targets its biggest weaknesses, from ...</a></li>

</ul>
</details>

**标签**: `#autonomous-driving`, `#tesla-fsd`, `#ai-systems`, `#software-release`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [特朗普提议对海外建 AI 数据中心的美国公司征“巨额税款”](https://apnews.com/article/trump-artificial-intelligence-data-centers-f1ac03b73d13445400eeed8631d9d879) ⭐️ 7.0/10

特朗普 11 月 20 日在白宫记者会上表示，计划对在海外建设人工智能数据中心的美国科技公司征收“巨额税款”，称目的是把数据中心留在美国、维持对中国的 AI 竞争优势；他并称尚未向政府内部官员透露该计划。

telegram · zaihuapd · 11月21日 03:26

**「背景」** 特朗普于 11 月 20 日在白宫记者会上提出这一设想，称目的是把数据中心留在美国、维持对中国的 AI 竞争优势，并表示尚未向政府内部官员透露该计划。目前全美多地社区因担忧数据中心的用电需求和噪音而反对新建项目。

**「潜在影响」** 若该拟议税收落地，在海外布局 AI 数据中心的美国大型科技公司可能面临额外成本，从而改变其选址决策；同时，正因用电和噪音问题反对新建数据中心的美国本地社区，可能因开发商被要求向社区付款而获得谈判筹码。目前该措施仅为表态，尚无税率、适用范围或立法时间表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/data-centers/trump-announces-mandate-for-data-centers-to-pay-dividends-to-the-local-community-hopes-to-win-more-data-center-supporters-through-dividend-scheme">Trump announces mandate forcing AI data centers to pay energy...</a></li>
<li><a href="https://ainewsglobal.online/data-center-anxiety-community-pushback-ai/">Data Center Anxiety: Why Communities Are Fighting Back</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#tax policy`, `#US-China tech competition`, `#data centers`, `#technology regulation`

---