---
author: House of El - AI
date: '2026-05-26'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=WuhAaMSXD9A
speaker: House of El - AI
tags:
  - compute-cost
  - jevons-paradox
  - agentic-ai
  - resource-allocation
title: AI的昂贵真相：算力内卷、成本危机与真正的价值重塑
summary: 各大科技公司内部推行激进的AI采用策略，导致算力成本失控。通过分析Uber、Meta、微软的荒诞激励机制与英伟达高管的言论悖论，揭示将算力盲目投入消耗竞争而非关键科学研究的战略误区。
insight: ''
draft: true
series: ''
category: tech-trends
area: tech-engineering
project: []
people: []
companies_orgs:
  - Uber
  - Meta
  - Amazon
  - Microsoft
  - Nvidia
products_models:
  - Claude Code
  - GitHub Copilot
media_books: []
status: evergreen
---
### 失控账单与杰文斯悖论

2026年4月，**Uber**的首席技术官低调承认了一个令人震惊的事实：到4月份，公司就已经耗尽了全年的 AI 预算——原本12个月的预算在短短4个月内被彻底烧光。细节则更加糟糕。Uber 在2025年12月向其工程团队推出了 **Anthropic** 的 **Claude Code**（一款 AI 编程工具）。到了3月份，该工具在公司5000名工程师中的采用率从 32% 飙升至 84%。其中，95% 的工程师每月都在使用 AI 工具，而 70% 的提交代码是由 AI 生成的。除了基本工资外，个别工程师每月产生的 AI 使用费用高达 500 至 2000 美元。

这并非偶然，而是 Uber 主动激励的结果。公司建立了内部排行榜，根据工程团队使用的 AI 工具数量进行排名。本质上，你消耗得越多，排名就越高；排名越高，你的表现看起来就越好。他们建立了一个奖励消耗的系统，这也无怪乎12个月的预算会在4个月内化为乌有。这相当于给每个员工发一张公司信用卡，并设立一个花钱最多的排行榜，然后当账单到来时却故作惊讶。作为一名计算机科学博士，我通过分析 AI 的发展来揭示炒作背后的真相。如今真正的现状是：AI 行业已经发展出一个极其严重的成本问题，以至于连销售这项技术的公司都承认其账目无法平衡。

要理解这种失控，我们需要先认识一个核心概念：**Token**（Token：AI模型处理数据的基本单位，约等于一个单词）。每一次使用 AI 工具，无论是提问、编写代码还是运行 AI 代理，都在消耗 Token，而 Token 是需要花钱的。任务越复杂，消耗的 Token 就越多。一个简单的聊天机器人对话可能只消耗几千个 Token，而一个跨越多个文件执行多步骤任务的 AI 代理则会烧掉数百万 Token。

尽管单个 Token 的成本正在快速下降，**Gartner** 的近期报告指出，到2030年，运行前沿 AI 模型的推理成本将比2025年下降超过90%。但这并非全是好消息。因为**代理式 AI**（Agentic AI：能自主执行复杂工作流的系统）完成每项任务所需的 Token 数量是标准聊天机器人的5到30倍。因此，单价下降了，但使用数量却呈爆炸式增长。**高盛**（Goldman Sachs）预测，代理式 AI 可能会使 Token 消耗量在2030年增加24倍。这就是著名的**杰文斯悖论**（Jevons Paradox）：当资源的使用效率提高时，人们不会减少使用量，反而会大幅增加消耗。更便宜的 Token 并不意味着更廉价的 AI 账单。正如 Gartner 高级分析总监指出，企业不应将作为商品的 Token 贬值，与前沿推理能力的普及混为一谈。

<details>
<summary>Original English Source</summary>

