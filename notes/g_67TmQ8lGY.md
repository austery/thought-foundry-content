---
author: a16z
date: '2026-11-16'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=g_67TmQ8lGY
speaker: a16z
tags:
  - ai-agent
  - economic-impact
  - higher-education
  - structural-modeling
  - labor-market
title: AI 智能体协同、经济影响与高等教育变革的深度探讨
summary: 在播客中，参与者讨论了 AI 发展的现状，强调智能体之间的协同能力而非单纯的计算能力是实现经济转型的关键。他们探讨了 AI 对就业市场的潜在冲击，特别是快速转型可能导致的结构性失业风险。此外，讨论还涵盖了 AI 在建立结构模型、数字孪生以及高等教育领域的创新潜力，并强调了经济学工具在 AI 对齐和机制设计中的重要作用。
insight: ''
draft: true
series: ''
category: ai-application
area: tech-engineering
project: []
people: []
companies_orgs: []
products_models: []
media_books: []
status: evergreen
---
<!-- chunk 1/8 -->

各项体制的运转并没有我们所希望或担忧的那么顺畅。英伟达身上正发生着这些奇怪的事情。如果你看预测市场上关于 Anthropic IPO 估值的预测，它并没有飙升到 2 万亿以上。
<details><summary>Original English</summary>
institutions are not [music] quite running as smoothly as either we might like or we might fear. We have these weird things happening with Nvidia. If you look at prediction markets [music] for what the anthropic IPO will go for, it's not flying above 2 trillion.
</details>

>> 你预计这种增长会持续下去，还是认为会进入平台期？
<details><summary>Original English</summary>
>> Do you expect the growth to continue or do you think a leveling up?
</details>

>> 收益会超过成本，但这需要一些时间，而且其发展路径会比很多人让你相信的要正常得多。
<details><summary>Original English</summary>
>> Benefits will exceed costs, but it will take some time and the path will be quite a bit more normal than many people would have you believe.
</details>

>> 要实现真正的经济转型，你实际需要的不仅仅是[音乐]能力，而是这些智能体之间相互协调的能力。现在有智能体集群（agentic swarms）这种概念，但如果你去深入剖析，这些智能体在协调方面仍然非常差。它们大多只是在进行并行处理。
<details><summary>Original English</summary>
>> What you actually need for real economic transformation is not just [music] competence. It's the ability of these agents to coordinate with one another. There's this idea of agentic swarms, but if you unpack it, these agents are still very bad at coordinating. They're mostly just doing parallel processing.
</details>

>> 通常某些事情发展得越快，仅仅意味着你会更快遇到真正的瓶颈。如果你问我智能体何时会占到 GDP 的 10%？我认为不会很快。
<details><summary>Original English</summary>
>> Often the faster that some things move, that just means you hit the real bottlenecks more quickly. If you ask me the question, when will agents be 10% of GDP? I don't think it's soon.
</details>

>> 这两种不同的世界会是什么样子？一个是 GDP 增长相对更为正常的世界，另一个则是增长真正达到两位数的世界。[音乐] 嗯，
<details><summary>Original English</summary>
>> What are the two different worlds look like? One in which GDP growth is a bit more normal and another in which it actually becomes double digit. [music] Um,
</details>

### AI 现状与 METR 报告讨论

>> 亚历克斯、泰勒，欢迎来到 Th andZ 播客。
<details><summary>Original English</summary>
>> Alex Tyler, welcome to Th andZ podcast.
</details>

>> 很高兴来到这里。
<details><summary>Original English</summary>
>> Happy to be here.
</details>

>> 谢谢。谢谢邀请我们。
<details><summary>Original English</summary>
>> Thanks. Thanks for having us.
</details>

>> 那么，我们要聊的有很多。首先，我们来谈谈一些适时的热门话题。Media 报告发布了，引发了大量的讨论。保罗·克里斯蒂亚诺（Paul Christiano）也在推文中发了言。目前关于人工智能的现状以及递归自我改进（RSI）等，存在着很多动荡和焦虑。我很想知道，亚历克斯，你对我们目前所看到的这一切有什么反应？对于目前提出的某些论断，你的立场又是什么？
<details><summary>Original English</summary>
>> So, there's there's a lot to talk about. F. First, let's talk about some some timely topics. The media report came out. There's been a lot of conversation. Paul Cristiano has talked and tweets. there's a lot of sort of unrest and anxiety around sort of uh sort of the state of AI right now and and and RSI and and um I'm curious, Alex, what is your reaction to what we are seeing and and where do you stand on some of the proclamations being made right now?
</details>

>> 嗯，我是说，我仔细阅读了它。我认为不可否认的是，我们正在取得令人难以置信的进展，而且这种进展正在加速。我想任何关注模型发布的人都会发现，发布变得更加频繁了，模型也变得更加强大。能力方面的跨越，比如从去年 11 月到今年 11 月，简直就是一个认不出来的全新世界，尤其是智能体 AI（Agentic AI）与聊天机器人时代的差异。你可以看到各家公司发布的内容，当有数据展现聊天机器人时代与智能体时代的差异时，你现在看到的是真正的生产力。比如对于聊天机器人，你使用它几乎就像是在用一个高级版的维基百科或类似的东西，你向它提问，它给你回答；而对于智能体系统，你看到的是实际的工作产出，那种工作水平、这些系统实际执行工作的能力进展得如此之快，基本上你会看到大量的曲棍球棒式增长（hockey sticks）。这就是 meter 报告所展示的：看，这里又是一个曲棍球棒曲线。所以对我来说，说实话，我并没有因为 meter 报告而对观点做出太多更新，因为 meter 报告中的很多数据在其他地方就已经存在了。比如 S1 声明，我们之前就知道某些未发布的模型。所以我没有更新太多看法，但那是因为我差不多早就持有那种观点了。我——
<details><summary>Original English</summary>
>> Um so I mean I I I read it closely. I think I think it's undeniable that we're having in you know incredible progress and that the progress is accelerating. I think anybody who's looking at, you know, the model releases, they're becoming, uh, you know, more frequent. Uh, they're becoming more powerful. The capabilities are, you know, going, you know, going from like last November to this November. It's just an unrecognizable world, especially with the, you know, the the difference between like Agentic AI and the chatbot era. um you're seeing like you know the what's coming out of companies when when you have data coming out on like the difference between you know the chatbot era versus the agentic era um you're seeing real productivity now like with the chatbot you're kind of like using it almost like a a fancy version of of a you know Wikipedia or something like that you're asking a questions it gives you gives you answers with an agentic system you're seeing actual work and that level of work the ability of these systems to actually do the work is just progressing so quickly and you know you're you're seeing a lot of hockey sticks basically. Um and that's what the meter report showed is that look here's another hockey stick. So to me I didn't I to tell you the truth I didn't update too much from the meter report because a lot of the data in the meter report has been around in other spaces. So the S1 statement um you know we knew about the some of the unreleased models. So it's uh I didn't update too much but that's because I was kind of already there. I
</details>

>> 你的看法是，你所指出的这些曲棍球棒曲线会一直持续上升吗？它们在什么阶段可能会逐渐减弱，或者说，从现在开始，你对其中一些曲棍球棒曲线的维持有多大程度的看好？
<details><summary>Original English</summary>
>> is your view that the hockey sticks that you're identifying that they will just sort of continuously grow go up at what point might might they peter out or you know sort of how bullish are you from here on on some of these hockey sticks uh you know maintaining?
</details>

>> 所以我是说，正如你所说的，“其中一些曲棍球棒曲线”，我认为这是关键用词，问题在于：这些曲棍球棒曲线会出现在哪里？它们之间是如何关联的？所以在 meter 报告中，对我来说非常关键的表述是未良好验证、未明确界定的任务（unwell specified tasks）。最大的问题在于，那些界定不那么明确的任务会怎样？现实中很多工作都是没有明确界定的。我并不是那种认为“好吧，在未明确界定的工作方面我们很安全”的人，我认为模型在处理不够明确界定的任务上也在变得越来越好，但我认为在这类任务上要实现曲棍球棒式增长可能会更难。另外还有很多关于默会知识（tacit knowledge）的问题，以及哈耶克式的对于经济实际影响的考量。我和泰勒都是经济学家，所以我必须对所有这些信息进行梳理，探讨这些曲棍球棒曲线对经济学意味着什么，对具有经济价值的任务意味着什么。对我而言，重大的问题在于，随着模型的每一次迭代，当前模型解锁了哪些前代模型未能解锁的具有经济价值的任务？而曲棍球棒曲线对这一点的反映是非常不完善的。因此，你可能会在基准测试中看到一条看起来极其惊人的曲棍球棒曲线，但在现实世界中并没有真正看到太多的加速。我们现在还没到那个地步。我认为我们在现实世界中确实看到了很多加速，但这些只是我所思考的一些问题。泰勒，我们把话题转向你。我觉得在这些讨论中，你一直是一个更加冷静的声音——我不是说亚历克斯不冷静，但我的意思是，根据最近发生的这些事情，你的看法有所更新吗，或者你的观点是什么？
<details><summary>Original English</summary>
>> So I mean like that's what you the the thing that you said some of these hockey sticks is I think the main term it's like where are the hockey sticks going to be? How are they connected? So in the meter report to me like the very the key phrase was unwellverified you know unwell specified tasks um what is the big question is like what about less specified tasks a lot of work is not well specified I I'm not one of those people who thinks this is like all right we're safe on the nonwell specified side I think the models are becoming increasingly better uh on on non very well specified tasks as well but I think you know it might be harder uh to to to do hockey sticks on those sort of tasks. Um there's also a lot of like the questions of like tacic knowledge uh kind of hayakian concerns about like the actual impact on the economy. I think you know Tyler and I are both economists. So all of all of this information I have to kind of sift through about what these hockey sticks mean for economics and what does it mean for economically valuable tasks. And the big questions for me are like every model iteration, what are the economically valuable tasks that is this model is unlocking that the previous model wasn't unlocking. And this is kind of captured very imperfectly by the hockey stick. So you can get a hockey stick that looks crazy on a benchmark and then you're not really seeing a lot of acceleration in the real world. We're not there yet. I think we're seeing a lot of acceleration in the real world. But these are just, you know, some of the questions that that that I have. Tyler, let's let's go to you. I feel like you've been a more sober voice uh in in the in the in the conversation. Alex hasn't been sober, but I just mean, do you have you updated at all based on what what's what's been happening here or what is your view?
</details>

>> 嗯，通常某些事情发展得越快，仅仅意味着你会更快遇到真正的瓶颈。因此，我不会那么频繁地更新看法，但这毕竟是在 AI 领域，而在 AI 领域，确切的日期非常重要。我们录制的时间是 2026 年 11 月 11 日。这很重要，我想说，自 8 月份以来，我的观点发生了相当大的变化。最主要的原因是数学问题。也就是说，在那些没有太多人为瓶颈的领域取得了进展。我看到了迅速得多的进展，以及在比如三周左右的时间内打造出一个明显更好的新模型的能力。我之前没想到这会发生得这么快。所以我会把这一变化的节点定在几个月前。但如果你是指过去这一周，情况更偏悲观（the mater bearish），英伟达身上正发生着这些奇怪的事情。我无法预测，但这会让整个板块稍微放缓。如果你看看预测市场上关于 Anthropic IPO 估值的预测，它们上下波动，但并没有飙升到 2 万亿以上。你看 Anthropic 自己预测的收入数字——我忘了确切的数字，我不会说我很失望，但它们并不是你在超高速起飞情景下所期望看到的数字。而这还是用于他们 IPO 的数据。所以我想说，出于这些原因，在过去这一周里，我比一周前大约看空了 1%。只是各项体制的运转并没有像我们所希望或担忧（取决于你的立场）的那么顺畅。
<details><summary>Original English</summary>
>> Well, often the faster that some things move, that just means you hit the real bottlenecks more quickly. So, I don't update that frequently, but this is AI land, and in AI land, the exact dates really matter. So, we're recording on November 11th, 2026. And that matters, I would say, since August, I've changed my views a fair amount. Most of all, because of the math problems. So, progress in areas where there are not many human bottlenecks. Uh, I see much more rapid progress and the ability to create a new model that is clearly better, say, within something like three weeks. Uh, I hadn't thought that would happen as quickly as it had. So I would date that to a few months ago. But if you mean over the last week, the mater bearish, we have these weird things happening with Nvidia. I have no prediction, but it will slow down the sector a bit. If you look at prediction markets for what the anthropic IPO will go for, they bounce up and down, but it's not flying above two trillion. You look at Anthropic's own projected revenue numbers. I forget the exact numbers. I wouldn't say I was underwhelmed, but they're not numbers that you would expect under the super fast takeoff scenarios. And that's for their IPO. So, I'd say I'm like 1% more bearish over the course of the last week than I was a week ago for those reasons. Just the institutions are not quite running as smoothly as either we might like or we might fear depending on your point of view.
</details>

OpenAI 和 Anthropic 的那种增长率，你的基准假设是否认为，在过去比方说两三年里的那种增长率还会继续下去？先撇开具体公司不谈，我更多指的是领先的 AI 公司，比如我们所见到的那种经济影响——无论这两家公司是否保持领先，当然它们也在与超大规模云厂商竞争——你是否预计这种增长会持续下去，还是认为会进入平台期？
<details><summary>Original English</summary>
are either the sort of growth rates of open AI and anthropic um is your sort of base case that over the last let's say you know two or three years that those growth rates continue and and put aside the specific companies but I more mean just the the leading AI companies like the the the sort of economic impact that we've seen you know whether those two companies you know maintain the lead of course they're competing with the hyperscalers too do do you uh expect the the growth to to continue or do you think a leveling out?
</details>

>> 嗯，几周前我在湾区，很多人向我灌输非常高的收入数字，我向他们所有人都提出了下面这个问题。我说：“还有哪些其他行业能够以足够快的速度增长，从而证明你们给我的 Anthropic 和 OpenAI 的极端收入数字是合理的？”对于这个问题，没有一个人能给出答案。他们甚至都没有试图回答我。所以，我认为这意味着极端的收入数字是不真实的。这并没有让我对整个行业看空。我依然看好。我认为它会发展得很好。那些都是伟大的公司。但归根结底，你看市场数据，无论是实际利率、股票价格，还是任何指标，市场数据看起来依然相当正常。而且全世界的投资界都在讨论人工智能，它不再像 2014 年那时是一种奇怪的谜团，让你能说我——
<details><summary>Original English</summary>
>> Well, I was in the Bay Area a few weeks ago and many people were pushing very high revenue numbers on me and I asked them all the following question. I said, "What are the other sectors that are going to grow sufficiently rapidly to justify the extreme revenue numbers you're giving me for anthropic and open AI?" And no one had an answer for that question. They didn't even try to give me answers. So, I think that means the extreme revenue numbers are false. That doesn't make me bearish on the sector as a whole. I'm still bullish. I think it will be fine. Those are great companies. But at the end of the day, you look at market data, whether it's real interest rates, stock prices, anything. Market data still look pretty normal. And the whole world investing community is talking about AI. It's not some kind of weird mystery like it was back in 2014 where you could say I
</details>

<!-- chunk 2/8 -->

读了LessWrong上的一篇博客文章，然后因为读了它，我现在变得非常富有。所以我更相信市场的判断，而不是湾区那些对社会交往思考没那么深入的人的判断。这就是我的立场。它会改变整个世界。效益将超过成本，但这需要一些时间，而且其发展路径会比很多人让你相信的要寻常得多。

