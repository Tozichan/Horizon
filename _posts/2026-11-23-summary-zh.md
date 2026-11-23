---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 51 条内容中筛选出 6 条重要资讯。

---

**科技新闻**
1. [OpenAI 探讨困惑度与模型智能的关系](#item-tech-news-1) ⭐️ 7.0/10
2. [GL.iNet 云管理漏洞遭利用，路由器与 KVM 设备被植入后门](#item-tech-news-2) ⭐️ 7.0/10
3. [谷歌为 Chrome AI 代理搭建模拟互联网测试环境](#item-tech-news-3) ⭐️ 7.0/10

**财经新闻**
1. [美股科技股单日重挫，亚洲多地推出应急稳市措施](#item-finance-news-1) ⭐️ 8.0/10
2. [中国商务部要求美国撤销电话号段接入限制](#item-finance-news-2) ⭐️ 7.0/10
3. [蚂蚁集团领投 Simplexity Robotics 1 亿美元融资，投后估值 16 亿美元](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenAI 探讨困惑度与模型智能的关系](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI 发布文章《Perplexity and Intelligence》，讨论困惑度（perplexity）与模型智能之间的关系。由于没有提供文章正文，无法核实其具体技术结论或实验数据。社区讨论中，有评论者指出文章未定义困惑度，并补充说明：困惑度衡量模型预测下一个 token 时的“惊讶程度”，最差情况等于词表大小，最好情况为 1。另有评论者称，交叉熵损失与模型能力的相关性趋势“非常明显”，并认为这提供了一种比日益复杂的评测更简单的基准。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**「背景」** OpenAI 首席科学家 Jakub Pachocki 在该文中主张，将困惑度（perplexity，等价于交叉熵损失）确立为跨模型开发者比较的指标，并用于支撑共享的安全标准。困惑度衡量模型预测下一 token 时的“意外程度”：最差情形等于词表大小，最佳情形为 1。

**「社区讨论」** 有评论者表示，在强化学习使用日益增多的背景下，交叉熵损失仍然重要，这令其感到意外，并称这种趋势“非常明显”。另一位评论者认为，困惑度与智能的对应关系初看令人惊讶，但事后看别无他法，因为从原始数据流中提取世界模型的能力，正好可以用预测（即压缩）率来衡量。还有评论者引用一条推文称，微软的 Mustafa Suleyman 表示 MAI 模型已加入同一评测图表，并报告 MAI-2 Base 的 log-perplexity 为 0.819；该说法来自社区转述，未经独立核实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#language-models`, `#perplexity`, `#model-evaluation`, `#openai`

---

<a id="item-tech-news-2"></a>
### [GL.iNet 云管理漏洞遭利用，路由器与 KVM 设备被植入后门](https://www.bleepingcomputer.com/news/security/hackers-exploit-glinet-cloud-flaw-to-infect-routers-kvm-devices/) ⭐️ 7.0/10

GL.iNet 确认，攻击者利用其云远程管理服务中的一处漏洞，在客户的路由器和 KVM 设备上安装了定制恶意软件。部分受影响用户报告称，设备上出现了后门和反向 shell，使攻击者能够远程访问被感染的设备。报道未披露漏洞的具体技术细节、受影响的固件或云服务版本、修复状态以及受影响设备数量。

rss · BleepingComputer · 11月22日 18:45

**「事件背景」** GL.iNet 于 2026 年 11 月 20 日发布安全公告，称当天在其云远程管理服务中发现一处漏洞，未经授权的第三方利用该漏洞访问并在一部分 GL.iNet 路由器和 KVM 设备上安装了恶意软件。此次事件涉及的正是这项云远程管理服务，攻击者借助它向设备植入恶意程序。

**「影响与应对」** 使用 GL.iNet 云远程管理功能的用户应假定其路由器或 KVM 设备可能已被入侵，并检查是否存在异常连接、未知账户或非预期固件改动。在厂商公布修复信息前，可考虑停用云远程管理并限制设备的管理接口暴露在公网。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20">GL.iNet Security Notice 2026-11-20</a></li>
<li><a href="https://forum.gl-inet.com/t/2026-11-20-gl-inet-security-notice-goodcloud-kvm-routers/73056">2026-11-20: GL.iNet Security Notice - GoodCloud / KVM / Routers</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#routers`, `#embedded-systems`, `#cloud`

---

<a id="item-tech-news-3"></a>
### [谷歌为 Chrome AI 代理搭建模拟互联网测试环境](https://www.landian.news/archives/128701.html) ⭐️ 7.0/10

据蓝点网报道，谷歌为 Chrome 的 AI 代理搭建了一个名为 Mirror Dimension 的模拟互联网，在隔离环境中测试其打开网站、搜索浏览、登录、加购和完成任务等操作。报道称该环境包含数千个模拟网站，每名工程师单独隔离测试，每天运行超过 1000 个测试案例，重点防御恶意网页的提示词注入等攻击。上述细节来自二手转述，尚无谷歌官方说明或独立验证。

telegram · zaihuapd · 11月23日 01:30

**「背景」** 谷歌在 2026 年 11 月 19 日的安全博客中介绍了 Mirror Dimension，Wired 同日也作了报道。它是 Chrome 团队为测试浏览器 AI 代理（auto browse）而搭建的合成网络环境，包含数千个模拟网站，让工程师在接近真实的上网场景中评估代理行为，而不必承担真实世界中的安全风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/security/mirror-dimension-for-agents/">Mirror Dimension for Agents: Evaluating Browser-Use Agents ...</a></li>
<li><a href="https://www.wired.com/story/google-built-a-giant-mirror-dimension-internet-to-test-its-chrome-ai-agents/">Google Built a Giant ‘Mirror Dimension’ Internet to Test Its ...</a></li>
<li><a href="https://explainx.ai/blog/google-mirror-dimension-synthetic-web-chrome-auto-browse-agents-prompt-injection-testing-2026">Google Mirror Dimension: Fake Web for Chrome AI Agents ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#browser automation`, `#prompt injection`, `#AI security`, `#testing infrastructure`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美股科技股单日重挫，亚洲多地推出应急稳市措施](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

美国 AI 科技股周五遭遇大规模抛售，纳斯达克指数单日下跌 5.28%，费城半导体指数重挫近 11%。随后，中国内地、韩国和中国台湾地区在同一周内相继出台融资保证金、卖空限制等应急稳市措施。

telegram · zaihuapd · 11月22日 13:24

**「背景」** 融资保证金比例指投资者借钱买股票时需自付的资金占比，下调该比例意味着券商可提供更多融资；禁止“平盘以下卖空”则是限制投资者在股价低于前一日收盘价时做空。

**「影响」** 这些措施直接改变中国内地、韩国和中国台湾地区股市投资者的融资成本与做空条件，其中韩国放宽回购限制为期 3 个月，中国台湾地区将融券保证金比例由 130%提高至 150%。

**标签**: `#US tech selloff`, `#market stabilization policy`, `#short-selling rules`, `#Asian equities`, `#margin requirements`

---

<a id="item-finance-news-2"></a>
### [中国商务部要求美国撤销电话号段接入限制](https://www.bloomberg.com/news/articles/2026-11-22/china-objects-to-us-curbs-on-telecoms-access-to-phone-numbers) ⭐️ 7.0/10

中国商务部 11 月 22 日敦促美国撤销一项限制中国移动、中国电信、中国联通直接接入美国电话号码的措施，称其违反非歧视与公平竞争原则；美国联邦通信委员会（FCC）则于 11 月 19 日投票收紧对申请直接接入美国号码的互联网语音服务商的安全要求，新增国家安全认证。

telegram · zaihuapd · 11月22日 06:44

**「背景」** 美国联邦通信委员会（FCC）此前已逐步收紧对中国三大运营商的授权：2019 年驳回中国移动在美提供电信服务的申请，2021 年和 2022 年又分别撤销中国电信和中国联通的授权。此次 11 月 19 日的投票进一步要求申请直接接入美国号码的互联网语音服务商通过新增的国家安全认证，以阻止其“涵盖清单”上的实体、设备和服务接入美国网络。

**「影响」** 若该措施维持，三家中国运营商将更难直接接入美国电话网络，依赖其线路的中美跨境通话用户和企业可能面临通话路径调整。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.foxbusiness.com/politics/fcc-bans-chinese-firms-direct-access-us-phone-numbers-bid-curb-robocalls">FCC regulators bar Chinese telecom giants from direct number access</a></li>
<li><a href="https://insidetowers.com/congress-subpoenas-three-china-telecoms/">Congress Subpoenas Three China Telecoms - Inside Towers</a></li>

</ul>
</details>

**标签**: `#telecom regulation`, `#US-China relations`, `#FCC`, `#China carriers`, `#trade policy`

---

<a id="item-finance-news-3"></a>
### [蚂蚁集团领投 Simplexity Robotics 1 亿美元融资，投后估值 16 亿美元](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 7.0/10

彭博报道，中国具身智能公司 Simplexity Robotics 完成 1 亿美元 pre-A 轮融资，由蚂蚁集团领投，投后估值 16 亿美元；董事长兼联合创始人 Wang Kai 向彭博确认了这一消息。

telegram · zaihuapd · 11月23日 02:02

**「背景」** Simplexity Robotics（至简动力）于 2025 年 7 月在杭州成立，核心团队来自理想汽车；据盖世汽车报道，该公司今年 3 月首次公开融资消息，称成立半年内完成五轮融资、累计 20 亿元人民币，当时投后估值已超过 10 亿美元。

**「影响」** 这笔融资将用于与宇树、优必选等更成熟的厂商争夺市场，意味着中国具身智能和人形机器人赛道的资本正进一步向少数头部初创公司集中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gasgoo.com/robot/news/70449505-%E7%90%86%E6%83%B3%E5%89%8D%E9%AB%98%E7%AE%A1%E5%81%9A%E6%9C%BA%E5%99%A8%E4%BA%BA-%E5%8D%8A%E5%B9%B4%E8%9E%8D%E4%BA%8620%E4%BA%BF-%E6%80%8E%E4%B9%88%E5%81%9A%E5%88%B0%E7%9A%84/">理 想 前高管做机器人，半年 融 了20亿，怎么做到的？ | 盖世 汽 车</a></li>

</ul>
</details>

**标签**: `#embodied AI`, `#humanoid robotics`, `#venture funding`, `#China tech`, `#Ant Group`

---