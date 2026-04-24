---
author: The Pragmatic Engineer
date: '2026-04-22'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=SVOrURyOu_U
speaker: The Pragmatic Engineer
tags: []
title: Untitled
summary: ''
insight: ''
draft: true
series: ''
category: ''
area: ''
project: []
people: []
companies_orgs: []
products_models: []
media_books: []
status: evergreen
---
<article>
### 节目介绍与嘉宾

**主持人**: 我们应该考虑多区域、多副本甚至多云的设置吗？你愿意承担多少可用性风险，以及计算开销和实际设计、操作系统的人力开销呢？**MapReduce** 已死，现在没人用了。但我们增加覆盖的其他领域是支持 **AI** 的系统，比如向量索引。作为一名软件工程师，是否会存在不再有动力去理解底层架构的风险？如果你依赖于更高层次的抽象，你就不再考虑底层细节。如果你正在构建更高层次的业务逻辑，实际上，我认为这完全没问题。大型语言模型（**LLM**）增加了对这些形式化证明的需求，因为我们正在大量编写代码。我认为形式化验证未来会变得更重要，原因之一是：

**Designing Data-intensive Applications** 一直是所有构建大型后端系统的人的首选书籍。这本书出版九年后，第二版问世了。**Martin Kleppmann** 是这本划时代著作的作者。我与他坐下来，今天我们将探讨在 **LinkedIn** 参与 **Kafka** 的工作如何直接塑造了这本书第一版的思想，第二版有哪些新内容，以及为什么像 **MapReduce** 这样的技术从更新版本中被移除。形式化方法、本地优先软件、去中心化访问等等。如果你关心大型系统如何运作、它们的发展方向以及哪些基本原理不会改变，那么本期节目就是为你准备的。

<details>
<summary>Original English</summary>
**主持人**: Should I consider multi-zone, multi-region, or even a multi-cloud setup? How much availability risk are you willing to take on versus the computational overheads, but also the human overheads actually designing and operating the system? **MapReduce** is dead. Nobody uses it anymore. But other areas where we've increased the coverage are systems in support of **AI** like vector indexes. Is there any risk as a software engineer that you're no longer incentivized to understand the underlying layer? If you rely on a higher level abstraction, you're no longer thinking about the lower level details. If you're building higher level business logic, actually, I think it's just fine. **LLM**s increase the need for these formal proofs because we're vip coding a bunch of stuff. The reason I think that formal verification could become more important in the future. One is that **Designing Data-intensive Applications** has been the go-to book for anyone building large backend systems. 9 years after publishing this book, the second edition is here. **Martin Kleppmann** is the author of this generational book. I sat down with him and today we cover how working on **Kafka** at **LinkedIn** directly shaped ideas that became the first edition of the book, what's new in the second edition, and why things like **MapReduce** got removed from this updated version. Formal methods, local first software, decentralized access, and many more. If you care about how large systems work, where they're heading, and what the fundamentals are that don't change, this episode is for you.
</details>

### 赞助商介绍

**主持人**: 本期节目由 **Statsig** 赞助，**Statsig** 是一个统一平台，支持实验和持续发布。内置实验意味着每一次发布都会自动成为一个学习机会，通过适当的统计分析，精确展示功能如何影响你的指标。特性标志（Feature flags）让你能够自信地持续发布。由于所有功能都在一个平台上，拥有相同的产品数据，你的组织内各团队可以协作并做出数据驱动的决策。要了解更多信息，请访问 **statsig.com/pragmatic**。

<details>
<summary>Original English</summary>
**主持人**: This episode is presented by **Statsig**, the unified platform for flags, analytics, experiments, and more. Built-in experimentation means that every roll out automatically becomes a learning opportunity with proper statistical analysis showing you exactly how features impact your metrics. Feature flags let you ship continuously with confidence. And because it's all in one platform with the same product data, teams across your organization can collaborate and make data-driven decisions. To learn more, head to **statsig.com/pragmatic**.
</details>

### Sonar赞助

**主持人**: 本期节目由 **Sonar** 赞助。**Sonar**，**SonarQube** 的开发者，深知代码质量不仅仅是避免语法错误。它关乎通过保护系统的结构完整性来实现长期可维护性。当代理大规模生成代码时，它们常常忽视系统的结构完整性。这会造成代码缠结、重复代码和其他可维护性问题。这些问题会将模块设计变成一团糟，使其扩展变得越来越困难。但这里有一个非常有用的工具：**SonarQube** 的架构管理。它将架构治理从静态 Wiki 转移到你的自动化工作流程中。它允许你可视化当前架构，定义架构边界，并实时管理架构问题。无论是人类还是 **AI** 代理在键盘前，**Sonar** 都能充当结构衰退的断路器。它确保每一次提交都尊重系统蓝图，保护你最复杂应用程序的长期健康。访问 **sonarsource.com/pragmatic** 了解更多信息。那么，**Martin**，欢迎来到播客。

<details>
<summary>Original English</summary>
**主持人**: This episode is brought to you by **Sonar**. **Sonar**, the makers of **SonarQube**, understands that code quality is about more than just avoiding syntax errors. It's about long-term maintainability by protecting the structural integrity of the system. As agents generate code at massive scale, they often ignore your system structural integrity. This creates tangles, duplicated code, and other maintainability issues. These issues turn a module design into a big ball of mud, making it increasingly difficult to extend. But here's something that's really helpful. **SonarQube**'s architecture management. It moves architectural governance out of static wikis and into your automated workflow. It allows you to visualize your current architecture, define architectural boundaries, and manage architectural issues in real time. Whether it's a human or an **AI** agent at the keyboard, **Sonar** acts as a circuit breaker for structural decay. It ensures every commit respects the systems blueprint protecting the long-term health of your most complex applications. Head to **sonarsource.com/pragmatic** to find out more. So **Martin**, welcome to the podcast.
</details>

### 嘉宾背景与技术之路

**Martin Kleppmann**: 嗨，**Ger**，很高兴来到这里。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Hi **Ger**, it's great to be here.
</details>

**主持人**: 很高兴能邀请到你。我想你对许多软件工程师来说，包括我自己，都不需要介绍了。你是这本标志性书籍的作者，这本书在我书架上放了大概十年了，它刚出版不久我就有了。在我们深入讨论这本书之前，我想问一下，你是如何进入技术领域的？

<details>
<summary>Original English</summary>
**主持人**: It's amazing to have you here. I don't think you need introduction to many software engineers, including myself. You're the author of this iconic book that I've had on my bookshelf for probably about 10 years, not much longer after it came out. Before we get into this book, which we're going to talk about, how did you get into the technology field?
</details>

**Martin Kleppmann**: 是的。嗯，我像许多人一样，读了计算机科学本科。然后，在那之后，我不太确定自己的人生该做什么，但我当时觉得，创办一家初创公司似乎是一件有趣的事情。所以，我就创办了一家初创公司，当时完全不知道自己具体要做什么，然后最初一段时间都在四处寻找可能有趣的事情。第一家初创公司经营得不太顺利，但通过那次经历，我遇到了一些人，他们后来成为了我第二家初创公司的联合创始人，那家公司做得更好，我们把它卖给了 **LinkedIn**。在那之后，我开始对教授这些分布式系统概念感兴趣，所以那时我开始写这本书。在写书的过程中，我也从工业界回到了学术界。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes. Well, I did an undergraduate computer science like many others. And then after that, I wasn't quite sure what to do with my life, but I thought, well, starting a startup seems like an interesting thing to try. So, I started a startup having no clue what I was going to actually do and then spent the first while searching around for things that might be interesting. The first startup didn't work out that well, but through that I met some others who then became my co-founders for the second startup which worked better and we sold that one to **LinkedIn** and then after that I started being interested in teaching these distributed systems concepts so that's when I got into writing the book and then during the writing of the book I also switched over from industry back to academia.
</details>

**主持人**: 我们能聊聊你的第一家和第二家初创公司吗？

<details>
<summary>Original English</summary>
**主持人**: Can we talk a little bit about your first and second startup?
</details>

**Martin Kleppmann**: 好的，**Go Test It**，大概是 2008 年左右。那是一个人们在让 **JavaScript** 跨浏览器工作时遇到很大困难的时代。当时 **Internet Explorer** 仍然很流行，**Chrome** 才刚刚发布。所有的浏览器都互不兼容，所以 **Go Test It** 是一个用于网站的跨浏览器自动化测试服务。它基于 **Selenium**，一个至今仍在使用的开源项目。其理念是，你可以编写测试脚本，自动化用户点击网站的各种交互，然后检查是否发生了正确的行为。所以，它基于 **Selenium**，但作为一个托管服务提供，这样人们就不必自己运行各种带有不同操作系统的虚拟机。技术上是可行的，但我发现很难获得用户。很多网站开发者理论上说：“哦，这太棒了，我们需要进行跨浏览器测试。”但实际上，让他们将其整合到工作流程中，养成使用习惯，并投入编写测试脚本是非常困难的。所以，那家公司最终没有取得任何进展。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, **Go Test It**. This was like 2008 or something like that. It was the age where people were having really difficulties getting their **JavaScript** working cross browser. **Internet Explorer** was still pretty big at the time. **Chrome** had just come out. All the browsers were incompatible with each other and so **Go Test It** was a cross browser automated testing service for websites. It was based on **Selenium**, an open source project that still exists. And the idea is you would write test scripts that automate a user clicking through the various interactions with a website and then just check that the right behavior happens. And so yeah, it was based on **Selenium** but just as it provided as a hosted service so people wouldn't have to run various VMs with various operating systems themselves. It worked technically but I found it really hard to actually get adoption for it. A lot of people building websites in theory said, "Oh yeah, this is great. We need to test cross browser." And in practice actually it was really difficult to get them to integrate it into their workflow and just get in the habit of using it and investing in writing the test scripts. So, so that ended up not really going anywhere.
</details>

**主持人**: 所以，当时并没有什么可行的业务，或者说没有能够产生有意义收入的途径？

<details>
<summary>Original English</summary>
**主持人**: So, so like there wasn't like a business to be done or or like revenue to be generated in meaningful sense.
</details>

**Martin Kleppmann**: 是的，当时至少还有一两家同期的公司成功建立了业务。**Source Labs** 就是其中一家成功了的。但即使对他们来说，这也是一个发展缓慢的业务。我认为这不是一个容易经营的行业。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. Well, there's at least one other maybe two other companies from that same era that did manage to make a business. **Source Labs** is one that managed to actually succeed. But it even for them it was a pretty slow running business. I think it was not an easy business to be in.
</details>

**主持人**: 那家初创公司是在英国建立的吗？

<details>
<summary>Original English</summary>
**主持人**: And for the startup, were you in in the UK building it?
</details>

**Martin Kleppmann**: 我当时在英国。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: I was in the UK at the time.
</details>

**主持人**: 是自力更生（bootstrapped）的吗？你有没有筹集到一些资金？团队有多大？我们能想象一下当时的情况吗？

<details>
<summary>Original English</summary>
**主持人**: Was it was it bootstrapped? Did you raise some some kind of funding? How big was the team? How can we imagine this?
</details>

**Martin Kleppmann**: 主要是自力更生。我做了很多咨询工作来资助招聘一些人，然后以低廉的价格雇佣了一些朋友来帮助实际构建产品。所以一切都非常节俭。我只有一小笔天使投资，但大部分是自力更生。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: It was mostly bootstrapped. So I did a bunch of consulting in order to fund hiring some people and then hired some like friends on the cheap to help contribute to actually building the product. And so it was done all very cheaply. I had a very small amount of angel money in there but mostly bootstrapped.
</details>

**主持人**: 嗯。那么当你决定不再继续下去的时候，下一家初创公司是如何出现的？是 **Reportive**，对吗？

<details>
<summary>Original English</summary>
**主持人**: Mhm. And then when you decided to to not go forward with this, how did the next startup come? Reportive, right?
</details>

**Martin Kleppmann**: 是的，第二家是 **Reportive**。那家公司发展得好多了。基本上，它把社交媒体整合到了 **Gmail** 里面。所以，想法是，如果你收到一封来自陌生人的邮件，我们有一个小型的浏览器扩展程序，它会操作 **Gmail** 的网页界面，这样在邮件旁边，我们会显示一个社交资料摘要，包括个人头像、从 **LinkedIn** 获取的职位头衔、从 **Twitter** 获取的最新推文，以及可能来自 **Facebook** 的最新帖子等等。总之，就是我们能找到的关于那个人的任何信息，并将其作为社交摘要放在邮件旁边。我们大概在 2010 年左右开始，然后很快就变得非常受欢迎。因此，在此基础上，我们得以从 **Y Combinator** 筹集到一些资金，当时 **Y Combinator** 还相当年轻。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, the second one was **Reportive**. That went a lot better. So, that was putting social media inside **Gmail** basically. So, the idea was that if you get an email from someone you don't know, we had a little browser extension which manipulated the **Gmail** web interface so that on the side next to the email, we'd show you a summary social profile with like a profile picture and like a job title pulled from **LinkedIn** and recent tweets pulled from **Twitter** and maybe recent **Facebook** post or things like that. Just whatever we could find about that person and put that as a social summary next to the email. We started in 2010 or something like that. It was then pretty quickly became quite popular. And so on the back of that we were then able to raise some money from **Y Combinator** which was still fairly young at the time.
</details>

**主持人**: 那时候它还很年轻。你肯定是最早几批之一。

<details>
<summary>Original English</summary>
**主持人**: That was very young. That you must have been one of the very early batches.
</details>

**Martin Kleppmann**: 是的，我不记得他们具体什么时候开始的，但那肯定是在早期。我认为当时 **Y Combinator** 已经建立了相当好的声誉，但规模仍然很小。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, I can't remember exactly when they started but it was certainly in the early years. I think **Y Combinator** had already built up a quite a good reputation at the time, but it was still fairly small.
</details>

**主持人**: 那么作为 **Y Combinator** 的一部分，你是否必须从英国飞到旧金山参加那个为期十周的项目？如果我没记错的话。

<details>
<summary>Original English</summary>
**主持人**: And then as part of **Y Combinator**, did you have to fly you from from the UK to San Francisco to attend that 10-week program if I remember?
</details>

**Martin Kleppmann**: 没错，是的。所以我们最初是来参加 **Y Combinator** 的三个月（或更长时间）项目，但后来我们成功获得了美国工作签证，并在旧金山永久定居。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Exactly. Yes. So we initially came for for the 3 months or whatever it was of the **Y Combinator** but then we were able to get US work visas for ourselves and set up permanently in San Francisco.
</details>

### 迁居旧金山与公司发展

**主持人**: 从你在英国上大学、创办第一家初创公司、以及这段经历的初期，到来到旧金山，这种转变是怎样的？

<details>
<summary>Original English</summary>
**主持人**: How was that shift from from the UK where you spent going to university your first startup the first part of this to coming to San Francisco?
</details>

**Martin Kleppmann**: 感觉非常激动人心，因为你知道，那就像是去了所有事情发生的核心地带。我们刚开始时完全不认识任何人。在整个湾区，我们只认识一两个人，但我们联系了他们，他们又把我们介绍给更多的人，然后那些人又把我们介绍给更多的人。所以我们很快就建立起了一个网络，我非常感激这一点，因为它对我们这些外来者非常开放，我们基本上带着一个想法和一家早期初创公司就能来到这里，我们成功筹集到了一些资金，并在湾区站稳了脚跟。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: It was very exciting because you know it felt like going to the center of where it was all happening really and we at the started out not knowing anybody at all. We knew like one or two people in the entire Bay Area, but we like contacted them and they introduced us to more people and they introduced us to more people. And so we were able to pretty quickly actually build up a network and that that's something that I really appreciated that it was actually so open to outsiders like us who could just basically turn up with an idea and an early stage startup and we managed to raise some money and managed to like actually become somewhat established in the in the Bay Area.
</details>

**主持人**: 你能告诉我公司是如何成长的，以及 **LinkedIn** 的收购要约是在什么时候提出的？我们如何想象你作为这家公司的创始人当时的处境？

<details>
<summary>Original English</summary>
**主持人**: And can you tell me how the how the company grew and and at what point did the **LinkedIn** acquisition offer come and and how can we imagine even you were a founder of this company.
</details>

**Martin Kleppmann**: 大约在 2012 年，我们卖掉了公司。当时我们有五个人。所以规模仍然很小。虽然没有涉及巨额资金，但我会说这对所有参与者来说都是一次成功。收购过程本身很顺利。就像这类交易常有的那样，过程中充满了曲折，有些时候我们觉得一切都会泡汤，然后我们几乎要耗尽资金，而且也没有成功筹集到新一轮融资。所以我们有点被迫出售或关闭。我们承受了相当大的压力。我们不能削减自己的工资，因为那样会违反我们的签证条件。是的。所以，考虑到我们当时缺乏谈判筹码，我们处于一种稍微有点僵局的境地。但实际上，我对最终的结果非常满意。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: It was about in 2012 that we sold it. And we were five people at the time. So it's all still pretty small. Not vast amounts of money involved but it it was a success I would say for everybody involved. The acquisition process itself was fine. As always with these kinds of transactions, there was like twists and turns and moments where we thought it would all fall apart and then we were almost running out of money and hadn't really succeeded in raising another round. So, we kind of had to sell or shut down. So, we were under quite a bit of pressure. We couldn't reduce our own salaries because to do so would have violated the conditions of our visas. Yes. So, we were in a slightly stuck situation given our lack of leverage in that situation. And actually I'm pretty happy how it all turned out.
</details>