In April 2026, Uber's chief technology officer made a quiet admission. The company had already burned through its entire annual AI budget, the entire annual AI budget by April, a budget size for 12 months gone in four. The details make it even worse. Uber had rolled out Anthropic's Claude code, an AI coding tool, to its engineering team in December 2025. By March, adoption had jumped from 32% to 84% of the company's 5,000 engineers. 95% of those engineers were using AI tools every month. 70% of committed code was AI generated. Individual engineers were costing between $500 and $2,000 per month in AI usage on top of their salaries. And the thing is, this didn't happen by accident. Uber had actively incentivized it. The company built internal leaderboards that ranked engineering teams by how much AI tooling they used. Essentially, the more you consume, the higher you ranked. The higher you ranked, the better you looked. A 12-month budget incinerated in four because the company built a system that rewarded spending it. This is the corporate equivalent of giving every employee a company credit card with a leaderboard for who spends the most and then acting surprised when the bill arrives. I'm ML, I have a PhD in computer science, and I analyze AI developments to understand what's actually happening beneath the hype. And what's actually happening right now is that the AI industry has developed a cost problem so significant that even the companies selling the technology are admitting it just doesn't add up.

Before I get into what happened, I need to explain one concept that makes the rest of the story legible super quickly, just like 15 seconds tops. A token is the basic unit of data that an AI model processes. It's roughly one word, sometimes part of a word. Every time you use an AI tool, you ask it a question, have it write code, run an AI agent, you're consuming tokens, and tokens cost money. The more complex the task, the more tokens it consumes. A simple chatbot exchange might use a few thousand tokens. An AI agent performing a multi-step coding task can burn millions.

Here's where it gets interesting. The cost of individual tokens is falling, fast. A recent report from Gartner found that by 2030, the cost of actually using a frontier AI model, sending it a prompt, getting a result back, also called running inference by the way, will cost providers over 90% less than it did in 2025. That sounds like good news. It's not because agentic AI models, the ones that don't just answer a question, but actually go and do things autonomously, like writing code across multiple files, booking flights, or managing workflows without a human guiding every step, require between five and 30 times more tokens per task than a standard chatbot. So, the unit price drops, but the number of units explodes. Goldman Sachs projects that agentic AI could drive a 24-fold increase in token consumption by 2030, reaching 120 quadrillion tokens processed per month.

This is a well-known economic pattern called the Jevons paradox. When a resource becomes more efficient to use, people don't use less of it, they use dramatically more. I covered this concept at length in a previous video where I applied it to the relationship between AI deployment and human employment. The same paradox applies here except instead of jobs, the resource being consumed is compute. Cheaper tokens don't mean cheaper AI, they mean more tokens. As Gartner senior director analyst Will Summer put it, chief product officers should not confuse the deflation of commodity tokens with the democratization of frontier reasoning. That sentence is doing an extraordinary amount of work and I suspect most of the people who need to hear it are not reading Gartner reports.

</details>

### 算力锦标赛与平台垄断

在这种“单价降低但总成本攀升”的背景下，如果企业文化继续奖励无限消耗，荒诞的现象便会发生。2026年4月初，《The Information》报道了 **Meta** 内部网上一个名为 **Clodonomics** 的排行榜。它追踪了超过 85,000 名员工的 AI Token 消耗量，不仅为前 250 名重度用户排名，还授予诸如“Token传奇”、“会话不朽者”和“现金巫师”等游戏化头衔。在一个月内，Meta 员工总共消耗了 60万亿 个 Token，排名第一的用户日均消耗高达 93.6亿 个 Token。按照公共 API 价格计算，总成本约为 9亿美元。

最能说明这套机制无效的细节是：一些员工为了在排行榜上攀升，竟然让 AI 代理闲置运行数小时。他们发明了一种让机器替他们“无所事事”的自动化方法。虽然排行榜随后被撤下，但 Meta 首席技术官依然公开支持其背后的逻辑，认为即便工程师消耗了相当于工资的 Token，只要能带来生产力提升就值得鼓励。不仅是 Meta，**Amazon** 据报道也在促使员工进行 **Token Maxing**（最大化使用 Token）。员工们让内部 AI 工具执行微不足道的任务来夸大 Token 数量并提升内部排名。科技巨头们正陷入一场竞争性的 AI 浪费中。这就像奖励销售团队不是基于他们卖了多少房子，而是基于他们开车去开会烧了多少汽油。排行榜追踪的是燃料消耗，却没人关注产生的收入。工程师们往往容易过度迷恋系统的复杂性，而忽视了软件解决问题的根本目的。Token Maxing 便是这种技术冲动在组织层面的体现，它优化了消耗指标，却完全脱离了价值创造。

