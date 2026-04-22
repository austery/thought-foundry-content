---
author: The Pragmatic Engineer
date: '2026-04-22'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=SVOrURyOu_U
speaker: The Pragmatic Engineer
tags:
  - distributed-systems
  - data-intensive-applications
  - formal-verification
  - local-first-software
  - cloud-native
title: 对话 Martin Kleppmann：重新审视数据密集型应用系统与 AI 时代的工程挑战
summary: 本访谈深入探讨了分布式系统权威专家 Martin Kleppmann 的职业生涯。从早期创业到在 LinkedIn 参与 Kafka 的开发，再到撰写享誉全球的《数据密集型应用系统设计》。他分享了该书第二版针对云原生环境的更新，并讨论了形式化验证在 AI 代码生成背景下的重要性，以及他在学术界推动的 local-first 软件和加密供应链验证等前沿研究。
insight: ''
draft: true
series: ''
category: architecture
area: tech-engineering
project: []
people:
  - Martin Kleppmann
companies_orgs:
  - LinkedIn
products_models:
  - Apache Kafka
  - Designing Data-Intensive Applications
media_books: []
status: evergreen
---
### 嘉宾背景与职业生涯起步

**主持人**: 我是否应该考虑多区、多地域甚至多云的架构？为了降低可用性风险，你愿意承担多少计算开销和人为的设计运维成本？**MapReduce** 已经过时了，几乎没人再用了。但在其他领域，我们增加了覆盖范围，比如支持 AI 的系统，例如**向量索引**。作为软件工程师，如果过于依赖高层抽象而不再思考底层细节，是否会失去理解底层的动力？如果你在构建高层业务逻辑，我认为这没问题。但 **LLM** 增加了对**形式化证明**的需求，因为我们现在很多代码都是“凭感觉”写出来的。我认为形式化验证在未来会变得更重要。

《**数据密集型应用系统设计**》（Designing Data-Intensive Applications）一直是所有构建大型后端系统的工程师的必读书籍。出版 9 年后，第二版终于问世了。该书的作者 **Martin Kleppmann** 是一位跨时代的专家。我与他坐下来深入探讨了他在 **LinkedIn** 参与 **Kafka** 的工作如何直接塑造了书的第一版思想，第二版有哪些新内容，以及为什么像 MapReduce 这样的内容被删除了。我们还聊到了形式化方法、**Local-first 软件**、去中心化访问等话题。如果你关心大型系统的工作原理及其发展方向，这一集不容错过。

那么 Martin，欢迎来到播客。

<details>
<summary>Original English</summary>

**Host**: Should I consider multiszone, multi-reion or even a multi-cloud setup? How much availability risk are you willing to take on versus the computational overheads, but also the human overheads actually designing and operating the system? MapReduce is dead. Nobody uses it anymore. But other areas where we've increased the coverage are systems in support of AI like vector indexes. Is there any risk as a software engineer that you're no longer incentivized to understand the underlying layer? If you rely on a higher level abstraction, you're no longer thinking about the lower level details. If you're building higher level business logic, actually, I think it's just fine. LLMs increase the need for these formal proofs because we're vibe coding a bunch of stuff. The reason I think that formal verification could become more important in the future.

One is that Designing Data-Intensive Applications has been the go-to book for anyone building large backend systems. 9 years after publishing this book, the second edition is here. Martin Kleppmann is the author of this generational book. I sat down with him and today we cover how working on Kafka at LinkedIn directly shaped ideas that became the first edition of the book, what's new in the second edition, and why things like MapReduce got removed from this updated version. Formal methods, local-first software, decentralized access, and many more. If you care about how large systems work, where they're heading, and what the fundamentals are that don't change, this episode is for you.

So Martin, welcome to the podcast.

</details>

**Martin Kleppmann**: 你好 Ger，很高兴能来到这里。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Hi Ger, it's great to be here.

</details>

**主持人**: 能请到你真是太棒了。我想对很多软件工程师（包括我自己在内）来说，你不需要过多的介绍。你是这本标志性书籍的作者，这本书在我的书架上已经放了大概 10 年了，几乎是它一出版我就买了。在聊这本书之前，你是如何进入技术领域的？

<details>
<summary>Original English</summary>

**Host**: It's amazing to have you here. I don't think you need introduction to many software engineers, including myself. You're the author of this iconic book that I've had on my bookshelf for probably about 10 years, not much longer after it came out. Before we get into this book, which we're going to talk about, how did you get into the technology field?

</details>