**主持人**: 是的，很高兴我们能坦诚地谈论这件事，因为很多时候，当你看到 **LinkedIn** 的收购时，你可能会问创始人，他们会说这是他们的梦想或目标，或者我们会一起做很多事情。但你很少听到的是，其中也存在压力。那么，你当时是想出售公司，因为你觉得情况有点不妙，要么需要进行新一轮融资，要么就卖给别人，然后你发现 **LinkedIn** 是最好的选择，甚至是唯一的选择，或者说是最佳选择？

<details>
<summary>Original English</summary>
**主持人**: Yeah, it's nice that you know like for 10 plus years we can talk about this honestly because often times you see an acquisition by **LinkedIn** and of course you might ask the founders and they would say like this was our either our dream or our goal or we will do so many things together but some things that you don't often hear is well that there was a pressure involved as well. So, did you go into this wanting to sell the company because you saw that things were getting a little either you needed to raise a new round or you sell to someone and then you found **LinkedIn** to be the the best of or the only or or or the best option to to go into.
</details>

**Martin Kleppmann**: 我们尝试了一下，看看有哪些能产生收入的选择，但并没有真正成功。所以我们只是在烧钱，用户增长还可以，但不足以进行大额融资。所以我们有点陷入困境，而出售公司似乎是当时最不坏的选择。我对结果很满意，因为 **LinkedIn** 实际上很棒。他们对我们非常好。他们允许我们作为公司内部的一个独立团队运作。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: We tried a little bit to see like what revenue generating options we had and hadn't really managed to make that work. So, we were just burning money and our user growth was okay but not really enough to go and raise a big round. So we were like a little bit stuck there and selling the company seemed like the least bad option there in a way. And I'm pretty happy how it turned out because **LinkedIn** was great actually. They they were very good to us. They allowed us to operate as essentially like an independent team within the company.
</details>

**主持人**: 那么，你的团队仍然在一起工作吗？

<details>
<summary>Original English</summary>
**主持人**: So So your team stayed together?
</details>

**Martin Kleppmann**: 我们的团队仍然在一起。我们继续开发我们想要做的产品。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Our team stayed together. We continued working on the product that we wanted to make.
</details>

**主持人**: 哦，你们可以继续开发 **Reportive**？

<details>
<summary>Original English</summary>
**主持人**: Oh, you you got to keep working on **Reportive**?
</details>

**Martin Kleppmann**: 是的。实际上，**Reportive**，也就是 **Gmail** 浏览器扩展程序，有点被搁置了，但我们当时正在开发一款新产品，它最终以 **LinkedIn Intro** 的名字发布。当时它受到了有点奇怪的反响，发布后不久就被关闭了。这背后有一个更长的故事，但我仍然非常满意 **LinkedIn**，他们给了我们这样做的自由，并允许我们推出这款产品，尽管它没有成功，但他们在这个过程中对我们非常好。在那之后，产品被关闭，我们的团队也解散了。但我们在 **LinkedIn** 内部开发这款产品时度过了一段美好的时光。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes. Well, actually, so **Reportive** of the **Gmail** browser extension sort of got put on life support, but we were working on a new product at the time, which did eventually get released under the name **LinkedIn Intro**. It kind of got a slightly weird reception at the time and it ended up getting shut down shortly after we released it. This kind of longer background story there, but I'm still really happy with **LinkedIn** like how they gave us the freedom to do this and allowed us to launch this product and even though it didn't succeed, you know, they were very good to us throughout that process and then after that got shut down then our team got disbanded. But we had a good run within **LinkedIn** building this product.
</details>

**主持人**: 当时你们使用的技术栈是什么？

<details>
<summary>Original English</summary>
**主持人**: What tech stack did you work at the time which what do you use?
</details>

**Martin Kleppmann**: **Reportive** 的技术栈相当普通。它基本上是一个 **Rails** 应用程序，配有 **Postgres** 数据库，以及一些 **Redis** 和类似的东西混合在一起。所以，实际上并没有什么特别革命性的东西。我们基本上在 **Postgres** 之上构建了一个图数据库。所以其中有一些技术上的兴趣点，但没有什么特别出格的。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: The **Reportive** was fairly unexciting. It was a **Rails** app with a **Postgres** database basically and some **Redis** and some similar things like that mixed in. So actually you know nothing particularly revolutionary. We essentially built a graph database on top of **Postgres**. So there was a a little bit of technical interest in there but you know nothing particularly outrageous.
</details>

### LinkedIn与Kafka

**主持人**: 那么在 **LinkedIn Intro** 之后，你仍然在 **LinkedIn** 工作，据我所知，你从事数据基础设施方面的工作，对吗？

<details>
<summary>Original English</summary>
**主持人**: And then you you spent time after **LinkedIn Intro** you still work inside **LinkedIn** as I understand you worked on data infrastructure right?
</details>

**Martin Kleppmann**: 是的，数据基础设施。在我们的团队解散后，我转到了流处理团队。当时 **Kafka** 刚刚在 **LinkedIn** 开发出来，并且刚刚开源。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes data infrastructure. After our team got disbanded, I switched over to the stream processing team. So **Kafka** had just been developed at **LinkedIn** and had just been open sourced.
</details>

**主持人**: 哦，它刚刚开源。

<details>
<summary>Original English</summary>
**主持人**: Oh, it was just being open sourced.
</details>

**Martin Kleppmann**: 是的，我想它刚刚开源，然后我开始从事 **Samsa** 的工作，它是一个基于 **Kafka** 的流处理框架。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, I think it had just been open sourced and then I got to work on **Samsa** which was a stream processing framework on top of **Kafka**.
</details>

**主持人**: 我一直想问这个问题，现在正好问。为什么 **LinkedIn** 要构建或开发 **Kafka**？它现在已经成为如此基础性的技术，我一直很好奇，为什么一家公司会觉得有必要构建这种看起来非常通用、似乎每个人都需要的东西？

<details>
<summary>Original English</summary>
**主持人**: I always wanted to ask this question so this comes here. Why did **LinkedIn** build **Kafka** or or develop **Kafka**? Every time it's now such a fun foundational technology there always I was always curious like why did a company feel the necessity to build this thing that seems pretty generic and it seems everyone would have needed it.
</details>

**Martin Kleppmann**: 是的。我认为 **Jay Kreps** 在那个时期写了一篇非常好的博客文章，叫做《The Log》，他在其中解释了 **Kafka** 背后的动机，以及为什么把它做成一个追加日志（append-only log），而不是传统的**消息队列**之类的东西。我认为其动机主要是关于数据集成，因为当时有大量的数据库和事件生成系统，比如用户的活动事件，它们都以流的形式生成数据，然后有一大批下游系统想要消费这些数据，比如想把数据导入数据仓库，想把数据导入当时的 **Hadoop** 集群，以便在其上运行机器学习等任务。当时就存在一个数据集成问题，即如何实际地将数据从一个系统物理地取出并放入另一个系统。**Jay** 将 **Kafka** 设计成一个集成点，本质上就像是最低的公分母，但仍然是一个通用的抽象，用于集成各种数据源到下游数据接收器。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes. So I think **Jay Kreps** has a pretty good blog post from that era called **The Log** where he explains his motivation behind **Kafka** and why make it an append-only log rather than like a traditional message queue or something like that. I think the motivation was really about data integration because there were a whole bunch of databases and event generating systems, like activity events from users for example, they were all generating data that in a sort of stream shape and then a bunch of downstream systems that wanted to consume this like wanted to get it into the data warehouse and wanted to be able to get it into the **Hadoop** cluster at the time in order to run like machine learning and things over it and there was just this data integration problem of actually like how do you physically get the data out of one system and into another and **Jay** designed **Kafka** as this integration point essentially like the almost the kind of lowest common denominator but still a general purpose abstraction for integrating various data sources and to downstream data sinks.
</details>

**主持人**: 在 **LinkedIn** 这样规模的公司，从事 **Kafka** 的工作，你学到了什么？或者说，在这样规模的工作中，什么让你感到惊讶？据我所知，这是你第一次亲手接触真正大型的系统，对吗？

<details>
<summary>Original English</summary>
**主持人**: Working at **LinkedIn** at **Kafka** and at **LinkedIn** scale what did you learn or what surprised you about working at this type of scale as I understand this was for the first time that you hands-on worked at a really large system, right?
</details>

**Martin Kleppmann**: 没错，是的。因为之前我工作过的最大公司是 **Reportive**，只有五个人。我们有一个相当大的数据库，但它仍然是一个单实例数据库，从大局来看，规模并不算大。然后突然间，我来到了 **LinkedIn**，哦，我们得使用他们的大型 **Hadoop** 集群。那很有趣，当时用 **Java** 手写 **MapReduce** 任务。所以我在那里学到了很多东西。尤其是当流处理思想出现，**Jay** 推广 **Kafka** 的使用以及它能做的事情时。那对我来说真是一种启示，我突然觉得：“啊，这有点道理。”我开始理解这些各种数据系统是如何协同工作的，它们有什么共同点，以及基本原理是什么。所以那段经历直接促成了这本书的写作。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: That's right. Yes. Because previously the biggest company I had worked in was **Reportive** with five people. We had a sizable database but it was still like a single instance database and not really that big in the grand scheme of things. And then suddenly I was at **LinkedIn** and oh we got to use their big **Hadoop** cluster. That was fun like hand coding **MapReduce** jobs in **Java** at the time and so I learned a huge amount there. Especially when the stream processing ideas came up and **Jay** was evangelizing the use of **Kafka** and the things you could do with it. That was kind of a revelation for me really where I suddenly felt, "Ah, this kind of makes sense." I start to understand how these various data systems fit together what they have in common what the fundamental principles are and so that experience then fed directly into the writing of the book.
</details>

### 离开LinkedIn与写作生涯

**主持人**: 你是在什么时候决定离开 **LinkedIn** 的？对我来说，回顾你的职业生涯，从英国开始，创办一家初创公司，再创办第二家初创公司，参加 **Y Combinator**，搬到旧金山，被 **LinkedIn** 收购。大多数人会设想的轨迹是，好吧，在硅谷做更多事情，或者可能再创办一家初创公司等等。但你却决定离开 **LinkedIn**。

<details>
<summary>Original English</summary>
**主持人**: At what point did you decide to leave **LinkedIn**? To me, in in your careers, I'm looking through the career, start out in the UK, do a startup, do a second startup, **Y Combinator**, move to San Francisco, get acquired by **LinkedIn**. The arc that most people would draw would be, okay, do something more in Silicon Valley or maybe start a second startup, etc. And instead you decided to leave **LinkedIn**.
</details>

**Martin Kleppmann**: 是的。所以，首先我决定搬回英国，然后我继续为 **LinkedIn** 远程工作。这主要是因为我当时的女朋友（现在是妻子）仍在英国，异地恋并不好玩，而且我在湾区也感觉不太自在。所以我也没有真正鼓励她搬到湾区。我觉得我回到欧洲会更好，我对这个决定非常满意。我在湾区仍然有很多好朋友。我喜欢去那里旅游，但老实说，我不想住在那里。然后我仍然为 **LinkedIn** 远程工作，那段时间一切都很好。当我开始写这本书时，**LinkedIn** 甚至给了我 50% 的时间自由，让我可以在履行软件工程职责的同时写书，这真的很棒。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. So, first I decided to move back to the UK actually and I continued working for **LinkedIn** remotely. Okay. That was mostly because my girlfriend at the time, now wife, was still in the UK and long-distance relationship is not a lot of fun and I didn't feel that at home in the Bay Area. So, I wasn't really encouraging her to move to the Bay Area either. I thought it was better for me to go back to Europe and I'm very happy with that decision. Like, I still have a lot of great friends in the Bay Area. I love it as a place to visit, but I wouldn't want to live here honestly. Then I was still remotely working for **LinkedIn** and that worked all right for a while. When I then started writing the book, **LinkedIn** even gave me 50% of my time free to work on my book alongside my software engineering duties, which is really great.
</details>

**主持人**: 太棒了。是的，他们真是太好了。

<details>
<summary>Original English</summary>
**主持人**: Amazing. Yeah, that is so nice of them.
</details>

**Martin Kleppmann**: 绝对是。他们完全没有必要这样做。**LinkedIn** 也没有直接从中获得任何回报，除了他们可以用于内部培训目的的一本书。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Absolutely. And there they don't have to do that. And **LinkedIn** didn't directly get anything out of it in response other than like a book that they could use for internal training purposes.
</details>

**主持人**: 嗯，向 **LinkedIn** 致敬。

<details>
<summary>Original English</summary>
**主持人**: Well, shout out shout out to **LinkedIn** for this.
</details>

**Martin Kleppmann**: 是的，绝对是。不过后来我发现，一边做软件工程工作，一边值班等等，同时写一本书，我根本做不到。上下文切换太多了，值班的紧急事情很容易占据主导，然后就没有了写新东西所需的自由。所以过了一段时间，我决定，好吧，也许我最好全职专注于写书。所以我离开了 **LinkedIn**，休了一个无薪的学术假，也就是失业，只是为了全职专注于写书一段时间。然后，直到那之后，我才真正考虑进入学术界。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, absolutely. Though then I did find then that actually trying to write a book in parallel with doing a software engineering job and being on call etc. I just wasn't able to do it. It's just too much context switching and it's very easy for the urgent things from the on call to dominate and and then not to have the you know the freedom of that you need in order to to write something new. And so then after a while I decided okay like it's it's probably better if I focus full-time on the book. So I then left **LinkedIn** and just took a sabbatical unpaid sabbatical i.e. unemployment to just focus full-time on the book for a while and then it's only after that that I actually even considered getting into academia.
</details>

### 书籍的构思与写作

**主持人**: 那么这本书的想法是如何产生的？你是在什么时候决定要写书的？你当时心里决定要写什么？是已经有了这本书的布局，还是当时只是一个初步的想法？

<details>
<summary>Original English</summary>
**主持人**: So how did the idea of the book come? What was a point where you decided you would write and in your mind what were you deciding to write? What was was it already you know this this book with with with this layout or you had an early idea back then?
</details>

**Martin Kleppmann**: 我当时有一个想法，当然最终的产品看起来有所不同，但我认为总体目标保持不变。我当时知道我想写一些内容广泛的概念性概述。所以不是关于如何使用任何一个特定的系统或工具，而是比较许多不同类型工具之间的权衡。而且我知道我希望它以实践者为中心，不是一本理论教科书，而是人们可以用来构建真实系统的东西。这基本上就是我着手时的目标。这正是我希望在我刚开始工作时，比如在 **Reportive** 工作时能拥有的一本书，因为我们当时都在黑暗中摸索，我们的数据库遇到了性能问题，但我们基本上不知道该怎么办，因为我们完全缺乏理解问题所在和诊断问题的基础知识。所以我当时觉得，如果我对这些数据系统内部如何运作有更多的背景知识，那么我就能凭直觉知道如何调试这类性能问题。然后过了一段时间，在我对数据系统如何运作有了更多了解之后，我想，好吧，是时候把这些写下来了，这样其他人就不必通过艰难的方式学习，而是希望能更好地了解这些系统如何运作，从而更好地管理他们自己的数据系统。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: I had an idea that it of course the final product ended up looking somewhat different but the the overall goal I think stayed the same. So what I knew I wanted to write something that was a broad conceptual overview. So not about how you use any one specific system or tool but comparing the trade-offs between many different types of tools. And I knew that I wanted to be practitioner focused like not a theoretical textbook but something that people could use to build real systems. That was basically like the the goal with which I appreciate approached it. And this was exactly the book that I wish I had had when I was starting out and working at **Reportive** for example because we were all like searching around in the dark where we're having performance problems with our database and we had no idea what to do basically because we were totally lacking the foundations to actually understand what was going on and how to diagnose the issues. And so I felt that well if I had had a bit more background on how these data systems actually work internally then I could have had an intuition about how to debug these kinds of performance issues. And then after a while after I'd learned more about how data systems work I thought well okay it's it's time to write this down so that others don't have to learn it the hard way but can hopefully just get a better idea of how these systems work and thus be better at managing their their own data systems.
</details>

**主持人**: 首先，你是如何学习数据库如何工作的？因为从你在 **Reportive** 的故事来看，你构建了系统，遇到了一些性能问题，虽然规模比 **LinkedIn** 小。然后你在 **LinkedIn** 工作，看到了一些内部运作方式。但我知道很多软件工程师走过这条路，他们仍然不真正了解底层系统如何工作，他们只知道公司内部有一个平台团队来构建它。我可以阅读 **RFC**，但这需要大量工作，或者规划文档，我可以查看源代码。在我看来，即使在那时，你还是深入挖掘了。你使用了哪些资源？你是如何找到那些你后来写入书中的基础知识的？

<details>
<summary>Original English</summary>
**主持人**: To start with how did you learn about for example how databases work because again from from your story at **Reportive** you you build systems you've had some performance issues at a smaller scale to to be fair compared to **LinkedIn** then you worked at **LinkedIn** and you saw a little bit of how the sausage was made but I know a lot of software engineers who have been in this path and they still don't really know how the fundamental systems work they just know okay we have a platform team inside our company and they build it I could read the **RFC**'s but it's a lot of work or the planning docs I could look look at the source code it feels to me that even at that point you just went down and and tried to dig in. What resources did you use? How how did you find out those those basics which you later put into the book?
</details>

**Martin Kleppmann**: 很多时候，我只是好奇，并与人交流，问他们很多问题。在 **LinkedIn**，有很多资深的数据系统工程师，他们非常了解自己的领域，但可能没有必要把这些写下来。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: A lot of it was just kind of being curious and talking to people actually and just asking them lots of questions. And at **LinkedIn** there were like a bunch of senior data systems engineers who understood their stuff very well but hadn't maybe necessarily written it down.
</details>