除了盲目消耗，平台间的利益争夺也在加剧成本转嫁。**Microsoft** 内部曾进行过为期6个月的实验，同时提供 Claude Code 和自家的 **GitHub Copilot** CLI。尽管工程师们认为 Claude Code 在实际任务中表现更优，微软依然在5月份决定取消前者的许可证，要求团队统一使用 Copilot。官方理由是“工具链统一”，但底层逻辑是削减向 Anthropic 支付的许可与 API 费，将计费留在微软的生态系统内。当自家工程师选择了竞争对手的优质产品时，微软的反应是扼杀对手的产品，而不是改进自己。这是一家将平台控制权置于工程质量之上的公司。更讽刺的是，Copilot 同时转向了导致 Uber 预算破产的同款基于使用量的计费模式。成本问题并未解决，只是换了一个供应商标志。

<details>
<summary>Original English Source</summary>

So, with all of that context, what happens when you take a resource that's getting cheaper per unit but more expensive in aggregate and then build a corporate culture that rewards consuming as much of it as possible. You get Meta's Clodonomics. In early April 2026, The Information reported on an internal Meta leaderboard built voluntarily by an employee on the company's intranet called Clodonomics. It tracked AI token consumption across more than 85,000 Meta employees. It ranked the top 250 power users. It awarded gamified titles like token legend for the highest consumers, session immortal for extraordinary session duration, cash wizard for efficiency in reuse. In a single 30-day period, Meta employees collectively consumed 60 trillion tokens. The top individual user burned through 281 billion tokens averaging 9.36 billion tokens per day. At Anthropic's public API prices, the total would have cost approximately $900 million. Even at steep enterprise discounts, the figure is still staggering.

And here is the detail that tells you everything you need to know about whether this consumption was producing proportional value. Some employees were leaving AI agents running idle for hours doing nothing in order to inflate their position on the leaderboard. They invented a way to get a robot to do nothing on their behalf. Is that automation or delegation of idleness? An AI version of dolce far niente, maybe? The leaderboard was taken down after press coverage, but Meta CTO Andrew Bosworth had publicly endorsed the underlying logic. He said his best engineer was spending the equivalent of his salary in tokens, but was five to 10 times more productive as a result. "It's like this is easy money," Bosworth told Forbes. "Keep doing it. No limit."

And Meta is not alone in this. Amazon has reportedly pushed its employees to token max, a term that has entered Silicon Valley vocabulary in 2026, meaning use as many AI tokens as possible. According to the Financial Times, Amazon employees have been running the company's internal AI tool on trivial tasks to inflate their token counts and climb internal rankings. The industry has invented a term for competitive AI waste, and the largest technology companies on Earth are participating in it. Somewhere an economy is writing a paper about this. The AI will probably summarize it wrong.

I want to pause here and name what this is because I think the absurdity of it can obscure the analytical point. These companies are measuring input, how many tokens are you consuming, as a proxy for output, how much value are you creating, and those two things have no guaranteed relationship. This is like rewarding your sales team not for how many houses they sold, but for how much petrol they burned driving to meetings. The top performer isn't the one who closed the most deals, is the one who drove the most miles. The leaderboard tracks fuel consumption, but nobody's striking revenue. Engineers, and I say this with a lot of love because I am one, have a tendency to get so enamored with the complexity of a system that they often lose sight of what the system is supposed to do. It's almost like being an artist. You want the code to be beautiful, you want the architecture to be elegant, you want the documentation to be pristine, and all of those things have value. I'm not saying they don't before somebody comes at me, but they are secondary to the fundamental purpose of software, which is to solve a problem, to do the thing, to work. Token maxing is the organizational version of that same impulse. It's optimizing for a metric that feels important, consumption, activity, usage, while completely decoupling from the question of whether any of that consumption is producing proportional value.