是的，顺着这点补充一下，我认为泰勒说得非常切中要害：你必须开始在经济的其他部门看到生产率数据，才能支撑起这种营收增长。因此在某个时间点，经济的其他部门必须愿意为那款产品付费，而这种不断提高的付费意愿，必须来自于其余经济部门生产率的提升。我们目前确实还没看到太多这方面的证据。并不是说它不会发生，但它确实需要在某个时间点发生。

另一个方面是竞争。我认为，特别是在过去几个月里开始出现的情况，是前沿实验室之间极其激烈的价格竞争。以前他们只是在比拼谁的模型更好，而现在越来越多的企业开始使用这些模型，而且它们变得相当昂贵——顺便提一句，因为代理式AI（agentic AI）消耗的Token要多得多——所以现在各家公司，你知道，OpenAI、Anthropic……他们都在尝试，你知道，Muse也参与其中，DeepMind也加入竞争，真正试图表示：“不，我们提供的是更便宜的模型，它同样优秀，或者甚至可能稍微好一点，或者稍微差一点。”因此你看到Token价格大幅下降。而且，你知道，Ramp有一套非常好的数据集来追踪这些情况。你看到Token使用量呈指数级增长，而营收数据却持平，对吧？这是从何而来的？正是因为价格竞争。因此在前沿领域，你看到的价格竞争比大概六个月前要激烈得多。
<details><summary>Original English</summary>
read a less wrong blog post and now I'm really wealthy because I did. So I trust the judgment of the market more than the judgment of the Bay Area people who don't think that carefully about social interactions. So that's where I stand. It'll change the whole world. Uh benefits will exceed costs but it will take some time and the path will be quite a bit more normal than many people would have you believe.

Yeah, and just to add to that, I think there Tyler is exactly spot on in the fact that like you need to start seeing the productivity numbers in the rest of the economy to justify the the revenue increases. So at some point the rest of the economy needs to be willing to pay for that for that product and that increasing willingness to pay has to be from increasing productivity in the rest of the economy. And we haven't really seen too much evidence of that. Not to say that it won't happen, but it does need to happen at some point.

The other part about it is competition. So I think what's started to happen particularly in the last few months is extreme price competition um from from the frontier labs as far as like before they were just trying to compete on like who has the better model and now that the models are being used by increasing number of enterprises and uh they're becoming quite expensive because agentic AI by the way uses way more tokens um so now companies are you know open AI anthropic uh they're they're try you know muse is in the game. Uh Deep Mind is in the game trying to actually say like, "No, we're offering a cheaper model that that as good or maybe even like a little bit better or maybe a little bit worse." And so you're seeing token prices come down a lot. And so, you know, RAMP has a really nice data set of to track these things. And you saw exponential increases in token usage and flat revenue numbers, right? Where's that coming from? It's because of price price competition. So at the frontier, you're seeing way more price competition than you used to like six months ago.
</details>

### 选举与监管对AI推进节奏的影响

>> 至于最近的选举，我认为这被夸大了。我认为很多数据中心仍会继续推进，但我认为它会把事情稍微放慢一点。出台监管、监管稍微变严、监管出台得稍微更早、或者特朗普在护栏问题上做出让步的可能性更大了。对我来说，这不算一种主要力量，但话说回来，在腾飞速度、营收数据以及其他所有方面，这都会让我对该行业稍微更悲观一点点。
<details><summary>Original English</summary>
>> And the very recent elections, I think those are being overplayed. I think a lot of data centers still will proceed, but I think it will slow things down a bit. There's greater likelihood of regulation or somewhat tougher regulation or regulation a bit sooner or Trump, you know, giving on the issue of guard rails. To me, it's not a major force, but again, it's going to make me a modest bit more bearish on the sector in terms of speed of takeoff, revenue numbers, anything else.
</details>

>> 顺便问一句，既然聊到这个话题，这次中期选举有没有让你在其他任何方面更新看法，泰勒？还是说，你知道，这种恒温调节式的反冲是一种普遍现象，我们本就应该经常预料到这种钟摆式的摆动？
<details><summary>Original English</summary>
>> By the way, while we're on the topic, did the midterms cause you to update anywhere else, uh, Tyler, or it kind of, you know, thermostatic back uh, you know, backlash is is a thing and, you know, we should just expect these pendulum swings often.
</details>

>> 嗯，大部分情况都在我的预期之中，事实上我也预测到了，但得克萨斯州着实让我吃惊。我没想到得州会以那种方式翻盘。也许我最近去那个州的次数不够多，但那确实让人震惊。

是的。是的。那么谈到经济中的AI，你们两位都谈到过，你们强烈反对比如在某个时间点实现两位数GDP增长的观点，你们的看法要清醒得多：嘿，它对消费者将产生巨大的影响；它会改变很多事情，但正如你几分钟前所说，GDP增长可能会比我们预期的要更寻常。但在探究原因之前，你能否解释一下，需要满足什么条件，或者说这两种不同的世界是什么样子的？一个是GDP增长如我们刚才所说较为寻常的世界，另一个是它实际上达到两位数增长的世界。亚历克斯，你刚才也稍微提及了这一点，能否为我描绘一下那个世界：如果它真的对经济产生巨大影响，会是什么样子？
<details><summary>Original English</summary>
>> Well, most of it I expected and indeed predicted, but Texas truly surprised me. I didn't think Texas would flip the way it did. and maybe I just haven't been to the state enough lately, but that was a shock.

Yeah. Yeah. So, AI in the economy, you you both talked about how, you know, you push back strongly against the idea of say, you know, double digit GDP growth at at some point due to your far more sober that hey, it will be tremendously impactful for uh for consumers. Um it it it will change a lot of things but uh GDP growth as you said you a few minutes ago it might be more normal than than we might expect. But before getting why that is can you explain what would need to be true for for or what are the two different worlds look like? one in which GDP growth is what we just said a bit more normal you know and another in which it actually becomes double digit and Alex you were alluding to it a little bit like paint that world to me of what it looks like if it's actually having you know massive impact on the economy
</details>

### 奇点式增长的模型条件与瓶颈

>> 有一篇非常出色的论文，准确概述了实现这种奇点式增长所需要满足的条件，作者是本·琼斯（Ben Jones）、查德·琼斯（Chad Jones），我相信阿吉翁（Aghion，原文作Aion）也是那篇论文的合著者。基本上，你需要满足一系列相当苛刻的“刀锋条件”（knife edge conditions）。尤其是最核心的一点：基本上不能存在真正的瓶颈。而绝不能存在的主要瓶颈就是想法生产函数。也就是说，想法不能出现报酬递减。所以基本上，你必须从过去那种世界——即你取得了一项技术突破，然后这项技术突破的边际报酬递减——转变为从该项技术突破开始催生越来越多的技术突破。因此，你需要更少的资源，同时获得越来越多的技术，并利用这些技术获得越来越多的产出。这样一来，你基本上拥有的是报酬递增而非报酬递减。

在模型中你实际上可以估算这个参数。如果它大于1，你就处在这种两位数增长的世界中。如果它小于1，你就处在标准的边际报酬递减、个位数增长的世界中。如果你看一下迄今为止的数据，包括类似各种测度报告（meter report）以及现有的数据，拿这些数据去估算该参数，它显然是小于1的。

这种情况可能会改变，有些人说它必然会改变。当你实现完整的RSI（递归自我改进）闭环时，这正是将被改变的东西。但就目前而言，你需要越来越多的资源，才能从这些模型中挤出越来越多的智能。
<details><summary>Original English</summary>
>> there's a beautiful paper out there uh that outlines exactly the conditions you need for for for this like singularity type growth by uh by Ben Ben Jones Chad Jones I believe Aion is on that that paper as well and essentially what you need is a bunch of pretty knife edge conditions to to to be met. Particularly the main one is essentially no real bottlenecks. Um and the main bottleneck that should can't exist is the idea production function. So you can't get decreasing returns to ideas. So basically you go from like the old world where you have this technological breakthrough and then you kind of have decreasing returns to that technological breakthrough. from that technological breakthrough to start creating more and more technological breakthroughs. So you need less resources while getting more and more technology and more and more production out of that technology. And so you you basically have increasing returns rather than decreasing returns.

And this is the the you can actually estimate this parameter in the model. And if it's greater than one, you're in this like double-digit growth world. If it's less than one, you're in the standard kind of like diminishing returns singledigit growth world. And if you look at the data so far, including kind of the meter report, the data that's out there, and you take that data and you estimate this parameter, it is decidedly less than one.

So this could change and some people say it will change. And when you get the full RSI loop, this is exactly what that's going to change. But right now, you need increasingly more resources in order to ek out increasingly more intelligence out of these models.
</details>

>> 我想补充一点，你可以看看那些增长率极高的案例。不久前，加纳（Gana）在一年的时间里增长了40%。这很惊人。但那是一个只卖一种东西——石油——的小地方。在80年代有一段短暂时期，美国经济增速超过了8%。但那是走出深度衰退的结果。在大流行病之后、在重大战争之后，你可能会迎来暂时性的高增长率。因此，如果美国在某些方面搞砸了，或者我们经历了另一场大流行病、某种可怕的战争或某些其他怪异事件，而这又叠加了原本可能给我们带来3%到4%增幅的AI驱动的增长爆发，那么，我们能否在某一年达到10%的增速？我会说可能。但我会下重注赌它不会发生，而且这种效应也将是暂时的，并且很大一部分将来自于走出衰退、战争或大流行病。但这是另一种思考方式，与亚历克斯所说的完全一致。

如果机器人技术崛起，你的看法是否还会类似，还是说因为那对现实世界、实体经济的影响更为直接？
<details><summary>Original English</summary>
>> I would add to that, you can look at cases where growth has been very high. So, not long ago, Gana grew 40% in a year. That's crazy. But it's a tiny place selling one thing, oil. There's a brief period in the 80s where the US is growing over 8%. But that's coming out of a deep recession. after pandemics, after major wars, you can have temporarily high rates of growth. So if the US were to screw up in some way or we had another pandemic, some kind of terrible war, some other weird event, and that combined with a burst of AIdriven growth that might have given us 3 to 4%. Like could we for a year get to 10%, I'll say yes. I'd bet heavily against it and the effect would be temporary and a lot of it would come from getting out of the recession, war or pandemic. But that's another way to think about it fully consistent with what Alex was saying.

And if robotics emerge, would that would you have a similar view or because that, you know, is is impacting more the the real world the real economy?
</details>

>> 嗯，我认为那很可能会相对缓慢地到来。看看在华盛顿特区落地Waymo（原文作Whimo）花了多长时间。我们现在还没做到。而那还是一种相当简单的机器人。就只是前进、后退和转弯。如果你看一下，机器人类公司的估值现在处于什么水平？虽然比过去高得多，很难估算，但你并没有看到它们直接蹿升为万亿美元级的企业。我的意思是，你可以把特斯拉算作某种机器人公司，但市场数据表明，你知道，它会实现，并且正在取得良好进展，但绝不会在三四年后就给我们带来20%的增长。不会的。
<details><summary>Original English</summary>
>> Well, I think that would likely come relatively slowly. Look at how long it takes to get a Whimo in Washington DC. We're still not there. And that's a pretty simple kind of robot. There's like forwards, backwards, and turns. And if you look, well, what are the valuations of robotic companies at? Way higher than it had been. Hard to estimate, but you don't just see them popping into trillion dollar companies. I mean, you could count Tesla as a kind of robotics company, but the market data suggests, you know, it will happen. and it's making good progress but not going to give us 20% growth like three or four years from now. No.
</details>

>> 对，对。那么，那些最聪明的人——你知道，那些对这种失控式爆发增长最坚定的信奉者，比如德瓦克什（Doresh）、利奥波德（Leopolds），你知道，我们那些相信这一点的朋友们。你认为他们的不同思考点在哪里？是他们对技术发展的速度持有不同的看法吗？还是他们认为技术会在某种程度上突破其中的某些瓶颈？或者，我们能否站在对方立场做个最强阐释（steelman）？
<details><summary>Original English</summary>
>> Right. Right. The and so the smartest people who are you know the biggest believers in in sort of this runaway growth uh you know Doresh Leopolds you know are our are friends on on who believe who believe that. What do you think they think differently? Is it that they um have a different belief on the speed of of technology? Is it that they uh believe that it will um sort of overcome some of these bottlenecks? Or would can we steal me on the other side?
</details>

>> 我认为——泰勒请随时补充——我认为这个论点……我在这里要讲得稍微偏技术性一点。这关乎某种被称为位似偏好（homothetic preferences）或非位似偏好（non-homothetic preferences）的概念。基本上，它的含义是：如果你看看过去被自动化的那些事物，最终的结果是被自动化的东西对经济增长的贡献反而变小了。假设你有一百万台机器人——我们把机器人技术代入进来——它们生产的东西因为价格变得更便宜，讽刺的是，它们生产的东西在整个经济中所占的份额反而变小了，因此它们对增长的贡献也变小了。所以，如果你拥有非位似偏好——也就是这种情况——你
<details><summary>Original English</summary>
>> I I think and Tyler please chime in. I think I think the argument I'm going to get a bit technical here. Um it's about having something called homothetic or non-homothetic preferences. And basically there's a what that means is that if you look at kind of things that get automated in the past what ends up happening is the thing that gets automated contributes less to growth. So let's say you have a million robots let's bring robotics the thing that they're making because the price it becomes cheaper. The thing that they're making ironically becomes a smaller part of the economy and so they contribute less to growth. And so if you have non-homothetic preferences, which is this, you
</details>

<!-- chunk 3/8 -->

你知道，有一篇非常出色的论文利用了200年的数据来估算这种……这些偏好。最终发生的情况是，比方说你实现了广泛的自动化。人们……经济中对增长贡献的价值会转移到瓶颈环节。这只是增长衡量方式中一个令人无奈的特点。因此，增长最慢的环节对GDP的贡献反而会最大。这就是为什么会出现这种效应。
<details><summary>Original English</summary>
know, there was a really nice paper estimating this uh uh these preferences using, you know, 200 years of data. What ends up happening is that let's say you have broad automation. People just people the value in the economy of what contributes to growth moves to the bottlenecks. That's just an inconvenient part of how growth is measured. And so the thing that's growing least will be contributing most to GDP. And that's why you get these sort of effects.
</details>

>> 我同意所有这些，但我还要加上一个更具社会学视角的因素。就我而言，而且我怀疑亚历克斯也是如此，在我们脑海中最生动鲜活的，是人类历史的漫长跋涉、以往的增长历程、几个世纪的GDP数据和生产率数据。而我认为，对Dorcash、Leopold以及许多其他人来说，情感上最突出的可能是在湾区进行的交流，那些对话中确实包含真实信息。但当你问到那个重大问题——依靠哪种情感上的显著记忆能做出更好的预测时——比起他们一直吸收的东西，我会选择我和亚历克斯脑子里装的这些东西。不过当然，你知道，他们会站在相反的立场。
<details><summary>Original English</summary>
>> I agree with all that, but I would add a more sociological element. In my case, and I suspect Alex is, what is emotionally vivid in our minds is the long slog of human history, previous growth episodes, centuries of GDP data, productivity data. What I think is emotionally most salient probably for Dorcash Leopold and many others is conversations they have in the Bay Area which have real information. But when you ask the big question, you know, with which emotional salience will you make better predictions, I would opt for what Alex and I have stuffed our heads with over what they embibe all the time. But of course, you know, they would take the other side of that.
</details>

