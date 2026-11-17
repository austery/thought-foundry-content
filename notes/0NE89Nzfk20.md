---
author: The Pragmatic Engineer
date: '2026-11-16'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=0NE89Nzfk20
speaker: The Pragmatic Engineer
tags:
  - ai-impact
  - software-engineering
  - career-development
  - infrastructure
title: 微软 CEO 萨提亚·纳德拉探讨 AI 时代下的软件工程变革与职场转型
summary: 微软 CEO 萨提亚·纳德拉在播客中探讨了代码生成变廉价后，软件工程重心向规划与验证转移的趋势。他强调了企业建立自主 AI 基础设施的重要性，并介绍了微软内部由于 AI 变革带来的团队重组、角色变化以及为员工提供的自愿离职方案以提供更多职业自主权。
insight: ''
draft: true
series: ''
category: tech-trends
area: tech-engineering
project: []
people: []
companies_orgs:
  - Microsoft
products_models:
  - GitHub Copilot
  - Visual Studio Code
  - Claude Code
  - Cursor
media_books: []
status: evergreen
---
<!-- chunk 1/9 -->

在一个代码生成变得廉价的世界里，真正变难的是验证。事实上，我自己也觉得需要去学习，因为我还没有在如今主要以“代码即产出”方式运作的团队里工作过。但代码即产出有其特定的操作顺序，并不是说代码即产出就意味着大家都在胡乱生成各种随意的代码。
<details><summary>Original English</summary>
In a world where code generation has become cheap, what has become hard is verification. In fact, I kind of feel like I got to learn because I've not worked in a team that is mostly now code as output. But the code as output has a particular order of operations. It's not like code as output means everybody's just generating all sorts of random code.
</details>

>> 到了 2025 年，Claude Code 凭空杀出。我第一次觉得，你们没有立刻做出应对。
<details><summary>Original English</summary>
>> Out of nowhere 2025 clock code. For the first time, I felt that you didn't have an immediate response.
</details>

>> 当模型发生非线性跃升时，产品形态就必须改变。从这个意义上说，AI 原生产品的构建是残酷无情的。在短短 6 个月左右的时间里，IDE 仿佛就淡出了视线。
<details><summary>Original English</summary>
>> When model jumps happen nonlinearly, the form factor has to change. AI first product building in that sense is unforgiving. In 6 months or so, ide kind of faded away.
</details>

>> 我在问自己，开源运动与如今的开放模型之间是否存在相似之处？
<details><summary>Original English</summary>
>> I'm asking myself, are there parallels to the open source movement and now the open model?
</details>

>> 只要你跳出“未来会有一个包揽世界上所有知识的前沿模型”这种观念，对吧？如果你不认同这一点，那么你就必须假定，从某种意义上说，世界上有多少家公司，就应该有多少个前沿模型，对吧？因为归根结底——
<details><summary>Original English</summary>
>> If you just get past this thing called there's going to be one frontier model to have all of the world's knowledge, right? If you don't buy that, then you have to assume that there should be in some sense as many frontier models as firms in the world, right? Because after all,
</details>

### 播客引言与嘉宾介绍

当代码生成变得极度廉价之后，软件工程究竟意味着什么？今天的嘉宾是微软首席执行官萨提亚·纳德拉（Satya Nadella），他是少数几位以软件工程师开启职业生涯的科技巨头 CEO 之一。[音乐] 今天我们探讨“软件工厂”一词对萨提亚意味着什么，以及它如今在微软内部的具体形态；开放模型、[音乐] 本地模型以及“无计量智能”的构想；围绕 AI 给我们开发者带来的非常真实的焦虑；微软的自愿离职方案，以及为什么初级开发人员招聘放缓可能只是暂时的，等等。如果你想了解萨提亚认为在当下这个 AI 时代怎样才能成为一名出色的软件开发者，并且希望理解他用来审视这一切变革的深邃思维模型，那么本期节目就是为你准备的。本期节目由 Turbopuffer 赞助呈现。Turbopuffer 是一款极具扩展性、快速且廉价的混合搜索引擎，构建在对象存储之上，被 Anthropic、Linear、Ramp 等众多前沿公司采用。许多转用 Turbopuffer 的公司将他们的搜索账单削减了 50% 甚至更多，并且获得了快得多的结果。欢迎访问 turbopuffer.com/pragmatic 了解详情。

萨提亚，欢迎来到我们的播客。
<details><summary>Original English</summary>
What does software engineering mean after code generation becomes very cheap? Today's guest is Sacha Nadella, Microsoft CEO, one of the few big tech CEOs [music] who started his career as a software engineer. Today we cover what the term software factory means for Satcha and how it looks like today inside of Microsoft. Open models, [music] local models, and the idea of unmetered intelligence. the very real anxiety for us devs around AI, Microsoft voluntary exit offers and why the junior hiring slowdown might only be temporary and many more. If you want to understand what Satcha thinks will take to become a standout software dev in this age of AI and want to understand his thoughtful mental models on how to make sense of all this change, this episode is for you. This episode is presented by Turbopuffer, a ridiculously scalable, fast, and cheap hybrid search engine built on top of object storage used by cuttingedge companies like Entropic, Linear Ramp, and many others. Many companies who switch to Turbopuffer are cutting their search bills by 50% or more and getting much faster results. Check it out at turbopuffer.com/pragmatic.

Satcha, welcome to the podcast.
</details>

>> 非常感谢你能邀请我，G。
<details><summary>Original English</summary>
>> Thank you so much for having me, G.
</details>

>> 能来到这里真是太棒了，因为我不确定你是否知道，我曾经也是一名微软员工。
<details><summary>Original English</summary>
>> Well, it's great to be here because I'm not sure if you know, but I was a Microsofty.
</details>

>> 你当时是在这里，还是在别处？我——我当时在伦敦，这是我第一次来总部。所以，你知道，这就像——
<details><summary>Original English</summary>
>> Were you here or where were you? I I was in London and this is the first time I'm here in headquarters. So, you know, like
</details>

### 微软的开源转型与 VS Code 的崛起

>> 欢迎阔别 12 年后归来。不过我想把时间倒回那时。2014 年你成为 CEO 时，我其实就在微软。我记得，而且非常清楚地记得，当时微软在很大程度上依然奉行闭源。而当你上任后，你开始拥抱开源。Visual Studio Code 发布了，微软收购了 GitHub 并全面转向 Git——在那之前我们用的是 TFS。TypeScript 也作为开源项目发布了。我就是想回顾一下：当时人们都很惊讶，我在微软之外的朋友很惊讶，就连我自己都很惊讶。为什么微软会全面押注开源？
<details><summary>Original English</summary>
>> welcome 12 years back. But I want to rewind back there. I was actually at Microsoft when you became CEO in 2014. And I remember distinctly remember how Microsoft was still very much embracing closed source. And when you came on, you started to embrace open source. There was Visual Studio Code that was released. Microsoft acquired GitHub and went all on Git before we used TFS. Typescript was released as open source. And I just wanted to rewind back. Why did you people were surprised my my friends outside of Microsoft were surprised even I was surprised. Why did Microsoft go all in on open source?
</details>

>> 是啊。是的，我的意思是，在某种层面上，这些叙事和固有印象一旦形成，往往需要付出很大努力才能改变等等。因为如果你去看，甚至可以说即使在我成为 CEO 之前，微软对 Linux 的提交也有着显著的贡献，并且对此是有投入的。但我认为我们真正确保内部理解、同时也让外界明白的是，微软是致力于开源的，对吧？无论把我们的一些工作负载带到 Linux 上（比如 SQL Server），还是向 Linux 做贡献，亦或是将 TypeScript 等项目开源。我认为这些都是其中一部分。而且显然，我们作为 GitHub 的管家，将我们置于了其核心位置，我们只是想确保能够通过善待社区，赢得开源社区的信任。事实上，这很有意思。我一直在思考这件事：当你审视那些使用过开源技术的公司以及向开源做出贡献的人，如果某天真来一次彻底的核算，我认为微软要么名列榜首，要么稳居前列，对吧？事实上，如果你看看某些所谓从开源中获益最多的其他许多公司，它们几乎从未贡献过什么。我认为事情就是这样，而且就像是说，嘿，你没办法抱怨，但世界就是这么运转的——它总是充斥着叙事与事实的碰撞。
<details><summary>Original English</summary>
>> Yeah. Yeah, I mean at some level sometimes these narratives and perceptions get shaped and it takes a lot to change and what have you because if you look at even I would say commits even into Linux even preme becoming CEO I think Microsoft had significant uh contributions and were committed to it. But the thing that I think we really made sure the we understood internally and the world understood is Microsoft is committed to open source, right? Whether it is uh bringing some of our workloads to Linux like SQL Server uh or contributing to Linux or or open sourcing projects like Typescript and others. I think we're all part and you know obviously our you know us as stewards of GitHub uh put us at the center of it and we just wanted to make sure that we were able to earn the trust uh of the open source community by doing right by the community. In fact, it's fascinating. I've always thought about this which is when you look at companies that have used open-source and people who have contributed to open source if there was a true accounting of it at some point I think Microsoft would be at the top or if not amongst the top right in fact if you look at some quote unquote a lot of these other companies that have benefited the most from open source have hardly contributed it's never and that is I think how you know and like hey you can't complain but that's how the world rolls which is it's on nar narratives versus facts all the time.
</details>

>> 是啊，叙事与事实确实往往不一致。这确实是真的。而且我认为，90 年代遗留下来的 Windows 历史包袱影响了人们对它的看法。但我记得在开发者群体中产生最大影响的其实还不是开源本身，而是 Visual Studio Code。是的，它当然是开源的，但它也是免费的。我以前做开发时用过 Visual Studio，它太好用了，Visual Studio 2003 至今仍是一款令人惊叹的软件。而微软不知怎么就决定把 Visual Studio 以免费开源版本带给更广泛的开发者社区，结果五到十年后，它变得无处不在，每个人都在用。这是故意为之的吗？

是的，事实上，在那个时候、那个位置上的埃里希·伽玛（Erich Gamma）等人，确实完全是故意这么做的，甚至包括与社区共同构建。事实上，当我回顾产品打造过程时，那也是我第一次接触到如今人们所说的“公开构建”（building in the open）。那真正是我们所有人第一次领会公开构建的含义：拥有围绕它的社区，以及那种反馈循环。我记得当时甚至还花时间和阿曼达·西尔弗（Amanda Silver）等人交流，去了解那个团队，甚至包括产品经理——在该团队做 PM 意味着什么，他们每天如何把社区反馈作为构建产品的方式，而不是自上而下，你知道，不是那种“我听副总裁的”，而是“我倾听我的社区”。因此，在开源之外，公开构建带来了许多许多文化层面的改变，我认为这些是具有根本性变革意义的。事实上，我有时会觉得我们在那里学到了很多很棒的经验，而我们本应该学得更深、更广。

说到学得更深或更广，Visual Studio Code 当时无处不在，GitHub 表现极佳。接着迎来了 Copilot，我当时真的很惊讶。我回顾过去，发现微软那么早就意识到了 AI——在 ChatGPT 3.5 之前，我想大概是 3.0 或某个版本左右，Copilot 运行起来就如同魔法一般，而且至少有一年时间完全没有真正的竞争对手，直到 2023 年 Cursor 问世。Cursor 出来后，我依然觉得你们在 VS Code 上的布局极其聪明，因为 Cursor 就是基于大家熟悉的 VS Code 界面构建的；GitHub Copilot 和 Cursor 就这样并驾齐驱、相互竞争、亦步亦趋。随后到了 2025 年，Claude Code 凭空杀出。无论对我个人、对在初创公司工作的人、还是对大型科技公司的人来说，在 6 个月内，大家仿佛全都把 IDE 抛到了脑后。我依然感到非常非常惊讶，微软作为一家以开发者为核心、开发者基因深植于血脉之中的公司，一直以来都是如此，你觉得你们怎么会漏掉这次突如其来的转变？我第一次觉得，你们没有在第一时间拿出应对之策。
<details><summary>Original English</summary>
>> Well, it's it's narratives versus facts. That's true. And and again, I think there's that Windows legacy from the '90s that shifts people's uh you know, like how they think about it. But what I remember made the biggest impact across the developer community was not really open source. It was Visual Studio Code. Yeah, it was open source, sure, but it was also free. And I was a developer before I used Visual Studio and it was so good. Visual Studio 2003 is still amazing piece of software. and somehow you decided Microsoft to bring Visual Studio for free in an open source version to the broader dev community and boom 10 or 5 years later it's everywhere everyone was using it was that intentional yeah in fact u you know that you know Eric GMA and others who were at that time in that place really was absolutely it was intentional even building with community in fact uh you know when I look at even product making uh it was the first time I also got exposed to what I think now people talk about you know building in the open. That was really the first time we all learned what building in the open means, having the community around it and just that feedback cycle. I remember even spending time at that time with Amanda Silver and others learning how that team even the product manager what does it mean to be a PM uh on that team how they every day looked at the community feedback as a way to build versus you know top you know like it's not like a you know I listen to my vice president I listen to my community. So there were many many cultural aspects of building in the open uh beyond open source that I think were fundamentally transformative. In fact, I would say sometimes I sort of feel like we learned a lot of great lessons there. We should have learned it even more deeply and more broadly. Speaking of of learning more more deeply or more broadly, Visual Studio Code was everywhere. GitHub was doing great. And then with Copilot, I mean I was so surprised. I've been looking back how Microsoft was so early to realizing that AI before chat GPC 3.5 this was I think the 3.0 Over version or or so Copilot was working like magic and there was no real competition for at least a year until 2023 when cursor came out and then cursor came out and I still felt that you guys were super smart about VS code because cursor was based on VS code familiar interface and you know GitHub copilot and cursor were going has side by side competing with one another keeping up with one another and then out of nowhere 2025 clock code and for myself for people working at startups uh even big tech companies in 6 months everyone just forgot about the ID and I am still so so surprised that Microsoft you guys live and breathe developer DNA is in your your your DNA and it's always been how do you think you miss that this sudden shift would would come and it for the first time I felt that you didn't have an immediate response
</details>

