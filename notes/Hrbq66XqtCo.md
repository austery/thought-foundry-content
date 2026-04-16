---
author: Dwarkesh Patel
date: '2026-04-15'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=Hrbq66XqtCo
speaker: Dwarkesh Patel
tags:
  - accelerated-computing
  - token-economics
  - supply-chain-strategy
  - software-ecosystem
  - geopolitical-tech-competition
title: 对话黄仁勋：英伟达的护城河、对华政策与加速计算的终极使命
summary: 英伟达 CEO 黄仁勋在访谈中深度解析了公司的核心竞争力和 AI 产业的未来。他提出英伟达的本质是将“电子转化为 Token”，并通过软硬协同设计实现超越摩尔定律的性能飞跃。访谈重点探讨了供应链垂直整合、CUDA 生态的不可替代性、对华芯片出口限制的利弊权衡，以及能源政策对再工业化的深远影响。
insight: ''
draft: true
series: ''
category: ai-ml
area: tech-engineering
project: []
people: []
companies_orgs:
  - Nvidia
  - TSMC
  - OpenAI
  - Anthropic
  - Google
  - Huawei
  - Broadcom
products_models:
  - CUDA
  - Blackwell
  - Hopper
  - Vera Rubin
  - TPU
  - NVLink
media_books: []
status: evergreen
---
### 软件商品化与英伟达

**Dwarkesh Patel**: 我们看到许多软件公司的估值暴跌，因为人们预期 AI 会使软件商品化。有一种潜在的幼稚想法：英伟达将 GDS2 文件发送给 **TSMC**（台积电），台积电制造逻辑芯片和开关，然后与 **SK Hynix**、**Micron**（美光）和 **Samsung**（三星）生产的 **HBM** 封装在一起。接着发往台湾的 ODM 组装成机架。英伟达本质上是在开发由他人制造的软件。如果软件被商品化，英伟达也会被商品化吗？

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: We've seen the valuations of a bunch of software companies crash because people are expecting AI to commoditize software. There's a potentially naive way of thinking about things, which is: look, Nvidia sends a GDS2 file to TSMC. TSMC builds the logic dies, it builds the switches, then it packages them with the HBM that SK Hynix, Micron, and Samsung make. Then it sends it to an ODM in Taiwan where they assemble the racks. Nvidia is fundamentally making software that other people are manufacturing, and if software gets commoditized, does Nvidia get commoditized? 

</details>

**Jensen Huang**: 归根结底，必须有东西将**电子转化为 Token**。这种“从电子到 Token”的转化，并随着时间的推移使这些 Token 变得更有价值，是很难被完全商品化的。从电子到 Token 的旅程是如此不可思议。制造那个 Token 就像制造一个比另一个更有价值的分子。为了使那个 Token 具有价值，其中投入了大量的艺术、工程、科学和发明，显然我们正在实时见证这一切。这种转换、制造以及其中涉及的所有科学远未被深刻理解，这段旅程也远未结束。我怀疑这（商品化）会发生。当然，我们会让它变得更高效。

<details>
<summary>Original English</summary>

**Jensen Huang**: In the end, something has to transform electrons to tokens. The transformation of electrons to tokens and making those tokens more valuable over time is hard to completely commoditize. The transformation from electrons to tokens is such an incredible journey. Making that token is like making one molecule more valuable than another molecule, making one token more valuable than another. The amount of artistry, engineering, science, and invention that goes into making that token valuable, obviously we're watching it happen in real time. The transformation, the manufacturing, all of the science that goes in there is far from deeply understood and the journey is far from over. I doubt that it will happen. We're going to make it more efficient, of course. 

</details>

### 五层蛋糕与生态系统

**Jensen Huang**: 你提问的方式正是我对公司的思维模型：输入是电子，输出是 Token。中间是 **Nvidia**。我们的工作是尽一切必要努力，同时尽可能少地干预，以实现这种具有惊人能力的转换。我所说的“尽可能少”，是指任何我不需要做的事情，我都会与他人合作，使其成为我生态系统的一部分。如果你看今天的英伟达，我们可能拥有最大的合作伙伴生态系统，包括上游和下游供应链、所有的计算机公司、应用程序开发者和模型制造者。如果愿意的话，你可以把 AI 看作一个**五层蛋糕**，我们在所有五个层级都有生态系统。我们尽量做得少，但事实证明，我们必须做的那部分难得离谱。我不认为那会被商品化。

<details>
<summary>Original English</summary>

**Jensen Huang**: The way that you framed the question is my mental model of our company. The input is electrons, the output is tokens. In the middle is Nvidia. Our job is to do as much as necessary and as little as possible to enable that transformation to be done at incredible capabilities. What I mean by "as little as possible," whatever I don't need to do, I partner with somebody and make it part of my ecosystem. If you look at Nvidia today, we probably have the largest ecosystem of partners, both in the supply chain upstream and downstream, all of the computer companies, application developers, and model makers. AI is a five-layer cake, if you will. We have ecosystems across the entire five layers. We try to do as little as possible, but the part that we have to do, as it turns out, is insanely hard. I don't think that gets commoditized. 

</details>

### 代理人与工具软件

