---
author: The Pragmatic Engineer
date: '2026-06-03'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=UlXpOGIpITM
speaker: The Pragmatic Engineer
tags:
  - career-path
  - self-taught
  - infrastructure-automation
  - data-center
title: Kelsey Hightower：从麦当劳打工到谷歌卓越工程师的非传统进阶之路
summary: 在本次深度访谈中，知名技术先驱 Kelsey Hightower 讲述了他非传统的职业轨迹。从高中辍学、考取 A+ 认证进入 IT 行业，到自主创业，再到加入谷歌管理数据中心。他分享了在互联网发展早期的硬件运维经历，以及他对自动化和声明式基础设施的独到见解，揭示了通过极强执行力在科技行业不断突破自我的真实故事。
insight: ''
draft: true
series: ''
category: career-development
area: work-career
project: []
people:
  - Kelsey Hightower
companies_orgs:
  - Google
  - Microsoft
  - Docker
  - Rackspace
  - Puppet
products_models:
  - Kubernetes
  - Terraform
  - FreeBSD
  - AutoCAD
media_books: []
status: evergreen
---
### 引言：容器大突破与微软的邀约

**主持人**: 你认为究竟是什么让 **Kubernetes** 取得了突破？

<details>
<summary>Original English</summary>

**Host**: What do you think really made Kubernetes breakthrough?

</details>

**Kelsey**: 排名第一的成功标准是 **Docker**。现在，你不需要再争论 Java、Python 还是 Ruby，你只需要讨论如何调度 Docker 容器。我们已经赢在了起跑线上，因为你可以直接复用相同的 Docker 容器。我还记得我收到了微软 CEO 萨提亚（**Satya Nadella**）发来的一封邮件，我当时想，天哪，他写了这么热情洋溢的邮件，我点开那个 PDF，发现薪资数字后面加了一个零。你看着这个会觉得，我都不知道他们还能开出这种条件。我们知道有这种事，但那个在 1999 年高中毕业、选择去考 **A+ 认证**的人，根本不知道还有这种机会。所以我当时是很认真地考虑去**微软**的。

我不是那种纯粹讨厌生成式 AI（**GenAI**）的人。我只是不喜欢那种天真盲目的推崇和采用。我认为应该采取更具战略性的方式。因为我把 GenAI 看作一种工具，而不是伟大的人类替代品，这样我就可以用更加务实的方式去使用它。当涉及 AI 时，在这个会议开始前我唯一会做的事就是，绝对不要提 AI，因为……

<details>
<summary>Original English</summary>

**Kelsey**: The number one success criteria was Docker. Now instead of talking about Java versus Python versus Ruby, you only have to talk about scheduling Docker containers. We were already off to a running start because you could just reuse the same Docker containers. And I remember I get this email from Satia, the CEO of Microsoft, and I'm like, man, he wrote this nice email and I open a PDF and there's a zero get added to the equation. And so you're looking at this like, I didn't even know that they do that. We know that it happens, but the person that graduated from high school in 1999 that chose the A+ certification didn't know that was available. So, I was serious about going to Microsoft. I'm not just like a Genai hater. I just don't like the naive promotion and adoption of it. I think it should be way strategic. And since I think about Genai as a tool versus the great human replacement, then I can use it in way more primatic ways. And when AI is involved, the one thing I just do before the thing kicks off in this meeting, do not say AI because

</details>

### 节目介绍与声明式测试工具

**主持人**: **Kelsey Hightower** 虽被誉为 Kubernetes 社区最具影响力的声音之一，但你绝对猜不到他的职业生涯是如何开始的。19 岁时，他从大学辍学成为一名 DSL 调制解调器安装员，随后成为了一名自学成才的开发者，并最终晋升为**谷歌**的杰出工程师 (Distinguished Engineer)。在 43 岁这年，他在行业的巅峰时期选择了退休。今天，我们将探讨 Kelsey 进入科技界的非传统路径，以及他如何（往往在不知不觉中）不断为自己创造新的机会。这里有容器大战、**Puppet**、Docker、**Terraform**、**CoreOS** 以及 Kubernetes 最终如何胜出的内幕故事。我们会聊到他如何从一名谷歌的独立贡献者 (IC) 走到高管级别，以及他如何拒绝了萨提亚·纳德拉亲自发出的微软邀约，却依然让自己的薪水翻倍。他为那些担心被 AI 商品化的软件工程师提供了脚踏实地且务实的建议，此外还有很多精彩内容。如果你是一名正在思考长期职业发展轨迹的工程师，无论你是想晋升到 Staff 以上级别、成为独立开发者，还是甚至在悄悄计划离开这个行业，这一期节目都是为你准备的。坦白说，这期节目比平常的节目要长，因为我完全被钉在了椅子上，几乎全程都在倾听 Kelsey 的故事和思考。

<details>
<summary>Original English</summary>

**Host**: Kelsey High Tower is known as one of the most influential voices in the Kubernetes community, but you wouldn't guess from how his career started. At 19, he dropped out of college to be a DSL model installer, became a self-taught developer, and still went on to become a distinguished engineer at Google. At age 43, he then retired at the very top of the industry. Today we cover Kelsey's unconventional path into tech and how he kept creating new opportunities for himself often unknowingly. The inside story of the container wars, puppet, Docker, Terraform, Coros and how Kubernetes eventually won. Going from a Google IC to executive level and how he rejected a Microsoft offer from Sachio Nadella himself and still doubled his compensation. His grounded on pragmatic advice for software engineers worried about being commoditized by AI and so much more. If you're an engineer thinking about your long-term career trajectory, whether that's getting into a staff plus level, going independent, or even quietly planning to leave the industry, this episode is for you. This episode is longer than a normal episode, frankly, because I was so glued to my chair, mostly listening to Kelsey's stories and thinking.

</details>

**主持人**: 本期节目由 **Antithesis** 呈现。无需人工审查或传统的集成测试，即可验证系统的正确性，避免系统错误或宕机。在我们开始之前，我想提一下我们的展示赞助商 Antithesis，顺便给大家上一堂简短的历史课。在过去的二十年里，软件开发经历了一场从命令式 (imperative) 到声明式 (declarative) 方法的思维转变。基础设施就是一个完美的例子。想想像 Puppet 和 Ansible 这样的工具，它们允许我们声明单个服务器应该如何配置。然后是 Terraform，它让我们能够声明整个基础设施的期望最终状态——服务器、网络、数据库以及它们之间的关系。接着有了 Kubernetes，我们不再需要编写脚本来管理容器的生命周期。相反，我们编写清单 (manifests)，声明类似“我希望这个应用的副本暴露在这样一个具有指定 CPU 和内存的服务背后”。一旦我们不再需要指定基础设施的每一个微小细节，部署软件的速度就变得快得多了。

但随后的瓶颈变成了我们能多快地测试和验证要部署的代码。测试依然是命令式的。我们必须为每一个小细节编写测试。而现在有了 LLM（大语言模型），我们在代码编写方式上也处于声明式转变的边缘。只需告诉模型你想要什么，让它去搞定细节，但这将使验证瓶颈恶化一百万倍。Antithesis 是一款声明式测试工具，能够跟上你的 AI 编码智能体的节奏。你只需声明你希望软件具备的属性，Antithesis 就会想办法为你进行验证。以智能体编写代码的速度来验证你的代码，并带着满满的信心发布产品。欢迎访问 insys.com/pragmatic。

<details>
<summary>Original English</summary>