Meanwhile, Microsoft has been dealing with its own version of this problem, and the details reveal something slightly different but equally instructive. In December 2025, Microsoft opened up access to Anthropic's Claude Code alongside its own GitHub Copilot CLI. Both are AI coding tools that run in a developer's terminal and can write, edit, and manage code. For roughly 6 months, Microsoft engineers run both tools side by side. The engineers preferred Claude Code. Internal comparisons reportedly showed it outperforming Copilot CLI on real engineering tasks. It became, as The Verge's Tom Warren put it, very popular, perhaps a little too popular.

In May, Microsoft began canceling Claude Code licenses. Engineers in the Experiences and Devices division, the teams behind Windows, Microsoft 365, Outlook, Teams, and Surface were given until June 30th to remove Claude Code from their workflows and switch to Copilot CLI. The official justification was tool chain unification. The timing, June 30th, the last day of Microsoft fiscal year, suggests cost-cutting was at least equally important. The specifics of the billing difference are very technical. But the short version is essentially, running cloud code means paying Anthropic both a per-seat license fee and API rate token cost on top. Routing Claude's models through Copilot CLI, which Microsoft owns via GitHub, eliminates the licensing layer and brings the billing in-house. It's cheaper and the money stays inside Microsoft ecosystem.

But the cost story obscures the more revealing detail. Microsoft ran a 6-month experiment. Its own engineers chose the competitor's product, and Microsoft responded by killing the competitor's product rather than improving its own. That is a company optimizing for platform control over engineering quality. Whether that's the right strategic decision is debatable. That it's a cost-driven decision is not. And consider the timing more broadly. GitHub Copilot is simultaneously transitioning to usage-based billing on June 1st, moving from flat premium request counts to a token consumption model using AI credits. So, Microsoft is consolidating onto a single platform at exactly the moment that platform is switching to the same consumption-based pricing model that blew up Uber's budget. The cost problem is not being solved. It is being reorganized under a different logo.

</details>

### 错位激励与群体跟风陷阱

这种企业层面的 AI 成本危机并非单一的戏剧性失败，而是由成千上万个看似理性的采购决策累积而成。它们共同揭示了一个事实：整个行业的支出速度已经远远超过了其衡量回报的能力。这种矛盾在 **Nvidia**（英伟达）高管的言论中体现得最为淋漓尽致。

Nvidia 首席执行官 Jensen Huang 曾表示，如果一名年薪50万美元的工程师没有消耗至少25万美元的 AI Token，他会感到震惊，并将其视为提高生产力的必然要求。然而，Nvidia 应用深度学习副总裁 Bryan Catanzaro 却坦言，对于他的团队来说，算力的成本已经远远超过了员工的人力成本。同一家公司的高管释放出截然相反的信号，这并非谎言，而是由于激励结构的不同。作为制造并销售 GPU 的公司 CEO，其核心动机是最大化需求；而作为管理实际工程预算的副总裁，其动机是在有限的成本内交付结果。

真正危险的是，这种来自供应链顶端、从消费中获利最多的“鼓励消耗”信号，正向下级联至整个行业：在 Meta 变成了 Clodonomics，在 Amazon 变成了 Token Maxing，在 Uber 则变成了在4个月内烧光全年预算的排行榜。整个行业的策略似乎仅仅是让已经拥有工具的人用得更多，而从未系统衡量消耗与产出是否匹配。

人们自然会问：这是泡沫吗？只有在泡沫破裂后，我们才能确切地称其为泡沫。但数据不会说谎。Amazon、Microsoft、Alphabet 和 Meta 在2026年的总资本支出逼近 7400亿美元，比前一年增长了 69%。与此同时，科技行业却经历了超过 92,000 人的裁员。研究显示，AI 自动化目前仅在少数岗位具有经济可行性，而在 77% 的场景下，保留人类员工仍然更具成本效益。必须承认，AI 技术本身是有效的，它确实能写代码、完成复杂任务。问题不在于技术是否有效，而在于当前的支出速度相对于回报率是否具有可持续性。各大公司之所以如此疯狂地投资，是因为“害怕成为唯一一个投资不足而错失 AI 浪潮的人”。这种错失恐惧症（FOMO）比缺乏实际回报的数据更有驱动力。这不是技术驱动的投资战略，而是一场价值 7400亿美元的群体跟风行为。