**主持人**: 嗯。

<details>
<summary>Original English</summary>
**主持人**: Mh.
</details>

**Martin Kleppmann**: 所以我只是和他们中的很多人交谈，向他们提问，通过这种方式，我开始在自己的脑海中构建出这些东西是如何运作的图景。然后，一旦我从这些对话中掌握了基础知识，我就能够去阅读研究论文，例如。这些论文会更详细地解释事物是如何以及为何这样设计的。但是，你知道，阅读这些东西是很耗时的。所以，我尝试做的是，提取出真正重要的思想。我还阅读了大量的博客文章。所以，你看到书的每一章末尾有那么多参考文献的原因是，那实际上就是我自己用来理解正在发生的事情的材料。然后我想，好吧，如果我发现这些东西有用，那么我也会在书中引用它们，作为任何想要超越书中基础知识的读者进一步阅读的好资源。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: And so I just talked to a bunch of them and and quizzed them and that way started building an image in my own mind of how this stuff works. And then once I sort of got the basics from these conversations, then I was able to go and read research papers for example. They go into much more detail of exactly how and why things are designed in such a way. But you know it is time-consuming to read those things. So so then what I tried to do was like pull out what what are really the essential ideas. I just read a ton of blog posts as well. And so the reason why you see so many references at the end of each chapter in the book is well that is actually the material that I myself used in order to understand what was going on. And then I thought well okay well if I found these things useful then I'll also cite them in the book as a way for anyone any reader who wants to go beyond the basics covered in the book here are some some good sources to further reading.
</details>

**主持人**: 是的，这本书的结构，至少是第一版，分为基础数据系统、分布式数据和派生数据。如果我理解没错，这是三个主要部分。你在开始写书时就已经有了这样的结构，还是在写作过程中逐渐形成的？

<details>
<summary>Original English</summary>
**主持人**: Yeah, the the structure of the book, this first book at least, it's foundational data systems, distributed data, and derived data. If I understood, these are three big parts. Did you already have a structure in mind when you started writing the book or did it shape as you went?
</details>

**Martin Kleppmann**: 这三部分结构在本书的设计中并不是那么关键。这更像是事后我才想到：“哦，好吧，似乎我们可以把这些章节大致归类到这种结构中。”但章节的主题或多或少是我设想好的。所以我知道我想谈论事务到底是什么。我知道我想谈论复制。我知道我想谈论分片或分区。我知道我想谈论一致性和共识。这些高层次的主题，我想，从我最初给出版商的书籍提案中就已经很清楚了。每个章节内部的细节，那是我在写到该章节时才常常弄清楚的。所以我一次写一章，每章都从大量的背景研究开始，以便自己先掌握该主题。通常只有在那时，比如对于复制，我才决定：“好吧，看来实现复制的三种主要方式是单主、多主或无主。”

<details>
<summary>Original English</summary>
**Martin Kleppmann**: This three-part structure is not that critical in the design of the of the design of the book really. That's sort of more after the fact I thought, "Oh, well, it seems like we can group the chapters into roughly this sort of structure." But the topics of the chapters were more or less what I had envisaged. So I knew that I wanted to talk about like what a transaction actually is. I knew that I want to talk about replication. Knew that I wanted to talk about sharding or partitioning. Knew that I want to talk about like consistency and consensus. Those the sort of high-level topics I think were clear from like my initial book proposal to the publisher. The details within each chapter. That is something that I often figured out once I got to that chapter. So, I wrote one chapter at a time and started each chapter work with just a lot of background research to actually get up to speed on the topic myself. And it's often only then that say for then replication I decided okay well it seems like the three major ways of doing this are single leader, multi-leader or leaderless.
</details>

**主持人**: 嗯。

<details>
<summary>Original English</summary>
**主持人**: Mhm.
</details>

**Martin Kleppmann**: 我基本上是在开始写每一章时才决定这种结构，然后尝试将我想要表达的各种观点融入到这个叙事结构中。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: I would decide on that structure at essentially when I started writing each chapter and then try to fit the various points I wanted to make into into this narrative structure.
</details>

**主持人**: 作为一名也写过书的同行作者，我注意到在估算一本书的写作时间和估算一个软件项目的时间之间存在一些相似之处：你带着一个估算进来，如果你以前从未做过，你往往会大错特错。在你这段旅程中是怎样的？此外，你还有一位出版商，出版商有点像项目经理。他们喜欢有一个时间表。他们喜欢让你保持在正轨上。他们喜欢问什么时候能完成？你是如何管理这部分的？最后，你开始时估计会花多长时间，而实际又花了多长时间？

<details>
<summary>Original English</summary>
**主持人**: As a as a fellow author who also wrote a book, one thing I've noticed there's a bit of parallels between estimating a book and estimating a software project in that you come in with a estimate and if you've never done it before you tend to be wildly off. How was this in your journey? And and addition, you also had a publisher and publishers are are a little bit like project managers. They, you know, they they like to have a a schedule. They like to try to keep you on track. They they like to ask what when is it done? How did you manage that part as well? And and in the end, how long did you estimate it would take when you started and how long did it actually take?
</details>

**Martin Kleppmann**: 和往常一样，它花费的时间远远超过预期。我认为写书和软件项目都是如此。所以我想我花了大约四年时间写第一版，那不是四年全职，可能相当于两年半的全职工作量，但写了大约四年。所以它确实花了很长时间。我大大错过了出版商的截止日期。我想我错过了大约两年半左右。但幸运的是，**O'Reilly** 对第一版相当宽松，很乐意让我慢慢来，把它做好。到了第二版，**O'Reilly** 就变得有点咄咄逼人，催促我遵守截止日期。我想那时这本书已经很受欢迎了，人们都在 eagerly 等待第二版。所以我有点理解他们想要加速的愿望，但同时，我非常感谢第一版给予我的自由，可以按照自己的时间表工作。而第二版在这方面的自由就少了一些。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: As always, it takes vastly longer than expected. It's the same for software and projects as it is for writing, I think. So I think it took me about four years to write the first edition and that was not four years of full-time maybe like two and a half years of full-time equivalent or something like that but written over the course of about four years. So it definitely took a long time. The publisher deadline I missed by a ludicrous margin. I think I missed it by about 2 and a half years or something like that. But fortunately **O'Reilly** were pretty laid-back with the with the first edition and were happy for me to just take my time and make it good. When it came to the second edition then actually **O'Reilly** got a bit more aggressive and pushy about sticking to deadlines. I guess by that point the book had been established and people were waiting eagerly for the second edition. So, I kind of understand the the desire to to want to accelerate it, but at the same time, I I really appreciated the the freedom that I had for the first edition to work on my own schedule. And I had a bit less of that with the second.
</details>

### 可靠性、可伸缩性与可维护性

**主持人**: 第一版的标语，我相信和第二版是一样的，是“可靠、可伸缩、可维护系统背后的宏大思想”。可靠、可伸缩、可维护。这些目标对你意味着什么？

<details>
<summary>Original English</summary>
**主持人**: The tagline for the first edition, which I believe is the same as second edition, the big ideas behind reliable, scalable, and maintainable systems. Reliable, scalable, and maintainable. What do these objectives mean to you?
</details>

**Martin Kleppmann**: 是的。所以它们都有些模糊定义，对吧？所以没有对这些东西的正式定义。但对我来说，可靠性主要意味着容错。也就是说，一个系统总体上应该继续工作，即使网络链接中断或节点崩溃之类的。所以这本书的大部分内容是关于支持容错的技术，比如复制。嗯，这就是可靠性。可伸缩性是那些被大量提及的术语之一，它被提及得如此之多，而且让事物可伸缩似乎很时尚很酷，因为这暗示着成功和数百万用户，所以每个人当然都希望事物具有可伸缩性，因为每个人都希望这本书成功。我在这里试图采取一种更冷静的态度，说可伸缩性只是我们应对负载变化的机制。如果负载增加，我们如何向系统添加计算容量，例如，以便系统仍然继续工作。然后你用来实现可伸缩性的技术，比如分片。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. So they're all slightly vaguely defined, right? So there's there's not a a formal definition of those things. But for me, reliability means fault tolerance primarily. So meaning that a system should on the whole continue working even if like a network link is interrupted or a node crashes or something like that. So a lot of the book is about techniques that support fault tolerance like replication for example. So that's reliability. Scalability is one of those terms that gets thrown around a lot and it's sort of so much and it's it's like fashionable and cool to make things scalable, you know, because it's it suggests success and millions of users and so that's of course everyone wants things to be scalable because everyone wants success for this book. Here tried to take a bit more dispassionate kind of approach and said scalability is just like what mechanisms we have for dealing with changes in load if load increases how can we add computing capacity to a system for example so that the system still continues working and then the techniques that you use to achieve scalability well they are like sharding for example and and but in this case.
</details>

**主持人**: 在这种情况下，可伸缩性，你的定义，我是否理解为你主要指的是横向可伸缩性，所以它们不能计算向上或向下？

<details>
<summary>Original English</summary>
**主持人**: Scalability your definition do I understand that you're mostly referring to horizontal scalability so they cannot compute up or down pretty much.
</details>

**Martin Kleppmann**: 是的，我想是因为那是更有趣的一个。是的，你总是可以买一台更大的机器。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, I guess because that's the the more interesting one like yes, you can always buy a bigger machine and.
</details>

**主持人**: 那有什么有趣的呢？

<details>
<summary>Original English</summary>
**主持人**: What's interesting about that.
</details>

**Martin Kleppmann**: 没错，关于这一点没什么好说的。我的意思是，即使在单机上也有如何扩展的细节，但我认为现代云服务和一般的后端服务之所以变得有趣，部分原因在于它们引入了横向可伸缩性和无共享系统的概念。所以我们可以构建能够应对非常高负载的系统，即使单个组件只是相当便宜的商用机器。但也许可伸缩性故事的一部分，我当时没有考虑那么多，但最近开始更多思考的是，不仅仅是向上扩展，还有向下扩展。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: And exactly there's just there's not that much to be said about it. I mean there are details of how you scale even on a single machine but I think like part of what is become interesting about like modern cloud services and just backend services in general is like how they've introduced this idea of horizontal scalability and shared nothing systems. So we can build systems that you know are able to cope with very high load even if the individual components are just fairly cheap commodity machines. But maybe sort of part of the scalability story which I wasn't thinking about as much at the time but started thinking about more recently is not just scaling up but scaling down as well.
</details>

**主持人**: 那么实际上，你如何以这样一种方式运行服务：如果它的负载非常小，运行成本就会非常低？这在某种程度上与如何在高负载下继续运行服务是同一个问题。

<details>
<summary>Original English</summary>
**主持人**: So actually how do you run a service in such a way that if it has a very small amount of load it's really cheap to run it. That's sort of a in a way the same question as how do you continue running a service if it has very high load.
</details>

**Martin Kleppmann**: 嗯，通常你只是希望成本和计算容量与你拥有的负载大致成比例。而在低端，这意味着能够向下扩展到运行成本极低的东西。这并不一定是理所当然的。例如，对于本地部署的软件来说，这很难做到，因为如果你有一台物理机器，它就是一个部署单元，是的，你可以把它分割成几十个虚拟机，并使这些虚拟机很小，但它仍然需要某种资源分配。所以，例如，一些无服务器系统之所以有趣，部分原因在于它们能够向下扩展，并说：“好吧，如果你每天只处理三个请求，那也完全没问题。”

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Um generally like you just want the the cost and the computing capacity to be roughly proportional to the load that you have. And at the low end that means actually being able to scale down to something that is extremely cheap to run. And that's like not so necessarily a given. That's something that is hard with on premises software for example because like if you've got a machine a physical machine that's like a a unit of deployment and yes you could carve it up into two dozen virtual machines and make those small virtual machines but um it still requires like some sort of resource allocation. So so part of what's interesting about some serverless systems for example is actually their ability to scale down and say like okay if you're going to handle just three requests per day that's just fine as well.
</details>

**主持人**: 你能告诉我第二版的情况吗？这个想法是什么时候产生的？

<details>
<summary>Original English</summary>
**主持人**: Can you tell me about the second edition? When did the idea come about?
</details>

**Martin Kleppmann**: 是的，几年前就已经很清楚需要第二版了，仅仅是因为第一版有点过时了。技术发生了变化，而第一版中没有反映出来。所以，我想更新它，但你知道，我现在有了一份学术工作。我主要是在做研究和教学，更新这本书在某种程度上只是我的副业。所以，进展相当缓慢，因为我总是在做其他项目的同时进行这项工作，本质上又回到了我写第一版时遇到的上下文切换问题，只是现在我有一份学术工作，我不想放弃，因为我实际上很喜欢它。最初，第二版的进展非常缓慢，我也意识到我有点脱离了当前的行业实践，因为我转到了学术界。我在理论方面深入了很多，但我不再了解人们在使用数据湖之类的东西时在做什么。所以，在某个时候，我记起了 **Chris Rkamini**，一位来自 **LinkedIn** 的老同事。我曾和他一起从事流处理方面的工作。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, it it had been clear for a couple of years that the second edition was needed just because the first edition was getting a bit dated. There were changes in technology that just hadn't been reflected in the in the first edition. So, I I wanted to update it, but you know, I now have an academic job. I'm actually like doing research and teaching is my main thing, and updating the book is just a sort of sideline business on the side in some sense. So it actually took quite a while to make progress with that because I was always doing it alongside other projects and essentially back to that context switching problem that that I had while writing the first edition but just now with an academic job that I didn't want to just drop because actually quite enjoy it initially then I made very slow progress with the second edition and also I kind of realized that I had slightly lost touch with current industry practices because you know I'd switched over to the the academic side. I gone much deeper on the theory. But I was no longer up to speed on like what people were doing with say data lakes or things like that. So then at some point it I remembered **Chris Rkamini**, an old colleague from **LinkedIn**. I had worked with him on the stream processing stuff.
</details>

**主持人**: 你和他一起工作过。他是 **The Missing ReadMe** 的作者。

<details>
<summary>Original English</summary>
**主持人**: You work with him. He's he's the author of **The Missing ReadMe**.
</details>

**Martin Kleppmann**: 没错。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Exactly.
</details>

**主持人**: 哇，世界真小。

<details>
<summary>Original English</summary>
**主持人**: Wow. What a small world.
</details>

**Martin Kleppmann**: 是的。我读过 **Chris** 的书 **The Missing ReadMe**，觉得“哦，他是个很棒的作家。”我曾和他一起做软件工程师，发现他是一位很棒的同事，而且他还一直在写一份名为 **Materialized View** 的新闻通讯，内容主要是关于数据系统最新趋势的，并成为了该领域的初创公司投资者。所以，在某个时候，我想，好吧，我得联系 **Chris**，问他是否愿意帮助我完成第二版。他很乐意这样做。这变成了一次非常好的合作，因为他了解行业中最新技术的前沿动态。我对于如何教学有很强的看法。所以，如何解释书中的内容，确保我们以一种非常精确、措辞非常谨慎，但同时又非常易懂的方式解释所有内容，以便读者能够轻松阅读。所以我们基本上结合了我的写作风格和 **Chris** 对最新行业趋势的了解，使这本书与时俱进，那是一次非常棒的合作。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. And I I had read **Chris**'s book, **The Missing ReadMe**, and thought, "Oh, he's a great writer." And I had worked with him as a software engineer and found him him a great colleague and also he had been writing this newsletter called **Materialized View** on like latest trends in data systems essentially and become a startup investor in in that space. And so at some point I thought, well, actually I have to get in touch with **Chris** and ask him whether he wants to help out with the second edition. And he was keen to do that. And that turned into such a good collaboration because he was up to date on like what the cutting edge was in terms of technology in industry. Um, I had strong opinions on how to teach essentially. So how to explain things in the book, make sure that we were explaining everything in a in a way that was like very precise, very carefully chosen words, but at the same time very accessible so that it's hopefully easy to read. And so we took essentially like my writing style plus **Chris**'s knowledge of latest industry trends to bring the book up to date and that was a a great collaboration.
</details>

### 第二版的新增与删减

**主持人**: 你们新增了哪些重要内容？其中哪些是你一开始就知道会缺失的，哪些是在写作过程中才意识到需要加入的？

<details>
<summary>Original English</summary>
**主持人**: What are the big things that you added that and and which ones of these you knew would be missing and which ones did you realize during the writing process that okay this needs to be in here now?
</details>