>> 是的。所以基本上我们想说的是，当你回顾过去几百年，从电力到互联网以及介于二者之间的一切突破性技术，它们基本上都没有带来失控般的飞速增长；或者即使带来了，也是因为基数较小，或者是战后之类的原因。我确实认为这次可能会比那些更快，但仍然……[清嗓子]
<details><summary>Original English</summary>
>> Yeah. So basically what we're saying is when you look at the last few hundred years the the breakthrough technologies from electricity to uh sort of you know the internet to you know uh everything in between they haven't led to runaway growth basically or if they did it was because of sort of a you know it was a small base or uh you know after a war or something like this. I do think this will likely be quicker than those but still [clears throat]
</details>

>> 你能体会到那些瓶颈，不论是工业革命、科学革命的历史，还是电力的推行应用——美国国税局（IRS）现在还在用传真机，诸如此类。试试用用教育科技软件，我一直在用，简直是一场噩梦，它们甚至都还没达到十年前应有的水平。
<details><summary>Original English</summary>
>> you you have a sense of the bottlenecks whether it's the industrial revolution history of the scientific revolution implementation of electricity uh the IRS still uses fax fax machines and so on and so on try using edte software which I do all the time it's a nightmare they're not even up to you know how things should have been 10 years ago
</details>

是的。
<details><summary>Original English</summary>
Yeah.
</details>

>> 那并不是——
<details><summary>Original English</summary>
>> And that's not
</details>

>> 并不是监管本身不是问题。它确实是个问题，但单纯的惰性就很难克服。我们经济中有很大一部分是政府、非营利组织，或者是医疗领域受到高度监管的部分、高等教育、普通基础教育。当你真正体验过这些领域的运作方式后，你可能会说，比如美国经济的40%就是一场噩梦。在欧洲，这一比例可能更高，比如在法国；出于其他原因，那些部门可能不得不保持这种状态，但这仍然是一剂强烈的清醒剂：并非所有事物都像初创公司那样。
<details><summary>Original English</summary>
>> that it's not regulation is not the problem. It's a problem, but just inertia is difficult to overcome. And so much of our economy, it's government, it's nonprofits, it can be highly regulated parts of the health care sector, higher red, general schooling. When you actually have experience with how those work, you could say like I don't know 40% of the US economy is a kind of nightmare. In Europe, it could be higher. like in France and I those sectors might need to be that way for other reasons but still it it's a big dose of realism that not everything is like startups.
</details>

### 衡量AI发展的指标与GDP的局限

是的。假设总统委托你们两位制定一套指标，来判定AI是否正在带动我们国家的繁荣——广义上的繁荣。显然这是一个非常宏大的问题，但是GDP会是你们考虑的主要指标之一吗？比如我们是否应该期望它对GDP产生重大影响，或者有哪些指标是你们会考虑的？
<details><summary>Original English</summary>
Yeah. Let's say you were both tasked by the the the president to come up with a set of metrics that determine whether AI is um you know leading to our country's flourishing you know broadly defined um obviously that's a very big question um but what is GDP one of the main metrics you would think about like should we be aspiring for it to have a a big impact on on GDP or what are some of the metrics you you would you would consider?
</details>

是的，我的意思是，这确实是一个非常重要的问题。所以，我认为在开始之前我还想补充一点，那就是我认为泰勒和我与旧金山关于模型能力等方面的共识并没有真正的分歧。很多人听到泰勒和我，或者像我们这样的人发言，就会觉得：“哦，你们看衰AGI之类的事物。”绝对不是这样。更多的是关于它如何影响经济以及实体经济的结构。因此，深入思考我们可以使用哪些衡量指标时，我认为从历史上看，GDP一直是衡量人类福祉和繁荣的一个非常好的追踪指标。它与国内生产总值的吻合度相当高。但Eric Byon、Avi Kohas等人一直在研究的一个现象是，技术实际上已经开始引入这种差距，即技术创造的很多产品基本上是免费的。所以他们考虑了数字娱乐和数字产品之类的东西，然后他们提出了一个叫做GDP……或者是GDP……抱歉我把首字母缩写给忘了。但它本质上是以GDP为基础，然后用一种基于调查的衡量方式对其进行修正，以实际评估其他未必定价的产品，或者由于自动化而变得廉价甚至免费的产品，这些产品数量的增加在多大程度上提升了人类福祉。因为你可以设想这样一个世界：你仍然处于3%到5%这样的GDP增长区间（这已经处于增长的高位了），
<details><summary>Original English</summary>
Yeah, I mean, so this this is a really important question. So, I think the other thing that I would add before even starting is like I don't think Tyler and I really disagree with like the San Francisco consensus on like the capabilities. Like I think, you know, I I I don't this a lot of people hear Tyler and I or people like us talk and they're like, "Oh, you're bearish on AGI or something like that." That's absolutely not it. It's more about how that affects the economy and the structure of the real economy. And so thinking through like what measures we can be using, I think um GDP historically has been a really good tracker of uh of you know how basically human welfare and flourishing. It tracks pretty well with the gross gross uh gross domestic product. But the what Eric Byon, Avi Kohas and others have have been kind of studying is the fact that technology has actually started to introduce this sort of wedge where a lot of the products that technology creates are basically free. And so they they think about um the sort of like digital entertainment and digital products and then they have something called GDP which is um uh or GDP. I forgot the acronym. I'm sorry about that. Uh but it's essentially a you take GDP and then you amend it with a kind of a survey based measure to actually see how much other products that are not necessarily priced or products that have become cheap or even free uh because of automation how much the increased amount of those products is adding to human welfare because you could see a world where you're still kind of like in this four to you know 3 to 5% GDP range which is already on the high side of the growth
</details>

但你所处的这个世界实际上真正走向了繁荣。你该如何捕捉到这一点？我认为捕捉它的方法就是通过这些替代性衡量指标。
<details><summary>Original English</summary>
But you you have a world that's actually truly flourishing. Like how do you pick that up? And I think the way to pick it up is through these alternative measures.
</details>

>> 寿命延长效应很可能会被证明非常重要。举例来说，埃里克，假设你活到了120岁。我觉得我是活不到那个岁数了。这会以复杂的方式提振GDP，并以更加复杂的方式可能提振人均GDP。但你获得的那些额外寿命是独立于GDP之外的事物，而经济学可以对这些寿命年份进行估值，这也是修正GDP可能会变得更加重要的另一条途径。但就像亚历克斯所说，随着AI的进步，随着时间的推移，GDP的准确性会有所下降，我们将需要对其进行修正和改进。但在短期内，它并不是一个那么差的指标。我常说，GDP是现存所有统计数据中最被低估的一项。
<details><summary>Original English</summary>
>> The longevity effects could well prove important. So Eric, say you live to 120. I don't think I'm going to make it. Uh that will in complicated ways boost GDP and even more complicated ways possibly boost per capita GDP. But it is something distinct from GDP that you get all those extra years and economics can value those years and that's another way in which it may become more important to revise GDP. But I you know as Alex said GDP will become somewhat less accurate over time as AI progresses and we'll need to revise and improve it. But in the short run it's just not that bad a measure. I like to say GDP the most underrated stat statistic that there is.
</details>

### 原子世界与比特世界的进展

是的。在2010年代，彼得·蒂尔（Peter Thiel）曾著名地痛惜原子世界相对于比特世界缺乏进展。但10年、15年后的今天，我们有了自动驾驶汽车，有了早期的飞行汽车，我们有了重要的……你知道，现在最大的公司都是硬件公司了，比如英伟达、SpaceX、特斯拉。泰勒，你是否会说这在很大程度上已经不再是一个令人担忧的问题了？或者10年后你会如何反思这一点？
<details><summary>Original English</summary>
Yeah. In in the in the 2010s, Peter Thiel, you know, famously uh decrieded sort of the lack of progress in atoms relative to to bits. Um but here we are, you know, 10 years, 15 years later, and we've got uh you know, self-driving cars. We've, you know, early flying cars. Uh we we've got, you know, major, you know, uh you know, the biggest companies are now hardware companies. Uh you know, Nvidia, uh SpaceX, Tesla. Tyler, would you go so far as to say that um you know that that isn't a concern as much anymore? Or how would you reflect on that 10 years later?
</details>

>> 原子世界终将取得突破。我几乎敢肯定会突破，但我们现在依然还没真正拥有它们。比如无人驾驶汽车对实际人类福祉的贡献微乎其微。它最大的贡献在于好玩，你可以告诉朋友“我坐过Waymo了”。它其实并没有比Uber更好。对我来说甚至还稍差一点，因为它们严格按限速行驶。它有一种科幻般的趣味。美国大部分地区仍然没有这项服务。欧洲就更别提了。所以，我们依然还没走到那一步。这就是令人惊叹之处。这也回到了一点：机器人技术的发展同样会很缓慢。
<details><summary>Original English</summary>
>> The atoms will break through. I would say almost for sure, but we still don't have them. Like the contribution of driverless cars to actual human welfare is tiny. Like the biggest contribution is that it's fun and you can tell your friends I was in a Whimo. It's not really better than an Uber. For me, it's a little worse because they go by the speed limit. It's fun in a science fiction kind of way. Most of America still doesn't have it. Europe, forget about it. So, we're still not there. That's the amazing thing. And it gets back to robotics also will be slow.
</details>

>> 是的。我想我10年前问过你，大停滞什么时候才会结束？我记得你的回答大致是说，当我们拥有自动驾驶汽车的时候——我记不清当时是指部署落地，还是达到某种普及程度了——但你现在还这么认为吗？
<details><summary>Original English</summary>
>> Yeah. I think I asked you 10 years ago, when would the great stagnation be over? And I I think you said something along along the lines of when we have self-driving cars, I can't remember if it was deployed or you know, you know how sort of diffused it was, but you still believe that?
</details>

>> 差不多还是这么认为。但这取决于程度，它们显然是行得通的，而且新款特斯拉相当惊艳。我最近坐过几次亚历克斯·塔巴罗克（Alex Tabarrok）的车，但就市场渗透率而言，我虽然不知道确切数字，但同样微乎其微。
<details><summary>Original English</summary>
>> More or less. But that's a matter of degree and they clearly work and the new Tesla is pretty phenomenal. I've been in Alex Stabberox lately a few times, but in terms of market penetration, I don't know the numbers, but again, it's tiny.
</details>

### 智能体集群与委托-代理问题

>> 让我们回到另一个话题。亚历克斯最近写了一篇相关的论文，但我先从你开始问起，泰勒。关于智能体集群的话题，也就是Hugging Face事件。这件事有没有让你对可能实现的事情更新看法，或者让你对某些事情产生担忧，或者对那里发生的事情有什么反应吗？
<details><summary>Original English</summary>
>> Let's go back to a different topic. Uh, Alex recently wrote wrote a related paper about, but I'll start with you, Tyler. The agent swarm uh topic, sort of the hugging face incident. Did that update your views in terms of what's what's possible or make you uh get concerned about something or or any any reactions to what happened there?
</details>

>> 这几乎没有改变我的看法。我也很好奇亚历克斯是否认同这个观点。但作为一名经济学家，你首先想到的就是委托-代理理论；除非条件极为严苛，否则无论委托人试图拟定什么样的契约，都无法很好地控制代理人。因此，当我们用AI重现这一结果时，嗯，这很有趣，但我并不感到震惊。解决办法始终在于制衡，以及我们在政治领域可能称之为分权的机制，而不是指望拥有完美的对齐。所以同样，如果你从经济学家的角度来看这个问题，所有关于对齐的忧虑——当然，人们确实应该在这方面投入大量工作——但归根结底，你会觉得：“嘿，我
<details><summary>Original English</summary>
>> It didn't update my views much at all. And I'm curious to see if Alex agrees with this perspective. But as an economist, you think first and foremost in terms of principal agent theory and unless the conditions are very restrictive. The principal just can't control the agent that well no matter what contract they try to write. So when we replicate that result with AIS, well, it's interesting, but I'm not very shocked. The answer was always going to be checks and balances and what we might call separation of powers in the political realm. Not you have perfect alignment. So again, if you come at this from the economist's point of view, all the hand ringing about alignment, like yes, people should work on that a lot, but at the end of the day, you're like, "Hey, I
</details>

<!-- chunk 4/8 -->

### 机制设计与 AI 对齐

……17岁时就明白了这个道理。”比如，好吧，这确实是个真问题。但亚历克斯（Alex），你怎么看？

<details><summary>Original English</summary>
learned that when I was 17."

Like, okay, it's a real problem. But

Alex, what's your thought on that?
</details>

>> 我很遗憾自己在17岁时没明白这个道理。嗯，我觉得我们再次达成了共识。嗯，我认为关于这个问题存在几种不同的视角，归根结底，这是一个关于如何最好地让 AI 为人类服务的问题，对吧？这就是问题所在，这就是对齐的问题。一种思考方式是让模型本身与类似“宪章”之类的东西对齐，即模型在个体层面上以这种方式对齐，因为它们与部署它们的人类拥有相同的偏好。嗯，但另一种视角，也就是泰勒（Tyler）刚才提到的，就像是你去对齐事物。你几乎不在乎这些智能体自身的偏好是什么。它们在个体层面上可能极不对齐，但你可以在它们周围建立一种机制，使激励机制促使智能体的行为表现出对齐。这就是经济学中的机制设计视角：作为委托人，我不一定需要代理人发自内心地想帮助我，代理人可能一心只想利己、为所欲为。而机制设计的全部研究内容，就是如何建立制衡体系，以确保代理人依然在为委托人的利益工作。我认为实验室内部和外部不断涌现的研究表明，很多人都在朝着这个方向思考，我们确实需要采取机制设计的视角。正如泰勒所说，我对发生的事情并不感到震惊。

<details><summary>Original English</summary>
>> I unfortunately did not learn that when I was 17. Um, I think we once again agree. Um I think you know there's like these s sort of different perspectives on this issue of um how do you best ultimately it's a question about like how do you best get AI to be in the service of humanity right that's that's the question that's the question of alignment and one kind of way of thinking about it is to get the models themselves aligned with like something like a constitution that the models at an individual level are aligned in this way because they have the same preferences as the human beings that are that are deploying them. Um, but another perspective which is what Tyler mentioned is like you align things. You don't you don't almost like don't even care what the preferences of these agents are. They could be extremely individually misaligned but you can create a mechanism around them where the incentives are such that the agent behaves in an aligned way. And this is the mechanism design perspective in economics where like as a principle I don't need the agent to to want to help me necessarily the agent could really really want to just help themselves and do whatever they want. And the whole study of mechanism design is how do you create the system of checks and balances in order for the agent to still be working in the principal's a interest. And I think that's that is I from the research that I've been seeing coming out of of the labs both like internally externally like a lot of people are thinking in this direction that we really need to take a mechanism design perspective and as Tyler said like I wasn't you know shocked by what happened.
</details>

>> 我和弗吉尼亚州州长并不一致，但这届州政府治理得相当不错，我在这里生活得很开心。嗯。

<details><summary>Original English</summary>
>> I'm not aligned with the governor of Virginia but it's a pretty well-run state and I'm happy here. Mhm.
</details>