**Jensen Huang**: 事实上，我也不认为企业软件公司、工具制造商会消失。今天大多数软件公司都是工具制造商。有些是工作流规范化系统，但对很多公司来说，他们是工具商。例如，**Excel** 是工具，**PowerPoint** 是工具，**Cadence** 和 **Synopsys** 制造工具。我看到的与人们看到的截然相反。我认为 **Agent**（代理人）的数量将呈指数级增长，工具使用者的数量也将呈指数级增长。所有这些工具的实例（Instance）极有可能激增。

<details>
<summary>Original English</summary>

**Jensen Huang**: In fact, I also don't think the enterprise software companies, the tools makers… Most software companies today are tool makers. Some of them are not. Some of them are workflow codification systems. But for a lot of companies, they're tool makers. For example, Excel is a tool, PowerPoint is a tool, Cadence makes tools, Synopsys makes tools. I actually see the opposite of what people see. I think the number of agents is going to grow exponentially, and the number of tool users is going to grow exponentially. It's very likely that the number of instances of all these tools is going to skyrocket. 

</details>

**Jensen Huang**: **Synopsys Design Compiler** 的实例数量极有可能激增，伴随着大量使用布局规划工具、布线工具和设计规则检查器的 Agent。今天，我们受限于工程师的数量。明天，这些工程师将得到一堆 Agent 的支持。我们将以前所未有的方式探索设计空间，并使用我们今天使用的工具。我认为工具的使用将导致软件公司业绩飙升。目前还没发生的原因是 Agent 使用工具的能力还不够好。要么这些公司自己构建 Agent，要么 Agent 变得足够聪明能使用那些工具。我认为这将是两者的结合。

<details>
<summary>Original English</summary>

**Jensen Huang**: It’s very likely that the number of instances of Synopsys Design Compiler is going to skyrocket, along with the number of agents using the floor planners, our layout tools, and our design rule checkers. Today we're limited by the number of engineers. Tomorrow, those engineers are going to be supported by a bunch of agents. We're going to be exploring the design space like you've never seen before, and we're going to use the tools that we use today. I think tool use is going to cause the software companies to skyrocket. The reason why it hasn't happened yet is because the agents aren't good enough at using their tools yet. Either these companies are going to build the agents themselves, or agents are going to get good enough to be able to use those tools. I think it's going to be a combination of both. 

</details>

### 锁定稀缺资源的护城河

**Dwarkesh Patel**: 我认为在你最新的财报中，你与代工厂、内存和封装商有近 1000 亿美元的采购承诺。**SemiAnalysis** 报告称，你将有 2500 亿美元的此类采购承诺。一种解释是，英伟达的护城河实际上在于你锁定了未来多年这些稀缺组件的供应。别人可能有加速器，但他们能买到内存来制造它吗？他们能买到逻辑芯片来制造它吗？这真的是英伟达未来几年的大护城河吗？

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: I think in your latest filings, you had almost a $100 billion in purchase commitments with foundries, memory, and packaging. SemiAnalysis has reported that you will have $250 billion of these kinds of purchase commitments. One interpretation is that Nvidia's moat is really that you've locked up many years of these scarce components. Somebody else might have an accelerator, but can they actually get the memory to build it? Can they actually get the logic to build it? Is this really Nvidia's big moat for the next few years? 

</details>

**Jensen Huang**: 这是我们能做到而别人很难做到的事情之一。我们在上游做了巨大的承诺。有些是明确的，比如你提到的这些承诺。有些是隐含的。例如，上游的很多投资是由我们的供应链完成的，因为我对他们的 CEO 说：“让我告诉你这个行业将会有多大，让我向你解释原因，让我和你一起推导，让我向你展示我所看到的。”通过这种通知、激励和与各行业上游 CEO 达成共识的过程，他们愿意进行投资。为什么他们愿意为我投资而不是别人？原因在于他们知道我有能力购买他们的供应，并通过我的下游卖出去。

<details>
<summary>Original English</summary>

**Jensen Huang**: It's one of the things that we can do that is hard for someone else to do. We've made enormous commitments upstream. Some of it is explicit, these commitments that you mentioned. Some of it is implicit. For example, a lot of the investments that are upstream are made by our supply chain because I said to the CEOs, "Let me tell you how big this industry is going to be, let me explain to you why, let me reason through it with you, and let me show you what I see." As a result of that process of informing, inspiring, and aligning with CEOs of all different industries upstream, they're willing to make the investments. Why are they willing to make the investments for me and not someone else? The reason for that is because they know that I have the capacity to buy their supply and sell it through my downstream. 

</details>

**Jensen Huang**: 事实是，英伟达的下游供应链和我们的下游需求如此巨大，以至于他们愿意在上游进行投资。在 **GTC** 大会上，人们对它的规模和参会人员感到惊叹。那是全方位的 360 度，整个 AI 宇宙都聚集在一个地方。他们聚在一起是因为他们需要见到彼此。我把他们聚集在一起，是为了让下游能看到上游，上游能看到下游，所有人都能看到 AI 的进展。非常重要的是，他们都能见到 AI 原住民、所有正在建立的 AI 初创公司，亲眼看到我告诉他们的一切。我花了很多时间直接或间接地告知我们的供应链、合作伙伴和生态系统，关于我们面前的机遇。

<details>
<summary>Original English</summary>