**Martin Kleppmann**: 是的。和很多人一样，我本科读的是**计算机科学**。毕业后我不确定人生该做些什么，但我觉得创办一家**创业公司**似乎是个有趣的尝试。于是我开了一家公司，当时完全不知道要做什么，花了一段时间摸索有趣的方向。第一家创业公司不太成功，但我因此结识了一些人，后来他们成了我第二家创业公司的联合创始人。第二家公司运作得更好，我们把它卖给了 LinkedIn。在那之后，我开始对教学这些分布式系统的概念产生兴趣，这就是我开始写书的契机。在写书的过程中，我也从工业界转回了学术界。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yes. Well, I did a undergraduate computer science like many others. And then after that, I wasn't quite sure what to do with my life, but I thought, well, starting a startup seems like an interesting thing to try. So, I started a startup having no clue what I was going to actually do and then spent the first while searching around for things that might be interesting. The first startup didn't work out that well but through that I met some others who then became my co-founders for the second startup which worked better and we sold that one to LinkedIn and then after that I started being interested in like teaching these distributed systems concepts so that's when I got into writing the book and then during the writing of the book I also switched over from industry back to academia.

</details>

### 从测试服务到 Reportive 的被收购之路

**主持人**: 我们可以聊聊你的第一家和第二家创业公司吗？

<details>
<summary>Original English</summary>

**Host**: Can we talk a little bit about your first and second startup?

</details>

**Martin Kleppmann**: 没问题。第一家叫 **Go Test It**，大概是在 2008 年左右。那是人们很难在不同浏览器上运行 **JavaScript** 的年代。**Internet Explorer** 当时还很流行，**Chrome** 刚问世，所有的浏览器都互不兼容。Go Test It 是一个基于 **Selenium**（一个至今仍然存在的开源项目）的网站自动化跨浏览器测试服务。其核心理念是编写测试脚本，模拟用户在网站上的点击交互并检查行为是否正确。我们提供托管服务，这样人们就不用自己运行各种操作系统和虚拟机。技术上它是可行的，但我发现很难让用户真正采纳。很多开发者在理论上说“这太棒了”，但在实践中，让他们将其整合到工作流中并投入精力编写测试脚本是非常困难的。所以那家公司最后没能做大。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yeah. Go Test It, this was like 2008 or something like that. It was the age where people were having really difficulties getting their JavaScript working cross browser. Internet Explorer was still pretty big at the time. Chrome had just come out. All the browsers were incompatible with each other and so Go Test It was a cross browser automated testing service for websites was based on Selenium, an open source project that still exists. And the idea is you would write like test scripts that automate a user clicking through the various interactions with a website and then just check that the right behavior happens. And so yeah, it was based on selenium but just as it provided as a hosted service so people wouldn't have to run various VMs with various operating systems themselves. It worked technically but I found it really hard to actually get adoption for it. A lot of people building websites like in theory said oh yeah this is great. We need to test cross browser and in practice actually it was really difficult to get them to integrate it into their workflow and just get in the habit of using it and investing in writing the test scripts. So, so that ended up not really going anywhere.

</details>

**主持人**: 所以当时并没有形成有意义的商业模式或收入？

<details>
<summary>Original English</summary>

**Host**: So, so like there wasn't like a business to be done or or like revenue to be generated in meaningful sense.

</details>

**Martin Kleppmann**: 那个时代至少还有一两家同类公司成功转型为商业公司。**Sauce Labs** 就是其中之一。但即使对他们来说，业务增长也非常缓慢，那不是一个容易做的行业。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yeah. Well, there's at least one other maybe two other companies from that same era that did manage to make a business. Sauce Labs is one that that managed to actually succeed. Um, but even for them it was a pretty slow running business. I think it was not an easy business to be in.

</details>

**主持人**: 对于你的第二家创业公司 **Reportive**，它是如何诞生的？

<details>
<summary>Original English</summary>

**Martin Kleppmann**: 第二家公司 Reportive 顺利得多。我们的想法是将社交媒体集成到 **Gmail** 内部。当你收到一封陌生人的邮件时，我们的浏览器扩展程序会修改 Gmail 的界面，在邮件旁边显示一个社交档案摘要，包括来自 LinkedIn 的职位和头像、来自 **Twitter** 的推文、Facebook 的动态等等。我们在 2010 年左右起步，很快就变得非常流行。基于此，我们成功从当时还很年轻的 **Y Combinator** 筹到了钱。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yeah, the second one was Reportive. That went a lot better. So, that was putting social media inside Gmail basically. So, the idea was that if you get an email from someone you don't know, we had a little browser extension which manipulated the Gmail web interface so that on the side next to the email, we'd show you a summary social profile with like a profile picture and like a job title pulled from LinkedIn and recent tweets pulled from Twitter and maybe recent Facebook post or things like that. Just whatever we could find about that person and put that as a social summary next to the email. We started in 2010 or something like that. It was then pretty quickly became quite popular. Um and so on the back of that we were then able to raise some money from Y Combinator which was still fairly young at the time.

