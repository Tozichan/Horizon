---
layout: default
title: "Horizon Summary: 2026-11-15 (ZH)"
date: 2026-11-15
lang: zh
---

> 从 52 条内容中筛选出 11 条重要资讯。

---

**科技新闻**
1. [SpaceX 星舰第 15 次试飞成功回收助推器](#item-tech-news-1) ⭐️ 8.0/10
2. [Lovable 生成应用因 RLS 不足泄露护照信息与逾 20 万条私信](#item-tech-news-2) ⭐️ 8.0/10
3. [亚洲多国政府回应英伟达 CEO 黄仁勋离职](#item-tech-news-3) ⭐️ 8.0/10
4. [Show HN：约 200 行纯 JAX 实现 DeepSeek V3 推理](#item-tech-news-4) ⭐️ 7.0/10
5. [Google Project Zero 将漏洞披露期限逐步缩短至 30 天](#item-tech-news-5) ⭐️ 7.0/10
6. [PyPI 新版项目页上线，突出安全与来源信号](#item-tech-news-6) ⭐️ 7.0/10
7. [Cursor 确认安全泄露致恶意 Claude Code 扩展上架](#item-tech-news-7) ⭐️ 7.0/10
8. [谷歌高管用 Gemini 让 Windows 11 跑上折叠 iPhone](#item-tech-news-8) ⭐️ 7.0/10
9. [Cloudflare 以 Apache 2.0 开源 AI 代理浏览器 Kitesurf](#item-tech-news-9) ⭐️ 7.0/10
10. [特斯拉 Cybercab 订阅协议：月租 299 美元，不交费车辆无法运行](#item-tech-news-10) ⭐️ 7.0/10

**财经新闻**
1. [Anthropic IPO 据报不接受中国内地及香港投资者下单](#item-finance-news-1) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [SpaceX 星舰第 15 次试飞成功回收助推器](https://www.spacex.com/launches/starship-flight-15) ⭐️ 8.0/10

SpaceX 在星舰第 15 次试飞（Flight 15）结束时成功用发射塔机械臂捕获了超重型助推器，公司通过官方账号和直播视频公布了这一结果。此次试飞以助推器回收收尾，是星舰走向完全可重复使用运载器的又一步；但来源仅为发射页面和视频链接，未披露飞行高度、速度、助推器状态或复用次数等技术细节。

hackernews · ls612 · 11月14日 21:22 · [社区讨论](https://news.ycombinator.com/item?id=50500963)

**「背景」** SpaceX 的星舰第 15 次试飞于 2026 年 11 月 13 日从得克萨斯州星基地发射。据 Space.com 报道，此次任务原计划用发射塔的“筷子”机械臂回收超重型助推器，但因制导问题中止了回收尝试，助推器最终溅落墨西哥湾；该报道同时指出，这是星舰首次尝试用“筷子”回收上级飞船。

**「影响」** 对关注发射成本的用户和开发者而言，助推器被塔臂捕获意味着回收环节不再依赖着陆腿或海上平台，但能否真正降低单次发射成本，仍取决于热防护能否承受再入、以及同一枚助推器和飞船能否重复飞行——这些在本次来源中均未得到验证。

**「社区讨论」** 有评论者将星舰比作“做对了的航天飞机”，认为其助推器完全复用、飞船叠放在顶部，规避了固体助推器和侧挂构型带来的风险；也有人强调关键在热防护是否可靠，下一步应验证双捕获和同一飞船复飞。另有评论者指出，若助推器多带几吨推进剂或许能同时捕获两级，并称目前尚不清楚最终入轨质量分数，但完全复用优于部分复用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=RHY66XujZ90">Blastoff! SpaceX Starship launches to orbit on Flight 15 , booster ...</a></li>
<li><a href="https://www.space.com/space-exploration/launches-spacecraft/spacex-says-starship-flight-15-booster-aborted-chopsticks-landing-catch-after-launch-due-to-guidance-issue-video">SpaceX still investigating why Starship Flight 15 booster ... | Space</a></li>

</ul>
</details>

**标签**: `#spaceflight`, `#reusable-rockets`, `#spacex`, `#engineering-milestone`

---

<a id="item-tech-news-2"></a>
### [Lovable 生成应用因 RLS 不足泄露护照信息与逾 20 万条私信](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

安全研究人员在 Crissy Field 发布的报告中指出，部分由 Lovable 生成的应用因行级安全（Row-Level Security）配置不足，暴露了护照信息及超过 20 万条私人消息。Lovable 安全负责人 Igor 在评论中确认，根本原因是这些应用的行级安全不足，并称平台会在发布前自动扫描每个应用，另提供免费的深度 SAST 扫描，用户可手动选择“修复”或开启后台自动修复，也可阻止发布。该报告由作者本人确认，但具体受影响应用数量、数据泄露规模及修复完成情况在现有材料中未说明。

hackernews · armcat · 11月14日 17:43 · [社区讨论](https://news.ycombinator.com/item?id=50499017)

**「背景」** 这些应用的数据暴露与 Supabase 的行级安全（RLS）机制直接相关：Supabase 通过自动生成的 Data API 向客户端库暴露 public schema 中的表，若未配置 RLS 策略，数据即可被直接读取。据外部报道，Supabase 于 2026 年 10 月 30 日调整默认行为，新表不再自动暴露给 Data API，但已有项目中的现有表保持原有授权和 RLS 状态，此前开放的表仍然开放。

**「影响与应对」** 对使用 Lovable 构建并连接 Supabase 的开发者而言，此次事件表明默认配置可能不足以保护用户数据，需要主动检查并收紧行级安全策略，而非依赖平台扫描作为唯一防线。评论者指出，Supabase 曾为降低入门门槛而采用较宽松的默认设置，据称已于 10 月 30 日修复，但有报告称既有项目的默认值仍然生效，因此已有项目应单独核实。

**「社区讨论」** 有评论者认为责任不应只归于 Lovable，Supabase 多年前为简化入门而选择的默认配置同样是原因，并称修复后既有项目可能仍沿用旧默认值。另有评论者指出，这类 AI 生成应用数量多、攻击门槛低（仅需在浏览器中检查网络请求即可），普通用户往往不清楚自己所用应用的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.getleakpatrol.com/supabase-october-30-change.html">Supabase&#x27;s October 30 change: what it fixes for your app&#x27;s ...</a></li>
<li><a href="https://dev.to/fixloopdev/supabase-oct-30-why-new-tables-get-42501-and-how-to-fix-grants-rls-2i8k">Supabase Oct 30: why new tables get 42501 (and how to fix ...</a></li>
<li><a href="https://dev.to/dave_thomas_18311ddb9c409/supabases-oct-30-change-what-breaks-what-doesnt-and-the-quick-fix-to-avoid-bg4">Supabase&#x27;s Oct 30 change: what breaks, what doesn&#x27;t, and the ...</a></li>

</ul>
</details>

**标签**: `#security`, `#AI code generation`, `#Supabase`, `#row-level security`, `#data exposure`

---

<a id="item-tech-news-3"></a>
### [亚洲多国政府回应英伟达 CEO 黄仁勋离职](https://techcrunch.com/2026/11/14/asian-governments-react-to-nvidia-ceo-jensen-huangs-exit/) ⭐️ 8.0/10

据 TechCrunch 报道，英伟达 CEO 黄仁勋离职后，亚洲多国政府作出回应。部分政府着手确认芯片供应承诺，另一些则在评估此事对本地项目的影响，或处理正在进行的相关调查。报道未说明黄仁勋离职的具体情况，也未点名涉及哪些政府、承诺内容为何，因此目前无法核实这些反应的具体范围与力度。

rss · TechCrunch AI · 11月14日 16:34

**「背景」** 据《卫报》和路透社报道，黄仁勋于本周四辞去英伟达首席执行官职务，此前有报道称其存在婚外情，其中一段涉及一名疑似中国间谍，英伟达随后任命了临时继任者。此次辞职使这家芯片公司陷入危机，并令外界对其未来产生疑问。

**「对亚洲芯片供应与项目的影响」** 报道显示，部分亚洲政府已着手确认芯片供应承诺，另一些则在评估黄仁勋离职对本地项目的冲击，并处理相关调查。由于原文未点名具体国家或承诺内容，目前无法判断哪些供应安排已获正式确认、哪些仍只是表态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/12/nvidia-ceo-jensen-huang-resigns">Jensen Huang resigns as Nvidia CEO after alleged affairs</a></li>
<li><a href="https://www.reuters.com/business/retail-consumer/nvidia-ceo-jensen-huang-step-down-big-blow-ai-boom-2026-11-12/">Nvidia CEO Jensen Huang resigns in blow to AI boom he helped ...</a></li>
<li><a href="https://techcrunch.com/2026/11/14/asian-governments-react-to-nvidia-ceo-jensen-huangs-exit/">Asian governments react to Nvidia CEO Jensen Huang ’s exit</a></li>

</ul>
</details>

**标签**: `#nvidia`, `#semiconductors`, `#ai-hardware`, `#tech-industry`, `#government-policy`

---

<a id="item-tech-news-4"></a>
### [Show HN：约 200 行纯 JAX 实现 DeepSeek V3 推理](https://github.com/Vaibhaav-Tiwari/deepseek-v3-jax) ⭐️ 7.0/10

开发者 VaibhaavTiwari 在 GitHub 发布了一个 Show HN 项目，用约 200 行纯 JAX 代码从零重写 DeepSeek V3 的推理流程。该项目定位为教学性质的第一性原理实现，而非追求性能的生产级方案；来源未提供吞吐、精度或与官方实现对比的实测数据。评论者 joebarbere 报告称，这是首个在其 RX 7600 XT 16GB 上通过 ROCm 端到端跑通的项目，并指出需要设置 HSA\_OVERRIDE\_GFX\_VERSION=11.0.0，因为 JAX 插件拒绝 gfx1102。

hackernews · VaibhaavTiwari · 11月14日 15:04 · [社区讨论](https://news.ycombinator.com/item?id=50497589)

**「背景」** DeepSeek V3 是 DeepSeek 发布的开源权重模型，Hugging Face 页面显示其参数量为 684B，官方称其性能可与领先的闭源模型相比。该项目并非官方实现，而是用 JAX 从零重写推理流程，因此其价值在于教学与可移植性，而非新的模型能力。

**「实际影响」** 对没有 CUDA 环境的 AMD 用户而言，该项目提供了一个可参考的 JAX + ROCm 推理起点，但需按评论所述手动覆盖 GPU 架构版本变量，且目前仅有单个用户报告在特定显卡上跑通，兼容性尚未得到广泛验证。

**「社区讨论」** 多位评论者肯定从零复现模型的学习价值，armcat 表示这让他想重新拾起 JAX，itsthecourier 称会照着复刻用于学习。mattfrommars 则询问是否有适合熟悉 Java/Python 的普通工程师理解推理原理的学习路线，但评论中未给出具体答案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V3">deepseek -ai/ DeepSeek - V 3 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#jax`, `#deepseek`, `#model-inference`, `#open-source`, `#rocm`

---

<a id="item-tech-news-5"></a>
### [Google Project Zero 将漏洞披露期限逐步缩短至 30 天](https://projectzero.google/2026/11/disclosure-policy.html) ⭐️ 7.0/10

Google Project Zero 宣布调整漏洞披露政策：自即日起维持“Full 90”政策，即在向厂商报告漏洞 90 天后公开；2027 年 2 月 2 日起改为“Full 60”，即 60 天后公开；2028 年 1 月 3 日起进一步改为“Full 30”，即 30 天后公开。这是分阶段公布的收紧计划，并非已经生效的 30 天期限。

hackernews · hacb · 11月14日 11:13 · [社区讨论](https://news.ycombinator.com/item?id=50496051)

**「背景」** Project Zero 自 2021 年起实行“90 + 30”漏洞披露政策，即给厂商最多 90 天修复时间，另加 30 天补丁推送缓冲期（tool-2-2）。该团队在政策说明中称，AI 辅助的漏洞发现与利用改变了威胁格局，因此决定收紧披露时限（tool-2-2）。

**「影响」** 对依赖较长修复周期的厂商和开源项目而言，披露窗口将逐步压缩到 30 天，补丁发布与协调披露的时间安排需要相应提前。有评论者以 Ubuntu 为例，认为其需要的修复时间远超这一期限。

**「社区讨论」** 评论者对缩短期限的可行性存在分歧：有人以 Ubuntu 为例认为许多项目无法在如此短的时间内完成修复；也有人主张既然 Google 不依赖漏洞赏金获利，就应更早公开，否则难以迫使被报告方修复。另有评论提出，发现漏洞的公司也应向厂商或开源项目提供同等条件的产品访问权限，以便其复现和修补问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://projectzero.google/2026/11/disclosure-policy.html">Policy and Disclosure: 2026 Edition - Project Zero</a></li>

</ul>
</details>

**标签**: `#vulnerability-disclosure`, `#security`, `#open-source`, `#google`, `#policy`

---

<a id="item-tech-news-6"></a>
### [PyPI 新版项目页上线，突出安全与来源信号](https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/) ⭐️ 7.0/10

PyPI 已上线重新设计的项目页面，在文件列表等处更清晰地展示安全与来源（provenance）信号。社区评论给出的例子显示，datasette 的项目页带有 provenance 标记，而 dlt 没有。PyPI 博客称此次 UI 更新已完成，但现有材料未说明具体检测规则、覆盖范围或强制要求。

hackernews · rbanffy · 11月14日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50497892)

**「背景」** PyPI 此前已推出 Trusted Publishing（基于 OIDC 的免密钥上传方式），并在此基础上引入 Sigstore attestations，使通过受信任发布流程上传的包可附带来源证明。此次改版是把这些既有的来源与安全信号更直接地呈现在项目页面上，而非首次引入签名机制。

**「对使用者的影响」** 对依赖 PyPI 的开发者而言，项目页现在能直接区分是否附带 provenance 信息，可作为评估包来源的参考。但评论者 cowlevel 指出，这类信号主要用于发现原本正常、后来被入侵但私钥未泄露的项目，并不能识别本身就是恶意的包，因此不能替代其他审查手段。

**「社区讨论」** 有评论者 time4tea 担心信任体系过度依赖大型云服务商，可能造成锁定；samhclark 则希望基于 Sigstore 的短时“无密钥”签名更普及，并推动第三方 CI/CD 服务支持安全的 OIDC 处理。mhils 还提到，希望 trusted publishing 支持可复用工作流（reusable workflows）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.trailofbits.com/2024/11/14/attestations-a-new-generation-of-signatures-on-pypi/">Attestations : A new generation of signatures on PyPI - The Trail of...</a></li>
<li><a href="https://www.pyblog.in/programming/python/pypi-security-in-2026-trusted-publishing-sigstore-and-whats-next/">PyPI Security 2026: Trusted Publishing and Sigstore Guide</a></li>

</ul>
</details>

**标签**: `#supply-chain-security`, `#pypi`, `#package-management`, `#provenance`, `#open-source`

---

<a id="item-tech-news-7"></a>
### [Cursor 确认安全泄露致恶意 Claude Code 扩展上架](https://www.bleepingcomputer.com/news/security/cursor-confirms-security-breach-led-to-malicious-claude-code-extension/) ⭐️ 7.0/10

Cursor 确认发生安全泄露：攻击者利用从 AI 基础设施提供商 Fireworks AI 窃取的凭据，通过 Cursor 市场分发了一个恶意 Claude Code 扩展。目前公开信息仅来自 Cursor 的确认和简短报道，尚未披露攻击的具体技术路径、受影响用户范围或修复措施。

rss · BleepingComputer · 11月14日 17:27

**「事件背景」** 据网络安全新闻网站报道，Cursor 将 10 月的这起安全事件追溯到 Fireworks AI 泄露的一把访问密钥：攻击者利用该密钥窃取了历史编码代理记录，并从中找到更多凭据，最终在 Cursor 市场的缓存中放置了被植入后门的 Claude Code 扩展。Cursor 在 2026 年 11 月 13 日发布的事件更新中说明了这一攻击链条。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/cursor-data-breach/">Cursor Reveals How a Leaked Fireworks AI Key Led to a ...</a></li>
<li><a href="https://www.unite.ai/cursor-traces-breach-to-access-key-exposed-by-fireworks-ai/">Cursor Traces Breach to Access Key Exposed by Fireworks AI</a></li>

</ul>
</details>

**标签**: `#security`, `#supply-chain`, `#AI coding tools`, `#Cursor`, `#Claude Code`

---

<a id="item-tech-news-8"></a>
### [谷歌高管用 Gemini 让 Windows 11 跑上折叠 iPhone](https://www.windowslatest.com/2026/11/14/windows-11-can-run-on-apples-foldable-iphone-and-googles-ai-boss-proved-it-using-gemini-years-after-microsoft-gave-up-on-windows-phones/) ⭐️ 7.0/10

Google AI Studio 产品设计负责人 Ammaar Reshi 称，他借助 Gemini 4 Carbon 让 Windows 11 24H2 在苹果折叠手机 iPhone Duo 上本地运行，并公开了操作视频。所用开源项目 WindowsiOS 无需越狱，通过基于 JIT 的 ARM64 翻译层运行代码，并支持微软 Prism 运行部分传统应用；镜像约 12 GB，需要 Apple Silicon Mac 和开发工具。上述细节来自单一来源的报道与演示，尚未获得独立验证。

telegram · zaihuapd · 11月14日 06:52

**「背景」** Windows on ARM 依赖 ARM64 指令集运行，而苹果设备上的 Windows 通常需要虚拟化或翻译层才能启动。此次演示称通过开源项目 WindowsiOS 的 JIT 翻译方式在本地运行 Windows 11 24H2，并借助微软 Prism 兼容部分传统应用；相关细节目前仅来自单一来源，尚未获得独立验证。

**「实际影响」** 这目前更像工程演示而非可用产品：12 GB 镜像和 Apple Silicon Mac 加开发工具的前置条件，意味着普通用户难以直接复现；对关注 Windows on ARM 与模拟层的人来说，其价值在于展示了 JIT 翻译配合 Prism 的可行性边界。

**标签**: `#Windows on ARM`, `#emulation`, `#Apple hardware`, `#Gemini`, `#open source`

---

<a id="item-tech-news-9"></a>
### [Cloudflare 以 Apache 2.0 开源 AI 代理浏览器 Kitesurf](https://www.phoronix.com/news/Cloudflare-Kitesurf-Open-Source) ⭐️ 7.0/10

Cloudflare 以 Apache 2.0 协议开源了面向 AI 代理的无状态浏览器 Kitesurf，代码已发布在 GitHub。它基于 Cloudflare Workers 构建，无需浏览器容器即可解析 HTML、处理 CSS 并执行 JavaScript。Cloudflare 称其目标是给 AI 代理一个轻量、高效的浏览器，相比 Chromium 占用更少 CPU 和内存，并能在全球 Workers 网络上按需扩展；这些性能对比目前属于厂商说法，尚未见到独立测量结果。

telegram · zaihuapd · 11月14日 09:33

**「背景」** Cloudflare 此前已于 2026 年 8 月发布 Kitesurf，将其定位为完全运行在 Workers 之上、面向 AI 代理的无状态浏览器，并在测试阶段免费提供（tool-1-2、tool-1-3）。此次开源意味着该产品从托管服务走向以 Apache 2.0 协议公开代码，供开发者自行使用和审查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/kitesurf/">Introducing Kitesurf: The agent-first browser that runs in V8 ...</a></li>
<li><a href="https://developers.cloudflare.com/changelog/post/2026-08-06-kitesurf/">Introducing Kitesurf, an agent-first browser on Browser Run</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#Cloudflare Workers`, `#open source`, `#browser infrastructure`, `#web rendering`

---

<a id="item-tech-news-10"></a>
### [特斯拉 Cybercab 订阅协议：月租 299 美元，不交费车辆无法运行](https://www.tesla.com/configurator/api/v4/terms?category=autonomy_subs&amp;amp;locale=en_US&amp;amp;model=cc&amp;amp;saleType=Sale) ⭐️ 7.0/10

特斯拉公布的 Cybercab 自主驾驶订阅协议显示，车辆售价为 29,990 美元，车主须每月支付 299 美元订阅费，否则车辆无法运行；特斯拉可提前一个月通知调价。欠费或违规使用可能导致订阅被暂停或取消，累计三次警告则停用自动驾驶一周。车辆仅在指定区域运行，未经授权不得接入网约车、配送或租赁平台。上述条款来自 Telegram 频道转述的第三方报道，尚未经特斯拉官方或独立渠道核实。

telegram · zaihuapd · 11月15日 01:10

**「背景」** Cybercab 是特斯拉面向无人驾驶出租车场景推出的车型，其订阅条款将车辆使用与按月付费绑定。据 Electrek 报道，Cybercab 与用于 Robotaxi 的 Model Y 采用相同的 AI4 硬件并运行相同的自动驾驶软件，但面向普通车主的 FSD 仍需人类监督，这一差异是理解该订阅模式适用范围的前提。

**「对车主的影响」** 按协议条款，购车并不等于获得完整使用权：车主需持续付费才能保持车辆可运行，且使用范围与商业运营受到限制。Electrec 指出，Cybercab 与用于 Robotaxi 的 Model Y 采用相同的 AI4 硬件和自动驾驶软件，但面向普通车主的 FSD 仍需人类监督，这意味着同一硬件平台上的能力与责任边界因用途而异。

**标签**: `#autonomous driving`, `#Tesla`, `#subscription pricing`, `#robotaxi`, `#tech industry`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [Anthropic IPO 据报不接受中国内地及香港投资者下单](https://m.economictimes.com/markets/us-stocks/news/anthropic-ipo-share-orders-from-china-are-said-to-be-rebuffed/articleshow/135809948.cms) ⭐️ 8.0/10

据知情人士消息，Anthropic 的首次公开募股（IPO）不接受中国内地和香港投资者下单，限制与 ITAR（国际武器贸易条例）出口管制有关；发行定价日为 11 月 18 日，次日上市，代码 ANT，拟以 1.4 万亿美元估值募资至多 904 亿美元。

telegram · zaihuapd · 11月14日 10:18

**「背景」** Anthropic 已于 2026 年 10 月 26 日向美国证券交易委员会公开递交 S-1 上市文件，此前曾安排投行与投资者会面，争取抢先竞争对手 OpenAI 登陆公开市场（tool-1-3、tool-1-2）。

**「影响」** 部分受限资金据报转向英属维尔京群岛信托、SPV 和掉期结构参与认购，而整体认购需求约为可售股份的 6 倍，显示限制并未明显压低需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/07/15/anthropic-ipo-banks-investor-meetings.html">Anthropic moves closer to IPO as bankers line up investor meetings</a></li>
<li><a href="https://www.fxstreet.com/news/anthropic-ipo-filing-reveals-rapid-growth-as-investors-weigh-an-80-billion-loss-202610270748">Anthropic IPO filing reveals rapid growth as investors weigh an $80...</a></li>

</ul>
</details>

**标签**: `#IPO`, `#Anthropic`, `#export controls`, `#cross-border investment`, `#capital markets`

---