**Jensen Huang**: The fact is that Nvidia's downstream supply chain and our downstream demand is so large, they're willing to make the investment upstream. If you look at GTC, people are marveled by the scale of it and the people that go. It's a full 360 degrees, the entire universe of AI all in one place. They're all in one place because they need to see each other. I bring them together so that the downstream can see the upstream, the upstream can see the downstream, and all of them can see the advances in AI. Very importantly, they can all meet the AI natives, all the AI startups being built, and all the amazing things happening so they can see firsthand all the things that I tell them. I spend a lot of my time informing, directly or indirectly, our supply chain, partners, and ecosystem about the opportunity in front of us. 

</details>

### 上游供应链能否跟上？

**Dwarkesh Patel**: 有人开玩笑说，黄仁勋的大多数演讲都是一个接一个的公告。但你的演讲总有一部分有点“折磨人”，感觉像是在上课。

**Jensen Huang**: 事实上，这正是我所想的。我需要确保整个供应链（上游和下游）以及生态系统都理解正在发生什么、为什么发生、何时发生、规模会有多大，并能够像我一样系统地进行推导。关于你描述的护城河，我们有能力为未来进行建设。如果未来几年的规模是一万亿美元，我们有供应链来实现它。如果没有我们的触达能力和业务速度……就像有现金流一样，也有供应链流，还有周转。如果业务周转率低，没有人会为一种架构建立供应链。我们维持规模的能力仅是因为我们的下游需求如此巨大。他们看到了，听到了，看到这一切都在到来。

<details>
<summary>Original English</summary>

**Jensen Huang**: Some people always say, "Jensen, in most keynotes, it's one announcement after another." With our keynotes, there’s always a part of it that's a little torturous in the sense that it almost comes across like education. In fact, that's exactly on my mind. I need to make sure the entire supply chain, upstream and downstream, the ecosystem, understands what is coming at us, why it's coming, when it's coming, how big it's going to be, and is able to reason about it systematically, just like I reason about it. Regarding the moat as you describe it, we're able to build for a future. If our next several years are a trillion dollars in scale, we have the supply chain to do it. Without our reach, the velocity of our business… Just as there's cash flow, there's supply chain flow, there's churns. Nobody is going to build a supply chain for an architecture if the business churns are low. Our ability to sustain the scale is only because our downstream demand is so great. And they see it, they hear about it, they see it all coming. That allows us to do the things we're able to do at the scale we do them. 

</details>

**Dwarkesh Patel**: 我想更具体地了解上游是否能跟上。多年来，你们的收入每年翻倍。你们提供给世界的 **FLOPs** 每年增长两倍多。在这种规模下每年翻倍真的很不可思议。但看看逻辑芯片。你是台积电 **N3** 节点最大的客户，也是 **N2** 最大的客户之一。根据 SemiAnalysis 的数据，今年 AI 整体将占 N3 的 60%，明年将占 86%。如果你已经是大头了，你怎么翻倍？每年都翻倍？我们现在是否处于 AI 计算增长率必须因上游原因而放缓的状态？

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: I do want to understand more concretely whether the upstream can keep up. For many years now, you guys have been 2x-ing revenue year over year. You've been more than tripling the amount of flops you're providing to the world year over year. And 2x-ing at this scale now is really incredible. Exactly. But then you look at logic. You're the biggest customer on TSMC's N3 node, and you're one of the biggest on N2. AI as a whole this year is going to be sixty percent of N3. It's going to be 86% next year, according to SemiAnalysis. How do you double if you're the majority? And how do you do that year over year? Are we in a regime now where the growth rate in AI compute has to slow because of upstream? 

</details>

### 制造瓶颈：管道工与 EUV

**Jensen Huang**: 在某种程度上，瞬时需求大于全球上游和下游的供应。在任何时刻，我们都可能受限于**管道工**的数量，这确实发生过。顺便说一下，明年的 GTC 我会邀请管道工们参加。这是一个很好的状态。你希望身处一个瞬时需求大于行业总供应的行业。反之显然不妙。如果一个特定组件差得太远，整个行业都会蜂拥而至解决它。例如，注意到人们不再怎么谈论 **CoWoS** 了吗？原因是在两年的时间里，我们全力以赴地解决了它。我们实现了翻倍、再翻倍、连着翻了好几次。

<details>
<summary>Original English</summary>

**Jensen Huang**: At some level, the instantaneous demand is greater than the supply upstream and downstream in the world. At any instant, we could be limited by the number of plumbers, which actually happens. The plumbers are invited to next year's GTC. By the way, great idea. But that's a good condition. You want an industry where the instantaneous demand is greater than the total supply of the industry. The opposite is obviously less good. If we're too far apart, if one particular component is too far away, the industry swarms it. For example, notice people aren't talking very much about CoWoS anymore. The reason for that is because for two years we swarmed the living daylights out of it. We doubled, doubled, doubled on several doubles. 

</details>

**Jensen Huang**: 现在我认为我们的状况相当好。台积电现在知道 CoWoS 供应必须跟上逻辑芯片和内存的需求。他们正在像扩展逻辑芯片一样扩展 CoWoS 和未来的封装技术。这太棒了，因为长期以来，CoWoS 和 HBM 内存相当小众。但现在它们不再是小众了。人们意识到它们是主流计算技术。现在我们能够更大范围地影响我们的供应链。在 AI 革命开始时，我现在说的一切，五年前我就说过了。