**Martin Kleppmann**: 是的，我们从一开始就知道要反映的是云原生系统架构。这是一个有点模糊的术语，但我的意思是，它本质上是在云服务之上构建数据系统作为基础抽象。在第一版中，基本假设是你有一些机器。每台机器都有一些本地磁盘。你可以在一台机器上运行数据库实例。它会将数据写入本地磁盘。如果你想将其复制到另一台机器，那么数据库软件会在数据库层面将其复制到另一台机器，该机器也会将数据写入其本地磁盘。很长一段时间以来，计算机就是这样工作的。而现在，人们突然开始在对象存储之上构建数据库，例如。现在，复制发生在对象存储层面，不再是数据库层面。或者也许数据库层面仍然有一些复制，但如果你在对象存储之上构建，事情的性质真的改变了。这与在虚拟块设备（如 **EBS**）之上构建不同，因为这些块设备虽然是云服务，但它们仍然提供一种单节点操作系统抽象，即在其之上运行文件系统的块设备，而对象存储则是一种全新的抽象，它看起来与文件系统不同，行为也不同。所以，在第一版出版时，人们已经开始在对象存储之上构建作为基础抽象，但自第一版以来，这种做法已经真正普及开来，现在已经有大量系统以这种方式构建。所以，这是一个我们真正想要融入的想法，我们将其贯穿于整本书中。所以它不仅仅是一个单独的部分，而是一个我们整合到整个叙事中的想法。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, so the thing we knew from the start that we wanted to reflect was cloud-native systems architecture. It's it's a bit of a vague term but what I mean with that is essentially building data systems on top of cloud services as the foundational abstraction in the first edition the assumption was basically that you have some machines. Each machine has some local discs. You can run a database instance on a machine. It will write its data to the local disk. If you want to replicate it to another machine, then well the database software will replicate it at the database level to another machine which will also write the data to its local discs. For a long time that was exactly the way computers worked. And now suddenly people are building databases on top of object stores for example. And now the replication happens at the object store level. No, no longer at the database level. Or maybe there's still some replication at the database level but it really changes the the nature of things if you're building on top of an object store and this is different from say building on top of a virtual block device like **EBS** or so because these block devices although they are cloud services but they still offer the abstraction that is a sort of single node operating system abstraction of a block device on top of which you run a file system whereas an object store is just like a brand new abstraction it just looks different from a file system, it behaves differently. And so then building on top of that as a foundational abstraction is something that like people were starting to do at the time of the first edition, but since the first edition that has really taken off like a whole lot of system have have been built in that style now. And so that's an idea that we really wanted to incorporate and we weaved that in throughout the book. So it's not just like one section here. But it's it's sort of a an idea that we've integrated throughout the entire narrative.
</details>

**主持人**: 现在也有很多托管服务。我们使用的基本原语，但也有很多云提供商使用的托管服务，很多工程师常常直接使用托管服务，因为它们负责复制。它们有正常运行时间的服务水平协议（**SLA**）等等。但是当你基于这些东西构建，并且你将它们作为原语使用时，作为一名软件工程师，是否会存在不再有动力去理解底层架构的风险？或者说，我们是否因此构建了更好的系统？你是如何看待这个问题的？感觉因为云，抽象层次发生了变化，对吗？

<details>
<summary>Original English</summary>
**主持人**: There's now a lot of managed services as well. The per primitives that we use, but there's also so many managed services that all the cloud providers use and a lot of engineers, they often just use the managed services as is because they they take care of replication. They have **SLA**s for uptime and so on. But when you build on top of these things and you you kind of use those as a as primitives as well, is there any risk as a software engineer that you're no longer incentivized to understand the underlying layer or are we building better systems because of that? How do you think about this? It it feels there's a move of abstraction because of cloud, right?
</details>

**Martin Kleppmann**: 是的，这确实是向不同且更高层次抽象的转变，但你知道，这自计算机工业诞生以来就一直是整个行业的故事。它就像是构建新的抽象。所以，如果你依赖于更高层次的抽象，你就不再考虑底层细节，这是事实。因此，如果你使用带有垃圾回收器的编程语言，你就不再考虑内存分配。那么这是一种损失吗？嗯，也许吧。如果你正在构建底层系统，你仍然需要关心内存分配。如果你正在构建更高层次的业务逻辑。实际上，我认为人们不关心内存管理是完全没问题的。所以我认为数据系统也存在类似的情况，如果你正在构建不需要特别关心底层基础设施的更高层次系统，那么这没问题。只需使用更高层次的抽象即可。这没什么不对。但仍然需要有人从更低层次的组件构建这些更低层次的抽象。总得有人来实现云服务。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, it's definitely a a shift to different and higher level abstractions, but you know that's been the story of the entire computing industry since the start. It's like building new abstractions. So it is true that like if you rely on a higher level abstraction, you're no longer thinking about the lower level details. And so it's you're using a a programming language with a garbage collector, you're no longer thinking about memory allocation. And so is that a loss? Well, maybe. Like if you if you're building low-level systems, you should still have to care about memory allocation. You're building higher level business logic. Actually, I think it's just fine for people not to care about memory management. So I think there's an analogous thing here with data systems that if you're building the higher level systems that don't need to particularly care about the underlying infrastructure, then that's fine. Just use the higher level abstractions. Nothing wrong with that. But somebody still has to build those lower level abstractions from lower level components. Somebody's got to implement the cloud services.
</details>

### WorkOS与Statsig赞助

**主持人**: **Martin** 谈到了使用云服务带来的权衡。现在是时候谈谈我们的本季赞助商 **WorkOS** 了。如果你读过 **Designing Data-intensive Applications**，你就知道构建大规模系统就是关于权衡的。但有一件事不是权衡，那就是企业级功能。当你获得更大的客户时，你需要 **SSO**、目录同步、**RBAC**、审计日志，所有这些他们期望开箱即用的功能。自己构建这些可能需要数月。**WorkOS** 提供 **API**，让你几天内就能实现，这样你就可以专注于你的核心产品。这就是为什么像 **OpenAI** 和 **Anthropic** 这样的公司都在使用 **WorkOS**。访问 **workos.com** 了解更多。

<details>
<summary>Original English</summary>
**主持人**: **Martin** talked about trade-offs that come with using cloud services. And this is a good time to talk about our season sponsor **WorkOS**. If you've read **Designing Data-intensive Applications**, you know that building system at scale is all about trade-offs. But one thing isn't a trade-off. That's enterprise features. The moment you land bigger customers, you need **SSO**, directory sync, **RBAC**, audit logs, all the things they expect out of the box. Building that yourself can take months. **WorkOS** gives you **API**s to ship it in days so you can stay focused on your core product. That's why companies like **OpenAI** and **Anthropic** run on **WorkOS**. Visit **workos.com** to learn more.
</details>

**主持人**: 我还要提一下我们的主要赞助商 **Statsig**。**Statsig** 构建了一个统一平台，既能实现实验，又能实现持续发布。内置实验意味着每一次发布都会自动成为一个学习机会，通过适当的统计分析，精确展示功能如何影响你的指标。特性标志让你能够自信地持续发布。由于所有功能都在一个平台上，拥有相同的产品数据，你的组织内各团队可以协作并做出数据驱动的决策。要了解更多信息，请访问 **statsig.com/pragmatic**。

<details>
<summary>Original English</summary>
**主持人**: I'd also like to mention our presenting sponsor **Statsig**. **Statsig** build a unified platform that enables both experimentation and continuous shipping. Built-in experimentation means that every roll out automatically becomes a learning opportunity with proper statistical analysis showing you exactly how features impact your metrics. Feature flags let you ship continuously with confidence. And because it's all in one platform with the same product data, teams across your organization can collaborate and make data-driven decisions. To learn more, head to **statsig.com/pragmatic**.
</details>

**主持人**: 接下来，让我们回到 **Martin** 和使用云服务所带来的权衡。

<details>
<summary>Original English</summary>
**主持人**: With this, let's get back to **Martin** and the trade-offs that come with using cloud services.
</details>

### 抽象层次与系统内部

**Martin Kleppmann**: 所以那些人将不得不更专业地从事如何工程化这些云服务的细节，如何使它们可靠，如何操作它们等等。技能仍然存在。只是发生了一些专业化，有些人可以担心更高层次的事情，而不必关心更低层次的事情。有些人专注于更低层次的事情，并将更高层次的方面视为他们的客户。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: And so those people will have to then specialize even more in actually the details of how you engineer those cloud services, how you make them reliable, how you operate them and so on. The skills are still there. It's just a bit of specialization happening that some some people can worry about the higher level things without having to concern themselves with the lower level things. Some people focus on the lower level things and treat that higher level aspect as their customers.
</details>

**主持人**: 有趣。所以在我看来，如果你是一名工程师，使用了大量这些服务，你可能不需要确切了解它们是如何工作的。

<details>
<summary>Original English</summary>
**主持人**: Interesting. So it it sounds to me that if you're an engineer who is utilizing a lot of these services, you might not need to know how they exactly work.
</details>

**Martin Kleppmann**: 是的。我想说，整本书的底层哲学是让人们深入了解系统内部运作的本质。这样，如果他们开始出现奇怪的性能行为，你就能对为什么会这样以及如何解决它有一些直觉。例如，存储引擎那一章会告诉你 **B-树** 如何工作，以及日志结构化合并树（**LSM 树**）存储引擎如何工作。这本书并不是为那些将要实际构建自己的数据库和实现自己的存储引擎的人准备的。如果你想这样做，你需要比这本书涵盖的深度更深入得多。但其理念是，作为一名应用程序开发者，如果你对存储引擎的内部工作原理有一些了解，你就能更好地以一种能提供良好性能的方式使用它，并诊断任何问题。我们也将这种哲学保留在云服务的背景下，是的，云服务隐藏了一些应用程序开发者不再需要考虑的操作细节，但他们仍然应该对它们内部如何工作有一些了解，以便有效地使用它们。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes. And I would say like the underlying philosophy of the entire book is to give people insights into just the sort of essence of how the systems work internally. So that if for example they start having weird performance behavior, you can have a bit of intuition for why it's doing that and how you might solve it. So for example, say the storage engine chapter tells you about how **B-trees** work and how log-structured **LSM trees** storage engines work. And the book is not intended for people who are going to actually build their own databases and implement their own storage engines. If you want to do that, you have to go much much more much greater depth than this book covers. But the idea is that as an app developer, if you know just a little bit about how the storage engine works internally, you'll be in a much better place to use it in a way that is that gives you good performance for example and to diagnose any issues. That philosophy we've kept also in the context of cloud services where yes, like cloud service hides some of the operational details that app developers don't need to think about anymore, but they should still know a bit about how they work internally just so that they can use them effectively.
</details>

**主持人**: 我想我是在争论权衡取舍，决定使用哪种服务，以及要关注哪些特性。

<details>
<summary>Original English</summary>
**主持人**: I guess I argue about the trade-offs deciding on which which service to use, which characteristics to look out for.
</details>

**Martin Kleppmann**: 是的。对于你的用例，对吗？没错。而且，你知道，如果你在做分析，使用行式存储还是列式存储，这之间有巨大的差异。这有点技术性，甚至需要一些背景阅读才能理解这意味着什么，但它对系统最终行为的性能有巨大的影响。所以，这些地方我觉得了解一些内部原理实际上是一种超能力。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. For for your use case, right? Exactly. And and you know, they're huge differences of say if you're doing analytics whether you're using row oriented storage or column oriented storage. That's a bit of a technical distinction and it takes a little bit of background reading to even understand what that means, but it has a massive performance implication in terms of the final behavior of the system. And so those are those places where I feel like knowing a bit about the the internals is actually like a superpower.
</details>

**主持人**: 是的，我想工程师们总是需要争论或者至少应该争论的一点是成本与性能。而我所说的性能是指用户的延迟，当然还有弹性，如果发生什么事情，比如一个区域故障，一个可用区故障，一台机器故障，一个可用区故障，一个区域故障，我们的产品会受到怎样的影响，以及什么是可接受的。那里的基本思想似乎是，你愿意承担多少可用性风险，以及系统本身的开销，比如计算开销，还有实际设计和操作系统的人力开销，以及成本开销。

<details>
<summary>Original English</summary>
**主持人**: Yeah. And I guess engineers the one thing that we always need to argue about or should need to argue about is at the very least cost versus performance. And by performance I mean latency to the user and of course resilience of if if something happens you know like a region go like a zone goes down a machine goes down zone goes down region goes down how our product is affected and what's acceptable. The basic idea there seems to be like how much availability risk are you willing to take on versus the both like the overheads in terms of um the the system itself like the computational overheads but also the human overheads actually designing and operating the system and and the cost overhead.
</details>

**Martin Kleppmann**: 是的，没错。所以，是的，你可以拥有一个更能容忍各种类型故障的系统，但它的设计和操作成本更高，而一个更简单的系统，你知道，它可能会更频繁地宕机，但成本更低。这没有对错之分。每个人都需要自己弄清楚他们在这个权衡空间中的位置。我想说，多区域部署是朝着更高可用性方向发展，因为它意味着你可以容忍整个区域的停机。但这会对你在不同区域之间获得的一致性模型产生影响。所以，这是这本书试图非常明确地指出的一个权衡，以帮助人们理清思路，找出对他们来说什么是正确的选择。就多云而言，例如，我最近一个月一直关注的一件事是欧洲对美国云服务的依赖。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, exactly. And so yes, you can have a a system that is more able to tolerate various types of faults but it which is more expensive to uh to design and operate versus a simpler system that you know might go down a bit more often but which is cheaper. And there's no right and wrong with that. You know it's a everyone needs to figure out where they sit on that on that trade-off space themselves. And I would say that like multi-region is like pushing in the direction of like higher availability because it means you could tolerate the outage of an entire region. But then it has implications on the consistency model that you can get across different regions for example. So that's a trade-off that the book tries to make very explicit to help people reason that through of like what is the right choice for them. In terms of multi-cloud, for example, one thing that I've been concerned about just in the last month really is European dependence on US cloud services.
</details>

**主持人**: 是的。那么，如果地缘政治出现严重问题，紧张局势升级，欧洲突然被排除在美国云服务之外，会发生什么？

<details>
<summary>Original English</summary>
**主持人**: Yes. So what if geopolitics was to go horribly wrong and tensions escalate and Europe finds itself suddenly locked out of US cloud services?
</details>

**Martin Kleppmann**: 我希望那不会发生。我仍然认为这不太可能，但它不再是不可想象的了。因此，我从欧洲的角度出发，一直在思考我们如何设计系统来应对这种事情，而这不仅仅是区域性中断，它本质上是一种业务风险，而多云设置可以帮助缓解这种风险，这样至少，例如，如果一家公司将你拒之门外，你仍然可以在另一家公司拥有系统。这再次非常倾向于昂贵但高可用性风险降低的一端。但对于那些工作负载确实非常关键，并且他们认为这种地缘政治风险是足够大的风险的人来说，我认为认真考虑这种设置是值得的。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: I hope that doesn't happen. I still think it's fairly unlikely, but it's no longer unthinkable. And and as a result I coming sort of from this European perspective have been thinking a fair bit about how can we engineer systems to be resilient against that sort of thing and that's you know not just like a regional outage but it's like a a business risk essentially and a multi-cloud setup could help mitigate against that sort of risk so that at least for example if one company locks you out then you could still have systems on on another company again that that's very much towards the expensive but high availability risk reduction end of the spectrum. But for the people who have you know really critical workloads where they think this sort of geopolitical risk is a significant enough risk I think it's seriously worth considering that kind of setup.
</details>

**主持人**: 我认为我们有责任，因为除了我们，谁还会做这件事呢？

<details>
<summary>Original English</summary>
**主持人**: I'm thinking that that as we do have the responsibility because because who else will will do this?
</details>

**Martin Kleppmann**: 是的，完全正确。但我完全同意你的观点，即理解风险并沟通权衡取舍，我认为这将是我们作为工程师未来核心职责的一部分。也许随着 **AI** 编写我们越来越多的代码，它将不再是关于你如何用特定的编程语言表达逻辑的细节，而更多是关于那些高层次的权衡取舍。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes, totally. But I totally agree with you as well that this understanding what the risks are and communicating what the trade-offs are I think is is going to be a core part of our role as engineers moving forward as well. Maybe as **AI** writes more and more code of our code, it's less about like the details of how you express logic in a particular programming language and much more about those kinds of high-level trade-offs.
</details>

### 可伸缩性与分片

**主持人**: 在这本书中，可伸缩性的定义是如何变化的？因为正如我们之前谈到的，在云出现之前，构建可伸缩系统听起来非常复杂，因为构建一个横向可伸缩系统非常复杂，你需要把所有组件都组合在一起。在第一版书中，你详细描述了这一点。有了云，很多服务实际上都定义了它们如何实现横向伸缩以及权衡是什么。你是否觉得在使用这些原语时，更容易理解可伸缩性？

<details>
<summary>Original English</summary>
**主持人**: How has the definition of scale changed in this book? Because as we talk with cloud before cloud building a scalable system it sounded pretty involved because building a horizontally scalable system it's it's complicated all all the pieces you need to put it in in the first book you detail a lot of this with cloud a lot of the services actually they do define how they allow horizontal scaling what the tradeoffs are do you feel that it's made a lot easier to reason about scale scalability when you are using these primitives?
</details>

**Martin Kleppmann**: 我认为实现真正高规模仍然具有挑战性，因为尽管我们有云服务，比如对象存储，它提供了非常弹性的存储模型，至少你不再需要担心磁盘的容量规划，也不用担心磁盘空间不足，因为这些操作性的事情它们会处理。但是如果你需要分片，例如，这实际上会反映在应用程序代码上，你无法完全透明地实现它。所以如果你处于足够大的规模，分片是必需的，因为一台机器不足以处理你的工作负载。那么我认为即使使用云系统，你仍然需要做大量的工程思考，思考如何实现这一点。我认为云在向下扩展的低端帮助很大。如果你想要一个非常轻量级的服务，只处理少量请求。我们拥有的无服务器系统能够非常快速地启动和关闭一个非常轻量级的实例，这是一个很好的创新，它使得那些非常低规模的服务成为可能，而如果没有云服务，这将很难做到，因为你必须静态地为特定的虚拟机分配一定量的内存和一定的 **CPU** 资源。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: So I think achieving Being really high scale is still challenging because even though we have cloud services like object storage for example which provide you this very elastic storage model at least you don't have to worry about capacity planning on your discs anymore and running out of disk space because those kinds of operational things they're taking care of but if you need sharding for example that's something that actually does reflect on the application code as well you can't really make that entirely transparent and so you're at a sufficiently large scale The charting is required because a single machine is not powerful enough to process your workload. Then I think even with cloud systems you still have to do quite a bit of engineering thinking of of how to realize that where I think the cloud has helped quite a bit is actually at the lower end of scaling down. If you want to have a very lightweight service that processes only a small number of requests. What we've got with serverless systems being able to very quickly spin up and spin down an instance very lightweight that's quite a a good innovation that has enabled those those very low scale services and that's something that's would be much harder to do without cloud services because you would have to statically allocate a certain amount of memory and certain **CPU** resources to a particular virtual machine.
</details>