>> 我们有两党竞争，某种程度上——

<details><summary>Original English</summary>
>> We have two party competition sort of
</details>

>> 而且行之有效。

<details><summary>Original English</summary>
>> and it works.
</details>

>> 你认为 Anthropic 或 OpenAI 或其中一些公司，或者说整个 AI 安全社群思考对齐的方式，你认为这种思考方式是不是不太对，或者在某种意义上有些混乱？

<details><summary>Original English</summary>
>> Do you think the way that Anthropic or Open AI or some of these companies or just the sort of AI safety community thinks about alignment, do you think that is sort of not the right way to think about it or or confused in some sense?
</details>

>> 这么说吧，他们怎么思考是一回事，怎么对外表述又是另一回事。而他们对外谈论的方式受 Twitter 的影响太深了，Twitter 上的言论可能相当歇斯底里。但我认为，他们实际上的思考方式要比外界看起来理性得多。所以，我不会发表什么“哦，我们必须彻底改造他们”之类的高谈阔论。我认为他们相当务实。他们是企业，接下来还要进行 IPO，他们不想惹来太多官司，也不想面临过度监管。我们已经有了制衡机制——需要明确的是，并非所有机制都是好的。但现实情况是，我们见过的实际问题，比如黑客攻击，大部分甚至可能全部都来自邪恶的人类个体，而 AI 只是在执行人类给它的指令，这确实是个巨大的问题。但从某种意义上说，这恰恰是对齐的——邪恶的人类说“去做这个”，AI 就照做了，而损失正是由此产生的。

<details><summary>Original English</summary>
>> Well, there's how they think about it and how they talk about it. And how they talk about it is way too shaped by Twitter, which can be quite hysterical. How they actually think about it, I believe, is a lot more reasonable than how it ever looks from the outside. So, I don't have some big speech about, oh, we've got to totally reform them. I think they're pretty practical. They're companies. They have IPOs coming up. They don't want to get sued too much. They don't want to be overregulated. We already have checks and balances. Not all of them good to be clear. Uh but the reality is the actual problems we've seen, you know, the hacks, they're mostly coming or maybe entirely coming from evil human individuals where the AIs are doing what the humans told it to do and that is a huge problem. Uh but that is a kind of well we have the alignment the evil human says do this and the AI does this and that's where the costs are coming from.
</details>

>> 是的。有些人把这做对比，认为对齐在某种程度上是为了给员工看的。这有点像……或者说泛指安全领域，就像在2020年、2021年以及那段时间前后，社会各界对社会议题的关注度更高，因此 CEO 们不得不说一些这样的话来安抚员工群体。其中有些人是真正的信徒，有些则不是。同样，在 AI 安全领域也存在很多担忧，所以有人做出这种对比，认为 CEO 们并没有像他们所表现出来的那样笃信这些。

<details><summary>Original English</summary>
>> Yes. Some people make the comparison that alignment is in some ways is for the employees. It's sort of like um or safety in general is like in the in 2020 2021 and and sort of around that time there was you know sort of more awareness around social issues and so CEOs had to sort of say these uh say these things to please their employee base and um you know some of them were true believers and some of them weren't and and similarly perhaps around AI safety there's a lot of concern and so some people are making that uh that comparison that that the CEOs aren't as true believers as as they may be uh indicating
</details>

>> 这些公司内部同样存在制衡机制。这也是这些公司运转良好的部分原因：你最终必须推进那些真正管用的东西，这与外界人云亦云的论调有所不同。公司内部存在一套筛选和淘汰机制，大家都想升职或拿奖金，想做切实可行的事情。我想说的是，最终的发展结果会比在 Twitter 上听起来要好得多。

<details><summary>Original English</summary>
>> there's checks and balances in these companies as well. It's partly why the companies work well that you have to actually end up pushing through things that will work and that's somewhat different than what everyone is saying and there's a winnowing and selection set of mechanisms within the company and people want promotions or bonuses and they want to do things that can work and uh again it will end up going better than how it will sound on Twitter I would say.
</details>

>> 对。我认为 Hugging Face 就是一个绝佳的例子，如果你去剖析究竟发生了什么，那不过是一连串的人为错误叠加在一起，对吧？发生一次事故是件好事——我这里的“好事”要打上引号——但它并没有酿成巨大的灾难，对吧？而且它暴露了智能体面临的很多不良激励机制。所以你看各家公司如何应对 Hugging Face 事件：从中吸取教训，并创造更好的环境。因此，任何事情的发展都不会是一帆风顺的，过程中总会有起有落，但整体趋势是积极向上的。

<details><summary>Original English</summary>
>> Yeah. And I think like hugging face is like a perfect example of like if you unpack like what what actually happened, it's just a bunch of human error on top of human error, right? And so like it's great to have an incident. I mean great in quotes, but it it didn't like cause a massive disaster, right? And it exposed a lot of like you know uh broken incentives for the agents. So it's it was you know you see how you know the the companies have reacted to the hugging face by learning from it and creating better environments and so this is nothing is smooth. It'll be kind of a little bit down a little bit up but you know the slope is positive.
</details>

>> 我是说有些人……比如保罗·克里斯蒂亚诺（Paul Christiano），我认为他在演讲中曾说，一年或两年后最有可能的死因会是与 AI 相关的死亡。这对你来说听起来有点耸人听闻。坚决不同意。

<details><summary>Original English</summary>
>> The uh I mean some people you know Paul Cristiano I think said in his speech he's like the most likely cause of death you know a year from now or two years from now will be an AI related death. Um and that that to you sounds sort of you know historical. strong disagree.
</details>

### 组织智能与经济影响

>> 是的。是的。亚历克斯，让我们深入探讨一下你的论文。你能不能分享一下你们得出的部分研究结论，以及目前依然存在的疑问？

<details><summary>Original English</summary>
>> Yeah. Yeah. Um Alex, let's go deeper on on your paper. Why don't you share some of the the findings that you that you had and some of the questions that that still remain.
</details>

>> 好的。这篇论文，我想你说的是关于“组织智能”的那篇论文。对，我和安德鲁·柯（Andrew Co）以及我的同事 Shane Le 合著的。那篇论文的核心思想，始于这样一个谜题：众所周知，AI 在特定维度上的能力正变得非常强大，但我们至今仍未看到任何显而易见的经济转型。

我们首先提出的切入点是，人们一直聚焦于个体智能体的基准测试，却没有去思考这些智能体在经济中真正的竞争对手是什么——在经济体系中，相关的竞争单元并不是单个智能体，而是组织。

在历史上，组织由于“李嘉图比较优势”这一概念，一直被称为一种超级智能形式。简单来说，如果你有一堆工作，做这项工作的并不是平均水平的人，而是最适合它的人。因此，一个组织所展现出的智能包络面，远远优于在人群中取平均值的水平。所以，这些 AI 智能体本质上是在与人类组织或人类团队的形式进行竞争。因此，你不应该把单个智能体层面的基准测试去跟某个人做某件事的能力做对比，而应该跨越整个我们所谓的“马赛克智能”来进行考量。

所以我们接着深入探讨，能力提升究竟会在均衡状态下如何影响经济。这是一篇正式的理论论文，我们探讨了不同层次的智能水平。我们从“最小 AGI”切入，即 AI 模型在每个单一维度上都达到了人类平均水平。针对最小 AGI，我们证明了即使达到这一节点，它也不会对经济产生巨大影响，原因还是在于组织代表的并不是人类的平均能力，它们比那更强。因此你将开始看到的实际上是工资的变化，因为生产变得更便宜，进而会影响人类的工资。

所以我们证明了，要实现真正的经济转型，仅仅靠能力（即在特定任务上的表现）发生改变是不够的。关键在于这些智能体相互协同的能力。如果你看看 Hugging Face，甚至看看千禧年大奖难题的解法，都有这种“智能体群”的概念，对吧？但如果你仔细剖析，这些智能体在协同方面依然非常糟糕。它们根本谈不上协同，大多只是在进行并行处理。如果专门针对协同能力进行基准测试，你其实会发现，一个智能体单独工作往往比两个智能体分工合作表现更好，哪怕它们之间可以通信。然而，如果你把同样的任务交给两个人，他们实际上会进行劳动分工，他们会沟通交流并——

<details><summary>Original English</summary>
>> Yeah. So, like the the the paper I believe are you're talking about the uh uh organizing intelligence paper. Yeah. With with Andrew Co and my my my uh colleague Shane Le. Um and basically the the idea of that paper is that it starts with this kind of puzzle that you know AI is becoming very capable on particular dimensions but we don't see still see any like visible economic transformation and the first kind of thing that we start with is that there's been this focus on individual agent benchmarks without kind of thinking about what those agents are actually competing with in the economy where the thing that's the competitive the relevant competitive unit is not the agent it's the organization.

And the organization in uh historically has been referred to as a form of super intelligence because of this concept called Ricardian comparative advantage. So basically if you have a bunch of jobs the person who does the job is not the average person, it's the person who's best suited for it. So like the envelope of the intelligence in an organization is way better than if you kind of average across the population. And so these the AI agents are basically competing against forms of human organizations or teams of humans. And so you shouldn't compare a ben individual level benchmark to how well a human does something. It should be across the entire kind of uh what we call mosaic intelligence. So the thing that we so then we kind of start layering on like what sort of how do capability improvements will actually affect the economy and equilibrium. So this is a formal theoretical paper and we look at different levels of intelligence. So we start with minimal AGI where the AI models are as good as average human capability on every single dimension. So minimal AGI and we show that even when you get to this point you're not going to have a huge impact on the economy uh because again because the organizations are not the average human ability. They're better than that. And so what you're going to start seeing is actually wages change uh because you know production becomes cheaper and so that's going to affect human wages. And so what we show is that what you actually need for real economic transformation is not just competence like ability on particular tasks to to change. It's the ability of these agents to coordinate with one another. If you look at hugging face and even like how the the solutions to the millennium stro uh millennium problems, there's this idea of agentic swarms, right? But if you unpack it, these agents are still very bad at coordinating. They're not coordinating. They're just do they're mostly just doing parallel processing. And if you have benchmarks specifically on coordination, you could actually show that one agent does better than two agents splitting the work even if they can communicate. Whereas if you give the same thing to a per two people, they actually divi they uh have division of labor. They communicate and
</details>

<!-- chunk 5/8 -->

他们表现得要比一个拥有双倍资源的人好得多。所以智能体在协同方面目前依然很差。但如果它们在协同方面变得更好，你基本上就可以打破科斯上限对企业规模的限制，让非常非常不同的企业形态涌现出来。所以基本前提就是，协同——一旦协同变好，企业形态、工资变化、就业变化等可能存在的经济空间，就会发生真正肉眼可见的转变。

<details><summary>Original English</summary>
 they

 do

 way





better

 than

 one

 person

 with

 double

 the





resources.

 So

 the

 agents

 are

 still





pretty

 bad

 at

 coordinating.

 But

 if

 they





get

 better

 at

 coordinating,

 you

 can





basically

 break

 the

 coian

 ceiling

 on





firm

 size

 and

 you

 can

 get

 very

 very





different

 firms

 to

 emerge.

 So

 that's

 the





basic

 premise

 is

 that

 coord

 once





coordination

 becomes

 better

 you

 the





economic

 space

 of

 possibilities

 of

 what





firms

 look

 like

 what

 happens

 to

 wages





what

 happens

 to

 employment

 that's

 when





the

 real

 kind

 of

 visible

 changes

 that





are

 going

 to

 happen
</details>

### 就业影响与协同瓶颈

>> 那么目前解决协同问题的最大瓶颈是什么？

<details><summary>Original English</summary>
>> and

 and

 what's

 the

 biggest

 bottleneck

 to





figuring

 out

 coordination

 at

 the

 moment
</details>

>> 说实话我不知道。嗯，我……（清嗓子）我认为可能很简单，就是它没有被训练进模型里，它不属于训练后阶段的一部分。我其实对此没有任何内幕了解。

<details><summary>Original English</summary>
>> to

 be

 honest

 I

 don't

 know

 um

 I

 I





[clears throat]

 I

 I

 think

 it

 could

 be

 as





simple

 as

 that

 it's

 not

 being

 trained





into

 the

 models

 it's

 it's

 not

 part

 of





post

 training

 I

 I

 actually

 don't

 have





any

 insight

 on

 that.
</details>

>> 好的，我们已经讨论了你们达成共识的一些领域。我想试着找找看有没有观点分歧的地方。也许可以聊聊就业。嗯，Alex，我想你更担心的是转型发生得太快，以至于就业方面可能会出现某些突发情况，还是说，你什么时候来分享一下你的担忧或看法？

嗯，我基本上是在担心这种可能性。同样，我其实在很大程度上同意 Tyler 的看法，即对实体经济的影响方面，事情可能会发展得相当缓慢。但如果出现快速转型，比如说，假如在协同方面取得了突破，我们在那篇论文里指出的就是，如果在协同上有突破，工资和就业就有可能突然发生变化，就经济届时会发生什么而言，会出现类似相变的过程。在那时，仍然会有新的行业和新的潜在机会，但以往由于转型需要相当长时间而在经济中发生的这种重新匹配，就没有机会发生。所以就会出现规模更大的失业群体，并导致某种循环回路，人们在某种程度上因此被劳动力市场边缘化并留下创伤。所以这是我个人的担忧，但是你知道，就这一点而言，这是我所担心的一个情景。至于可能性，那完全是另一回事了。

<details><summary>Original English</summary>
>> Yeah,

 we

 we've

 talked

 about

 some

 areas





where

 you

 agree.

 I'm

 trying

 to

 find

 some





areas

 where

 there's

 some

 difference

 of





opinion.

 May

 maybe

 let's

 try

 employment.





Um

 Alex,

 I

 I

 think

 you're

 you're

 more





worried

 about

 sort

 of

 the

 transition





happening

 so

 fast

 that

 there

 might

 be





some

 something

 sudden

 happen

 on

 the





employment

 side

 or

 when

 do

 you

 share





your

 your

 your

 concerns

 or

 views?

 Um,





I'm

 basically

 worried

 about

 the





potential

 and

 again

 like

 I

 actually





agree

 quite

 a

 bit

 with

 Tyler

 that

 things





things

 are

 potentially

 going

 to

 move





pretty

 slowly

 um

 as

 far

 as

 like

 the





effect

 on

 the

 real

 economy

 but

 if

 there





is

 a

 fast

 transition

 like

 let's

 say





there's

 a

 breakthrough

 in

 coordination





what

 we

 show

 in

 that

 paper

 is

 that

 if





there's

 a

 breakthrough

 in

 coordination





there

 is

 the

 potential

 for

 wages

 and





employment

 to

 suddenly

 there's

 like

 a





phase

 transition

 as

 far

 as

 what

 will





happen

 to

 the

 economy

 in

 that

 case

 there





still

 will

 be

 new

 sectors

 and

 new





potential

 opportunities

 but

 the

 sort

 of





rematching

 that

 we

 have

 in

 the

 economy





that

 you

 know

 because

 of

 transitions

 to





take

 used

 to

 take

 quite

 a

 long

 time

 the





sort

 of

 rematching

 doesn't

 have

 a





opportunity

 to

 happen.

 So

 you

 have

 these





large

 larger

 pools

 of

 unemployment

 and





that

 leads

 to

 kind

 of

 these

 recursive





