---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 53 条内容中筛选出 9 条重要资讯。

---

**科技新闻**
1. [Telegram 传闻称黎曼猜想已通过 Lean 验证](#item-tech-news-1) ⭐️ 10.0/10
2. [OpenRouter 披露推理供应商数据处理事件](#item-tech-news-2) ⭐️ 7.0/10
3. [博客称 Anthropic 2028 年电力 87%来自天然气、11%来自煤炭](#item-tech-news-3) ⭐️ 7.0/10
4. [FBI 与 USDA 据报遭黑客入侵，FBI 目标为 NCIC 数据库](#item-tech-news-4) ⭐️ 7.0/10
5. [Rackspace Spot 遭入侵，客户 Kubernetes 密钥被访问](#item-tech-news-5) ⭐️ 7.0/10
6. [微软 Entra Connect Health 漏洞遭利用，租户数据被窃](#item-tech-news-6) ⭐️ 7.0/10

**财经新闻**
1. [美股科技股大跌，亚洲多地出台稳市措施](#item-finance-news-1) ⭐️ 9.0/10
2. [英媒指太子集团相关人员涉英伟达芯片对华走私](#item-finance-news-2) ⭐️ 7.0/10
3. [中国要求美国撤销电话号段接入限制](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Telegram 传闻称黎曼猜想已通过 Lean 验证](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 10.0/10

一则 Telegram 帖子声称，Levent Alpöge 于 2026 年 11 月 20 日发布了黎曼猜想的 Lean 形式化证明，代码库约 1700 万行；次日 Lean FRO 与 Mathlib Initiative 联合声明认证该命题与证明均正确，称社区确认其命题与 Mathlib 的 RiemannHypothesis 一致、代码库可无错编译，且多个独立证明检查器验证证明有效。上述说法目前仅见于该 Telegram 帖子及其引述的 Lean community blog，尚无独立来源核实，应视为未经证实的声明。

telegram · zaihuapd · 11月21日 16:48

**「背景」** 据外部报道，Anthropic 研究者 Levent Alpöge 于 2026 年 11 月 20 日在其个人网站发布了一份 Lean 归档，声称与 Claude 共同发现了黎曼猜想的证明，并给出了将其推广到 Dirichlet L 函数的方法；该归档包含约 17.5 万个文件，并称经过 MIT 内核检查。这些外部报道本身仍将该声明描述为未经核实的个人主张，与本次 Telegram 消息所称 Lean FRO 和 Mathlib 已联合认证的说法并不等同。

**「影响与待核实点」** 若该认证属实，数学界与形式化验证社区将获得一个可直接在 Lean 中复用的黎曼猜想证明，相关研究者需要以 Mathlib 的 RiemannHypothesis 定义为基准复核命题一致性。在独立核实之前，开发者与研究者不宜将该代码库当作已验证结果引用或依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unite.ai/levent-alpoges-unverified-riemann-claim-puts-claudes-lean-code-in-focus/">Levent Alpöge’s Unverified Riemann Claim Puts Claude’s Lean ...</a></li>
<li><a href="https://casrai.org/news/anthropic-levent-alpoge-claude-lean-riemann-hypothesis-claim-2026">175,000-File Lean Riemann Hypothesis Proof Claim — CASRAI</a></li>
<li><a href="https://lean4.dev/proofs/riemann-hypothesis-claim">The Riemann Hypothesis: a claimed proof, delivered in Lean</a></li>

</ul>
</details>

**标签**: `#formal-verification`, `#lean`, `#mathematics`, `#riemann-hypothesis`, `#mathlib`

---

<a id="item-tech-news-2"></a>
### [OpenRouter 披露推理供应商数据处理事件](https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/) ⭐️ 7.0/10

OpenRouter 发布公告，披露其推理供应商之间存在数据处理事件。公告未在现有材料中给出具体供应商名单、受影响请求数量或时间范围，因此事件规模尚不明确。社区讨论集中在供应商审核、零数据保留（ZDR）协议，以及部分供应商将提示词转发给上游服务（如 MiniMax）而非自行提供推理。

hackernews · sdko · 11月22日 02:14 · [社区讨论](https://news.ycombinator.com/item?id=50595554)

**「背景」** OpenRouter 是一个统一 API 平台，开发者通过单一接口调用多家推理提供商的模型。据其公告，OpenRouter 在调查后已将三家提供商从平台下架，并取消了 125 个端点的零数据保留（ZDR）资格。

**「对用户的影响」** 有评论者称自己仅有一条提示词受此次事件影响，并表示已将 OpenRouter 设置改为只允许自己信任的供应商，而不再让平台自动路由。对于依赖 OpenRouter 处理敏感数据的用户，这意味着需要主动检查路由配置和供应商的 ZDR 条款，而不能仅依赖平台默认设置。

**「社区讨论」** 有评论者认为此次事件暴露了 OpenRouter 对供应商缺乏尽职调查和约束，并因此放弃迁移计划；也有人肯定 OpenRouter 的应对是积极的第一步，但指出最可靠的 ZDR 仍是企业直接与推理供应商签订协议，且即便如此仍需信任对方。另有评论者提醒，部分供应商会把提示词转发给上游服务，这本身就是需要关注的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/">Data Processing Incidents on Inference Providers</a></li>
<li><a href="https://downdetector.com/status/openrouter/">OpenRouter down? Current problems and outages | US</a></li>

</ul>
</details>

**标签**: `#AI privacy`, `#inference providers`, `#OpenRouter`, `#data processing`, `#LLM infrastructure`

---

<a id="item-tech-news-3"></a>
### [博客称 Anthropic 2028 年电力 87%来自天然气、11%来自煤炭](https://betterdatacenterproject.com/2026/11/16/how-ai-is-powered-a-breakdown-of-byop-and-grid-power/) ⭐️ 7.0/10

一篇博客文章对 AI 数据中心的电力来源做了拆解，并声称 Anthropic 在 2028 年的能源结构将是 87%天然气、11%煤炭。该数字来自单一博客的预测，而非 Anthropic 公布的数据或独立测量结果，原始报道也未提供可核验的测算方法。Hacker News 上的讨论主要围绕外部性成本与 AI 能耗规模展开。

hackernews · happosai · 11月22日 08:57 · [社区讨论](https://news.ycombinator.com/item?id=50597612)

**「背景」** AI 数据中心需要 24 小时不间断供电，这使电力来源成为衡量其环境成本的关键指标。据《金融时报》报道，Anthropic 已达成一项 34 亿美元的协议，为其数据中心提供天然气发电。

**「影响」** 若该预测接近实际，Anthropic 的算力扩张将高度依赖化石燃料，其对外宣称的清洁能源目标与实际采购结构之间会出现明显落差；关注 AI 供应链碳排放的企业客户和投资者需要向厂商索取实际电力采购数据，而不能依赖第三方博客的推算。

**「社区讨论」** 有评论者认为，纯财务核算忽略了环境与社会成本，因此需要监管来约束外部性；也有人指出 AI 数据中心的能耗规模远超公众直觉，并以某在建数据中心的技术评估为例。另有评论认为，电力成本直接体现在模型厂商的资产负债表上，降低推理成本的经济激励本身会推动效率提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.technologyreview.com/2025/05/20/1116327/ai-energy-usage-climate-footprint-big-tech/">We did the math on AI’s energy footprint. | MIT Technology Review</a></li>
<li><a href="https://www.ft.com/content/a6c43402-719e-4295-ae5f-541edb0aeb29?syn-25a6b1a6=1">‘Bold but sane’: what we learnt from Anthropic ’s 240,000-word IPO filing</a></li>

</ul>
</details>

**标签**: `#ai-infrastructure`, `#data-centers`, `#energy`, `#climate`, `#industry-analysis`

---

<a id="item-tech-news-4"></a>
### [FBI 与 USDA 据报遭黑客入侵，FBI 目标为 NCIC 数据库](https://www.theverge.com/tech/1039543/fbi-usda-hacked) ⭐️ 7.0/10

据 11 月 21 日（周五）的报道，美国农业部（USDA）和联邦调查局（FBI）均遭黑客入侵。CNN 报道称，这是 FBI 近几个月内第二次遭此类攻击，此次目标是全国犯罪信息中心（NCIC）——联邦、州和地方执法机构用来共享通缉令、失踪人员等信息的系统。特朗普总统随后在接受 Fox News 采访时证实了 FBI 遭入侵一事。NBC 最先报道了 USDA 被入侵，路透社援引报道称，目前已知的入侵范围是支付数据库，但前官员警告情况可能不止于此。上述信息均来自媒体转述，报道未披露攻击手法、影响规模或数据是否外泄等技术细节。

rss · The Verge · 11月21日 17:42

**「背景」** 据 The Verge 援引 CNN 报道，这是近几个月内 FBI 第二次遭到此类攻击，本次目标为联邦、州和地方执法机构共享逮捕令、失踪人员等信息的全国犯罪信息中心（NCIC）。NBC 于周五率先报道了农业部遭入侵一事，路透社随后跟进，称目前已知的入侵范围是支付数据库。

**「直接影响」** 据《卫报》和路透社报道，此次入侵涉及美国农业部用于向农民发放款项的系统，以及联邦、州和地方执法机构共享逮捕令和失踪人员信息的 NCIC。这意味着依赖 NCIC 的执法机构可能面临数据完整性核查需求，而农业部的农民付款流程可能受到干扰；不过目前公开信息仅确认付款数据库是已知的入侵范围，前官员警告影响可能更广。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/us-news/2026/nov/21/usda-fbi-outages-cyber-attack">USDA, FBI breached by hackers amid spate of tech... | The Guardian</a></li>
<li><a href="https://nypost.com/2026/11/20/us-news/hackers-reportedly-breach-fbi-crime-database-the-2nd-time-the-bureau-was-targeted-in-months/">Hackers reportedly breach FBI crime database — the 2nd time the...</a></li>
<li><a href="https://www.theguardian.com/us-news/2026/nov/21/usda-fbi-outages-cyber-attack">USDA, FBI breached by hackers amid spate of tech outages ...</a></li>
<li><a href="https://www.reuters.com/legal/litigation/us-department-agriculture-breached-by-hackers-this-week-nbc-news-reports-2026-11-20/">Hackers breached US Department of Agriculture, NBC News ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#government`, `#data breach`, `#law enforcement`

---

<a id="item-tech-news-5"></a>
### [Rackspace Spot 遭入侵，客户 Kubernetes 密钥被访问](https://www.bleepingcomputer.com/news/security/rackspace-spot-breach-let-hackers-access-customer-kubernetes-secrets/) ⭐️ 7.0/10

Rackspace 警告客户，攻击者利用泄露的凭据入侵了其 Rackspace Spot 云平台，部署了未经授权的工作负载，并访问了客户集群中的 Kubernetes 密钥。Rackspace 将此次事件定性为凭据泄露导致的入侵，但披露内容未说明受影响客户数量、入侵时间窗口或密钥的具体类型。目前尚不清楚 Rackspace 是否已强制轮换相关凭据或提供补救措施。

rss · BleepingComputer · 11月21日 22:59

**「背景」** Rackspace Spot 是 Rackspace 提供的云平台，客户在其上运行 Kubernetes 集群。Kubernetes 集群中的 Secret 对象通常用于存放凭据、令牌和证书等敏感配置，一旦被读取，攻击者可能借此进一步访问客户的工作负载或关联服务。此次事件中，攻击者据称通过泄露的凭据进入平台，并部署了未经授权的工作负载。

**「对客户的影响」** 受影响客户应假定其集群中的 Kubernetes Secrets 可能已被读取，并尽快轮换相关凭据；但 Rackspace Spot 管理控制台曾长时间中断，一度妨碍客户管理集群和轮换可能已泄露的凭据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/rackspace-spot-breach-let-hackers-access-customer-kubernetes-secrets/">Rackspace Spot breach let hackers access customer Kubernetes ...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/rackspace-spot-breach-let-hackers-access-customer-kubernetes-secrets/">Rackspace Spot breach let hackers access customer Kubernetes ...</a></li>
<li><a href="https://securityelites.com/news/rackspace-spot-breach-kubernetes-secrets-exposed/">Rackspace Spot Breach Exposed Kubernetes Secrets</a></li>

</ul>
</details>

**标签**: `#cloud security`, `#kubernetes`, `#security breach`, `#rackspace`, `#infrastructure`

---

<a id="item-tech-news-6"></a>
### [微软 Entra Connect Health 漏洞遭利用，租户数据被窃](https://www.bleepingcomputer.com/news/security/microsoft-entra-connect-health-flaw-exploited-to-steal-tenant-data/) ⭐️ 7.0/10

微软警告称，攻击者利用 Entra Connect Health 服务中的一个漏洞，未经授权获取了管理员电子邮件地址和租户配置信息，构成一起数据泄露事件。微软已就此向组织发出通知。现有报道未披露漏洞的技术细节、受影响的租户数量或修复与缓解措施的具体状态。

rss · BleepingComputer · 11月21日 18:01

**「背景」** Entra Connect Health 是微软用于监控本地 Active Directory 与 Entra ID 同步健康状况的组件，其租户级元数据由微软托管。据半岛电视台援引的报道，微软表示已修复该漏洞，事件造成的是对部分租户联系人与配置元数据的未授权只读访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thepeninsulaqatar.com/article/22/11/2026/microsoft-addresses-security-vulnerability-in-entra-connect-health">Microsoft addresses security vulnerability in Entra Connect Health</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#microsoft`, `#identity`, `#data-breach`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美股科技股大跌，亚洲多地出台稳市措施](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 9.0/10

美国 AI 科技股周五遭遇大规模抛售，纳斯达克指数单日下跌 5.28%，费城半导体指数下跌近 11%。随后，中国内地、韩国和中国台湾地区相继推出稳市措施，包括下调融资保证金比例、放宽回购限制和禁止平盘以下卖空。

telegram · zaihuapd · 11月22日 13:24

**「背景」** 此前一天（11 月 20 日），费城半导体指数已下跌 10.7%，自 6 月高点累计下跌 43%，显示这轮抛售并非单日事件。

**「影响」** 这些措施直接作用于中国内地、韩国和中国台湾地区的股市交易者：融资买入的最低保证金比例下调、卖空受限或禁止、回购与借券规则调整，都会改变投资者加杠杆和做空的成本与可行性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.guancha.cn/GuoJi%C2%B7ZhanLue/2026_11_21_909399.shtml">AI恐慌爆发，华尔街震荡，美国科技股 跌 入熊市</a></li>

</ul>
</details>

**标签**: `#US tech selloff`, `#market volatility`, `#market stabilization policy`, `#short-selling rules`, `#Asian equities`

---

<a id="item-finance-news-2"></a>
### [英媒指太子集团相关人员涉英伟达芯片对华走私](https://www.ft.com/content/f3ad8a81-3890-4a8a-8853-ff0a94b08ba9?syn-25a6b1a6=1) ⭐️ 7.0/10

英国《金融时报》援引知情人士称，被美国财政部指为柬埔寨太子集团“二号人物”的胡小伟涉嫌参与将英伟达芯片运入中国；该报援引的贸易数据显示，2024 年 12 月至 2025 年 12 月，Megaspeed 马来西亚子公司申报进口货值约 46 亿美元，部分芯片据称流入中国黑市。太子集团否认胡小伟曾为其工作，并称有关非法网络和私人飞机走私的指控缺乏事实依据。

telegram · zaihuapd · 11月22日 04:34

**「背景」** 美国财政部此前已将胡小伟列为柬埔寨太子集团跨国犯罪组织的“二号人物”并实施制裁，指其在柬埔寨境外设立并管理多家涉及航空、房地产和香港金融业务的相关实体（tool-1-2、tool-1-1）。美国对华先进芯片出口管制催生了由复杂交易、空壳公司和芯片走私构成的灰色产业，而此次报道涉及的 Megaspeed 是一家总部位于新加坡的云计算服务商，其在新加坡和马来西亚建有业务网络（tool-2-2、tool-2-1）。

**「影响」** 若相关指控成立，这一路径可能成为美国对华芯片出口管制的规避渠道，涉及向中国转售芯片的贸易商和中间商将面临更严格的审查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hu_Xiaowei">Hu Xiaowei - Wikipedia</a></li>
<li><a href="https://home.treasury.gov/news/press-releases/sb0538">Treasury Further Dismantles Overseas Scam Operations ...</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/megaspeed-built-network-singapore-malaysia-024836098.html?fr=sycsrp_catchall">How Megaspeed built a network in Singapore and Malaysia to ...</a></li>
<li><a href="https://www.cnn.com/2026/11/14/tech/china-megaspeed-nvidia-scandal-hnk-intl">How the Nvidia scandal lifted the curtain on a loophole that ...</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#export controls`, `#Nvidia`, `#smuggling`, `#China`

---

<a id="item-finance-news-3"></a>
### [中国要求美国撤销电话号段接入限制](https://www.bloomberg.com/news/articles/2026-11-22/china-objects-to-us-curbs-on-telecoms-access-to-phone-numbers) ⭐️ 7.0/10

中国商务部 11 月 22 日敦促美国撤销一项限制中国移动、中国电信、中国联通直接接入美国电话号码的措施，称其违反非歧视与公平竞争原则。美国联邦通信委员会（FCC）于 11 月 19 日投票收紧对申请直接接入美国号码的互联网语音服务商的安全要求，新增国家安全认证，以阻止其“涵盖清单”上的实体、设备和服务接入美国网络。

telegram · zaihuapd · 11月22日 06:44

**「背景」** 美国联邦通信委员会（FCC）于 11 月 19 日投票通过新规，要求申请直接接入美国电话号码的互联网语音服务商接受新的国家安全认证，以阻止其“涵盖清单”上的实体、设备和服务接入美国网络。此前，FCC 已分别于 2021 年和 2022 年撤销中国电信（美洲）和中国联通（美洲）在美国的国内及国际运营授权。

**「影响」** 若该措施维持，中国移动、中国电信、中国联通将无法直接接入美国电话号码，依赖其线路提供跨境语音服务的相关企业需另寻接入渠道。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fcc.gov/document/fcc-cracks-down-bad-actors-access-us-phone-numbers-0">FCC Cracks Down on Bad Actors&#x27; Access to U.S. Phone Numbers</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/DOC-427320A1.pdf">FCC Cracks Down on Bad Actors’ Access to U.S. Phone Numbers</a></li>
<li><a href="https://www.fcc.gov/document/china-telecom-americas-order-revocation-and-termination">China Telecom Americas Order on Revocation and Termination</a></li>
<li><a href="https://docs.fcc.gov/public/attachments/FCC-22-9A1.pdf">Federal Communications Commission FCC 22-9 Before the Federal ...</a></li>
<li><a href="https://www.nst.com.my/business/economy/2026/11/1583171/china-slams-malicious-us-ban-telecom-firms-phone-number-access">China slams &#x27;malicious&#x27; US ban on telecom firms&#x27; phone number ...</a></li>

</ul>
</details>

**标签**: `#telecom regulation`, `#US-China relations`, `#FCC`, `#national security`, `#telecommunications`

---