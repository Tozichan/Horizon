---
layout: default
title: "Horizon Summary: 2026-11-16 (EN)"
date: 2026-11-16
lang: en
---

> From 52 items, 10 important content pieces were selected

---

**Technology News**
1. [Meta FAIR and NYU study finds vision encoder pretraining optional, vision-only parameters necessary](#item-tech-news-1) ⭐️ 8.0/10
2. [World-model CS:GO-like multiplayer beta runs per-player views on local GPUs](#item-tech-news-2) ⭐️ 8.0/10
3. [Meituan open-sources LongCat-2.5, claims Huawei Ascend-only training](#item-tech-news-3) ⭐️ 8.0/10
4. [MacBook Pro OLED PWM Flicker Draws Technical Scrutiny](#item-tech-news-4) ⭐️ 7.0/10
5. [Protomaps Makes Self-Hosting Map Tiles Cheap and Easy](#item-tech-news-5) ⭐️ 7.0/10
6. [Congress Moves to Tighten AI Chip Export Rules After Nvidia Scandal](#item-tech-news-6) ⭐️ 7.0/10
7. [FBI warns AI hacking framework ARTEX is automating cyberattacks](#item-tech-news-7) ⭐️ 7.0/10
8. [Tool claims ~5x faster pageable cudaMemcpy on B300](#item-tech-news-8) ⭐️ 7.0/10

**Financial News**
1. [US, China, Russia Leaders to Hold First Trilateral Meeting at Shenzhen APEC](#item-finance-news-1) ⭐️ 9.0/10
2. [US Judge Allows DRAM Price-Fixing Lawsuit Against Micron, Samsung and SK Hynix to Proceed](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Meta FAIR and NYU study finds vision encoder pretraining optional, vision-only parameters necessary](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR and NYU researchers trained more than 200 multimodal LLMs from scratch on identical data and matched lifetime compute budgets to isolate three design choices in standard vision encoders: separate pretraining, vision-only parameters, and placement before the LLM. They report that encoder pretraining is optional — encoders pretrained with contrastive, self-supervised, or captioning objectives at best tied an encoder trained from scratch with the LLM, and even free pretraining did not help; extending MetaCLIP pretraining 6.5x raised ImageNet linear-probe accuracy from 80.4% to 84.4% without improving VQA. Vision-only parameters were required: encoder-free models trailed at every size from 0.6B to 6.4B and needed roughly 3x the compute to catch up. Placement before the LLM was also optional, with an &quot;in-fusion&quot; variant adding zero-initialized vision-only weights to the LLM&\#x27;s first 8 layers matching the encoder from 1.7B to 6.4B while cutting time to first token by about 13%. Main comparisons used Qwen3-1.7B and 4B configurations with 0.4B vision parameters, evaluated on 16 Cambrian VQA benchmarks at 448 px and 12 language benchmarks; the post links to a paper and blog rather than a full technical writeup.

reddit · r/MachineLearning · /u/trungh98 · Nov 15, 17:38

**「Background」** Standard multimodal LLM designs typically pair a separately pretrained vision encoder, such as CLIP-style contrastive models, with a language model, and published models differ widely in whether they keep, drop, or retrain that encoder. Because those models also differ in training data and compute, their results cannot isolate which encoder design choices actually matter. The Meta FAIR and NYU study addresses this by training 200+ models from scratch under matched data and compute budgets, counting encoder pretraining against the same lifetime compute as multimodal training.

**「Impact」** The results suggest teams building MLLMs can skip a separate vision-encoder pretraining stage and its compute cost, but should still allocate dedicated vision-only parameters rather than sharing them with text tokens. The authors also report that adding vision-only branches to the first 8 layers of a pretrained 1.7B LLM during midtraining preserved the effect, indicating the approach is not limited to from-scratch training.

**Tags**: `#multimodal LLMs`, `#vision encoders`, `#model architecture`, `#training methodology`, `#research`

---

<a id="item-tech-news-2"></a>
### [World-model CS:GO-like multiplayer beta runs per-player views on local GPUs](https://www.reddit.com/r/MachineLearning/comments/1xx4ta3/we_made_a_multiplayer_game_where_each_players/) ⭐️ 8.0/10

A team has opened a free beta of a multiplayer game in which each player&\#x27;s view is generated locally by a world model running on their own GPU, rather than rendered by a central server. The model was trained on the team&\#x27;s open dataset of 10-player CS:GO bot matches, about 3,958 hours with all POVs and inputs aligned at 16 Hz, and released last month. A lightweight server keeps game state in sync while diffusion transformers draw each next frame from server state, player actions, and previous frames. The beta is explicitly limited to one small map and pistols only, with imperfect fine details, and requires an RTX 3080 or better, though an experimental Mac build exists; the team says it is not affiliated with Valve.

reddit · r/MachineLearning · /u/bengal7ion · Nov 15, 19:46

**「Background」** The project builds on a dataset the team released the previous month: roughly 3,958 hours of 10-player CS:GO bot matches with all player viewpoints and inputs aligned at 16 Hz. The team&\#x27;s site describes using CS:GO&\#x27;s built-in bots and GOTV recorder to capture every tick of every match, which it says makes automated data production possible without recruiting players or capturing screens. The new beta adds networked multiplayer on top of that data, with a lightweight server syncing game state while each player&\#x27;s GPU generates their own view.

**「Impact」** Players need an RTX 3080-class GPU to run the beta, since frame generation happens on their own hardware rather than the server, and the experimental Mac build is described as untested in scope. The released dataset and open beta give researchers a concrete testbed for real-time generative world models in a multiplayer setting, but the one-map, pistol-only scope means results should not be read as general gameplay capability.

<details><summary>References</summary>
<ul>
<li><a href="https://vor.tech/">VOR.TECH — open multiplayer gameplay data for world models</a></li>

</ul>
</details>

**Tags**: `#world models`, `#diffusion transformers`, `#generative games`, `#open datasets`, `#real-time inference`

---

<a id="item-tech-news-3"></a>
### [Meituan open-sources LongCat-2.5, claims Huawei Ascend-only training](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 8.0/10

Meituan&\#x27;s LongCat team published the weights for LongCat-2.5 a week after the model&\#x27;s official launch, releasing them under the MIT license for commercial use. The model is designed for agents that autonomously complete long, multi-step tasks, especially coding, and activates roughly 48 billion parameters per token while accepting text, image, and video input. The team claims training used only Chinese chips—Huawei Ascend accelerators—and no NVIDIA GPUs, a vendor claim not independently verified in the source. It reports a score of 88.4 on Terminal Bench v2.1, slightly below Claude Opus 5&\#x27;s 89.1.

telegram · zaihuapd · Nov 15, 11:08

**「Background」** LongCat-2.5 is a 1.6-trillion-parameter mixture-of-experts model that activates roughly 48 billion parameters per token, and its self-hosting guide covers Huawei Ascend hardware only; the sample deployment runs on 194 Ascend chips. Meituan&\#x27;s own benchmark figures place it near leading Western models on some coding tests and well behind on others, so the reported Terminal Bench score is a vendor claim rather than an independently measured result.

**「Impact」** Because the weights are MIT-licensed, developers can deploy and modify LongCat-2.5 commercially without the restrictions of more limited open licenses. The claimed Ascend-only training pipeline, if confirmed, would offer a concrete example of a large model trained outside NVIDIA&\#x27;s ecosystem, though the source provides no independent verification of the hardware claim or the benchmark result.

<details><summary>References</summary>
<ul>
<li><a href="https://pulse.adyog.com/insights/meituan-longcat-2-5-open-agent-model-huawei">Meituan LongCat-2.5: Open Agent Model, Huawei Ascend Guide</a></li>
<li><a href="https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/">Meituan releases a 1.6-trillion-parameter agent model that ...</a></li>
<li><a href="https://phemex.com/news/article/meituan-opensources-16tparameter-longcat25-model-trained-entirely-on-domestic-chinese-hardware-103629">Meituan LongCat-2.5: 1.6T MoE AI Model Trained on Huawei Chi ...</a></li>

</ul>
</details>

**Tags**: `#open-source AI`, `#LLM training`, `#Huawei Ascend`, `#agent models`, `#AI hardware`

---

<a id="item-tech-news-4"></a>
### [MacBook Pro OLED PWM Flicker Draws Technical Scrutiny](https://macanorak.com/the-macbook-pros-oled-pwm-problem-when-a-better-display-becomes-worse-to-use/) ⭐️ 7.0/10

A MacAnorak technical article examines how the MacBook Pro&\#x27;s OLED display uses pulse-width modulation \(PWM\) dimming, which can cause flicker sensitivity issues for some users. The piece reports a 240Hz PWM figure, but commenters dispute that measurement: one argues the tandem-OLED panels each pulse at 480Hz and run 180 degrees out of phase, producing an effective 960Hz across most usable brightness levels. The article is a technical analysis rather than an independently verified measurement, and the actual PWM frequency remains contested in the discussion.

hackernews · MacAnorak · Nov 15, 13:15 · [Discussion](https://news.ycombinator.com/item?id=50506719)

**「Background」** Earlier coverage reported that the new 14-inch MacBook Pro&\#x27;s PROLED XDR panel dims via 240 Hz PWM at any brightness of 99% or lower, with roughly 56% flicker depth, and that some early buyers reported eye strain and dizziness. For comparison, testing of the M4 Pro MacBook Pro&\#x27;s Mini-LED display recorded a modulation frequency of 14,880 Hz, about 62 times faster than the tandem OLED configuration.

**「Why It Matters」** For users sensitive to display flicker, the practical concern is whether the MacBook Pro&\#x27;s OLED dimming causes eye strain or discomfort at the brightness levels they actually use. The disagreement over the true frequency matters because a higher effective rate would make the display more tolerable than the 240Hz figure suggests, so readers should treat the reported number as unconfirmed until independent measurements settle it.

**「Community Reaction」** Commenters broadly welcomed attention to flicker sensitivity, with one noting that a concussion made all screens difficult to focus on, not just bright OLEDs, and another citing a Nature paper suggesting humans can perceive flicker above twice a display&\#x27;s refresh rate. Others raised related sensitivities such as white-LED color rendering \(CRI\) and LCD motion blur, and one commenter called for more research into how many people are affected by PWM.

<details><summary>References</summary>
<ul>
<li><a href="https://www.appleheadlines.com/macbook-pro-oled-eye-strain-pwm-flicker/">MacBook Pro OLED Eye Strain &amp; PWM Flicker: 7 Moves - AH</a></li>
<li><a href="https://macbreeze.com/proled-macbook-pro-pwm-dimming-eye-strain/">PROLED MacBook Pro Users Report Eye Strain Driven by Low ...</a></li>
<li><a href="https://techbytes.app/posts/the-macbook-pros-oled-pwm-problem-when-a-better-display/">The MacBook Pro&#x27;s OLED PWM Problem: When a &#x27;Better&#x27; Display ...</a></li>

</ul>
</details>

**Tags**: `#OLED displays`, `#PWM flicker`, `#hardware`, `#display technology`, `#accessibility`

---

<a id="item-tech-news-5"></a>
### [Protomaps Makes Self-Hosting Map Tiles Cheap and Easy](https://bruceroettgers.eu/blog/protomaps/) ⭐️ 7.0/10

A blog post and Hacker News discussion describe how Protomaps, built around the PMTiles format, makes self-hosting map tiles inexpensive and straightforward for developers. Commenters report using the approach for privacy, access control, and cost reasons, with one developer saying Protomaps made a location-based side project affordable where Mapbox or Google Maps would have been prohibitive. The discussion also notes limits: commenters say basemaps are small enough to host cheaply, but high-resolution satellite imagery grows large and expensive at higher zoom levels, with one developer stopping at z17 due to projected storage needs. No source content was supplied, so specific cost figures, versions, and measured results could not be verified.

hackernews · bcye · Nov 15, 19:26 · [Discussion](https://news.ycombinator.com/item?id=50509837)

**「Background」** Protomaps packages a customizable world map as a single static file that can be deployed on cloud storage, using the open PMTiles tile format. That design is what allows self-hosting without a dedicated tile server, which is the premise the blog post and discussion build on.

**「Impact」** Developers building location-based apps can now consider owning their map infrastructure rather than paying a hosted provider, with commenters citing privacy, access control, and reduced load on public infrastructure as reasons. Those needing satellite imagery should plan storage carefully, since commenters report global high-resolution coverage can reach hundreds of terabytes and become impractical to serve from object storage alone.

**「Community Discussion」** Commenters pointed to OpenFreeMap as a similar free, no-API-key alternative and described running PMTiles behind Cloudflare R2 to own their map infrastructure. One developer said Protomaps made a Wikipedia walking game affordable for a side project, while another cautioned that satellite mosaics become storage-heavy at high zoom levels.

<details><summary>References</summary>
<ul>
<li><a href="https://protomaps.com/">Protomaps - The open source map in a file</a></li>
<li><a href="https://github.com/Rezivure/Grid-Protomaps">Rezivure/Grid- Protomaps : The Protomaps &quot;serverless&quot; map tile ...</a></li>

</ul>
</details>

**Tags**: `#maps`, `#self-hosting`, `#open-source`, `#PMTiles`, `#geospatial`

---

<a id="item-tech-news-6"></a>
### [Congress Moves to Tighten AI Chip Export Rules After Nvidia Scandal](https://www.theverge.com/ai-artificial-intelligence/1033984/congress-export-rules-ai-chips-china) ⭐️ 7.0/10

Following a scandal involving now-former Nvidia CEO Jensen Huang and a suspected Chinese spy, Democrats and Republicans in Congress have voiced support for measures and bills that would tighten AI chip export rules. Senate Minority Leader Chuck Schumer said Huang and the Trump administration need to answer to Congress, and Senate Banking Committee Chairman Tim Scott sent letters calling on Huang and Commerce Secretary Howard Lutnick to publicly testify. The supplied report is truncated, so the specific bills, their provisions, and any vote or enactment status remain unverified.

rss · The Verge · Nov 15, 19:15

**「Background」** The push follows Jensen Huang&\#x27;s resignation as Nvidia CEO, which the company board announced after reports that his extramarital relationship involved a Chinese national suspected by U.S. intelligence of being recruited as a spy. The Verge&\#x27;s earlier reporting noted that Senate Minority Leader Chuck Schumer said Huang would still need to answer to Congress despite stepping down.

**「Impact」** Nvidia&\#x27;s pending export-license applications under the Commerce Department&\#x27;s January 2026 advanced-computing-chip rule could face added scrutiny if Congress tightens the regime, according to ZeroHedge&\#x27;s account of the oversight push. The source does not specify which bills or measures have been introduced, so the concrete scope of any new restrictions on Nvidia&\#x27;s China sales remains unverified.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Jensen_Huang_spying_scandal">Jensen Huang spying scandal - Wikipedia</a></li>
<li><a href="https://www.cbsnews.com/news/nvidia-ceo-jensen-huang-resigns/">Nvidia CEO Jensen Huang resigns in wake of affair with woman ...</a></li>
<li><a href="https://www.cbsnews.com/news/jensen-huang-nvidia-resignation-scandal-timeline/">Timeline of a scandal: How Jensen Huang&#x27;s abrupt resignation ...</a></li>
<li><a href="https://www.zerohedge.com/political/preserve-all-evidence-huang-out-nvidia-democrats-want-every-record-his-calls-trump">Preserve All Evidence: With Huang Out At Nvidia ... | ZeroHedge</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#export controls`, `#Nvidia`, `#technology policy`, `#semiconductors`

---

<a id="item-tech-news-7"></a>
### [FBI warns AI hacking framework ARTEX is automating cyberattacks](https://www.bleepingcomputer.com/news/security/fbi-warns-artex-ai-hacking-tool-is-powering-global-cyberattacks/) ⭐️ 7.0/10

The FBI is warning that hackers are using an AI-powered penetration testing framework called ARTEX to automate cyberattacks against organizations worldwide. The warning cites a recent ConnectWise supply-chain breach that compromised Microsoft 365 customer environments. The supplied excerpt provides no further technical details, such as affected versions, indicators of compromise, or remediation guidance.

rss · BleepingComputer · Nov 15, 18:29

**「Background」** ARTEX is described in reporting on the FBI flash alert as a penetration-testing platform that translates high-level tactical goals stated in words into machine commands executed by AI agents, with minimal human interaction beyond setting the initial objectives, and it can integrate any AI model, including frontier models \(tool-1-1\). Microsoft attributed the ConnectWise Cloud Backup supply-chain compromise to a China state-aligned actor tracked as Storm-0940, which used ARTEX, described as a Go-based agentic AI penetration-testing framework \(tool-1-3\).

<details><summary>References</summary>
<ul>
<li><a href="https://therecord.media/artex-ai-tool-fbi-flash-alert">FBI flash alert says Artex tool automating cyberattacks at ‘machine...</a></li>
<li><a href="https://thehackernews.com/2026/10/china-linked-hackers-use-artex-ai.html">China-Linked Hackers Use ARTEX AI Agents in ConnectWise Supply...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#AI`, `#supply-chain`, `#FBI`, `#hacking-tools`

---

<a id="item-tech-news-8"></a>
### [Tool claims ~5x faster pageable cudaMemcpy on B300](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 7.0/10

A Reddit user published an open-source tool, cudamemcpy-tuner, and an accompanying blog post claiming to speed up pageable cudaMemcpy host-to-device transfers roughly 5x on an Nvidia B300 GPU. The post&\#x27;s benchmark copies a 1 GB uint8 tensor to the GPU five times and reports 10.2 GB/s without the tool versus 51.5 GB/s when the benchmark is run through \`cmt tune\`. The claim rests on this single benchmark snippet from the author, not on independent measurement, and applies specifically to pageable transfers rather than all cudaMemcpy paths.

reddit · r/MachineLearning · /u/makneeee · Nov 15, 18:20

**「Why pageable transfers are slow」** CUDA distinguishes pageable host memory, which the OS can swap out, from pinned \(page-locked\) memory, which stays resident and can be used for direct DMA transfers; NVIDIA&\#x27;s own guidance notes that pinned transfers use the same cudaMemcpy\(\) syntax but generally achieve higher bandwidth. Pinned memory is also required to overlap copy and compute, and it can help when transfer buffers are reused. The tool here targets the pageable path, which is the default for ordinary host allocations such as a PyTorch CPU tensor.

**「Impact」** If the result holds, developers moving large tensors from pageable host memory to a B300 could see substantially higher effective bandwidth without changing their copy calls, since the tool is invoked as a wrapper around the existing benchmark command. The evidence covers only one GPU model and one transfer size and direction, so users should reproduce the benchmark on their own hardware before relying on the speedup.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/how-optimize-data-transfers-cuda-cc/">How to Optimize Data Transfers in CUDA C/C++ | NVIDIA Technical...</a></li>
<li><a href="https://stackoverflow.com/questions/50184146/cuda-pinned-memory-vs-pageable-memory-tradeoffs">optimization - CUDA - Pinned Memory vs. Pageable Memory ...</a></li>
<li><a href="https://www.linkedin.com/pulse/supercharging-data-transfers-cuda-power-page-locked-pinned-mohapatra-bejec">Supercharging Data Transfers in CUDA: The Power of Page-Locked...</a></li>

</ul>
</details>

**Tags**: `#cuda`, `#gpu-memory`, `#performance-optimization`, `#machine-learning-systems`, `#open-source-tools`

---

## Financial News

<a id="item-finance-news-1"></a>
### [US, China, Russia Leaders to Hold First Trilateral Meeting at Shenzhen APEC](https://apnews.com/article/trump-xi-putin-summit-china-5fe92253ef38100bae913834a9b74d72) ⭐️ 9.0/10

China&\#x27;s foreign ministry said the leaders of the US, China, and Russia will hold their first dedicated trilateral meeting on November 19, on the sidelines of the APEC summit in Shenzhen and outside its formal agenda, according to AP. Media reports describe it as the first meeting held specifically among the three leaders.

telegram · zaihuapd · Nov 16, 01:38

**「Background」** The 2026 APEC summit is being held in Shenzhen on November 18–19, China&\#x27;s first time hosting since 2014, and the trilateral meeting is planned on its sidelines rather than as part of the formal agenda. Media reports describe the three-way meeting as the first of its kind.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/2026%E5%B9%B4%E4%B8%AD%E5%9B%BDAPEC%E5%B3%B0%E4%BC%9A">2026年中国APEC峰会 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.gessymorgan.com/apec-2026-china/">APEC 2026 China: Shenzhen Summit Dates and Agenda</a></li>
<li><a href="https://www.scmp.com/topics/2026-xi-trump-putin-trilateral-meeting">2026 Xi-Trump-Putin trilateral meeting: Latest News and ...</a></li>

</ul>
</details>

**Tags**: `#geopolitics`, `#APEC`, `#US-China-Russia`, `#diplomacy`, `#trade policy`

---

<a id="item-finance-news-2"></a>
### [US Judge Allows DRAM Price-Fixing Lawsuit Against Micron, Samsung and SK Hynix to Proceed](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 7.0/10

A US federal judge, Noël Wise, rejected motions by Micron, Samsung and SK Hynix to dismiss a class-action lawsuit accusing them of fixing DRAM prices, finding the plaintiffs&\#x27; evidence of coordinated supply cuts plausible. The plaintiffs — 17 individuals and small businesses — allege the three companies made four parallel moves to restrict DRAM supply within a year, with prices rising by as much as 500%.

telegram · zaihuapd · Nov 15, 16:39

**「Background」** The ruling came in a proposed class action by 17 individuals and small businesses in the Northern District of California, who allege the three chipmakers made four parallel moves to restrict DRAM supply within a year, pushing prices up by as much as 500%. The companies had argued their close watching of one another reflects tight competition, but Judge Noël Wise found the alleged conduct goes beyond that.

**「Impact」** The ruling keeps the class action alive, so the three chipmakers face continued litigation exposure on behalf of the 17 individual and small-business plaintiffs; it is a procedural decision, not a finding of liability.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge">Judge denies motion to dismiss DRAM price - fixing lawsuit against...</a></li>
<li><a href="https://www.techpowerup.com/354863/samsung-sk-hynix-and-micron-fail-to-get-dram-antitrust-suit-dismissed">Samsung , SK hynix , and Micron Fail to Get DRAM Antitrust Suit ...</a></li>
<li><a href="https://litnews.ai/articles/garciaguirre-samsung-sk-hynix-micron-dram-conspiracy-suit-survives-dismissal">Judge Refuses to Dismiss DRAM Supply Conspiracy Suit Against...</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge">Judge denies motion to dismiss DRAM price -fixing... | Tom&#x27;s Hardware</a></li>

</ul>
</details>

**Tags**: `#DRAM`, `#price-fixing litigation`, `#semiconductors`, `#Micron`, `#Samsung/SK Hynix`

---