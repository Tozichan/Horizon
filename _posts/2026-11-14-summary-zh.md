---
layout: default
title: "Horizon Summary: 2026-11-14 (ZH)"
date: 2026-11-14
lang: zh
---

> 从 62 条内容中筛选出 13 条重要资讯。

---

**科技新闻**
1. [英伟达 CEO 黄仁勋据报因婚外情辞职](#item-tech-news-1) ⭐️ 8.0/10
2. [TorchTitan 在 384 块 GH200 上训练 1T MoE](#item-tech-news-2) ⭐️ 8.0/10
3. [用双 4090 与 B210 实时监听并转写全频段航空波段](#item-tech-news-3) ⭐️ 7.0/10
4. [亚马逊拟建“世界商品图谱”索引全网购物数据](#item-tech-news-4) ⭐️ 7.0/10
5. [OpenAI 推出 ChatGPT Wallet，Dots 智能体可代用户付款](#item-tech-news-5) ⭐️ 7.0/10
6. [黄仁勋离任或令 AI 初创融资出现巨大缺口](#item-tech-news-6) ⭐️ 7.0/10
7. [研究称中国最强 AI 模型使用被禁 Nvidia 芯片训练](#item-tech-news-7) ⭐️ 7.0/10
8. [Check Point 网关遭 PHP2Shell 攻击，ESXi 主机被植入擦除型恶意软件](#item-tech-news-8) ⭐️ 7.0/10
9. [ICML 2027 拟推两阶段审稿与互惠审稿人新规](#item-tech-news-9) ⭐️ 7.0/10
10. [上海公布交大医学院基因编辑事件调查结果](#item-tech-news-10) ⭐️ 7.0/10
11. [Python 早期贡献者 Tim Peters 去世，享年 74 岁](#item-tech-news-11) ⭐️ 7.0/10
12. [DeepSeek 开放应用 API：服务端自动调用搜索、OCR、语音等工具](#item-tech-news-12) ⭐️ 7.0/10
13. [SpaceX 裁撤 Grok Imagine 团队约 60 人](#item-tech-news-13) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [英伟达 CEO 黄仁勋据报因婚外情辞职](https://techcrunch.com/2026/11/13/nvidia-ceo-jensen-huangs-affair-with-alleged-chinese-spy-a-timeline/) ⭐️ 8.0/10

TechCrunch 于 2026 年 11 月 13 日发布的一篇报道称，英伟达 CEO 黄仁勋因一段婚外情已辞去公司职务，报道称该事件可能对国家安全产生影响，背景是美国与中国在先进 AI 基础设施领域的竞争。该报道仅以一句话概括此事，未提供时间线细节、消息来源或任何佐证材料，因此辞职是否属实、涉及何人以及具体经过均无法从现有内容中核实。

rss · TechCrunch AI · 11月13日 15:58

**「事件背景」** 据《卫报》报道，黄仁勋因被曝与一名疑似中国间谍及两名公司员工存在婚外情而辞去英伟达首席执行官职务，公司首席财务官 Colette Kress 暂代其职，直至确定正式继任者。BBC 报道称，英伟达董事会已确认其辞职，黄仁勋表示愿意在辞职后出席美国国会作证。

**「潜在影响」** 若黄仁勋辞职一事属实，英伟达将面临领导层真空，竞争对手可能借机争夺市场份额；但现有来源仅有一句摘要，未提供辞职生效时间、继任安排或官方确认，因此上述后果仍属基于未经核实报道的推测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/12/nvidia-ceo-jensen-huang-resigns">Jensen Huang resigns as Nvidia CEO after alleged affairs</a></li>
<li><a href="https://www.bbc.com/news/live/c6zjry11v8w1t">Huang agrees to appear before Congress, US lawmakers... - BBC News</a></li>
<li><a href="https://apnews.com/article/nvidia-jensen-china-ai-chips-1b7431af84c9d78773c277672a9486f3">Jensen Huang&#x27;s departure as Nvidia CEO may dampen mood around ...</a></li>

</ul>
</details>

**标签**: `#nvidia`, `#ai-industry`, `#us-china-tech`, `#national-security`, `#corporate-leadership`

---

<a id="item-tech-news-2"></a>
### [TorchTitan 在 384 块 GH200 上训练 1T MoE](https://www.reddit.com/r/MachineLearning/comments/1xvce5h/scaling_to_1t_moe_on_torchtitan_p/) ⭐️ 8.0/10

一位实践者报告称，使用 TorchTitan 在 384 块 GH200（JUPITER 超算所用 GPU）上训练约 1T 参数 MoE，达到每 GPU 约 1,300 tokens/s，相比起点提升 14 倍。其方案采用 384 路 FSDP 加 4 路专家并行（EP 严格限制在节点内），并放弃流水线并行，理由是 PP 需要大量微批次来掩盖气泡，导致单步过长、调试迭代慢。作者还分享了多项具体优化：全量激活检查点带来 4 倍提升；将检查点激活卸载到 Grace 并通过 C2C 链路预取；用 Muon 替代 Adam 以支持 64k token 序列；将 Newton-Schulz 迭代移到 GPU 后优化器步从 42 秒降至约 2 秒、吞吐提升 35%。这些是实践者经验报告而非同行评审结果，且原文摘录在结尾处被截断。

reddit · r/MachineLearning · /u/f14-bertolotti · 11月13日 16:28

**「背景」** TorchTitan 是 PyTorch 原生的大规模训练平台，将 FSDP、张量并行、流水线并行、上下文并行和专家并行组合在同一套可配置代码中，覆盖从预训练到微调的流程。据 PyTorch 博客 2025 年 12 月的介绍，它已被用于在 1K 块 AMD GPU 上开展 MoE 预训练。本次报告则是在 JUPITER 超算的 GH200 集群上，用 384 块 GPU 验证 TorchTitan 对约 1T 参数 MoE 的扩展能力。

**「对大规模训练实践的影响」** 该报告给出的具体优化手段对在 InfiniBand 集群上训练超大 MoE 的团队有直接参考价值：将专家梯度 reduce-scatter 改为 bf16 all-to-all 并在本地以 fp32 累加，可在保持精度的同时把梯度传输字节减半；把 FP8 与 bf16 集合通信的临时缓冲移到计算流上，可避免缓存分配器在侧流上占用显存，作者称重试从 384 个 rank 降为零、峰值预留显存减少 13.5 GiB。不过这些数字来自单一实践者的对比运行，且原文被截断，采用前仍需在自身拓扑上验证。

**「社区讨论」** 该条目没有可用的社区评论，因此无法总结实质性讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/pytorch/torchtitan">GitHub - pytorch/torchtitan: A PyTorch native platform for ...</a></li>
<li><a href="https://pytorch.org/blog/efficient-moe-pre-training-at-scale-with-torchtitan/">Efficient MoE Pre-training at Scale on 1K AMD GPUs ... - PyTorch</a></li>

</ul>
</details>

**标签**: `#large-language-models`, `#mixture-of-experts`, `#distributed-training`, `#pytorch`, `#gpu-scaling`

---

<a id="item-tech-news-3"></a>
### [用双 4090 与 B210 实时监听并转写全频段航空波段](https://orcasairband.com/) ⭐️ 7.0/10

一个名为 orcasairband.com 的业余项目用 ETTUS B210 软件无线电接收机配合双 RTX 4090 显卡，通过 CUDA 编写的多相信道化器把整个航空波段切分、解调、检测发射并转写为文字，同时丢弃数据类传输。作者 mmaunder 在 Hacker News 上说明，该项目在当天维多利亚（Victoria）与奥卡斯（Orcas）发生地面停飞（ground stop）时意外派上用场，并贴出了标注 UTC 时间的原始转写片段，例如 2143Z 在 126.400 维多利亚地面频率上听到“通信问题，所以把航班流量停住了”。这些转写未经人工编辑，部分信号较弱、内容不完整，属于个人项目而非已发布的产品或经独立验证的成果。

hackernews · mmaunder · 11月13日 22:04 · [社区讨论](https://news.ycombinator.com/item?id=50490593)

**「背景」** 该项目使用 Ettus Research 的 USRP B210 软件定义无线电，这是一款单板双通道收发器，官方标称连续频率覆盖 70 MHz 至 6 GHz，因此可覆盖航空波段。作者在评论中说明，系统用 CUDA 代码在双 RTX 4090 上对整个航空波段做多相信道化，再解调、检测发射并转写。此前已有研究用 GPU 对整段频谱实时信道化处理，例如针对蓝牙频谱的嗅探系统，但那是学术原型，并非面向航空通信的公开在线服务。

**「实际用途」** 在官方信息有限时，这类全频段实时转写能让附近飞行员和爱好者直接了解空域内的通话情况；但转写质量受信号强弱影响，作者贴出的片段中就有“无法辨识”和信号微弱的情况，因此不宜作为运行决策的唯一依据。

**「社区讨论」** 有评论者 molsongolden 回翻到链接发布时的 14:03，指出当时正好有一段确认温哥华地面停飞的对话被记录下来。plipt 则对许多通话听起来含糊不清感到意外，并询问航空通信是否仍为模拟制式以兼顾安全与互操作。ltrg 提到一个类似的 Claude 业余项目，它通过公开的 KiwiSDR 接收机解码船舶 DSC 信号，并尝试用多接收机时延进行定位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ettus.com/all-products/ub210-kit/">USRP B 210 USB Software Defined Radio ( SDR ) - Ettus Research</a></li>
<li><a href="https://www.pure.ed.ac.uk/ws/files/148736420/medcomnet2020.pdf">One GPU to Snoop Them All: a Full- Band</a></li>

</ul>
</details>

**标签**: `#software-defined-radio`, `#GPU-computing`, `#signal-processing`, `#speech-transcription`, `#hobbyist-engineering`

---

<a id="item-tech-news-4"></a>
### [亚马逊拟建“世界商品图谱”索引全网购物数据](https://www.theverge.com/tech/1033697/amazon-world-product-graph-ai-search) ⭐️ 7.0/10

据 Reuters 报道，亚马逊计划构建名为“World Product Graph”的商品数据索引库，收录互联网上销售的商品信息，包括亚马逊自身并不销售的商品，并通过亚马逊网站对外提供这些信息。该项目的目标是降低购物者转去 Reddit 或 Google 做商品调研的可能性，并让搜索其他平台商品的用户最终仍来到亚马逊；对于 AI 购物代理，亚马逊希望凭借规模最大的购物数据储备，使其优先依赖亚马逊的商品索引。目前这仍是报道中的计划，The Verge 的原文内容被截断，尚无具体技术细节、上线时间或可用范围。

rss · The Verge · 11月13日 23:49

**「背景」** 据路透社报道，亚马逊的“World Product Graph”计划来自一份内部文件，目标是汇集几乎所有在售商品的数据，无论亚马逊是否销售该商品。亚马逊方面回应称该文件是一份过时的头脑风暴材料，目前没有确认的发布计划，因此这仍是一项被报道的内部构想，而非已上线的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/business/media-telecom/amazons-plan-own-worlds-product-data-fight-ai-shopping-agents-2026-11-13/">Amazon’s plan to own the world’s product data and fight AI ...</a></li>
<li><a href="https://explainx.ai/blog/amazon-world-product-graph-reuters-ai-shopping-agents-draft-memo-claimed-vs-verified-2026">Amazon World Product Graph: What Reuters Found vs Confirmed ...</a></li>
<li><a href="https://economictimes.indiatimes.com/tech/artificial-intelligence/amazons-plan-to-own-the-worlds-product-data-and-fight-ai-shopping-agents/articleshow/135800426.cms">Amazon&#x27;s plan to own the world&#x27;s product data and fight AI ...</a></li>

</ul>
</details>

**标签**: `#AI search`, `#e-commerce`, `#product data`, `#Amazon`, `#AI agents`

---

<a id="item-tech-news-5"></a>
### [OpenAI 推出 ChatGPT Wallet，Dots 智能体可代用户付款](https://www.theverge.com/ai-artificial-intelligence/1033425/openai-chatgpt-wallet) ⭐️ 7.0/10

OpenAI 开始向美国 ChatGPT Pro 订阅用户推出 ChatGPT Wallet，让 Dots 智能体在用户授权下完成购物付款。该功能面向年满 18 岁、使用美国账单地址并绑定符合条件的美国发行美国运通、Chase、万事达或 Visa 卡的用户。用户添加卡片后，智能体可依据指令选购商品，但每次结账前都会与用户确认，且每笔购买都需通过 Face ID 或指纹等生物识别验证。支付时使用支付网络下发的替代卡号令牌，智能体不会接触真实卡号。

rss · The Verge · 11月13日 20:45

**「背景」** OpenAI 今年早些时候推出了 Dots AI 智能体平台，这些常驻智能体可在 ChatGPT 内持续执行用户设定的任务。据外部报道，Dots 于 2026 年 9 月底发布，每个智能体拥有独立的云端计算机并接入大量应用。此次 ChatGPT Wallet 是在该平台之上新增的支付能力。

**「对用户的影响」** 对符合条件的 Pro 用户而言，智能体代购被限制在逐笔人工确认和生物识别验证之下，实际使用更接近“代为下单、本人批准”，而非无人值守的自动消费。美国以外地区、非 Pro 用户以及使用其他发卡行的用户暂时无法使用该功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://supergok.com/openai-dots/">OpenAI Dots Bring Always-On AI Agents to ChatGPT</a></li>
<li><a href="https://www.dragapp.com/blog/openai-dots/">OpenAI Dots and Email: What a Dot Can Do With Your Inbox ( 2026 )</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#OpenAI`, `#agentic commerce`, `#payments`, `#AI industry`

---

<a id="item-tech-news-6"></a>
### [黄仁勋离任或令 AI 初创融资出现巨大缺口](https://techcrunch.com/2026/11/13/jensen-huangs-departure-blasts-big-hole-in-ai-startup-funding-vcs-and-founders-say/) ⭐️ 7.0/10

TechCrunch 报道称，随着黄仁勋离任，英伟达在黄仁勋领导下对 AI 初创公司的大规模投资角色据称将结束。报道称英伟达此前向 AI 初创公司投入了数百亿美元，但未给出具体金额、时间范围或投资明细。创始人和风投人士预计，此后融资支票会变小、估值会降低。上述影响来自受访者的预期，而非已发生的融资数据或英伟达正式披露的计划。

rss · TechCrunch AI · 11月13日 22:43

**「背景」** 据《纽约时报》报道，截至 7 月底，英伟达持有 229 家私营公司的股份，价值约 480 亿美元，其中包括 OpenAI 和 Anthropic；黄仁勋本人一直积极支持初创企业。TechCrunch 前一日报道称，黄仁勋辞职后，英伟达对开源 AI 的承诺（包括 Hugging Face 收购、开放权重模型及反对限制的立场）也因领导层过渡而受到质疑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/13/technology/jensen-huang-silicon-valley-start-ups.html">Jensen Huang ’s Resignation From Nvidia Worries the A . I . Start - Up ...</a></li>
<li><a href="https://techcrunch.com/2026/11/12/jensen-huangs-exit-puts-nvidias-support-for-open-source-in-question/">Jensen Huang ’s exit puts Nvidia ’s support for open... | TechCrunch</a></li>

</ul>
</details>

**标签**: `#AI startups`, `#venture capital`, `#Nvidia`, `#industry news`, `#funding`

---

<a id="item-tech-news-7"></a>
### [研究称中国最强 AI 模型使用被禁 Nvidia 芯片训练](https://techcrunch.com/2026/11/13/export-banned-nvidia-chips-are-behind-chinas-most-powerful-ai-models-uh-oh-jensen/) ⭐️ 7.0/10

TechCrunch 于 2026 年 11 月 13 日报道称，一项新研究显示，中国最先进的 AI 模型是在受出口禁令限制的 Nvidia 芯片上训练的。该报道据此质疑出口管制的实际效果。但现有材料仅有一句概述，未披露研究机构、所用芯片型号、模型名称、训练规模或验证方法，因此这一结论目前无法从来源中进一步核实。

rss · TechCrunch AI · 11月13日 18:40

**「背景」** 美国对华先进 AI 芯片出口管制已实施多轮，其核心目标是限制中国获得用于训练大模型的 Nvidia 高端算力。此前已有报道称，中国 AI 公司被指通过海外渠道获取受限的 Nvidia 算力，例如 CNBC 在 2026 年 7 月报道白宫官员指控 Moonshot 访问 Nvidia 先进芯片，8 月又报道中国 AI 企业利用海外算力测试出口管制的执行效果。

**「对出口管制的影响」** 若该研究结论成立，则说明现有出口管制未能阻止受禁 Nvidia 芯片用于中国最先进模型的训练，政策制定者可能需要重新评估芯片出口与云端算力访问等管控环节的有效性。此前已有报道称中国 AI 企业通过海外渠道获取先进 Nvidia 算力，美国方面也在讨论如何堵住云访问这一缺口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/07/23/moonshot-kimi-nvidia-ai-chips-export-ban.html">China&#x27;s Moonshot AI accessed banned Nvidia chips, U.S ... - CNBC</a></li>
<li><a href="https://www.cnbc.com/2026/08/19/china-ai-nvidia-chips-us-export-controls.html">China AI firms tap Nvidia power overseas as U.S ... - CNBC</a></li>
<li><a href="https://www.cnbc.com/2026/08/19/china-ai-nvidia-chips-us-export-controls.html">China AI firms tap Nvidia power overseas as U.S ... - CNBC</a></li>
<li><a href="https://www.cnbc.com/2026/05/31/us-takes-step-to-halt-nvidia-ai-chip-shipments-to-chinese-firms-outside-china.html">U.S. takes step to halt Nvidia AI chip shipments to Chinese ...</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#export controls`, `#Nvidia`, `#China AI`, `#AI policy`

---

<a id="item-tech-news-8"></a>
### [Check Point 网关遭 PHP2Shell 攻击，ESXi 主机被植入擦除型恶意软件](https://www.bleepingcomputer.com/news/security/check-point-gateways-hacked-via-php2shell-to-deploy-vmware-esxi-wiper/) ⭐️ 7.0/10

Check Point 已发布紧急热修复，修复一个高危漏洞；攻击者自 10 月下旬起利用该漏洞在存在漏洞的 Security Gateway 设备上获取 root 权限并建立持久化。据 BleepingComputer 报道，这些 PHP2Shell 攻击进一步在 VMware ESXi 主机上部署了数据擦除型恶意软件。报道未披露漏洞编号、受影响版本范围或攻击者身份，因此目前只能确认厂商已发布修复、攻击已被实际利用，具体技术细节仍不完整。

rss · BleepingComputer · 11月13日 16:21

**「背景」** Check Point 已发布紧急热修复，修复编号为 CVE-2026-123039 的高危漏洞；该漏洞自 10 月下旬起被攻击者利用，用于获取 root 权限并在设备上建立持久化。据 Check Point 说明，PHP2Shell 漏洞先提供初始访问，随后攻击者通过 DynamicCLI 接口完成权限提升，并部署 PHP Web Shell、持久化后门 TSGA 及其内嵌的 TSProxy 网络组件。

**「实际影响」** 攻击链显示，攻击者会通过 SSH 使用 vpxuser 服务账号横向移动至 VMware ESXi 主机，并投放名为 destroy\_v6 的 Linux ELF 擦除器，递归删除目标目录下所有文件。运行 Check Point Security Gateway 且与 ESXi 环境存在连通的管理员应尽快安装紧急热修复，并重点审查 vpxuser 账号的 SSH 登录记录与网关到 ESXi 主机的访问路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/check-point-patches-zero-day-that-lets-hackers-get-root-access/">Check Point warns of zero-day flaw exploited for root access</a></li>
<li><a href="https://thehackernews.com/2026/11/hackers-exploit-php2shell-flaws-in.html">Hackers Exploit PHP 2 Shell Flaws in Check Point Gateways to Deploy...</a></li>
<li><a href="https://thehackernews.com/2026/11/hackers-exploit-php2shell-flaws-in.html">Hackers Exploit PHP2Shell Flaws in Check Point Gateways to Deploy...</a></li>

</ul>
</details>

**标签**: `#security`, `#malware`, `#VMware ESXi`, `#Check Point`, `#vulnerability exploitation`

---

<a id="item-tech-news-9"></a>
### [ICML 2027 拟推两阶段审稿与互惠审稿人新规](https://www.reddit.com/r/MachineLearning/comments/1xvkxbj/icml_2027_changes_d/) ⭐️ 7.0/10

Reddit 用户根据 ICML 2027 征稿通知（CFP）总结称，大会将采用两阶段审稿：由领域主席决定论文是否进入完整评审，任何一阶段拒稿须经高级领域主席确认，作者可在 2 月 23 日前收到简短理由。新规还限制每人最多出现在 20 份投稿中，每篇论文须从作者名单中指定一名互惠审稿人（每位审稿人最多对应 6 篇），投稿 3 篇及以上者须加入程序委员会，不合规论文可能被直接拒稿。该用户认为影响最大的是每名作者最多只能有一篇论文没有合格的互惠审稿人。上述内容为社区对 CFP 的转述，并非 ICML 官方公告。

reddit · r/MachineLearning · /u/Gravitist · 11月13日 21:53

**「背景」** ICML 2027 的征稿通知提出了投稿与审稿负担挂钩的规则，而同期其他会议也在尝试类似机制：搜索结果中的 IJCAI 2027 主赛道征稿通知同样引入了“作者承诺审稿”（reciprocal reviewing）要求，将其定位为维持审稿流程可持续性的共同责任。ICML 2026 的审稿 FAQ 则显示，该届已计划公开录用论文（以及选择公开的被拒论文）的评审与作者回复，并提到相关提名将提交给 ICML 2027 程序委员会。

**「对作者的影响」** 按该总结，作者在组稿时需提前确认合作者能否承担审稿，否则可用于“无合格互惠审稿人”论文的额度仅有一次；投稿量达到 3 篇的作者还须承担程序委员会审稿工作。依赖本科生、实习生或领域外合作者署名的团队将更直接受到这一规则约束。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://icml.cc/Conferences/2026/PeerReviewFAQ">ICML 2026 Peer Review FAQ</a></li>
<li><a href="https://2027.ijcai.org/ijcai-2027-call-for-papers-main-track/">IJCAI 2027 Call for papers (Main Track) – IJCAI 2027</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#peer-review`, `#conference-policy`, `#icml`, `#research-community`

---

<a id="item-tech-news-10"></a>
### [上海公布交大医学院基因编辑事件调查结果](https://mp.weixin.qq.com/s/p0iC3tcI1yr10EBl2NjUvg) ⭐️ 7.0/10

上海有关部门公布了对上海交通大学医学院一起定制基因编辑治疗事件的调查结果，认定该疗法在临床前研究、伦理审查和知情同意三个环节均存在缺陷。涉事患儿确诊罕见病 Snijders Blok-Campeau 综合征，家属于 2023 年联系仇某某团队定制基因编辑疗法，患儿在 2025 年 3 月注射后因血栓性微血管病死亡，相关论文于 2026 年 2 月发表在《自然》。调查还认定部分人员收受家属财物约 106 万元，仇某某、杨某被开除并取消资格 5 年，相关机构被约谈整改并受到行政处罚。上述内容来自新华社转述的简要报道，具体细节未在现有材料中独立核实。

telegram · zaihuapd · 11月13日 09:24

**「事件背景」** 涉事团队此前在《自然》2026 年 2 月刊发表论文，描述针对 Snijders Blok-Campeau 综合征的基因编辑疗法临床前工作；据 Retraction Watch 2026 年 7 月报道，该论文发表后期刊与校方启动了调查。Science 与 Retraction Watch 的联合调查随后披露了这名 6 岁女孩在接受实验性治疗后死亡的情况，引发对中国基因治疗监管的讨论。

**「对研究者与机构的影响」** 调查将临床前研究、伦理审查和知情同意列为缺陷环节，并同时对个人和机构追责，这意味着开展类似定制化基因编辑治疗的研究团队和所在机构需重新审视超说明书、个体化治疗的伦理审批与知情同意流程；涉事人员被取消资格 5 年，也表明此类违规会直接影响个人执业与研究资格。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://retractionwatch.com/2026/07/30/nature-university-china-investigations-gene-editing-death-science/">Journal, university investigations launched into gene-editing ...</a></li>
<li><a href="https://www.livescience.com/health/genetics/6-year-old-in-china-dies-after-experimental-treatment-investigation-finds-raising-questions-about-the-countrys-gene-therapy-regulations">An experimental gene therapy killed a 6-year-old girl in ...</a></li>

</ul>
</details>

**标签**: `#gene-editing`, `#research-ethics`, `#biotech-regulation`, `#clinical-trials`, `#China`

---

<a id="item-tech-news-11"></a>
### [Python 早期贡献者 Tim Peters 去世，享年 74 岁](https://x.com/Itsfoss/status/2120957452937998716) ⭐️ 7.0/10

Python 创造者 Guido van Rossum 宣布，Python 社区早期贡献者 Tim Peters 去世，享年 74 岁。Peters 是 Python 的第二位真实用户，也是 Timsort 排序算法的作者和《Python 之禅》（PEP 20）的撰写者，并曾在 Python 软件基金会（PSF）董事会任职 13 年。上述信息来自一条转述该消息的社交媒体帖文，未提供更多细节。

telegram · zaihuapd · 11月13日 09:55

**「背景」** Tim Peters 是 Python 早期核心贡献者，以创建 Timsort 混合排序算法和对 CPython 原始实现的重要贡献而知名。据外部资料，他于 1999 年 6 月写下《Python 之禅》（PEP 20），以格言形式概括 Python 的核心设计哲学。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tim_Peters_%28software_engineer%29">Tim Peters (software engineer) - Wikipedia</a></li>
<li><a href="https://grokipedia.com/page/Tim_Peters_%28software_engineer%29">Tim Peters (software engineer) — Grokipedia</a></li>

</ul>
</details>

**标签**: `#python`, `#open-source`, `#community`, `#algorithms`, `#obituary`

---

<a id="item-tech-news-12"></a>
### [DeepSeek 开放应用 API：服务端自动调用搜索、OCR、语音等工具](https://mp.weixin.qq.com/s/78KBHc4-4N5b2vfL9SkutQ) ⭐️ 7.0/10

DeepSeek 于 11 月 13 日开放“全家桶”应用 API，开发者在原有 API 中开启对应参数，即可获得深度思考搜索、文件输入、链接阅读和语音等对话能力，工具调用与上下文拼接由服务端自动完成。V4.1-Flash 模型已在三个接口支持这些能力；Search、Fetch、OCR、ASR、TTS 也可单独调用。官方同时开源了可导入历史对话的前端 Demo（deepseek-ai/chat-demo），并提供了在线体验地址。上述信息来自一条简短的 Telegram 转发，具体接口名称、参数和计费细节尚未披露。

telegram · zaihuapd · 11月13日 14:27

**「背景」** DeepSeek 此前已发布 V4.1-Flash 模型，并公开了对应的技术报告，说明该模型可通过 vLLM 等方式部署使用。此次更新在此基础上把搜索、抓取、OCR、ASR、TTS 等能力同时以独立 API 形式开放，供开发者按需组合调用。

**「对开发者的影响」** 开发者无需自行编排搜索、抓取、OCR 和语音等工具链，只需在现有 API 中开启参数即可获得端到端的对话能力，降低了搭建多模态应用的门槛。需要留意的是，目前仅 V4.1-Flash 在三个接口上支持该能力，其他模型是否兼容、各独立接口的调用限制与价格均未在来源中说明，接入前应向官方文档核实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/news/news261113/">The full DeepSeek App experience, now via API | DeepSeek API Docs</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash/blob/main/DeepSeek_V41_Tech_Report.pdf">DeepSeek _ V 41_Tech_Report.pdf...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#API`, `#LLM tooling`, `#open source`, `#speech/OCR`

---

<a id="item-tech-news-13"></a>
### [SpaceX 裁撤 Grok Imagine 团队约 60 人](https://weibo.com/1642634100/RreMyi69Y) ⭐️ 7.0/10

据新浪科技转述，SpaceX 上周裁撤 Grok Imagine 约 60 名研发人员，仅留少量人员维持这款视频与图像生成工具的基本运转。产品目前仍可正常使用，但专职团队解散后前景不明。报道称，SpaceX 今年 2 月以价值 2500 亿美元股票收购 xAI 后，重心转向 AI 代码工具与 GrokBot 智能体，8 月又以 600 亿美元收购 AI 代码初创公司 Cursor。上述裁员与收购信息均来自单一聚合来源，尚无 SpaceX 或 xAI 的官方确认。

telegram · zaihuapd · 11月13日 15:00

**「背景」** 据 Forbes 报道，SpaceX 于今年 8 月以 600 亿美元收购 AI 编程平台 Cursor，其订阅档位随后与 xAI 的订阅价格对齐。NBC News 则提到，xAI 已于今年 2 月被 SpaceX 收购。这些交易构成了 Grok Imagine 团队调整前公司资源向编程工具倾斜的背景。

**「影响」** 若裁员属实，Grok Imagine 将进入仅维持基本运转的状态，依赖该工具进行视频和图像生成的用户与开发者需为后续功能更新放缓或服务调整做好准备。报道所述战略重心转向代码工具与智能体，也意味着相关团队资源可能进一步向编程类产品集中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.forbes.com/sites/siladityaray/2026/11/02/musk-says-grok-bots-costs-were-unsustainably-high-weeks-after-touting-rapid-growth/">Elon Musk Says Grok Bot Costs Were ‘Unsustainably High’ Amid...</a></li>
<li><a href="https://www.nbcnews.com/tech/tech-news/musks-ai-chatbot-grok-xai-making-sexual-deepfakes-imagine-rcna265855">Musk’s AI chatbot Grok is still making sexual deepfakes</a></li>

</ul>
</details>

**标签**: `#AI industry`, `#layoffs`, `#Grok Imagine`, `#xAI`, `#generative media`

---