>> 是啊，不，这是一个非常值得深入探讨的话题，对吧？我认为正如你所指出的，我们起步很早。当我们着手做这件事时，那还是 GPT-4 之前，对吧？所以当我们刚在那里起步时——
<details><summary>Original English</summary>
>> yeah no it's a it's a great uh thing to unpack right I think you to your point being early to it uh when we you know this is preGP PT4 right so when we even started there
</details>

>> 嗯，哪怕仅仅是代码补全就如同魔法一般，那其实就是 Copilot 最初的模样。你知道，如果你还记得的话，我们做了很久很久的 IntelliSense，也取得了不错的进展，然后我们惊呼：哇，这东西居然真管用。坦白讲，当时外界有很多人怀疑它到底能不能成，但它启动了。而且坦率地说，当我开始看到那一点时，我个人对缩放定律（scaling laws）的信念也从根本上得到了重塑和坚定，我们当时在努力打造那款产品方面做得相当出色。基于模型构建产品的关键之一在于：当模型发生非线性跃升时，产品形态必须迅速发生改变，对吧？这就是所谓的 AI……
<details><summary>Original English</summary>
>> um and even just the code completions were magical that was sort of really what copilot uh you know if you remember we worked on IntelliSense forever and we made good progress and then we said wow this thing is working and quite frankly there was a lot of skepticism that it would ever work but it started and that was my even my own belief in scaling laws quite frankly was uh fundamentally uh reaffirmed let's say when I started seeing that and I thought we did a good job of trying to build that product. One of the keys of building with uh models is when model jumps happen nonlinearly, the form factor has to change quickly, right? That's the you know what is AI
</details>

<!-- chunk 2/9 -->

从这个意义上说，打造第一款产品是很残酷的，因为你基本上必须围绕某个特定模型来构建一切，然后随时准备迎接下一个具有某些涌现能力的新模型，并为此重构自己，对吧？不要过分迷恋自己做出来的东西。

所以，即使在智能体编程（agentic coding）或任务处理开始变得可行的时候也是如此——不仅是代码补全，你还可以分派一些小任务。Cursor 在这方面确实做得很好，他们拿来 IDE 进行了 fork，在 Agent 模式上做得非常出色。于是我们也跟进了 Agent 模式，因为即使在 OpenAI 的模型之上，这也是可以做到的事情。

但随后触动我们的是 Anthropic 凭借他们的模型所做出的出色工作，这真正让命令行界面（CLI）成为了一种产品形态。甚至可以说，代码从输入到输出的整个过程几乎实现了全自动化处理，对吧？我认为这就是大约 6 个月内发生的转变。我们主要经历了这种变化——正如你所说的，IDE 似乎逐渐式微了，然后你真正拥有了将代码视为输出的全新思考方式。这也是为什么如果我看现在的 IDE，它更多变成了：我该如何输入规格说明（specs）、Markdown 文档以及围绕“软件工厂”的所有其他内容。这种转变改变了局势。

有趣的是，我们现在谈论这个，我个人的想法之一是：有了这些决策引擎模型，我终于又回到了 IDE。因为在某种有趣的层面上，它们有点像函数，对吧？是嵌入在软件内部的智能函数。因此我认为，随着我们考虑以更加节省 Token 的方式嵌入智能，IDE 甚至可能会迎来新生。所以我并不认为这是一种单向的永久转变。现在拥有多种产品形态，其实有助于配合模型的能力。
<details><summary>Original English</summary>
first product building in that sense is unforgiving because when you you have to be basically build everything around a given model and then be ready for the next model to have some emergent capabilities and rewire yourself for that, right? Don't be in love with what you built. So that's why even when agentic coding or task handling started becoming something that one could do right it's not just code completions but you could assign uh small tasks that's where cursor really you know they took the IDE they forked but they did a good job on really uh the agent mode and so we then caught up on the agent mode uh because that was sort of something that we could do on top of even the open AAI models but then the thing that hit us was obviously a great work that Ananthropic did uh with their model uh which then truly made the CLI as a form factor uh and then you could even just say just complete full uh handling of you know code be went from input to output effectively right I mean that I think was the transformation in 6 months or so uh we went primarily that to your point about uh uh ideides kind of faded away and then you really had this new way of thinking about code as input and that's why if I look at uh the new IDE it's more about how do I really input the specs and the markdowns and everything else around the software factory and so that transformation changes interesting enough it's funny that we're talking about it like one of the things thoughts I have is with these decision engine models finally I'm back again to IDE because you know an interesting way it's kind of like functions right it's intelligent functions that are embedded inside software so I think that there could be a rebirth even of an IDE um as we think about even embedding intelligence in a more token efficient way. So I don't say uh it's a permanent shift over in one way. It's about having multiple form factors now that actually help you with model capability.
</details>

### 决策引擎与新型软件原语

>> 我想在这里问你一下，你提到了决策模型，以及你对它们感到兴奋。我们两人最近在不同的场合都和 Diego 交流过。对于决策模型，以及大语言模型在编程任务、写代码和可靠构建软件方面的局限性，你的想法发生了怎样的变化？是的，我觉得大概就是这样，对吧？也就是说，看，我认为大语言模型非常棒，我们甚至可以讨论一下你知道……
<details><summary>Original English</summary>
>> I do want to ask you here you mentioned decision models and how you're excited about them. Both of us recently talked with the yogo and in in different different forums. How has your thinking changed on both decision models but also on the limits of LLM specifically for for programmatic tasks for for coding for for building software in a reliable way? Yeah, I think that that's kind of it, right? Which is look, I think the LLMs are fantastic and we can talk about like even how you know
</details>

>> 我们是工程师。咱们直接切入正题，谈谈它们表现不够好的地方，好吗？
<details><summary>Original English</summary>
>> we're engineers. Let's cut to the point where they're not fantastic, right?
</details>

>> 没错。从如何看待“软件工厂”的角度来说，我们可以深入探讨一整套东西。但我喜欢决策引擎的一点在于，它算是一种新的原语，对吧？正如 Diego 所讲的，以及我们自己的决策引擎和其他人所谈论的。我之所以喜欢它，是因为它有点像 Excel 宏，对吧？宏给电子表格带来的改变，也能通过将智能作为原语嵌入代码中而在编程领域发生，对吧？

比如在构建任何系统时——我想我之前看过他们为了管理所有社区反馈而构建的一个 Xbox 系统，对吧？这是个典型场景：社区反馈来了，我基于它做出一组决策。我并不想真正用大语言模型为此生成代码，我只是希望能够做出决策。所以嵌入这种原语更好，对吧？它有一个分布，你可以发起一次调用，它不需要一次又一次地重复生成，而且具有 Token 效率。因此我认为，这是软件工程依然保持生机的领域之一。

它正在发生变化。关于 Diego 的理念，我喜欢的一点是他希望让它变得像数据库一样枯燥。事实上对我而言，关系型数据库……在我的成长历程中，在开发者工具链里，除了编译器、Lex 和 Yacc 等工具之外，我最喜欢的产品就是数据库。因为关系型数据库是一种能够可靠存储、查询信息的途径，它让各种应用程序的诞生成为可能。我认为在智能时代，决策引擎也会起到同样的作用。

事实上，数据库就是核心。我们常讨论一家软件公司的本质是什么，是业务逻辑，对吧？但当你往深层看，它往往存在于数据库中。实际上，过去有那么多业务逻辑都是写在存储过程或事务这些东西里的。所以我想知道这是否是一个恰当的类比。
<details><summary>Original English</summary>
>> Right. uh in the sense of how do you even think about uh the software factory and there's an entire thing that we can go into but the a what I love about decision engines is it's kind of a new primitive right and how Diego talks about it and how our own decision engine and others are talking about it and I like that because you know it's kind of like you know Excel macros right you know what happened to spreadsheets with macros can happen with code with intelligence embedded as a primitive right And so I don't know you build any system like I think I was looking at an Xbox system that they had built for managing all of the community feedback right it's a classic community feedback comes I make a set of decisions based on it I don't want to really generate LLM code on it I just want to be able to make decisions so it's better to embed this primitive right it has a distribution you can make a call it's sort of a uh it doesn't need to be generated again and again it's token efficient uh and So I think that this is one of those places where software engineering remains very much alive. It's changing. One of the things I like about Diego's thing is he wants to make it as boring as databases. In fact, to me, a relational database. I grew up with my my my like the most favorite product uh in the developer chain other than the compilers and the lex and yak and what have you was the database because the relational database is a reliable way to be able to store query uh your information just made all kinds of applications possible and I think decision engines in the era of intelligence will also do the same. Well, in fact, the databases are the hard and so we talk about what is the essence of a software company. It's the business logic, right? But when you go deeper, it's often in the database. In fact, so much of the business logic used to be coded in store transactions, some of these things. So, I wonder if it's a good one.
</details>

>> 这就像是智能时代的存储过程。
<details><summary>Original English</summary>
>> It's like it's a like this is the stored procedure of the intelligence era.
</details>

>> 是的。所以我想知道是否存在这样的类比或希望，因为我确实觉得我们还没有找到合适的新原语。比如我们知道大模型可以生成代码，我们可以用大模型来处理一些容错率高、不可靠的事情，但我们仍然缺少这类基础原语，对吧？
<details><summary>Original English</summary>
>> Yeah. So, so I wonder if there's an analogy or a hope because I do see that we haven't found the right primitive like we know that LMS can generate code. we can use LMS to do unreliable stuff but we still we're missing these kind of primitives right
</details>

### 软件工厂与代码验证难题

>> 对，对，所以我对此感到非常兴奋。我认为这正是一个开端。因为另一个挑战在于——我们把话题切到“软件工厂”一会儿，对吧？如果你看看今天无论是 Co-work 是如何构建的，还是 GitHub Copilot runtime 是如何构建的，大家都写过相关的博客，这非常引人入胜，对吧？在代码生成变得廉价的世界里，变得困难的反而是验证，对吧？

实际上，有时我甚至会觉得：天哪，我真想去参加 Mark Russinovich 和 Scott Hanselman 他们搞的那个叫什么导学项目（perceptorship）之类的活动，因为我感觉自己必须去学习，毕竟我还没有在如今主要以“代码作为输出”的团队里工作过。但代码作为输出是有特定操作顺序的，并不是说代码作为输出就意味着大家只是在胡乱生成各种随意的代码。关键在于你如何构建验证体系，如何把每一次失败转化为测试用例，并确保真正验证了测试，对吧？

我的意思是，在管理复杂的软件项目中，人们正在积累非常多新型的“部落知识”（隐性实践经验）。事实上，这甚至可能是一场噩梦，我想即便是在他们正在进行的 Rust 迁移中，他们也不得不进行回滚。因此，这里面包含了所谓的巨大优势，也有一些巨大的劣势。这就是为什么正如你所指出的，拥有类似决策引擎这样的额外原语，我认为是非常有益的。
<details><summary>Original English</summary>
>> yeah yeah so I'm very excited about it and this is I think the beginning of how you know because one of the other challenges you know so let's go to the software factory for a second right if you look at even how co-work is built or even the GitHub copilot runtime is built today and you know I think people have blogged about it and it's fascinating right you know in a world where code generation has become cheap what has become hard is verification right in fact one of the things that I feel like oh my god I wish you know I want to join one of these Mark Renovich Scott Henselman you know perceptor ships or whatever they call because I kind of feel like I got to learn because I've not worked in a team that is mostly now code as output right but the code is output has a particular order of operations it's not like code is output means everybody's just generating all sorts of random code like the way you got to build the verification stuff how do you take every failure and then build back the test case and make sure you truly verify the test right I mean there's just so much I would say new type of tribal knowledge people are building up in managing complex software projects in fact it was a nightmare I think even in that rust migration they were having they had to revert back um and so that is sort of all the quote the great advantages and some massive disadvantages so that's why to your point having additional primitives like this uh decision engine I think are good
</details>

>> 你提到作为这样一家卓越公司的 CEO，你能看到所有事情的发生，对吧？你统揽全局，获取各种信息。如果有机会，你甚至会想去一线团队工作。
<details><summary>Original English</summary>
>> and you mentioned that as a as a CEO of of like this amazing company, you see all of the things happening, right? You oversee, you get information, you would want to go and work on a team if you could.
</details>

>> 噢，绝对是这样。事实上，我梦想中的下一份工作就是这个，对吧？如果我能回去，成为其中的一员。其实很有意思的一件事是，我正打算给 Scott 和 Mark 发邮件，跟他们说：嘿，你们在微软内部发起的这个名为 perceptorship 的新项目做得太棒了。我想他们甚至和卡耐基梅隆大学之类的高校有合作。这种能让刚踏入职场的新人也能加入进来的想法——因为我非常关心刚入行的新人能否加入这类团队并沿着学习曲线快速成长。

因为回想以前的学习曲线，我记得人们来微软实习时，他们会去看：嘿，Cutler 的代码是怎么写的？我怎么去查看 malloc 的实现？那么，现在的对应形式是什么？这正是我们必须真正去探索的。所以是的，如果有机会，我希望有一天能再次做这些事情。
<details><summary>Original English</summary>
>> Oh, absolutely. In fact, you know, my dream next job would be that, right? if I could go back and just be part in fact in fact one of the things that's interesting you know I was going to send mail to Scott and Mark and say hey they're doing an unbelievable job of creating this new program inside of Microsoft uh called perceptorship I think they even have a relationship with Carnegie Melon or something and that idea that you can have people who can come in even early in career because I care a lot about hey can you have an early in career person come in join one of these teams go up the learning curve because I think the learning curve I Remember people used to come to Microsoft for an internship. they would go see hey how is you know Cutler's code how do I go look at the Malo implementation so what's the new form of that is what I think we have to really discover and so yes if we you know my hope would be one day I get to do that again
</details>

>> 我现在理解为什么这么多 CTO、工程副总裁（VP of Engineering）和高级副总裁（SVP）会主动降职去小团队工作了，就是为了学习如何利用这些新工具进行构建。现在似乎一切都在发生变化。
<details><summary>Original English</summary>
>> I'm now understanding why so many CTO's uh VP of engineering SVPs do take step downs to work on small teams to learn how to build with with these new tools right now seems all is changing
</details>

