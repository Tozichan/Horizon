---
layout: default
title: "Horizon Summary: 2026-11-26 (ZH)"
date: 2026-11-26
lang: zh
---

> 从 74 条内容中筛选出 13 条重要资讯。

---

**科技新闻**
1. [1Password 披露员工 GitHub 账户被入侵事件](#item-tech-news-1) ⭐️ 8.0/10
2. [Anthropic 相关 GRH Lean 验证出现大幅精简版本](#item-tech-news-2) ⭐️ 8.0/10
3. [Linux 内核 NFS 服务器曝出潜伏 12 年的预认证远程 root 漏洞](#item-tech-news-3) ⭐️ 8.0/10
4. [FCC 批准 SpaceX 部署最多 100 万颗 Starmind 数据中心卫星](#item-tech-news-4) ⭐️ 8.0/10
5. [Minecraft Java 版曝高危 RCE 漏洞，暂无官方补丁](#item-tech-news-5) ⭐️ 8.0/10
6. [Aaronson 博客与矩阵乘法指数论文引发热议](#item-tech-news-6) ⭐️ 7.0/10
7. [意大利与瑞士警告自主 AI 驱动网络攻击](#item-tech-news-7) ⭐️ 7.0/10
8. [Drupal 严重 RCE 漏洞已被在野利用，可劫持站点](#item-tech-news-8) ⭐️ 7.0/10
9. [OpenAI 将网络安全列为下一个增长引擎，称其规模或超编程业务](#item-tech-news-9) ⭐️ 7.0/10
10. [腾讯开源 Hy4 flash 量化权重，最小版可在 64 GB Mac mini 运行](#item-tech-news-10) ⭐️ 7.0/10
11. [三星与 SK 海力士据报交叉许可采用长江存储 Xtacking 技术](#item-tech-news-11) ⭐️ 7.0/10

**财经新闻**
1. [美商务部被曝施压英特尔交出 10%股权](#item-finance-news-1) ⭐️ 8.0/10
2. [美国拟对 14 个贸易伙伴加征第 301 条关税](#item-finance-news-2) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [1Password 披露员工 GitHub 账户被入侵事件](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password 披露了一起安全事件：一名员工的企业 GitHub 账户被入侵，攻击者借此访问源代码，并向公司后台服务推送恶意代码，导致部分客户账户信息被下载。公司称泄露信息包括姓名、邮箱地址、账户标识以及账户创建和最近登录时间，客户保险库及其内容未受影响。1Password 于 11 月 19 日开始调查相关迹象，未披露受影响用户数量，已停用涉事账户、轮换或撤销可能暴露的内部凭证，并加强了邀请和恢复邮件的验证码。公司表示用户无需更改账户，但应警惕钓鱼。

hackernews · lxhrstn · 11月25日 17:18 · [社区讨论](https://news.ycombinator.com/item?id=50644817)

**「事件背景」** 1Password 于 2026 年 11 月 19 日开始调查员工企业 GitHub 账户被入侵的迹象，随后确认攻击者通过该账户访问源代码并向后台服务推送恶意代码，导致部分客户账户信息被下载。此次披露的细节包括：受影响数据涉及姓名、邮箱地址、账户标识及创建和最近登录时间，客户保险库及其内容未受影响；公司未披露受影响用户数量，已停用涉事账户、轮换或撤销可能暴露的内部凭证，并加强了邀请和恢复邮件的验证码机制。

**「影响与应对」** 1Password 表示现有用户无需更改账户或密码，但需对冒充该公司的钓鱼邮件保持警惕。对使用在线同步保险库的用户而言，此次事件的关键限制在于：公司称保险库内容未被访问，但未说明加密保险库本身是否被下载。

**「社区讨论」** 评论者 tptacek 认为，员工笔记本被攻陷后向 GitHub 推送代码并部署，是 SaaS 公司最主要的攻击路径，随着员工规模增长，这类风险几乎不可避免。评论者 ctidd 批评公告未说明是否缺少分支保护规则、推送主分支为何未被阻止；qixxiq 则报告收到一封包含部分个人细节的高质量钓鱼邮件，发件域并非 1Password 官方域名。另有长期用户 ChrisHardie 表示，因担心此类事件而坚持使用仅本地保险库。

<details><summary>参考链接</summary>
<ul>
<li>Update on a security incident involving 1Password&#x27;s backend systems.</li>
<li>1Password Discloses GitHub Account Breach Exposing Limited Customer Data</li>
<li>1Password posted an update on its Nov 19 security incident. An attacker got into an employee&#x27;s ... - Threads</li>

</ul>
</details>

**标签**: `#security`, `#supply-chain`, `#saas`, `#password-managers`, `#phishing`

---

<a id="item-tech-news-2"></a>
### [Anthropic 相关 GRH Lean 验证出现大幅精简版本](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

GitHub 上出现了一个更短、更易读的广义黎曼猜想（GRH）Lean 验证仓库，被归为 Anthropic 相关工作的产物。据社区评论，该版本从约 1700 万行缩减到约 7.6 万行，并明确区分“已知数学”与“新数学”，还配有大量人类可读文档。上述行数对比来自评论者而非独立测量，仓库本身也未在现有材料中给出独立验证结论。

hackernews · nb-t · 11月25日 21:48 · [社区讨论](https://news.ycombinator.com/item?id=50648050)

**「背景」** 广义黎曼猜想是黎曼猜想向更一般数域情形的推广，后者断言黎曼ζ函数的所有非平凡零点都位于临界线上。据 NPR 报道，Anthropic 的 Levent Alpöge 与 Claude 合作，以约 1700 万行 Lean 代码发布了该猜想的证明，但这一结果尚未得到确认。此次仓库则提供了据称约 7.6 万行的更短、更易读的 Lean 验证版本。

**「对形式化验证社区的影响」** 该仓库将证明规模从约 1700 万行压缩到约 7.6 万行，并明确区分“已知数学”与“新数学”，这直接降低了人工审阅 Lean 代码的门槛。不过，社区讨论中有人指出，仍需数学家真正理解核心论证并写成可读的数学论文；这与 Terence Tao 此前提出的“AI 能生成正确但无人能读的证明”的担忧相呼应，说明可读性改善并不等于数学洞见已经得到验证。

**「社区讨论」** 有评论者认为，清晰区分已知与新数学、加上可读文档，将显著降低理解门槛；也有人追问这是否回应了陶哲轩此前关于“巨大证明缺乏洞见”的担忧，以及更聪明的 LLM 是否已能压缩并解释证明。另有评论者表示，更希望有数学家真正吃透核心论证，写成正式数学论文并在会议上讲解，而不只是提供 Lean 代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Riemann_hypothesis">Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://phys.org/news/2026-11-sacred-mathematics-riemann-hypothesis-ai.html">&#x27;The sacred object in mathematics&#x27;: The Riemann hypothesis , AI and...</a></li>
<li><a href="https://www.npr.org/2026/11/21/g-s1-154922/anthropic-worker-claims-to-have-solved-a-holy-grail-of-math-problems-with-the-help-of-ai">Anthropic worker claims to have solved a Holy Grail of math... : NPR</a></li>
<li><a href="https://tangente-mag.com/en/articles/terence-tao-warns-ai-is-writing-proofs-that-no-one-can-read">Terence Tao warns: AI writes proofs no one can read</a></li>
<li><a href="https://yage.ai/share/tao-lean-formalization-credibility-en-20260623.html">When Terence Tao Says AI Crossed the Critical Threshold of ...</a></li>

</ul>
</details>

**标签**: `#formal-verification`, `#lean`, `#mathematics`, `#ai-assisted-proofs`, `#open-source`

---

<a id="item-tech-news-3"></a>
### [Linux 内核 NFS 服务器曝出潜伏 12 年的预认证远程 root 漏洞](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

一篇博客文章披露了 Linux 内核 NFS 服务器中一个长期存在的预认证远程 root 漏洞，据称已潜伏 12 年。文章给出的临时缓解措施是关闭 NFS 4.1 和 4.2 协议，例如在停止 nfs-server 后执行 \`echo &quot;-4.1 -4.2&quot; \| sudo tee /proc/fs/nfsd/versions\`，该改动在重启后会失效。社区评论指出，上游据称已在数月前修复，且目前没有公开的 PoC。由于没有源代码内容可供核对，漏洞编号、受影响内核版本和修复提交等细节无法从现有材料中确认。

hackernews · dm · 11月25日 20:35 · [社区讨论](https://news.ycombinator.com/item?id=50647161)

**「背景」** 该漏洞被编号为 CVE-2026-99362，影响 Linux 内核 NFS 服务器（nfsd，监听 2049 端口），据 OpenSec 的博客描述，其存在时间约 12 年。社区讨论指出，该问题主要涉及 NFS 4.1 和 4.2 及更高版本协议，并称上游已在数月前完成修补。

**「影响与应对」** 运行 NFS 服务且无法立即升级内核的用户，可参照文章建议先确认客户端是否实际使用 4.1/4.2，再通过 \`/proc/fs/nfsd/versions\` 临时禁用这两个子版本；但该设置重启后失效，需要重新应用或改用持久化配置。评论者同时提醒，NFS 通常不应直接暴露在公网，这在一定程度上限制了实际攻击面。

**「社区讨论」** 有评论者表示可用 yeet 的 XDP 七层可编程防火墙规则拦截，并称已在自己的环境中验证；另有评论者认为该漏洞仅涉及 NFS 4.1/4.2，因此对不受支持的内核发行版采用禁用这两个版本的临时方案。也有人强调目前没有公开 PoC、上游数月前已修复，并认为这再次说明不应把 C 代码直接暴露在互联网上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS 2 ROOT ( CVE - 2026 - 99362 ): pre - auth root in Linux nfsd | OpenSec</a></li>

</ul>
</details>

**标签**: `#linux-kernel`, `#nfs`, `#security-vulnerability`, `#remote-code-execution`, `#mitigation`

---

<a id="item-tech-news-4"></a>
### [FCC 批准 SpaceX 部署最多 100 万颗 Starmind 数据中心卫星](https://www.theverge.com/science/1042278/spacex-fcc-starmind-ai-space-data-centers) ⭐️ 8.0/10

美国联邦通信委员会（FCC）批准 SpaceX 部署最多 100 万颗搭载 AI 芯片的卫星，用于其“Starmind”在轨数据处理网络，卫星运行高度为 500 至 1002 公里。FCC 称这是该机构首次批准完整的 AI 卫星星座，此前 Google、Blue Origin 等公司也在探索太空数据中心。授权附带条件：首颗卫星须不晚于 2033 年投入运行，100 万颗的规模须在 2040 年前达成，并需满足通信备份、定期提交进展和轨道碎片减缓方案等要求。FCC 同时暂缓处理 SpaceX 关于将 600 公里以上卫星处置于“坟墓轨道”的请求，并驳回了亚马逊、Viasat 和美国天文学会的反对意见。

rss · The Verge · 11月25日 17:44

**「背景」** Starmind 是 SpaceX 正在推进的在轨 AI 数据中心星座计划，其首款卫星设计名为 AI1。FCC 此次批准的是该星座的完整部署授权，而非单颗试验卫星；此前 Google、Blue Origin 等公司也在探索太空数据中心方案，但 FCC 称这是其首次批准完整的 AI 卫星星座。

**「对相关方的影响」** 该授权为 SpaceX 设定了明确的分阶段履约节点：首颗卫星须在 2033 年前投入运行，100 万颗规模须在 2040 年前达成，并需定期提交进展报告和轨道碎片减缓方案。FCC 同时驳回了亚马逊、Viasat 和美国天文学会的反对意见，并暂缓处理 SpaceX 关于在 600 公里以上采用“墓地轨道”处置卫星的请求，这意味着高轨卫星的处置方式仍待进一步明确。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Starmind_%28satellite%29">Starmind (satellite) - Wikipedia</a></li>
<li><a href="https://www.space.com/space-exploration/launches-spacecraft/green-light-for-starmind-spacex-gets-approval-to-deploy-1-million-ai-satellites">Green light for Starmind: SpaceX gets approval to deploy 1 ...</a></li>

</ul>
</details>

**标签**: `#space-computing`, `#AI-infrastructure`, `#satellites`, `#regulation`, `#SpaceX`

---

<a id="item-tech-news-5"></a>
### [Minecraft Java 版曝高危 RCE 漏洞，暂无官方补丁](https://github.com/bikini/minecraft2shell) ⭐️ 8.0/10

11 月 22 日公开的 minecraft2shell 披露，Minecraft Java 版服务器资源包中的特制 TrueType 字体可触发 FreeType 2.14.3 及更早版本的原生越界写，从而在 Windows 客户端执行任意代码。受影响范围为 Java 版 1.20.5 至 1.21.10 以及 26.1 至 26.4 快照，1.20.4 及更早版本和基岩版不受影响。Mojang 目前仍使用 lwjgl-freetype 3.4.3，尚未发布官方补丁；社区于 11 月 24 日发布 m2sfix 1.0.0，通过 Java agent 或 mod 关闭 hinting 作为临时缓解。投稿人建议在修复前不要添加任何资源包，将多人游戏服务器资源包权限设为“禁用”，或安装社区临时修复 mod。

telegram · zaihuapd · 11月25日 12:46

**「背景」** 该漏洞的根源在 FreeType 字体渲染库：Minecraft Java 版通过 lwjgl-freetype 调用它来解析服务器资源包中的 TrueType 字体，而 2.14.3 及更早版本的 FreeType 存在原生越界写问题。公开的 minecraft2shell 项目展示了如何利用这一缺陷，在受影响客户端上实现任意代码执行。

**「影响与应对」** 在官方补丁发布前，服务器运营者和玩家应避免加载不受信任的资源包，或将多人游戏资源包权限设为“禁用”。社区修复项目 minecraft2shell-fix 说明，1.20.5 至 1.21.x 运行 Java 21，可直接使用其 Java agent 或 mod 关闭 hinting；1.20.4 及更早版本客户端不调用 FreeType，因此该修复对其无效。该项目自述为临时方案而非 Mojang 官方修复，可能产生误报和漏报，安装风险由用户自行承担。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/bikini/minecraft2shell">GitHub - bikini/ minecraft 2 shell : Minecraft to native RCE · GitHub</a></li>
<li><a href="https://github.com/sunrisemc-tw/minecraft2shell-fix">GitHub - sunrisemc-tw/minecraft2shell-fix: Client-side ...</a></li>
<li><a href="https://github.com/sunrisemc-tw/minecraft2shell-fix/releases">Releases · sunrisemc-tw/minecraft2shell-fix · GitHub</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#minecraft`, `#freetype`, `#open-source`

---

<a id="item-tech-news-6"></a>
### [Aaronson 博客与矩阵乘法指数论文引发热议](https://scottaaronson.blog/?p=10379) ⭐️ 7.0/10

Hacker News 上一条指向 Scott Aaronson 博客文章、并关联一篇题为《The matrix multiplication exponent is nine fourths》的论文的帖子获得约 1132 分和 960 条评论。现有材料只包含链接和评论摘录，没有给出论文的具体方法、证明细节或可验证的数值结果，因此无法确认“矩阵乘法指数为九分之四”这一说法本身是否成立。讨论的核心并非技术细节，而是 AI 在数学与科学发现中扮演的角色。

hackernews · Kotlopou · 11月25日 19:11 · [社区讨论](https://news.ycombinator.com/item?id=50646108)

**「背景」** 该讨论围绕一篇 2026 年 11 月 24 日发布在 OpenAI 数学仓库的预印本展开，论文声称方阵乘法的指数 ω 在每个域上都恰好等于 9/4（即 2.25），并称其将 9/4 的上界与形式算术电路所需的下界相匹配。此前 9/4 仅作为上界已知，因此该预印本的新意在于声称给出了匹配的下界；这些结论来自论文自身声明，尚待独立验证。

**「社区讨论」** 有评论者（jsLavaGoat）认为，AI 擅长公理化数学这类分析性、先验性的工作，但这不能推出它同样能“解决”其他领域或写出《银河百科全书》。另一位评论者（utopiah）则质疑，仅靠 Lean、MathLib 和大量算力、不借助 LLM 或生成式 AI，是否也能取得类似进展，并指出相关基础设施已积累十余年。这些均为个人观点，评论热度不代表共识。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://raw.githubusercontent.com/openai/math/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf">The matrix multiplication exponent is nine fourths</a></li>
<li><a href="https://aiweekly.co/alerts/openai-claims-matrix-multiplication-exponent-is-exactly-94">OpenAI claims matrix multiplication exponent is exactly 9/4</a></li>

</ul>
</details>

**标签**: `#AI`, `#mathematics`, `#matrix multiplication`, `#scientific progress`, `#community discussion`

---

<a id="item-tech-news-7"></a>
### [意大利与瑞士警告自主 AI 驱动网络攻击](https://www.bleepingcomputer.com/news/security/italy-and-switzerland-warn-of-autonomous-ai-driven-cyberattacks/) ⭐️ 7.0/10

瑞士和意大利的网络安全机构警告称，由 AI 智能体驱动的自动化网络攻击正针对关键基础设施领域的组织。该警告来自两国官方网络安全机构，但现有报道仅为简短摘要，未披露具体攻击手法、受影响组织、时间范围或已确认的入侵案例。因此，这目前属于机构风险提示，而非已独立验证的攻击事件或技术细节披露。

rss · BleepingComputer · 11月25日 19:39

**「背景」** 瑞士国家网络安全中心（NCSC）与意大利 CSIRT 于 2026 年 11 月发布协调警告，此前瑞士方面确认了该国首批由 AI 辅助实施的网络攻击案例，受影响对象包括至少两个行业的企业和关键基础设施运营者。据外部威胁研究报道，攻击者使用了 ARTEX AI、CyberStrikeAI、DeepSeek Harness 和 PentAGI 等多智能体框架，自主串联漏洞与配置错误；该细节来自第三方报道，尚未在原始来源中得到独立确认。

**「对关键基础设施运营方的影响」** 该警告针对的是关键基础设施领域的组织，而 AI 代理能够自主读取文件、调用 API、执行代码并串联多步操作，无需人工逐步批准，这意味着传统依赖人工审核环节的防御节奏可能跟不上攻击速度。运营方应把代理式 AI 的权限边界和操作审计纳入现有安全评估，并关注本国监管机构后续发布的具体指引；目前来源仅给出警告，未提供攻击样本、受影响系统或缓解措施细节。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aviatrix.ai/threat-research-center/italy-switzerland-autonomous-ai-driven-cyberattacks-2026/">Italy &amp; Switzerland Warn of Autonomous AI Cyberattacks on ...</a></li>
<li><a href="https://cybersecuritynews.com/switzerland-ai-agent-cyberattacks/">Switzerland Confirms First AI-Agent Cyberattacks That ...</a></li>
<li><a href="https://jetico.com/blog/agentic-ai-security-risks-enisas-warning-and-the-hugging-face-incident/">Agentic AI Security Risks: ENISA&#x27;s Warning &amp; the Hugging... - Jetico</a></li>

</ul>
</details>

**标签**: `#AI security`, `#cybersecurity`, `#autonomous agents`, `#critical infrastructure`

---

<a id="item-tech-news-8"></a>
### [Drupal 严重 RCE 漏洞已被在野利用，可劫持站点](https://www.bleepingcomputer.com/news/security/hackers-now-exploit-critical-drupal-rce-flaw-to-hijack-sites/) ⭐️ 7.0/10

Drupal 安全团队确认，一个可让攻击者劫持未修补站点的严重远程代码执行漏洞至少自周四起已被在野积极利用。该漏洞的具体技术细节、受影响版本范围以及修复补丁信息在现有报道中尚未披露。运行 Drupal 的站点运营方应尽快关注官方安全公告并采取修补措施。

rss · BleepingComputer · 11月25日 10:10

**「背景」** Drupal 安全团队此前披露并修复了一个被评级为“严重”的安装程序漏洞 CVE-2026-132165，该漏洞在特定配置下可能导致站点被接管或远程代码执行。此次报道的漏洞是另一个已被确认在野利用的严重 RCE 问题，说明相关风险已从理论缺陷转为实际攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/drupal-patches-critical-installer-flaw.html">Drupal Patches Critical Installer Flaw That Could Give...</a></li>

</ul>
</details>

**标签**: `#security`, `#drupal`, `#vulnerability`, `#remote-code-execution`, `#web-security`

---

<a id="item-tech-news-9"></a>
### [OpenAI 将网络安全列为下一个增长引擎，称其规模或超编程业务](https://www.theinformation.com/newsletters/ai-agenda/openais-roadmap-making-cyber-bigger-coding-remains-blurry) ⭐️ 7.0/10

OpenAI 将网络安全定位为可能超过编程业务的下一个增长引擎。公司 CFO 表示，外界对网络安全市场规模超过 3000 亿美元的估算仍被严重低估；总裁格雷格·布罗克曼称，网络安全将成为 OpenAI 比编程更大的业务板块。公司已推出面向安全研究的 GPT-6 Cyber，并扩大“网络安全受信访问”计划（Daybreak），截至今年 9 月覆盖数千名经过验证的防御者及约 2000 个获批组织和工作空间，支持漏洞发现、代码库分析与二进制逆向。上述市场规模和业务对比均为公司方面的说法，报道同时指出，其与 Anthropic、Google 的竞争以及规模化商业化前景仍不清晰。

telegram · zaihuapd · 11月25日 04:51

**「背景」** Daybreak 是 OpenAI 面向网络安全的受信访问计划，官方说明其通过 Blue 和 Red 两个访问层级，让符合条件的企业客户和安全从业者在授权范围内使用 OpenAI 模型开展防御性工作与高级测试。此次报道中的 GPT-6 Cyber 与 Daybreak 扩容，是在这一既有计划基础上的进一步推进。

**「对安全团队的影响」** 对安全研究团队而言，Daybreak 的准入机制意味着相关能力并非公开可用，而是需要经过验证并获得组织级批准；报道给出的约 2000 个获批组织和工作空间，可作为评估当前覆盖范围的参考。由于商业化路径尚未明确，企业暂不宜据此调整采购或工具链规划。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity</a></li>
<li><a href="https://help.openai.com/en/articles/20001258-openai-daybreak-trusted-access-for-cyber-overview">OpenAI Daybreak - Trusted Access for Cyber overview</a></li>
<li><a href="https://openai.com/business/solutions/cybersecurity/">AI for Cybersecurity Teams | OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#cybersecurity`, `#AI security`, `#business strategy`, `#trusted access`

---

<a id="item-tech-news-10"></a>
### [腾讯开源 Hy4 flash 量化权重，最小版可在 64 GB Mac mini 运行](https://mp.weixin.qq.com/s/o0xxShVQX6g2UllrrEv1WQ) ⭐️ 7.0/10

腾讯混元通过大模型压缩加速工具箱 AngelSlim 开源了 224B 参数模型 Hy4 flash 的 GGUF 量化权重。原权重约 410.27GiB，最小的 IQ2-AH 版本为 125.73GiB，约为原版的 30%；据称借助 Strata offload 框架，64 GB Mac mini 可以运行该版本。来源还给出吞吐数据：48 GB 显存设备在 10K 上下文下每秒生成 89 个 token，M5 Max 128 GB 上 Q3\_K 版本在 32K 上下文下每秒生成 47 个 token；在 DeepSWE v1.1 等评测中，Q3\_K 与原模型得分差距不超过 0.4 分。上述运行与性能数据来自腾讯方面的说法，来源未提供独立复现。

telegram · zaihuapd · 11月25日 09:29

**「背景」** Hy4 flash 是腾讯混元此前已开放权重的约 220B 参数模型（约 12B 激活参数），其 Hugging Face 模型页同时指向腾讯的模型压缩工具包 AngelSlim。此次开源的是 AngelSlim 产出的 GGUF 量化权重，而非新的基础模型；量化把原始约 410.27GiB 的权重压缩到最小 125.73GiB，并配合 Strata offload 框架降低本地运行的内存门槛。

**「对本地部署的影响」** 对希望在消费级硬件上本地运行大模型的用户而言，这次发布提供了 224B 模型的多种 GGUF 量化档位，其中 IQ2-AH 的体积门槛最低，但 125.73GiB 仍远超 64 GB 内存，实际运行依赖 Strata offload 将部分权重卸载到其他存储或内存层级，因此速度与体验会受卸载策略影响。Q3\_K 在评测中与原模型差距不超过 0.4 分，说明量化在精度上的代价较小，但相关吞吐数字对应的是特定硬件和上下文长度，不能直接外推到其他设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=85Gm68lK0sI">Tencent Hy 4 Flash Is Out. Time to Ditch Qwen 3.8 Flash ... - YouTube</a></li>
<li><a href="https://huggingface.co/tencent/Hy4-flash">tencent / Hy 4 - flash · Hugging Face</a></li>
<li><a href="https://github.com/Tencent/AngelSlim">GitHub - Tencent / AngelSlim : Model compression toolkit engineered...</a></li>

</ul>
</details>

**标签**: `#open-source`, `#quantization`, `#LLM inference`, `#local deployment`, `#Tencent Hunyuan`

---

<a id="item-tech-news-11"></a>
### [三星与 SK 海力士据报交叉许可采用长江存储 Xtacking 技术](https://tech.ifeng.com/c/8yLRPKxQy4L) ⭐️ 7.0/10

据凤凰网报道，三星电子和 SK 海力士已通过交叉许可协议，同意在 3D NAND 闪存中采用长江存储 Xtacking 堆叠技术的部分内容。Xtacking 将存储单元与控制电路（CMOS）分别制作在两片晶圆上，再通过键合工艺合二为一，使两部分可独立生产和优化。报道称三方均拒绝置评，因此协议的具体范围、许可条款和量产时间均未得到确认。

telegram · zaihuapd · 11月25日 14:33

**「背景」** Xtacking 是长江存储提出的 3D NAND 架构：存储单元阵列与 CMOS 逻辑电路分别在两片晶圆上制造，再通过键合工艺合为一体，使两部分可独立生产与优化。据 TrendForce 和 TechPowerUp 报道，三星与 SK 海力士正推进数百层堆叠的 3D NAND，单晶圆工艺逐渐逼近限制，而长江存储的键合方案已历经量产验证，并自 2018 年以来积累了 4000 多项与 3D 存储制造、封装相关的专利。

**「潜在影响」** 若报道属实，采用该键合架构后，存储厂商可将逻辑电路交由晶圆代工厂生产，从而使用更先进的制程；Omdia 高级分析师在报道中表达了这一观点。由于各方未确认，目前尚不能判断相关技术会用于哪些产品线或何时落地。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.trendforce.com/news/2026/11/25/news-sk-hynix-reportedly-joins-samsung-in-licensing-ymtcs-xtacking-technology-as-nand-race-heats-up/">[News] SK hynix Reportedly Joins Samsung in Licensing YMTC’s ...</a></li>
<li><a href="https://www.techpowerup.com/355199/samsung-and-sk-hynix-to-license-ymtcs-xtacking-technology">Samsung and SK hynix to License YMTC&#x27;s Xtacking Technology</a></li>

</ul>
</details>

**标签**: `#3D NAND`, `#semiconductor manufacturing`, `#hybrid bonding`, `#YMTC`, `#memory hardware`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美商务部被曝施压英特尔交出 10%股权](https://www.wired.com/story/inside-trumps-demands-to-another-chips-ceo/) ⭐️ 8.0/10

据 WIRED 援引法庭文件报道，2025 年 8 月美国商务部律师在与英特尔首席财务官通话时表示，这并非一场谈判，总统希望周五宣布协议，董事会可以拒绝但会面临无法预测的后果；几天后英特尔董事会交出了美方要求的股份。特朗普随后宣布美国政府“完全拥有并控制英特尔 10%的股份”，且未为此付款，这批股份现值约 110 亿美元。

telegram · zaihuapd · 11月25日 13:25

**「背景」** 据《纽约时报》报道，特朗普政府正通过持股方式向英特尔等私营企业投入数十亿美元，这种非常规做法目前没有放缓迹象（tool-2-2）。

**「影响」** 若报道属实，美国政府直接持有英特尔约 10%股份，意味着其从补贴提供方变为股东，可能影响这家芯片制造商的公司治理与决策独立性；分析人士指出，此类深度政府介入存在政治反弹风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2025/11/25/us/politics/trump-intel-steel-minerals-china.html">Trump Administration Is Taking Billions in Stakes in Firms Like Intel ...</a></li>
<li><a href="https://www.npr.org/2025/09/06/nx-s1-5530190/government-stake-intel-ai-competition-china">The U.S. government is taking a stake in Intel . It&#x27;s rare — and... : NPR</a></li>
<li><a href="https://www.ainvest.com/news/trump-policy-shifts-reshaping-chip-investment-incentives-navigating-high-stakes-semiconductor-landscape-2508/">Trump&#x27;s Policy Shifts and the Reshaping of U.S. Chip Investment...</a></li>

</ul>
</details>

**标签**: `#semiconductor industry`, `#US industrial policy`, `#Intel`, `#government equity stake`, `#corporate governance`

---

<a id="item-finance-news-2"></a>
### [美国拟对 14 个贸易伙伴加征第 301 条关税](https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html) ⭐️ 8.0/10

美国政府拟依据 1974 年《贸易法》第 301 条，对中国、欧盟、日本、印度等 14 个贸易伙伴加征国别设定的新关税，理由是这些国家制造业存在结构性产能过剩。其中，中国将在 2018 年已加征的 25%关税之上再加征 20%；若中国未遵守 2025 年 10 月在韩国釜山达成的贸易休战协议，对华新关税可能升至 40%。

telegram · zaihuapd · 11月25日 13:59

**「背景」** 美国贸易代表办公室于 2026 年 3 月启动了对 16 个经济体制造业“结构性产能过剩”的第 301 条调查，此次拟议关税正是该调查的后续裁定。中美两国领导人于 2025 年 10 月在韩国釜山会晤并达成贸易休战协议，该协议是美方评估是否将对华新关税从 20%上调至 40%的依据。

**「可能影响」** 若该提案落地，中国输美商品将在 2018 年已加征的 25%关税之上再叠加 20%，相关出口企业和美国进口商、消费者将直接承担更高成本；欧盟、日本、印度等 13 个伙伴的税率按国别设定，具体商品范围和生效时间尚未公布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.hklaw.com/en/insights/publications/2026/11/ustr-proposes-tariffs-following-14-section-301">USTR Proposes Tariffs Following 14 Section 301 Manufacturing ...</a></li>
<li><a href="https://kpmg.com/us/en/taxnewsflash/news/2026/11/tnf-ustr-findings-and-proposed-section-301-tariffs-on-14-economies-relating-to-structural-excess-capacity-and-production-in-manufacturing-sectors.html">USTR findings and proposed Section 301 tariffs on 14 ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Busan_Summit">Busan Summit - Wikipedia</a></li>
<li><a href="https://www.cfr.org/articles/united-states-and-china-agree-trade-truce">United States and China Agree to Trade Truce | Council on ...</a></li>
<li><a href="https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html">U . S . unveils new Section 301 tariffs targeting China , EU and others</a></li>

</ul>
</details>

**标签**: `#trade policy`, `#tariffs`, `#Section 301`, `#US-China trade`, `#manufacturing`

---