**主持人**: 我喜欢无服务器。我有一个小型网站运行在无服务器上，我的账单是每月 13 美分，因为它负载很小。

<details>
<summary>Original English</summary>
**主持人**: I love serverless I I have a small website that runs on serverless and my bill is like 13 cents per month because it has very little load.
</details>

**Martin Kleppmann**: 绝对是。它只是更有效地利用计算资源。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Absolutely. It's just making more efficient use of computational resources.
</details>

**主持人**: 让我们谈谈分片。在第一版书中，以及你写第一版书时，我在 **Uber** 工作，我们谈论了很多分片，并且有很多内部实现或面试都涉及分片，因为我们当时正在设计分片系统。我确实感觉到，随着时间的推移，随着云系统开始提供更多交钥匙解决方案，更像平台，你发送数据，它会处理这些事情，需要实际实现分片的工程师越来越少。在你的研究中，你看到了什么？在哪些情况下，分片仍然很重要？在哪些情况下，它可能已经不再是一个问题了？我的意思是，知道它仍然很好，但你可能不需要实现它。

<details>
<summary>Original English</summary>
**主持人**: Let's talk about sharding. In in the first book and when you wrote the first book when I was working at **Uber**, we talked a lot about sharding and there was a lot of internal implementations or interviews involved asking about sharding because we were designing systems that were sharding. I did sense that over time again as as cloud systems start to become available that give you turnkey solutions more that act more like platforms. You send the data and it takes care of of these things. Fewer engineers have to actually implement sharding with cloud native systems in your research. What have you seen? What what are the cases where putting sharding in place is still important and where are the places where it it might have just disappeared as a as a concern? I mean it's still nice to know but you might not have to implement it.
</details>

**Martin Kleppmann**: 我认为这可能更多是硬件变得更强大，而不是云的影响。现在一台大型机器可以做很多事情。如果你有一台大型机器，这意味着越来越多的工作负载可以在单机上运行，这实际上已经足以实现相当大的规模。仍然存在如何有效利用单机上数百个 **CPU** 核心的问题，所以并行性仍然是需要考虑的问题，而分片是实现并行性的一种方式。但至少这种跨多台机器的分片可能已经不再是一个紧迫的问题，仅仅是因为越来越多的工作负载可以在单机上运行。有些人仍然有非常大规模的工作负载，确实需要跨多台机器进行分片，但它并没有完全消失。而且复制仍然与较小规模相关，因为那是为了容错，而不是为了可伸缩性。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: I think it's probably less of an effect of cloud and more of just hardware getting more powerful that oh actually like a big machine nowadays can do a lot on a big machine you if you and that means that more and more workloads you can just run on a single machine and that is sufficient actually to achieve quite significant scale already there's still concerns of like how to actually efficiently make use of hundreds of **CPU** cores that you have on a single machine so there's still parallelism is still are a required thing to think about there and sharding is one way of achieving parallelism. But at least this sort of sharding across multiple machines is maybe become less of a pressing issue just because more and more workloads can just run on a single machine. Some people still have very large scale workloads that do have to be sharded across multiple machines but it's not going away entirely and replication is still relevant even at smaller scales because that's for fault tolerance that's not for scalability.
</details>

### 分布式系统中的问题

**主持人**: 你有一章叫做《分布式系统中的问题》，其中介绍了许多可能出错的事情。在不深入整章内容的情况下，你能回忆起一些让你印象深刻或你觉得重要的东西吗？

<details>
<summary>Original English</summary>
**主持人**: You have a chapter called the troubles with distributed systems which goes through a lot of things that can go wrong without going through the whole chapter. Can you recall some of the things that are memorable to you or some of the things that you feel are are important to remember?
</details>

**Martin Kleppmann**: 是的。这一章的全部思想是，在分布式系统理论中，我们倾向于假设某些事情。例如，我们只是假设消息在网络上传输的时间没有上限。所以你发送一条消息，它可能在 100 微秒内到达，也可能需要 10 年，分布式系统理论只是尽量不对此类时间做出任何假设。或者更确切地说，有些理论确实做出了这些假设，但这是一个危险的假设，因为偶尔网络延迟确实会比典型情况高得多。另一件事是关于崩溃。例如，分布式系统理论只是说节点可能会崩溃，但这实际上意味着什么？在实践中，节点变得不可用意味着什么？它可能是一个软件崩溃，但它也可能是一个硬件故障。它可能是有人拔掉了电源线。它可能是节点实际上仍在运行，但只是与网络断开连接了。这本书这一章的重点是捍卫和证明我们用于分析分布式系统的那些理论模型，并提供大量故事和案例研究，表明实际上确实有很多事情会出错，而且不要相信任何说“哦，故障很少见，别担心，没关系”的人。这一章的真正寓意是，如果你想让系统可靠，你确实必须担心一大堆奇怪的、不寻常但肯定可能发生的边缘情况。时间是其中之一，比如，你知道，很容易假设你的时钟是正确的，而且大多数时候时钟都相当正确，但我们不能完全依赖它，因为实际上它们总体上不够精确。所以很多时候，人们很容易做出某些假设，认为事情会表现良好，而在分布式系统中，如果我们希望系统即使在出现问题时也能可靠地工作，我们就必须努力摆脱这些假设。但写这一章真的很有趣，因为它本质上是大量出错事情的集合。所以我查阅了许多科技公司发布的事故报告，以便了解“好吧，事情出错的根本原因是什么？我们能从中吸取哪些适用于整本书的教训？”而且，你知道，有一些有趣的事情，比如鲨鱼咬海底电缆并损坏它们，这本身就是一个很棒的故事。然后我听说近年来海底电缆的屏蔽做得更好了，所以鲨鱼不再咬它们了。但相反，陆地上的牛正在踩踏电缆，偶尔会以这种方式造成网络中断。你知道，这类事情让它变得更有趣。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. The whole idea of this chapter is that in distributed system theory there are certain things that we tend to assume. Like for example, we just assume that there's no upper bound on how long it might take for a message to go over the network. So you send a message, it might arrive within a 100 microseconds or it might take 10 years and distributed system theory just doesn't make any assumptions about that sort of timing if we can avoid it or rather some some theory does make those assumptions but it's an dangerous assumption to make because occasionally the network delay does become much higher than than what is typical. Another thing is about crashes. For example, the distributed system theory just says like nodes can crash but what does that actually mean? Like what in practice does it mean for a node to become unavailable because it might be a software crash but yes it might be a hardware failure. It might be somebody unplugging the power cable. It might be that the node is actually still running but it's just become disconnected from the network. The point of this book chapter really is to defend and justify those theoretical models that we use for analyzing distributed systems and just giving a lot of stories and case studies that show that you know actually tons of stuff does go wrong and like don't believe anyone who says oh failures are rare it's don't don't worry about it it's fine. The the the moral of this chapter is really that actually know if you want to make things reliable, you really do have to worry about a whole bunch of weird unusual but but certainly possible edge cases. Timing is another one of those things like you know it's very easy to assume that your clocks are correct and most of the times the clocks are pretty correct but we just can't rely on it because actually they're just not precise enough on the whole and so a lot of it is about it's very tempting to make certain assumptions that things are well behaved and and in distributed systems we just have to try to get away from those assumptions if we want the systems to work reliably even in the face of things going wrong but it was a really fun chapter to Right? Because you know it's it's essentially a big collection of stuff that has gone wrong. And so I went through a bunch of postmortems published by various tech companies for example in order to see okay what was the root cause of how things went wrong and what kind of lessons can we draw from this that apply to the the book in general. And you know there's some fun stuff like the the sharks biting undersea cables and damaging them that just you know makes for a great story. And then I I hear that in recent years the shielding of undersea cables has got better and therefore the sharks are not biting them anymore. But instead the cows on land are stepping on cables and occasionally causing network interruptions that way. And you know that sort of thing is just it makes it a bit more fun.
</details>

**主持人**: 那一章也很有趣，因为根据你所从事的团队或与你交谈的人，当我与 **S3** 团队交谈时，对他们来说，那一整章就是他们的日常。当硬盘出现问题，或者数据中心发生火灾，对他们来说，这并不是什么奇怪的事情，他们已经为所有这些事情做好了准备。他们处于这样的规模，这些事情会定期发生，因为他们是最大规模的团队之一。而在一家较小的公司，即使你读了这一章，你也会认为“这可能会发生”，但当它实际发生时，那将是十年一遇的大事。

<details>
<summary>Original English</summary>
**主持人**: That chapter is so interesting also because when depending on what kind of teams you work on or what kind of people you talk with when I talk with the **S3** team for them that whole chapter is just their day-to-day. It's it's they they don't it's not a weird thing when you know like a a hard drive goes up or or there might be okay it might be a weird thing to have a fire in a data center but they're prepared for all of those things. They're at the scale where these things just happen on a regular cadence because they're one of the the largest scales whereas at a smaller company even if you read this chapter and you know you will treat this as like well this could happen but when it h when it actually happens it will be a once in 10 year and it will be a big deal.
</details>

**Martin Kleppmann**: 是的。但我认为没有一个“正确”的答案。广义上讲，这是风险和成本之间的权衡。这意味着必须做出商业决策，决定公司希望在这个权衡中处于何种位置。所以这一章的目标实际上只是为了给人们提供信息，以便他们做出明智的决策。但我不想替人们做这个决定。这需要企业自己决定。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. But I think there's there's no like right answer. It's a it's a trade-off between risk and cost broadly speaking. And that's means a business decision has to be made in terms of where the business wants to lie on that trade-off. And so the goal of this chapter is really just to give people the information in order to make an educated decision. But I don't want to make that decision for people. That's for businesses themselves to decide.
</details>

**主持人**: 那说得很清楚。你有没有遇到过书中提到的某些概念或 **SIP**（服务改进提案），在第一版和现在的第二版中，它们变得更受欢迎或更不受欢迎，或者被读者引用得更多或更少，比如流处理系统、批处理或其他任何东西？

<details>
<summary>Original English</summary>
**主持人**: That's very clear. Have you come across some concepts or **SIP**s as mentioned in the book in the first edition and now in the second edition that are becoming either more popular or less popular over time more or less referenced by your readers thinking about from things like streaming systems, batch processing or or anything else?
</details>

**Martin Kleppmann**: 是的。所以与第一版相比，我们能够从书中删除一些内容，特别是关于 **MapReduce** 的详细介绍，在第一版中相当详细，但基本上 **MapReduce** 已死，现在没人用了。它的继任者，比如 **Spark** 和 **Flink**，它们仍在被使用，所以我们在第二版中仍然引用 **MapReduce**，但更多是作为一种学习工具，以便理解这类分区、分片的批处理系统是如何工作的。所以这是我们能够减少覆盖的一个方面。但是我们增加覆盖的其他领域，例如，是支持 **AI** 的系统。所以，尽管这不是一本 **AI** 书籍，但在需要支持 **AI** 应用程序时，仍然会出现数据系统方面的问题，比如一个经典的例子是向量索引。所以，我们在存储引擎那一章中增加了一些关于向量索引的内容。它在那里非常契合，因为它已经涵盖了各种不同的索引策略。所以向量索引，你知道，它只是另一种索引策略。我们还增加了一些关于数据帧（**data frames**）的内容，例如。这并非完全是 **AI** 相关的东西，但数据帧是一种非常好的数据表示形式，例如用于训练数据。这在第一版中不是我们讨论的数据模型之一，但我们决定将其添加到第二版中，因为它实际上已经成为一个非常重要的数据模型，人们正在与所有经典数据模型（如关系型、图、**JSON** 文档等）一起使用。所以这些地方我们只是稍微扩展了覆盖范围，以反映人们正在构建的系统类型，例如支持 **AI**，而没有完全改变这本书的方向。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. So the some things that we've been able to take out out of the book compared to the first edition in particular for example coverage of **MapReduce** was quite detailed in the first edition but basically **MapReduce** is dead nobody uses it anymore. It's successors like in the form of **Spark** and **Flink** for example they are used and so we still reference **MapReduce** in the second edition but more as a learning tool in order to understand how these kind of partition sharded batch processing systems work. So that's one thing where we've been able to reduce the coverage. But other areas where we've increased the coverage are, for example, systems in support of **AI**. And so, even though this is not an **AI** book, but there are still data systems concerns that arise when needing to support **AI** applications, like a classic one is vector indexes, for example. And so, we've added some coverage of vector indexes to the storage engine chapter. Fit in really well there because it already covers various different indexing strategies anyway. And so vector indexes, you know, it's just another indexing strategy. We also added some coverage of data frames, for example. That's not an exclusively **AI** thing. But data frames are quite a good data representation for training data, for example. And that was not one of the data models that we discussed in the first edition, but we decided to add to the second edition because it has actually become a very important data model that people are using alongside all of the classic data models like relational and graph and **JSON** documents and so on. And so there these these places where we've just expanded the coverage a bit to to reflect the kinds of systems people are building for example to support **AI** without it like changing the direction of the book entirely.
</details>

### 工程师的责任与伦理

**主持人**: 第一版中的最后一个小节，前几个小部分标题是“做正确的事”，在第二版中，这成了一个独立的章节。最后一章是“做正确的事”，我引用了其中的一小段话：“我们这些构建这些系统的工程师有责任仔细考虑这些后果，并有意识地决定我们想生活在什么样的世界里。”我们能稍微谈谈这一节的重要性吗？

<details>
<summary>Original English</summary>
**主持人**: The final subsection in this first edition the first few I guess like sub parts were titled doing the right thing and in the second edition this has its own chapter. The final chapter is doing the right thing and I I quote a little bit from it. We the engineers building these systems have a responsibility to carefully consider those consequences and consciously decide what kind of world we want to live in. Can we talk a little bit about this section and the importance of it?
</details>

**Martin Kleppmann**: 绝对是。是的。所以，在第一版中加入伦理章节的动机是，我只是觉得在我从事工业界期间，它作为一个问题被相当忽视了。尤其是在初创公司，人们非常专注于构建客户会喜欢的产品，而在过程中真正地将这些伦理问题降级。所以，例如，对于面向消费者的产品，产品可能非常倾向于数据收集，收集行为数据，因为这可以通过广告形式变现，而对于这些事情的好坏似乎很少有反思。所以我真的只是想鼓励大家多思考一下。并不是真的想规定一种特定的方法，但至少要指出，现在有数据保护立法，我们确实需要在数据系统架构中考虑这些，并且存在伦理责任。你知道，人们说你进入科技行业是为了改变世界。如果你想改变世界，那么思考你的技术对世界的影响就是你工作的一部分。这确实是一个非常重要的部分，而工程师们常常容易忽视这一点，因为我们只关注技术，而较少关注技术在现实世界中会产生的影响。所以这一章实际上只是一个尝试，让人们对此多思考一点。它也是我自身过程的一种反映，因为当我开始从事这些系统时，我也没有特别思考伦理问题。所以我感觉我必须把那一节放在那里，既是为了我自己，也是为了读者，因为那是我自己处理这些问题的一种方式。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Absolutely. Yeah. So the motivation for putting in an ethics section there in in the first edition was that I just felt it had been quite ignored as a concern during my time in industry. That like especially in startups people were very focused on like building a product that their customers would love and really like deprioritizing these sort of ethical questions in the in the process. And so for example with the consumer-facing products it might be that the products are very much geared towards essentially data harvesting collecting behavioral data because that's what can be monetized in the form of advertising and there seemed to be just very little reflection on what was good and bad about these sort of things. So I really just wanted to encourage a bit of thinking there. Not really wanting to prescribe too much like a a particular approach there but at least to point out you know there there is this thing such as data protection legislation now which we do have to think about in the architecture of our data systems and there is an ethical responsibility. You know people say that you get into tech in order to change the world. If you want to change the world, then thinking about the impact that your technologies have on the world is part of your job. It's it's a really essential part really and something that engineers are often prone to ignoring as we focus just on the technology and less on the effects that that technology will have out in the real world. And so this chapter is really just an attempt to get people thinking about it a bit. And it's sort of a a reflection of my own process as well because as I started working on these systems, I didn't really think about ethical things particularly either. So I felt like I had to put that section in there for myself as well as for the readers because it was my own way of of grappling with these questions a bit.
</details>

**主持人**: 这样说公平吗：作为构建这些系统、可能对广泛事物产生潜在社会影响的工程师，我们正处于一个能够直接影响甚至改变方向的有利位置。所以，我是否理解这一部分是在提醒我们，通过构建这些系统，我们有巨大的机会来塑造它们，我们可能拥有比几年后监管机构更强大的发言权？

<details>
<summary>Original English</summary>
**主持人**: Is it fair to say that as engineers building these systems that will have an impact on on a wide range of things potentially societal wide impact we are just in such a good position to directly influence and maybe even change course. So do I understand that this section is a bit of reminder that by building it we have a huge opportunity to shape these we probably have a lot stronger voices maybe as strong voices as later on the regulator might have years down the road.
</details>