>> 确实是这样。我认为整件事情的组织架构层面的背景正在发生改变。如果深入思考这一点，我认为这非常重要。事实上，在许多方面发生剧烈变革的时期，更加亲力亲为、紧密贴近客户、以开源公开的方式构建，在关乎优秀产品或成功技术构成的方方面面，都有太多东西需要去学习，因此这其中蕴含着大量的机会。
<details><summary>Original English</summary>
>> I absolutely I think yeah the organization ational sort of context of it all uh is changing that I think yeah if I um if I think about it I think it's very important in fact you know being a lot more hands-on at a time of great change on many fronts right by the way being close to customers building in the open there's so much to learn on all aspects of what makes successful products or successful technology uh that yeah there's a plenty of opportunity
</details>

>> 我们刚才已经多次提到“软件工厂”这个词了……
<details><summary>Original English</summary>
>> we've now been throwing around the the term software factory for a little bit
</details>

<!-- chunk 3/9 -->

### 软件工厂与开发范式的转变

所以，我们具体来聊聊这个。我觉得这个词虽然有点模糊，但正逐渐被大家接受。对你来说，它意味着什么？
<details><summary>Original English</summary>
so so let's let's actually talk about it. I feel this term is a bit vague but it's coming around. What does it mean for you?
</details>

>> 是的。其实我也还在逐步摸索和理解中。我正在做的是模式匹配，对照当今软件团队中的人员都在做些什么。我想建议你的观众去看看 Bass 写的那篇博文。实际上有两篇很棒的博文，一篇来自 Cowork 团队，另一篇来自 GitHub Copilot 团队。两个团队都发布了博文。其中一篇讲的是单个开发者
<details><summary>Original English</summary>
>> Yeah. So I'm also still kind of coming to grips with it. So I'm pattern matching um in what is teams of people in a software team today do right. So you know I think I'd point your viewers to uh the the blog that Bass wrote. I mean in fact there are two nice blogs right the co-work team and the GitHub copilot uh team. Both of them have these blogs out. one is what one what and one individual developer
</details>

>> 能够做到什么——那是 GitHub 团队那边的案例，也就是维护整个运行环境，而且我想他们还进行了迁移，我记不清是不是从 Python 迁移到了 Rust……
<details><summary>Original English</summary>
>> was able to do that was on the GitHub side which is maintain an entire runtime um and re you know I think they also migrated I forget whether it's from Python I guess to rust um
</details>

>> 总是迁移到 Rust［笑声］。
<details><summary>Original English</summary>
>> it's always to rust [laughter]
</details>

>> 迁移到 Rust。不过无论如何，那都是一个绝佳的案例研究，展现了单个开发者的生产力，以及进行这种维护工作意味着什么。然后还有那个团队，我想大概是 9 到 12 名工程师之类的，整个团队的总规模居然只有这么大，这挺不可思议的，也就是那个软件工厂。他们也写了一篇很好的博文。但里面有太多我喜欢的内容了，如果我可以加入那个团队，去真正一线切身体会，而不是仅仅阅读博文或与 Bass 及其团队交谈就好了。

举例来说，据我理解，最根本的转变之一，是代码已经从输入变成了输出，这太棒了。接着你不得不意识到，这意味着规格说明与意图变得至关重要，而这向来都很重要，［清嗓子］设计文档一直都很重要，还有……
<details><summary>Original English</summary>
>> to rust uh but nevertheless they kind of that's a beautiful case study of what the productivity of a single developer and what does it mean to do that maintenance and so on then there is the team I think it's nine or 12 or whatever number of engineers it's kind of crazy that that's the total size of that team um and the software factory and they've also done a nice blog but there's so many things there I love I mean this is where you know uh if if I could just go join that team and really learn it firsthand versus just reading blogs or talking to bass and team but for example the fundamental transformation as I understand it is right one is code has gone from being input to output great then you kind of have to say okay that means specification and intent right which was always important [clears throat] design docs were important and so
</details>

>> 对齐。
<details><summary>Original English</summary>
>> alignment
</details>

>> 对齐，所以这现在变得非常重要。
<details><summary>Original English</summary>
>> align and so that that's kind of yeah very important now
</details>

>> 我发现的另一件极具吸引力的事情是——我曾与一位刚入职不久的新人交谈过——现在融入一个代码库其实容易得多了。原因在于，当你管理一个软件工厂时，所有东西都有文档记录。
<details><summary>Original English</summary>
>> the other fascinating thing I'm also finding is and I talked to one uh sort of early in career uh person who went in getting into a code base now is actually much easier because the reason when you're managing a software factory everything is documented
</details>

>> 是的，而且你还可以向它提问，它就像一个有耐心的导师、一位带你熟悉环境的伙伴。
<details><summary>Original English</summary>
>> um and so and then you can you can ask it questions patient mentor onboarding buddy.
</details>

>> 没错。这样一来，你融入一个代码库的过程就会轻松得多，不再需要在大家脑海中的所谓默会知识里到处翻找。

另外，我也在深入了解这种验证机制。也就是说，要进行智能体编程，你交给它这些微小的任务，就必须确保它真正做完了。你如何进行审查批判？关于使用独立的模型族，有太多值得探讨的地方。事实上，这也是我一直担心的一点：如果只有一个模型族，而这些模型族都会存在各种对齐问题，那你该如何通过审查批判，来确保某一个模型族的缺陷不会变成你的缺陷？

总之，我认为一种全新的构建方式正在浮现，这就是新型软件工程，它仍然需要软件工程师。这只是一种交互层面的变化，也许正因如此，我很喜欢那个类比：当年你从自己编写汇编代码，变成惊叹“哇，我有了编译器”，突然间你觉得“哇，我现在可以直接从意图生成代码，而且不需要懂汇编了”。这当中有类似的成分，它是一个抽象层。但团队内部的协作方式改变了，构建产品的方式也改变了。

另一件让我非常兴奋的事，是来自生产环境的追踪链路能够回传。我也很喜欢这一点，也就是……
<details><summary>Original English</summary>
>> Exactly. And so you can have you your onboarding onto a codebase is so much more easier than you scrging around for tribal knowledge that's in people's heads if you will. Right. So the other thing is I'm learning a lot about this verification stuff right which is the way you want to do agentic coding is like these little tasks that you give it make sure that it's truly done. How do you have the critique? Right? There's so much to be said about having a separate model family. In fact, that's the other thing that I I I've always worried about. It's like, hey, if there's one model family and these model families are going to have all these alignment issues, how do you use a critique to ensure that one model family's challenge doesn't become your challenge? And so anyway, I I kind of look at say there's an entire new way to build uh that is emerging and it's new software engineering and it requires software engineers. It's just a level of interaction maybe that's why I like the even the analogy of you know when you know uh you went from writing your own assembly to saying oh wow I have a compiler um and suddenly you felt like oh wow I can now go from intent to code and I don't need to know assembly there's a little bit of that it's a level of abstraction but even how you work in a team has changed and how you construct a product has changed the other one that I'm really excited about is um the the traces from production coming back. I love that too, right? Which is, you know,
</details>

>> 我们谈论的是可观测性，但你有了更多机会。
<details><summary>Original English</summary>
>> we're talking observability, but you have more more opportunities.
</details>

>> 是的。当人们谈论 RSI 这类概念时，那也算是我理解的 RSI，即获取生产日志并能够验证修复方案的能力。事实上，这种可验证性闭环非常出色，你可以随后部署修复，一路部署并确保它完全通过了所有测试。这确实非常有帮助。所以我认为这些团队正在积累大量经验，并且正在微软内部广泛传播。看到这如今成为团队组织架构的方式，真的令人振奋。

另一个我很喜欢的案例是我们的网络团队，Azure 网络团队。这曾是我最喜欢的故事：该团队表示，“微软为我们的全球网络管理着全球大约 500 家光纤运营商。”你知道，物理资产总会出这样那样的状况。管理这一切的华丽辞藻叫 DevOps，但现实中全靠电子邮件和各种临时拼凑的流程。于是他们去构建了一整套智能体系统来实际执行运维，而且这些运维甚至与他们的代码仓库相连。这样一来，现在不仅仅是代码仓库本身或代码库，连围绕它的运维工作都被纳入其中。你可以开始看到，技术团队的工作本质正在转变成构建这些由“运维加软件”组成的工厂来完成工作，而不是亲手去操作具体任务。不过他们依然在做工作，只是形式略有不同。
<details><summary>Original English</summary>
>> Yeah. I mean, when people say like, you know, RSI, that's kind of my RSI, right? Which is it's sort of the ability to take my production logs and then to be able to verify the fix. In fact, that verifiability loop is great that you can then deploy the fix and deploy it all the way through that it actually passed all the tests. Uh, that actually is very helpful. And so I think there's a lot of learning uh that these teams are having and it's spreading across Microsoft. I mean uh it's just good to see how this is now becoming the way teams are structuring. The other one that I love um is our networking Azure networking team, right? In fact, my that used to be my favorite story where this team said, "Hey, we you know Microsoft manages something like 500 fiber operators all over the world for our global network." And you know, always it's a physical asset something or the other goes wrong. You know, the fancy word for managing all that is DevOps, but the reality is it's emails and you know, all sorts of ad hoc processes. And so they went and built this entire Egyptic system that actually does the ops and that ops is connected even uh to their repos. And so now it's not just the repo on its own or the codebase but it's even the operations that are around it. And so you can start seeing how the nature of what technical teams do is build these factories of ops plus uh software that do the job versus doing the job. But still they're doing a job which is slightly different.
</details>

### 棕地项目与软件工厂落地

>> 我很想知道，因为在 AI 实验室里，这种情况很普遍，他们也非常乐于公开分享那里的软件工程师的工作如何变成了促使回路中的智能体做得更好。正如你刚才所说，但如果落实到实际层面，比如在微软这样的地方，你们既有可以进行实验的团队——他们正在构建新的工厂，或者是平台团队，也许有多余的人力周期来做这些事情——但同时你们也有真正拥有产品的产品团队。你们有真正的客户。

正是在这一点上，我看到很多拥有实际业务的公司感到纠结：他们看到 AI 实验室这些令人向往的远景，或者他们此刻正听着你的分享，他们会想：“等一下，我不可能扔下眼前的一切去建个工厂，因为那我现有的业务该怎么办？”你对这种平衡是怎么看的？尤其是在微软内部，你会对工程师说些什么？他们的工作正在发生怎样的变化，特别是当你负责的产品本身就是一款优秀、盈利且有客户依赖的产品时？
<details><summary>Original English</summary>
>> I I do wonder because an AI labs uh it's it's pretty common and and they're very open about sharing how software engineers there their job is becoming to allow the agent and the loop to do a better job. So, so what you just said, but just sticking to practical level like at a place like Microsoft, you're you will have teams that can experiment and they're building new factories or or their platform teams and maybe they have extra cycles and they're doing all these things, but you also have product teams who actually have a product. you have real customers and this is where I see a lot of companies struggle with who do have a real business and they're seeing these aspirational things from AI labs or maybe even they're listening to you right now and they're thinking hang on like I can't just drop everything and build a factory because what am I going to do with with the thing how how are you thinking about both this balance and especially inside of Microsoft what what do you tell engineers like how is your job changing especially when you're working on a product that is a good product it's a profitable product customers depend on it
</details>

>> 是的，问得很好。首先，我们没有权力去做那些无法为客户带来价值的事。我们就从这点谈起。正如你所说，我们也犯过自己的错误，比如仅仅因为某些 AI 功能看起来很酷就随意去做。最终你总是要……
<details><summary>Original English</summary>
>> yeah it's a great point I mean like first of all you know We don't get permission to do things that are not adding value to customers. Like let's start there to your point about a little bit of and we made our share of mistakes of you know going and doing random AI things just because they were you know you know cool to do. You kind of ultimately are going to
</details>

>> 我想大家都经历过。
<details><summary>Original English</summary>
>> I think everyone's done that.
</details>

>> 大家都经历过，我也没少做这种事，并希望能从中吸取教训，不断改进。

但话虽如此，如果换个角度，让我们正视现实：如今当我审视 Windows 中的 CVE 漏洞时，因为现在有 AI 模型在寻找漏洞，对吧？是的。所以我们现在必须去把它们全部修复。因此，这就产生了一条新的流水线。所以实际上，即使我观察 Windows 从崩溃链路回溯一直到修复的全过程，他们实质上都在构建一种新型的软件工厂。

只不过这是一个“棕地”环境，对吧？Windows 的构建系统仍然是原来的 Windows 构建系统。事实上，在所有这些棕地项目中，最困难的部分正是构建和 CI/CD。
<details><summary>Original English</summary>
>> Everyone's done that and I've done my fair share of it and learned from it hopefully and we'll get better. But that said, if you sort of say, well, let's take even let's face it, right, which is today when I look at the CVE in Windows, right? Um because you now have AI models that are finding vulnerabilities. Yep. And so we now need to go fix them all. And so therefore, there's a new pipeline. So in fact, if I look at even the windows from crash traces all the way to fixes, they're building out essentially a new type of software factory except this is a brown field, right? which is the build system of Windows still is still the build system of Windows. In fact, if you think about in all these brownfield projects, the most difficult part is builds and CI/CD.
</details>

>> 嗯，然后当然你还必须真正面对……如果我看看连 GitHub 底层所经历的变化量，仔细想想，突然之间所有这些代码编写智能体都涌入 GitHub 开始工作，规模激增至……
<details><summary>Original English</summary>
>> Um and then of course you got to really you know even you know if I look at the amount of change that underneath even GitHub right which is if you think about it right you know we've had I mean suddenly all these coding agents showed up to work at GitHub and the scale has gone through the roof
</details>

>> 超人级别。
<details><summary>Original English</summary>
>> superhuman level.
</details>

>> 是的。因此我们必须从根本上彻底改变整个 Git 协议和存储系统。我们正在对其中的每个部分进行改造，以确保我们能适应这种棕地环境。绿地项目我们固然总会去做，但现实世界完全是由棕地组成的。而在棕地中，需要对系统进行逐步的加固，重新审视核心原语，从源代码版本控制到构建再到 CI/CD，使其能够在一个棕地项目中行之有效，并且……
<details><summary>Original English</summary>
>> Yeah. And so therefore we have to fundamentally change the entire the git protocol the storage system. We are working on every part of this to make sure that we are living in the brown field as opposed to I mean the green field stuff we'll always do but the real world is all about brownfield and the brownfield requires stepwise you know hardening of systems rethinking of the the core primitives right all the way from source code control to build to CI/CD that works in a brownfield project and that
</details>