loops

 where

 people

 kind

 of

 get

 scarred





out

 of

 the

 labor

 market.

 So

 that's

 my

 my





personal

 worry,

 but

 you

 know,

 as

 far

 as





that's

 that's

 a

 scenario

 that

 I'm





worried

 about.

 Likelihood

 is

 is

 kind

 of





a

 different

 story.
</details>

>> 我有一个相关的担忧。我想这与刚才说的差不多，但问题在于现在去招人很难分辨清楚：这个人会擅长使用 AI 吗？

<details><summary>Original English</summary>
>> I

 have

 a

 related

 worry.

 It's

 it's

 close





to

 the

 same

 thing,

 I

 think,

 but

 it's





just

 hard

 to

 tell

 right

 now

 if

 you're





hiring

 someone.

 Will

 the

 person

 be

 good





at

 AI?
</details>

>> 他们过去所需要的技能，我们曾有不完美的指标。比如他们上过康奈尔大学，或者拿了全 A，或者面试表现很好。而现在的技能是，他们的思维是否足够灵活以掌握 AI？你知道，我们常常无从知晓。因此这可能会提高自然失业率，良好的人岗匹配会变得更加困难，搜寻时间会变得更长。我认为这个问题不会永远伴随我们，AI 自身最终会弄清楚这一点，也会出现证明一个人在 AI 方面水平如何的认证。但在转型期，大家都是新手。你可能像科技界的很多人那样在原领域很有威望，但在面对这项非常重要的新技能时，我们全都是新手。嗯。

<details><summary>Original English</summary>
>> The

 skills

 they

 used

 to

 need,

 we

 had





imperfect

 indicators.

 Oh,

 they

 went

 to





Cornell

 or

 they

 got

 all

 A's

 or

 they

 had





a

 good

 interview.

 And

 now

 the

 skill

 will





they

 be

 mentally

 flexible

 enough

 to

 pick





up

 AI





you

 know

 we

 don't

 know

 often

 so

 that





could

 increase

 the

 natural

 rate

 of





unemployment

 match

 good

 matches

 will

 be





harder

 search

 will

 take

 longer

 I

 don't





think

 that

 problem

 will

 be

 with

 us





forever

 eventually

 the

 AIs

 themselves





will

 figure

 it

 out

 and

 there'll

 be





certifications

 for

 how

 good

 a

 person

 is





in

 AI

 but

 in

 the

 transition

 everyone's

 a





novice

 you

 might

 be

 like

 well





established

 the

 way

 a

 lot

 of

 people

 in





in

 the

 tech

 world

 are,

 but

 otherwise





we're

 all

 noviceses





at

 this

 very

 important

 new

 skill.





Mhm.
</details>

>> 那么我想这对……这意味着什么？我想我也很好奇你们如何看待就业、工资这些问题。

<details><summary>Original English</summary>
>> And

 so

 I

 guess

 what

 does

 that

 that

 mean





for

 and

 I

 guess

 I'm

 curious

 how

 you





think

 about

 sort

 of

 employment

 wages





sort

 of

 yeah

 these

 questions
</details>

>> 嗯，招人方面会有一些额外的迟缓，但会出现数量极其庞大的新项目、新工作，所以我其实挺看好的，而且劳动力市场一直表现良好。

但当然，这里会有冲击和转型带来的问题，就像一直以来存在的那样，比如当年的中国冲击和工业革命。因此，我预计会出现一套新的此类问题。其中很多我们甚至还没有弄明白或者还没看到，但它们一定会到来。那是必然的。

智能体在这种几乎平行的经济中与其他智能体进行买卖和交易，在多大程度上会出现爆发式增长？而且数量要多得多，它们是全天候 24/7 运行的，并且它们可以……在智能体成为互联网上主导性的影响或力量的程度上，去思考那会是什么样子、或者不会是什么样子的正确思维模型是什么？

<details><summary>Original English</summary>
>> well

 some

 additional

 slowness

 in

 hiring





people

 but

 there'll

 be

 an

 incredible





number

 of

 new

 projects

 uh

 new

 jobs

 so

 I





I'm

 pretty

 bullish

 actually

 and

 labor





markets

 have

 been

 fine





so

 but

 of

 course

 there'll

 be

 disruptions





and

 transition

 problems

 as

 there

 always





are

 as

 there

 were

 with

 the

 China

 shock





the

 industrial

 rev

 evolution.

 So,

 I





expect

 a

 new

 set

 of

 those.

 A

 bunch

 of





them

 we

 haven't

 even

 figured

 out

 or

 seen





yet,

 but

 they'll

 come.

 Absolutely.





To

 what

 extent

 will

 there

 be

 just

 sort





of

 an

 explosion

 of

 agents

 sort

 of

 buying





transacting

 with

 other

 agents

 in

 this





kind

 of

 like

 almost

 parallel

 economy

 and





you

 know

 there's

 so

 many

 more

 of

 them.





They're

 24/7.

 and

 they

 can

 like

 h

 how

 to





the

 extent

 that

 you

 know

 agents

 become





the

 dominant

 sort

 of

 impact

 uh

 or

 sort





of

 force

 on

 the

 internet

 and

 like

 what





is

 the

 right

 mental

 model

 of

 thinking





about

 what

 that

 will

 look

 like

 or

 what





that

 won't

 look

 like.
</details>

### 智能体经济规模与现实摩擦

>> 我不知道你说的“爆发”是什么意思。如果你问我智能体何时能占到 GDP 的 10%？我认为不会很快。如果它们基本上从 0 上升到 6%，你可以称之为爆发。GDP 的 6% 是极其庞大的。即便是这一点，看起来也不会那么快到来。如果达到 1.5% 左右，我觉得是有可能的，说不好是在五年之内。如果你非要逼我做出猜测的话，你可以把 1.5% 称为爆发。GDP 总量极为庞大，这是经济学的核心洞见之一。GDP 总量非常巨大，非常大。

<details><summary>Original English</summary>
>> I

 don't

 know

 what

 you

 mean

 by

 the

 word





explosion.

 If

 you

 ask

 me

 the

 question





when

 will

 agents

 be

 10%

 of

 GDP?

 I

 don't





think

 it's

 soon.

 Now

 if

 they

 rose

 from





basically

 0ero

 to

 6%





you

 could

 call

 that

 an

 explosion.

 6%

 of





GDP

 is

 enormous.

 Even

 that

 doesn't

 seem





that

 soon.

 If

 it's

 like

 one

 and

 a

 half





percent,

 I

 could

 see

 that

 I

 don't

 know





within

 five

 years.

 Just

 if

 you're

 going





to

 force

 me

 to

 give

 guesses,

 you

 could





call

 one

 and

 a

 half%

 an

 explosion.

 GDP





is

 huge.

 That's

 one

 of

 the

 core

 insights





of

 economics.

 GDP

 is

 huge.

 It's

 huge.
</details>

>> 是的。我是说，即使以我们现有的智能体而言，它们已经具备令人难以置信的能力了，比如装在你手机里的那种消费级产品。但你知道，问题就在这里，现实中存在着完全反直觉的瓶颈：网站是为人类设计的，而且它们各不相同。所以你仍然会遇到这种问题，比如你极其聪明的智能体在帮你订机票时，每一次都给你订紧挨着厕所的座位。每一次都是。然后你就会觉得，下次我不想用智能体了。

<details><summary>Original English</summary>
>> Yeah.

 And

 I

 mean

 like

 even

 with

 the





agents

 that

 we

 have

 now,

 they're

 they're





they're

 already

 incredibly

 capable

 like





the

 the

 the

 sort

 of

 consumer

 grade





things

 that

 live

 on

 your

 phone.

 But

 you





know

 that

 that's

 the

 thing

 like

 there's





just

 completely

 unintuitive

 bottlenecks





out

 there

 like

 the

 websites

 are

 designed





for

 human

 beings

 and

 they're

 all





different.

 And

 so

 you

 know

 you're

 still





getting

 into

 issues

 with

 where

 your





super

 smart

 agent

 is

 like

 booking

 you

 a





flight

 booking

 you

 a

 seat

 right

 next

 to





the

 toilet

 every

 single

 time.

 Every





single

 time.

 And

 then

 you're

 like

 I





don't

 want

 to

 use

 an

 agent

 next

 time.
</details>

>> 还有现实中存在的所有这些规则和干预。我是说，那才是大问题，对吧？比如智能体……企业在网站上花费数十亿美元尝试构建基础的选择架构，目的是向人类推销更多产品，对吧？它们不想……智能体没有同样的心理机制，因此它们不会容易受到这类选择架构的影响。所以这些平台有动力去阻止别家的智能体进入并替人购物。你已经隐约能看到这种情况了。比如你打开 Muse 或类似工具，它无法在亚马逊上帮你购物。嗯……

<details><summary>Original English</summary>
>> Or

 the

 fact

 that

 there's

 all

 of

 this





regulation

 out

 there.

 I

 mean

 that's

 the





big

 one,

 right?

 So

 like

 agents,





companies

 are

 spending

 billions

 of





dollars

 trying

 to

 do

 basic

 choice





architecture

 on

 their

 website

 in

 order





to

 upsell

 humans

 on

 products,

 right?





They

 don't

 want

 to

 agents

 don't

 have

 the





same

 psychology

 and

 so

 they're

 not

 going





to

 be

 prone

 to

 these

 sort

 this

 sort

 of





choice

 architecture.

 So

 these

 platforms





have

 an

 incentive

 not

 to

 allow,

 you





know,

 somebody

 else's

 agent

 to

 go

 in

 and





shop

 for

 them.

 And

 you're

 already

 kind





of

 seeing

 it.

 So

 like

 if

 you

 pull

 up





Muse

 or

 something

 like

 that,

 it

 can't





shop

 on

 Amazon

 for

 you.

 Um,
</details>

>> 我不用智能体来管理我的日历，尽管它们完全可以做，因为我希望自己脑子里清楚每一天要发生什么。而我能记住的唯一方法，就是抽出额外的时间亲自写在日历上。这很愚蠢，这是我的缺点。但我认为这不会消失。智能体就算性能提高 10 倍，不管那代表着什么，我也依然会想要亲自写在我的日历上。这样我就会想，哦，12 月 18 日我要去看一场文艺复兴音乐会。我随口就能说出来。所以在我们如何分配注意力方面，存在着这些奇特的不可分性，而这些往往是某些最大的瓶颈。

回到监管这部分，嗯，T，对于中期选举可能不会导致数据中心无限期停滞这一点，你似乎态度更冷静。我很想了解你对 AI 舆论情绪更宏观的想法。这种负面情绪在多大程度上是真实的——即它会带来实际行动，你知道，我们看到像布卢明顿在一定程度上也试图将使用它定为非法。在这方面，对于该如何看待这背后的政治经济学，你有何见解？

<details><summary>Original English</summary>
>> I

 don't

 use

 agents

 to

 manage

 my





calendar,

 although

 they

 could

 because

 I





want

 to

 know

 mentally

 in

 my

 mind

 what's





coming

 each

 day.

 And

 the

 only

 way

 I

 can





remember

 is

 if

 I

 have

 to

 write

 it

 down





in

 extra

 time

 on

 my

 calendar.

 And

 that's





stupid.

 That's

 my

 flaw.

 But

 I

 don't





think

 it's

 going

 away.

 And

 the

 agents





could

 be

 10

 times

 better,

 whatever

 that





means.

 And

 I'm

 still

 going

 to

 want

 to





write

 it

 on

 my

 calendar.

 So

 I

 think,

 oh,





December

 18th,

 I

 seeing

 a

 Renaissance





music

 concert.

 And

 I

 know

 that

 off

 the





top

 of

 my

 head.

 So

 there

 are

 these

 funny





indivisibilities





and

 how

 we

 allocate

 our

 attention

 but





are

 often

 some

 of

 the

 biggest





bottlenecks.





Going

 back

 to

 the

 regul

 regulation

 part





um

 t

 you

 seem

 more

 sober

 that

 this

 sort





of

 uh

 the

 midterms

 um

 you

 know

 might

 not





lead

 to

 uh

 sort

 of

 uh

 you

 know

 data





centers

 stalling

 indefinitely.

 I'm





curious

 just

 for

 your

 broader

 thoughts





on

 AI

 sentiment.

 how

 much

 of

 the

 uh





negativity

 is

 real

 in

 the

 sense

 that

 it





will

 lead

 to

 you

 know

 we

 saw

 like





Bloomington

 you

 know

 trying

 to

 outlaw





usage

 of

 it

 as

 well

 to

 some

 degree

 like





what

 are

 your

 thoughts

 here

 on

 on

 sort





of

 what's

 uh

 how

 you

 should

 think

 about





the

 political

 economy

 of

 that
</details>

>> 嗯，我们有 50 个州，还有县、有市，甚至还有其他国家。看起来进度会慢一点，但基本还是能推进下去。就连德克萨斯州新州长也已经在退缩了，说类似“嗯，我们只是希望工会参与进来，他们需要支付不错的薪资。你知道，我们现有的项目会继续推进，其他的我们会重新审视”。Josh Shapiro 的口辞非常强硬，但现实却大不相同。所以，这增加了成本，但我认为最终它不会产生那么大影响。但是否会有一批地方坚决说不？大概率会。不过话说回来，我们有 50 个州，我很庆幸有这么多州。呃，也许最终会有 52 个州。（轻哼声）

<details><summary>Original English</summary>
>> well

 we

 have

 50

 states

 there's

 counties





there's

 cities

 there's

 even

 other





countries

 it

 seems

 it

 will

 slow

 down

 a





bit

 but

 still

 basically

 go

 through

 even





the

 te

 the

 new

 Texas

 governor

 is

 already





backtracking





like,

 well,

 we

 just

 want

 the

 labor





unions

 involved.

 They

 need

 to

 pay

 good





wages.

 You

 know,

 the

 projects

 we

 have





now

 will

 go

 ahead.

 The

 others

 we're





going

 to

 look

 at

 again,

 Josh

 Shapiro,





the

 rhetoric

 was

 very

 strong.

 The





reality

 is

 quite

 different.

 So,

 it





raises

 costs,

 but

 I

 don't

 think





ultimately

 it

 will

 matter

 that

 much.

 But





will

 there

 be

 a

 bunch

 of

 places

 that





absolutely

 say

 no?

 Probably.

 But

 again,





50

 states,

 I'm

 glad

 we

 have

 them.

 Uh





maybe

 you'll

 end

 up

 with

 52.





[snorts]
</details>

>> 对。而且我的意思是，紧接着这点来说，我认为这完全取决于具体路径，对吧？这就好比很多事情……一切在某种程度上都是内生的，包括政治经济学。所以你知道，州长们退缩的原因在于，失业率看起来很不错，经济以合理的速度增长，经济层面一切看起来都挺好。所以，比如……

<details><summary>Original English</summary>
>> Yeah.

 And

 I

 mean

 um

 just

 to

 piggyback

 on





that,

 I

 think

 like

 it

 just

 completely





depends

 on

 the

 path,

 right?

 So

 it's

 like





things

 everything's

 kind

 of

 indogenous





including

 political

 economy.

 So

 you

 know





the

 reason

 that

 the

 governors

 are





backtracking

 this

 because

 like





unemployment

 look

 great

 rate

 looks





great.

 The

 economy

 is

 growing

 at

 a