**Host**: This episode is presented by Anticys. Verify your systems correctness without human review or traditional integration tests and avoid bugs or outages. Before we start, I'd like to mention our presenting sponsor, Antithesis, and maybe offer a little history lesson. Over the last two decades, software development has gone through a mindset shift from an imperative approach to declarative one. Infrastructure is a perfect example. Think about how tools like Puppet and Ansible allow declaring how individual servers should be configured. Then came Terraform, the ability to declare the desired end state of your whole infrastructure, servers, networks, databases, and their relationships. And then with Kubernetes, we stop scripting container life cycles. Instead, we write manifests that say things like, I want the replicas of this application exposed behind a surface with this much CPU and memory. Once we didn't have to specify every little detail of our infrastructure anymore, deploying software became much faster. But then the bottleneck became how quickly we could test and verify the code to be deployed. Testing remained imperative. We had to write tests for every little detail. And now with LLMs, we're on the verge of a declarative shift in the way code is written as well. Just tell the model what you want and let it figure out the details, and it's going to make the verification bottleneck a million times worse. Anthesis is a declarative testing tool that can keep up with your AI coding agents. You state the properties you want your software to have, and antithesis figures out how to check them for you. Verify your code as fast as agents can write it and ship with Growlin confidence. Head to insys.com/pragmatic.

</details>

### 麦当劳打工与早年经历

**主持人**: Kelsey，欢迎来到播客。很高兴能见到你本人。

<details>
<summary>Original English</summary>

**Host**: Kelsey, welcome to the podcast. It's so nice to see you in person.

</details>

**Kelsey**: 是的，我其实也很高兴来到这里，主要是因为这些年来我一直在关注你的内容。所以，我也很荣幸能来到阿姆斯特丹。

<details>
<summary>Original English</summary>

**Kelsey**: Yeah, I'm actually happy to be here mainly because I kind of look at your stuff over the years. So, it's honor to be here in Amsterdam as well.

</details>

**主持人**: 你工作后赚的第一笔钱是怎么来的？

<details>
<summary>Original English</summary>

**Host**: How did you make your first dollar at a job?

</details>

**Kelsey**: 噢，我工作后赚的第一笔钱是在**麦当劳**，对吧？那也算。在高中时，你通常会找离你最近的工作。所以，那家店就在我离家步行的范围内。我一到法定年龄，嗯，14 岁，就拿到了工作许可。我去了那里，那是那种你当天去填申请表的工作。通常你当天留下信息或者当天就会被录用。他们问我什么时候能开始？我说，就现在。他们就去后面给你找了件衬衫。问我穿什么尺码？嗯，男士大号。那份工作我喜欢的一点是，你要和匆匆忙忙的真实人群打交道。这份工作不好的地方大概是，很多人并不尊重做这份工作的人。所以，他们有点把你当成他们和他们想要的东西之间的一个中间介质。但是在那样一家餐厅里，涉及到非常多的事情。它的运作非常高效。嗯，你知道，人们是有期望的。而我学会了如何管理整家店。

所以，到了我 15 岁的时候，我已经是一名助理经理了。所以在晚上和周末，其他经理会离开。他们会把钥匙交给这个 15 岁的孩子。我知道那里所有事情的操作流程，包括关店结账，对吧？所以你必须清点所有的钱。每天晚上你必须把这张巨大的电子表格传真给总部。然后我妈妈会来接我。所以在那个年纪学习如何真正承担起成人的责任，是非常好的学习经历。这就是我赚到第一笔钱的方式。

<details>
<summary>Original English</summary>

**Kelsey**: Oh, my first dollar at a job McDonald's, right? That counts. So, in high school, you get the job that's closest to you. So, it was in walking distance of my house. As soon as I turned legal age, uh 14, get a work permit. And I went there and it was one of those jobs where, you know, you go, you fill out the application the same day. You typically get your information or you're going to get hired the same day. When can you start? I'm like, right now. They go get a shirt for you in the back. You What size do you wear? Uh, men's large. And the one thing I liked about that job is you're dealing with real people that are in a hurry. I guess one bad part about the job, you know, a lot of people don't respect people who have that job. So, they kind of look at you as just like this intermediary thing between them and what they want. But there's so many things that go into a restaurant like that. It's very efficient. Um, you know, people have expectations. And I learned how to run the whole store. 

So, by the time I turned 15, I was a assistant manager. So, nights and weekends, you know, other managers would leave. They would give this 15-year-old the keys. And I knew how to do everything there, including close out the store, right? So, you have to count all the money. You have to fax this huge spreadsheet to corporate every night. And then my mom would pick me up. And so it was really good learning how to really be responsible even for adults at that age. So that's how I got my first dollar.

</details>

### 结缘编程与放弃大学

**主持人**: 你是如何进入科技行业的？你是怎么接触到编程的？

<details>
<summary>Original English</summary>

**Host**: How did you get into tech? How did you get into programming

</details>

**Kelsey**: 在高中的时候，因为我从加州搬到了亚特兰大，对吧？你从国家的这一头搬到了另一头。我大概错过了 3 到 6 个月的课程，为了能按时毕业，我必须多修几门课。作为一个参加体育运动、跑田径、打橄榄球、打篮球的人，我当时觉得，那什么计算机编程，不是，是计算机俱乐部、技术学生协会，它一部分是课堂学习，一部分是课后活动。我当时在想，我不知道，伙计。这些计算机相关的玩意是给那些……你知道的，我可是想当个酷小孩的。但我确实做了一件事，而且我非常喜欢，对吧？所以我对 **AutoCAD** 产生了兴趣。我甚至参加了 AutoCAD 的州级比赛。我们开车过去比赛。他们给你一个任务，你坐在电脑前。那是我第一年参加，但我真的很喜欢这种感觉，就是拿到一个规范要求，把它设计出来。如果我能让产品正常运行的话，我可能就拿第一名了，因为你还必须把它打印出来，让评委来评审你的作品。所以我拿了第二名，尽管我并没有完全搞定。

<details>
<summary>Original English</summary>

**Kelsey**: in high school since I moved from California to Atlanta? So right, you're going from one side of the country to another side of the country. And uh I missed maybe 3 to 6 months of school and in order to graduate on time, I had to take some extra classes. And so as someone who played sports, ran track, uh played football, played basketball, and it's like, you know, there's this computer programming not, you know, computer club, technology student association. There was a class component and then there was after school component. And I was like, I don't know, man. This computer stuff that's for the, you know, you know, I'm trying to be a cool kid. But the one thing I did, I really enjoyed it, right? So I I had a liking to AutoCAD. I even competed at the state level in AutoCAD. So we we drove down and you compete. They give you a task and you sit in front of the computer. It was my first year doing it, but I really like the idea of like taking a specification, designing it, and I probably would have gotten first place if I would have got the product to work because you also have to print it out so that the judges can review your work. So I got second place even though I didn't.

</details>

**主持人**: 这是 3D 建模。

<details>
<summary>Original English</summary>

**Host**: This is the 3D modeling.

</details>

**Kelsey**: 是的。AutoCAD，你知道，就是 AutoCAD。对。课程的一部分是，造桥。我们还和分会的团队做过一些活动，比如设计一个徽章，或者进行一场辩论。你学会了所有这些与商业相关的东西，但 CAD 是我最喜欢的东西之一。同样在那门课上，我的一个同学教了我 **TI-BASIC**。

<details>
<summary>Original English</summary>

**Kelsey**: Yeah. AutoCAD, you know, just AutoCAD. Yeah. So part of the curriculum was, you know, you build bridges. We did this thing with um chapter team where you know you have a code of arms and you're kind of doing like a debate. Do you kind of learn all of these things uh related to business but CAD was one of the things I like most? Also in that class one of the classmates taught me TI basic.

</details>

**主持人**: 那是 BASIC 语言的一个版本吗？

<details>
<summary>Original English</summary>

**Host**: Is that a version of of basic?

</details>