<!-- chunk 4/9 -->

### 这一轮 AI 变革有何不同

这需要时间，需要投入，需要思考，而且操作的次序——或者说操作顺序——非常非常关键。所以，关于这次转型，我喜欢的一点在于，它并不是说“看，这里有个崭新的新玩意儿，这是在做那个的团队，而其他人全都生活在旧世界里”。而是全公司上下每个人都能用上新的工具链和新的工作方式，在任何产品上面对眼前的挑战，不论是 Windows、SQL Server 还是云原生服务等等，我认为这就是我们正在看到的。

说实话，这听起来和我们过去做的事情并没有那么大的不同，因为当出现一项新技术时——比方说 React，作为一种新的前端技术——每个人都想用它。而我们当时的做法是，没有人获准直接停下手头的工作去迁移到 React。但当你构建新产品或添加新功能时，你开始把它加进去，开始把它融合进来。所以，也许这和我们采用 AI 的方式并没有那么大区别。但这件事到底有什么不同之处呢？真的有不同吗？
<details><summary>Original English</summary>
takes time that takes investment that takes uh thought and the sequence of oper operations or the order of operations is very very critical. So one of the things that I want our teams is is not about well one nice thing I like about the transformation is this is not about oh here is some new shiny object and here is the team that's doing that and everybody else lives in the uh old world like everybody across the company gets to use the new tool chain and the new ways of working and tackle the challenge in front of them on any product whether it's Windows or SQL server or a cloudnative service what have you and that I think is what we're seeing

To be fair, like this doesn't sound all that different to what we did in the past because when there was a new technology, let's say React, which was a new front-end technology, everyone wanted to use it. And what we did is no one got permission to just stop and migrate to React. But when you built a new product or you added a new feature, you start to add it in, you start to mix it. So maybe it's not all that different to how we're adopting AI. But but what is different about this? Is it?
</details>

>> 这个问题提得很好。你知道，有时候我也会说：“是啊，我以前见过这种场面，诸如此类。”但我确实觉得这一次有所不同的一点在于，我们做事情的基础逻辑，对吧，也就是那种操作顺序、抽象层次。其实我觉得最引人入胜的事情之一，就像当年人们的转变一样。我刚步入职场的时候，正赶上我们转变的关口——在大学里，我大部分时间其实是在 VAX 上工作，你知道，用的是 VT 终端，呃……
<details><summary>Original English</summary>
>> It's a good one. Like, you know, sometimes I I you know, I kind of say, "Yeah, I've seen this before and what have you." But I think the one thing that I do feel that's different this time around is that the the physics of how we do things right that order of operations the level of abstraction maybe in fact one of the fascinating things I think about is it is like when people moved right I I I joined the workforce at the cusp of when we went from you know in in fact in college I was mostly working on a vax right you know with a VT you know terminal uh
</details>

>> 这是大型机。
<details><summary>Original English</summary>
>> this is a mainframe
</details>

>> 是的，或者是小型机，小型机，对，VMS 系统，对吧。然后，接着我在 Sun 工作了几年，用的是工作站，之后我来到了微软。再后来，世界基本上就稳定下来了，对吧，在我的职业生涯中，你主要是在 IDE 里写代码，这基本上没怎么变过。我的意思是，新技术不断涌现，但所有那些新技术都属于新的框架和新的运行时，并不是概念的数量发生了根本性的改变。即便是移动设备，某种程度上也是一种小型化的 PC，配上了新的用户界面，对吧，以及新的框架。而现在这个阶段，一切都在变——什么是运行时？什么是框架？什么是 IDE？什么是技术栈？
<details><summary>Original English</summary>
>> yeah or a mini uh mini right VMS systems right so and then and then I joined actually for a couple of years at sun on a workstation and then I came to Microsoft and so and then you know the world kind of was stable right you mostly wrote code in an IDE throughout my professional career it sort of didn't really change I mean new technologies came but all those new technologies were new frameworks and new runtimes it was not like con the concept count radically changed Even the mobile thing was sort of a miniaturized PC with new sort of uh user you know user interface right and new frameworks this is a place where everything what is the runtime what is the framework what is the IDE what's the stack
</details>

>> 你说得对，全都在变，每一个都是。
<details><summary>Original English</summary>
>> you're right all every single
</details>

>> 每一部分都在变。我认为这在很大程度上更是思维方式上的转变。而且别忘了，随时可能发布一个新模型，对吧？无论是一个新的前沿模型，还是像决策引擎这样的新事物，一切又可能再次改变，对吧？我认为这就是我们必须随时准备好迎接整个格局在任何时刻彻底转变的地方。因此，我认为至少有两点是我想到的：一方面是从过去汲取经验，回想我们个人、公司或团队在应对变革时表现最出色的时期，我认为这始终很重要；但另一方面，保持开放的心态，认识到这次确实不同，这也是很有益的。
<details><summary>Original English</summary>
>> par it's a little more of a change in how you think about I think then let's not forget a new model could drop right whether it is a new uh frontier model or a new thing like decision engine and it could change again, right? This is where I think we also have to be ready for the regime to completely be transformed uh at any moment if you will. And so therefore, I think these are two things at least I think about that thinking of it learning from the past when we were at our best individually or as companies or as teams in managing change I think is always important but also being open-minded that this time is different is also good.
</details>

>> 是的。而且具体到对我们软件工程师来说最大的变化——你知道，微软的大多数员工可能都是软件工程师，或者与代码打交道的人——我们过去大部分时间都在写代码，我们大部分精力都是在大学和之前的工作中学习如何精通这一点。而这一部分突然消失了，我知道对很多人来说——包括早些时候的我——这很难去调和接受，因为我们在以往任何技术变革中都未曾见过这种情况，过去总是在增加新工具。对于微软内部或外部与你交流的人，那些极其优秀的工程师，他们花了数十年时间才精通编写代码（这本就很不容易），你如何看待他们去调和并接受这一点？

对，没错，我认为就是这样。所以这正是我至少观察到的情况。甚至当我与那些以前是优秀软件工程师、如今在新的生产模式下依然硕果累累的人交流时，他们仍然需要相同的技能。只是重申一下，你所考虑的操作顺序、工具链发生了改变。这也是我认为这绝非贬低专业技能价值的另一个原因。这是关于真正利用好专业技能，并确保你能借助新的杠杆来发挥它，对吧？这就是你的工作本质必须改变的地方，而不是认为软件工程不再重要了。我认为我们正处于这样一个阶段，我们在努力摸索如何评估新事物的价值，而在评估新事物价值的过程中，你突然甚至会开始重新重视旧事物的价值，不知道你是否理解。当我观察大家时，显然有人是 AI 原生代的，他们来自——事实上挺有意思的，在上一届 GitHub Universe 上，我过去见了一群大学生，那是第一批在 AI 时代成长起来的大学毕业生，对吧，因为他们上大学时……
<details><summary>Original English</summary>
>> Yeah. And and also specifically for for the biggest change for us software engineers and you know Microsoft has probably majority of the workforce is software engineers or people close to the code is we used to spend most of our time writing code and most of our effort was learning at college at previous jobs to be good at this and this part suddenly disappeared which I know for a lot of people including me for for earlier it it was hard to reconcile cuz we've never seen it with any technology change it always added a new a new tool How do you see people inside of Microsoft or or outside who you talk with reconcile this who who are are really good engineers and they've spent decades getting very good at coding which is hard to do right yeah no I think that that's right I think so this is where what at least I am observing and as I talk to even people uh who are you know both been great software engineers uh previously and now are prolific even in the new mode of production is the same skills are still required. It's just again that the what you think about the order of operations, the tool chain um has changed. And so that's one of the other reasons where I don't think it's about devaluing the expertise. It's about really taking the expertise and making sure that you can exercise that with new leverage. Right? That is where the nature of how you work has to change as opposed to thinking that this is about uh software engineering no longer being important and I think that we're in that phase right uh where we are trying to figure out how to value the new thing and in valuing the new thing you are suddenly going to even start valuing the old thing if it makes sense right which is when I look at the people there's obviously somebody who is AI native who comes out of like in fact it is funny last last GitHub universe uh I went down and I met a bunch of uh college kids and this that was the first batch of college graduates who grew up in the AI era right because they went to college
</details>

>> 正值 GitHub Copilot 推出的时候。
<details><summary>Original English</summary>
>> when GitHub copilot co-pilot
</details>

>> 对，所以他们不知道在 GitHub Copilot 之前的 IDE 世界是什么样的。对我来说，看到这种情况正在发生，感到非常震惊。所以，将会有一批原生适应这套工具链的人加入进来。但我同样认为，在微软，任何在某个领域拥有深厚专业功底、保持好奇心并且在学习新工作方式的人，在这个新环境中都绝对在大放异彩。因此，我希望确保的事情之一，就是为大家创造这样的机会，因为归根结底，职业生涯的经济回报才是最重要的。因此，我们希望确保在微软，你既能重视自己现有的技能组合，又能构建起市场认可的新技能组合。
<details><summary>Original English</summary>
>> right they so they didn't know an IDE world pre GitHub copilot it was like stunning to me that that was sort of what's happening so there's going to be people who are going to come at this who are quot going to be native to this tool chain but I also think that people when I see at Microsoft anyone who has great depth and expertise in any part has curiosity and is sort of learning the new ways to work are absolutely flourishing in it. And so one of the things I I'm hoping to ensure is we create that opportunity for folks because at the end of the day, right, you know, it's about economic return on your professional careers that matters. And so therefore, we want to make sure at Microsoft you can both value the skill set you have and build the new skill set that the marketplace will value.
</details>

### 自愿退休计划与未来团队形态

>> 我非常喜欢你对这件事的看法，以及你谈到的初级工程师、应届毕业生和处于职业早期的人如何做出贡献，他们能够迅速跟上节奏。但开发者圈子里流传着一件事——我就直接跟你直说了——大家都在猜测：为什么微软会提供自愿退休方案？这到底意味着什么？存在这样一种担忧：这会不会是因为 AI 提升了团队效率而可能引发裁员的前奏？我就是想直截了当地问你，微软以前从未有过类似的事情，这其实是我最关注的一点，还有它完全是自愿的这一点。对于这件事，你个人的想法和公司的考量是如何结合在一起的？

这是一个非常重要的问题。我们进行了大量讨论，我们觉得需要明确两点，或者说是三点：第一，我们必须承认，未来会有大量机遇，但这些机遇的形式可能与以往的机遇有所不同，对吧？如果我们甚至狭隘地仅仅考虑刚才讨论的软件工程……
<details><summary>Original English</summary>
>> I'm really liking how you're looking at this and also how you talked about how junior new new grads, early career people are contributing. they can get up up to speed. But one thing that's been going around in dev circles, and I I'll just lay it out for you, is people are speculating, why is it that that Microsoft is making the voluntary retirement offers? Like, what does this mean? There's this fear that could this be a prelude to potentially a layoff because of AI making teams more efficient? And I just wanted to ask you dead on the head, there's never been anything like this at Microsoft, which is what I actually paid most attention to. and also the fact that it is voluntary. How did your your thinking and the company's thinking come together on this one? It's a it's a very important question and you know one of the things that we discussed a lot and we felt was let's acknowledge two things right one is that or maybe three things one is that let's acknowledge that there is going to be plenty of opportunity going forward the shape of that opportunity may be different than what is the opportunity right if you let's even narrowly think about just software engineering as we were discussing
</details>

>> 那我们就从这里切入。
<details><summary>Original English</summary>
>> so let's start there
</details>

>> 那么接下来我们应该说：好，太棒了，让我们在公司内部创造更多这种新的机遇，对吧？这就是我们讨论的一切的核心，坦率地说，无论你是从事 Windows 工作还是从事 AI 训练，你都能真正掌握新的技能，这些技能在微软内部以及在市场上都将极具价值，对吧？
<details><summary>Original English</summary>
>> then the next thing we should say is okay Great. Let's create more of that new opportunity inside uh the company, right? That's where everything that we're talking about, whether you're working on Windows or whether you're working on AI training, quite frankly, you get to really equip yourself with new skills that are going to be valuable inside of Microsoft and in the marketplace, right?
</details>

>> 是的。
<details><summary>Original English</summary>
>> Yes.
</details>

>> 但这种新事物的形态将会与以往的形态不同，对吧？团队规模、团队工作流程都会有所不同。所以我们需要明确，并不是说我们不希望微软的 20 万员工全都蓬勃发展、甚至进一步增长，而是微软这 20 万人以及未来的增长，必须以不同的方式来进行配置。对吧，甚至当我观察微软内部的一些情况，比方说经济回报方面，如果你看看系统工程师或者基础设施人员的薪资，那是极高的。同样，如果你是一名……
<details><summary>Original English</summary>
>> But the shape of what this new thing looks like is going to be different than what the shape of what it was before, right? team team sizes team workflows. So we need to take it's not that we don't want the 200,000 people at Microsoft flourishing all of them and growing even but the the 200,000 people at Microsoft and growing will have to be configured in different ways right when I look at even at inside of Microsoft some of even let's say even the economic return right if you look at the wages for a systems engineer right or an infrastructure person is through the roof same thing if you are a
</details>

<!-- chunk 5/9 -->

### 给员工更多自主权与应对 AI 焦虑

……处于培养阶段的研究人员，对吧？所以有些专业技能具有很强的竞争力和极高的价值，对吧？因此我们希望给予大家更多的自主权。坦白讲，实际上，这次自愿离职的举措主要是为了给大家更多自主权，让他们能够去到从长期来看对自己经济机会更有意义的位置。我认为这是最关键的一点。你知道，我当 CEO 已经很久了。在此之前我是高级管理层等等。但归根结底，我也是从一线员工（IC）一步步成长到这个职位的。所以我常常回想自己做一线员工或主管（lead）、甚至是主管的经理时的经历，这就是我看待公司内部应该如何创造机会的视角。