<details>
<summary>Original English</summary>

**Jensen Huang**: Now I think we're in fairly good shape. TSMC now knows that CoWoS supply has to keep up with the rest of the logic demand and the memory demand. They're scaling CoWoS and future packaging technologies at the same level as they scale logic. This is terrific, because for a long time, CoWoS and HBM memory were rather specialty. But they're not specialties anymore. People now realize they're mainstream computing technology. Of course, we're now much more able to influence a larger scope of our supply chain. At the beginning of the AI revolution, all the things that I say now, I was saying five years ago. 

</details>

**Jensen Huang**: 有些人相信了并进行了投资，例如 Sanjay 和 Micron 团队。我依然清楚记得那场会议，我明确说明了将会发生什么，为什么会发生。他们真的加倍下注了。我们在 **LPDDR** 和 **HBM** 内存上与他们合作，他们投入巨资。这显然对公司来说是巨大的成就。有些人来得晚一点，但现在他们都来了。每一个瓶颈都会得到极大关注。现在我们提前数年预判瓶颈。例如，我们过去几年对 **Lumentum**、**Coherent** 以及**硅光子**生态系统的投资真正重塑了供应链。我们围绕台积电建立了一整套供应链。我们与他们合作开发了 **COUPE**，发明了一堆技术，并将这些专利许可给供应链，以保持开放性。我们正在通过发明新技术、新流程、新测试设备（如双面探测）来准备供应链。

<details>
<summary>Original English</summary>

**Jensen Huang**: Some people believed in it and invested in it, for example, Sanjay and the Micron team. I still remember the meeting really well where I was clear about exactly what was going to happen, why it was going to happen, and the predictions of today. They really doubled down on it. We partnered with them across LPDDR and HBM memories, and they really invested in it. It obviously has been tremendous for the company. Some people came a little bit later, but now they're all here. Each one of these bottlenecks gets a great deal of attention. Now we're prefetching the bottlenecks years in advance. For example, the investments that we've done with Lumentum, Coherent, and the silicon photonics ecosystem over the last several years really reshaped the supply chain. We built up an entire supply chain around TSMC. We partnered with them on COUPE, invented a whole bunch of technology, and licensed those patents to the supply chain to keep it nice and open. We're preparing the supply chain through the invention of new technologies, new workflows, new testing equipment like double-sided probing, investing in companies, and helping them scale up their capacity. 

</details>

**Dwarkesh Patel**: 最终，内存和逻辑芯片都受限于 **EUV** 光刻机。你如何让 EUV 机器的数量每年翻倍？

**Jensen Huang**: 这一切都不是不可能快速扩展的。在两三年内都很容易做到。你只需要一个需求信号。一旦你能制造出一台，你就能制造出十台；一旦你能制造出十台，你就能制造出一百万台。这些东西并不难复制。有些我必须直接联系，有些是间接联系……如果我能说服台积电，**ASML**（阿斯麦）就会被说服。我们需要思考关键的卡点。但如果台积电被说服了，几年后你就会有充足的 EUV 机器。我的观点是，没有任何瓶颈会持续超过两三年，一个都没有。

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: Ultimately, memory and logic are bottlenecked by EUV. How do you get to 2x as many EUV machines year over year? 

**Jensen Huang**: None of that is impossible to scale quickly. All of that is easy to do within two or three years. You just need a demand signal. Once you can build one, you can build ten, and once you can build ten, you can build a million. These things are not hard to replicate. Some of them I have to directly, some of them indirectly, and some of them… If I can convince TSMC, ASML will be convinced. We have to think about the critical pinch points. But if TSMC is convinced, you'll have plenty of EUV machines in a few years. My point is that none of the bottlenecks last longer than a couple of years, two, three years, none of them. 

</details>

### 能源：真正的挑战

**Jensen Huang**: 与此同时，我们将计算效率提高了 10 到 20 倍，从 **Hopper** 到 **Blackwell**，提高了 30 到 50 倍。我们不断提出新算法，因为 **CUDA** 非常灵活。我们正在开发各种新技术，以便在增加产能的同时驱动效率。这些事情都不让我担心。让我担心的是我们的下游。防止能源流动的**能源政策**……没有能源你就无法创造一个行业。没有能源你就无法创造一个全新的制造业。我们想让美国重新工业化，带回芯片制造、计算机制造和封装，建造像电动汽车和机器人这样的新事物，建造 AI 工厂。没有能源，你无法建造任何这些东西，而这些东西需要很长时间。芯片产能、CoWoS 产能，那是 2 到 3 年的问题。能源问题则更长。

<details>
<summary>Original English</summary>

**Jensen Huang**: Meanwhile, we're improving computing efficiency by 10x 20x, and in the case of Hopper to Blackwell, 30x to 50x. We're coming up with new algorithms because CUDA is so flexible. We're developing all kinds of new techniques so that we drive efficiency in addition to increasing capacity. None of those things worry me. It's the stuff that's downstream from us. Energy policies that prevent energy from… You can't create an industry without energy. You can't create a whole new manufacturing industry without energy. We want to reindustrialize the United States. We want to bring back chip manufacturing, computer manufacturing, and packaging. We want to build new things like EVs and robots. We want to build AI factories. You can't build any of these things without energy, and those things take a long time. More chip capacity, that's a 2-3 year problem. More CoWoS capacity, 2-3 year problem. 