**Kelsey**: 这个嘛，TI-BASIC，你知道那个图形计算器吧，就像 **TI-86**。

<details>
<summary>Original English</summary>

**Kelsey**: Well so TI basic so you know the graphing calculator it's like a TI86. Oh yeah.

</details>

**主持人**: 你可以给它编程。

<details>
<summary>Original English</summary>

**Host**: You can program it.

</details>

**Kelsey**: 哦，对。所以在课上他们说，嘿，你知道这不仅仅是一个图形计算器，你实际上是可以给它编程的。我当时就问，那是什么意思？他们说，看，在那个时候，你会编写贪吃蛇游戏，对吧？基本上就是拿一本杂志，复制粘贴上面的代码，然后运行它，现在你就在玩基于你自己写的代码的贪吃蛇了。你会摆弄这个概念，所以这大概是我第一次接触编程，字面意思上就是给我的 TI-86 计算器编程。

<details>
<summary>Original English</summary>

**Kelsey**: Oh right. So in class they're like hey you know it's not just a graphing calculator you can actually program it. And I was like what's that? And it's like look we can you know every at that one at that time you would create the snake game right so it's basically get a magazine copy and paste the code and then you run it and now you're playing snake uh based on the code you wrote and so you would toy around with this concept so that was probably the first introduction to programming was literally programming my my TI86 calculator

</details>

**主持人**: 高中毕业后你上大学了吗？或者你考虑过上大学对吧？

<details>
<summary>Original English</summary>

**Host**: and after high school did you go to college or you considered college right

</details>

**Kelsey**: 我考虑过上大学，因为当时的佐治亚州，直到今天也是，有一个叫 HOPE 奖学金的项目。如果你有 B 或以上的平均成绩，你就可以免费上任何公立学校。佐治亚州的公立学校包括佐治亚理工学院 (Georgia Tech)、佐治亚州立大学 (Georgia State)。这些都是相当不错的高校。它们真的很棒。于是我决定去附近的一所大学。前两周我觉得，嗯，这太慢了。这根本不是我想前进的节奏。而且记住，我毕业那会儿可是 1999 年。所以当你打开电视时，人们正排着队购买新版本的 Windows。到处都充满着狂热的情绪。AOL 开始逐渐淘汰，我们开始接触高速互联网。我当时就觉得，哟，看看这发展的速度！而且你也会听到各种传闻。比尔·盖茨 (Bill Gates) 从大学辍学了。大家不再像以前那样过度美化文凭了。现在一切都看重技能。

然而对我来说不幸的是，我不认识任何当程序员的人。我不认识任何系统管理员，因为在那个时候，所有的系统都像 Sun 微系统 (Sun Microsystems) 或是 IBM 大型机，这些仍然是企业里在用的东西。所以当我查看招聘信息时，我看到了一堆我根本不知道该如何获取的技能。所以，我没有去上大学，当时我还在做快餐，在必胜客送披萨。我记得我去了一家书店，他们那里有 **A+ 认证**的指南，我看了看，当时有些招聘广告上写着，“嘿，你需要有 A+ 认证才能胜任这个技术支持职位（或者其他什么职位）。” 我当时想：“你知道吗？这不需要上大学。这书才卖 35 美元。” 

我记得我买了那本书，这是一个官方的认证流程。它看起来属于就业市场的一部分。所以我记得我买了那本书，然后一遍又一遍地从头读到尾。你在学习所有的基础知识，对吧？你在学习主板、内存以及所有这些东西是如何工作的，它有一部分是关于操作系统的，然后在书的后面有一小段模拟考试。所以对我这样的人来说，有这种快速的反馈循环非常好：你把 CD 放进去，你参加考试，即使是选择题，你也会觉得，如果我做错了任何一题，我就可以翻回书本，确保我理解了那里写的内容，然后再去考一次。而且它还有一点随机性，所以你不能仅仅依靠死记硬背。

我记得去考试中心参加考试，你在那个小房间里，他们想确保你不会作弊。所以有一个摄像头对着你，你只管做题。这种考试的好处在于，没有陷阱题。你要么知道，要么不知道。我想他们大概会给你一个小时到一个半小时的时间。我记得我只用了大概 10 分钟就做完了。当我走下来的时候，你等在那里，拨号网络连接上，他们计算出你的分数，然后说：“嘿，你通过了。” 接着你走出去，你就成了拥有 A+ 认证的人了。那是我职业生涯中第一次感觉到，哦，原来只要你投入努力，你就能获得证书。当我拿到那个证书的时候，我记得当时有一个类似招聘会的地方，说嘿，任何拥有 A+ 和 Network+ 认证的人，都可以加入承包商团队，当时我们正在把人们的拨号上网替换成 DSL。

<details>
<summary>Original English</summary>

**Kelsey**: I considered college because in Georgia at the time and still today there's a thing we're called the hope program. So if you have a B average or above, you can go to any public school for free. And public schools in Georgia include Georgia Tech, Georgia State. These are pretty good universities. They're really good. And so I decided to go to one that was near me. The first two weeks I was like, um, this is too slow. This is not this is not the pace that I want to move at. And also remember it's 1999 when I'm graduating. And so when you turn on the TV, people are standing in line for the next version of Windows. There's a lot of euphoria. AOL is starting to phase out and we're starting to touch on highspeed internet and and I was like, yo, look at look at the pace this is moving, but also you're hearing the narratives. Bill Gates drops out of college. These people are not necessarily glorifying the degree anymore. It's all about the skill. 

Now, unfortunately for me, I didn't know anyone that was a programmer. I didn't know anyone that was like a system administrator because at that time all the systems with like Sun Micros systemystems or IBM mainframe those are still the things that are in the enterprise. So when I looked at the job openings I'm seeing a bunch of skills that I don't even know how to acquire. And so instead of going to college you know I'm still doing fast food delivering pizzas at this time at Pizza Hut. And I remember going to a bookstore and they had the A+ certification guide and I looked and some of the job postings said, "Hey, you need to be A+ certified to take this support role or whatever it was." And I was like, "You know what? That doesn't require college. The book is only $35." 

And I remember buying the book and it is an official certification process. It looks like it was part of the job market. And so I remember buying that book and reading it cover to cover over and over again. and you're learning all the fundamentals, right? You're learning about, you know, how motherboards and how memory and all these things work and there's an OS component and then there's a little practice exam in the back. And so for someone like me, having that fast feedback loop of like you put the CD in, you take the exam and even though it was multiple choice, you kind of felt like if I got anything wrong, I would just go back to the book and make sure that I understood what was written there and then you go take the test again. and it had a little randomization to it so you couldn't just rely on absolute remembering everything. 

And I remember going to the facility to take the test and you know you're in that little room and they want to make sure you don't cheat. So there's a camera pointed at you and you're just going through it. And so the nice thing about those tests, there's no trick questions. Either you know it or you don't. And I think they maybe give you an hour, hour and a half. And I remember finishing that thing in like 10 minutes. And when I walk down, you know, you wait, the dialup goes and they calculate your score and say, "Hey, you passed." And then you walk out and you're like A+ certified. And that was like the first time in my career that I felt like, oh, so if you put the effort in, you can gain the certificate. And when I got that certificate, I remember there was like a job fair where, hey, anyone that has A+ and network plus certification, you can be part of the contractors that were replacing people's dialup with DSL at the time.

</details>

**主持人**: 可以说你当时认为这是进入科技行业最有效率的方法吗？

<details>
<summary>Original English</summary>

**Host**: Is it fair to say that you saw that this could be the most efficient way to get into tech at the time?

</details>

**Kelsey**: 我想我当时是把它看作唯一的方法。

<details>
<summary>Original English</summary>

