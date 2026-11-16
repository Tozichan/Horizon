---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 52 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Meta FAIR 与 NYU 训练 200+ 多模态模型：视觉编码器预训练非必需](#item-tech-news-1) ⭐️ 8.0/10
2. [世界模型驱动的多人游戏：每名玩家本地生成视角](#item-tech-news-2) ⭐️ 8.0/10
3. [美团开源 LongCat-2.5，称训练全程未用英伟达 GPU](#item-tech-news-3) ⭐️ 8.0/10
4. [MacBook Pro OLED 屏幕的 PWM 调光争议](#item-tech-news-4) ⭐️ 7.0/10
5. [Protomaps 让自托管地图瓦片变得便宜又简单](#item-tech-news-5) ⭐️ 7.0/10
6. [国会拟收紧 AI 芯片出口规则，要求黄仁勋作证](#item-tech-news-6) ⭐️ 7.0/10
7. [FBI 警告 AI 黑客框架 ARTEX 被用于全球网络攻击](#item-tech-news-7) ⭐️ 7.0/10
8. [开源工具称在 B300 上将 pageable cudaMemcpy 提速约 5 倍](#item-tech-news-8) ⭐️ 7.0/10

**财经新闻**
1. [中美俄领导人将在深圳 APEC 场边首次举行三方会晤](#item-finance-news-1) ⭐️ 9.0/10
2. [美法官驳回美光、三星、SK 海力士 DRAM 价格操纵案撤诉动议](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Meta FAIR 与 NYU 训练 200+ 多模态模型：视觉编码器预训练非必需](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR 与 NYU 的研究者从零训练了 200 多个多模态大语言模型（LLM 本身也从头训练），在相同数据和计算预算下分别检验视觉编码器的三个设计选择：独立预训练、仅视觉使用的参数、以及编码器置于 LLM 之前。结果显示，独立预训练是可选的——用对比学习、自监督和两种描述生成目标预训练的编码器，在同等计算下最多只能与随 LLM 一起从零训练的编码器打平；即便把 MetaCLIP 预训练延长 6.5 倍，ImageNet 线性探测准确率从 80.4% 升至 84.4%，VQA 表现也未提升。但仅视觉参数是必需的：无编码器模型在 0.6B 到 6.4B 各规模上均落后，约需 3 倍计算才能追平。作者同时披露自己是论文作者之一。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**「背景」** 多模态大模型长期沿用“独立预训练视觉编码器 + 接入语言模型”的架构，但不同团队的做法已明显分化：Gemma 4 12B 去掉了编码器，Kimi K3 从零训练编码器，Inkling 2 Small 则重新引入编码器。由于已发布模型在训练数据和算力上各不相同，且很少单独核算编码器预训练成本，这些差异无法直接比较，这正是该研究试图用统一预算拆解各设计选择的原因。

**「对架构选择的影响」** 研究还提出“In-fusion”方案：在 LLM 前 8 层加入零初始化的仅视觉权重，文本 token 不使用这些参数，在 1.7B 至 6.4B 规模上与前置编码器持平，首 token 时间约低 13%。在 1.7B 配置下，第 1–8 层的仅视觉分支达到 45.0 VQA（编码器为 44.4），而文本共享这些参数时为 42.3，放在最后 8 层则为 35.1。这意味着团队若想省去独立编码器，应保留视觉专用参数，而非简单地把视觉 token 直接送入 LLM。

**标签**: `#multimodal LLMs`, `#vision encoders`, `#model architecture`, `#training methodology`, `#research`

---

<a id="item-tech-news-2"></a>
### [世界模型驱动的多人游戏：每名玩家本地生成视角](https://www.reddit.com/r/MachineLearning/comments/1xx4ta3/we_made_a_multiplayer_game_where_each_players/) ⭐️ 8.0/10

一个团队用其上月开源的 10 人 CS:GO 机器人对局数据集（约 3,958 小时，所有视角与输入以 16 Hz 对齐）训练了世界模型，并推出了可多人游玩的免费测试版。轻量服务器只负责同步游戏状态，每名玩家在自己的 GPU 上运行模型，根据服务器状态、自身操作和上一帧，通过扩散 Transformer 生成自己的画面。目前范围有限：仅一张小地图、只用手枪，细节仍不理想；运行需要 RTX 3080 或更高配置，另有实验性 Mac 版本，项目与 Valve 无关。

reddit · r/MachineLearning · /u/bengal7ion · 11月15日 19:46

**「背景」** 该项目建立在团队上月公开的 CS:GO 机器人对局数据集之上：约 3,958 小时、10 名玩家、所有视角与输入按 16 Hz 对齐。据项目方介绍，CS:GO 自带机器人和 GOTV 逐 tick 录制功能，因此无需招募真人或录屏即可批量生成对局数据，首个数据集来自一张地图、33 台服务器、五天的运行。

**「对玩家的影响」** 想试玩的用户需要 RTX 3080 级别的本地 GPU，因为画面生成发生在客户端而非服务器；Mac 用户只能使用实验性版本，兼容性和性能尚无保证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vor.tech/">VOR.TECH — open multiplayer gameplay data for world models</a></li>

</ul>
</details>

**标签**: `#world models`, `#diffusion transformers`, `#generative games`, `#open datasets`, `#real-time inference`

---

<a id="item-tech-news-3"></a>
### [美团开源 LongCat-2.5，称训练全程未用英伟达 GPU](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 8.0/10

美团 LongCat 团队在模型正式发布一周后公开了 LongCat-2.5 的权重，采用 MIT 许可证，允许商用。该模型面向能自主完成冗长多步骤任务（尤其是编程）的智能体，每个 token 激活约 480 亿参数，支持文本、图像和视频输入。官方称训练全程使用华为升腾加速卡、未使用英伟达 GPU，并称其在 Terminal Bench v2.1 上得分 88.4，略低于 Claude Opus 5 的 89.1。上述训练硬件与跑分均为厂商说法，来源未提供独立验证或详细技术说明。

telegram · zaihuapd · 11月15日 11:08

**「背景」** LongCat-2.5 是美团 LongCat 团队发布的智能体模型，总参数 1.6 万亿，采用混合专家（MoE）架构，每个 token 激活约 480 亿参数。据 The Decoder 报道，其自托管指南仅覆盖华为升腾硬件，示例部署运行在 194 块升腾芯片上，美团未提及英伟达 GPU。

**「影响」** MIT 许可证意味着开发者可直接将权重用于商业产品，但需自行评估厂商未披露的训练细节与基准成绩。若升腾训练的说法成立，则表明大规模智能体模型存在英伟达之外的可行训练路径，不过目前尚无第三方复现或硬件配置细节可供核实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/">Meituan releases a 1.6-trillion-parameter agent model that ...</a></li>
<li><a href="https://phemex.com/news/article/meituan-opensources-16tparameter-longcat25-model-trained-entirely-on-domestic-chinese-hardware-103629">Meituan LongCat-2.5: 1.6T MoE AI Model Trained on Huawei Chi ...</a></li>

</ul>
</details>

**标签**: `#open-source AI`, `#LLM training`, `#Huawei Ascend`, `#agent models`, `#AI hardware`

---

<a id="item-tech-news-4"></a>
### [MacBook Pro OLED 屏幕的 PWM 调光争议](https://macanorak.com/the-macbook-pros-oled-pwm-problem-when-a-better-display-becomes-worse-to-use/) ⭐️ 7.0/10

MacAnorak 发表技术分析文章，指出 MacBook Pro 的 OLED 屏幕采用 PWM（脉冲宽度调制）调光，可能引发对闪烁敏感用户的不适。文章引用的 240Hz PWM 频率在社区中受到质疑：有评论者称自己复核测试数据后认为，串联 OLED 的两层可能各以 480Hz、相位相差 180 度工作，在常用亮度下叠加出约 960Hz 的有效频率。目前这些频率数字均来自文章与评论者的各自解读，尚无独立测量结果确认。

hackernews · MacAnorak · 11月15日 13:15 · [社区讨论](https://news.ycombinator.com/item?id=50506719)

**「背景」** 此前已有测试指出，新款 14 英寸 MacBook Pro 的 PROLED XDR 屏幕在亮度低于 99% 时采用约 240 Hz 的 PWM 调光，频闪深度约 56%，部分 PWM 敏感用户因此报告眼疲劳、头痛或恶心（tool-1-1、tool-1-2）。作为对照，搭载 Mini-LED 的 M4 Pro MacBook Pro 测得调制频率约 14,880 Hz，约为该串联 OLED 方案的 62 倍（tool-1-3）。

**「对敏感用户的影响」** 对闪烁敏感的用户在选购或长时间使用该机型前，值得先实际体验屏幕在低亮度下的表现；评论者还提到，除 PWM 外，白光 LED 的显色指数（CRI）和 LCD 的运动模糊也可能造成眼部不适，说明屏幕舒适度并非只由 PWM 频率决定。

**「社区讨论」** 讨论的焦点是实际 PWM 频率：legitronics 认为测试设备可能只捕捉到 240Hz，而串联 OLED 两层反相叠加后有效频率可达 960Hz；achr2 则对 Apple 采用如此低的频率表示意外，并引用研究称人眼可感知高于屏幕刷新率两倍的闪烁。另有 concussion 经历者表示，自己对所有屏幕都敏感，而不只是高亮度 OLED。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.appleheadlines.com/macbook-pro-oled-eye-strain-pwm-flicker/">MacBook Pro OLED Eye Strain &amp; PWM Flicker: 7 Moves - AH</a></li>
<li><a href="https://macbreeze.com/proled-macbook-pro-pwm-dimming-eye-strain/">PROLED MacBook Pro Users Report Eye Strain Driven by Low ...</a></li>
<li><a href="https://techbytes.app/posts/the-macbook-pros-oled-pwm-problem-when-a-better-display/">The MacBook Pro&#x27;s OLED PWM Problem: When a &#x27;Better&#x27; Display ...</a></li>

</ul>
</details>

**标签**: `#OLED displays`, `#PWM flicker`, `#hardware`, `#display technology`, `#accessibility`

---

<a id="item-tech-news-5"></a>
### [Protomaps 让自托管地图瓦片变得便宜又简单](https://bruceroettgers.eu/blog/protomaps/) ⭐️ 7.0/10

一篇博客文章与 Hacker News 讨论介绍了 Protomaps 如何让开发者以较低成本自托管地图瓦片，核心是 PMTiles 格式及相关工具链。讨论中，开发者提到用 Cloudflare R2 托管瓦片、用命令行工具 gloss 查看 PMTiles，以及基于 Protomaps 构建实际应用。这些内容属于社区经验分享，并非厂商发布的性能或成本基准；来源未提供具体版本号、价格数字或独立测量结果。

hackernews · bcye · 11月15日 19:26 · [社区讨论](https://news.ycombinator.com/item?id=50509837)

**「背景」** Protomaps 提供可免费定制、以单个静态文件形式部署在云存储上的世界地图，其 PMTiles 规范为公开领域或 CC0 许可。此前已有将其作为“无服务器”地图瓦片提供方接入自托管方案、以及部署到 Supabase Storage 的实践，本次讨论延续了这条自托管地图瓦片的技术路线。

**「实际影响」** 对构建位置类应用的开发者而言，自托管瓦片可减少对 Mapbox、Google Maps 等商业服务的依赖，并便于控制隐私与访问权限。但社区讨论指出，基础底图瓦片体积较小、成本可控，高分辨率卫星影像随缩放级别上升会迅速膨胀，有开发者因存储预估在 z17 停止，全球高分辨率覆盖可能达到数百 TB。

**「社区讨论」** 有评论推荐类似项目 OpenFreeMap，称其公共实例免费且无请求限制、无需 API 密钥。另有开发者表示，若使用 Mapbox 或 Google Maps 就不会考虑做自己的 Wikipedia 步行游戏，Protomaps 让这个副项目变得可负担；也有人提到 Cartes.app 过去付费使用 Maptiler。这些均为个人经验与观点，不构成对成本或性能的独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://protomaps.com/">Protomaps - The open source map in a file</a></li>
<li><a href="https://github.com/Rezivure/Grid-Protomaps">Rezivure/Grid- Protomaps : The Protomaps &quot;serverless&quot; map tile ...</a></li>
<li><a href="https://www.youtube.com/watch?v=l7QBpiLRwJc">Self - host Maps with Protomaps and Supabase Storage - YouTube</a></li>

</ul>
</details>

**标签**: `#maps`, `#self-hosting`, `#open-source`, `#PMTiles`, `#geospatial`

---

<a id="item-tech-news-6"></a>
### [国会拟收紧 AI 芯片出口规则，要求黄仁勋作证](https://www.theverge.com/ai-artificial-intelligence/1033984/congress-export-rules-ai-chips-china) ⭐️ 7.0/10

在涉及前英伟达 CEO 黄仁勋与一名疑似中国间谍的丑闻之后，美国国会两党议员表示支持多项收紧 AI 芯片出口限制的措施和法案。参议院少数党领袖查克·舒默称黄仁勋和特朗普政府需要向国会作出交代，参议院银行委员会主席蒂姆·斯科特已致信黄仁勋和商务部长霍华德·卢特尼克，要求他们公开向该委员会作证。报道未说明具体法案条款、生效时间或适用范围，相关立法仍处于推动阶段而非已生效的规则。

rss · The Verge · 11月15日 19:15

**「背景」** 据 CBS News 报道，黄仁勋因与一名疑似中国间谍的婚外情丑闻辞去英伟达 CEO 职务，即刻生效，公司董事会在周四宣布了这一消息。维基百科条目称，这名女子是新加坡公司 Megaspeed 的高管，美国情报来源怀疑她已被中国国家安全部招募。The Verge 的报道指出，国会两党正是在此事件后推动收紧 AI 芯片出口规则，并要求黄仁勋等英伟达高管作证。

**「潜在影响」** 若相关立法推进，向中国出口先进 AI 芯片的许可审查可能进一步收紧，Nvidia 等厂商的对华销售与合规流程将直接受影响。目前报道仅显示两党表达支持并提出作证要求，具体法案条款、生效时间与适用范围均未确认，企业尚无法据此调整出货计划。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Jensen_Huang_spying_scandal">Jensen Huang spying scandal - Wikipedia</a></li>
<li><a href="https://www.cbsnews.com/news/nvidia-ceo-jensen-huang-resigns/">Nvidia CEO Jensen Huang resigns in wake of affair with woman ...</a></li>
<li><a href="https://www.cbsnews.com/news/jensen-huang-nvidia-resignation-scandal-timeline/">Timeline of a scandal: How Jensen Huang&#x27;s abrupt resignation ...</a></li>
<li><a href="https://www.zerohedge.com/political/preserve-all-evidence-huang-out-nvidia-democrats-want-every-record-his-calls-trump">Preserve All Evidence: With Huang Out At Nvidia ... | ZeroHedge</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#export controls`, `#Nvidia`, `#technology policy`, `#semiconductors`

---

<a id="item-tech-news-7"></a>
### [FBI 警告 AI 黑客框架 ARTEX 被用于全球网络攻击](https://www.bleepingcomputer.com/news/security/fbi-warns-artex-ai-hacking-tool-is-powering-global-cyberattacks/) ⭐️ 7.0/10

FBI 警告称，一个名为 ARTEX 的 AI 驱动渗透测试框架正被攻击者用来自动化针对全球组织的网络攻击。FBI 将该工具与近期一起 ConnectWise 供应链入侵事件联系起来，该事件导致 Microsoft 365 客户环境被攻破。现有报道未披露 ARTEX 的具体版本、技术细节或受影响组织的数量。

rss · BleepingComputer · 11月15日 18:29

**「背景」** ARTEX 是一个基于 Go 语言开发的智能体式 AI 渗透测试框架，可将用自然语言描述的高层战术目标转化为由 AI 智能体执行的机器命令，除设定初始目标外几乎无需人工干预，并支持接入包括前沿模型在内的多种 AI 模型。据 The Hacker News 报道，微软已披露近期 ConnectWise Cloud Backup 应用供应链入侵事件背后是一个被命名为 Storm-0940 的中国国家关联行为体，该行为体在此次事件中使用了 ARTEX。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://therecord.media/artex-ai-tool-fbi-flash-alert">FBI flash alert says Artex tool automating cyberattacks at ‘machine...</a></li>
<li><a href="https://thehackernews.com/2026/10/china-linked-hackers-use-artex-ai.html">China-Linked Hackers Use ARTEX AI Agents in ConnectWise Supply...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#AI`, `#supply-chain`, `#FBI`, `#hacking-tools`

---

<a id="item-tech-news-8"></a>
### [开源工具称在 B300 上将 pageable cudaMemcpy 提速约 5 倍](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 7.0/10

Reddit 用户 /u/makneeee 发布了一个名为 cudamemcpy-tuner 的开源工具，声称能加速 cudaMemcpy 的 pageable 主机与设备间传输。作者给出的示例是在 B300 上复制 1 GB uint8 张量，CPU→GPU 带宽从 10.2 GB/s 提升到 51.5 GB/s，约 5 倍。该结果来自作者自己的单条基准脚本，通过 \`cmt tune -- python bench.py\` 运行，并非独立复测；优化范围限于 pageable 传输，不涉及 pinned 内存路径。

reddit · r/MachineLearning · /u/makneeee · 11月15日 18:20

**「背景：pageable 与 pinned 内存传输」** CUDA 的主机到设备拷贝分为 pageable（可分页）和 pinned（页锁定）两类：pageable 内存可能被操作系统换出，传输时通常需要经过中间缓冲区；pinned 内存被锁定在 RAM 中，可直接通过 DMA 在 CPU 与 GPU 间搬运，因此往往更快，也是重叠拷贝与计算的前提。NVIDIA 的文档指出，两者使用相同的 cudaMemcpy\(\) 调用语法，可用 bandwidthTest 对比传输速率。该帖所称的优化正是针对 pageable 传输这一通常较慢的路径。

**「实际影响」** 如果该加速在更多负载下成立，依赖 pageable 内存做主机与设备拷贝的 PyTorch 用户和系统开发者可能获得明显更低的传输开销，而无需改动现有代码，只需在命令前加上 \`cmt tune\`。不过目前只有作者提供的一个基准示例，实际收益可能随张量大小、传输方向和驱动版本变化，采用前应自行复测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA Technical...</a></li>
<li><a href="https://stackoverflow.com/questions/50184146/cuda-pinned-memory-vs-pageable-memory-tradeoffs">optimization - CUDA - Pinned Memory vs. Pageable Memory ...</a></li>
<li><a href="https://www.linkedin.com/pulse/supercharging-data-transfers-cuda-power-page-locked-pinned-mohapatra-bejec">Supercharging Data Transfers in CUDA: The Power of Page-Locked...</a></li>

</ul>
</details>

**标签**: `#cuda`, `#gpu-memory`, `#performance-optimization`, `#machine-learning-systems`, `#open-source-tools`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中美俄领导人将在深圳 APEC 场边首次举行三方会晤](https://apnews.com/article/trump-xi-putin-summit-china-5fe92253ef38100bae913834a9b74d72) ⭐️ 9.0/10

中国外交部发言人宣布，中美俄三国领导人计划于 11 月 19 日在深圳 APEC 峰会期间举行三方会晤，会晤在 APEC 场边举行，不属于 APEC 正式议程。媒体称这将是三国领导人首次专门举行三方会晤。

telegram · zaihuapd · 11月16日 01:38

**「背景」** 2026 年 APEC 峰会定于 11 月 18 日至 19 日在深圳举行，这是中国自 2014 年以来首次主办该会议。此次三方会晤安排在 APEC 正式议程之外，媒体称这将是中美俄三国领导人首次专门举行三方会晤。

**「影响」** 会晤本身尚未公布任何具体协议或政策调整，因此目前无法确认对贸易、市场或企业的直接影响；分析人士对成果预期不高，认为北京可能更多将其作为外交姿态展示。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/2026%E5%B9%B4%E4%B8%AD%E5%9B%BDAPEC%E5%B3%B0%E4%BC%9A">2026年中国APEC峰会 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.gessymorgan.com/apec-2026-china/">APEC 2026 China: Shenzhen Summit Dates and Agenda</a></li>
<li><a href="https://www.scmp.com/topics/2026-xi-trump-putin-trilateral-meeting">2026 Xi-Trump-Putin trilateral meeting: Latest News and ...</a></li>
<li><a href="https://cepa.org/article/a-us-china-russia-summit-whats-at-stake/">A US-China-Russia Summit: What’s at Stake? - CEPA</a></li>

</ul>
</details>

**标签**: `#geopolitics`, `#APEC`, `#US-China-Russia`, `#diplomacy`, `#trade policy`

---

<a id="item-finance-news-2"></a>
### [美法官驳回美光、三星、SK 海力士 DRAM 价格操纵案撤诉动议](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 7.0/10

美国法官 Noël Wise 驳回美光、三星和 SK 海力士要求撤销 DRAM 价格操纵集体诉讼的动议，认为原告提交的新证据足以让三家厂商同步限供、价格至多上涨 500%的指控成立为“合理”。这是程序性裁定，并非最终认定三家公司负有责任；它们须在 12 月 7 日前回应，案件管理会议定于 2027 年 1 月。

telegram · zaihuapd · 11月15日 16:39

**「背景」** 美光、三星和 SK 海力士此前请求驳回这起集体诉讼，理由是存储芯片行业竞争激烈，各家公司只是像鹰一样互相紧盯对手的动向；法官 Noël Wise 认为，原告指控的行为已超出这种正常竞争观察。

**「影响」** 若诉讼推进，购买内存芯片的电脑、手机及服务器厂商可能面临更高的采购成本或供应不确定性；但当前仅为驳回撤诉动议的程序性裁定，尚未认定三家公司存在违法行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge">Judge denies motion to dismiss DRAM price - fixing lawsuit against...</a></li>
<li><a href="https://www.techpowerup.com/354863/samsung-sk-hynix-and-micron-fail-to-get-dram-antitrust-suit-dismissed">Samsung , SK hynix , and Micron Fail to Get DRAM Antitrust Suit ...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge">Judge denies motion to dismiss DRAM price -fixing... | Tom&#x27;s Hardware</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#price-fixing litigation`, `#semiconductors`, `#Micron`, `#Samsung/SK Hynix`

---