<details>
<summary>Original English Source</summary>

This is what the AI cost crisis actually looks like at the enterprise level. It is not a single dramatic failure. It is a thousand procurement decisions, each individually rational, that collectively reveal an industry spending faster than it can measure the returns. And then, there is Nvidia, where the contradiction is so clear it almost doesn't need commentary.

Jensen Huang, Nvidia's CEO, said in March 2026 that he would be deeply alarmed if a $500,000 engineer at his company was not consuming at least $250,000 in AI tokens. He framed this as a productivity imperative. The tokens make the engineer more valuable. Bryan Catanzaro, Nvidia's vice president of applied deep learning, told Axios, "For my team, the cost of compute is far beyond the cost of the employees." Same company, one executive says spend more on tokens, the other says the tokens already cost more than the people.

Neither of them is wrong, by the way, and I think that's the part that most people miss when they look at contradiction like this and assume somebody must be lying or confused or stupid. They're not. They have different incentive structures. Huang is the CEO of a company that manufactures the GPUs that process every token consumed everywhere in the world. More tokens consumed means more GPUs needed means more Nvidia revenue. His incentive is to maximize demand. Of course, he wants engineers to burn through tokens. Catanzaro manages an actual engineering budget. His incentive is to deliver results within a cost envelope. Of course, he notices when the compute bill exceeds the payroll. In life, there are very few good and bad actors in situations like this. There are incentives, objectives, and paths to reach them.

The problem isn't that Huang is wrong or that Catanzaro is wrong. The problem is that the use more signal from the top of the supply chain, from the company that profits most from consumption, cascades downwards through the entire industry. It reaches Meta, where it becomes Cloudonomics. It reaches Amazon, where it becomes token maxing on trivial tasks. It reaches Uber, where it becomes leaderboards that incinerate a year's budget in 4 months. The signal to consume originates from the people who sell what's being consumed. And at no point in this chain is anyone systematically measuring whether the consumption is producing proportional value.

At this point, the question that every comment section will ask is, of course, is this a bubble? I want to be very honest about this rather than satisfying for everyone. Nobody other than maybe God can call a bubble in real time. That is a near universal truth in economics and financial markets. You only know it was a bubble after it pops. People who confidently tell you this is definitely a bubble or this is definitely not a bubble are offering you certainty, which is comfortable and almost certainly wrong.

What I can do is describe what the numbers look like. Combined 2026 capital expenditure from Amazon, Microsoft, Alphabet, and Meta is now pushing $740 billion, a 69% increase from 2025. There have been over 92,000 tech layoffs in 2026 so far, already outpacing last year's total. A 2024 MIT study found that AI automation is economically viable in only 23% of roles where visual tasks are primary. In the remaining 77% keeping human workers is still cheaper. But, and this is very important, AI generally works. The underlying technology produces real output. Cloud code actually writes functional code. AI agents actually complete tasks. This is not a speculative technology with no demonstrated capability. The question is not whether AI works. The question is whether the rate of spending is sustainable given the current rate of return. And the honest answer is, I don't know. I don't think anyone does.

These companies are investing at this scale because they see potential, and that is not exactly irrational. The last time humanity encountered a technology with this kind of transformative promise was the Industrial Revolution, and for all the human suffering it caused, which I covered in a separate video, it was from a purely technological standpoint one of the most productive periods in human history. I can understand why CEOs are going all in. Their investment thesis is a combination of fundamentals and human judgment. The fundamentals are real. AI can deliver a certain set of things, and that set is expanding. The judgment part carries a great deal of hope. Hope that this technology will reshape industries that we steam and electricity did. Would I personally be more conservative? Probably, but everyone has their own risk appetite, right? And I'm not going to pretend I have better judgment than people who are running these companies.

