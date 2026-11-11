---
layout: default
title: "Horizon Summary: 2026-11-11 (ZH)"
date: 2026-11-11
lang: zh
---

> 从 69 条内容中筛选出 16 条重要资讯。

---

**科技新闻**
1. [用电压毛刺解锁矿卡中的 A100 能力](#item-tech-news-1) ⭐️ 8.0/10
2. [Google DeepMind 发布 AlphaGenome 2，聚焦疾病的细胞根源](#item-tech-news-2) ⭐️ 8.0/10
3. [用 macOS Secure Enclave 保护 SSH 私钥的实践指南](#item-tech-news-3) ⭐️ 7.0/10
4. [线性规划能否用于模型权重空间编程](#item-tech-news-4) ⭐️ 7.0/10
5. [纽约 AI 安全法生效，OpenAI 与 Anthropic 面临新监管](#item-tech-news-5) ⭐️ 7.0/10
6. [谷歌扩展 AI 芯片阵容，新增两款专用 TPU](#item-tech-news-6) ⭐️ 7.0/10
7. [Railway 遭入侵，约 74 万美元 AI 费用被欺诈产生](#item-tech-news-7) ⭐️ 7.0/10
8. [黑客利用受信任的 AWS 访问权限入侵多个云环境](#item-tech-news-8) ⭐️ 7.0/10
9. [Xen Orchestra 严重认证绕过漏洞遭在野利用，可劫持 XCP-ng 主机](#item-tech-news-9) ⭐️ 7.0/10
10. [Binance 警告 iOS 漏洞可能泄露加密钱包密钥](#item-tech-news-10) ⭐️ 7.0/10
11. [阿里预告 Qwen4 系列，Qwen4-Max 预览版上线 Token Plan](#item-tech-news-11) ⭐️ 7.0/10
12. [AMD 将 Mext 技术商用：用 AI 在 DRAM 与 NVMe 间迁移冷内存页](#item-tech-news-12) ⭐️ 7.0/10
13. [The Information 调查指 Alice Huang 协助 24 万颗英伟达芯片入华](#item-tech-news-13) ⭐️ 7.0/10

**财经新闻**
1. [离岸信托收益征税过渡期结束，累计申报超 1600 亿元](#item-finance-news-1) ⭐️ 8.0/10
2. [美 FCC 批准 SpaceX 收购全美 800 兆赫兹频谱](#item-finance-news-2) ⭐️ 7.0/10
3. [Stripe 宣布 OpenRouter 并入旗下](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [用电压毛刺解锁矿卡中的 A100 能力](https://blog.kate.land/posts/using-voltage-glitching-to-unlock-the-a100/) ⭐️ 8.0/10

一篇博客文章描述了如何通过电压毛刺（voltage glitching）在矿卡上重新启用 A100 级别的能力。文章发布在 kate.land，并在 Hacker News 上引发讨论。由于没有可用的原文内容，具体涉及的卡型号、被解锁的功能范围、所用设备与成功率等关键细节无法从现有材料中确认；目前可依据的仅是文章标题与社区讨论所反映的主题，即通过硬件故障注入绕过熔丝限制。

hackernews · lae · 11月11日 10:48 · [社区讨论](https://news.ycombinator.com/item?id=50451903)

**「背景」** 涉事硬件是 Nvidia 的 CMP 170HX 矿卡，它基于与 A100 相同的 GA100 芯片，但出厂时通过熔丝关闭了大部分显存和计算单元。据外部报道，研究者 Kate Temkin 针对 GA100 芯片实施电压故障注入，清除熔丝限制后解锁了隐藏的显存与计算单元，测试吞吐量超过零售版 A100。

**「影响」** 对持有同类矿卡的用户而言，这一方法提供了一条绕过厂商熔丝、恢复被禁用计算能力的可能路径，但电压毛刺属于有风险的硬件操作，可能损坏芯片，且博客未提供可验证的通用流程。

**「社区讨论」** 评论者 htrp 感叹曾有人把 80 GB HBM 装到芯片上却关掉其中九成；amelius 则提出另一种解释，认为这些熔丝可能用于屏蔽制造缺陷，而非纯粹的市场分层。mr\_roboto 认为，对功能完好却被人为限制能力的硬件进行销售在道德上难以接受，而 roger\_ 表示自己已入手这类卡并准备尝试，并提到价格从约 200 美元涨到 1000 美元的变化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.lavx.hu/article/kate-uses-voltage-glitching-to-turn-a-cmp-170hx-mining-card-into-an-a100-class-gpu">Kate uses voltage glitching to turn a CMP 170HX mining card ...</a></li>
<li><a href="https://todayforai.com/en/items/art-2770d0dd-6ab">Voltage Glitching Unlocks CMP Mining Card Into 80GB A100</a></li>

</ul>
</details>

**标签**: `#hardware-hacking`, `#voltage-glitching`, `#gpu`, `#nvidia`, `#security`

---

<a id="item-tech-news-2"></a>
### [Google DeepMind 发布 AlphaGenome 2，聚焦疾病的细胞根源](https://www.theverge.com/ai-artificial-intelligence/1031524/google-deepmind-alphagenome-2-genetic-ai-model) ⭐️ 8.0/10

Google DeepMind 公布了 AlphaGenome 2，这是其基因组预测 AI 模型 AlphaGenome 的后继版本，目标是解析 DNA 变化如何影响不同细胞类型。该模型延续了“同一套 DNA 在不同细胞中被差异化开关”的问题设定，DeepMind 称其能提供更细致的视角，可能有助于理解疾病成因并指向新疗法。目前公开信息仅为简短报道，未披露模型架构、训练数据、基准测试结果或独立验证，因此其实际能力尚无法评估。

rss · The Verge · 11月11日 15:00

**「背景」** AlphaGenome 是 Google DeepMind 此前发布的基因组预测模型，据 DeepMind 介绍，它能在多项基因组预测基准上达到当时的最佳水平，例如判断某个遗传变异会增强还是减弱基因表达，或改变基因的剪接方式。该模型以 1 Mb 的 DNA 序列为输入，在单碱基分辨率上预测多种功能基因组信号，并在变异效应预测上优于既有模型。此次发布的 AlphaGenome 2 是这一模型的后续版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/alphagenome-ai-for-better-understanding-the-genome/">AlphaGenome: AI for better understanding the genome</a></li>
<li><a href="https://www.nature.com/articles/s41586-025-10014-0">Advancing regulatory variant effect prediction with AlphaGenome</a></li>

</ul>
</details>

**标签**: `#genomics`, `#AI for science`, `#Google DeepMind`, `#machine learning`, `#biotechnology`

---

<a id="item-tech-news-3"></a>
### [用 macOS Secure Enclave 保护 SSH 私钥的实践指南](https://gatezh.com/posts/macos-secure-enclave-ssh-keys/) ⭐️ 7.0/10

一篇技术文章介绍了如何将 SSH 私钥存入 macOS Secure Enclave，使私钥无法被直接导出，签名操作在硬件内完成。文章作者在评论区说明，自己最终选择了第三方工具 Secretive，而非原生方案，原因是原生方案弹出的 Touch ID 提示方式无法接受，而 Secretive 保留了更可控的交互。文中还提到 Secretive 可用于 Git 提交签名。

hackernews · js2 · 11月11日 04:28 · [社区讨论](https://news.ycombinator.com/item?id=50449748)

**「背景」** Secure Enclave 是苹果在 Mac 上提供的独立安全协处理器，私钥在其中生成和使用，无法被导出到主系统。此前已有文章介绍借助第三方应用 Secretive 将 SSH 私钥存入 Secure Enclave 的做法，并讨论了相关限制与排错。本次文章则聚焦不依赖第三方应用的原生实现方式。

**「实际影响」** 对希望降低私钥泄露风险的 macOS 用户而言，这一方案把密钥保护绑定到特定硬件和系统生态：私钥不可导出意味着迁移和备份需要额外设计。评论者 jwr 表示，他因此选择与机器厂商无关、可备份和异地转移的 YubiKey，并已使用约十年。

**「社区讨论」** 评论者对硬件绑定密钥的可靠性存在分歧：database64128 报告称，WireGuard 在 macOS 系统升级后因钥匙串读取失败（错误码 -25300）而崩溃，并删除了全部配置，因此转而用文本编辑器管理配置；seemaze 和 flexorium 则表示长期使用 Secretive 体验良好，flexorium 还将其用于 Git 提交签名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gatezh.com/posts/macos-secure-enclave-ssh-keys/">Protecting SSH Keys with macOS Secure Enclave (Native ...</a></li>
<li><a href="https://popov.wtf/secure-ssh-keys-with-secure-enclave-on-macos">Secure SSH Keys with Secure Enclave on macOS | Pavel Popov</a></li>

</ul>
</details>

**标签**: `#security`, `#ssh`, `#macos`, `#hardware-security`, `#open-source`

---

<a id="item-tech-news-4"></a>
### [线性规划能否用于模型权重空间编程](https://nathan.rs/posts/weight-space-lp/) ⭐️ 7.0/10

技术博客 nathan.rs 的一篇文章探讨了能否用线性规划（LP）来做模型的权重空间编程，即通过线性约束表达“消除某种行为、保留另一种行为”等目标，再借助 LP 求解器求解权重修改。文章给出了关于约束构造和求解器选择的讨论，但证据仅来自博客与社区讨论，并非经过独立验证的突破。Hacker News 评论者认为，这更像是为 Astra 一类权重编辑方法提供求解工具，而非 LP 能独立完成 Astra 的工作。

hackernews · emschwartz · 11月11日 12:30 · [社区讨论](https://news.ycombinator.com/item?id=50452655)

**「背景」** 2026 年 11 月初，MIT CSAIL 的四位研究者发布博客称，GPT-6 Astra 能直接读写神经网络权重，无需梯度下降或训练循环；据其自述测试，仅改动 Qwen3.5-0.8B 约 0.016% 的权重，就把 MATH-500 成绩从 7.9% 提升到 48.1%（tool-1-2、tool-1-3）。这一说法随后引发讨论：有评论认为，把“前沿模型直接理解并操纵权重”当作字面能力并不合理，因为模型是在 token 和任务完成上训练的，而非在权重上训练（见社区评论）。本次讨论的博客正是在这一背景下，考察线性规划能否作为权重空间编辑的求解工具。

**「实际影响」** 对从事模型编辑的开发者而言，这一思路意味着可以把编辑目标写成线性约束并交给成熟的 LP 求解器处理，但博客并未给出可复现的基准或与现有编辑工具的对比结果，实际效果仍需验证。评论者 dansitu 认为，这种方法的简洁性说明它更适合作为训练时的正则化手段，而不是事后编辑。

**「社区讨论」** 评论者 ultimatefan1 指出，此前关于前沿模型能直接读写权重的报道可能被夸大，更合理的描述是 Astra 做了包含权重修改小实验的训练研究，并找到了能修复部分问题的编辑。jsw97 认为 LP 求解器可作为权重编辑的辅助工具，在给定约束下提升编辑效果；rbnafo 则希望数值分析和 LP 方法能重新受到重视。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights: MATH-500 7.9% to 48.1% ...</a></li>
<li><a href="https://www.datacamp.com/blog/weight-space-programming">Weight-Space Programming: How LLMs Edit Network Weights</a></li>

</ul>
</details>

**标签**: `#linear programming`, `#model editing`, `#weight-space optimization`, `#machine learning`, `#numerical methods`

---

<a id="item-tech-news-5"></a>
### [纽约 AI 安全法生效，OpenAI 与 Anthropic 面临新监管](https://techcrunch.com/2026/11/10/openai-anthropic-face-new-oversight-as-new-yorks-ai-safety-law-takes-effect/) ⭐️ 7.0/10

纽约州即将执行其全面的 AI 安全法，要求 OpenAI、Anthropic 等大型 AI 开发商进行注册、披露安全实践，并报告重大事故，否则将面临罚款。报道未说明适用门槛、具体罚则金额或执行时间表，因此目前只能确认这是一项针对主要开发商的注册、披露与事故报告义务，而非已公布细则的完整合规框架。

rss · TechCrunch AI · 11月10日 20:52

**「背景」** 纽约这项法律由州议员亚历克斯·博尔斯推动通过，他在 2026 年 6 月的曼哈顿初选中成为 AI 监管议题的代理战场：据 Fortune 报道，OpenAI 的支持者投入 760 万美元试图阻止他连任，而 Anthropic 则投入 1000 万美元支持他。此次生效意味着该法从立法阶段进入执行阶段，但现有材料未说明其适用范围、门槛、罚则和具体时间表。

**「对开发者的影响」** 据外部报道，该法（RAISE Act）对大型前沿开发者设有额外要求，包括强制安全计划、透明度报告和事件披露，并通过评估费用为监管提供资金。因此，受覆盖的开发者需要建立可审计的安全文档与事故上报流程，并确认自身是否达到“大型前沿开发者”门槛，以判断是否适用这些额外义务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fortune.com/2026/06/17/bores-openai-anthropic-manhattan-primary-ai-regulation/">OpenAI &#x27;s backers spent $7.6 million to destroy a state... | Fortune</a></li>
<li><a href="https://www.multistate.ai/updates/vol-83-new-york-ai-safety-law-raise-act">New York AI Safety Law : RAISE Act Changes — multistate. ai</a></li>
<li><a href="https://inews.zoombangla.com/new-york-enacts-strict-ai-safety-law-joining-california-in-landmark-regulation/">New York Enacts Strict AI Safety Law , Joining California in Landmark...</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#AI safety`, `#policy`, `#OpenAI`, `#Anthropic`

---

<a id="item-tech-news-6"></a>
### [谷歌扩展 AI 芯片阵容，新增两款专用 TPU](https://techcrunch.com/2026/11/10/google-broadens-its-ai-hardware-portfolio-with-two-new-specialized-chips/) ⭐️ 7.0/10

谷歌宣布推出两款新的专用张量处理单元（TPU），将其 AI 芯片产品线扩展到更多使用场景。据现有信息，这两款芯片分别面向机密模型训练和更大内存容量需求。目前披露的内容仅为简要概述，尚无具体型号、规格、性能数据或独立测试结果，因此这些芯片的实际能力与上市状态仍不明确。

rss · TechCrunch AI · 11月10日 15:54

**「背景」** Google 长期自研张量处理单元（TPU）用于其云与内部 AI 工作负载。据 ServeTheHome 报道，Google 在 2026 年 Hot Chips 大会上介绍了第八代 TPU 家族，包括面向训练的 TPU 8t 和面向推理的 TPU 8i。此次新增的两款专用芯片是在这一代产品基础上的进一步细分，分别面向机密模型训练和更大内存容量场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.servethehome.com/googles-tpuv8s-for-training-and-inference-at-hot-chips-2026/">Google’s TPUv8s for Training and Inference at Hot Chips 2026</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#TPU`, `#Google`, `#confidential computing`, `#AI infrastructure`

---

<a id="item-tech-news-7"></a>
### [Railway 遭入侵，约 74 万美元 AI 费用被欺诈产生](https://www.bleepingcomputer.com/news/apple/railway-breach-leads-to-740-000-in-fraudulent-ai-charges/) ⭐️ 7.0/10

云托管服务商 Railway 表示，攻击者利用其基础设施中的漏洞窃取客户认证密钥，并借此产生了约 74 万美元的欺诈性 AI 用量。该事件可能波及多达 10 万个工作区的凭据。上述信息来自 Railway 的说明，目前尚无独立验证的细节披露。

rss · BleepingComputer · 11月10日 22:20

**「背景」** Railway 是一家提供应用、服务器和数据库部署的全栈云平台，其服务包含自动扩缩容、监控与安全功能。此次事件中，攻击者利用该平台基础设施的漏洞窃取客户认证密钥，并借此产生约 74 万美元的欺诈性 AI 用量，可能波及多达 10 万个工作区的凭据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://railway.com/">Railway | The all-in-one intelligent cloud provider</a></li>

</ul>
</details>

**标签**: `#security`, `#cloud-infrastructure`, `#ai-compute`, `#credential-theft`, `#incident-report`

---

<a id="item-tech-news-8"></a>
### [黑客利用受信任的 AWS 访问权限入侵多个云环境](https://www.bleepingcomputer.com/news/security/hackers-exploit-trusted-aws-access-to-breach-multiple-cloud-environments/) ⭐️ 7.0/10

据 BleepingComputer 报道，一名威胁行为者利用与大数据平台 Qubole 的 AWS 账户关联的已泄露 IAM 凭据，访问并窃取了多个客户 AWS 环境中的数据。报道将此次事件定性为跨租户的数据外泄，但所提供的内容摘要较为简短，未披露受影响客户数量、入侵时间线或具体的数据类型。目前尚不清楚 Qubole 或 AWS 是否已发布修复措施或通知细节。

rss · BleepingComputer · 11月10日 19:31

**「背景」** Qubole 是一家提供大数据平台的服务商，其 AWS 账户中的 IAM 凭证一旦泄露，攻击者便可借助该平台与客户云环境之间的信任关系横向进入多个租户。SecurityWeek 的报道称，此次事件中攻击者利用泄露的 Qubole 凭证，从十余家组织窃取了凭证、密钥和文件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.securityweek.com/over-a-dozen-organizations-hit-in-qubole-supply-chain-attack/">Over a Dozen Organizations Hit in Qubole Supply... - SecurityWeek</a></li>

</ul>
</details>

**标签**: `#cloud security`, `#AWS`, `#IAM`, `#data breach`, `#supply chain`

---

<a id="item-tech-news-9"></a>
### [Xen Orchestra 严重认证绕过漏洞遭在野利用，可劫持 XCP-ng 主机](https://www.bleepingcomputer.com/news/security/critical-xen-orchestra-auth-bypass-flaw-exploited-to-hijack-vm-servers/) ⭐️ 7.0/10

据 BleepingComputer 报道，Xen Orchestra 中存在一个严重认证绕过漏洞，目前已被攻击者在实际攻击中利用。利用该漏洞可获取管理员权限，并进而接管 XCP-ng 虚拟化主机。报道未披露漏洞的具体技术机制、受影响版本或修复补丁信息，因此尚无法确认哪些部署需要升级以及是否已有官方修复可用。

rss · BleepingComputer · 11月10日 16:17

**「背景」** Xen Orchestra 是 XCP-ng 和 Citrix Hypervisor（原 XenServer）的网页管理界面，管理员通过它集中管理虚拟化主机和虚拟机。据安全媒体 SecurityArsenal 报道，此次被利用的漏洞编号为 CVE-2024-55555，CVSSv3.1 评分为 9.8（严重），未认证的远程攻击者可绕过登录机制直接获得管理员权限。

**「影响与应对」** 运行 Xen Orchestra 管理 XCP-ng 主机的运维团队应将该漏洞视为高优先级风险：一旦被利用，攻击者可获得管理员权限并控制虚拟化主机。由于来源未给出受影响版本和补丁细节，建议直接向厂商渠道核实修复状态，并在确认前限制管理界面的外部访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://securityarsenal.com/blog/xen-orchestra-authentication-bypass-cve-2024-55555-detection-and-remediation-guide-for-xcp-ng-infrastructure">Xen Orchestra Authentication Bypass (CVE-2024-55555 ...</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#virtualization`, `#Xen Orchestra`, `#XCP-ng`

---

<a id="item-tech-news-10"></a>
### [Binance 警告 iOS 漏洞可能泄露加密钱包密钥](https://www.bleepingcomputer.com/news/security/binance-warns-of-ios-flaw-that-could-leak-crypto-wallet-secrets/) ⭐️ 7.0/10

Binance 警告称，Apple iOS 26.7.1、27.0.1 和 27.2 存在一个漏洞，可能允许第三方应用读取其他应用存储的私有文件，其中包括加密货币助记词、私钥和登录凭据。该警告针对上述具体 iOS 版本，但现有信息未说明漏洞的技术细节、触发条件或是否已有修复版本。

rss · BleepingComputer · 11月10日 15:59

**「背景」** 该漏洞被命名为 worse\_query，据称可让恶意应用读取其他应用所属的本地文件。币安在 11 月 10 日的警告中点名了受影响的 iOS 版本，并指出种子短语、私钥和登录信息可能因此暴露。

**「影响与应对」** 使用受影响 iOS 版本的用户应尽快升级：工具结果显示，苹果已发布 iOS 27.2.1 和 iPadOS 27.2.1（适用于 iPhone 11 及更新机型）修复相关漏洞。在完成更新前，持有加密钱包的用户需警惕第三方应用可能读取其他应用的种子短语和凭据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/ios-flaw-expose-crypto-wallet/">Binance Warns iPhone Users of Major iOS Flaw That May Expose ...</a></li>
<li><a href="https://cryptonews.com/news/binance-ios-worse-query-iphone-duo-18pro-security-flaw/">iPhone Duo Under Attack? Binance Flags iOS Security Flaw</a></li>
<li><a href="https://happycoin.news/en/apple-i-google-zakryli-uyazvimosti-a-binance-predupredila-ob-atakah-na-seed-frazy-v-ios/">Apple , Google, and Binance have secured crypto wallet owners...</a></li>

</ul>
</details>

**标签**: `#security`, `#iOS`, `#vulnerability`, `#cryptocurrency`, `#mobile`

---

<a id="item-tech-news-11"></a>
### [阿里预告 Qwen4 系列，Qwen4-Max 预览版上线 Token Plan](https://mp.weixin.qq.com/s/J_zbVHa2R3mmY5KD4v3-bw) ⭐️ 7.0/10

阿里预告了 Qwen4 模型系列，并称其知识理解更深入、世界感知更立体，Coding 与 Agentic 能力继续进阶。Qwen4-Max 预览版已首发上线阿里 Token Plan，限时最低 1 折体验；Qoder、千问 App、QwenStudio 等产品已同步接入新模型。上述能力描述均为阿里方面的宣传口径，来源未给出技术细节、基准测试结果或独立验证。

telegram · zaihuapd · 11月11日 02:35

**「背景」** 阿里此前已通过 Qwen3.8-Flash-Next 这一开放权重多模态模型预览 Qwen 4 系列计划采用的架构，该实验模型参数量为 125B（据 tool-2-3）。此次 Qwen4-Max 预览版则是 Qwen 4 系列的旗舰模型，主打复杂编程与智能体任务，并已接入阿里 Token Plan、Qoder、千问 App 和 QwenStudio 等产品（据 tool-2-1）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kucoin.com/news/flash/aliyun-launches-qwen4-max-preview-focused-on-complex-programming">Aliyun Launches Qwen 4 - Max Preview Focused on Complex... | KuCoin</a></li>
<li><a href="https://ask.yugatech.com/general/qwen3-8-flash-next-previews-the-qwen4-architecture-with-125b-parameters/">Qwen3.8-Flash-Next Previews The Qwen 4 Architecture With...</a></li>

</ul>
</details>

**标签**: `#llm`, `#qwen`, `#alibaba`, `#model-release`, `#ai-agents`

---

<a id="item-tech-news-12"></a>
### [AMD 将 Mext 技术商用：用 AI 在 DRAM 与 NVMe 间迁移冷内存页](https://www.theregister.com/systems/2026/11/11/amd-where-were-going-we-dont-need-as-much-dram/5308953) ⭐️ 7.0/10

AMD 将收购所得的 Mext 技术做成一套软件，用 AI 模型在操作系统或应用察觉之前，把内存页面在 DRAM 与更便宜的 NVMe 闪存之间换入换出，以减少服务器所需内存。AMD 称，用闪存替代一半 DRAM 仍能保留最高 99% 的性能，并估算最多可把企业服务器成本降低 83%。这些数字均为 AMD 自身的说法，尚缺独立验证；该方案需在购买 Epyc 服务器时一并购买 Mext 授权。

telegram · zaihuapd · 11月11日 11:15

**「背景」** AMD 的 Mext 技术来自其 2026 年 6 月收购的初创公司 MEXT。据当时的报道，MEXT 开发的内存分层技术可让 NAND 闪存对操作系统呈现为 DRAM，从而缓解数据中心的内存容量约束。AMD 现在把这项技术作为纯软件方案商业化，用 AI 预测并迁移冷内存页。

**「对采购与部署的影响」** 由于 Mext 授权与 Epyc 服务器购买绑定，企业无法单独采购或试用这套内存分层软件，评估时需把授权成本与减少 DRAM 配置带来的节省一并核算。AMD 宣称的 99% 性能保留和 83% 成本下降均属厂商估算，实际效果取决于工作负载的冷热页分布，部署前应自行验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.amd.com/en/blogs/2026/amd-acquires-mext-for-memory-optimization.html">AMD Acquires MEXT to Advance Memory Optimization</a></li>
<li><a href="https://www.tomshardware.com/pc-components/cpus/amd-takes-over-mext-to-address-growing-memory-constraints-in-the-data-center-memory-tiering-technology-enables-flash-to-appear-as-dram-to-applications">AMD takes over MEXT for memory tiering tech that enables ...</a></li>
<li><a href="https://www.amd.com/en/products/software/mext.html">AMD MEXT Predictive Memory Software</a></li>

</ul>
</details>

**标签**: `#memory-tiering`, `#AMD`, `#server-hardware`, `#AI-for-systems`, `#NVMe`

---

<a id="item-tech-news-13"></a>
### [The Information 调查指 Alice Huang 协助 24 万颗英伟达芯片入华](https://www.tomshardware.com/tech-industry/policy/alice-huang-reportedly-instrumental-in-securing-over-usd7-5-billion-of-nvidia-ai-gpu-imports-during-three-year-relationship-with-jensen-huang-helped-move-240-000-banned-chips-into-china-mostly-h100-and-h200) ⭐️ 7.0/10

The Information 的一项调查（经 Tom&\#x27;s Hardware 转述）称，Alice Huang（黄乐）借助与英伟达 CEO 黄仁勋的关系，协助约 24 万颗被禁的英伟达 AI 芯片进入中国，其中多为 H100 和 H200，涉及进口金额约 75 亿美元。报道还提到上海世纪利通与新加坡 Megaspeed 等公司牵涉其中。上述内容目前均为调查报道中的指控，并非已确认的事实，且现有转述未提供原始证据细节。

telegram · zaihuapd · 11月11日 14:41

**「背景」** 美国自 2022 年起对华实施 AI 芯片出口管制，H100、H200 等高性能 GPU 属于受限或禁止对华销售的产品，需经许可才能出口。The Information 的调查称，在受限芯片订单受阻时，Alice Huang 借助与英伟达的关系获取供货，将约 24 万颗 H100、H200 及部分 A100 芯片送入中国，相关进口金额至少 75 亿美元。路透社同日报道称，英伟达正因 CEO 与 Alice Huang 的关系及涉嫌芯片走私而面临更深入的审查。

**「潜在影响」** 若指控成立，这一规模意味着大量受出口管制的 H100/H200 通过第三方渠道流入中国，相关进口商和中间商可能面临美国出口管制审查；对依赖合规采购的企业而言，供应链来源与最终用途的核查将更受关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theinformation.com/articles/jensen-huangs-yearslong-ties-alice-huang-enabled-nvidia-chip-sales-china">How Jensen Huang’s Yearslong Ties to Alice Huang Enabled $7 ...</a></li>
<li><a href="https://www.reuters.com/world/china/nvidia-ceos-affair-aided-75-billion-chip-shipments-china-information-reports-2026-11-10/">Nvidia faces deepening scrutiny over China chip ties, CEO ...</a></li>

</ul>
</details>

**标签**: `#nvidia`, `#export-controls`, `#ai-hardware`, `#supply-chain`, `#investigative-reporting`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [离岸信托收益征税过渡期结束，累计申报超 1600 亿元](https://www.news.cn/20261111/9bcce99c779b4a6197ff45bbbc3e4c50/c.html) ⭐️ 8.0/10

国家税务总局 11 月 11 日表示，离岸信托收益征税的 90 天过渡期已结束，累计申报个人所得税超过 1600 亿元人民币，其中 10 月当月入库超过 1200 亿元，带动 10 月全国个人所得税收入同比增长近 90%。

telegram · zaihuapd · 11月11日 10:35

**「背景」** 财政部、税务总局 2026 年 7 月 24 日发布公告，规定在 90 天过渡期内完成申报缴税可免收滞纳金；税务部门称，下一步将对未主动申报或申报不实的纳税人督促补缴并加收滞纳金，仍不改正的将依法立案稽查。

**「影响」** 这一措施直接针对持有离岸信托收益的纳税人，未在过渡期内如实申报者将面临补缴、滞纳金乃至立案稽查。

**标签**: `#offshore trusts`, `#personal income tax`, `#tax enforcement`, `#fiscal revenue`, `#China policy`

---

<a id="item-finance-news-2"></a>
### [美 FCC 批准 SpaceX 收购全美 800 兆赫兹频谱](https://wap.cj.sina.cn/7x24/5206981) ⭐️ 7.0/10

美国联邦通信委员会（FCC）批准了 SpaceX 收购 Grain Management 全美 800 兆赫兹频谱的申请，交易涉及 546 组成对牌照，覆盖近乎全部美国人口。Verizon、AT&amp;T 和 T-Mobile 均拒绝让 SpaceX 接入其网络。

telegram · zaihuapd · 11月11日 02:14

**「背景」** 2026 年 10 月 8 日，Grain Management 宣布与 SpaceX 达成最终协议，出售其全美 800 兆赫兹频谱组合；SpaceX 在提交给 FCC 的说明中称，获批后将快速部署这批“长期未被充分利用”的低频段牌照。

**「影响」** 获批的低频段频谱穿墙能力强、几乎适配所有智能手机，SpaceX 可借此在三大运营商拒绝其接入网络的情况下，自行建设覆盖全美、可进入室内的移动网络。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://graingp.com/grain-management-announces-definitive-agreement-to-sell-nationwide-800-mhz-spectrum-portfolio-to-spacex/">Grain Management Announces Definitive Agreement to Sell ...</a></li>
<li><a href="https://sxcontent9668.azureedge.us/cms-assets/assets/FCC_Narrative_10_8_26_f63e78e026.pdf">Draft PIS and Description of the Transaction (Grain 800 MHz ...</a></li>
<li><a href="https://wccftech.com/spacex-grabs-a-piece-of-the-800-mhz-spectrum-that-would-allow-starlink-mobile-to-work-indoors-sidestepping-att-t-mobile-and-verizon-after-they-refused-to-partner/">SpaceX Grabs A Piece Of The 800 MHz Spectrum That ... - Wccftech</a></li>
<li><a href="https://arstechnica.com/tech-policy/2026/10/starlink-spectrum-deal-boosts-musk-plan-to-beat-att-t-mobile-and-verizon/">Starlink spectrum deal boosts Musk plan to beat AT&amp;T, T ...</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#FCC`, `#spectrum`, `#telecom`, `#regulation`

---

<a id="item-finance-news-3"></a>
### [Stripe 宣布 OpenRouter 并入旗下](https://x.com/stripe/status/2120240651778355306) ⭐️ 7.0/10

支付公司 Stripe 于 2026 年 11 月 11 日宣布，AI 模型调用平台 OpenRouter 已并入旗下。Stripe 称此举旨在为 AI 搭建经济基础设施，帮助企业探索新模型并优化 token（模型调用计费单位）的路由与用量；公告未披露交易金额、估值或交易结构。

telegram · zaihuapd · 11月11日 09:45

**「背景」** OpenRouter 是一个连接开发者与多家 AI 模型的“路由”平台，此前在 2025 年完成 1.13 亿美元融资、估值 13 亿美元（据 tool-2-2）。Stripe 是支付公司，此次公告未披露交易金额；有报道称交易规模约 70 亿美元，但该数字来自外部报道而非 Stripe 公告（tool-1-1、tool-1-2）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finelo.com/blog/stripe-openrouter-acquisition-2026">Stripe Acquires OpenRouter | Understand the AI Deal | Finelo</a></li>
<li><a href="https://www.orcarouter.ai/blog/stripe-acquires-openrouter">Stripe OpenRouter Acquisition : $7B, What Changes for Devs</a></li>
<li><a href="https://laava.nl/en/news/openrouter-model-routing-enterprise-ai-runtime">OpenRouter &#x27;s funding shows why model routing belongs in the AI ...</a></li>

</ul>
</details>

**标签**: `#acquisition`, `#Stripe`, `#OpenRouter`, `#AI infrastructure`, `#fintech`

---