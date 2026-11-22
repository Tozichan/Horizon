---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 52 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [Telegram 帖称黎曼猜想已通过 Lean 验证](#item-tech-news-1) ⭐️ 10.0/10
2. [OpenRouter 披露推理供应商数据处理事件](#item-tech-news-2) ⭐️ 7.0/10
3. [FBI 与 USDA 据报遭黑客入侵，FBI 攻击目标为 NCIC 数据库](#item-tech-news-3) ⭐️ 7.0/10
4. [微软 Entra Connect Health 漏洞遭利用，租户数据被窃](#item-tech-news-4) ⭐️ 7.0/10
5. [特斯拉海外推送 FSD v15，宣称安全关键场景处理提升 25 倍](#item-tech-news-5) ⭐️ 7.0/10

**财经新闻**
1. [美股科技股大跌，亚洲多地出台稳市措施](#item-finance-news-1) ⭐️ 8.0/10
2. [英媒：柬埔寨太子集团相关人员被指参与英伟达芯片对华走私](#item-finance-news-2) ⭐️ 7.0/10
3. [中国商务部要求美国撤销电话号段接入限制](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Telegram 帖称黎曼猜想已通过 Lean 验证](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 10.0/10

一则 Telegram 帖子声称，Levent Alpöge 于 2026 年 11 月 20 日发布了黎曼猜想的 Lean 形式化证明，代码库约 1700 万行；次日 Lean FRO 与 Mathlib Initiative 联合声明认证该命题与证明均正确，社区确认命题与 Mathlib 的 RiemannHypothesis 一致、代码库可无错编译，且多个独立证明检查器验证有效。上述内容目前仅来自单一 Telegram 来源，尚未经独立核实，应视为未经证实的说法。

telegram · zaihuapd · 11月21日 16:48

**「背景」** 据 Unite.AI 报道，Levent Alpöge 于 2026 年 11 月 20 日表示，他相信自己与 Claude 发现了黎曼猜想的证明，以及一种可解决广义黎曼猜想的方法，但当时发布的 Lean 代码尚未经过对完整论证的独立验证。另一篇 dev.to 文章则把这一事件概括为“1700 万行 Lean 代码与 8 小时反转”，暗示相关说法在发布后短时间内出现了转折。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.unite.ai/levent-alpoges-unverified-riemann-claim-puts-claudes-lean-code-in-focus/">Levent Alpöge’s Unverified Riemann Claim Puts Claude’s Lean ...</a></li>
<li><a href="https://dev.to/kursatyz/17-million-lines-of-lean-code-and-an-8-hour-reversal-levent-alpoge-claude-and-the-riemann-42e7">17 Million Lines of Lean Code and an 8-Hour Reversal: Levent ...</a></li>

</ul>
</details>

**标签**: `#formal-verification`, `#lean`, `#mathematics`, `#riemann-hypothesis`, `#unverified-claim`

---

<a id="item-tech-news-2"></a>
### [OpenRouter 披露推理供应商数据处理事件](https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/) ⭐️ 7.0/10

OpenRouter 发布公告，披露了涉及多家推理供应商的数据处理事件。公告未在现有材料中给出具体供应商名单、受影响范围或时间线，因此事件规模尚不明确。社区讨论集中在供应商审核、零数据保留（ZDR）承诺的可信度，以及提示词被转发给上游厂商等问题上。

hackernews · sdko · 11月22日 02:14 · [社区讨论](https://news.ycombinator.com/item?id=50595554)

**「背景」** OpenRouter 是一个在多个推理提供商之间路由请求的 AI 推理 API 服务。据其公告及外部报道，安全研究人员通过 canary token 测试发现部分推理提供商未遵守其数据政策，OpenRouter 随后下架了三家提供商，并将 125 个端点移出零数据保留（ZDR）资格名单。公告强调这些发现并未显示 OpenRouter 自身遭到入侵。

**「对用户的影响」** 一位评论者称自己仅有一条提示词受此次事件影响，并表示此后已将 OpenRouter 设置改为只允许使用自己信任的供应商，而不再任由平台自动路由。对于依赖零数据保留承诺的用户，这意味着需要自行核查各供应商的实际处理方式，而不能仅依赖平台层面的保证。

**「社区讨论」** 有评论者认为，此次暴露的多种问题说明 OpenRouter 对合作供应商缺乏尽职调查和约束，并称这已使其放弃迁移计划；也有人肯定 OpenRouter 的应对是积极一步，但指出最可靠的 ZDR 仍是企业直接与推理供应商签订协议，且即便如此也只能选择信任对方。另有评论者指出，部分“供应商”实际上只是把提示词转发给上游厂商（如 MiniMax），而非自行提供推理服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/blog/announcements/data-processing-incidents-on-inference-providers/">Data Processing Incidents on Inference Providers - openrouter.ai</a></li>
<li><a href="https://openrouter.ai/blog/">Blog — OpenRouter Blog</a></li>
<li><a href="https://www.unite.ai/openrouter-cuts-three-providers-after-ai-prompt-exposure-findings/">OpenRouter Cuts Three Providers After AI Prompt Exposure ...</a></li>

</ul>
</details>

**标签**: `#ai-inference`, `#privacy`, `#openrouter`, `#llm-infrastructure`, `#data-processing`

---

<a id="item-tech-news-3"></a>
### [FBI 与 USDA 据报遭黑客入侵，FBI 攻击目标为 NCIC 数据库](https://www.theverge.com/tech/1039543/fbi-usda-hacked) ⭐️ 7.0/10

据 11 月 21 日的报道，美国农业部（USDA）和联邦调查局（FBI）均遭黑客入侵。CNN 报道称，FBI 此次攻击针对全国犯罪信息中心（NCIC），这是该机构近几个月内第二次遭遇此类攻击；NCIC 供联邦、州和地方执法机构共享通缉令、失踪人员等信息。特朗普总统随后在接受 Fox News 采访时证实了 FBI 遭入侵一事。NBC 最先报道了 USDA 被入侵，路透社援引报道称，目前已知的入侵范围是支付数据库，但前官员警告情况可能不止于此。

rss · The Verge · 11月21日 17:42

**「背景」** 美国国家犯罪信息中心（NCIC）是 FBI 最早建立的信息共享系统，用于在地方与全国执法机构之间交换犯罪嫌疑人、恐怖嫌疑人、失踪人员（包括儿童）等数据。据半岛电视台报道，FBI 曾在 9 月表示正在调查一起疑似网络攻击，一个网络组织声称窃取了该局约 3.8 万名员工的敏感信息；本次报道所述攻击是近几个月内针对 FBI 的第二次此类事件。

**「影响」** 若 NCIC 遭入侵的情况属实，依赖该数据库共享逮捕令、失踪人口等信息的联邦、州和地方执法机构将面临数据完整性与访问安全风险；USDA 方面目前已知的受影响范围是支付数据库，但前官员警告实际范围可能更大。报道未披露攻击手法或已确认的泄露数据，相关影响仍待官方调查确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.axios.com/2026/11/21/fbi-hack-personal-records-ncic">Latest hack of FBI puts personal records at risk</a></li>
<li><a href="https://www.aljazeera.com/news/2026/11/21/fbi-national-crime-database-suffers-suspected-breach-reports">FBI national crime database suffers suspected breach ... | Al Jazeera</a></li>
<li><a href="https://www.theguardian.com/us-news/2026/nov/21/usda-fbi-outages-cyber-attack">USDA , FBI breached by hackers amid spate of tech... | The Guardian</a></li>
<li><a href="https://www.zerohedge.com/technology/fbi-probes-suspected-hack-critical-nationwide-crime-database-cyber-pandemic-fears-mount">FBI Probes Suspected Hack Of Critical Nationwide Crime Database As...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#government`, `#data breach`, `#law enforcement`

---

<a id="item-tech-news-4"></a>
### [微软 Entra Connect Health 漏洞遭利用，租户数据被窃](https://www.bleepingcomputer.com/news/security/microsoft-entra-connect-health-flaw-exploited-to-steal-tenant-data/) ⭐️ 7.0/10

微软警告称，攻击者利用 Entra Connect Health 服务中的一个漏洞获得了未授权访问，导致管理员电子邮件地址和租户配置信息泄露。微软将此事定性为数据泄露事件，并已向相关组织发出通知。目前公开信息未披露漏洞的技术细节、受影响的租户数量或攻击者身份。

rss · BleepingComputer · 11月21日 18:01

**「背景」** Entra Connect Health 是微软 Entra 身份体系中的混合身份监控服务，用于监测本地 Active Directory 与 Entra ID 之间的同步和连接状态。此次事件中，微软表示已修复该漏洞，攻击者获得的是对部分租户级联系人与配置元数据的只读访问权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thepeninsulaqatar.com/article/22/11/2026/microsoft-addresses-security-vulnerability-in-entra-connect-health">Microsoft addresses security vulnerability in Entra Connect Health</a></li>
<li><a href="https://learn.microsoft.com/en-us/entra/identity/hybrid/connect/reference-connect-health-faq">Microsoft Entra Connect Health FAQ - Azure... | Microsoft Learn</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#microsoft`, `#cloud`, `#identity`

---

<a id="item-tech-news-5"></a>
### [特斯拉海外推送 FSD v15，宣称安全关键场景处理提升 25 倍](https://x.com/Tesla/status/2124222447855743019) ⭐️ 7.0/10

特斯拉在海外开始推送 FSD v15。官方宣称该版本对安全关键场景的处理能力提升至 25 倍，但这是厂商说法，尚无独立验证。更新新增“Tesla Reality View”可视化界面，可在车机屏幕叠加摄像头画面与 FSD 行驶规划，支持全屏、地图或分屏视图及安静模式。导航可将转弯等信息叠加显示，转向灯提示音更轻柔并逐渐减弱，同时优化了坑洼、碎片等路况的行驶体验以及学校和恶劣天气下的速度控制。

telegram · zaihuapd · 11月22日 00:03

**「背景」** FSD 是特斯拉面向其车辆提供的高级辅助驾驶软件套件，此前版本已采用端到端驾驶网络。据科技媒体报道，v15 称对端到端驾驶网络的“每一部分”都进行了升级，并新增可实时查看和干预 FSD 行驶规划的 Tesla Reality View 可视化功能。这些性能与功能描述目前均来自特斯拉及转述其发布内容的报道，尚无独立验证。

**「对用户的影响」** 已获推送的海外 FSD 用户会看到新的可视化界面和导航叠加显示，转向提示音与部分路况、限速场景的驾驶行为也随之调整；25 倍提升目前仅为特斯拉的宣称，实际效果需等待独立测试或用户实测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techau.com.au/tesla-fsd-v15-is-rolling-out-with-new-reality-view-dramatic-capability-improvements/">Tesla FSD V 15 is rolling out with new Reality View ... | techAU</a></li>
<li><a href="https://www.youtube.com/watch?v=eNBqkc7V1nU">Introducing Tesla Self-Driving V 15 - YouTube</a></li>
<li><a href="https://gizmodo.com/its-like-gta-musk-touts-video-game-like-update-to-tesla-fsd-2000843584">Tesla Adds GTA-Like Update to FSD</a></li>

</ul>
</details>

**标签**: `#autonomous driving`, `#Tesla FSD`, `#AI systems`, `#software release`, `#computer vision`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美股科技股大跌，亚洲多地出台稳市措施](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

美国 AI 科技股周五遭大规模抛售，纳斯达克单日暴跌 5.28%，费城半导体指数重挫近 11%。随后中国内地下调融资保证金最低比例至 80%，韩国自 11 月 24 日起放宽上市公司每日回购订单数量限制、为期 3 个月，中国台湾地区自 11 月 23 日起全面禁止平盘以下卖空，并将融券保证金比例由 130%提高至 150%。

telegram · zaihuapd · 11月22日 13:24

**「背景」** 此前，美国 AI 与半导体板块已出现一轮抛售：据福克斯商业频道报道，11 月 5 日纳斯达克进入回调区间，费城半导体指数当日一度下跌 11.9%。据路透社报道，中国三大证券交易所此次将融资买入股票的最低保证金比例由 100%下调至 80%，措施自 11 月 30 日起生效。

**「影响」** 这些措施直接改变了两融投资者、卖空交易者和上市公司回购的操作条件，涉及中国内地、韩国和中国台湾三个市场。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.foxbusiness.com/markets/stocks-nov-5-2026">Nasdaq tumbles 5%, Dow plunges more than 1,800... | Fox Business</a></li>
<li><a href="https://www.ft.com/content/7c6ceb4f-d7b1-49ec-9047-0e2e4cd2615c?syn-25a6b1a6=1">US midterms 2026 reaction as it happened: Global stocks tumble as...</a></li>
<li><a href="https://www.reuters.com/world/chinese-exchanges-ease-margin-trading-requirements-aid-stock-markets-2026-11-22/">Chinese exchanges ease margin trading requirements to aid ...</a></li>
<li><a href="https://en.sedaily.com/world/2026/11/22/china-eases-margin-rules-after-tech-selloff-wipes-out-17">China Eases Margin Rules After Tech Selloff Wipes Out $1.7 ...</a></li>

</ul>
</details>

**标签**: `#US tech selloff`, `#market stabilization policy`, `#short-selling rules`, `#Asian equities`, `#margin requirements`

---

<a id="item-finance-news-2"></a>
### [英媒：柬埔寨太子集团相关人员被指参与英伟达芯片对华走私](https://www.ft.com/content/f3ad8a81-3890-4a8a-8853-ff0a94b08ba9?syn-25a6b1a6=1) ⭐️ 7.0/10

英国《金融时报》援引知情人士称，被美国财政部指为柬埔寨太子集团“二号人物”的胡小伟涉嫌参与将英伟达芯片运入中国；该报援引的贸易数据显示，2024 年 12 月至 2025 年 12 月，Megaspeed 马来西亚子公司进口货物申报价值约 46 亿美元，部分芯片据称流入中国黑市。太子集团否认胡小伟曾为其工作，并称有关非法网络和私人飞机走私的指控缺乏事实依据。

telegram · zaihuapd · 11月22日 04:34

**「背景」** 美国财政部此前已将柬埔寨太子集团列为跨国犯罪组织，并于 2026 年 6 月对与该集团相关的 9 名个人和 26 家实体实施制裁。Megaspeed 此前已因涉嫌违反美国出口管制、将英伟达芯片转运至中国而受到审视。

**「影响」** 若相关指控成立，受出口管制的英伟达芯片可能经马来西亚转运流入中国，削弱美国对华半导体出口限制的效果；但上述说法目前仅为《金融时报》援引知情人士的指控，太子集团已否认，实际规模尚不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.state.gov/releases/office-of-the-spokesman/2026/06/dismantling-prince-group-transnational-criminal-organization-and-huione-group/">Dismantling Prince Group Transnational Criminal Organization ...</a></li>
<li><a href="https://home.treasury.gov/news/press-releases/sb0538">Treasury Further Dismantles Overseas Scam Operations ...</a></li>
<li><a href="https://www.dw.com/en/megaspeed-and-the-battle-to-go-high-end-nvidia-chips-into-china/a-79909129">Megaspeed : Nvidia partner at the center of the spy affair</a></li>
<li><a href="https://epoch.ai/publications/chip-smuggling">Diversion and resale: estimating compute smuggling to China</a></li>
<li><a href="https://www.cnbc.com/2025/12/31/160-million-export-controlled-nvidia-gpus-allegedly-smuggled-to-china.html">$160 million export-controlled Nvidia GPUs allegedly ... - CNBC</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#export controls`, `#Nvidia`, `#smuggling`, `#China trade`

---

<a id="item-finance-news-3"></a>
### [中国商务部要求美国撤销电话号段接入限制](https://www.bloomberg.com/news/articles/2026-11-22/china-objects-to-us-curbs-on-telecoms-access-to-phone-numbers) ⭐️ 7.0/10

中国商务部 11 月 22 日敦促美国撤销一项限制中国移动、中国电信、中国联通直接接入美国电话号码的措施，称其违反非歧视与公平竞争原则；美国联邦通信委员会（FCC）则于 11 月 19 日投票收紧对申请直接接入美国号码的互联网语音服务商的安全要求，新增国家安全认证。

telegram · zaihuapd · 11月22日 06:44

**「背景」** 美国联邦通信委员会（FCC）于 11 月 19 日投票收紧对申请直接接入美国电话号码的互联网语音服务商的安全要求，新增国家安全认证，以阻止其“涵盖清单”上的实体、设备和服务接入美国网络。此前，FCC 已以国家安全为由，自 2019 年起陆续对多家中国电信企业采取限制措施。

**「影响」** 若该措施维持，三家中国运营商将更难直接接入美国电话网络，依赖其线路拨打美国号码的用户和企业可能面临通话路径调整。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sg.news.yahoo.com/fcc-seeks-bar-hong-kong-093000777.html">FCC seeks to bar Hong Kong Telecom carrier from operating in US</a></li>

</ul>
</details>

**标签**: `#telecom regulation`, `#US-China relations`, `#FCC`, `#state-owned carriers`, `#trade policy`

---