What I will say is that hope is not a deployment strategy. And right now, the gap between the hope and the operational reality is being filled with leaderboards. And there is another thing that nobody seems willing to say. Nobody's forcing these companies to spend $740 billion in a single year. They could invest a fraction of that, say 100 bill, measure what actually produces returns, scale the things that work, and ramp up from there. The technology is not going to vanish next quarter. The models are not going to magically untrain themselves overnight. There is no external deadline, but every company is spending because every other company is spending, and the fear of being the only one that under invested, the one that missed AI, is more powerful than the absence of proven returns at this scale. That is not a technology-driven investment strategy. That is FOMO herd behavior at $740 billion. And the history of herd behavior at scale is not exactly encouraging, regardless of whether the underlying technology is real or not.

</details>

### 终止内卷：重塑算力价值

当前的算力部署策略——试图从已经饱和的软件工程师群体中榨取更多的 Token 消耗——并不能证明高达 7400亿美元投资的合理性。那些单纯移除人类员工并用 AI 替代的公司已经遭遇了结果崩溃，而现在，保留人类并叠加 AI 的公司则发现，AI 的成本甚至超过了人力。这两种部署失败都源于同一个根本问题：缺乏清晰的 AI 战略，仅仅因为同侪压力而盲目采纳，并把最容易衡量的“消耗量”当作了成功指标。

算力究竟应该流向何处？如果目标是创造能够支撑这数千亿美元资本支出的真实需求，答案不应该是迫使软件工程师去爬排行榜，而是应该将算力分配给那些正面临人类认知极限的难题的人群。**大学与科研机构**才是最具潜力的突破口。尽管目前已有零星的学术资助和研究合作，但与浪费在内部攀比机制上的资源相比，这些投入只是九牛一毛。

我们需要为化学家、物理学家、医学家、经济学家和气候科学家提供规模庞大的前沿 AI 算力支持。这些人已经懂得如何编程并理解计算方法，他们只是缺乏算力来完成此前无法想象的任务。当一位化学家试图在数十亿种配置中模拟分子相互作用，或是经济学家试图模拟复杂的非线性系统时，大规模算力将成为解题的关键。如果赋予研究人员足够的算力，他们不会去刷榜，而是去攻克科学难题。

从这种真正科研探索中涌现的突破，才能创造出行业极度渴求的、有机且可持续的需求。通过 AI 辅助的分子建模发现一个新药物靶点，不仅消耗了 Token，更会催生包括后续研究、临床试验和实际应用在内的庞大产业，这些都会持续产生对 AI 的需求。气候建模的突破同样会带来对持续监测和模拟的海量需求，足以让 GPU 制造商在未来几十年内保持运转。

这才是建立可持续需求的方法：将技术深度嵌入科学发现，让问题本身驱动算力消耗。技术在理解问题本质的专家手中，才能发挥最大的效用。如果 7400亿美元的资本支出是为了让工程师在虚荣心驱动的排行榜上竞争，那么这注定不可持续。但如果这笔资金被用来资助蛋白质折叠、气候建模、药物发现和经济模拟等领域的科学突破，那么这就不是泡沫，而是能带来真正价值重塑的伟大投资。

<details>
<summary>Original English Source</summary>

But what I do generally believe is that the current deployment strategy, squeezing more consumption out of the same use case, which is software engineering, is not the path that justifies this level of investment in my eyes at least. I covered the other side of the cost equation in a previous video, companies that fired their human workforce, replaced them with AI, and watch the results collapse. That video was about companies removing humans and AI failing to do the job. This one is about companies keeping the humans, adding AI on top, and discovering the AI costs more than the people it was supposed to augment. Both are deployment failures, and both stem from the same underlying problem. These companies do not have a coherent theory of what AI is supposed to do for them. They are adopting AI because everyone else is adopting AI. They are measuring consumption because consumption is easy to measure, and they are discovering one blown budget at a time that the absence of a strategy is itself the most expensive mistake they can make. The technology is not the problem. The technology works. The deployment of the technology, who decides how it's used, what's being measured, and whether anyone is checking if the output justifies the input, that's where every single one of these stories breaks down.