**Martin Kleppmann**: 没错。我认为工程师在这方面有非常强大的发言权，就像我们之前谈到的，工程师需要以一种方式阐明权衡取舍，以便商业领袖能够就如何处理这些权衡做出明智的决策。而这些权衡的一部分是指出风险。风险不仅包括技术风险，比如数据可能损坏，还包括社会风险。例如，这种技术可能产生哪些负面影响，可能造成哪些危害，可能产生哪些意想不到的后果，或者如果一种技术被发现具有有害影响，可能对公司声誉造成哪些损害。你知道，这会给制造它的公司带来负面影响，这必须成为权衡讨论的一部分，我只是希望人们能有意识地、深思熟虑地做出这类决定，而不是仅仅将其扫到地毯下面。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Exactly. I think engineers have a very strong voice there and like we talked about earlier engineers need to articulate trade-offs in such a way that business leaders can then make educated decisions about how to address those trade-offs. And part of those trade-offs is pointing out risks. And risks include not just technical risks like the data might get corrupted, but they include societal risks as well. For example, like what negative effects, what harms might arise from this technology, what sort of unintended consequences possibly or what like risk for reputational damage if it turns out that a technology has some harmful effects. You know that can reflect badly on the company that made it and that has to be part of the the trade-off discussion and I just want people to make intentional and deliberate decisions about this kind of things and not just sweep it under the carpet.
</details>

### 形式化验证与AI

**主持人**: 当前热门话题之一当然是 **AI**，你去年 12 月就此写了一篇非常有趣的文章，关于形式化验证以及你坚信形式化验证在 **AI** 领域可能会变得更重要。对于那些听说过形式化验证的用户，我们能谈谈它是什么，以及你如何设想它会变得更重要吗？

<details>
<summary>Original English</summary>
**主持人**: One of the hot topics these days is of course **AI** and you've written a very interesting post about this just in December about formal verification and how your conviction that formal verification might be more important with **AI**. Can we talk for for those of users who have heard formal verification, can we talk about what this is and how you envision this becoming more important?
</details>

**Martin Kleppmann**: 是的。所以形式化方法有很多种。一种方法是，例如，使用像 **TLA+** 或 **FSBY** 这样的规范语言，在高层次上描述系统的预期行为，然后使用模型检查器（本质上是一个随机测试用例生成器）来模拟大量场景，看看系统在所有不同场景中是否具有这些期望的行为。这可以说是入门级的形式化验证。更高级的层次是使用实际的形式化证明，在这种情况下，你可以用形式化语言（通常使用数学符号）编写某个系统的规范，然后进行数学证明，证明某个算法或某个实现总是满足该规范。与测试的区别在于，测试你只是尝试几个例子，给算法一些示例输入，并检查在这些特定例子中是否得到了预期的输出。但证明可以推理潜在的无限状态空间。所以它可以告诉你关于整个宇宙中可能发生的每一种情况，例如，证明某个安全属性总是成立的。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. So there's a whole range of formal methods. Um, one approach is to for example use a specification language like **FSBY** or **TLA+** or something like that to describe the expected behavior of a system at a at a high level and then use a model checker which is essentially like a randomized test case generator to just play through a lot of scenarios and see whether the the system has those desired behaviors in in all the different scenarios. That's like the sort of intro level formal verification. I would say the more advanced level is to use actual formal proof and in that case you can write a specification of some system in a formal language is usually using mathematical notation and then make a mathematical proof that a certain algorithm or certain implementation always satisfies that specification. And the distinction to testing there is that well in testing you just try through a couple of examples, give the algorithm some example inputs and check whether you get the expected output in those particular examples. But a proof can reason about potentially infinite state spaces. So it can tell you things about like every possible thing that could possibly happen in the entire universe show that for example a certain safety property is is always given in those.
</details>

**Martin Kleppmann**: 形式化验证是一项大量的工作。我从事工业界的时候从未用过它，因为它基本上太耗时了。我是在进入学术界后才开始接触形式化验证的，那时我才能负担得起花费几个月的时间来证明一个算法的正确性。但在那里，我开始发现它非常有用，特别是当我处理非常精妙的算法时，仅仅通过阅读实现很难判断它在所有可能情况下是否总是正确的。但是，如果它是一个重要的算法，例如，如果其中有错误会导致数据损坏，或者有安全漏洞，那么当涉及到高风险的事情时，我认为进行形式化验证是值得的，以确保代码确实是正确的。所以我做了一些形式化证明，例如使用 **Isabelle** 证明助手，还有其他一些，比如 **Coq** 和 **Lean** 等。这些证明真的很难写。学习编写这些证明的语言需要很长时间。然后即使你懂了这种语言，实际编写单个证明步骤仍然非常费力。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Formal verification is is a lot of work. I never used it in my time in industry because it's just too too time-consuming basically. I only got into formal verification when I was in academia and I could afford to take the time to spend a few months proving an algorithm correct. But there I've started finding this very useful especially if I was working on very subtle algorithms where it's very hard to tell just from reading the implementation whether this actually is always correct under all possible cases. But if it's an important algorithm where for example it will corrupt data if there's a mistake in it or it will have a security vulnerability if there's a mistake in it then when it's high stakes things like that then I feel it's worthwhile to have formal verification and to really make sure that the the code really is correct and so I've done some formal proofs using the **Isabelle** proof assistant for example there are a couple of others as well like **Coq** and **Lean** and so on. These proofs are really hard to write. It's it takes a long time to learn the language of writing those proofs. And then even once you know the language, it's just really laborious in order to actually write the individual proof steps.
</details>

**主持人**: 当你说它很难写时，作为一个懂很多不同编程语言的人，你能解释一下它为什么难写吗？它感觉像是一种严格的编程语言，有很多规则，还是有很多数学公式？是什么让你觉得学习它并擅长它很难？

<details>
<summary>Original English</summary>
**主持人**: And when you say it's hard to write, just as someone I I know how to code, you know, all so many different different languages. Can you just explain what what it means to hard to write? Is is it does it feel like a a strict programming language with all sorts of rules or lots of math formulas? What what makes it hard for for you to to learn it and and get good at it?
</details>

**Martin Kleppmann**: 是的。你正在尝试证明一段特定的代码总是满足某个特定的属性。在某些情况下，这个属性可能很容易指定。举一个非常简单的例子，你有两个列表，你想把它们连接起来。然后你想证明连接后的列表的长度等于两个单独列表的长度之和。你知道，这是一个非常非常简单的属性。你如何证明这样的事情？嗯，你会有一个连接两个列表的函数，然后你可能会对其中一个列表进行归纳证明，表明，好吧，如果你有一个长度为 i 的列表和另一个长度为零的列表，那么两者的和就是 i。如果你有一个长度为 i 的列表后面跟着一个长度为一的列表，那么就是 i + 1，依此类推。然后通过归纳证明，你可以证明连接后的列表的长度是 i + j，其中 i 和 j 是两个输入列表的长度，适用于 i 和 j 的每个可能值。而这在测试用例中，你可能会测试 j 等于 0、j 等于 1 和 j 等于 5 的情况。然后你就完成了。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. So, you're trying to make a proof that a certain piece of code always satisfies a certain property. In some cases, that property might be quite easy to to specify. Let's say as a really simple example, you have two lists and you want to concatenate them. And then you want to prove that the length of the concatenated list equals the sum of the two individual lists. You know, very very simple property. How would you prove something like this? Well, you would have a function that concatenates two lists and then you would probably do a proof by induction over one of the lists that shows that okay, well, if you have one list of length I and another list of length zero, well then the sum of the two is I. If you have a list of length I appended with a list of length one, well then it's I + one and so on. And then by using a proof by induction, you can then show that the length of the concatenated list is I + J where I and J are the lengths of two the two input lists for every possible value of I and J. And this is something that you know in a test case you would in tests you would maybe test it for the cases of J equals 0, J equals 1 and J equals 5. And then you're done.
</details>

**主持人**: J 等于最大整数。是的，边缘情况。我们就是这样做的。我就是这样写单元测试的。

<details>
<summary>Original English</summary>
**主持人**: Nj equals inter max. Yes, the edge case. That's what we do. That that's how I write my unit test.
</details>

**Martin Kleppmann**: 没错。所以这是一个微不足道的例子，比如列表连接。你可以很容易地阅读代码并说服自己它是正确的。但如果它是一个复杂得多的算法，那么我们的大脑就无法很好地理解这个算法，以至于如果你不证明它，就无法真正说服自己它是正确的。这就是这些证明变得方便的地方。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Exactly. And so this is a trivial example like list concatenation. You can easily just read the code and convince yourself that it's correct. But if it's a much more complex algorithm, then you our brains just can't like grock the algorithm well enough to really convince ourselves that it's correct if you don't prove it. And that's where these these proofs then become handy.
</details>

**主持人**: 如果我是一名工程师，并且我对开始使用形式化验证感兴趣，例如，因为我有一种观念，认为它在 **AI** 领域会变得更重要，当然，编写这些东西会更容易。你会建议工程师从哪里开始，或者你是如何进入这个领域的？

<details>
<summary>Original English</summary>
**主持人**: If I'm I'm an engineer and I would I would be interested in getting started with formal verification for example because I have the notion that it will be more important with **AI** of course it will be easier to to write these things. Where would you point engineers to to get started or how did you get started in this field?
</details>

**Martin Kleppmann**: 我会建议从模型检查开始。所以像 **TLA+** 或 **FSBY** 这样的工具比像 **Isabelle**、**Coq** 和 **Lean** 这样的证明助手更容易上手。这些证明助手需要大量的额外知识，而且老实说，学习编写这些形式化证明的资源并不是特别好。我也没有找到真正很棒的书籍。我学习它的方式是和实验室里的一些同事一起工作，他们通过多年的经验学会了它，我只是和他们坐在一起，在办公桌前结对编程，我描述我想要证明的东西，他们一步一步地向我展示如何证明，如何分解它。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: I would suggest starting with model checking. So something like **TLA+** or **FSBY** are much friendlier to getting started with compared to proof assistants like **Isabelle**, **Coq** and **Lean**. That these proof assistants just require a whole lot of additional know knowledge and the resources for learning about writing these formal proofs are to be honest not particularly good. I haven't really found really great books on it as well. The way I learned it was by working with some colleagues in my lab who who had learned it through years of prior experience and I just sat down with them and paired with them at a desk where like I described the thing I was trying to prove and they showed me how to prove it step by step how to break it down.
</details>

**主持人**: 我很想知道你的想法是否正确，那就是这件事会变得更主流，希望我们也会有更好的书籍和资源。

<details>
<summary>Original English</summary>
**主持人**: I'm interested to see if if what if you're thinking will be correct which is this thing will go more mainstream and hopefully we'll have better books and resources for it as well.
</details>

**Martin Kleppmann**: 是的，我确实希望如此。所以，我认为形式化验证未来会变得更重要的原因有几个方面。一个原因是，大型语言模型（**LLM**）在编写这些证明方面越来越出色，如果我们不必手动编写证明，那么在以前不经济的情况下，现在就可以进行证明了。但同时，**LLM** 也增加了对这些形式化证明的需求，因为我们正在大量编写代码。如果我们必须手动审查所有这些代码，那么这将成为瓶颈。所以，如果我们真的想获得 **AI** 的好处，我们也无法让人类审查所有生成的代码。所以我们需要某种自动化方式来检查代码是否正确。编写大量测试是一个非常好的起点。但证明可以做到测试无法做到的事情，那就是考虑所有可能发生的事情。这在安全领域尤其重要，例如，一个小小的错误就可能造成一个漏洞，从而破坏整个系统的安全性。所以我认为在那些我们真正希望完全没有 bug 的领域，形式化验证可以真正发挥作用。我希望 **LLM** 实际上能让那些以前认为形式化验证太难太贵而没有考虑使用它的人更容易接触到它。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes, I do hope so. So the the reason I think that formal verification could become more important in the future is kind of several aspects to it. One is that the **LLM**s are getting increasingly good at writing these proofs and if we don't have to write the proofs by hand as humans, it just becomes feasible to do them in situations where previously it would have not been economical. But also, **LLM** increase the need for these formal proofs because, you know, we're vibe coding a bunch of stuff. If we have to manually review all of that code, then that will become the bottleneck. So, we can't really have humans reviewing all of the generated code either if we really want to get the the benefits of of **AI**. So, we need some automated way of checking whether the code is correct. And writing lots of tests is a very good starting point. But the thing that proof can do that tests can't is to consider absolutely every possible thing that could happen. And that's really important in a security context for example where it just takes one little bug want to create a vulnerability that destroys the security of the whole system. And so I feel for those domains where like really we want to ensure there's a complete absence of bugs that's the kind of places where formal verification can really shine. And I'm hoping that **LLM**s will actually make that a lot more accessible to to people who would have previously not considered using formal verification because it was just too hard and too expensive.
</details>

### 工业界与学术界

**主持人**: 你曾在工业界工作，然后进入学术界。你能告诉我们两者之间的区别吗？我自己和大多数观看者都在你所说的工业界工作，在科技行业或不同的公司工作。我们正在自力更生或只是在做我们自己的事情。学术界与此有何不同？你和你的同事在学术界都做些什么？

<details>
<summary>Original English</summary>
**主持人**: You've worked in the industry and then you went into academia. Can you tell us what the difference is between us? Myself and and most people watching work in what you would call industry and the tech industry or work at different companies. We're bootstrapping our own or we're just doing build building our things. How does academia contrast to to this? What what do you and your colleagues do inside of academia?
</details>

**Martin Kleppmann**: 是的，在学术界，有很多不同的风格。没有一概而论。有些人完全专注于理论、数学，完全不关心现实世界，只想研究那些在智力上有趣的事情。这很好。有些人则非常倾向于应用端，希望进行可能对现实世界产生影响的研究。我更偏向应用端。这也没问题。但一个常见的区别是，学术界可以思考更长远的问题。所以，你知道，如果你在创业，你必须在几个月内推出一些东西。你无法负担得起思考未来十年。嗯，也许你会有某种长期的愿景，你正在逐步实现，但你确实必须在相当短的时间尺度内推出产品。在一家大公司，也许如果你从事基础设施方面的工作，你可以思考更长远一些，因为所需的需求可能更容易理解。在这种情况下，你知道，他们确保系统是可伸缩的、操作上健壮的等等。那么需求就相当清楚了，仍然是实现的问题，但在这种情况下，你可以思考更长远一些。但在学术界，我真正欣赏的是工作的自由，可以从事那些长期性的、不立即具有商业可行性或与商业公司的激励不一致的事情。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, within academia, there are lots of different styles really. There's not not one thing. Some people go full-on theoretical, mathematical, don't care about the real world at all, just want to work on things that are intellectually interesting. And that's fine. And some people are at the very much at the applied end of wanting to do research that is likely to have a real world impact. I'm more on the applied end. And that's fine too. But a common distinction there is that academia can just think much longer term. So the you know if you're doing a startup you have to ship something within a few months. You can't afford to think 10 years into the future. Well, maybe you'll have sort of a a sort of long-term vision that you're gradually getting towards, but you do have to really ship things on a fairly short time scale. At a bigger company, maybe if you're working on infrastructure or so, you can think on a bit of a longer time scale because the the requirements of what are needed is are perhaps better understood. And in that case, you know, they're making sure that the system is like scalable, operationally robust, and so on. It's then fairly clear what the requirements are and it's still a matter of implementing it but in that case you can think a bit longer term but in academia what I really appreciate is the freedom to work on things that are long-term and which are not like immediately commercially viable or which are not aligned with the incentives of commercial companies.
</details>

**Martin Kleppmann**: 我多年来一直从事的一个研究领域是我们称之为“本地优先软件”的东西，其理念是，我们希望从云运营商手中夺回一些权力，并将其归还给最终用户。所以最终用户应该更多地控制自己的数据，更少地依赖云服务来提供用户所需的应用程序和数据。而这并不是公司自然而然会做的事情，对吧？因为软件即服务（**SaaS**）企业，例如，他们能够收取订阅费的全部原因是因为他们能够基本上对客户施压，说：“支付你的订阅费，否则我们将删除你的所有数据。”我完全理解导致这种情况的商业必要性，但它也导致了这样一种情况，即人们一直处于被威胁的状态。在我看来，这不是一个健康的情况。但是，如果你从事的业务收入依赖于这种锁定情况的持续存在，那么以这种方式改变它，从客户头上拿走那把枪是困难的。而在学术界，我觉得我有自由去研究那些与公司商业激励相悖的事情，并说：“不，我将做我认为对用户正确的事情，我将把软件公司的商业模式放在次要位置。”我之所以能这样做，是因为我不依赖这种商业模式。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: One of research area that I've been on for several years now is what we call local first software which is this idea that we want to take away a bit of the power from cloud operators and give it back to end users. So end users should be more in control of their own data and less dependent on cloud services for providing the applications and the data that that the users need. And that's something that doesn't naturally come to companies, right? Because software as a service businesses, for example, the whole reason why they can charge a subscription is because they are able to essentially hold a gun to the customer's head and say, "Pay us your subscription, otherwise we will delete all your data." And I totally understand the the commercial imperatives that lead to that, but it also leads to this situation where like the people have a gun against their head all of the time. That isn't really a healthy situation to be in in my opinion. But changing that in such a way to take away that gun from customers heads is difficult if you're in a business whose revenue depends on perpetuating that kind of lock-in situation. And there I feel like in academia I have the freedom to work on things that go against this commercial incentive of companies and say like actually no I'm going to do what I think is right for the users and that I'm going to say the commercial model of the companies making the software is second priority and I can afford to do that because I'm I'm not dependent on this commercial model.
</details>

**主持人**: 除此之外，这还涉及非常有趣且具有挑战性的工程问题。

<details>
<summary>Original English</summary>
**主持人**: To add to this, it's very interesting and challenging engineering problems.
</details>

**Martin Kleppmann**: 是的。能够从事有趣的工程和计算机科学问题，同时又努力追求本地优先软件的更高层次愿景，这真是太棒了。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes. And it's wonderful to get to work on interesting engineering and computer science problems while at the same time like trying to pursue this this higher level vision for local first for first software.
</details>