</details>

### 加速计算 vs TPU

**Dwarkesh Patel**: 谈谈你的竞争对手。看看 **TPU**，可以说世界上前三大模型中的两个（**Claude** 和 **Gemini**）都是在 TPU 上训练的。这对英伟达的未来意味着什么？

**Jensen Huang**: 我们构建的是非常不同的东西。英伟达构建的是**加速计算**（Accelerated Computing），而不是张量处理单元（TPU）。加速计算用于各种领域：分子动力学、量子色动力学、数据处理、结构化和非结构化数据。它还用于流体力学和粒子物理。此外，我们将其用于 AI。加速计算要多样化得多。虽然 AI 是当今的话题，且极具影响力，但计算的范畴要广得多。

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: True. I want to ask about your competitors. If you look at the TPU, arguably two out of the top three models in the world, Claude and Gemini, were trained on TPU. What does that mean for Nvidia going forward? 

**Jensen Huang**: We build a very different thing. What Nvidia built is accelerated computing, not a tensor processing unit. Accelerated computing is used for all kinds of things: molecular dynamics, quantum chromodynamics, data processing, data frames, structured data, and unstructured data. It's also used for fluid dynamics and particle physics. In addition, we use it for AI. Accelerated computing is much more diverse. Although AI is the conversation today and is obviously very important and impactful, computing is much broader than that. 

</details>

**Jensen Huang**: 英伟达重新发明了计算方式，从通用计算转向加速计算。我们的市场覆盖范围远超任何 TPU 或 ASIC 所能达到的程度。我们是唯一一家加速各种应用程序的公司。我们拥有巨大的生态系统。由于我们的计算机是为他人操作而设计的，任何运营商都可以购买我们的系统。对于大多数自建系统，你必须成为自己的运营商，因为它们的设计灵活性不足以供他人操作。因为任何人都可以操作我们的系统，所以我们存在于每一个云平台中，包括 **Google**、**Amazon**、**Azure** 和 **OCI**。如果你想购买并运行自己的超级计算机，比如在 **Eli Lilly** 进行药物发现研究，我们可以帮助他们操作自己的超算。英伟达将 CUDA 打造为一个极好的张量处理单元，但它也处理数据处理、计算、AI 等每一个生命周期。

<details>
<summary>Original English</summary>

**Jensen Huang**: Nvidia has reinvented the way computing is done, moving from general-purpose computing to accelerated computing. Our market reach is far greater than any TPU or ASIC can possibly have. If you look at our position, we're the only company that accelerates applications of all kinds. We have a gigantic ecosystem. So all kinds of frameworks and algorithms run on Nvidia. Because our computers are designed to be operated by other people, anyone who's an operator can buy our systems. With most of these home-built systems, you have to be your own operator because they were never designed to be flexible enough for others to operate. Because anybody can operate our systems, we're in every cloud, including Google, Amazon, Azure, and OCI. If you want to operate it to rent, you better have a large ecosystem of customers in many industries to be the offtakers. If you want to operate it for yourself, we obviously have the ability to help you operate it yourself, like we did for Elon with xAI. And because we can enable operators in any company and any industry, you could use it to build a supercomputer for scientific research and drug discovery at Lilly. We can help them operate their own supercomputer and use it for the entire diversity of drug discovery and biological sciences that we accelerate. There are just a whole bunch of applications that we can address that you can't do with TPUs. Nvidia built CUDA to be a fantastic tensor processing unit as well, but it also handles every life cycle of data processing, computing, AI, and so on. Our market opportunity is just a lot larger, and our reach is a lot greater. 

</details>

### 编程灵活性与摩尔定律

**Dwarkesh Patel**: AI 难道不就是重复不断的、非常可预测的矩阵乘法吗？TPU 难道不正是针对目前这一大波收入增长和计算用例而优化的吗？

**Jensen Huang**: 矩阵乘法是 AI 的重要部分，但不是全部。如果你想提出一种新的注意力机制，以不同的方式解聚，或者发明一种全新的架构——比如混合 **SSM**——你需要一个通用的可编程架构。如果你想创建一个融合了**扩散模型**（Diffusion）和自回归技术的模型，你需要这种架构。我们的优势在于它允许更容易地发明新算法，这是 AI 快速进步的真正动力。TPU 像其他任何事物一样，受限于**摩尔定律**，我们知道它每年增长约 25%。实现 10 倍或 100 倍飞跃的唯一方法是每年从根本上改变算法及其计算方式。这就是英伟达的核心优势。Blackwell 能够比 Hopper 提升 50 倍，你不可能仅靠摩尔定律做到这一点。我们解决问题的方法是使用新模型，比如 **MoE**（专家混合模型），它们在计算系统中被并行化、解聚和分布式。如果不具备通过 CUDA 深入底层并开发新内核的能力，这很难实现。

<details>
<summary>Original English</summary>