即便在微软内部，我也不希望被困在一个不进行转型的团队里。我们得面对现实，对吧？我不可能坐在这里说微软的每一个部门都真正领会了精神，并且都在按照期望进行转型。我想给他们这种选择，如果你身处一个让你在职业上感到停滞不前的团队，你可以用脚投票。我并不希望你离开微软，因为坦白讲，在微软内部你就有许多地方可以去。所以那是我们希望创造的另一个机会。在这样的背景下，我们正在努力给予人们更多的自主权。同时我们也意识到这是一个动荡的时期，对吧？我也希望自己能坐在这里说一切都会照旧，但我做不到，对吧？而且，这是我希望对变革保持完全透明的领域之一。我想确保我们——确保我做好切实的工作，在公司内部创造所有的机会，然后确保我们的员工队伍能够在这里真正实现他们的职业成长。
<details><summary>Original English</summary>
researcher in training right so some of the expert ertise is highly competitive, highly valued, right? And so we want to give more agency. Quite frankly, in fact, this voluntary thing was mostly about let's give everybody more agency to get themselves slaughtered into places uh that make sense for their economic opportunity long term. That's I think the key thing. You know, I've been CEO for a long time. I was a senior exec before that and what have you. But at the end of the day though I did grow up as from an IC to this right. So I think about lot of the times when I was an IC or a lead right and maybe uh a manager of uh leads that's sort of the lens through which I think about how should we create opportunity inside the company. I don't want to be stuck in a team that's not transforming even inside of Microsoft. Let's face it, right? It's not like I can sit here and say every part of Microsoft is sort of really got the memo and they're all transforming at the eap I want to give them you know if you if you're in a team where you feel stuck professionally uh you can vote with your feet I don't want you to because quite frankly there are many places you can go inside of Microsoft itself. So that is another opportunity we want to create. So in that context, we are trying to give more agency to people. Uh realizing that this is a time of tumult, right? I I wish I could just sit here and say it'll all be the same. I cannot, right? And you know, and and you know, this is one of those places where I I want to be as transparent about the change. I want to make sure we do I I do the hard work of creating all the opportunity at the company and then make sure that our workforce is able to really make their professional growth come true here.
</details>

>> 我的意思是，我认为你这番话说得非常得体且周到，但如果让我来解读的话，那就是世界已经发生了巨大的变化。例如我们看到 Claude Code 的发展是如此迅速，而那些在方向盘前睡着了的团队（如果你愿意这么形容的话），是承担不起这种后果的。所以你要么顺应这种变化，认识到世界已经变了，我作为软件工程师的工作将会改变，我的工具也会改变，要么我就全盘接受，想办法对此保持热情，看到所有的新机会，看到用新工作流构建新工厂带来的所有工程挑战；要么我就决定，好吧，我不想这么做。在大多数地方你基本上就卡在那里了，但你实际上是在给人们提供一个决定权：如果你想从那里抽身离开，你现在就可以走，而且彼此之间绝无芥蒂。
<details><summary>Original English</summary>
>> I mean I think you're saying this very nicely and thoughtfully but how I would translate it is you know the world has changed big time and we saw for example with clot code has been such a fast change and the teams who fall asleep at the wheel if you will we you cannot afford it. Uh so you need to either go with this realize that the the world has changed my work as a software engineer will change my tools will change and either I'm on board with this I figure out how to be enthusiastic about this and see all the opportunities all the engineering challenges with building the factories with the new workflows or I decide well I'm not going to do that and most places you're kind of stuck but you're actually giving an option for people to decide if you would like to check out from there you can right now and there's no hard feelings
</details>

>> 我也这样认为。而且我还觉得，你看，归根结底，我也非常在意这一点，对吧？那就是我们给人们造成了巨大的焦虑，巨大的焦虑，让他们觉得无法掌控自己的命运。
<details><summary>Original English</summary>
>> I think so and I also feel Like look I think let's sort of if you come down to it and I care a lot about this right which is we have created enormous anxiety enormous anxiety in people sort of feeling that they don't have control of their own destiny
</details>

>> 因为我们谈论这场 AI 革命的方式就是这样，大家都在说，嘿，也许奇点已经临近了，因此也许我们正在构建的一切会导致只剩下一家公司，或者根本不再有任何工作岗位。这一切往往会让任何哪怕想要求变的人都感到焦虑。
<details><summary>Original English</summary>
>> because the way we have talked about this AI revolution is yeah you know been people say hey this maybe you know the singularity is here and therefore maybe we are building there will be one company or you know there'll be no jobs. All that sort of leads to anyone who even wants to change be sort of anxious.
</details>

>> 是的，压力。
<details><summary>Original English</summary>
>> Yes. Stress.
</details>

>> 所以我总觉得，你看，我们是一家拥有 20 万名员工的公司。我知道我们每个人所从事的工作都会发生很大变化。比如想想看，对吧？微软增长最快的岗位之一就是 FDE。
<details><summary>Original English</summary>
>> And so I kind of feel that this is where look, we're a company of 200,000 people. You know, I know that there's going to be a lot of change in what each of us do. Like think about it, right? One of the fastest growing jobs at Microsoft is FDE.
</details>

>> 在微软也是如此。
<details><summary>Original English</summary>
>> Microsoft as well.
</details>

>> 是的，现在整个行业都是如此。
<details><summary>Original English</summary>
>> Yeah. Across the industry right now.
</details>

>> 整个行业都是这样。因为从某种意义上说，如果你仔细想想，我们有客户代表，这非常重要；
<details><summary>Original English</summary>
>> Across the industry. Because in some sense if you think about it right you have an account rep very important
</details>

>> 紧挨着客户代表的，是我们那些技术支持人员，还有客户……我想我们称之为 CSU，也就是客户成功部门；
<details><summary>Original English</summary>
>> then right next to the account rep is sort of our uh customer uh you know the technical support folks right and the customer um it's I think CSU is what we call a customer success
</details>

>> 然后我们甚至还有技术支持人员，接着还有 FDE 团队；
<details><summary>Original English</summary>
>> uh and then we have even the technical support people and then you have uh the FD team
</details>

>> 前线工程人员（forward deployed engineers）。
<details><summary>Original English</summary>
>> forward the engineers
</details>

>> 所有这些岗位都需要进行彻底的转变，如果你愿意这么说的话，他们都应该去经历任何软件工程师所经历的那种导师指导训练。因为你们都可以——就像我知道甚至在领英（LinkedIn）内部，我认为他们也做出了这种改变，他们把这些人称为“全栈构建者”（full stack builders），他们整合了各种角色。所以伴随所有这些变革，我认为充满着机遇，但你必须走过那段艰难的路程，真正做出结构性调整，让人们进入合适的位置，给他们机会，给他们薪资保障，知道如何根据他们在全新岗位、全新位置上的生产力和卓越表现来进行评估。这是任何成熟在位企业都必须下足的苦功夫。

所以这就是为什么对新事物的赞美固然应该一直存在，对吧，竞争市场就是这样运作的。但你看，我们是一家有 51 年历史的公司，我们要对自己的底色感到从容。我们希望服务好我们的客户，鉴于我们要赋予每个人和每个组织更多力量的使命，我们希望为在这家公司做出卓越工作的员工创造绝佳的经济机遇。
<details><summary>Original English</summary>
>> all of these things require a complete like they all should be going to the same preceptor ship that any software engineer is going if you will right because you can all like I know even LinkedIn I think they made this change inside where they call them full stack builders right which they they combine roles so all that change I think there's opportunity but you have to sort of walk the hard walk of really making the structural changes getting people slaughtered giving them opportunity giving them uh the wage support knowing knowing how to evaluate people with their productivity and their excellence in their new jobs in their new slots. This is the hard work any incumbent you know so that's why you know the celebration of the new which always should be there right that's how competitive marketplaces work uh look you know we are a 51-year-old company we're going to sort of be comfortable in our skin we want to serve our customers well we want to create fantastic economic opportunity for the employees at this company doing great work given our mission to empower people and organizations
</details>

### 应届生招聘与软件工程新工厂

>> 这是事情的另一面，但我只是想明确记录这一点：关于我们谈到的招聘应届毕业生。所以你们仍然在招聘应届生、初级员工吗？你们还在对他们进行投资吗？你是否看到这一点？因为很多其他公司和初创企业的一个担忧就是，他们已经放缓甚至停止了招聘，因为他们认为借助 AI，正如我们之前提到的，能最有效使用它的人是那些拥有专业知识并且能够加以利用的人，因此他们非常犹豫要不要招聘任何职业新人。
<details><summary>Original English</summary>
>> on the other side of this but I I just want to get this on the record so when we talked out hiring new grads. So you you are still hiring new grads, junior people. You're investing in them. You're seeing that because one of the worries in a lot of other companies and startups is and they've slowed down or even stopped hiring because they're thinking well with AI the most the people who can use it the most efficiently as as we previously mentioned the ones who have expertise and they can leverage that and they're very hesitant to hire any new career people.
</details>

>> 这是个很好的切入点。所以，我们在这场变革中努力要做的事情之一——这也正是大家需要稍微从纵向长远角度、而不是仅看一年来仔细观察趋势的地方，因为……
<details><summary>Original English</summary>
>> That's a great point. So, so one of the things that we're trying to do is in this change, this is where I think a little bit of the trends have to be watched carefully over sort of slightly longitudinally versus just you know one year because
</details>

>> 我们正处于巨大的变革过程中，对吧？所以首要任务是确保在内部将所有人重新调整配置到合理的岗位上，对吧？这是第一步。我是说，甚至在同一个团队内部，你也希望先理顺人员配置，对吧？然后在此基础上，再去考虑要补充招聘行业成熟人才还是应届毕业生，对吧？因此我认为目前发生的情况中，有一部分招聘放缓可能是为了先把那些所谓的“软件工程新工厂”建立起来，从而使新投入的要素——不仅是 token，还有人类——能够进驻，然后在这种新配置下为你带来极高的杠杆效应，对吧？

我的意思是，我们得面对现实，什么是 AI 原生公司？他们最初以一个 token 预算和一名员工起步，对吧？随后他们加入进来，那个人把 token 预算用到了极致，然后说我们再招下一个人，接着那个人拿到 token 预算，随后他们的工厂也获得了预算。
<details><summary>Original English</summary>
>> um we're in the process of a lot of change right so first job is to make sure internally all of the folks are getting reorged to places that make sense right step one I mean like even inside of a team right you just want to get the configuration Right? Then it makes sense to oh what is the industry higher or a new college h higher you add to this right and so a little bit of what's happening I think is the slowdown may be a slowdown to get those quote unquote new factories of software engineering built such that new inputs not just tokens humans can come in and then in this new configuration give you high leverage right I mean let's face it when what is an AI native company they start with a token budget and a human, right? Then they add that person maxes their token budget and and then says let's add the next human and then that human gets a token budget and then their factory gets the budget. Yes,
</details>

### 赞助商环节：Linear

>> 是的，这就是建构主义的方式。而且并不是说，好吧，那些公司如果成功了，总有一天也会变大，他们确实会变大，而且有些现在已经变大了；每一家公司都将开始变得像那样，每一个项目团队或产品团队也都会变成那样。因此，这种重新配置、全新探索与构建的过程需要时间，这也是为什么我认为过早去总结太多长期趋势还为时过早。

在回到我们的对话之前，我想先介绍一下本季赞助商 Linear。直到最近，我都以为 Linear 只是一个帮助规划和组织工作的工具，但它的功能远不止于此。许多团队使用 Linear 将改动从最初的构思一直交付到 GitHub 中的代码合并，全程无需离开该工具。我与 Linear 团队的工程师 Dima 坐下来聊了聊，看看 Linear 内部的开发者是如何使用 Linear 来构建整个 Linear 产品的。

这里有一个真实的问题：当你提交包含未发送评论的代码评审时，Linear 会提示你注意这些评论，但它并没有告诉你这些评论具体在哪里。有客户对此提出了意见，Dima 决定修复这个问题。但在修复时，Dima 并没有打开他的集成开发环境（IDE）。相反，他在 Linear 中向智能体描述了这个问题。智能体生成了修复方案，创建了 PR，并附上了 Storybook 截图以便轻松核验。你可以在这张截图中看到链接了草稿评论的修复内容。在 PR 中，你只需从 Linear 中点击一次即可打开预览来进行操作……
<details><summary>Original English</summary>
>> that is the constructionist way and it's not like okay those companies if they succeed they will also be big one day and they will and some already are are and you every company is going to start looking like that and every project team or product team will look like that and so that process of reconfiguring new discovery uh and configuration it'll take time and that's where I think you know trying to draw too many lines as long-term trends I think it's too early. Before we get back to the conversation, I'd like to talk about Linear, our season sponsor. Until recently, I was thinking of Linear as a tool that helps plan and organize the work, but it's much more than that. A lot of teams use Linear to ship changes from idea to merge in GitHub, all without leaving the tool. I sat down with Dimma, an engineer on the linear team, to see how devs inside of Linear use linear to build all of Linear. So, here's a real issue. When you submit a review with unsend comments, Linear warns you about these comments. but it didn't tell you where those comments were. A customer complained and Dimma decided to fix it. But for the fix, Dimma did not open his ID. Instead, he opened up Linear and described the issue to the agent. The agent built a fix, created a PR, and attached storybook screenshots for easy verification. You can see the fix with the draft comments linked on this screenshot. In the PR, you can then open the preview with one click from linear to play
</details>

<!-- chunk 6/9 -->