**Kelsey**: I think I said I saw it as the only way.

</details>

**主持人**: 为什么大学从来没有告诉你，比如，好吧，这也可以是一条路。是因为你没有看到先例还是……

<details>
<summary>Original English</summary>

**Host**: Why was college never like telling you like, okay, that could be a way. Was it just you didn't see examples or

</details>

**Kelsey**: 是的，我从来没见过这样的先例。我从来没有看到过最终的结局会怎样。当时他们课程表里教的很多东西，感觉为了这些去付那么多钱是说不通的。你要知道，也许那不是一所好学校。也许我选错了课。这其中有很多因素。但当我看待这件事的时候，我当时敬仰的那些人，他们似乎走的都不是这条路。而且我真的受够了学校，对吧？如果你当时 18 岁，你就会觉得，听着，这套东西我已经受够了。因为在那个时候，我有点觉得学校就是这样，因为它对我来说太容易了，实际上。你知道，拿全 A 很容易。我不觉得有任何真正的挑战。所以就好像，嘿，我还得再去上四年这种东西。后来我了解到，本科很多时候和你在 K-12（从幼儿园到高三）经历的差不多，你就是记住一些东西，听听课，但在硕士阶段，你要对材料提出质疑，当然如果你能读到博士，理想情况下你要为这个领域增添新的东西。而我从未见过任何人能走到那一步。所以我从来没有把这些纳入我的计算之中。

但是，能拿到 A+ 认证并获得那种即时的反馈循环，让我觉得，哦，我准备好参与到实际的经济和生态系统中去了。所以，对我来说，我觉得这似乎是一条更好的路。而且这条路感觉是我自己可以掌控的。

<details>
<summary>Original English</summary>

**Kelsey**: I Yeah, I never saw the examples. I never saw the endgame. A lot of the stuff that they were teaching the curriculum, it didn't make sense that you would pay all that money. You know, look, maybe it wasn't a good school. Maybe it was the wrong class that I took. There's so many factors that could have went into this. But when I looked at it, none of the people that at the time that I was looking up to, this is not the path that they seem to be taking. And so I had enough of school, right? If you're 18 at that time, you're like, look, that that's enough of this. Because at the time, I kind of felt school was this because it was so easy for me actually. You know, it's like it was easy to get straight A's. I didn't feel like there was a serious challenge. So it's like, hey, I want to go and do four more years of this. And I would later learn that look bachelors is a lot of the similar that you go through through K through 12, you kind of remember stuff, you listen to the lessons, but then masters you challenge the material and of course if you make it to PhD ideally you're adding something new to the field and I never saw anyone that has made it that far. So I never put that in part of my calculus. 

So, but just having that immediate feedback loop of like getting this A+ certification and feeling like, oh, I'm ready to participate in the actual economy, the ecosystem. So, to me, I was like, this seems like a better path. And it felt like a path that I would control.

</details>

### 第一次技术工作与自主创业

**主持人**: 那么你能拿到证书后找到的第一份工作是什么？就是通过这个 CompTIA 认证找的，对吧？

<details>
<summary>Original English</summary>

**Host**: And then what was your first job that you could get with with the certification? This was the comta, right?

</details>

**Kelsey**: 是的。那时候，南方贝尔 (**BellSouth**) 可能是美国最大的电信公司。你知道，那个时候他们已经从当年 AT&T 的时代被拆分出来了。当时做电话线的人，对吧？他们是正式的南方贝尔技术员，他们开着拉风的卡车，拥有所有的设备。当他们开始转向高速互联网时，这意味着你必须真正去接触电脑，而我想作为一个工会，他们的态度是：听着，我们不碰电脑，我们甚至不进屋子。我们走到分界点，然后我们就停下。所以他们引进了承包商，而承包商的工作就是进来，做一些布线工作。所以如果你需要拉线，你就去拉。制作 Cat 5 规格的网线，你就去做。

<details>
<summary>Original English</summary>

**Kelsey**: Yeah. So, at that time, Bell South was, you know, the biggest telco uh probably in America. you know they had been broken up by that time from the AT&T days at that time the people who did phone lines right so those are the official Bell South technicians they drive the fancy trucks they have all the equipment and when they made the shift to highspeed internet that means you had to actually touch the computer and I think as a union they're like look we don't touch the computer we don't even go into the house we we get to you know the demark and we stop and so they had contractors come in and the contractor's job were to come in, have to do a little bit of wiring. So, if you had to run some cable, you did that. Create Cat 5 cables, you did that.

</details>

**主持人**: 哦，是的。你也做过这个，我最早的一份工作实际上也是布线。所以我还记得，我忘了确切的颜色代码了。

<details>
<summary>Original English</summary>

**Host**: Ooh, yeah. You you I one of my first jobs was actually cabling. So, I still I forgot the exact color code.

</details>

**Kelsey**: 橙白、橙、绿白、蓝、蓝白、绿，大概是这样。

<details>
<summary>Original English</summary>

**Kelsey**: Orange, green, white, green, blue, white, blue, something like that.

</details>

**主持人**: 现在它已经刻在你的脑海里了。

<details>
<summary>Original English</summary>

**Host**: It's burning in your head now.

</details>

**Kelsey**: 你知道的，所以无论需要做什么，你都得干。另一件你必须做的事是，你得打开电脑的机箱。你必须做出决定，对吧？如果他们的电脑足够新，他们可以使用 USB 调制解调器。那东西简直糟透了。它们总是坏，然后你就得总是上门维修。但对于一个新的安装订单，如果你真的想把工作做好，你会安装一个网卡 (NIC)，对吧？在他们的电脑背面装一个 Cat 5 端口。那个时候，我们说的可是 **Windows 98**。所以通常情况下，大概 20% 的概率，当你正在安装驱动程序时，电脑就会死机。现在你就面临一个全新的状况了。你现在必须排除故障，让这个东西重新上线或恢复正常运作。但如果一切顺利，他们就有了一张网卡，然后你再拿一个外置的调制解调器，把这个连接到电话线上，他们就有了高速互联网连接，然后你插上网线。这工作我大概做了一年。

然后我开始做企业的业务。所以你去人们的家里，就像挨家挨户敲门一样。然后当你去一家公司时，你会连接一台电脑，但显然那里有八台电脑，只有一台能上网。我记得那时候，你知道的，企业主，可能是一家小保险公司，他们会说：“嘿，我们怎么让其他电脑也连上网？” 第一次有人问我这个问题的时候，我心想：“我……我不知道啊伙计。我们只负责把这一台弄好。这是我的职权范围，对吧？” 但后来我决定：“好吧，让我去学学看。” 

我记得当时去了类似 Office Depot 的地方，对吧？他们卖电脑设备之类的地方。我走进店里问他们，我当时说：“哦，你们可以买一个这种 Linksys 路由器，对吧？” 就是那个臭名昭著的蓝色宇宙飞船模样的 Linksys 路由器。那些东西当时大概卖 50 块钱。我记得我直接买了一个，弄明白了如何让多台电脑共用一个网络连接。最终我觉得，听着，我不能在日常工作时间里做这个，因为我们必须完成规定任务然后离开，但这是我的名片。然后他们就会给你打电话。我记得我自己接的第一个独立安装单子。嗯，他们给我写了张支票，我当时说：“对，你们直接写支付给 Kelsey Hightower 就行。” 他说：“不，我们不把支票开给个人。我们把支票开给公司。” 我记得当时在现场，我就想：“哦天哪，我需要一个公司名字。” 我就随便编了一个：Digital Gateways（数字网关）。他们把这个写在支票上，我坐在那儿想：“所以，这玩意怎么兑现呢？” 