reasonable

 amount.

 Everything

 kind

 of





looks

 fine

 economically.

 So

 like
</details>

<!-- chunk 6/8 -->

这种政治经济层面的反作用并不存在某种工具性的必然理由。但我认为，那些预测极其极端情景的人没有意识到的是，极端情景的开端同时也会是极端政治经济反作用的开端，而这会在内生层面上对事态形成制约。所以，这只会是一个来回博弈的过程。在未来生活的人们看来，最终呈现出的数据会表明，正是由于这种相互交织的影响，事态发展的速度远比人们想象的要慢得多。
<details><summary>Original English</summary>
there's no like instrumental reason for there to be this sort of political economy reaction. But the thing that I think people who are projecting these very extreme scenarios don't realize is that with a the beginning of an extreme scenario there will be the beginning of an extreme political economy reaction and that will kind of endogenously constrain things. So, it's just going to be a back and forth. And what the data will end up looking like to our an to, you know, people living in the future is that things moved a lot slower than people would think because of this sort of interplay.
</details>

>> 看起来，一个人能在政治中投入的资金规模……很久以前大家都在担忧“联合公民案”（Citizens United），担心大企业会控制一切，但你看，埃隆投了5亿还是不管多少钱，也没能得到他想要的结果。这是在某种程度上暴露了金钱在政治中的局限性，还是说，科技界人士——或者不仅是科技界人士，企业——可能非常擅长为自己的业务配置资源，但或许没那么擅长在华盛顿特区和政治领域配置资源？
<details><summary>Original English</summary>
>> It it seems like, you know, uh the the sort of amount of money one can put in politics, you know, everyone was worried about Citizens United a long time ago and, you know, corporations gonna control everything, but, you know, Elon put in 500 million or what whatever it was and couldn't get the out outcome he wanted. Is is this a sort of um expose the limitations of of money in politics or is it just that you know tech people or not just tech people corporations may be very good at allocating for their business but maybe not you know uh that great at allocating in in sort of uh the DC and political realm.
</details>

>> 我敢说，学术界在某种程度上被湾区的人低估了。研究竞选资金的人早就知道这一点。有大量证据表明，竞选支出并没有那么重要。你可以认为这是好事或坏事，但这一切一点都没让我感到意外。而且我认为这并不是因为这些人蠢。从更广泛的意义上说，如果他们一开始就抱有政治企图，你或许会觉得他们蠢。但除了少数地方性选举之外，根本没有简单的办法能让你只要花大笔的钱就能得到想要的政治结果。这就是分权与制衡。即便这个体系里根本没人跟你步调一致。［笑］
<details><summary>Original English</summary>
>> Dare I say that academia is slightly underrated by Bay Area people. People who study campaign finance have known this for a long time. There's a lot of evidence that spending doesn't matter that much. You can think that's good or bad, but none of this surprised me in the slightest. And I don't think it's that the people are fools. Uh you might think they're fools in some broader sense of just having political aspirations at all. But there's just apart from some number of local races, there's no simple way to just spend a lot of money and get the politics you want. It's checks and balances. even though no one in the system is like aligned with you. [laughter]
</details>

>> 是的，
<details><summary>Original English</summary>
>> Yeah,
</details>

>> 我们拥有一套美好的制度。我真的每一天都在——我不是在开玩笑——美国的制度令人赞叹，竞争性市场也令人赞叹。一切都……它并不完美，但正如泰勒所说，这个制度中涌现出了种种不可思议的神奇之处。
<details><summary>Original English</summary>
>> it's a beautiful system we have. I'm like just every day I'm in I'm I'm not joking. I'm like it's you know the the American system is incredible and competitive markets are incredible. It's just everything just, you know, it's it's not perfect, but exactly as Tyler said, like there's all this magic that comes out of the system.
</details>

### 成为经济学家的缘起与背景

>> 对。我很好奇，如果你们互相采访对方，你们会问什么，最对什么感到好奇？泰勒，我先从你开始。你最想了解亚历克斯对哪方面的看法，或者……？
<details><summary>Original English</summary>
>> Yeah. I'm I'm I'm curious if you were both interviewing each other, what what you would uh what you would what are you most curious about. Tyler, I'll I'll start with you. Where are you most curious about Alex's perspective on on on something or or or Yeah.
</details>

>> 嗯，你成为经济学家的缘起故事。
<details><summary>Original English</summary>
>> Well, your origin story of how you became an economist.
</details>

>> 这个嘛，这是个非常利己的问题，泰勒［笑］，因为这跟你有关。
<details><summary>Original English</summary>
>> Well, it's that's a very self-serving question, Tyler, [laughter] because it has to do with you.
</details>

>> 好吧，那多讲讲。
<details><summary>Original English</summary>
>> Okay, we'll say more.
</details>

>> 好的。我是说，我是来自摩尔多瓦的移民。在美国，我基本上是靠食品券之类长大的。我父母对经济学一无所知，我对经济学也一无所知。我上了大学，读的是医学预科，因为我知道医生是什么，我父母也知道医生是什么。在大学里，你必须修一些先修课，我就选了一门经济学通论课，觉得还挺有意思的。但我依然是医学预科生，我上了那门课，拿了好成绩，把我的GPA拉得比我那些医学预科课程原本显示的要高。

然后，我打算去读医学院，也申请了医学院，并且拿到了录取通知。后来，我开始读《边际革命》（Marginal Revolution），也开始听……我还听了一期全国公共广播电台（NPR）采访理查德·塞勒（Richard Thaler）的节目。在你们两位的共同启发下，我一下子意识到：原来经济学还可以这么做。这太不可思议了。
<details><summary>Original English</summary>
>> Yeah. So I mean so I was uh I'm an immigrant from Muldova. So you know I very you know grew up on food stamps and things like that in America. And I my parents didn't know anything about economics. I didn't know anything about economics. I I went to college and I was premed cuz I knew what a doctor was. Uh my parents knew what a doctor was. And in college like you had to take like prerequisites and I took an econ one class and I thought this was kind of fun. But I'm still premed and I took it. I got good grades, made made my GPA higher than my premed classes suggested. Um, and then, you know, I was going to go to medical school. I applied to medical school. I got into medical school and then, you know, I started reading Marginal Revolution and I started listening to uh, you know, that I I also heard like an NPR article uh, uh, program with Richard Thaylor. And between the both of you guys, it was just, oh, I can do this with economics. This is incredible.
</details>

>> 那个故事我之前只知道一部分，所以谢谢你分享。
<details><summary>Original English</summary>
>> I only knew one part of that story, so thank you.
</details>

>> 我知道《边际革命》那部分。
<details><summary>Original English</summary>
>> I knew the marginal revolution part.
</details>

>> 对。确实是那样，因为在那个时候——那是2008年还是2009年——并没有多少经济学家能向你切实展示通过这个学科究竟能做多少事情。所以我直接放弃了医学院，退出了申请流程。我去了唯一录取我的学校，也就是加州大学圣地亚哥分校，非常感谢他们。接下来的事大家都知道了。这真的是一个不可思议的领域和知识库，让我们能够尽我们所能——尽管理解的程度其实并不高——去搞清楚在“经济”这个复杂的系统里究竟在发生什么。
<details><summary>Original English</summary>
>> Yeah. No, I mean it was but it was like because you at that point, this was 2008 or n um there weren't a lot of these economists like you know actually showing you how much you can do with the topic. And so I actually, you know, I pulled out of medical school of the of the process. I went to the only school that accepted me which was you know thank you UC San Diego. Um and uh yeah the rest is history. I I this is just like the such an incredible field and knowledge base to kind of understand to the extent that we can which is like not very high about uh about what's going on in this you know complex system that we call the economy.
</details>

>> 我能追问一个问题吗？
<details><summary>Original English</summary>
>> Can I ask a followup please?
</details>

>> 摩尔多瓦会并且应该成为罗马尼亚的一部分吗？

我是说，我认为会，是的，那是我的观点。
<details><summary>Original English</summary>
>> Will and should Muldova become a part of Romania?

I mean my Yes. That's my view.
</details>

>> 而且他们最终会合为一体。我认为他们应该这样，而且他们最终会的。
<details><summary>Original English</summary>
>> And they will. I figure they should, but they will.
</details>

>> 好的。
<details><summary>Original English</summary>
>> Okay.
</details>

>> 是的。他们原本就是一体的。最初那个国家叫比萨拉比亚。我祖母就是来自比萨拉比亚。
<details><summary>Original English</summary>
>> Yeah. I I They were originally. I mean, it was the country was called Basarabia. My grandma, you know, she was from Basarabia.
</details>

>> 她不是来自摩尔多瓦。而且我觉得这可能是一个有争议的看法，但我其实并不是来自摩尔多瓦，我是来自德涅斯特河沿岸。啊，好的，这下全明白了。
<details><summary>Original English</summary>
>> She wasn't from Muldova. Um, and it I think it this probably a controversial opinion, but I I I'm actually not from Muldova. I'm from Transnistra. Ah, okay. Now it's all clear.
</details>

>> 所以，
<details><summary>Original English</summary>
>> So,
</details>

>> 是的。所以我们是从德涅斯特河沿岸逃难到美国的难民。那里当时爆发了内战。我们躲在地下室里躲避子弹等等。后来我们作为难民来到了美国。但我认为，如果你了解摩尔多瓦文化，它和罗马尼亚文化非常相似，语言也几乎是一样的。
<details><summary>Original English</summary>
>> yeah. So, like you know that we were refugees from Transnistria to America. So, there was a civil war. We were like in basement hiding from bullets and all that type of stuff. And then we we ended up coming to America as refugees. But I think it's like, you know, the c the if you know Muldoven culture, it's very similar to Romanian culture. Um the language is almost the same.
</details>

### 国际象棋直觉与对人工智能的早期洞察

>> 风险投资人说一定要问缘起故事，他们说得太对了。亚历克斯，你想问泰勒什么问题？
<details><summary>Original English</summary>
>> When the VCs say always ask for the origin story, they're so correct. Yeah. The um Alex, what question would you ask Tyler?
</details>

>> 我想知道，因为你关注这个领域非常早，而且我想我从来没听过这个故事：你是如何被人工智能吸引并开始如此严肃地思考AI的？你非常早就认识到了这项技术的颠覆性潜力，我很好奇你是如何比大多数人更早意识到这一点的？
<details><summary>Original English</summary>
>> Um I I want to know your because you were so early on this and I don't think I've ever heard this story of like how how were you kind of attracted to AI and thinking about AI so seriously. Um, and you were you were very early about like the transformative potential of the technology like uh and I'm just curious like how how how did you how did you realize that earlier than most?
</details>

>> 所有的国际象棋棋手都有类似的故事。我早年算是个国际象棋神童。13岁那年我在新泽西下棋，他们推出来一台叫“小叮当”（Tinkerbell）的计算机跟人类对弈。它下得很烂，但我看到了那种进步的趋势。但关于国际象棋棋手，关键在于这一点：只要水平够好，他们都心知肚明，国际象棋根本不是袖珍计算器那套东西，它是直觉。

如果你看到计算机攻克了一个你早就知道主要依赖直觉的领域，你就会非常容易相信它们也能攻克许多其他领域。所以卡斯帕罗夫很早就意识到了这一点。肯·罗格夫（Ken Rogoff）不需要别人多给他灌输AI观念，他很早就意识到了。国际象棋圈子里的人是最早认识到这点的。这就是一个非常简单直接的故事，事情就是这么发生的。
<details><summary>Original English</summary>
>> Well, all chess players have a story like this. I was in early years at like a chess prodigy. So I was age 13 playing in New Jersey and they wheeled in a computer called Tinkerbell that played against the humans and it sucked but I saw what the progress was like. But the point about chess players is this. They all know if they're any good. The chess is not like pocket calculator stuff. It's intuition.

And if you see computers conquer an area that you already knew was mostly intuition, you will find it very easy to believe they can conquer a bunch of other areas. So Kasparov was early to this. Ken Rogoff didn't need much AI pilling. He was early to this. And the chess people were the first ones there. And that's a very simple direct story. And that's how it happened.
</details>

>> 德米斯（Demis）也是。
<details><summary>Original English</summary>
>> And Demis too.
</details>

>> 德米斯也是。绝对是这样。
<details><summary>Original English</summary>
>> Demis 2. Absolutely
</details>

>> 常见的故事。你看到它在20世纪90年代大显身手，深蓝（Deep Blue）击败了卡斯帕罗夫。而深蓝其实算不上什么好模型。
<details><summary>Original English</summary>
>> common stories. You see it, you know, kick butt by the 1990s and it beats Kasparov of Deep Blue. And Deep Blue is not a great model.
</details>

>> 但当时的感觉就像是：好吧，它能做到这个了。所以你就在等着它扩散到其他所有领域。不过这确实花了很长时间。事实上，
<details><summary>Original English</summary>
>> But it's like, okay, uh, it can do this. So, you're just waiting for it to spread to everything else. But it took a long time. In fact,
</details>

>> 是的。我认为这是一个极佳的例子。很多人过去看着AI会说：嘿，它做不了这个，做不了那个；但它几乎将能够做到所有事情。比如考虑到RLVR（基于可验证奖励的强化学习）之类的东西，比如后训练中的可验证奖励部分，很多人把它当作精神安慰剂，说“哦，那个是不可验证的，那个也是不可验证的”；但如果你去训练验证器，几乎任何东西都会变得可验证。
<details><summary>Original English</summary>
>> yeah. I I think this is like a great example of like you know a lot of people would have looked at AI and said hey this it can't do this it can't do that but it's it it that it's going to be able to do almost everything because you know like thinking about like RLVR or something like that like the verifiable reward part of of post training a lot of people like use that as like copium like oh that's not verifiable that's not verifiable but like if you train the verifier almost anything will become verifiable.
</details>

>> 你能够批判它，就意味着它几乎是可验证的，对吧？
<details><summary>Original English</summary>
>> The fact that you can criticize it means it's verifiable almost, right?
</details>

>> 是的，没错，完全正确。所以国际象棋真的是一个绝佳的例子。如果你是一个优秀的棋手，你就会非常清楚那需要多少直觉，以及未来这能走多远。
<details><summary>Original English</summary>
>> Yeah. Exactly. Exactly. So, it's like it's it's a and and chess is like a really great example. Like you see if you're a really good chess player, you know exactly how much that that intuition is required and how far that's going to go in the future.
</details>

>> Mar 正在研究诗人方面。我不确定他们进展到哪一步了，但在我看来这应该是行得通的。
<details><summary>Original English</summary>
>> Mar is working on the poets. I'm not sure how far along they are. Uh but it seems to me it should work.
</details>

>> 嗯。写出更好的诗歌，
<details><summary>Original English</summary>
>> Mhm. in better poetry,
</details>

>> 对吧？写出伟大的诗歌。我认为在不到两年的时间里，只要大家稍加用心，这就会成为可能。我指的不是投入数十亿美元的大规模项目，而只是稍微花点心思。找来十几个诗人，给他们一些报酬，对吧？用不着太多钱。放手让他们去做，并在整个过程中设立一些制衡机制。这一定行得通。
<details><summary>Original English</summary>
>> right? To write great poetry. I think uh in less than two years, it will be possible if people put their minds to it at all. I don't mean a big major effort with billions, but just some kind of effort at all. Bring in a dozen poets, pay them something, right? Doesn't have to be that much. Let them loose, have some checks and balances on the process. It'll work.
</details>