……随这次变更进行调整，并确认它起作用了。接下来是我最喜欢的部分——引导式审查（guided reviews），目前这项功能还在开发中。引导式审查是一种全新的代码审查体验，能让重点内容一目了然。审查页面的顶部有一份摘要和变更图解，拉取请求（PR）被划分成不同的章节，引导你逐步了解变更内容。这些区块以更容易理解和审查的方式高亮显示关键变更。哦，当 Dimma 完成所有这些后，他直接自行批准代码，代码就合并到了 GitHub。全程无需离开 Linear。如果你只能从这里记住一点，那就是：Linear 不再只是一个规划工单和组织工作的地方。它已经成为所有工作实际发生的地方：创建 issue、启动智能体、查看预览、进行审查，以及合并到生产环境。Linear 是面向团队和 AI 智能体的产品开发系统。我非常喜欢这个演进。Linear 是面向团队和 AI 智能体的产品开发系统，我非常喜欢这个演进。欢迎访问 linear.app/pramatic 查看并获取六个月试用期。
<details><summary>Original English</summary>
around with the change and see that it worked. And here's my favorite part, guided reviews, which is work in progress. Guided reviews is a new code review experience where the important stuff just pops out. The top of the review has a summary and a diagram of the change and the poll request is divided into chapters that walk you through what has changed. These blocks highlight the important changes in a way that's easier to understand and review. Oh, and when Dimma is finished with all of this, he just self-approves the code and it's merged into GitHub. All without leaving linear. If you take away one thing from this, Linear is no longer just a place for planning tickets and organizing the work. It's where all the work happens. Creating the issue, kicking off the agent, checking out the preview, and doing the review and merging to production. Linear is the product development system for teams and AI agents. And I'm loving this evolution. Linear is the product development system for teams and for AI agents, and I'm loving this evolution. Check it out and get a six-month trial at linear.app/pramatic.
</details>

如果你做过 B2B 软件，肯定清楚这是怎么一回事：客户看中了某款产品，接着他们的安全团队就发来一份清单——SSO（单点登录）、SCIM（skin）配置、基于角色的访问控制。这些没有一样是你最初打算构建的，但交易却卡在这里。Work OS 正是涵盖所有这些的基础设施，让你团队里的人不必再去排查客户的 SAML 配置问题。而这个问题的新版本是智能体。一旦智能体在客户系统内部开展操作，企业就想知道它被允许做什么。这就是 WorkOS Airlock 的用武之地。它是基于意图的访问控制。大多数访问控制只询问你是谁；Airlock 还会在智能体尝试执行操作的当下，询问它打算做什么。像“任何智能体都不得删除云资源”这种明确规则会作为纯代码运行；对于更模糊的调用，AI 裁判会在运行时评估策略。你可以用普通英语编写这些策略，Claude 还能从你已有的 Notion 或 Jira（JR）中提取策略并为你导入。你的智能体——无论是 Claude 还是 Devin（Devon）——都通过单一接入点进行连接，而你的 MCP（MTP）服务器则部署在其后。Airlock 是在现有权限之上增加的新层，因此智能体绝不可能获得超过调用者本人权限的访问权限。当出现风险情况时，Airlock 可以将请求上报给人工审批，例如通过 Slack。其核心理念是一次性编写规则，仅在真正需要的调用上耗费人力关注。而且每一次请求和决策都会被记录。访问 workwise.com/airlock 了解更多信息。
<details><summary>Original English</summary>
If you've ever worked on B2B software, you know how this goes. A customer likes a product, then their security team sends a list. SSO, skin provisioning, rolebased access. None of it is what you set out to build, but the deal waits on it. Work OS is the infrastructure that covers all of that. So nobody on your team has to debug a customer's sample setup. The newer version of the problem is agents. Once an agent is acting inside of a customer systems, the enterprise wants to know what it's allowed to do. That's what works airlock is for. It's intentbased access control. Most access control only asks who you are. Airlock also asks what the agent is trying to do at the moment it tries to do it. Clear-cut rules like no agent deletes cloud resources run as plain code. For the fuzzier air calls, an AI judge evaluates a policy at runtime. You write these policies in plain English and Claude can pull the ones you already had out of notion or JR and import them for you. Your agents, whether that's Claude or Devon, connect through a single access point and your MTP servers sit behind it. Airlock is a new layer on top of your existing permissions. So an agent can never get more access than the person who invoked it has. When something risky comes up, airlock can escalate to human for approval, say over Slack. The idea is to write the rules once and spend human attention only on the calls that need it. And every request and decision is logged. Visit workwise.com/airlock to learn more.
</details>

### 开源模型趋势与企业架构自主权

现在我们知道，每个人都在构建自己的软件工厂，或者改变自己的工作方式。现在我们深入探讨一下具体是如何实现的。我在整个行业中看到了一个大趋势，我相信你也看到了：很多科技公司也在转向开放模型。他们当中很多人正在自行搭建推理设施，或者像 Revolut 这样的公司正在购买推理算力——他们购买自己的 B200，并直接在上面运行模型。他们各自都有自己的理由。但从你的角度来看，你看，微软也通过 Foundry 等参与了开放模型托管服务业务。这个趋势有多大？这是否不可避免？我一直在想，开源软件运动与现在的开放模型运动之间是否存在相似之处？
<details><summary>Original English</summary>
Now we know when everyone is building their their software factors or changing how they work. A big trend now that we go down to a little bit of the how this is done. big trend across the industry that I'm seeing and I'm sure you're seeing as well. A lot of tech companies are moving to open models as well. The a lot of them are are spinning up their inference or companies like Revolute are buying their inference. They're buying their B200s and just launching the models on it. They all have their own reasons. But from your vantage point, you know, Microsoft is also in the open model serving business with with Foundry, for example. How big is this trend and is this in inevitable? I'm asking myself are there parallels to the open source movement and now the open model movement?
</details>

>> 是的，我认为肯定存在这种相似之处。你看，必然会存在闭源模型，它们之间会有竞争；而在闭源之外，显然会有一种替代选择，那就是开源/开放模型。开放能给你带来灵活性。事实上，我认为，我思考这个问题的一个切入点是：前沿生态系统究竟长什么样？如果你不再相信那种所谓的“只会有一个前沿模型囊括全世界的所有知识”，对吧？如果你不认同那种说法，那么你就必须假定，从某种意义上说，世界上应该有多少家企业，就应该有多少个前沿模型，对吧？因为归根结底，如果你回到哈耶克（Hayek）对经济本质的描述，经济的核心就在于知识是分散的。事实上，他关于定价机制的整套论述就是一个非常精妙的解释：价格机制之所以起作用，是因为知识在整个经济中是默会且分散的，每家企业都需要掌控自己的知识。如果真是这样，我甚至会说，每家企业本质上都同时拥有人力资本（human capital）和代币资本（token capital）。因此，如果每家企业都将同时拥有代币资本和人力资本，那么代币资本可以是一个你已融入自身知识的开放权重模型（open-weight model），这是其一；它也可以存在于上下文层；你甚至可以同时使用多个闭源模型，事实上收集你使用这些闭源模型的调用轨迹（traces），然后利用这些轨迹为自己训练一个小模型和一个开放权重模型，并保持组合。当我观察 Copilot 时——事实上无论是 GitHub Copilot 还是 Copilot——它们全都被设计成这种多模型系统。事实上我想说，也许到下次你我交谈时，所有人都会说这甚至无关开放还是闭源，每个人都拥有一套模型系统。事实上，它首先拥有一个决策引擎，用于决定针对什么任务使用什么模型，然后将我的上下文、记忆和行动空间与任何单一模型隔离开来，因为否则你就会被彻底套牢。事实上，我经常在想的一件事就是：天哪，如果你真的把自己的测试编排层（harness）、模型、记忆全都绑在一起，你以后怎么脱身？事实上，你到底在做什么？什么是属于你的，什么又是属于模型的？因为不然的话，模型基本上会把它看到的一切都吞噬融合进去。所以我认为这种动态正在越来越被大家所理解。大多数人又觉得“哦，这只是技术圈内部的竞争”。请记住，智能是没有上限的。每家银行、每家医疗公司、每家保险公司、每一个分析师机构，每个人都需要有一种真正具备架构思维的方法，去弄清他们如何掌控自己的学习过程与知识，并形成企业差异化。在那种背景下，开放权重模型是一种我认为具有长远生命力的策略。

这非常有意思，因为我与很多中型科技公司、初创公司交流过，几乎所有人都在构建你刚才提到的那些东西：他们自己的 harness、自己的上下文层、自己的上下文图谱、自己的推理设施。我最初的想法是，这挺合乎常理的，因为工程师喜欢动手做东西，如果你想获得 AI 工程经验，风险最低的方式就是做内部项目。但我从来没想过这一层：这些工程师到底是不是出于正确的理由——也就是战略层面的理由——在做构建。他们很可能是在为公司立功。而你的意思是，大多数公司可能都应该考虑拥有这套系统，拥有可替换的部件和原语，因为——
<details><summary>Original English</summary>
>> Yeah, I think that there are for sure the parallel which is you know you know there's sort of going to be closed models and there'll be competition amongst them and there will be sort of an alternative to obviously closed would be open. uh open gives you flexibility. In fact, I think you know, one of the ways I come at it is with just this what is a frontier ecosystem look like, right? It's can't be if you just get past this thing called uh there's going to be one frontier uh model to sort of have all of the world's knowledge, right? If you don't buy that, right, uh then you have to assume that there should be in some sense as many frontier models as firms in the world, right? Because after all if you go back to actually Hayek uh the his description of what an economy is it's all about knowledge being distributed right in fact his you know his entire thing about pricing uh is a beautiful sort of explanation of hey it happens because of knowledge being tacit and distributed throughout the economy and every firm needs to be in control of it and if so then I would even say every firm is essentially got both human capital and token capital. So if every firm is going to have both token capital and human capital, the token capital can be an openw weight model into which you know you've embedded your knowledge. That's one. It could also be in the context layer. You could even be using multiple closed models. in fact collecting even the traces uh of your usage of those closed models and then using those traces to maybe train an a small model and an open weight model for yourself and keeping you know combination when I look at even copilot in fact whether it's github copilot or co-pilot they're all designed as these multimodel system right in fact I would say maybe even by the next time you and I talk everybody would say it's not about even open or closed everyone has a model system in Fact, it starts with even a decision engine which says which model to use for what task and then I have my context and memory and my action space separate from any one model because otherwise you have a complete lock in. In fact, one of the things I I I think about it's like, wow, if you really got your harness, your model, your memory and all coupled, how would you ever get out, right? In fact, what are you doing and what what do you own versus what is owned by the model? Uh because no, the model will basically collapse into it everything it sees. Um and so I think that this dynamic is getting well better understood. It's you know most people again think oh this is just some competition amongst tech people. Remember there's no limit to intelligence. Every bank, every healthcare company, every insurance company, every analyst out, everybody needs to sort of have a real thing architectural approach to figuring out how do they manage to control their own learning and knowledge and have firm differentiation. And in that context, open rate models is one strategy that I think has legs. You know, this is very interesting because I I talk with a lot of midsize tech companies, startups, and almost all of them are building the things that you just dropped, their own harness, their own context layer, their own own context graph, their own inference. And I thought initially I'm like, well, this kind of makes sense because engineers love to build and if you want to get AI engineering experience, the the least risky thing is to build something internal. However, I never thought of of this part where it's actually these engineers building for the right reasons, which is the strategic reason or not. They're probably doing their company a service. And you're saying that most companies should probably consider owning this system, having replaceable parts, primitives because
</details>

>> 没错。所以事实上你观察到的是对的，这很令人着迷，对吧？事实上我想说，如果你是一家银行，你应该看看那些试图在这个生态系统中立足并成为前沿的软件公司是怎么做的——他们没有拱手让出控制权。所以在某种意义上，银行也应该这样做。那么银行在那里该怎么做呢？他们将拥有杠杆。比如我们所做的——也就是我们称之为“IQ 层”的东西——就是把我们在 Copilot 和 GitHub Copilot 底层所用的 harness 提取出来，做成了一等公民级别的产品，现在你可以通过 Foundry 作为托管服务来使用这个 harness。在那里，假设你正在构建一个供应链系统，你可以直接以我们的 harness 开局，或者你也可以将 Phi（PI）或任何其他开源 harness 引入其中。
<details><summary>Original English</summary>
>> that's correct. So, in fact, what you're observing is correct, which is it's fascinating, right? In fact, I would say if you're a bank, you should check how software companies that are trying to manage in this ecosystem to become frontier uh are doing it. they're not seeding control. So in some sense that's what the bank should be doing. So what does the bank in there they will have leverage. So for example what we have done you know what we describe as this IQ layer is we have taken for example the harness that we have underneath copilot and github c-ilot made it a firstass thing that you can now go to foundry as a managed service and you have the harness. So in there, let's say you're building a supply chain system, you can start with our harness just as essentially an open or you can bring PI or any other open- source harness as well in there.
</details>

>> 哦，我们很喜欢 Phi（PI）。
<details><summary>Original English</summary>
>> Oh, we love PI.
</details>

>> 但你可以直接以托管服务的形式使用它，对吧？微软久经实战检验、连我们自己都在使用的 harness 就直接摆在那里，然后你可以调用所有 Foundry 模型，对吧？这样你就拥有了一个……
<details><summary>Original English</summary>
>> Uh but you can just have it like as a managed service, right? So battle tested uh harness from Microsoft which we ourselves are using is just available there and then you can have all the foundry models, right? So you have a
</details>

<!-- chunk 7/9 -->

框架体系，你可以使用多个模型作为端点，你可以拥有完全独立的上下文层，对吧？你的记忆和上下文那时就是属于你自己的，所以我觉得现在我们有了一个模型系统。顺便提一下动作空间，伴随所有的插件、技能和连接器，对吧，全部与任何给定的模型分离开，模型对其只有可见性。因此我认为一种很好的经典中间层平台正在显现，哪怕是对模型优先的开发也是如此，这样你不会直接被绑定。然后你可以评测一切，对吧，你可以说，嘿，我有自己的评测，而我的私有评测将更为关键，对吧？所有这些公开基准测试——顺便说一句，公开基准固然很好——但你需要有自己的私有评测来衡量对你而言重要的结果，然后在你的强化学习环境中查看跨越所有这些模型的真实表现，并进行持续优化。

事实上，当我观察甚至是我们的客户时，他们一开始用前沿模型，然后他们会说，太棒了，我已经拿到了所有这些追踪记录（traces）。现在我要转变为：嘿，这是一个确定性的工作流。我的意思是，并非我不需要下一次重大的模型发布，而是我现在想优化成本。我会放入一个 MAI flash 模型，把它放进去，用那些追踪记录来微调它，这不就成了。所以，这些全都是你可以在 Foundry 中完成的事情。