</details>

**主持人**: 当时 YC 确实非常年轻，你一定是那批非常早期的学员之一。

<details>
<summary>Original English</summary>

**Host**: That was very young. That you must have been one of the very early batches.

</details>

**Martin Kleppmann**: 是的，我不记得确切时间了，但确实是在早期。当时 YC 已经建立了很好的声誉，但规模还很小。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yeah, I can't remember exactly when they started but it was certainly in the early years. I think Y Combinator had already built up a quite a good reputation at the time, but it was still fairly small.

</details>

**主持人**: 作为 YC 的一部分，你必须从英国飞到旧金山参加那个为期 10 周的项目对吧？

<details>
<summary>Original English</summary>

**Host**: And then as part of Y Combinator, did you have to fly you from from the UK to San Francisco to attend that 10-week program if I remember?

</details>

**Martin Kleppmann**: 没错。我们最初是为了 3 个月的 YC 项目而来的，但后来我们申请到了美国的**工作签证**，并在旧金山定居了。旧金山给人的感觉就像是世界的中心，一切都在这里发生。最初我们谁也不认识，只认识湾区的两三个人，但通过他们介绍，我们很快建立起了网络。我非常欣赏湾区这种对外部人士的开放性。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Exactly. Yes. So we initially came for for the 3 months or whatever it was of the Y combinator but then we were able to get US work visas for ourselves and set up permanently in San Francisco. It was very exciting because you know it felt like you know going to the center of where it was all happening really and we started out not knowing anybody at all. We knew like one or two people in the entire Bay Area, but we like contacted them and they introduced us to more people and they introduced us to more people. And so we were able to pretty quickly actually build up a network and that's something that I I really appreciated that it was actually so open to outsiders like us who could just basically turn up with an idea and an early stage startup and we managed to raise some money and managed to like actually become somewhat established in the Bay Area.

</details>

### LinkedIn 收购背后的真实压力

**主持人**: 能告诉我公司是如何成长的吗？LinkedIn 的收购邀约是在什么时候出现的？

<details>
<summary>Original English</summary>

**Host**: And can you tell me how the how the company grew and and at what point did the LinkedIn acquisition offer come and and how can we imagine even you were a founder of this company.

</details>

**Martin Kleppmann**: 我们是在 2012 年卖掉公司的，当时团队只有 5 个人。虽然金额不是天文数字，但对所有人来说都是成功的。收购过程本身有很多波折，有时我们觉得会泡汤。当时我们快没钱了，也没有成功拿到下一轮融资。所以我们面临要么卖掉要么关门的压力。由于签证条款，我们甚至不能通过降薪来节省资金。所以我对最终的结果感到很满意。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: It was about in 2012 that we sold it. Um and we were five people at the time. So it's all still pretty small. Um not vast amounts of money involved but it it was a success I would say uh for everybody involved. The acquisition process it itself was fine. Is like as always with these kinds of transactions, there was like twists and turns and moments where we thought it would all fall apart and then we were almost running out of money and hadn't really succeeded in raising another round. So, we kind of had to sell or shut down. So, we were under quite a bit of pressure. We couldn't reduce our own salaries because to do so would have violated the conditions of our visas. Yes. Um so, we were in a slightly stuck situation given our lack of leverage in that situation. And actually I'm pretty happy how it all turned out.

</details>

**主持人**: 你当时是因为看到情况变糟而想要卖掉公司吗？

<details>
<summary>Original English</summary>

**Host**: So, did you go into this wanting to sell the company because you saw that things were getting a little either you needed to raise a new round or you sell to someone and then you found LinkedIn to be the best of or the only or or or the best option to go into.

</details>

**Martin Kleppmann**: 我们尝试过探索盈利选项，但没成功。我们在持续烧钱，用户增长虽不错，但不足以支撑大规模融资。所以卖掉公司似乎是“最不坏”的选择。LinkedIn 对我们很好，让我们在公司内部保持独立团队运作，继续开发我们想要的产品。尽管后来推出的 **LinkedIn Intro** 反响一般并最终关闭，但我依然感激 LinkedIn 给我们的自由。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: We tried a little bit to see like what revenue generating options we had and hadn't really managed to make that work. So, we were just burning money and and our user growth was okay but not really enough to go and raise a big round. Um, so we were like a little bit stuck there and selling the company seemed like the least bad option there in a way. And I'm pretty happy how it turned out because you know LinkedIn was great actually. They they were very good to us. They allowed us to operate as essentially like a independent team within the company. We continued working on the product that we wanted to make.