**Jensen Huang**: Matrix multiplies are an important part of AI, but they're not the only part. If you want to come up with a new attention mechanism, disaggregate in a different way, or invent a whole new type of architecture altogether—like a hybrid SSM—you want an architecture that's generally programmable. If you want to create a model that fuses diffusion and autoregressive techniques, you want an architecture that’s just generally programmable. We run everything you can imagine. That's the advantage. It allows for the invention of new algorithms a lot more easily, because it's a programmable system. The ability to invent new algorithms is really what makes AI advance so quickly. TPUs, like anything else, are impacted by Moore's Law, which we know is increasing by about 25% per year. The only way to really get 10x or 100x leaps is to fundamentally change the algorithm and how it's computed every single year. That's Nvidia's fundamental advantage. The only reason we were able to make Blackwell to Hopper 50x… When I first announced Blackwell was going to be 35x more energy efficient than Hopper, nobody believed it. Then Dylan wrote an article saying I sandbagged, and it's actually fifty times. You can't reasonably do that with just Moore's Law. The way we solve that problem is with new models, like MoEs, that are parallelized, disaggregated, and distributed across a computing system. Without the ability to really get down and come up with new kernels with CUDA, it's really hard to do. 

</details>

### CUDA 护城河：安装基数与 TCO

**Dwarkesh Patel**: 你的客户（超大规模云商）有资源编写自己的内核。像 **Anthropic** 和 **Google** 都在运行自己的加速器。如果你的大多数客户都能编写自己的内核并替换 CUDA，那么 CUDA 还是让英伟达引领前沿 AI 的关键吗？

**Jensen Huang**: CUDA 是一个丰富的生态系统。如果你想先在任何计算机上构建，先基于 CUDA 是非常明智的。首先，如果你是开发任何东西的开发者，你最想要的是**安装基数**（Install Base）。你希望你写的软件能运行在大量其他计算机上。英伟达的 CUDA 生态系统终究是它的宝藏。我们现在有数亿个 GPU，每个云平台都有。无论你是一家机器人公司，还是在本地运行，CUDA 随处可见。这种通用性是不可估量的。

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: If most of your customers can and do make replacements for CUDA, to what extent is CUDA really the thing that is going to make frontier AI happen on Nvidia? 

**Jensen Huang**: CUDA is a rich ecosystem. If you want to build on any computer first, building on CUDA first is incredibly smart. Because the ecosystem is so rich, we support every framework. The second thing is, if you're a developer building anything at all, the single most important thing you want is an install base. You want the software you write to run on a whole bunch of other computers. Nvidia's CUDA ecosystem is ultimately its great treasure. We have several hundred million GPUs out there now. Every cloud has it. If you're a robotics company, you want that CUDA stack to actually run in the robot itself. We're literally everywhere. The install base means that once you develop the software or the model, it's going to be useful everywhere. That is just incredibly valuable. 

</details>

**Jensen Huang**: 其次，没有人比我们更了解我们的架构。这些架构不像 CPU 那样通用。CPU 像凯迪拉克，巡航很稳，但不会太快。但英伟达的 GPU、加速器就像 **F1 赛车**。每个人都能以 100 英里的时速驾驶它，但将其推向极限需要相当多的专业知识。我们的专业知识能轻松帮助我们的 AI 实验室合作伙伴在他们的堆栈上再获得 2 倍的性能。英伟达的计算堆栈是世界上 **TCO**（总拥有成本）表现最好的，没有之一。没有人能向我证明今天世界上有任何平台的性能 TCO 比率更好。无论是 TPU 还是 Trainium，他们都不敢在 **InferenceMAX** 这种基准测试上露面。我欢迎他们来展示他们宣称的那 40% 优势。

<details>
<summary>Original English</summary>

**Jensen Huang**: The second thing is, nobody knows our architecture better than we do. These architectures are not as general purpose as a CPU. A CPU is kind of like a Cadillac. It's a nice cruiser. It never goes too fast. Everybody drives it pretty well. It's got cruise control, and everything's easy. But in a lot of ways, Nvidia's GPUs, accelerators, are like F1 racers. I could imagine everybody's able to drive it at a hundred miles an hour, but it takes quite a bit of expertise to be able to push it to the limit. Our expertise helps our AI lab partners to get another 2x out of their stack easily oftentimes. It's not unusual that by the time we're done optimizing their stack or optimizing a particular kernel, their model sped up by 3x, 2x, 50%. Nvidia's computing stack is the best performance per TCO in the world, bar none. Nobody can demonstrate to me that any single platform in the world today has a better performance-TCO ratio. Not one company. In fact, the benchmarks that are out there. Dylan's InferenceMAX is sitting out there for everybody to use, and not one… TPU won't come, Trainium won't come. I would welcome Trainium to demonstrate their 40% that they claim all the time. 

</details>

### 飞轮效应与能源效率

**Jensen Huang**: 这个飞轮实际上是：安装基数、架构的可编程性、生态系统的丰富性。如果你是一家 AI 初创公司，你会选择最丰富的架构。我们的**每瓦性能**也是全球最高的。如果合作伙伴建造了一个 1 吉瓦的数据中心，他们希望能产生尽可能多的 Token，最大化收入。我们是全球每瓦 Token 产出最高的架构。

<details>
<summary>Original English</summary>