我去了银行，他们说：“先生，您必须去办营业执照。办了营业执照，您就可以以公司名义开展业务了。您必须这么做。” 所以，我在想，现在我 19 岁了。好吧，我得去弄个营业执照。必须把所有这些事情都弄清楚。所以我办妥了一切。我开了一个企业账户，就为了兑现那张支票。但在那一刻，我想：“哦，这个比那个（打工）赚得多。” 后来我变得非常擅长做这些网络安装。我也非常擅长排除故障，因为有时候有人给了他们一个 USB 调制解调器，打雷了，USB 调制解调器烧坏了，然后你就会去把它们换成网卡。

最终，我决定，我大概可以经营自己的业务了。我决定租个办公空间。所以我在亚特兰大郊外开了一家小电脑店。我会从分销商那里购买零件。我当时只有 19、20 岁。而且我买的量不足以真正有资格开一个批发账户。但幸运的是，我以前经常光顾的一家较小的电脑店向分销商推荐了我。就像是说，嘿，这是我们的人。他刚起步。于是他们给了我一个账户。我能够购买主板和显卡。人们会过来，比如他们带着孩子，拿着一张零件清单。我想要一台拥有所有这些配置的电脑，我们就组装机器，你知道，卖给他们，但同时它也是所有其他上门服务呼叫的总部。我做这个做了大概三、四年。

后来逐渐演变成同时在做的，现在我们说的是 2000 年、2001 年，许多音乐工作室正在从模拟设备和大型调音台转移到 **ProTools**，对吧？就是那种安装在机架上的小设备。他们都需要 Mac 电脑。他们都需要这些格式转换。所以我把这个也加入到了我的技能范围中。然后我在店里弄了一个小型的演示台，艺术家和音乐人走进来就会说：“嘿，我们工作室里就想要一个这个。” 然后我就接下了订单，把它加入了我可以提供的服务清单里。

<details>
<summary>Original English</summary>

**Kelsey**: And you know, so you did whatever it took. And the other thing you had to do was you have to open the computer. You have to make a decision, right? If they had a new enough computer, they can use a USB modem. Those were terrible. They always broke and you would always come out for a repair. Uh but for a new install, if you really wanted to do a good job, you install a a nick, right? Uh Cat 5 port on the back of their computer. And at that time, like we're talking Windows 98. And so usually, I don't know, 20% of the time as you're installing the drivers, the computer would crash. And now you have a whole another situation. You have to now troubleshoot getting this thing back online or back operational. But if everything went smoothly, they now had a network card and then you had an external modem that then you connected to, you know, the phone line and they had this high-speed internet connection and then you connected the network cable. And I did that for about let's say a year and then I started doing the businesses. 

So you go into people's homes like you're going door todoor and then when you go to a business you would hook up one computer but there's obviously eight computers there and only one of them has internet access. And I remember at the time, you know, the business owner, it could be like a small insurance company and they would say like, "Hey, how do we get all the other ones online?" And the first time someone asked me that, I'm like, "I I don't know, man. I don't." We put it on one computer like pay grade, right? But then I decided like, "Well, let me go learn." 

And that's when I remember like going to like Office Depot, right? They sell computer equipment and things like this. And I went in the store and I asked him, I was like, "Oh, you can get one of these Lynxys routers, right? infamous blue spaceship looking Lynxis router. And those things were probably like 50 bucks. And I remember just buying one and figuring out how to get multiple computers to to use one connection. And so eventually I was like, look, I can't do it as part of the job because we we have to do this and we have to leave, but here's my carp. And then they will call you. And I remember one of the first installations that I did on my own. Uh they wrote me a check and I was like, "Yep, you could just write it out to Kelsey High Tower." He was like, "No, we don't we don't write checks to people. We write checks to companies." And I remember right there on the spot, I'm like, "Oh man, I need a company name." And I just made one up digital gateways. And they wrote that on the check and I'm sitting there like, "So, how do you cash this?" 

So, I went to the bank and they're like, "Sir, you have to get a business license. The business license, you could just do business ads. You have to do this." So, I'm figuring out now I'm 19 years old. Like, okay, I got to go get a business license. Have to figure all this stuff out. So, I do everything. I open a business account just so I can cash the check. But at that point, I'm like, "Oh, this pays more than this does." And so, I got really good at doing those network installs. I really got good at troubleshooting cuz sometimes someone gave them a USB modem, lightning comes, the USB modem is fried, and then you would swap them out for a network card. 

And eventually, I decided like, I can probably do my own business. And I decided to get some office space. So, I opened a small computer store right outside of Atlanta. I would buy parts from the distributors. I was just like 19, 20 years old. And I wasn't buying enough to really qualify for an account. But luckily, one of the smaller computer stores I used to buy parts from gave a recommendation to the distributor. It's like, hey, this is our guy. He's just getting started. And they gave me an account. And I was able to buy motherboards and GPUs. And people would come over and like they bring their kid and they would have a parts list. I want a computer with all these things and we would assemble machines and you know sell them but also it was the headquarters for all the other service calls. I did that for like three, four years. 

you know, that ended up evolving into at the same time or now we're talking like 2000, 2001, a lot of the music studios were moving from analog gear and the large mixing boards to ProTools, right? The little rack mount unit. And they all needed max. They all need these conversions. So I added that to my uh abilities. And then I had a small setup in the store and artists and musicians would come in and say, "Hey, we want exactly that in our studio and I would get the order and I added it to the list of things I could do."

</details>

### 拥抱企业世界与进入谷歌

**主持人**: 我的意思是，在这一点上，你现在拥有了一家小企业。听起来进展顺利。然后突然你接受了一份作为员工的工作，也就是去谷歌。当我现在回看时，这件事是怎么发生的？到目前为止，这就像是，你知道，通常故事的走向会是：你成为一名企业家，你扩大你的业务，你顺理成章地发展下去。

<details>
<summary>Original English</summary>

**Host**: I mean, at this point, you now have a small business. Sounds like it's it's going well. And suddenly you take a job at an employee job at Google when I look back, how did that come up up to now? It's it's almost like this is like, you know, the story often times will continue. You become an entrepreneur, you grow your business, you you know, you just take it from there.

</details>

**Kelsey**: 甚至在那段时间里，作为那个店主，我还当过一名喜剧演员的经纪人，我们还一起去巡演。我有一个高中的哥们儿。他是个喜剧演员。结果证明他实际上非常擅长这个。我去了俱乐部看他的表演。他说，“嘿，我需要一个经纪人。” 我说，“你搞笑吗？我高中就认识你，但我不记得你搞笑到我会花钱听你讲笑话的程度。” 嗯，他说，“我今晚有场演出。” 于是我开车送他去了城市的北边。有趣的是，那是亚特兰大一个主要以黑人为主的观众群体。可以理解。他讲了这些笑话，观众都笑了，这是那种喜剧俱乐部之一，如果你不搞笑，大概 3 秒钟后他们就会嘘你下台，就这么完了。但他撑住了场子。我当时觉得，“哇，你竟然挺过了那一关。这太不可思议了。而且你确实挺搞笑的。” 

接着我们又向北开了一个小时的车，那里的观众主要是白人。在开车的路上，我心想，你绝对不可能在这个房间里讲那些同样的笑话。我得看看这会怎么收场。当时，他们付给喜剧演员的报酬大概只有 50 美元。所以，在早期你赚不了多少钱。他完全调整了整套表演内容，把那场观众也给震住了。我当时就说，“好吧，我可以做你的经纪人。我懂商业。我了解一些后勤物流。我知道怎么一起制定计划。”