</details>

### Kafka 的诞生与 LinkedIn 的分布式系统经验

**主持人**: 你当时的**技术栈**是什么？在团队解散后，你转向了数据基础设施团队对吧？

<details>
<summary>Original English</summary>

**Host**: What tech stack did you work at the time? After our team got disbanded, I switched over to the stream processing team.

</details>

**Martin Kleppmann**: Reportive 的技术栈很平庸，主要是 **Rails** 加 **Postgres**，还有一些 **Redis**。我们基本上在 Postgres 之上构建了一个**图数据库**。转向数据基础设施后，我加入了流处理团队。当时 Kafka 刚在 LinkedIn 开发出来并准备**开源**。我参与了基于 Kafka 的流处理框架 **Samza** 的工作。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: The reporter was fairly unexciting. It was a Rails app with a Postgress database basically and some Reddit and some similar things like that mixed in. So actually you know nothing particularly revolutionary. We essentially built a graph database on top of Postgres. After our team got disbanded, I switched over to the data infrastructure. Um after our team got disbanded, I switched over to the stream processing team. So Kafka had just been developed at LinkedIn and had just right. Oh, it was just being open sourced. Yeah, I think it had just been open sourced and then uh I got to work on Samza which was a stream processing framework on top of Kafka.

</details>

**主持人**: 我一直想问，为什么 LinkedIn 会开发 Kafka？

<details>
<summary>Original English</summary>

**Host**: I always wanted to ask this question. Why did LinkedIn build Kafka or or develop Kafka?

</details>

**Martin Kleppmann**: **Jay Kreps** 有一篇著名的博客文章叫《**日志**》（The Log），解释了他的动机。为什么选择**追加式日志**（append-only log）而不是传统的**消息队列**？动机在于**数据集成**。LinkedIn 当时有大量数据库和事件生成系统，都在产生流式数据，而下游系统（如数据仓库、Hadoop 集群）需要消费这些数据来运行机器学习算法。数据集成面临的物理难题是如何将数据从一个系统搬运到另一个系统。Jay 将 Kafka 设计为一个通用的抽象集成点，用于连接各种数据源和下游数据接收端。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yes. So I think Jay Kreps has a pretty good blog post from that era called The Log where he explains his motivation behind Kafka and you know why why make it an append-only log rather than like a traditional message queue or something like that. I think the motivation was really about data integration because there were a whole bunch of databases and like event generating systems you know like activity events from users for example they were all generating data that in a sort of stream shape and then a bunch of downstream systems that wanted to consume this like wanted to get it into the data warehouse and wanted to be able to get it into the Hadoop cluster at the time in order to run like machine learning and things over it and there was just this data integration problem of actually like how do you physically get the data out of one system and into another and Jay designed Kafka as this integration point essentially like the almost the kind of lowest common denominator but still a general purpose abstraction for integrating various data sources and to downstream data syncs.

</details>

**主持人**: 在 LinkedIn 这种规模的系统下工作，有什么让你感到惊讶的吗？

<details>
<summary>Original English</summary>

**Host**: Working at LinkedIn at at you know like Kafka and at LinkedIn scale what did you learn or what surprised you about working at this type of scale?

</details>

**Martin Kleppmann**: 之前我呆过最大的公司只有 5 个人。在 LinkedIn，我突然可以用他们庞大的 **Hadoop** 集群，在 Java 里手动编写 MapReduce 任务，这非常有趣。当流处理的概念出现，Jay 开始布道 Kafka 时，我突然有种豁然开朗的感觉。我开始理解这些数据系统是如何契合在一起的，它们的共同点和基础原理是什么。这些经验直接促成了后来那本书的写作。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: That's right. Yes. Because like previously the biggest company I had worked in was Reporter with five people. We had a sizable database but it was still like a single instance database and not really that big in the grand scheme of things. And then yet suddenly I was at LinkedIn and oh we got to get get to use their big Hadoop cluster. That was fun like hand coding MapReduce jobs in Java at the time and so I I learned a huge amount there. Especially when the stream processing ideas came up and Jay was evangelizing the use of Kafka and the things you could do with it. That was kind of a revelation for me really where I suddenly like felt ah this this kind of makes sense like I'm I start to understand how these various data systems fit together what they have in common what the fundamental principles are and so that experience then fed directly into the writing of the book.

</details>

### 写作背后的故事：LinkedIn 的支持与放弃

**主持人**: 你为什么决定离开 LinkedIn？很多人可能会选择留在硅谷继续创业。

<details>
<summary>Original English</summary>