**Jensen Huang**: So I think the flywheel is really install base, the programmability of our architecture, the richness of our ecosystem, and the fact that there's so many AI companies in the world. There's tens of thousands of them now. If you were one of those AI startups, what architecture would you choose? You would choose an architecture that's most abundant. We're the most abundant in the world. Second, our perf per watt is the highest in the world. So if one of these companies, if our partners, built a one gigawatt data center, that one gigawatt data center better deliver the maximum amount of revenues and number of tokens, which directly translates to revenues. You want it to generate as many tokens as possible, maximize the revenues for that data center. We are the highest tokens per watt architecture in the world. 

</details>

**Dwarkesh Patel**: 既然如此，为什么 Anthropic 几天前宣布与 **Broadcom**（博通）和 Google 达成数十亿美元的协议，使用 TPU 呢？

**Jensen Huang**: Anthropic 是一个特例，而不是趋势。如果没有 Anthropic，TPU 哪来的增长？100% 都是 Anthropic。如果没有 Anthropic，**Trainium** 哪来的增长？我并不会因为别人尝试其他东西而感到冒犯。如果他们不尝试，怎么知道我们的有多好？有时候你需要被提醒一下。建立一个比英伟达更好的东西并不容易。看看有多少 ASIC 项目被取消了。我们是唯一一家每年都在大幅跃进的公司。

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: If all these things are true about price, performance, and performance per watt, et cetera, are true, why do you think it is the case that, say, Anthropic for example, just announced a couple days ago they have a multi-gigawatt deal with Broadcom and Google for TPUs and majority of their compute? 

**Jensen Huang**: Anthropic is a unique instance, not a trend. Without Anthropic, why would there be any TPU growth at all? It's 100% Anthropic. Without Anthropic, why would there be Trainium growth at all? It's 100% Anthropic. I'm not offended by other people using something else and trying things. If they don't try these other things, how would they know how good ours is? Sometimes you've got to be reminded of it. Just because you're going to build an ASIC… You still have to build something better than Nvidia. It's not that easy building something better than Nvidia. 

</details>

### 投资 OpenAI 与遗憾

**Jensen Huang**: 很久以前，我们只是没能力做某些事。当时我没有深刻意识到建立像 **OpenAI** 和 Anthropic 这样的基础 AI 实验室有多困难，以及他们需要来自供应商本身的巨额投资。我们当时没能力给 Anthropic 投几十亿美元。但 Google 和 AWS 投了。我当时的错误是没意识到 VC 永远不会给一个实验室投 50-100 亿美元。但我不会再犯同样的错误了。我很高兴能投资 OpenAI，很高兴能帮助他们扩展。

<details>
<summary>Original English</summary>

**Jensen Huang**: A long time ago, we just didn't have the ability to do it. At the time, I didn't deeply internalize how difficult it would be to build a foundation AI lab like OpenAI and Anthropic, and the fact that they needed huge investments from the supplier themselves. We just weren't in a position to make the multi-billion dollar investment into Anthropic so that they could use our compute. But Google and AWS were. I would say my mistake is I didn't deeply internalize that they really had no other options, that a VC would never put in $5-10 billion of investment into an AI lab with the hopes of it turning out to be Anthropic. So that was my miss. But I'm not going to make that same mistake again. I'm delighted to invest in OpenAI, and I'm delighted to help them scale, and I believe it is essential to do so. 

</details>

**Dwarkesh Patel**: 为什么英伟达不自己成为云服务商，直接出租计算力呢？你有这么多现金。

**Jensen Huang**: 这是公司的哲学：**尽一切必要努力，但干预尽可能少**。如果我们不冒这个险去构建 **NVLink**，去建立整个堆栈，去坚持 20 年在 CUDA 上亏钱，这件事就没人会做。如果我们不创建 **cuLitho**（计算光刻库），就没人会做。所以我们应该全身心地去做这些事。然而，世界上有很多云。如果我们不去做，别人也会出现。我们支持 **CoreWeave** 这些“新云”（Neocloud），因为我们希望生态系统繁荣。我们不挑选赢家，我们支持所有人。

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: Why doesn't Nvidia become a cloud themselves? Why doesn't it become a hyperscaler themselves and rent this compute out? You have all this cash to do it. 

**Jensen Huang**: This is a philosophy of the company, and I think it's wise. We should do as much as needed, as little as possible. The work that we do with building our computing platform, if we don't do it, I genuinely believe it doesn't get done. If we didn't take the risk that we take—if we didn't build NVLink the way we built it, if we didn't build the whole stack, if we didn't create the ecosystem the way we did, if we didn't dedicate ourselves to 20 years of CUDA while losing money most of that time—if we didn't do it, nobody else would have done it. We created a library for computational lithography called cuLitho. If we didn't create it, nobody would have. However, the world has lots of clouds. If I didn't do it, somebody would show up. In the case of clouds, if we didn't support CoreWeave to exist, these neoclouds, these AI clouds, wouldn't exist. We invest in our ecosystem because I want our ecosystem to thrive. We don't pick winners. We need to support everyone. 

</details>

### 对华芯片出口政策辩论

**Dwarkesh Patel**: 谈谈中国。如果中国公司和政府有能力训练像 **Claude Mythos** 这种具有网络攻击能力的模型，这难道不是美国国家安全的威胁吗？