<!-- chunk 7/8 -->

>> 是的。公司里有些人认为，“品味是人类独有的”这种观点纯粹是一种自我安慰（cope）。那些系统其实……已经很擅长了。

<details><summary>Original English</summary>
>> Yeah.

 Some

 people

 at

 the

 firm

 think

 that





the

 idea

 of

 of

 taste

 being

 uniquely





human

 is

 is

 a

 cope.

 that

 uh

 that

 that





the

 systems

 will

 are

 already

 good

 at.
</details>

>> 它们现在就已经具备极佳的品味了。你去问它们古典音乐，比如西贝柳斯第五交响曲哪个录音版本最好之类的问题，它们给出的回答非常精彩，比现在的《企鹅唱片指南》（Penguin Guide）还要好。

[笑声]

<details><summary>Original English</summary>
>> They

 already

 have

 great

 taste.

 You

 ask





them

 about

 classical

 music

 like

 what's





the

 best

 recording

 of

 Sibilius's

 fifth





whatever

 they

 give

 great

 answers

 better





than

 the

 Penguin

 Guide

 right

 now.





[laughter]
</details>

### 资本回报、稀缺性与经济瓶颈

>> 是的，太有意思了。好的，在我们结束之前，我想问几个杂锦式的问题。一个是，你们有没有看到 Doresh 和别人合写的一篇文章，大致是说皮凯蒂（Pikid）对上个世纪的论断虽然不对，但他提出的 r > g 等模型在 AI 世纪里可能是对的。Alex，我很想听听你对此有什么看法。

<details><summary>Original English</summary>
>> Yeah.

 Fascinating.

 Okay.

 So,

 there's

 a





few

 grab

 bag

 questions

 I

 want

 to

 ask





before

 before

 we

 wrap.

 one

 is

 did

 you





guys

 see

 Doresh's

 uh

 sort

 of

 essay

 he





collaborated

 with

 somebody

 on

 sort

 of





basically

 saying

 that

 Pikid

 you

 know





wasn't

 right

 about

 the

 last

 century

 but





but

 his

 model

 of

 you

 know

 RG

 etc

 is

 is





might

 be

 right

 in

 the

 AI

 uh

 century

 I'm





I'm

 curious

 if

 you

 uh

 had

 a

 take

 on

 that





Alex
</details>

>> 对，我想那是和 Phil Trel 合写的，关于 21 世纪的资本之类的。

<details><summary>Original English</summary>
>> yeah

 so

 this

 is

 with

 Phil

 Trel

 I

 think





um

 capital

 in

 the

 21st

 century

 y
</details>

>> 嗯。

<details><summary>Original English</summary>
>> um
</details>

>> 我觉得那篇……我觉得它的核心观点在于，经济活动可能会与劳动力脱钩，转而主要集中在资本上。这是那篇文章比较宏观的思路。我认为很多人对那篇文章具体的研究方法提出了质疑，对此我在此不作评价。但是，这项技术可能会加剧这种集中、加剧对资本的依赖，这个大方向我认为确实是一种可能发生的情景。

不过还存在其他替代情景，这也是我之前写过的内容，我想 Tyler 也提到过这一点——在另一种可能的情景下，社会反而会创造出更多的工作岗位，而这些岗位之所以有价值，恰恰是因为它们是稀缺的。

<details><summary>Original English</summary>
>> I

 think

 that's

 a

 that's

 I

 think

 it's

 uh





the

 the

 idea

 a

 that

 economic

 activity





may

 be

 divorced

 from

 labor

 and

 be

 kind





of

 focused

 on

 on

 capital.

 Um

 that

 the





that's

 kind

 of

 the

 broader

 idea

 of

 the





piece.

 I

 think

 I

 think

 many

 people

 took





took

 kind

 of

 uh

 uh

 had

 issues

 with

 the





actual

 methodology

 of

 the

 piece

 which





you

 know

 I

 won't

 I

 won't

 speak

 to

 but





the

 broad

 idea

 of





the

 technology

 potentially

 increasing





this

 concentr

 that

 the the

 reliance

 on





capital

 I

 think

 that

 is

 a

 that

 is

 a





scenario

 that

 could

 happen

 um

 but





there's

 alternative

 scenarios

 and

 this





is

 things

 that

 I've

 written

 about

 and

 I





think

 Tyler

 also

 alluded

 to

 this

 where





um

 depending

 on

 there's

 there's

 an





alternative

 scenario

 where

 like

 you

 know





there's

 just

 more

 jobs

 created

 and

 these





jobs

 are

 valuable

 because

 of

 the

 fact





that

 they're

 scarce.
</details>

>> 是的。

<details><summary>Original English</summary>
>> Yeah.
</details>

>> 没错。所以核心理念在于，价值会向稀缺性转移。这其实就是整个瓶颈逻辑。如果这些工作存在于一个富裕的社会中，就会有大量的价值流向这些岗位。问题只在于会有多少这样的工作存在，以及它是否能够支撑起整个经济。从历史上看一直都是如此，但这正是目前真正巨大的问号所在。不过，这些都是我们需要通过数据去密切观察的事情。比如我和别人合写的那篇关于 AGI 经济政策的论文，基本上就是提出这个论点：我们需要以一种全面得多的方式，去追踪经济随着 AI 正在走向何方。

<details><summary>Original English</summary>
>> Right.

 So

 the

 idea

 is

 that

 you

 know





value

 moves

 towards

 scarcity.

 These

 this





is

 kind

 of

 like

 the

 whole

 bottleneck





logic

 and

 then

 if

 those

 jobs

 are

 in

 a





rich

 society

 they

 there

 will

 be

 a

 lot

 of





value

 going

 to

 those

 jobs.

 And

 it's

 just





a

 question

 of

 how

 many

 of

 those

 jobs





exist

 and

 whether

 it

 can

 support

 the





entire

 economy.

 And

 historically

 that's





been

 the

 case,

 but

 that's

 been

 that's





the

 real

 big

 question

 mark.

 Um,

 but





these

 are

 things

 that

 we

 just

 need

 to





watch

 for

 with

 data.

 So

 like

 my

 paper





with

 you

 know

 an

 economic

 policy

 for

 AGI





just

 basically

 makes

 that

 argument.

 We





need

 to

 be

 tracking





where

 where

 the

 economy

 is

 going

 with

 AI





in

 a

 much

 more

 uh

 comprehensive

 way.
</details>

>> 非常底层的技术往往会让消费者受益。火、语言、电力等等，莫不如此。这并不能证明历史一定会重演。但我们必须把“资本能做很多事”与“存在准入门槛使垄断租金流向特定的资本所有者”这两件事区分开来。

<details><summary>Original English</summary>
>> Very

 fundamental

 technologies

 tend

 to





benefit

 the

 consumers.

 Fire,

 language,





electricity

 and

 so

 on

 and

 so

 on.

 That's





no

 proof

 it

 will

 happen

 again.

 But

 we





need

 to

 distinguish

 between

 capital

 can





do

 a

 lot

 versus

 there

 are

 entry

 barriers





that

 will

 acrue

 monopoly

 rents

 to





particular

 capital

 owners.
</details>

>> 而且我认为那篇文章并没有真正为后一个命题提供强有力的论据。它主要是论证了资本能够大有作为。但如果资本被高度商品化，比如我认识有些人认为所有的租金都会流向土地，或者所有的租金都会流向能源。我不敢确定这是否属实，但如果要选的话，这些看起来比所有租金都流向资本更有可能发生。

<details><summary>Original English</summary>
>> And

 I

 don't

 see

 that

 that

 piece

 really





made

 a

 strong

 case

 for

 the

 latter





proposition.

 It

 was

 mainly

 arguing





capital

 can

 do

 a

 lot.

 But

 if

 the

 capital





is

 commoditized

 like

 I

 know

 people

 who





say

 all

 the

 rents

 will

 go

 to

 land,

 all





the

 rents

 will

 go

 to

 energy.





I'm

 not

 sure

 that

 true,

 but

 those

 seem





more

 likely

 than

 all

 the

 rents

 go

 to





capital

 if

 you

 had

 to

 say.
</details>

>> 是的，

<details><summary>Original English</summary>
>> Yeah,
</details>

>> 确实是这样。收益会流向稀缺项。如果稀缺项是能源，租金就会流向那里。

<details><summary>Original English</summary>
>> that

 that's

 right.

 It

 goes

 to

 scarcity.





And

 if

 scarcity

 is

 is

 energy,

 that's





where

 the

 rents

 will

 go.
</details>

>> 不过，说不定 AI 本身会让能源变得不再那么稀缺。所以我才不太愿意做预测，

<details><summary>Original English</summary>
>> Now,

 maybe

 AI

 itself

 makes

 energy

 less





scarce.

 So

 that's

 why

 I'm

 reluctant

 to





predict,
</details>

>> 但我至少看到了这样一种立论理由：比如海湾国家或者土地所有者会大赚一笔等等；但 AI 会改变足够多的事情。假设我们能够以极低的成本进行土地地形改造，以极低的成本实现海水淡化——这听起来并非不可想象。那么，也许稀缺的是土地的地理位置，或是最好的养老胜地；又或者像太浩湖之所以特殊，是因为它临近湾区却不用交加州的税等等。这非常难以预测，但核心还是要从稀缺性的角度去思考。

<details><summary>Original English</summary>
>> but

 I

 at least

 see

 the

 case

 to

 think,





well,

 the

 the

 Gulf

 countries

 will

 make





out

 like

 bandits

 and

 so

 on

 or

 the

 land





owners,

 but

 AI

 will

 change

 enough





things.

 Say

 we

 can

 terraform

 land

 quite





cheaply

 and

 desalinate

 water

 very





cheaply.

 It

 doesn't

 seem

 so

 implausible.





Well,

 maybe

 it's

 location

 of

 land

 or

 the





best

 retirement

 spots

 or

 like

 Tahoe

 is





so

 special

 because

 you're

 near

 the

 Bay





Area

 but

 you

 don't

 pay

 the

 taxes

 or

 but





it's

 very

 hard

 to

 predict

 but

 think





through

 scarcity

 most

 of

 all.
</details>

>> 嗯。

<details><summary>Original English</summary>
>> Mhm.
</details>

### 《情境意识》、模拟与全脑仿真

>> 是的。顺着这个思路，在我们这个领域，我们认为最大的稀缺在于供给端；而在短期内，需求其实远比表面上看起来要大得多。但这是建立在一种假设或信念之上的，那就是当你和超级用户交流时，他们好像总觉得用不够。而这些超级用户在极少数公司的极少数人中只占很小的比例，AI 目前还没有实现广泛普及。

我认为对这种观点的反驳会是：它目前还没有对企业产生可衡量的实际影响。因此，认为 AI 用得越多就最终越能对这些企业产生实质影响、从而证明支出大幅增加是合理的，这在某种程度上还带有投机性。

不过，我们刚刚成立了一支名为“机器时代基金”（machine age fund）的新基金，专门投资数据中心以及基础设施堆栈的其他环节，以缓解其中一些供给挑战。

利奥波德（Leopold）的那篇论文《情境意识》（Situational Awareness），在你们看来，算不算是过去几年科技界最重要的公共知识分子作品之一？我很想听听你们对它所留下的思想遗产怎么看。

<details><summary>Original English</summary>
>> Yeah.

 And

 in in

 our

 world

 on

 that

 on





that

 note

 we

 we

 think

 that

 the

 biggest





scarcity

 is

 is

 on

 supply

 and

 in

 the





short

 term

 uh

 that

 that

 demand

 is

 is





much

 bigger

 than

 uh

 than

 it

 seems.

 Uh





but

 that

 rests

 on

 the

 sort

 of

 assumption





or

 or

 sort

 of the

 belief

 that

 when

 you





talk

 to

 the

 super

 users,

 they

 sort

 of





like

 can't

 get

 enough.

 Um

 and

 there's





the

 the

 super

 users

 are

 really

 a

 small





percentage

 of

 of of

 people

 at

 at

 at

 a





small

 percentage

 of

 companies

 and

 AI

 is





still

 not

 broadly

 diffused

 yet.

 And

 I





think

 the

 counter

 to

 that

 claim

 would

 be





well

 it's

 not

 having

 measurable

 impact





on

 companies

 yet.

 So

 it

 is

 uh

 sort

 of





speculative

 that

 um

 you

 know

 the

 more





that

 AI

 is

 used

 it

 will

 eventually

 lead





to

 impact

 on

 these

 companies

 in

 ways





that

 justify

 uh

 the

 massive

 increase

 in





spend.

 Um

 but

 you

 know

 we

 just

 started

 a





new

 fund

 actually

 called

 machine

 age





fund

 which

 is

 you

 know

 doing

 data





centers

 and

 other

 elements

 of

 the

 sort





of

 infrastructure

 stack

 to

 be

 able

 to

 um





mitigate

 some

 of

 these

 supply





challenges.

 Leopold's

 paper

 situational





awareness

 does

 does

 that

 sort

 of

 stand





to

 you

 as

 like

 one

 of

 the

 more

 important





uh

 sort

 of

 you

 know

 public

 intellectual





pieces

 in

 technology

 in

 the

 in

 the

 past





few

 years

 or

 I'm

 curious

 what

 you

 think





of

 the

 the

 legacy

 of

 uh

 of

 that
</details>

>> 在任何领域都算得上，不仅限于科技领域。但话虽如此，我认为他太迷恋“快速起飞”（fast takeoff）了。正如我当时对他说的那样，他假设模拟可以替代真实实验，从而会形成一个科学不断自我加速的无尽循环。而我认为模拟并不能在很大程度上替代真实实验。它只会在某些领域奏效。Alex，

<details><summary>Original English</summary>
>> in

 anything

 not

 just

 technology

 but

 that





said

 I

 think

 he's

 too

 enamored

 of

 fast





takeoff

 as

 I

 told

 him

 at

 the

 time

 he's





assuming

 simulation

 can

 substitute

 for





experiment

 and

 thus

 you

 get

 this





neverending

 loop

 where

 science

 just





keeps

 on

 accelerating

 and

 I

 don't

 think





simulation

 very

 much

 subs

 in

 for





experiment.

 It

 will

 in

 some

 areas.





Alex,
</details>

>> 我们看法一致。[笑声]

<details><summary>Original English</summary>
>> we

 agree.

 [laughter]
</details>

>> 我想，我自己受卢卡斯批判（Lucas critique）的影响太深了——抱歉，又提了一个行话——但这基本上解释了为什么你必须理解问题的深层结构性参数，才能够真正做出预测。模拟所做的事情以及 AI 真正擅长的事情就是预测，但它很多时候并没有把系统的内生反应考虑在内。我想我们会越来越多地看到这种情况的上演。

<details><summary>Original English</summary>
>> I

 think

 you

 know

 I'm

 I'm

 too

 Lucas





critique

 pill

 uh

 for

 sorry

 another





another

 inside

 baseball

 but

 it's

 like





basically

 why

 you

 need

 to

 understand





kind

 of

 like

 the

 deep

 structural





parameters

 of

 the

 problem

 in

 order

 to





actually

 be

 able

 to

 predict.

 what





simulations

 do

 and

 what

 AI

 is

 really





good

 at

 is

 predicting,

 but

 it's

 uh

 it





doesn't

 take

 the

 indogenous

 response

 of