**Host**: At what point did you decide to leave LinkedIn? The arc that most people would draw would be, okay, do something more in Silicon Valley or maybe start a second startup, etc. And and instead you decided to leave LinkedIn.

</details>

**Martin Kleppmann**: 我决定回英国，继续为 LinkedIn **远程办公**。当时我女朋友（现在的妻子）还在英国，异地恋并不好受，而且我在湾区也没有强烈的归属感。我更喜欢欧洲的生活。后来我开始写书，LinkedIn 甚至大方地给了我 **50% 的带薪时间**专门用来写书，同时履行工程职责。这真的非常难得。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yeah. So, first I decided to move back to the UK actually and I continued working for LinkedIn remotely. That was mostly because my girlfriend at the time, now wife, was still in the UK and long-distance relationship is not a lot of fun and I didn't feel that at home in the Bay Area. So, I wasn't really encouraging her to move to the Bay Area either. I thought it was better for me to go back to Europe and I'm very happy with that decision. When I then started writing the book, LinkedIn even gave me 50% of my time free to work on my book alongside my software engineering duties, which is really great. Amazing. Yeah, that is so nice of them.

</details>

**Martin Kleppmann**: 确实，他们本不需要这样做。但后来我发现，边写书边做工程（还要轮值 **On-call**）太难了。**上下文切换**太多，紧急的运维任务会占据你的大脑，让你失去写作所需的思维自由。于是我决定专注于写书，离开了 LinkedIn。在那之后，我才考虑进入学术界。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Absolutely. Though then I did find then that actually trying to write a book in parallel with doing a software engineering job and being on call etc. I just wasn't able to do it. It's just too much context switching and it's very easy for the urgent things from the on call to dominate and and then not to have the you know the freedom of that you need in order to to write something new. Um and so then after a while I decided okay like it's it's probably better if I focus full-time on the book. So I then left LinkedIn and just took a sbatical unpaid sobatical i.e. unemployment to just focus full-time on the book for a while and then it's only after that that I actually even considered getting into academia.

</details>

### 如何学习分布式系统的底层逻辑

**主持人**: 写作的想法是怎么来的？你当时想写什么样的内容？

<details>
<summary>Original English</summary>

**Host**: So how did the idea of the book come? What was was it already you know this this book with with with this layout or you had an early idea back then?

</details>

**Martin Kleppmann**: 我想写一本广泛的概念概览，不是关于如何使用某个具体工具，而是比较不同类型工具之间的权衡。它必须面向从业者，而不是纯理论教材。这就是我刚入行在 Reportive 工作时最渴望读到的书。当时我们像在黑暗中摸索，遇到数据库性能问题却无从下手，因为缺乏理解底层原理的基础。如果我了解数据系统内部是如何运作的，我就能直观地诊断这些性能问题。所以我决定把它写下来，让别人不用再走弯路。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: I knew I wanted to write something that was a broad conceptual overview. So not about how you use any one specific system or tool but comparing the trade-offs between many different types of tools. And I knew that I wanted to be practitioner focused like not a theoretical textbook but something that people could use to build real systems. That was basically like the the goal with which I approached it. And this was exactly the book that I wish I had had when I was starting out and working at Reportive for example because we were all like searching around in the dark where we're having performance problems with our database and we had no idea what to do basically because we were totally lacking the foundations to actually understand what was going on and how to diagnose the issues. And so I felt that well if I had had a bit more background on how these data systems actually work internally then I could have had an intuition about how to debug these kinds of performance issues.

</details>

**主持人**: 你是如何学习这些底层原理的？比如数据库的具体工作方式？

<details>
<summary>Original English</summary>

**Host**: To start with how did you learn about for example how databases work? What resources did you use?

</details>

**Martin Kleppmann**: 很大程度上是出于好奇，不停地和人聊天并请教。在 LinkedIn，有很多资深工程师对这些东西了如指掌，但他们可能没写下来。我就不断地向他们提问，在大脑中构建起一个图景。在掌握基础后，我会去读**研究论文**，那里有更详尽的设计细节。我还读了海量的博客文章。这就是为什么每章末尾都有大量引用的原因——那都是我自己学习时参考过的资料。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: A lot of it was just kind of being curious and talking to people actually and just asking them lots of questions. And at LinkedIn there were like a bunch of senior data systems engineers who understood their stuff very well but hadn't maybe necessarily written it down. And so I just talked to a bunch of them and and quizzed them and that way started building a an image in my own mind of how this stuff works. And then once I sort of got the basics from these conversations, then I was able to go and read research papers for example. I just read a ton of blog posts as well. Um and so the reason why you see so many references at the end of each chapter in the book is well that is actually the material that I myself used in order to uh understand what was going on.

</details>