我做了很多年。你知道他赢得了一些电视转播的比赛。我们跟着 Earth, Wind & Fire 这样的乐队以及《喜剧之王》(Kings of Comedy) 和《喜剧女王》(Queens of Comedy) 的一些大牌喜剧演员一起巡演，我实际上还通过其背后的公司 Latham Entertainment 接到了一些 IT 活儿。他们当时在制作电影。所以现在我觉得，你知道，我在为他们做这些，我还有小生意。我还带着喜剧演员。所以，听着，我确实攒下了不少钱，但天哪，幸好当时我 20 岁，因为我有无穷的精力，但我工作得非常多。

最终，你会安定下来，你会成家，你会算一笔账，事实证明人们有点过度美化创业精神了。我认为很多人相信它有巨大的上升空间，对吧？我们所谈论的那种软件公司的创业模式，它的上升空间是惊人的。但当你做的是销售零部件或服务业务时，除非你打算开很多家分店并且你知道你要扩大员工基数，否则它和软件公司不是同样的增长轨迹。所以我在做了四年之后算了一下。我说看，我想安定下来了。如果你以前创过业，你就会知道员工是先拿钱的，老板是最后拿钱的。有几个月你拿的钱很少，或者你根本拿不到钱，而现在你只能靠吃存款，因为这不是他们（员工）的问题。但我整体做得很好，我非常成功。但我记得就像是：“你知道吗？我觉得我准备好了。”

所以我四处看了看，**谷歌**在附近有数据中心，我觉得我的技能组合非常棒。我懂，你知道的，设备上架那方面的操作。我懂网络堆栈硬件层面的东西。我懂从 Linux 到 Windows 的所有东西。我具备企业家的思维方式。我觉得没有什么是我做不到的。我记得去参加那个面试，他们正在招聘数据中心技术员。薪水是多少？在我的脑海里，我想的是你只需要工作 8 小时。你不需要开任何发票，不管发生什么，你每两周都能拿到报酬。没有库存压力。这太疯狂了。他们怎么可能提供这样的条件。于是我去了，我记得参加那场面试时，我并不是很懂 Linux。幸运的是，我很懂 **FreeBSD**。在我回答问题的时候，我说，听着，我不是 Linux 专家，不是谷歌问这些问题想要的那种专家。就好像桌子对面的三个人在连珠炮似的发问。我记得我说，我懂 FreeBSD。我发誓我走运了。其中一个面试官，我想他的腿上有一个 FreeBSD 的纹身，那个小恶魔的标志。我看到了这个标志。我心想：“哦，我得救了。” 然后我们开始讨论 FreeBSD 的问题，我通过了，在这家数据中心得到了这份工作。

这很好，因为我觉得，嘿，我在和同事们一起工作，但感觉有点慢，因为你只有一份工作。你进来，做这件事。我在这方面变得非常熟练，因为对我来说，我把它看作一场比赛。谁是这里最好的数据中心技术员？他们的指标是什么样的？我如何超越他们的指标？我想学习如何在这个数据中心里做所有特定的事情，因为以前作为企业主，你拥有的技能越多，你就能赚越多的钱。然后我就开始每 3 到 6 个月换一次工作，因为我只想探索一切来积累我的能力。算一算，我想每一次跳槽都大概有 25% 的加薪。我的意思是，基础薪资很低，当时感觉并不多，但经过几次跳槽后，我的薪水翻倍了。

<details>
<summary>Original English</summary>

**Kelsey**: Even during that time as that store owner, I managed a comedian and we went on the road. And I had a buddy from high school. He was a comedian. Turns out he was actually really good at it. We even I went to go see him at a club. He's like, "Hey, I need a manager." I was like, "Are you even funny? Like I know you from high school, but I don't remember you being like funny enough that I would pay to see you tell jokes." And um he was like, "I have a show tonight." And so I gave him a ride on the north side of town. And the interesting part, it was a predominantly black audience in Atlanta. Okay, makes sense. And he did these jokes and they laughed and it was one of these comedy clubs where if you're not funny, you have like 3 seconds and they would just boo you off the stage and that's the end of it. And he held it. I was like, "Wow, you survived that. That's um that's incredible. And you were pretty funny." 

And then we drove about an hour north and the audience is predominantly white. And so on the drive there, I'm like, there is no way you can do those jokes in this room. I got to see how this is going to go. And at the time, they're only paying the comedians like $50. So, you don't make a lot in the early days. And he totally pivoted the set and he held that audience, too. And I was like, "All right, I can be your manager. I know business. I know kind of logistics. I know how to, you know, make a plan together." 

And I did that for a number of years. and you know he won some televised competitions. We went on the road bands like Earthwind and Fire and some large comedians from Kings of Comedy and Queens of Comedy and I actually picked up some IT work with the company behind it called Letham Entertainment. they had been doing movies at this time. And so now I'm like, you know, doing it for them and I got the small business. I got the comedian. And so, look, I was able to save a lot of money, but man, luckily I was 20 years old cuz I had all this energy, but I was working quite a bit. 

Eventually, you settle down, you get a family, and you do the math, and it turns out people kind of over glorify entrepreneurship. I think a lot of people believe there is tremendous upside, right? the type of entrepreneurship we talk about with software companies, the the upside is crazy. But when you're doing like selling parts or service business, unless you plan to open lots of stores and you know grow a larger employee base, it's not the same growth trajectory as software companies. And so I kind of did the math after four years of doing that. I said look, I want to settle down. And if you've been an entrepreneur before, you know employees get paid first, the owner gets paid last. And there are months where you get paid less or you don't get paid at all and now you're kind of drawing from savings because it's not their problem. But I did well overall like I did very successful. But I remember it's like you know what I think I'm ready. 

And so I looked around and Google had data centers nearby and I felt like I had a great combination of skills. I understood you know the racking stack part of the world. I understood the physical part of the networking stack. I understood everything from Linux to Windows. I had an entrepreneur mindset. I didn't think there was nothing I could not do. And I remember going to that interview and they were hiring like data center technicians. What it paid? And in my mind, I'm like that you only have to work for 8 hours. You don't have to issue any invoices and you get paid every 2 weeks no matter what. No inventory. This is crazy. No way they're doing this. And so I go and I remember doing that interview and I didn't know Linux that well. And luckily for me, I knew FreeBSD well. And as I'm answering the questions, I'm like, look, I am not an expert on Linux, not the way Google was asking these questions. And it's like three people on the other side of this table just rapper firing. And I remember I was like, I know FreeBSD. I swear I got lucky. This one of the interview, I think they had a FreeBSD tattoo on their leg, the little beasty logo. And I saw this logo. I'm like, "Oh, I'm saved." And so we started going down the FreeBSD questions and I pass and I get this job in this data center. 

And it was good because it's like, hey, I'm I'm working with my colleagues, but it felt a bit slow because you only get one job. You come in, you do this thing. And I got really good at it cuz to me, I kind of saw it as like a bit of a competition. Who is the best data center tech here? What are their metrics look like? How do I exceed their metrics? I want to learn how to do every particular thing in this data center because previously as a business owner, the more skills you have, more money you can make. And then I just started switching jobs every 3 to 6 months because I just wanted to explore everything to just amass my abilities. And doing the math, I think every jump was like a 25% pay raise. I mean, coming from a small base, it wasn't it didn't feel big at the time, but after a few jumps, my salary doubled.

</details>

**主持人**: Puppet 是你职业生涯中的一个转折点。

<details>
<summary>Original English</summary>

**Host**: puppet was uh was a a bit of an inflection point in your career.

</details>

**Kelsey**: 你知道吗，我想说我职业生涯中最大的转折点是，在进入 Puppet Labs 之前，有两个转折点。

<details>
<summary>Original English</summary>

**Kelsey**: You know what and I would say the biggest inflection point in my career was there were two of them before I get into Puppet Labs.

</details>

**主持人**: 好的。