**主持人**: 那么，为了实现更可行的本地优先软件，我们需要解决哪些真正有趣的工程挑战呢？比如，笔记应用就是一个非常受欢迎的例子，对吧？

<details>
<summary>Original English</summary>
**主持人**: What are some of these really interesting engineering challenges that we we will need to solve or or we need to solve to get to a more viable local first software? May that be like let's say note-taking. It's a very popular one, right?
</details>

**Martin Kleppmann**: 是的。所以，在我们本地优先软件的愿景中，我们试图摆脱对中心化云服务的依赖。可能仍然会有云服务参与手机和笔记本电脑之间的数据同步，因为通常通过云服务是建立这种通信最便捷的方式。但我们只是不想必须信任某个云服务提供特定功能。那么，如果你能摆脱对这个单一云服务的假设，你就可以，例如，拥有多个云服务，在多个云提供商之间并行运行，你只需通过任何一个最先响应的服务进行同步，或者与所有服务同步，然后如果其中一个消失了，也没问题，因为你还有其他的。所以，如果我们摆脱对中心化云服务的假设，它会给我们带来巨大的自由和灵活性。但这带来了一系列有趣的研发和工程挑战，因为，例如，我们最近一直在研究的一个问题是访问控制。你知道，一个简单的问题是，你有一个文档，你希望能够授予协作者访问权限，并且能够撤销该权限。这听起来完全显而易见，应该非常简单。在中心化云服务模型中，它确实非常简单，因为。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. So with our vision of local first software, we're trying to get away from this dependency on centralized cloud services. There may still be cloud services involved in syncing data between your phone and your laptop say um because often going via cloud service is just the most convenient way of establishing that kind of communication. But we just don't want to have to trust on a cloud service providing a particular function. Then if you can get away from assuming this one cloud service, you could for example have multiple cloud services on multiple cloud providers side by side and you just sync by whichever happens to respond first or sync with all of them and then if one of them disappears, no problem because you've got the other one. And so it gives us a huge amount of freedom and flexibility if we get away from this assumption of centralized cloud services. But that introduces a whole bunch of interesting research and engineering challenges because so one thing that we've been working on lately say is access control. You know simple problem you have a document you want to be able to grant collaborators access and you want to be able to revoke that access. Again totally obvious to should be totally straightforward. In a centralized cloud service model it is totally straightforward because.
</details>

**主持人**: 你有规则，你确认那些事情，你检查正确的角色，就这样。

<details>
<summary>Original English</summary>
**主持人**: You have the rules you you you confirm that those sort of things and you check for the right roles and that's it.
</details>

**Martin Kleppmann**: 是的。但是如果你想在多个提供商上运行你的系统，甚至在点对点设置中，那么可能会发生的情况是，一个用户的编辑权限被撤销了，同时该用户对刚刚更改了权限的文档进行了编辑，现在有些设备可能会先看到对文档的编辑，然后才看到撤销，所以它们会接受对文档的编辑，而另一个设备可能会看到相反的情况。它们可能会先看到撤销，然后才看到对文档的编辑，它们会因为认为没有授权而放弃对文档的编辑。现在这些设备之间就变得永久不一致了。所以这意味着，如果我们真的想确保一致性，即使对于这种相当基本的设置，我们现在也必须想办法解决这种编辑与撤销同时发生的情况，即用户进行了编辑，但其权限被撤销了。解决这个问题意味着，在去中心化设置中，我们没有一个单一的服务器可以做出这个决定。在中心化设置中，你知道，你只有一个服务器，它决定是对文档的编辑先发生还是撤销先发生，那个服务器做出决定。但如果你有多个服务器，它们可能会做出不同的决定，那么你就可以有一个共识协议，但共识很麻烦，因为它需要一些法定票数，并且需要节点在线。所以我们一直在尝试在不进行共识的情况下完成所有事情。但是，在保持高可用性的同时，在保持用户离线工作的能力的同时，在保持无需任何服务器即可点对点同步的能力的同时，例如，这使得工程挑战变得更加困难，而且它是可以解决的，我们正在接近解决它，对于我正在开发的 **CRDT** 库 **Automerge** 来说。但是，它比中心化情况要复杂得多。但这正是从摆脱中心化服务的愿望中产生有趣工程挑战的一个很好的例子。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah. But if you want to run your system over multiple providers or even in a peer-to-peer setting then well what could happen is that a user gets their edit permissions revoked and concurrently that user makes an edit to the document whose permissions have just changed and now some devices may see the edit to the document first and the revocation second and so they would accept the edit to the document and another device may see it the other way around. They may see the revocation first and then the edit to the document second and they'll drop the edit to the document because they think it's not authorized. And now those devices have become inconsistent with each other permanently inconsistent. So that means if we actually want to ensure consistency even for this fairly basic setup we now have to somehow figure out how to resolve this situation of an edit that is concurrent with the revocation of the user who made that edit. Solving that problem then mean in in a decentralized setting where we don't have just a single server that can make that decision in a centralized setting you know you just have one server it decides did the edit to the document come first or did the revocation come first and that one decide server makes that decision but if you have multiple servers they might make different decisions so then you could have a consensus protocol but then consensus is messy because it requires like some quorum votes and requires nodes to be online and so we've been trying to do the whole thing without doing consensus. But but while um so while preserving high availability, while preserving the ability for user to work offline, preserving the ability to synchronize peer-to-peer without any servers, for example, that just makes the engineering challenge a lot harder and it's solvable and we are close to solving it for **Automerge**, which is the the **CRDT** library that that I work on. But it's it's just much less straightforward than it is in the in the centralized case. But that's a nice example of where interesting engineering challenges arise from this desire to get away from centralized services.
</details>

**主持人**: 我们刚才还在谈论时钟。但一个显而易见的想法是，如果所有设备的时钟都精确到微秒级同步，你就可以直接使用时钟，使用时间戳。但正如你在分布式系统中提到的，我们不能总是相信时钟是同步的。所以我猜你只是有很多你一直在研究和撰写的东西都回到了这个点。

<details>
<summary>Original English</summary>
**主持人**: And then we were just talking about clocks earlier. But an obvious thing that came to mind is well if if all of them had the same clock exactly to the microsecond, you could just use a clock, you could use a time stamp, but as you said in distributed systems, we cannot always trust the the clocks are always synchronized. So I I assume like you just have these a lot of the things that you have been researching and writing about are just coming back to.
</details>

**Martin Kleppmann**: 绝对是。在这种特定情况下，比如用户权限被撤销，如果一个被撤销权限的用户仍然想破坏文档，他们可以回溯编辑时间，给它一个更早的时间戳。所以在这里依赖时钟是绝对没用的，因为人们可以伪造这些时钟的时间戳，从而可能破坏访问控制机制。所以在这种系统中，我们必须担心潜在的恶意生成行为，当这些行为来自最终用户设备时。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Absolutely. And in this particular setting of like a user getting their edit permissions revoked if a revoked user still wants to say vandalize a document they can just backdate their edit give it an earlier time stamp. So relying on clocks is absolutely useless here because people can forge the time stamps from those clocks and thereby then potentially undermine the access control mechanism. So in this kind of system, we have to worry about potentially maliciously generated actions as well when the actions come from end user devices.
</details>

**主持人**: 这太引人入胜了，因为在我看来，你正在解决一个比一些初创公司更难，甚至可能更难的工程挑战，因为初创公司会走简单的路线。他们会接受一个限制，在这种情况下是一个中心化服务器，这在商业上是合理的，在收入上也是合理的。但因为你没有这样做，你现在需要为更难的问题寻找解决方案。如果你解决了这个更难的问题，你就可以提供一个构建模块，从而推动行业向前发展。只是为企业、个人或机构提供一个选择，不仅仅是使用中心化，而是使用这种去中心化、本地优先的方法，然后当然要权衡利弊并决定哪种更有意义。

<details>
<summary>Original English</summary>
**主持人**: This is fascinating because it feels to me that you're solving a hard or maybe even harder engineering challenge than some startups would do because the startups would go the easy route. They would take on a constraint in this case a centralized server which makes business sense, makes revenue sense. But because you are not doing this, you now need to look for a solution for a harder problem. And if you solve this harder problem, you can give a building block that can just move the industry forward. Just give a an option for either a business or an individual or an institution to you know like have an option not just to use centralized but use this decentralized local first approach and then of course reason about the trade-off and decide whichever makes sense.
</details>

**Martin Kleppmann**: 没错。这就是我所说的长期思考。这是一个例子，因为是研究，我们可以采取这种理想主义的、有原则的立场。我说，是的，我们将解决这个更难的工程问题，因为我们认为去中心化是一个有价值的特性，我们非常清楚大多数初创公司不会解决这个问题，因为他们只会做简单务实的事情，这对于初创公司来说是正确的做法。但是我们有不同的激励机制，我们有能力投入时间去尝试解决这些难题。正如你所说，如果我们能够解决它们，那么它就会为任何人，任何这项技术的使用者创造更多的选择性，如果他们愿意，他们可以选择使用这种去中心化技术。而且仍然存在权衡，但至少如果他们不必从头开始发明它，那么采用这种去中心化技术对那些想要使用它的人来说会容易得多。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Exactly. And that's what I mean with this long-term thinking. This is an example of it where because it's research we can afford to take this idealistic principled stance. I said yes we're going to solve this harder engineering problem because we think decentralization is a valuable feature and we know perfectly well that most startups are not going to solve this problem because they will just do the easy pragmatic thing which is the right thing for startups to do. But we have a different set of incentives and we can afford to put in the time to try and solve those hard problems. And as you said, if we can solve them, then it creates more optionality for anyone, any users of this technology, they can if they want to choose to use this decentralized tech. And there's still trade-offs around it, but at least if they're not having to invent it from scratch, it'll be a lot easier to adopt this kind of decentralized tech for for those who want to use it.
</details>

### 学术教学与计算机科学教育

**主持人**: 那么在学术界，你也在教学。你教哪些课程？

<details>
<summary>Original English</summary>
**主持人**: So in inside academia you're also teaching. What courses do you teach?
</details>

**Martin Kleppmann**: 目前，我为本科生开设一门并发和分布式系统课程，为硕士生开设一门密码协议工程课程。此外，今年我还开设了一门安全研讨课，并且还教授本科生操作系统课程。我今年的教学任务相当重。分布式系统课程在 **YouTube** 上有。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: At the moment I have a concurrent and distributed systems course for the undergraduates and a cryptographic protocol engineering course for the master students. And then additionally this year I have a a seminar course on security and a and teaching also the undergraduate operating systems course. I've got quite a lot of teaching this year. The distributed systems course, it's available on on **YouTube**.
</details>

**主持人**: 你能总结一下，那些学习这门课程的人（这门课程是免费提供的，感谢你和大学的开放）会学到什么？

<details>
<summary>Original English</summary>
**主持人**: Can you summarize what people who would go through this course which again is freely available? Thank you for you and the university for making it available. What what what would they learn throughout those courses?
</details>

**Martin Kleppmann**: 是的。那门分布式系统课程比书中的内容更偏理论化。它更侧重于算法，以及我们如何确信算法在分布式系统假设下（我们谈到的，比如节点可能崩溃、通信可能不可靠、时钟可能不准确等）能正确运行。所以这确实是它的重点。这不是一门很长的课程，只有八节课的材料。但它在算法方面比书本深入得多。例如，其中一节课详细讲解了整个 **Raft** 共识算法，它相当复杂。但我真的想向学生们展示它是如何精确运作的，因为它很好地说明了分布式系统的挑战，以及我们需要采取的各种措施来处理各种边缘情况和故障，并展示这些问题是可以克服的。这并不容易，算法非常精妙，很容易出现 bug，但以一种运行良好的方式解决共识问题是可能的。所以这确实是我试图通过这门课程传达的信息。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes. So that distributed systems course, it's a bit more theoretical than what is in the book. So it's more focused on algorithms and sort of the how we convince ourselves that the algorithms behave correctly under the assumptions of distributed systems that we talked about of like nodes may crash, communication might be unreliable, clocks might be wrong, etc. So that's really it. It's it's not a very long course. It's just eight lectures worth of of material. But it's it goes into substantially more detail on the algorithms than the book. So for example, one of the lectures goes through the entire **Raft** consensus algorithm which is pretty complex. But I really wanted to show the students exactly how it works because it's just such a nice illustration of the challenges of distributed systems and the various measures we need to take in order to handle the various types of edge cases and failures that can happen and showing that those those problems can be overcome. It's not easy and the algorithms are very subtle and it's very easy to have bugs in them but it is possible to solve consensus in a in a way that works pretty well and so that's really this the sort of message I'm trying to get across with this course.
</details>

**主持人**: 你提到，当你和 **Chris** 一起写书时，你带来了很多行业洞察和最新知识，而你带来了教学经验和有效的方法。

<details>
<summary>Original English</summary>
**主持人**: And you mentioned that when you're when you're writing the book together with **Chris** you brought a lot industry insight and being up to date and you brought your experience of of teaching and and what works.
</details>

**Martin Kleppmann**: 我不认为我有什么特别独特的教学风格，只是在讲座中我会使用幻灯片。我喜欢在讲座期间手写批注幻灯片。我只是在 **iPad** 上画画，让它更具互动性。但除此之外，它相当理论化。这部分是因为剑桥大学的系统运作方式，它更偏爱理论和笔试课程，而不是实践性的实现课程。我认为当然有可能开设一门实践课程，我未来可能会加入更多实践练习，但目前它主要是一门理论性的笔试课程，这很好。我开设的密码学课程则更注重实践。所以那门课是让学生们实际从头开始实现一些椭圆曲线之类的东西。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: I don't think I have a particularly like unique teaching style just in lectures I will go through slides. I I like to annotate the slides by hand during the lectures. I've just draw draw on an **iPad** to make it a little bit more interactive. But other than that, it it is fairly theoretical. That's partly the way the Cambridge system works. It kind of favors theoretical and pen and paper courses over say implementation practical courses. I think it it would be possible certainly to do a practical course on this and I may incorporate a bit more practical exercise in the future but right now it's mostly a theoretical pen and paper course when that is fine. The cryptography course that I do is that's much more hands-on. So that's about actually getting the students to like implement some elliptic curves from scratch for example.
</details>

**主持人**: 在你从事学术界这段时间里，你看到了计算机科学教育发生了怎样的变化？你认为未来它还会如何变化，尤其是在我们看到 **AI** 成为工业界乃至世界的一部分之后？

<details>
<summary>Original English</summary>
**主持人**: And how have you seen it in your time in in academia which has been it's now a longer time period. How have you seen computer science education changing? How do you think it might change further in in the future especially as we're seeing **AI** be part of industry and probably the world as well?
</details>

**Martin Kleppmann**: 是的，我的意思是，在 **AI** 爆发之前，计算机科学教学的变化速度实际上非常缓慢。部分原因可能在于剑桥大学，你知道，剑桥大学已经有 800 多年的历史了，每个人都以更长的时间尺度思考问题。人们往往不会急于追逐最新的潮流，而是努力专注于基本原理和思想。计算机科学的许多基本原理早在 20 世纪 30 年代就已经发展起来，并且至今仍然适用。你知道，比如 **Lambda** 演算之类的东西。所以我们相当注重这些基本原理，而不是追逐最新的时尚。话虽如此，**AI** 完全改变了我们评估课程作业的方式，例如，因为现在我们当然可以尝试禁止 **AI**，但实际上不可能强制执行这样的禁令。而且，这也有点适得其反，因为我们确实希望学生们接触新技术，并找出如何有效地利用它们。但我们希望以某种方式做到这一点，既能支持他们自己的学习，又不会损害它。那么，我们如何让学生以负责任、成熟的方式使用 **AI** 呢？我们不能完全依赖学生足够成熟，能够自己判断什么是对 **AI** 的有益使用，什么是损害他们自己学习的 **AI** 使用形式，因为他们中的一些人确实相当成熟，能够自己做出决定，但很多人不是，所以我们需要为他们提供一些护栏。而且我们确实需要确保，例如，当我们进行评估工作时，它是公平的，并且学生们认为它是公平的，如果学生们觉得他们的一些同学在没有做任何工作的情况下获得了非常好的分数，那会损害对整个系统的信任，所以我们必须非常小心地处理这个问题，老实说，我们还没有很好的答案。所以我们现在，例如，在第一学年开始时就有一个训练营，让新生接触基本的软件工程技能，比如版本控制、单元测试、生成式 **AI**，以及每个人都应该熟悉的基本知识，然后希望他们能在整个学业中利用这些来改进他们的工作。但我们如何精确处理评估等方面的事情，我们仍在摸索中。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, I mean prior to **AI** explosion happening actually rate of change is very slow in in computer science teaching. Partly that might be Cambridge, you know, Cambridge is over 800 years old like everyone thinks on longer time scales. People don't tend to rush into the latest fad and instead try to focus on the fundamentals and the ideas that a lot of the fundamentals of computer science were developed in the 1930s already and are still true today. And you know **Lambda** calculus and those types of things for example and so we have quite a bit of a focus on those sort of fundamentals rather than chasing the latest fashionable thing. That said, **AI** has totally changed the way we can assess coursework, for example, because of course now we we can try banning **AI**, but it's impossible to actually enforce such a ban. And also, it's kind of counterproductive because we do want students to engage with new technologies and figure out how to use them productively for themselves. But we want to somehow do that in a way that supports their own learning and doesn't undermine it. So, how do we get the students to use **AI** in in a responsible way, in a way that's mature? And we can't necessarily rely on the students being mature enough to know for themselves what is a helpful use of **AI** and what is a form of use of **AI** that undermines their own learning because some of them are quite mature and able to decide that for themselves, but many are not and so we need to provide some guardrails for them. And we do need to make sure that when we have assessed work for example it's fair and it's perceived as fair by the students and if the students feel that some of their co-students are getting really good marks without doing any work that undermines the trust in the entire system and so we have to be very careful with how we approach this and to be honest we don't really have good answers yet. So we do now for example have a boot camp right at the start of the first year for the new students to expose them to basic software engineering skills which is like this is version control, this is unit testing, this is generative **AI** and the sort of basics that really everyone should be familiar with and then the hope is that they will use that throughout their degree in order to just improve the work that they do. But how exactly we handle things for assessment for example we're we're still in the process of figuring out.
</details>