### 第一版与第二版的演进：云原生与对象存储

**主持人**: 聊聊第二版。你是从什么时候决定更新它的？

<details>
<summary>Original English</summary>

**Host**: Can you tell me about the second edition? When did the idea come about?

</details>

**Martin Kleppmann**: 第一版出版几年后，我就意识到需要更新了，因为它开始显得过时。技术环境发生了巨大变化。但现在我在学术界工作，写书成了副业，进度非常缓慢。我也意识到自己对最新的工业界实践（如 **Data Lake**）有点脱节。于是我联系了 LinkedIn 的老同事 **Chris Riccomini**（《The Missing ReadMe》的作者）。他的加入是一次完美的协作。他紧跟工业界的最前沿趋势和初创投资，而我擅长通过精准的词汇进行教学。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yeah, it it had been clear for a couple of years that the second edition was needed just because the first edition was getting a bit dated. There were changes in technology that just hadn't been reflected in the in the in the first edition. Initially then I made very slow progress with the second edition and also I kind of realized that I had slightly lost touch with current industry practices because you know I'd switched over to the the academic side. Um, but I was no longer up to speed on like what people were doing with say data legs or things like that. So then at some point it I remembered Chris Riccomini, an old colleague from LinkedIn. I had read Chris's book, The Missing ReadMe, and thought, "Oh, he's a great writer." He was up to date on like what the cutting edge was in terms of uh technology in industry. Um, I had strong opinions on how to teach essentially. And so we took essentially like my writing style plus Chris's knowledge of latest industry trends to bring the book up to date.

</details>

**主持人**: 第二版增加了哪些核心内容？

<details>
<summary>Original English</summary>

**Host**: What are the big things that you added?

</details>

**Martin Kleppmann**: 我们最想反映的是**云原生（Cloud-native）系统架构**。在第一版中，基本假设是你拥有一些带有本地磁盘的机器。如果你想在另一台机器上做副本，那是数据库软件在数据库层完成的。而现在，人们开始在**对象存储**（如 S3）之上构建数据库，副本是在存储层完成的，而不是数据库层。对象存储是一种全新的抽象，它表现得不像文件系统，其行为完全不同。这种转变在第一版出版后真正爆发了，我们将其贯穿到了全书的叙事中。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yeah so the thing we knew from the start that we wanted to reflect was uh cloud-native systems architecture. In the first edition the assumption was basically that you have some machines. Each machine has some local discs. If you want to replicate it to another machine, then well the database software will replicate it at the database level to another machine which will also write the data to its local discs. And now suddenly people are building databases on top of object stores for example. And now the replication happens at the object store level. No, no longer at the database level. Whereas an object store is just like a brand new abstraction it just looks different from a file system, it behaves differently. And so then building on top of that as a foundational abstraction is something that like people were starting to do at the time of the first edition, but since the first edition that has really taken off like a whole lot of system have have been built in that style now.

</details>

**主持人**: 现在有很多**托管服务**，工程师可能不再需要理解底层了。这有风险吗？

<details>
<summary>Original English</summary>

**Host**: But when you build on top of these things and you you kind of use those as a as primitives as well, is there any risk as a software engineer that you're no longer incentivized to understand the underlying layer?

</details>

**Martin Kleppmann**: 这确实是向更高层抽象的转变，但这正是计算机行业自诞生以来的历史。如果你在构建业务逻辑，不去关心垃圾回收或底层存储机制是完全没问题的。但总得有人去构建这些云服务。这本书的底层哲学是给人们提供系统内部运作的精华，当你遇到奇怪的性能问题时，你能有直觉知道为什么。例如，即使你使用云服务，了解 **LSM 树**或 **B 树**的区别仍然是一种“超能力”，因为这决定了你在分析场景下的系统表现。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Yeah, it's definitely a a shift to different and higher level abstractions, but you know that's been the story of the entire computing industry since the start. So it's true that like if you rely on a higher level abstraction, you're no longer thinking about the lower level details. Higher level business logic. Actually, I think it's just fine for people not to care about memory management. But somebody still has to build those lower level abstractions from lower level components. Somebody's got to implement the cloud services. I would say like the underlying philosophy of the entire book is to give people insights into just the sort of essence of how the systems work internally. So that if for example they start having weird performance behavior, you can have a bit of intuition for why it's doing that and how you might solve it.

</details>

### 可扩展性：从横向扩展到“向下扩展”

**主持人**: 你对“可靠性、可扩展性、可维护性”的定义是什么？

<details>
<summary>Original English</summary>

**Host**: Reliable, scalable, and maintainable. What do these objectives mean to you?

</details>