<details>
<summary>Original English</summary>

**Host**: Okay.

</details>

**Kelsey**: 首先是你来到谷歌，你看到了这种庞大的运营规模。那里有几十万台服务器。线缆完美无瑕，一尘不染。

<details>
<summary>Original English</summary>

**Kelsey**: So you come from Google, you see this huge operations. There's hundreds of thousands of servers. The cables are perfect. They're immaculate.

</details>

### 谷歌数据中心的故事

**主持人**: 哦，顺便问一下，你能帮我们想象一下当时谷歌的数据中心是什么样子的吗，你作为工作的一部分都做了些什么？

<details>
<summary>Original English</summary>

**Host**: Oh, by the way, can you help us imagine like what a data center back then looked like at Google and and what what did you do as as part of the job?

</details>

**Kelsey**: 是的。所以在 2004 也许 2005 年，那个数据中心就像一个仓库。我的意思是，它非常巨大。所以想象一个地方，我敢肯定他们总是夸大数字。所以夸张的数字是，想象在一个地方有 20 万台服务器。一切都完美无缺。许多人曾在数据中心工作过，那里一团糟。电线到处都是。你知道，你会临时添加和移除服务器。但谷歌是系统化的。那些机器从卡车上卸下来。它们被完美地包装着。当你把它们推到指定位置时，你接上网线，它们就会进行 PXE 启动。它们会进行老化测试。所以工作的一部分是，你知道，你推着一辆维修推车 (crash cart) 走来走去。所以根据你的能力，有些人的工作相当简单。你有一辆维修推车，上面放着你所有的工具，你走来走去，寻找需要维修的机器。

如果你有 20 万台机器，就算有 300 台坏了也没关系，对吧？系统可以绕过它路由。但如果它们坏了，它们就需要被修理。所以你会去 7 号机架，把它拉出来，你会看着它，哦，是的，SATA 控制卡起火了。它确实被烧坏了。所以你会说，我用眼睛就能诊断这个。这需要更换 SATA 卡。但问题是，你必须在系统里记录，你说，这个 SATA 控制器需要更换。所以你要做出你的预测，然后你要更换它，让它经过老化测试。它会重新加入集群，然后衡量你的标准是，你的预测有多准确。

所以你说是 SATA 控制器，而对我来说追求速度，你看似乎我觉得那就是 SATA 控制器，我不打算在这台机器上浪费更多时间了，因为我想提高我的指标数字。所以我直接更换了 SATA 控制器。你插上所有线缆，把它推回去，它进入流程，你就继续处理下一台机器，在此之前你还没拿到反馈。

有趣的是，有个叫蒂姆·霍金（**Tim Hockin**）的人，他在 Kubernetes 社区非常有名。他就像是网络负责人。在那个时候，Tim Hockin 还在谷歌的另一个部门工作，也就是谷歌更大的那个部门。他的首批项目之一是构建一个小工具，你可以把它插在主板上。它大概有九个灯，那些灯会来回闪烁，它会告诉你哪些内存插槽可能有问题。那些速度快的技术员，他们不会浪费时间，比如运行一个程序来对内存进行深度测试。你学会了如何使用这个小设备，你会走到主板前。所以我会在做任何事情之前，把这个插在主板上，获取读数，随着时间的推移，我学会了信任它：插槽一、插槽二坏了。接下来的目标就是，好吧，我推车上有很多内存。你把那两个插槽的内存换掉。确保先做完这一步。重启机器。你可能会觉得，我想这是唯一的问题了。再次重申，你要把这个输入到系统中：我认为我只需要更换内存插槽一和二。

然后，衡量你的标准是，那台机器需要多长时间才会被再次退回维修。所以如果它在，我不知道，30、60 天内没有被退回，你干得就不错。如果退回了，你的分数就会很低。所以，对于那些行事鲁莽的技术员，对吧？他们甚至连试都不试，只是一通乱换零件。你换错了硬盘。所以你处理的东西总是被退回来维修。你的效率就不高。所以我达到了这样的水平：我可以保持在 90 分以上的高分，同时还能比别人多修三倍的机器。就是维修大量机器，但返修率很低。然后我学会了如何处理网络交换机。然后还有电源审计，你要掀开地板上的瓷砖，确保一切看起来正常。你必须小心不要碰到它们，因为你可能会丧命。所以你了解了数据中心的一切，比如服务环 (service loop)。你知道你布设了所有的 Cat 5 网线，它必须有一个完美的服务环。光纤走在机架的不同部分，对吧？所以你绝对不能把这些东西混在一起。因此，作为一个还在 20 岁出头的人，我以为所有的数据中心都是这样的。并非如此。

<details>
<summary>Original English</summary>

**Kelsey**: Yeah. So in 200 maybe four maybe 2005 that data center is like a warehouse. I mean it's huge. So think about a place where and I'm pretty sure they always exaggerated the numbers. So exaggerated number to think about is like think about 200,000 servers in one place. Everything is immaculate. So a lot of people have worked in data centers and it's a mess. Wires are all over the place. You know you're ad hoc adding and removing servers. But Google was systematic. Those machines came off a truck. They were wrapped perfectly. When you wheeled them into their spot, you connected the network cables, they would pixie boot. They would burn in. So part of the job was, you know, you walked around with a crash cart. So depending on what your abilities were, some people had pretty straightforward jobs. You had a crash cart, had all your tools on it, and you would walk around and you would find machines that were needing of repair. So if you have 200,000 machines, it's okay if like 300 of them are broken, right? the system can route around that. But if they were broken, they needed to be repaired. So you would go to rack a server 7, you will pull it out and you will look at it and oh yeah, the SATA card is on fire. Like it's literally burned. It's burning. It was burnt. And so he's like, I can diagnose this one with my eyes. It needs to replace the SATA card. But the thing is, you would go into the system and you would say, this SATA controller needs to be replaced. So you would be making your prediction and then you would replace it and you would go through its burn-in process. It would join back to the fleet and then the way you were measured was how good were your predictions. 

Oh, right. So you said it's a SATA controller and to me moving fast you look as if I think that SATA controller I'm not going to waste any more time on this one because I'm trying to get my numbers up. So I just swap the SATA controller. You bring in all the cables, you slide it back, it goes through his process, and you move on to the next machine before you get the feedback. 

Yeah. And fun fact, there's a guy named Tim Hawk is very popular in the Kubernetes community. He's like the network lead. So back then, Tim Hawkins is working at the other side of Google, like the bigger side of Google. And one of his first projects was built a little tool that you would put on the motherboard. It had about nine lights on it, and the lights would flash back and forth, and it would tell you what dim slots were potentially bad. The technicians that were fast, they didn't waste time like running a program to do a extensive test of the memory. You learn how to use this little device and you would walk up to the motherboard. So the thing I would do is like before I do anything, put this on the motherboard, get the reading, and I learned to trust it over time, dim one, dim two are bad. And the goal would be all right, I have all this memory on my cart. You swatch those two dim slots. Make sure that that's done first. Reboot the machine. And you might be like, I think that's the only thing wrong. And again, you were put in the system. I believe I only need to do DIM one and two. 

And then the way you were measured is how long before that machine gets kicked back to repair. So if it doesn't get kicked back within, I don't know, 30, 60 days, you did a good job. If you didn't, your scores would be low. So for the technicians that were just reckless, right? They wouldn't even try and you're just swapping the wrong part. You're swapping the wrong hard drive. And so your stuff is always coming back for repair. You were not efficient. So I got to the point where I can maintain high 90s but also repair let's call it three times more machines than other people. So lots of machines rate of return. And then I learned how to do the network switches. And then there's power audits where you're lifting up tiles from the floor and you're making sure that everything looks good. You got to be careful not to touch them because you could die. And so you learn everything about a data center like the service loop. You know you're running all this cat 5 cable and it has to have a perfect service loop. fiber runs on a different part of the rack, right? So you don't ever mix these things. So as a person still like I'm in my early 20s. I'm thinking this is how all data centers look. It's not the case.