So, where should the computer actually go? Right now, Jensen Huang wants his engineers to burn $250,000 in tokens each. Meta built a leaderboard to see who could consume the most. Amazon told employees to token max. The entire demand generation strategy of the AI industry appears to be take the people who already have AI tools and tell them to just use more. That is the wrong axis entirely. If the goal is to generate the kind of demand that actually justifies $740 billion in capital expenditure, the answer is not to squeeze more consumption out of software engineers who are already saturated. The answer is to point the compute at people who have unsolved problems. Universities are the obvious candidate, I think, and I say this as somebody who has worked in academia.

Now, before the comments fill up with but this already exists, yes, it does. Nvidia has CUDA research grants, I'm aware. Google has academic partnerships. Microsoft has Azure credits for researchers. These programs are real and they are doing useful work, but they are a fraction of what's possible and they are dwarfed by the resources being poured into internal leaderboards and token maxing incentives. The question again is not whether university partnerships exist, it is whether the industry is serious about scaling them or whether they remain a rounding error next to the budget being spent encouraging Meta employees to compete for the title of session immortal.

Give researchers in chemistry, physics, medicine, economics, and climate science free or subsidized access to frontier AI models at a scale that matches the ambition of the investment. Not for homework, I don't mean exams, but I mean for research legitimately. These are people who already know how to code, who already understand computational methods, and who are sitting on problems that generally exceed human cognitive capacity. The chemist trying to model molecular interactions across billions of configurations. The economist trying to simulate non-linear systems that the entire field still models with linear regressions. The medical researcher trying to identify drug interactions across data sets too large for any human team to process. The physicist running simulations that currently take months on existing hardware.

If somebody had given me a large allocation of free compute when I was working in academia, I would have been significantly more incentivized to experiment more, to try things that felt too computationally expensive to justify on a limited budget. Everybody in academia is incentivized to publish papers, to discover, to push their field forward. The real opportunity isn't just within computer science. It is in empowering the other scientists, the chemists, the physicists, the economists, the medical researchers. They are already excellent at coding. They already understand data. They just need the compute to do things that were previously impossible.

If you give researchers compute, they will use it, not to climb a leaderboard, but to try to solve something. And the breakthroughs that emerge from that process would create the organic sustainable demand that the industry desperately needs. Demand rooted in genuine discovery, not in gamified consumption. A new drug target identified through AI-assisted molecular modeling doesn't just tokens, it creates an entire industry of follow-on research, clinical trials, and applications that need more AI. A breakthrough in climate modeling doesn't just use compute, it generates demand for continuous monitoring, prediction, and simulation at a scale that would keep GPU manufacturers happy and busy for decades. That is how you build sustainable demand, not by telling software engineers to consume harder, but by embedding the technology in as many fields as possible, and letting the problems themselves generate the usage.

I am not saying this should be done to displace researchers or make their expertise obsolete. I'm saying the exact opposite. The whole point is to harness the technology to empower people who are already doing important work, to supercharge human expertise, not replace it. The technology works best when it's pointed at a problem by somebody who understands the problem. A leaderboard doesn't understand much, but a researcher definitely does. And that distinction matters. If the path to justifying $740 billion in annual capital expenditure is make engineers climb leaderboards, then yes, the spending probably isn't sustainable. But if the path is fund breakthroughs in protein folding, climate modeling, drug discovery, and economic simulation that couldn't happen without this technology, that is not a bubble. That is an investment. The difference between those two outcomes is not the technology. The tech is the same. The difference is where we pointed. Right now, the industry is pointing it at leaderboards, at AI token legend badges. It engineers running agents idle to inflate a number that nobody has connected to a business outcome. The people who built these leaderboards sat in a room and decided that measuring consumption was a strategy. Another meeting can happen. A different strategy can emerge. That's not failure, it's just course correction. But it requires the humility to look at the data, recognize that burning a 12-month budget in 4 months while your employees gain the metrics is not exactly a sign of success and just change direction.

</details>