**Martin Kleppmann**: **可靠性**主要指**容错**（fault tolerance），即系统在网络中断或节点崩溃时仍能继续工作。**可扩展性**是讨论应对负载变化的机制。以前我主要关注**横向扩展**（水平扩展），因为单机扩容没什么好聊的。但最近我开始思考“**向下扩展**”（scaling down）。如何让一个小流量服务运行得非常便宜？像 **Serverless** 系统能够快速冷启动和关闭，使得处理每天仅有几个请求的任务几乎零成本。这在非云环境下很难实现，因为你必须静态分配 CPU 和内存。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Reliability means fall tolerance primarily. So meaning that a system should on the whole continue working even if like a network link is interrupted or a node crashes. Scalability is just like what mechanisms we have for dealing with changes in load. I guess because that's the the more interesting one like yes, you can always buy a bigger machine and exactly there's just there's not that much to be said about it. But maybe sort of part of the scalability story which I wasn't thinking about as much at the time but started thinking about more recently is not just scaling up but scaling down as well. So actually um how do you run a service in such a way that if it has a very small amount of load it's really cheap to run it. Part of what's interesting about some serverless systems for example is actually their ability to scale down and say like okay if you're going to handle just three requests per day that's just fine as well.

</details>

### 分布式系统的坑：故障与时钟

**主持人**: 你有一章专门讲分布式系统的麻烦。有哪些让你印象深刻的部分？

<details>
<summary>Original English</summary>

**Host**: You have a chapter called the troubles with distributed systems. Can you recall some of the things that are memorable to you?

</details>

**Martin Kleppmann**: 分布式系统理论中，我们倾向于假设一些事情，比如消息传输没有上限时间。在实践中，这意味着你不能假设网络延迟。另一个是“崩溃”的定义——是软件崩溃、硬件故障、电源线被拔掉，还是仅仅是网络断连？这一章引用了大量的案例研究，比如鲨鱼咬断海底电缆导致网络中断。后来海底电缆的屏蔽增强了，鲨鱼不咬了，但陆地上的牛可能会踩断电缆。不要相信任何人说的“故障很少见，不用担心”，如果你想要可靠性，就必须考虑各种奇怪的边缘情况。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: The whole idea of this chapter is that in distributed system theory there are certain things that we tend to assume. Like for example, we just assume that there's no upper bound on how long it might take for a message to go over the network. Another thing is about uh crashes. Distributed system theory just says like nodes can crash but what does that actually mean? Is like don't believe anyone who says oh failures are rare it's don't don't worry about it it's fine. The the the moral of this chapter is really that actually know if you want to make things reliable, you really do have to worry about a whole bunch of weird unusual but but certainly possible edge cases. Timing is another one. We just can't rely on clocks because actually they're just not precise enough.

</details>

### 形式化验证与 AI 的交汇

**主持人**: 你最近写过一篇关于**形式化验证**及其在 AI 时代重要性的文章。你能解释一下它吗？

<details>
<summary>Original English</summary>

**Host**: One of the hot topics these days is of course AI and you've written a very interesting post about this just in December about formal verification. Can we talk about what this is and how you envision this becoming more important?

</details>

**Martin Kleppmann**: 形式化方法包括使用 **TLA+** 或 **FizzBee** 等规范语言描述系统预期行为，并通过模型检查器运行大量场景。更进阶的是**形式化证明**，即通过数学证明算法实现始终满足规范。这和测试的区别在于：测试只是尝试一些例子，而证明可以涵盖无限的状态空间，排除所有可能的漏洞。以前这太耗时了，我在工业界从没用过，直到进入学术界才有时间花几个月证明一个精妙的算法。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: One approach is to for example use a specification language like FizzBee or TLA+ to describe the expected behavior of a system. The more advanced level is to use actual formal proof. And the distinction to testing there is that well in testing you just try through a couple of examples. But a proof can reason about potentially infinite state spaces. It can tell you things about like every possible thing that could possibly happen in the entire universe. Formal verification is is a lot of work. I never used it in my time in industry because it's just too too timeconuming basically.

</details>

**Martin Kleppmann**: 为什么我觉得它在未来更重要？
1. **LLM 擅长写证明**: 如果我们不需要手工编写繁琐的证明步骤，形式化验证在经济上就变得可行了。
2. **“凭感觉编码”（Vibe coding）**: 随着 AI 生成海量代码，人工审查会成为瓶颈。我们需要自动化的方式来确保代码正确。特别是在安全领域，一个微小的 Bug 就能摧毁整个系统，形式化验证能确保完全没有 Bug。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: The reason I think that formal verification could become more important in the future is kind of several aspects to it. One is that the LLMs are getting increasingly good at writing these proofs. But also, LLM increase the need for these formal proofs because, you know, we're vibe coding a bunch of stuff. If we have to manually review all of that code, then that will become the bottleneck. So, we need some automated way of checking whether the code is correct. And writing lots of tests is a very good starting point. But the thing that proof can do that tests can't is to consider absolutely every possible thing that could happen. And that's really important in a security context.