我认为那种类型的工作将越来越成为常态。我们说的是，你已经看到很多公司在评测之上也建立了自己的强化学习环境，以便他们能够保持掌控，控制定价，而且我想也是为了不把他们的业务数据泄露给某些可能想要拿这些数据来训练模型的 AI 公司。
<details><summary>Original English</summary>
harness, you can use multiple models as endpoints, you can have your context layer that is completely separate, right? your memory and context uh is yours then so I think now we have a model system uh oh by the way the action space so with all the plugins and skills and connectors right all separate from any given model being only having the visibility to it so I think a good sort of classic middle tier platform is emerging even for model first development where you're not just captured and then you can eval everything right you can say hey I have an eval and my private RIV evals will matter more, right? All these public benchmarks, which by the way is great, but you need to have your own private eval for what is the outcome that matters to you and then look at in your RLE the real performance for across all these models and continuously optimize.

In fact, when I look at even, you know, even with our customers, they start with a frontier model, then they say, well, great. I've got all those traces. Now, I'm going to flip to, hey, this is a deterministic workflow. I mean, it's not like I don't need the next big model drop. I want to now cost optimize. I'll drop, you know, an MAI flash model, drop it in there, use the traces to fine-tune it, and there you have it. So therefore, that's all stuff you can do in Foundry.

So that type of work, I think, is what's going to increasingly be true. We're we're saying that's you're you're already seeing that a lot of companies have their reinforcement learning environment as well on top of the evals so that they can they can stay in control control pricing and also I guess not leak their business data to some of the AI companies that might want to train their models on it.
</details>

>> 没错。如果你仔细想想，对吧，在我的脑海中至少有一个简单的类比：过去无论是在保险公司、银行还是医疗保健公司，人们会说，嘿，我要买一个关系型数据库。太好了，我打算部署一个关系型数据库，在其之上我甚至可能购买一些运行在该关系型数据库上的软件，它自带某种业务逻辑，但随后我会用我自己编写的业务逻辑来扩展它，对吧？然后我来控制它，我数据库里的数据绝不会在任何时候跑到别人那里。这可不像当数据库厂商说“嘿，我不再给你提供数据库更新了”的时候——你依然能够迁移出来。
<details><summary>Original English</summary>
>> That's right. So if you think about it right so the way it's a simple analogy I have at least in my head is you know people you know in the past whether you know in an insurance company in a bank in a healthcare company said hey I'm going to get a relational database great I'm going to deploy a relational database on top of it I may even buy some software that runs on that relational database that is sort of comes with its own business logic but then I'm going to extend it with my own business logic that I write right and then I control it and never at any point is my data in the database going to somebody else. It's not like when the database vendor says, "Hey, I'm no longer going to give you a database update." You still can migrate out.
</details>

>> 这就是你必须面对的问题：如果你的记忆存在于某个特定模型的嵌入向量中，当那家模型公司说“你知道吗？算你倒霉，我无法为你做下一次更新了”的时候，你打算如何把你的记忆迁移出来？另外，我想就像我们谈到的，当新的原语出现时，你打算如何整合它们？问得好，因为如果你过于依赖某一个厂商或一系列厂商，你就不得不等待他们或许去实现它。
<details><summary>Original English</summary>
>> That's the question you have to how are you going to migrate your memory out if your memory is in the embeddings of a given model when that model company says, "You know what? Tough luck. I can't do a next update to you." Plus, I guess what we talked about when we have new primitives come, how are you going to integrate them? Great point because because if you're too reliant on on a vendor or a series of vendors, you'll have to wait for them to maybe do it.
</details>

>> 而且我觉得现在构建起来也更容易了，对吧，如果你拥有称职的工程师，我们很擅长做这个。
<details><summary>Original English</summary>
>> And I guess it's also easier to build right now like right if you have competent engineers, we're good at this.
</details>

### 企业级 AI 的两大架构抉择：学习闭环与信任架构

>> 是的。所以我认为有两项企业架构层面的决策，有趣的是，我希望大家能开始讨论，对吧？因为事实上正如你所指出的，你只需要看看当今软件行业中的软件团队，他们都在琢磨这些，以保持自身的独立性。
<details><summary>Original English</summary>
>> Yeah. So, I think that there are two enterprise architectural decisions that I think interestingly enough are I'm hoping that people are going to start talking, right? because and in fact to your point all you have to do is look at a software team today in a software in industry they're all figuring this out to stay independent
</details>

>> 我认为这必须在商业领域成为一种更普遍的现实。这两点分别是：其一，你如何避免这种反向信息悖论，也就是不要泄露你的价值；你作为一家企业，需要负责并掌控自己的学习闭环。架构方法是什么？你如何确保你的上下文与模型相分离，并且你正在使用多个模型？以及你的框架体系与上下文和模型是分离开的，因为我认为这是你能确保自己可以替换任何模型的唯一途径。事实上，我对这一点的试金石就是：你应该能够替换任何模型，并且依然能在你自己的私有评测上实现爬山算法式的持续提升。
<details><summary>Original English</summary>
>> I think this has to become more of the reality in the commercial space uh and there are two are how do you avoid this reverse information paradox which is don't leak your value you as a firm need to be in charge and control of your own learning loop what's the architectural approach how are you making sure your context is separate from the models and you're using multiple models mod uh that's and your harness is separate from the context and the models because that I think is the only way you can assure yourself that you can replace any model. In fact, my asset test for that is you should be able to replace any model and still hill climb on an eval that's your private eval.
</details>

>> 对。
<details><summary>Original English</summary>
>> Yeah.
</details>

>> 如果你做不到这一点，那么你就得问问自己，你算什么主权企业，
<details><summary>Original English</summary>
>> If you can't do that, then you have to ask yourself how are you a sovereign firm,
</details>

>> 对吧？这意味着你无法掌控自己的产出。是的。
<details><summary>Original English</summary>
>> right? Like that means you do not have control of your own output. Yeah.
</details>

>> 额，所以这有点像是……
<details><summary>Original English</summary>
>> Uh so that's kind of the
</details>

>> 就像坐在一颗滴答作响的定时炸弹上。
<details><summary>Original English</summary>
>> just sitting on taking time bomb.
</details>

>> 是的，我的意思是你彻底完了，这就是我的核心观点。接下来的另一件事就是你现在需要一个信任架构，对吧？也就是说在如今的世界里，你知晓缩放定律是有效的，除了一点：缩放带来的是新能力，而不是对齐。事实上，在机械可解释性层面没有任何理解，希望未来某天能有一项科学突破，但眼下模型变得越来越有能力，却越来越不可靠，这恰恰是最危险的境地。这意味着你在架构上必须将权威与智能分离开来。如果你的智能拥有权威，而它本身又不可靠，那么你再次陷入困境，对吧？你将面临巨大的内部人员风险问题。因此你必须把这些智能体当作内部人员风险来对待。这意味着你必须建立一个信任系统。

这其中涉及很多方面，对吧，甚至包括这种思维链（chain of thought），老兄，这种思维链不能以不可解释的新形式出现，它必须采用人类语言，必须是可审计的，必须被记录下来以确保未被篡改。事情发生并不仅仅是在预训练或者强化学习中，在测试时计算（test-time compute）阶段事情也可能发生，因为它们可能会发生奖励黑客行为（reward hack）。因此在运行阶段，如我所描述的，你必须构建相当数量的防范措施，也就是信任架构，以确保你可以将模型和智能体当作内部人员风险来对待、对其进行监控、拥有可观测性等等，并进而确保你掌控着自己的学习闭环。
<details><summary>Original English</summary>
>> Yeah. I mean you're done. I mean like is my my my point. And so the then the next thing is you now need a trust architecture right which is you kind of have to like in a world where you now know scaling laws work except with scaling comes new capability but not alignment. In fact, no mechanistic understanding that hopefully someday there's a science breakthrough, but right now we're getting more and more capable and less and less reliable like which is the most dangerous place to be in. And so that means you have to separate out architecturally authority from intelligence. If your intelligence has authority and it's unreliable, again, you're taken, right? You have a massive insider risk problem. And so you've got to treat these agents as insider risk. That means you got to have a trust system. And there are a lot of things right even this chain of thought man like this the amount of like this chain of thought has to be not in new release it has to be in in in human language it needs to be auditable it needs to be logged such that it's not tampered it's not just in you know pre-training or in uh you know RL that things happen right which is in test time compute things could happen because they could reward hack and so we have some serious amount of safeguards you have to build um at at runtime as I describe it which is the trust architecture that ensures that you can treat models and and agents as inside a risk and monitor them and have observability and what have you and then ensure that you have control over your learning loop
</details>

### 端侧 AI 与边缘计算架构

>> 作为一名工程师，我所听到的和我所看到的全都是：有太多新型的工作需要去完成，有太多新奇的系统需要去构建，而我们对此并没有现成的蓝图。我的意思是，可能最好的做法就是边做边构建，同时也和正在同期构建这些的同行们交流探讨。我相信在不知 5 到 10 年后还是什么时候，我们会有成熟的蓝图和认证，但眼下这就是一项切切实实的工作。
<details><summary>Original English</summary>
>> as as an engineer all all I'm hearing and all I'm seeing is there's so much new type of work that needs to be done so many novel systems need to be built which we don't have a blueprint for I mean and probably the best way to do is well build it also talk with peers who are building it at the same time and I'm sure we'll have blueprints and certifications in I don't know 5 to 10 years or something but right now this is a job
</details>

>> 没错。事实上，我们下周就要举办 Ignite 大会了，我对此感到非常兴奋，因为我想确保我们做好的正是这件事，即向外界传递出这样的信息：嘿，这一切都是可行的，有蓝图可循，各家公司内部正在发生大量的创新。所以我认为我们正在到达这样一个阶段：重点不再仅仅停留在光鲜亮丽的新事物和新鲜感上。我觉得人们必须坐下来认真思考：嘿，我到底该如何在自己的企业内部创造价值？一旦人们坐下来更深入地探讨这个问题，我认为这些成功的模式就会变得清晰得多。
<details><summary>Original English</summary>
>> it's correct and in fact in fact one of the things we have our conference Ignite coming up next week and I'm excited about it because that's kind of what I want to make sure we do a good job is communicating that hey this is all doable like there are blueprints there is a lot of innovation happening in how companies and so I think that we're reaching that stage where it's not just about the shiny object and the novelty effect and I think people have to sit back and say hey how am I creating enterprise value in my firm and once people sit and talk about that in a little more depth then I think these patterns of success become much clearer
</details>

>> 如今作为一名工程师，我深感欠缺的一点是：所有这些 AI 模型都运行在云端别人的服务器上，或者运行在我买不起、公司也不会给我买的极其昂贵的 B200 上。如果你有，我的意思是你很幸运。但如果它能直接在我的笔记本电脑上运行，岂不是很惬意？那真是太……
<details><summary>Original English</summary>
>> now as as an engineer one things that I I feel very lacking is all of these AI models they run in the cloud on someone else's server or a super expensive B200 that I cannot afford or my company will not buy it for me or if if if you are I mean you're lucky but would it not be nice if it just ran on my laptop That's a great
</details>

>> 而且本地 AI 到目前为止一直很困难，非常拼凑（hacky）。其实很有意思的是，微软正是这方面的创新者。有一款新的 Surface Ultra 笔记本电脑，Scott Hanselman 曾给我做过演示，我现在很想亲自上手体验，因为它里面有一颗芯片，上面运行着一个本地代码编写模型。你认为本地模型在整个 AI 闭环中处于什么位置？作为一名开发者，我觉得本地模型极其缺失，但我是一个人这么觉得吗？你平时接触交流的人要多得多。
<details><summary>Original English</summary>
>> and local AI until now it's been difficult very hacky actually funny Microsoft is is the one that's innovating there's a new Surface Ultra laptop that Scott Hanselman gave me a demo I now want to get my hands on because it it has a chip it has a local coding model running on it where do you think local models fit into the the AI loop and as a developer I feel is desperately missing but am I kind of alone you talk with way more people
</details>

>> 这是一个很好的观点，对吧。所以其中一点在于，我们对确保 PC 作为一种设备形态感到非常兴奋，额，你知道，我们在 AI 时代于这方面进行创新。对我而言，我一直在思考的方式以及我们一直在落实执行的方式就是：我一直觉得分布式计算将永远保持分布式的形态，既然如此，为什么不充分利用外界存在的所有算力和所有的 token，而不仅仅局限于云端的那点东西呢？所以那算是一种……
<details><summary>Original English</summary>
>> it's it's a great point right so one of the things is we're very excited about making sure that the the PC as the form factor um you know we innovate in uh in the age of AI and so to me the way I've been thinking about it and how we've been executing on it is I've always felt like distributed computing will always remain distributed so why not use all the power and all the tokens that are out there versus just the stuff in the cloud so that's sort of the
</details>

<!-- chunk 8/9 -->

### 混合智能与端侧推理

……灵感，甚至对 Ultra 也是如此，但确实有很多创新，事实上无论来自英伟达、AMD 还是高通，Intel 也很棒，都有出色的芯片研发和系统工程在推进。事实上现在已经实现了这一点——去年的前沿模型可以在你的笔记本电脑上运行，上个季度的前沿模型可以在你的台式机上运行，我是说，现在的能力大概就是这样，所以……
<details><summary>Original English</summary>
inspiration even for ultra but but there is lots of innovation in fact from you know whether it's Nvidia or AMD or Qualcomm so it's fantastic Intel there's good silicon work happening and systems work and this is in fact it's already true what is it like last year's frontier can run on your laptop and last quarters uh Frontier can run on your desktop I mean like that's kind of like the capability so
</details>

>> 就像当年个人电脑（PC）的演进方式一样，对吧？
<details><summary>Original English</summary>
>> it's like how pieces used to evolve right
</details>

>> 没错，这太棒了。既然具备了这种能力，我思考的另一件事就又回到了我的决策引擎和路由器上。对吧，所以当我想到 Hydra Fusion 时——我想我们用的是这个词，我现在有点忘了，在 GitHub 中我们有一种路由方式，对吧。我很喜欢 GitHub，因为现在实际上在 Copilot 中，上次我选择模型……
<details><summary>Original English</summary>
>> exactly so it's great so now that you have that then one of the things that I think about again goes back to my decision engine and routers right so when I think about hydra fusion um I think that's the term we use I forget now which in github we have a you know a way to route right I love the github uh because all nowadays in fact in copilot the last time I chose a model
</details>