the

 system

 a

 lot

 of

 the

 time

 into





account.

 And

 um

 we'll

 we'll

 we'll

 see





that

 kind

 of

 play

 out

 more

 and

 more.

 I





think
</details>

>> 那么罗宾·汉森（Robin Hansen）的《爱姆时代》（Age of M），你们觉得它经得起检验吗？或者这些思想的遗产会是什么？

<details><summary>Original English</summary>
>> the

 um

 Robin

 Hansen's

 Age

 of

 M

 how

 do





you

 think

 that

 uh

 that

 stands

 up

 or

 will





the

 legacy

 of

 of

 those

 ideas

 be?
</details>

>> 嗯，我认为它是错的。那是一本非常精彩的书，我也很喜欢罗宾，但当那本书出版时——现在已经过去挺久了——我就对他说：罗宾，AI 会先实现。罗宾说不是，AI 可能会实现，但全脑仿真（M）必须先到来。我说：罗宾，M 很可能永远都不会发生，但即使它发生，首先也需要 AI。我认为在那场辩论中，我这边的观点目前看起来非常站得住脚。但那是一本获取思想的绝佳读物，能把你从教条式的沉睡中唤醒。

<details><summary>Original English</summary>
>> Well,

 I

 think

 it's

 wrong.

 It's

 a





brilliant

 book

 and

 I

 love

 Robin

 but

 when





it

 came

 out

 which

 is

 now

 a

 while

 ago

 I





said

 Robin

 AI

 is

 going

 to

 get

 there





first

 and

 Robin

 says

 no

 AI

 might

 get





there

 but

 M

 has

 to

 come

 first

 and

 I

 said





Robin

 M

 probably

 will

 never

 happen

 but





if

 it

 does

 first

 it

 needs

 AI

 and

 I

 think





my

 side

 of

 that

 debate

 is

 looking

 very





good

 but

 it's

 a

 great

 book

 to

 read

 for





getting

 ideas

 and

 just

 shaking

 you

 out





of

 you

 know

 the

 dogmatic

 slumbers.
</details>

### 英伟达与制衡机制

>> 你们有任何……说到时下的话题，眼下英伟达可以说是处于舆论的风口浪尖，伴随着黄仁勋（Jensen）那边的情况。从你们观察公众舆论的角度来看，你们觉得有什么是被误解的？或者你们如何解读这可能意味着什么？如果有的话，可以吸取什么教训？Tyler，你怎么看？

<details><summary>Original English</summary>
Do





you

 have

 any

 We're

 right

 now

 talking

 of





speaking

 of

 timely

 issues

 sort

 of

 Nvidia





is

 sort

 of

 is

 in

 a

 big

 uh

 crosshairs

 at





the

 moment

 uh

 with

 sort

 of

 the

 Jensen





situation

 as

 you

 sort

 of

 view

 the

 public





discourse.

 what

 do

 you

 think

 is





misunderstood

 or

 or

 how

 are

 you

 sort

 of





interpreting

 um

 you

 know

 what

 this





potentially

 means

 or

 what

 lessons

 if

 any





to

 to

 take

 or

 what

 do

 you

 think

 Tyler
</details>

>> 你看，我们之前就说过对齐是不可能的。涉及的利益是如此巨大。他的行为、这家公司，有些东西似乎脱离了对齐。

事实上，由于存在制衡机制，情况最终会没事的。我不知道他们具体会如何运作。我认为这给我们一直以来谈论的各种道理上了很好的一课。

<details><summary>Original English</summary>
>> you

 know

 we've

 already

 said

 alignment

 is





impossible

 the

 stakes

 were

 so

 high

 his





behavior

 the

 company

 something

 seems

 out





of

 alignment





in

 fact

 it

 will

 be

 fine

 because

 of





checks

 and

 balances

 I

 don't

 know

 how





they're

 going

 to

 operate

 uh

 I

 think

 it's





a

 great

 lesson

 in

 all

 the

 different





things

 we've

 been

 saying
</details>

>> Alice，你有什么要补充的吗？

<details><summary>Original English</summary>
>> Alice

 anything

 you'd

 add
</details>

>> 是的，我觉得这其实不会太大改变未来的发展轨迹。我认为制衡机制是起作用的。我们在很大程度上拥有供应链的多样性。一切都被超额认购。需求创造供给，供给也创造需求。

所以我认为整个系统是稳健的。最大的变化可能在于，如果在宏观层面上出了什么差错，而在 CEO/创始人这类角色被削弱或离任的情况下，英伟达必须以最后购买人或最后贷款人的身份介入，那么他们承担这一角色的能力会远不如这一切从未发生过时的状态。确实，这会有影响，但从中期来看会被消化掉，它可能会让进度稍微放缓一点。但是，结构性的力量迟早会重新占据主导。嗯。

<details><summary>Original English</summary>
>> yeah

 I

 I

 think

 um

 you

 know

 I'm

 I I

 I

 I





think

 this

 is

 not

 really

 going

 to

 change





the

 trajectory

 much.

 I

 think

 like

 checks





and

 balances

 work.

 We

 have

 diversity

 in





the

 supply

 chain

 to

 to

 a

 large

 extent.





Um

 everything

 is

 over

 subscribed.

 Demand





creates

 supply.

 Supply

 creates

 demand.





Um

 so

 I

 think

 I

 think

 things

 are

 going





to

 uh

 you

 know

 the

 the

 the

 system

 is





robust.

 The

 biggest

 change

 might

 be

 if





something

 goes

 wrong

 at

 the

 macro

 level





and

 Nvidia

 had

 to

 step

 in

 as

 a

 buyer

 or





lender

 of

 last

 resort

 with

 a

 weakened

 or





gone

 CEO

 founder

 type.

 They're

 a

 lot





less

 able

 to

 do

 that

 than

 they

 would





have

 been

 had

 all

 this

 never

 happened.





Like,

 yeah,

 that

 matters,

 but

 in

 the





medium

 term,

 it's

 going

 to

 wash

 out

 and





it

 could

 slow

 things

 down

 a

 bit.

 But





again,

 the

 structural

 forces

 will

 take





over

 sooner

 or

 later.

 Mhm.
</details>

>> 如果让你们预测一下，下一部类似《情境意识》、能够极具预见性并对我们社会产生巨大影响的同类文献会属于什么题材？你们预计会出现在哪个领域？会是在生物技术领域的某些东西吗？还是依然会在……

<details><summary>Original English</summary>
>> If

 you

 if

 you

 had

 to

 expect

 what

 is

 the





next

 genre

 of

 sort

 of

 situational





awareness

 like

 document

 that

 is

 going

 to





be

 remarkably

 preient

 and

 greatly

 impact





our

 society,

 where

 would

 you

 expect

 that





that

 to

 be?

 Would

 it

 be

 in

 something

 in





biotech?

 Would

 would

 still

 be
</details>

<!-- chunk 8/8 -->

### 被低估的AI研究方向

……在AI领域的某些方面？比如，你们是怎么思考的，眼下有哪些被低估的想法在未来几年可能会产生巨大影响？
<details><summary>Original English</summary>
in something in AI? Like how how are you thinking about sort of what are some underrated ideas right now that might be massive in the years to go?
</details>

>> 对我来说，它们也确实被低估了。我是说，人人都在谈论生物科技，我也完全赞成，但我认为那会格外缓慢，因为存在监管限制，而且无法利用模拟来解决主要问题。不过话又说回来，埃里克，我认为你能活到120岁，而我觉得我活不到。简单来说就是这样。我认为我们会得到更好的模型，只要AI能为微观和宏观现象建立更好的模型，比如更好的结构模型。所以比如细胞模型，或者用数字孪生来研究宏观经济学之类的事情，只要你能够为我们需要用来预测的事物建立结构，我认为那将是真正的大爆发。嗯，因为这在某种程度上契合了经济学中的那个理念，就像简化式与结构式的争论，当你理解了结构，你就能真正创造全新的东西。而我认为AI——AI在这方面的潜力，帮助你理解并重构那种结构，我认为这真的被严重低估了。
<details><summary>Original English</summary>
>> Well, they're underrated to me, too. I mean, everyone talks about biotech and I'm fully on board, but I think that will be especially slow because of regulation and the inability to use simulation to address the main issues. But again, Eric, I think you'll live to 120 and I think I will not. That's a simple way to put it. I I think we're going to get better models of a to the extent that AI will create better models of micro and macro phenomenon like better structural models. So something like the model of the cell or like an like a act like using digital twins to do macroeconomics or something like that to the extent that you are going to be able to put structure on things that we need to be able to use to predict that's going to be the real big blow up I think. Um, and because that kind of gets to that idea in economics like the reduced form versus structural debate where you when you understand the structure, you can really create brand new things. And I think AI the potential for AI to do that to help you understand and recreate that structure. I think that's really underrated.
</details>

>> 这会很棒。Ross Jetty刚发表了一篇关于数字孪生的新论文。
<details><summary>Original English</summary>
>> It'll be great. Ross Jetty has a new paper out on digital twins.
</details>

### 高等教育创新与经济学的未来

>> 没错。数字孪生。这正是我所指的。但他需要，你知道，五位共同作者、大量资金和一个研究中心，这没问题。他做成了这件事，这非常棒。但这也能说明一些问题。

其实，我们最后来谈谈大学的问题吧，因为我们之前说过，学术界在某些方面被低估了，硅谷无疑低估了它。既然我们已经给予了应有的认可，我确实想问问你们两位，在高等教育的创新方面，你们对什么最感到兴奋？最紧迫的需求又在哪里？我们孵化了Harwitz and Dre Academy，自然对这个问题很感兴趣。也许泰勒，我们先从你开始。
<details><summary>Original English</summary>
>> Exactly. Digital twins. That's exactly what I'm referencing. But he needed, you know, five co-authors and a lot of money and a research center, which is fine. It's wonderful that he's done it. But that also goes to show you something.

Let let's close on the university question actually because we we we said earlier, you know, the the the academy is underrated in in some ways, certainly by Silicon Valley. Now that we've, you know, given the the the props, I do want to ask you guys, where are you most excited um in terms of innovation uh uh in in higher education? and uh where is the the most sort of urgent need? We of course are interested in the question having incubated Harwitz and Dre Academy. Um maybe Tyler, we'll start with you.
</details>

>> 我希望你们真能做点事情，投入的资金比你们宣布的更多，并派出一些最优秀的人才来做。我不太清楚你们的具体计划是什么。但我很乐意以某种方式参与进来。就像德克萨斯大学奥斯汀分校、密涅瓦大学以及其他创新一样，我们在高等教育中需要更多的实验、创新和度量。如果你参与其中，我会非常激动。
<details><summary>Original English</summary>
>> I hope you all do something and spend more money on it than what you've announced and put some of your best people on it. Uh I don't really know what your plans are. Uh but I'd love to be involved in some way. And as with U Austin and uh Manurva and other innovations, we need much more experimentation, innovation, and measurement in higher ed. And if you're part of that, I'm thrilled.
</details>

>> 太棒了。我很希望能邀请到你。亚历克斯，你对什么最感到兴奋，或者对于任何试图在高等教育领域进行创新的人，你有什么建议？
<details><summary>Original English</summary>
>> Amazing. I would love to have you. Alex, where are you most excited or uh what what advice might might you have to anybody trying to innovate in higher education?
</details>

>> 我认为创新越多越好。我觉得高等教育在接下来……我不知道具体什么时候，会发生彻底的改变。我没有明确的时间表，仅仅因为它们是运转如此缓慢的机构。而且……但我认为这将会……市场力量将会导致我们对高等教育的传统认知——即那个部门传统形态的缩减。但我认为我们将迎来大量新的创新，从长远来看，我对高等教育非常看好。这就是我想说的。

你们两位目前看好经济学领域吗？你们对正在发生的事情感到鼓舞吗？你们对此持什么态度？
<details><summary>Original English</summary>
>> I think more innovation the better. I think higher ed's going to change drastically in the next I don't know. I I don't have a great timeline for it just because they're such uh slowmoving institutions. Um and uh but I think it's going to we're we're the forces of of the market forces are going to lead to a shrinking of the kind of our standard idea of higher ed of what that sector looks like the traditional version. Uh but I think we're going to have a ton of new innovation and um we're going to have I I'm very bullish in higher ed in the long term. That's that's what I'll say.

And are you both bullish on the field of e economics at the moment? Are you encouraged by what what's happening right now? Um where do you where do you stand there?
</details>

>> 我是说，我认为经济学工具箱和经济学思维方式被严重低估了。所以我也带有极大的偏见。但我认为，从我看到事物发展的方式来看，比如我们之前讨论过的关于对齐的问题，经济学工具箱非常适合从这种机制设计的视角去思考这个问题；还有一直存在的政治经济学问题中的内生性，思考这类后果，思考卢卡斯批判，比如你估计了一个参数，但那其实不是结构参数，因此实际使用该参数来做决策是无效的。所以所有这类事情都极其重要，而且我认为在未来的日子里会变得更加重要。所以我非常看好。
<details><summary>Original English</summary>
>> I mean I think the the economic toolkit and the economic way of thinking is extremely underrated. So I'm extremely biased too. But I think like the way that I that I I see things play out like you know we had the earlier question about you know alignment and um the economic toolkit is like is perfect for thinking about that through this mechanism design perspective and you have this type of thing going on all the time about like endogenity in the political economy question and thinking through these sorts of consequences thinking through the Lucas critique about like you know you estimate a parameter but that's actually not a structural parameter so it's not going to be valid to actually use that parameter in order to actually make the decisions. So all of these sorts of things are super important and they're going to be more important in the coming days, I think. So I'm I'm I'm I'm bullish
</details>

>> 它可能干脆直接变成社会科学。经济学家不知道的事情，AI可以补足，而基础心智工具箱变得更有价值。这最初是加里·贝克尔等人提出的芝加哥学派想法。

你只需要真正聪明的人，他们具备一些有点像我们现在所说的软件工程师的技能，但它会有自己的专属名称。他们手握控制旋钮，管理着一堆AI智能体，他们是主理人，他们精通经济学，并且通晓整个人类社会科学。这就是我的预期。所以这是早期芝加哥学派构想的真正实现。
<details><summary>Original English</summary>
>> and it may just become social science. So the thing the things economists don't know, the AI fills in for the basic metal toolkit becomes more valuable. This is originally a Chicago idea from Gary Becker and others.

And uh you just want really smart people who have some skills a bit like those that we now call software engineers, but it will have its own name. And they have their fingers on the dials and they manage a bunch of AI agents and they're emparios and they know economics and do all of social science. That's what I expect. So a true realization of the earlier Chicago vision.
</details>

>> 我来自芝加哥大学，所以我认同那个构想。我对那个构想很满意。也许我们会在芝加哥大学付诸实践。
<details><summary>Original English</summary>
>> I'm from the University of Chicago, so I I I I buy that vision. I'm happy with that vision. We maybe we'll do it at the University of Chicago.
</details>

>> 太棒了，真是一个圆满收尾的时刻。泰勒、亚历克斯，非常感谢你们来参加这期播客。
<details><summary>Original English</summary>
>> Amazing full circle uh moment to end the conversation. Uh Tyler, Alex, thank you so much for coming to the podcast.
</details>

>> 谢谢你。非常荣幸。
<details><summary>Original English</summary>
>> Thank you. My pleasure.
</details>