</details>

### 学术研究的自由：Local-first 软件

**主持人**: 你如何看待学术界与工业界的差异？

<details>
<summary>Original English</summary>

**Martin Kleppmann**: 学术界可以思考得更长远。在创业公司，你必须在几个月内出货，无法思考 10 年后的事情。学术界有自由去研究那些目前商业上不可行，甚至与商业激励相悖的方向。我研究了多年的 **Local-first 软件**就是其中之一。其核心理念是削弱云运营商的权力，将数据控制权还给终端用户。**SaaS** 商业模式本质上是威胁用户：“付订阅费，否则我就删除你的数据”。虽然我理解这种商业逻辑，但这对用户来说并不健康。作为学者，我可以把商业模式放在次要位置，优先考虑用户的权利。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: Academia can just think much longer term. If you're doing a startup you have to ship something within a few months. In academia what I really appreciate is the freedom to work on things that are long-term and which are not like immediately commercially viable or which are not aligned with the incentives of commercial companies. Um so one of research area that I've been on for several years now is what we call local first software which is this idea that we want to take away a bit of the power from cloud operators and give it back to end users. Software as a service businesses, for example, the whole reason why they can charge a subscription is because they are able to essentially hold a gun to the customer's head and say, "Pay us your subscription, otherwise we will delete all your data."

</details>

**主持人**: 这种去中心化架构带来了哪些工程挑战？

<details>
<summary>Original English</summary>

**Host**: What are some of these really interesting engineering challenges that we we will need to solve to get to a more viable local first software?

</details>

**Martin Kleppmann**: 挑战非常巨大。比如简单的**访问控制**。在中心化服务中，服务器决定谁先撤销了权限，谁后修改了文档。但在去中心化或点对点设置中，可能会出现用户权限被撤销的同时又修改了文档。不同设备看到这两个事件的顺序不同，导致永久性的不一致。为了保持高可用和离线工作能力，我们不能简单地使用**共识协议**（Consensus），因为那要求节点在线并进行投票。我们尝试在不依赖共识的情况下解决这个问题。我参与的 **Automerge**（一个 **CRDT** 库）就在尝试攻克这些极其复杂的分布式计算难题。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: In a centralized cloud service model it is totally straightforward because you have the rules you confirm that those sort of things and you check for the right roles and that's it. But if you want to run your system over multiple providers or even in a peer-to-peer setting then what could happen is that a user gets their edit permissions revoked and concurrently that user makes an edit to the document. Now some devices may see the edit first and the revocation second, and another device may see it the other way around. They've become permanently inconsistent. So then you could have a consensus protocol, but then consensus is messy because it requires nodes to be online. We've been trying to do the whole thing without doing consensus.preserving high availability, preserving the ability for user to work offline.

</details>

### AI 时代的教育：结果与过程的权衡

**主持人**: 你在剑桥大学教书，AI 爆炸如何改变了计算机科学教育？

<details>
<summary>Original English</summary>

**Host**: How have you seen computer science education changing? How do you think it might change further in in the future especially as we're seeing AI be part of industry?

</details>

**Martin Kleppmann**: 工业界的目标是结果——一个能运行的产品。如果 AI 能帮你更快完成，尽管去做。但教育的目标不是那篇论文或代码本身，而是学生在创作过程中经历的**思考过程**。我们无法禁止 AI，也没必要，但我们必须给学生提供“护栏”，确保他们没有因为依赖 AI 而削弱了自己的学习能力。有些研究表明，使用 AI 的初级工程师学习效果较差，因为你必须经历一番挣扎才能真正学会某些东西。如果 AI 只是帮你解决技术琐碎让你专注于核心逻辑，那是好事；但如果它代替了你的思考，那就有问题了。

<details>
<summary>Original English</summary>

**Martin Kleppmann**: In industry generally the desired outcome is like a working product. In academia the actual artifacts that the students produce like an essay that the students write that's not really the point. We ask them to write essays because we want them to go through a thought process which helps them learn something. And so we need to provide some guardrails for them. Sometimes in order to learn something you just have to struggle with it a bit. If people are stuck on some technicality and they can use AI to get unblocked and then be able to focus really on the the main learning outcome then I think uh it's good. But if the point is to actually like grapple with some difficult ideas and think them through their own minds, then we need to still find ways to make sure the students are doing that.

</details>