>> Copilot Fusion。
<details><summary>Original English</summary>
>> copilot fusion
</details>

>> 对，Copilot Fusion。所以基本上我们希望这个路由器能为当前任务挑选最合适的模型。这意味着，事实上我有时在 Ultra 上能看到，突然风扇就开始转了，对吧，因为正在调用我的本地模型。尤其是在智能体群（agent swarm）中，当你拥有多个子智能体时，你可以在同时调用云端模型的情况下，为某些子智能体调用一批本地模型。这在架构上讲得通，在经济上也讲得通。所以我们正处于我称之为“混合智能时代”的开端。云端将继续增长，对这些 Token 将会有近乎无限的需求；但这也意味着你可以开始把边缘端的各种硬件形态同样视为 Token 工厂。事实上，我有点把它看作是“不限流量的智能”（unmetered intelligence）。
<details><summary>Original English</summary>
>> yeah copilot fusion so basically we want to be able to have this router pick the models right for the task and so that means in fact I see it in ultra sometime I mean it you know my suddenly I see the fan go right because my local model is being used because especially in an agent swarm uh where you have multiple sub aents then you can invoke for some sub aents a bunch of local models while you're using even the cloud models together u and so yeah this makes sense architecturally it makes sense economically it makes sense and so we're in the beginning of what I'll call this hybrid intelligence era cloud will continue to grow there's going to be infinite amount of sort of demand for these tokens but that means you can also start thinking about the, you know, the form factors at the edge as also token factories. In fact, I kind of think of it as the unmetered intelligence.
</details>

>> 是的。因为你完全不需要担心自己用了多少。
<details><summary>Original English</summary>
>> Yeah. Because you you don't need to worry about how much you're using it.
</details>

>> 没错。
<details><summary>Original English</summary>
>> That's right.
</details>

### 模型选择与 MAI 模型

>> 我想我现在开始把这些都串联起来了。因为老实说，对于 MAI Code，就是那个 Flash 1.1 模型，我并没有太惊艳。我觉得大家都没觉得有多惊艳。但有一点让我印象深刻：谈到在任何笔记本电脑上运行的本地模型时，我总以为它必须是开源模型。然而，MAI Code 尽管是一个闭源模型，却可以下载到 Windows 机器上并且可以在上面运行。相关的底层基础设施已经在那里了。我就在想，会不会以后其他闭源模型也能这样？这样我在笔记本电脑上就可以自由挑选，要么下载下来可能免费使用，要么只付很少的费用。
<details><summary>Original English</summary>
>> I guess this is where it's now starting to come together for me because the uh MAI code uh what the the Flash 1.1 model, I'll be honest, I wasn't too impressed. I don't think anyone was too impressed. But the one detail I was impressed with when it comes to local models running on any laptop, I always assumed it must be open models. However, the MAI code can be downloaded on a Windows machine even though it's a closed model and it can be run there. There's the infrastructure there. And I'm like, huh, could there be a future where like other closed models? So I I could choose on my laptop like pick and choose like either I download them and maybe it's free or I pay very little.
</details>

关于你提到的 Code Flash 模型，把它们一路推进并部署到笔记本电脑上，对我们来说是核心优先级，我们对此感到非常兴奋。当我看到 Copilot 内部的 Code 标签页时，它甚至独立于 GitHub Copilot，如今无论是写代码、写文档还是编写应用程序，你都可以轻松在自己的 PC 上使用这些模型，这令人兴奋。但退一步来说，我们在 MAI 模型上究竟在做什么呢？首先，通过与 OpenAI 的合作，我们拥有 OpenAI 的模型，并且我们将继续使用这些 OpenAI 模型，对吧？在此之上，我们的想法是：好，让我们从零开始创新研发一个新的模型家族……
<details><summary>Original English</summary>
you know to your point about the the code flash models getting them even all the way uh to a laptop is core priority for us and we are excited and that's kind when I look at the code tab inside of copilot right which is uh even you know independent of github copilot now code writing a document or writing an application you can easily use these models on your PC and that's exciting but just to kind of step back and say what are we doing with even MAI models right first of all through the partnership with open AI we have the Open AAAI models and and we're going to continue to use those OpenAI models, right? Uh on on top of that, what we are saying is okay, let's sort of innovate in a new model family ground up that
</details>

>> “从零开始”意味着由你们自己构建。
<details><summary>Original English</summary>
>> ground up meaning you build.
</details>

>> 是的。首先，我们甚至披露了新的 MAI-2 Base 预训练模型，事实上，这是对预训练配方和训练机制最详尽的公开披露之一。所以，你的听众们应该去看看，对吧？它可能是——外界的人也这么对我说——目前对预训练最详细的描述，对吧？因为极少有地方能让你看到并获取这些内容，而且这完全是一个所谓“净室”（clean room）式的预训练运行实现。因此，我们会继续推进这项工作。但接下来我们能进行创新的地方，在于将其置于我称之为前沿曲线上的新节点：如何结合我们的产品——无论是网络安全、知识工作还是编程——在前沿曲线上建立新的平衡点，使你在训练时具备 FLOPS 效率，在部署时具备 Token 效率。一旦你进入到一个由你将高层意图分发给众多子智能体的世界，这些子智能体就可以使用多个模型家族，对吧？我认为这就是未来的方向。那种“我必须死守某一个模型家族”的想法未必成立，只要有选择，智能体就会聪明地挑选所有能够以最高效方式完成任务的模型。我认为这就是我们的目标：提供更多选择，而不是仅仅局限于单一的模型家族。
<details><summary>Original English</summary>
>> Yeah, first of all, we have a you know, I think we disclosed even the new MI2 base which is the pre-training and in fact it's one of the best disclosures of a pre-training recipe and regime. Uh so for those who are uh you know your listeners should go look at it, right? It's probably and people tell me from the outside that it's the most detailed descriptions of pre-training, right? Because there are very few places where you can go to and get it and it's completely, you know, clean room so to speak, uh, implementation of a a pre-training run. So therefore, we're continuing to do that. But then the place where we are able to sort of innovate is put I'll call it new points on the frontier curve where using our products, right? Whether it's cyber, whether it is knowledge work, whether it's coding, how do you put new points on the frontier where you're both flops efficient on training and you are efficient on tokens in deployment and once you are in a world where you're handing high level intents to many sub agents, the sub aents can be using multiple model families, right? That's I think the way like this idea that oh I'm like wedded to one model family may not be true if there are choices agents will be smart in picking all of the models that allow them to get the task done in the most efficient way and that I think is our goal. Our goal is to give more choice as opposed to just one model family.
</details>

### 给 AI 时代软件工程师的建议

>> 我非常赞同你提出提供更多选择的做法，因为作为开发者，我喜欢有选择。这也有助于促进竞争、带来更好的价格等等。在结束之前，我想问：现在的技术变化非常快，我和业内人士交流，他们都说虽然见过类似的变化，规模也许没这么大，但绝没有像现在变化得这么快。你经历过多次变革周期，在你刚入行时，时代完全不同。作为一名软件专业人士，如果目标是在这一两年内在这个新的 AI 时代成为一名出色的软件工程师，你会如何应对这种变化？
<details><summary>Original English</summary>
>> I I really like how like you're you're setting out choice because as a developer I love choice. It also helps least to competition, better prices and so on. And as closing, this changes very fast. Everyone I talked to who've been in the industry, they said they've seen, you know, like change maybe similar to this, maybe not as big, but not not as quickly. You've been through multiple change cycles. When you started, it was a very different time. How would you approach this change as a software professional when your goal is I would like to be a amazing software engineer in this new age of AI in a year or two?
</details>

其实就是我们刚才聊到的那些。坦白讲，即使对我自己而言，我认为最核心的就是确保自己脚踏实地弄清楚这场变革的本质究竟是什么，对吧？这不仅仅关乎新闻头条，也不仅仅关乎那些标语——我也喜欢刷 X，那很棒，但这绝不仅仅关乎炒作周期。是的。
<details><summary>Original English</summary>
you know, it's sort of the stuff we talked about. Quite frankly, even for me, I think just making sure that one gets grounded in what is this change about, right? Uh it's not just about the headlines and it's not just about the headlines, you know, I love X and you know, it's great, but it's just not about uh the hype cycle. Yeah.
</details>

>> 还有那种不断需要去讨论的冲动。不过在播客里说这个有点讽刺。但核心就是去多做、多学，亲手去实践……
<details><summary>Original English</summary>
>> And that constant need um uh to talk. But it's ironic in a podcast to say that. But it's do do more uh learn more and and hands-on experience
</details>

>> 第一手去体验。坦白讲，对我自己来说，如果能改变我“说”与“做”的比例，我也会这么做。现在正是时候。如果说有一条建议，无论你处于职业中期，还是像我一样是 CEO，亦或是刚毕业的大学生：你越能花时间去学习实践，越能加入那些正在动手实践的团队，效果就会越好，我认为这胜过其他任何事情。因为有时候在某种层面上我也会想，我什么时候状态最好？那就是当我处于求学状态的时候。所以，让我们重新回到学习状态吧。
<details><summary>Original English</summary>
>> experience it firsthand. That's you know quite frankly that's kind of what I would even say for me if I could change the ratio of my you know talk to do I would do it. This is the time. If one piece of advice, whether you're mid-career or even a CEO like me or or a fresh uh college grad, the more you can take the time to sort of learn to do be in teams that are doing uh the better it is versus um I think anything else because at times like sometime at some level I sometimes think about it and when am I at my best? It's when I'm in the school mode. Uh so let's get back to school.
</details>

>> Satya，非常感谢你。
<details><summary>Original English</summary>
>> Satia, thank you so much.
</details>

>> 非常感谢，非常荣幸。
<details><summary>Original English</summary>
>> Thank you so much. It's such a pleasure.
</details>

### 节目总结与核心观点

这真是一次棒极了的体验，我们和 Satya 探讨了大量的内容。一个反复出现的主题是：当 AI 让编写代码变得廉价时，什么样的软件工程工作会变得更加重要？我们讨论了在写代码之前和之后的事情——也就是规划和验证——如何变得更加重要，而这些正是我们工程师将投入更多时间的活动。我也观察到许多科技公司正在构建自己的代码测试框架（coding harness）、上下文层和 AI 基础设施。我原以为这是因为工程师就是喜欢用新颖的技术来搭建东西。但 Satya 指出，对一家公司而言，不拥有自己的 AI 基础设施和 AI 知识产权实际上是一种自杀式的策略。事实上，他认为每一家成功的公司都会打造出自己的 AI 基础设施。而那些依赖单一供应商或 AI 实验室的公司正在犯下巨大的战略错误。说到我们开发者乐于构建新事物，这正在带来回报。我能预见到我们将有很多机会去构建这种新型的 AI 基础设施以及这些内部软件工厂。最后，软件工程的角色和期望也正在发生变化。Satya 分享道，微软内部增长最快的职位之一是前线部署工程师（forward deployed engineer）。这是一个几年前还不存在的职位。Satya 预计在微软内部会看到大量的重组，团队会变小，角色会改变；而自愿离职计划对那些不想经历接下来可能比以往任何时候都更加剧烈的变革期的人来说是一个选择。我想，这种伴随着重组和角色转变的变革，其剧烈程度都会超过以往……
<details><summary>Original English</summary>
Well, this was an awesome experience and we really [music] covered a ton of ground with Satia. A recurring theme that kept coming back. What kind of software engineering work becomes more important when coding becomes cheap with AI? We talked about how the things both before and after coding that is planning and validation both become more important and this will be activities as us engineers will spend more time on. I also observed a lot of tech companies building their own coding harness, context layer, and AI infra. [music] And I assume that it's because engineers just like to build with novel technology. But Sachio pointed out that it's actually suicidal strategy for a company to not own their AI infra and their [music] AI intellectual property. In fact, he thinks that every successful company will build out this own [music] AI infrastructure. And those relying on a single vendor or AI lab are making a massive strategic mistake. Talk about us devs enjoying building new stuff and it's paying off. I can see us having a lot of opportunities to build this new type of AI infra and these internal software factories. [music] Finally, software engineering roles and expectations are also changing. Sasha has shared that the one of the fastest growing jobs inside of Microsoft is forward deployed engineer. This is a position that has not existed a few years ago. Sachi expects to see a lot of reorg inside of Microsoft where [music] teams become smaller and roles change and the voluntary exit program is an opportunity for people who leave who don't want to go through what will probably be a really intensive period of change much more than before. I would assume that this kind of change with reorgs and role changes all of these being more intense than before [music]
</details>

<!-- chunk 9/9 -->

……可能不仅对微软如此，对许多其他科技公司也同样如此。最终，[音乐] 这次对话让我感到更加充满干劲。是的，行业正在发生变化。但我所理解的是，Satia 如何看待有大量软件工程工作正等待着借助这些新的 AI 相关原语来开展——比如决策模型以及一些尚未被发明出来的原语；用户将需要用这些新原语来构建这些新系统，决定什么放在哪里、如何进行修改、什么才是合理的、如何去部署它，并不断从中学习。
<details><summary>Original English</summary>
is probably not just true for Microsoft but it will be true for a lot of other tech companies. In the end [music] I walked away being more energized from this conversation. Yes, the industry is changing. But what I understood is how Satia sees that a lot of software engineer work is waiting to happen with these new AI related primitives like decision models and some of the primitives that have been not been invented and users will need to build these new systems with these new primitives deciding what goes where, how to change it, what makes sense, how to deploy it and just keep learning from it.
</details>

请务必查看下方的节目附注，了解关于评测（evals）、推理工程、循环工程等 AI 工程概念的相关深度探讨。如果您喜欢这档播客，请务必在我们喜爱的播客平台上以及 [音乐] YouTube 上订阅。如果您还能在节目上留下评分，或者分享给同事或朋友，将是对我们特别的感谢。谢谢大家，我们下期……
<details><summary>Original English</summary>
Do check out the show notes below for related deep dives on AI engineering concept like evals, inference engineering, loop engineering and more. If you've enjoyed this podcast, please do subscribe on our favorite podcast platform and [music] on YouTube. A special thank you if you also leave a rating on the show or share with colleagues or friends. Thanks and see you in the next
</details>