**Jensen Huang**: 首先，芯片在中国是存在的。他们制造了世界上 60% 以上的主流芯片。他们有世界上最伟大的计算机科学家，所有 AI 实验室中 50% 的研究员都是华人。面对这一切，创造安全世界的最佳方式是什么？把他们变成敌人可能不是最佳答案。我们希望美国赢，但对话和研究对话是必不可少的。我们应该在“不使用 AI 做什么”上达成共识。

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: I want to ask about China. So if Chinese companies and Chinese labs and the Chinese government had access to the AI chips to train a model like Claude Mythos with these cyber-offensive capabilities and run millions of instances of it with more compute, the question is, is that a threat to American companies, to American national security? 

**Jensen Huang**: First of all, chips exist in China. They manufacture 60% of the world's mainstream chips, maybe more. They have some of the world's greatest computer scientists. As you know, most of the AI researchers in all of these AI labs are Chinese. They have 50% of the world's AI researchers. So the question is, considering all the assets they already have—if you're worried about them, what is the best way to create a safe world? Victimizing them, turning them into an enemy, likely isn't the best answer. We want the United States to win. But I think having a dialogue and having research dialogue is probably the safest thing to do. It is essential that we try to both agree on what not to use the AI for. 

</details>

**Jensen Huang**: 我们希望所有 AI 开发者都在美国的技术栈上进行开发。如果创建一个开源生态系统只运行在外国技术栈上，而封闭生态系统运行在美国技术栈上，那对美国来说将是一个可怕的结果。中国有充足的能源，AI 是并行计算问题，能源可以弥补芯片的不足。即使使用 **7nm** 芯片，如果能源几乎免费，你也可以通过堆砌芯片来获得巨大的算力。**7nm 芯片基本上就是 Hopper 级别**，今天的模型大多是在 Hopper 这一代训练的。华为去年取得了公司历史上最强劲的一年，他们出货了数百万颗芯片，这比 Anthropic 拥有的还要多。

<details>
<summary>Original English</summary>

**Jensen Huang**: What we also want is to make sure that all the AI developers in the world are developing on the American tech stack. It would be extremely foolish to create two ecosystems: the open source ecosystem, and it only runs on a foreign tech stack, and a closed ecosystem that runs on the American tech stack. I think that would be a horrible outcome for the United States. AI is a parallel computing problem, isn't it? Why can't they just put 4x, 10x, as many chips together because energy's free? 7nm chips are essentially Hopper. The ability for Hopper… I've got to tell you, today's models are largely trained on Hopper, Hopper generation. So 7nm chips are plenty good. Huawei just had the largest single year in the history of their company. How many chips did they ship? A ton. Millions. Millions is way more than Anthropic has. 

</details>

### 算法与领先地位

**Dwarkesh Patel**: 但美国实验室能先达到这些能力，是因为我们有更多的 **FLOPs**。如果我们把芯片发往中国，这如何让美国保持领先？

**Jensen Huang**: 我们有 **Vera Rubin** 系列。我们希望美国在每一层都获胜。通过政策放弃世界上第二大市场是对我们国家的失职，是对国家安全的失职。芯片行业是美国生态系统的一部分。那种认为通过限制出口就能完全阻止竞争的思维是幼稚的。英伟达最重要资产之一是生态系统的丰富性，而 50% 的 AI 开发者都在中国。我们不应该放弃他们。如果让全世界的 AI 模型都在别人的技术栈上运行，那对美国有什么好处？计算不像汽车，生态系统非常难以被取代。我们应该去竞争并获胜，而不是直接认输。

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: But how is shipping chips to China keeping the US ahead if they’re bottlenecked on compute? 

**Jensen Huang**: No, no. We've got Vera Rubin for the United States. Why is it that your policy, your philosophy, leads to the United States giving up a vast part of the world's market? Conceding the entire market is not going to allow the United States to win the technology race long-term in the chip layer, in the computing stack. That is just a fact. The single most important thing to our company is the richness of our ecosystem, which is about developers. 50% of the AI developers are in China. The United States should not give that up. Conceding a marketplace based on the premise you described, I simply can't acknowledge that. It makes no sense. 

</details>

### 加速计算的未来

**Dwarkesh Patel**: 最后一个问题。假设深度学习革命没有发生。英伟达现在会在做什么？

**Jensen Huang**: 做同样的事情：加速计算。我们的前提是摩尔定律会失效，通用计算虽然好，但对于很多计算来说并不理想。即使 AI 不存在，英伟达也会非常巨大。因为通用计算的持续扩展能力已经基本走到了尽头。通过领域特定的加速，我们让科学突破成为可能。我们会继续民主化深度学习，让任何学生或研究员只需一张 **GeForce** 显卡就能做惊人的科学。如果没有 AI，我会很伤心，但我们的基本使命——带来加速计算以解决通用计算无法解决的应用——不会改变。

<details>
<summary>Original English</summary>

**Dwarkesh Patel**: Alright, final question. Suppose the deep learning revolution didn't happen. What would Nvidia be doing? 

**Jensen Huang**: Accelerated computing, the same thing we've been doing all along. The premise of our company is that Moore's law is going to… General purpose computing is good for a lot of things, but for a lot of computation it's not ideal. Even if AI doesn't exist today, Nvidia would be very, very large. The reason for that is fairly fundamental, which is that the ability for general purpose computing to continue to scale has largely run its course. If there were no AI, I would be very sad. But the fundamental promise hasn't changed, not even a little bit. We want to help everybody. 

</details>