</details>

### 数据指标与自动化运维启蒙

**主持人**: 但回顾过去感觉很疯狂，你知道，我也当过经理，当然也做过很长时间的软件工程师，但在那里，你的表现是如此持续地被衡量并反馈给你，而且你是基于此被评估的。这感觉要比，怎么说呢，比如包括谷歌在内的软件工程师的工作，要严格得多。我的意思是其反馈频率和期望值。

<details>
<summary>Original English</summary>

**Host**: But it's it's crazy because just as I think back, you know, I was a manager before as well and of course a software engineer for a long time, but the way your performance was continuously measured and fed back to you and you were evaluated based on it. It feels way more strict, should I say, than you know like folks who work as software engineers including at Google. I mean the frequency, the expectations.

</details>

**Kelsey**: 为什么我没有觉得现在的某些指标像别人说的那么糟糕，因为我觉得我可以控制结果。感觉上它不仅仅是一个毫无作用的衡量数据。如果我觉得我的分数受到影响，我会觉得，你知道吗，我在诊断这些机器时确实有点草率了。我记得有一次我的分数差点跌破 90 分。我开始编写额外的 Shell 脚本，开始把不同的功能组合在一起。这就像是，你知道吗？不能再这么一味图快了。我有一种方法可以同时诊断机器的多个部件。所以，我会在处理内存组件的同时诊断 SATA 阵列和所有的硬盘。然后当机器重启时，我会在把推车收拾好的同时再跑一次脚本，以捕捉剩下的那个问题。一旦我开始这么做，我就可以随心所欲地提高速度，而且分数也很好。

所以对我来说，当分数实际上与你正在做的事情相匹配时，这就是一种健康的反馈。而且再说一次，除非需要谈论，否则没人真正去谈论分数。所以我有点把它当成个人的工具了。我早上把它拉出来。我看看我的表现指标，在很多方面，我是基于我得到的这个详细的反馈来调整我的策略的。所以我认为当时我很欣赏那种级别的细致度，因为它感觉像是对我有帮助的东西，而不仅仅是对我的经理有帮助。

<details>
<summary>Original English</summary>

**Kelsey**: The reason why I didn't feel as bad as some of the metrics people are using now is because I felt like I can control the outcome. It didn't feel like it was a thing that was just a metric that didn't do anything. If I felt like my score was taking a hit and I was like, you know what, I am being a bit sloppy and how I'm diagnosing these machines. And I remember one time where I almost had my score dip below 90. I started writing additional shell scripts to starting combining different functions together. It's like, you know what? Can't be moving this fast. There's a way for me to diagnose multiple things of the machine at one time. And so, I would diagnose the Saturn array, all the hard drives while I'm doing the memory component. And then when it rebooted, I would just run the script one more time as I'm putting my cart back together to catch that one more thing. And once I started doing that, I can move as fast as I want it and the scores are right. 

So to me, when the scores actually match the things that you're doing, then it's a healthy feedback. And again, no one really talked about it unless you needed to talk about it. And so I kind of leveraged it for a personal thing. I pulled it up in the morning. I kind of looked at my performance metrics and in many ways I calibrated my strategy based on this detailed feedback that I was getting. So, I think I appreciated that level, that granularity back then because it felt like it was uh something that was helpful for me, not just my manager.

</details>

**主持人**: 你刚才说你有两次大的转折点。其中一个是……

<details>
<summary>Original English</summary>

**Host**: And you said you had two two kind of big big inflection points. One of them was

</details>

**Kelsey**: 谷歌是一个。还有自主创业。当我进入网络托管行业时，我去了那家名为 **Peer 1** 的公司。他们是 **Rackspace** 拆分出来的，主打全自动自主托管，对吧？

<details>
<summary>Original English</summary>

**Kelsey**: Google was a big one. Like that was definitely one of course my entrepreneurship. And when I got to web hosting, I went to a company called Pier 1. They're a spin-off of Rackspace and they were all about fully automated self-hosting, right? So,

</details>

**主持人**: 这大概是在 2005、2006、2007 年左右？

<details>
<summary>Original English</summary>

**Host**: this was back in like what 2005 67?

</details>

**Kelsey**: 是的。大概是在 2005、2006 年。哦，那时他们已经主打这个了。他们的口号是“延迟致命” (Latency kills)。所以在那个时候你上网。很多客户群体是，比如，那些自己托管游戏服务器的人，对吧？如果你想玩游戏，那时你能做的一件事就是托管一台游戏服务器，但你需要一个多人都能连接的游戏服务器。所以你就会上网去 ServerBeach。这是 Rackspace 拆分出来的。Rackspace 的模式更像是，你知道的，我们买一台服务器，一旦你拿到了它，还有很多手动步骤。ServerBeach 更偏向于“让我们自动化一切”。所以机器进行 PXE 启动，一些 PHP 脚本就会运行。如果你订购了 RAID 设置，我们就会在机器网络启动时配置 RAID，然后我们会把你放在你应该在的 VLAN 上。我们会根据你的订单安装正确的操作系统，我们只需获取一个表单。我们经历所有这些步骤，然后当我们完成后，这大概需要一个小时。当我们完成后，你就拥有了一个 IP 地址、登录凭证，如果你需要电子邮件以及网站管理之类的东西，这些也都有了。当你用完后，你把它退还回来，然后我们把它放回资源池里，为下一个客户做好准备。

所以当我看到我们是如何做到这一点的时候，我当时想，哟，这还不错。你可以端到端地实现一切自动化。而且这里重要的一点是，我们还在更新 RAID 控制器的固件等，因为一旦你让服务器进行 PXE 启动，现在你就进入了内存之中，你可以访问所有的硬件。你还没有挂载真正的操作系统，但你拥有的权限足以做你想做的任何事。所以如果你想配置 RAID 控制器，那时候还没有什么清晰的 API，我们真的是在运行 Curl 脚本和命令行工具，试图让这台机器达到正确的状态，并且……

<details>
<summary>Original English</summary>

**Kelsey**: Yeah, this is like Yeah. 2005, 2006. Oh, they were already about that was their thing. Their tagline was latency kills. And so back then you would go online. A lot of the customer base was like um people hosting their own game servers, right? So if you wanted to play a game, one thing you could do back then is host a game server, but you needed a game server that multiple people could hit. And so you would go along to server beach. So this is a spin out of Rackspace. So Rackspace is more like, you know, we'll buy a server and once you get it and it's a lot of manual steps. Rackspace was more of a let's automated everything. So the machine would pixie some PHP scripts would run. If you ordered a RAID setup, then we would configure the RAID while the machine was net booted and then we would put you on the VLAN that you belonged on. We would install the right operating system based on what you've ordered and we just took a form. We just went through all of these steps and then when we were done, and it took maybe about an hour. When we were done, you had an IP address, login credentials, and if you wanted email and plus, you know, website management, all these things, you got it. And when you were done, you gave it back and then we put it back into the pool ready for the next customer. 

And so when I saw how we were doing that, I was like, yo, this is okay. You can automate things end to end. And the other thing that was important here, we were doing things like updating the firmware for RAID controllers because once you pixie a server, now you're in memory and you have access to all the hardware. You haven't committed to an operating system yet, but you have enough to do whatever you want. So if you want to configure the RAID controller and back then there wasn't like clean APIs. We were literally running curl scripts and command line utilities trying to get this machine into the right shape and

</details>