**主持人**: 所以听起来，行业和学术界的变化速度都会很快，我们可能会适应它，然后看看接下来会发生什么。

<details>
<summary>Original English</summary>
**主持人**: So it it sounds like the the the pace of of change is going to be fast in the industry and also in academia we'll probably adopt it and we'll see you know like what what comes after.
</details>

**Martin Kleppmann**: 是的。不过有一个区别，那就是期望的结果不同。我认为在工业界，通常期望的结果是，例如，一个可用的产品。在学术界，学生们实际产出的成果，比如学生们写的论文，那并不是重点。我们不要求学生写论文，不是因为我们喜欢阅读他们精彩的论文。我们要求他们写论文，是因为我们希望他们经历一个思维过程，这有助于他们学习一些东西。而这个思维过程和学习才是这里真正期望的结果。所以这意味着我们确实必须以稍微不同的方式来处理它，因为通常在工业界，如果你能使用 **AI** 更快地完成工作，并且得到一个等效的结果，那就绝对去做，因为是的，那就是期望的结果。而在教育领域，我们确实必须思考如何确保学习成果和思维过程仍然得到保留，以便学生在智力上受益。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes. There's a difference though which is in the desired outcomes. I think with industry generally the desired outcome is like a working product for example. In academia the actual artifacts that the students produce like an essay that the students write that's not really the point. We don't ask the students to write essays because we love reading their amazing essays. We ask them to write essays because we want them to go through a thought process which helps them learn something. And it's that thought process and that learning which is really the the desired outcome here. And so that means that we do have to approach it a little differently because in generally in in industry, you know, if you can use **AI** to get a job done faster and you get to the an equivalent result, do it absolutely because yes, that that is the desired outcome. Whereas in education we do have to think about how we ensure that the the learning outcomes and the thought processes are still preserved such that the the students benefit intellectually.
</details>

**主持人**: 这非常相关，尤其是 **Anthropic** 最近有一项研究，他们观察了初级工程师，其中一组使用了 **AI**，另一组没有，他们发现，正如你所解释的，使用 **AI** 的那组几乎没有学习到什么，而没有使用 **AI** 的那组则确实学到了。

<details>
<summary>Original English</summary>
**主持人**: It's very relevant especially **Anthropic** had a recent study where they looked at junior engineers they one of them used one group used **AI** the other one did not and they found unsurprisingly from what what you also explained that the group who used **AI** they had little to no learning whereas the group that did not they actually learned it.
</details>

**Martin Kleppmann**: 是的，我也看到了那项研究。我认为那项研究的详细方法我们可能会有点争议，但我认为其普遍原则似乎是正确的，是的，有时为了学习一些东西，你确实需要努力一下，但不要太努力。所以如果人们在某个技术细节上卡住了，他们可以使用 **AI** 来解除障碍，然后能够真正专注于主要的学习成果，那么我认为使用这些工具是好的。但是如果重点是真正地应对一些困难的想法，并在自己的头脑中思考它们，那么我们仍然需要找到方法来确保学生们正在这样做。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yes, I saw that study as well. I think the detailed methods of that study we might be able to quibble with a bit but I think the the general principle seems true that yes so sometimes in order to learn something you just have to struggle with it a bit not struggle too much so if people are stuck on some technicality and they can use **AI** to get unblocked and then be able to focus really on the the main learning outcome then I think it's good to use these types of tools but if if the point is to actually like grapple with some difficult ideas and think them through their own minds, then we need to still find ways to make sure the students are doing that.
</details>

### 工业界与学术界的互鉴

**主持人**: 你同时在工业界和学术界工作。你认为工业界可以从学术界学到什么？学术界又可以从工业界学到什么？

<details>
<summary>Original English</summary>
**主持人**: You work both in industry and academia. What what do you think industry could learn from academia and academia can learn from industry?
</details>

**Martin Kleppmann**: 这两者真的可以更紧密地结合在一起，因为它们常常相互不尊重。工业界的人会说：“啊，那是理论，那是学术，与现实世界无关。”他们真的错失了一个机会，因为实际上研究中有很多有趣的见解与现实世界非常相关。但它们不一定能跨越这个鸿沟。反过来，学术界的人会说：“哦，这些工业界的东西，你知道，那只是工程。”他们并没有真正做任何有趣的思考。那只是写一些常规的东西。我认为我将建立更好的相互尊重视为我的目标之一，通过将研究中有趣的见解带入工业实践，同时也通过现实世界中出现的问题来指导我们的研究，从而更好地将这两者结合起来。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: The two really could be closer together because often they regard each other with sort of disrespect really like the the industry people will say, "Ah, that's theoretical, that's academic, it's got nothing to do with the real world." And they're really missing a trick there because actually there's a lot of interesting insights from research that are very relevant to the real world. But they're not necessarily making their way across that chasm. In the other direction, the academics will say, "Oh, this industry stuff, you know, that's just engineering." They're not actually doing any interesting thinking. It's just like writing routine stuff. I think I see it as one of my goals to try and build better respect across both in both directions by bringing interesting insights from research into industrial practice but also by informing our research by the problems that arise in in real world and so that way like joining those two things up a bit better.
</details>

### 当前研究方向

**主持人**: 你目前正在研究哪些课题？哪些是你感到兴奋的？

<details>
<summary>Original English</summary>
**主持人**: What are your current research topics that you're working on ones that you're excited about?
</details>

**Martin Kleppmann**: 我目前主要有两个研究领域。一个是本地优先软件。这个想法是，我们希望像 **Google Docs**、**Figma** 等协作软件，但以一种能更好地保护用户数据、更少依赖单一云提供商（他们可能会将你锁定在你的文件之外）的方式，因此更具弹性。它赋予用户对其自身数据更大的自主权和掌控力。所以，这是我过去十年左右一直在研究的领域，通过开源工作、算法开发和形式化验证等多种方式。我现在还在尝试在一个完全不同的主题上建立一个全新的研究领域，那就是利用密码学来证明物理世界中的事物。我特别感兴趣的是与可持续性相关的事情。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: I have two main areas I'm working on at the moment. One is local first software. So that's this idea that we want collaborative software like **Google Docs**, like **Figma**, etc., but in a way that gives better protection to users data that's less dependent on a single cloud provider who can lock you out of your files and that's therefore more resilient. Gives users greater agency and greater autonomy over their own data. So that's an area that I've been working on for the last 10 years or so through a mixture of open source work and algorithm development and formal verification and so on. I'm now also trying to set up a brand new research area in a totally different topic which is on using cryptography to prove things about the physical world. So I'm interested there in especially sustainability related things.
</details>

**Martin Kleppmann**: 例如，如果你想验证制造特定产品所涉及的碳排放量是 X，并且你希望确保这个数字是正确的，因为你可能想将排放量作为购买决策的一部分，并选择排放量较低的产品。要使这有意义，排放量数字必须是正确的。不幸的是，目前这些数字通常不正确，因为存在谎报、欺骗和使用创造性会计技术的动机，所有这些都是为了“漂绿”。或者一个相关的事情正在欧盟发生，例如，欧盟正在出台新法规，以防止热带雨林的砍伐。所以，例如，进口到欧盟的咖啡、可可、棕榈油等，进口商需要精确证明它实际来自哪块土地，然后对照卫星图像检查该土地最近是否没有被砍伐。所以我一直在研究如何使用密码学作为一种工具来证明这些物理产品的供应链中的事物，但同时不泄露商业敏感信息。例如，一家公司不会希望透露其供应商是谁，以及它从哪个供应商购买了其生产过程中的哪种成分，因为这可能会泄露其秘密配方。所以这里的希望是，密码学可以让我们证明，例如，供应链中的会计工作已经正确完成，而无需公开透露任何关于供应商或其他客户的敏感数据。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: So for example, if you want to verify that the carbon emissions involved in manufacturing a particular product were X and you want to be sure that that number is correct because maybe you want to include emissions as part of your purchasing decision and choose the product with the lower emissions. For that to be meaningful, the emissions number has to be correct. And unfortunately at the moment the numbers are generally not correct because the incentives are to lie and cheat and to use creative accounting techniques all as a way of like greenwashing basically or a related thing is happening in the EU for example which is bringing in new regulations on preventing deforestation of tropical rainforests. So that's for example coffee, cocoa, palm oil etc imported into the EU. The importer needs to prove exactly which plot of land it actually came from and then check against satellite imagery that that was not recently deforested. And so I've been looking into using cryptography as a tool of proving things about the supply chains of these physical products but without revealing commercially sensitive information. For example, a a company will not want to reveal who its suppliers were and which ingredient to its process it purchased from which supplier, for example, because that might reveal something about its secret recipe that it uses. And so the hope here is that cryptography can allow us to prove that for example the the accounting has been done correctly across supply chains but without having to reveal publicly any of this sensitive data about suppliers or other customers.
</details>

### AI对学术界和工业界的影响

**主持人**: 从你的角度来看，**AI** 对学术界（不仅仅是学生学习方面）以及通过你的行业联系对工业界产生了怎样的影响？

<details>
<summary>Original English</summary>
**主持人**: What is your view from your vantage point on the impact that **AI** is having on academia not not just for for students studying beyond that and also industry with your industry contacts?
</details>

**Martin Kleppmann**: 是的，我的意思是，我并没有那么深入地研究 **AI**。我更多是通过我的合作者看到它，他们非常善于利用 **AI** 工具，尤其是在软件开发方面。我个人现在很少写代码，所以我自己并没有太多需要或机会实际使用 **AI** 代理。在写作散文时，比如写书时，我仍然喜欢用老式的方式，手写每一个字。所以我没有让 **AI** 接触书中的文字，例如。我不知道这是否是正确的决定。这并不是一个原则性的问题，我不认为这样做是错误的。更多的是，对我来说，写作过程是我理清思路的方式，而理清思路才是我的目标。所以我正在努力在自己的头脑中理清思路，为此我必须自己写。似乎没有其他办法。但是，将 **AI** 作为一种获取想法反馈或探索某个想法是否经得起推敲的工具，这似乎是一种非常富有成效的技术使用方式，我认为这适用于工业界和学术界。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, I mean I'm not not that deeply into the **AI** things really. I'm seeing it more through my collaborators who are making very good use of of **AI** tools for for software development especially. I personally write very little code these days and so I haven't had that much need or occasion to actually use **AI** agents myself personally. When when writing prose like working on the book for example, I prefer to still do that the old-fashioned way of just write every word by hand. So I I haven't let **AI** anywhere near the text of the book for example. And I don't know if that's that's the right decision. It's not really a a principle thing that I I think it would be wrong to do so. It's more that for myself the process of writing is the way how I figure things out and figuring things out is really my goal here. So I'm I'm trying to figure it out in my own head and for that I just have to write it myself. Does there doesn't seem to be any way around it. But using **AI** as a way of like getting feedback on ideas or exploring like whether an idea really holds up to scrutiny or things like that seems like a very productive use of the technology and that applies for for both industry and academia I would say.
</details>

### 职业发展建议

**主持人**: 那么，作为结束语，对于仍在学习并考虑进入工业界或学术界的学生或年轻专业人士，你认为哪种人会在其中一个领域更成功？

<details>
<summary>Original English</summary>
**主持人**: So as as closing for a student or a young professional who is is still studying and considering the route into either industry or academia, what have you seen who thrives in one or the other?
</details>

**Martin Kleppmann**: 是的，我的感觉是它们并非完全相互排斥。或者更确切地说，我合作过的一些最优秀的博士生，例如，实际上都有几年的行业经验。所以他们可能读了本科，也许读了硕士，然后花几年时间在工业界从事实际的软件工程工作，了解现实世界，然后可能在某个时候感到厌倦，觉得“哦，实际上，我想研究一些更理想主义的东西，或者有更多自由选择自己的研究课题”，然后开始对攻读博士学位感兴趣，我认为这是一条相当健康的道路。确实有些人直接从本科和硕士毕业后就攻读博士学位，但有时这些人可能缺乏一些广阔的视野。所以我认为，看到一些现实世界的工程实践，对人们来说实际上非常有帮助，即使他们后来想留在研究领域。但反过来，我认为它也能很好地发挥作用，因为在学术研究中，我们能够比工业界的人更仔细地思考问题。工业界的人常常，我感觉，会短路式地推理，比如可能不会从第一性原理出发彻底思考问题，而只是“哦，我在一个会议演讲中听到了这个。我就照着做吧。”而学术界可以教导的是这种细致入微的批判性思维，例如，真正地权衡利弊，并真正地证明为什么某件事是正确的。所以我认为，如果人们能在工业界和学术界之间穿梭，而不是将其视为两条完全相互排斥的职业道路，而是两者之间有一些切换，那实际上是非常好的。

<details>
<summary>Original English</summary>
**Martin Kleppmann**: Yeah, my feeling is they're not really that mutually exclusive or rather some of the best **PhD** students I've worked with for example actually have a few years of industry experience. So they might have done an undergraduate maybe done a masters then spent a few years in industry developing like actual doing real software engineering learning about the real world and then maybe at some point got bored and thought oh actually you know I want to work on maybe more idealistic things or have more freedom to choose their own research topics and then start getting interested in doing a **PhD** and that I find is is quite a healthy route. You do get people who go, you know, straight from their undergraduate degree and masters into doing a **PhD**, but sometimes those people can just lack a bit of the breadth of perspective. And so I think having seen a bit of just real world engineering is is actually really helpful for people even if they then want to stay in research. But in the opposite direction, I think it can work very well too because in in research research in academia, we just get to think things through a lot more carefully than people often do in industry. Often people in industry, I feel like sort of have short circuit reasoning, like don't maybe don't quite reason something through from first principles, but just like uh oh, I heard this from a conference talk. I'm just going to go with that. And oh yeah, what what academia can teach is this sort of nuanced and and critical thinking to really reason through trade-offs, for example, and to really like justify why something is true. And so I think it's really good actually if people can weave in and out of industry and academia a bit and not regard it as like two totally mutually exclusive career paths, but actually have a bit of switching between the two.
</details>

**主持人**: 好的，**Martin**，非常感谢。我原以为我们会更多地谈论你的书，我们也确实谈了，但我对你和所有其他人正在做的所有重要而有趣的学术工作有了新的好奇心和尊重。所以非常感谢你。感谢你接受这次精彩的采访。这真的很有趣。

<details>
<summary>Original English</summary>
**主持人**: Well, **Martin**, thank you very much. I expected us to talk a lot more about your book which we did but I I have a newfound curiosity and and respect for all the important and interesting academic work that you and everyone else is doing. So thank you so much for this. Thank you for the great interview. This was really interesting.
</details>

### 总结与展望

**主持人**: 我希望你喜欢与 **Martin Kleppmann** 的这次难得的对话。我发现了解这本书的第一版假设你拥有带有本地磁盘的机器很有趣。但实际上，如今大多数工程师不再以这种方式构建系统了。像 **S3** 这样的云原生原语改变了你构建系统的方式，这就是为什么这本书需要更新。我也很欣赏 **Martin** 对工程师在使用托管服务时是否仍然需要了解系统内部的看法。如果你在这些服务之上构建业务逻辑，你可能不需要知道每一个细节，但能够深入了解会很有用，尤其是在你需要调试系统时。在我们的对话结束时，我对 **Martin** 正在进行的学术研究有了很多新的认识。本地优先软件的工作、去中心化系统中的访问控制问题、使用密码学验证供应链排放。这些都是一些很少有初创公司会承担的艰难工程问题。很高兴能理解学术界如何能够很好地从事具有长期焦点的研究工作。请查看下面的节目笔记，了解与 **Pragmatic Engineer** 深度探讨相关的内容。如果你喜欢这个播客，请务必在你喜欢的播客平台和 **YouTube** 上订阅。如果你也给节目留下评分，我们将特别感谢。谢谢，下期再见。

<details>
<summary>Original English</summary>
**主持人**: I hope you enjoyed this rare conversation with **Martin Kleppmann**. I found it interesting to learn that the first edition of the book assumed that you have machines with local discs. But actually today this is not how most engineers build systems anymore. Cloud-native primitives like **S3** change how you build systems and this is why this book just needed a refresh. I also appreciated **Martin**'s take on whether engineers still need to undertest system internals when they're using managed services. If you're building business logic on top of these services, you probably don't need to know every detail, but it can become useful to be able to look deeper, especially when you need to debug your system. By the end of our conversation, I gained a lot of appreciation for the academic research that **Martin** is doing. The local first software work, the access control problem in decentralized systems, using cryptography to verify supply chain emissions. A lot of these are hard engineering problems that few startups would take on. It was nice to understand how academia is in a good position to do work that has a long-term focus. Do check out the show notes below for related to **Pragmatic Engineer** deep dives. If you've enjoyed this podcast, please do subscribe on your favorite podcast platform and on **YouTube**. A special thank you if you also leave a rating on the show. Thanks and see you in the next one.
</details>
</article>