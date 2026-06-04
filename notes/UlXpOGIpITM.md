---
author: The Pragmatic Engineer
date: '2026-06-03'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=UlXpOGIpITM
speaker: The Pragmatic Engineer
tags:
  - career-path
  - tech-industry
  - kubernetes
  - professional-growth
  - ai-impact
title: Kelsey Hightower：从快餐店打工到Google杰出工程师的传奇之路与技术洞察
summary: 本期访谈深入探讨了Kelsey Hightower非传统的职业路径，涵盖了从PC维修、创业到Google技术专家的成长历程。他分享了Kubernetes成功的核心原因，探讨了工程师在AI时代的职业规划，并强调了务实心态与持续学习的重要性。
insight: ''
draft: true
series: ''
category: career-development
area: work-career
project: []
people:
  - Kelsey Hightower
  - Satya Nadella
companies_orgs:
  - Google
  - Microsoft
  - Docker
products_models:
  - Kubernetes
  - Docker
  - Terraform
  - Puppet
media_books: []
status: evergreen
---
### 播客精彩片段预告

**主持人**: 你认为真正让 **Kubernetes** 取得突破的原因是什么？

<details>
<summary>Original English</summary>

**Interviewer**: What do you think really made Kubernetes breakthrough?

</details>

**Kelsey Hightower**: 排名第一的成功标准是 **Docker**。现在，你不需要再讨论 Java、Python 还是 Ruby 之间的对比，你只需要讨论调度 Docker 容器。我们一开始就处于领先地位，因为你可以直接重用相同的 Docker 容器。我还记得我收到了微软 CEO Satya 的一封邮件，我当时想，天哪，他写了这封友好的邮件，然后我打开了一个 PDF，发现薪水方程里多加了一个零。你看着这个会想，我甚至都不知道他们会这样做。我们知道这种事会发生，但在 1999 年高中毕业、选择了 A+ 认证的那个人，并不知道有这种机会。所以，我当时是真的认真考虑去微软的。我并不是一个生成式 AI 讨厌者。我只是不喜欢对它那种天真的推广和采用。我认为它应该更有战略性。因为我把生成式 AI 看作是一个工具，而不是伟大的人类替代品，那么我就可以用更务实的方式来使用它。而且当涉及到 AI 时，在这个会议开始之前我唯一会做的一件事就是，不要提 AI。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: The number one success criteria was Docker. Now instead of talking about Java versus Python versus Ruby, you only have to talk about scheduling Docker containers. We were already off to a running start because you could just reuse the same Docker containers. And I remember I get this email from Satia, the CEO of Microsoft, and I'm like, man, he wrote this nice email and I open a PDF and there's a zero get added to the equation. And so you're looking at this like, I didn't even know that they do that. We know that it happens, but the person that graduated from high school in 1999 that chose the A+ certification didn't know that was available. So, I was serious about going to Microsoft. I'm not just like a Genai hater. I just don't like the naive promotion and adoption of it. I think it should be way strategic. And since I think about Genai as a tool versus the great human replacement, then I can use it in way more primatic ways. And when AI is involved, the one thing I just do before the thing kicks off in this meeting, do not say AI because...

</details>

### 开场白与背景介绍

**主持人**: Kelsey Hightower 被誉为 Kubernetes 社区中最具影响力的声音之一，但你很难猜到他的职业生涯是如何开始的。19 岁时，他从大学辍学，成为一名 DSL 调制解调器安装员，后来成为一名自学成才的开发者，并最终成为 **Google** 的杰出工程师。43 岁时，他在行业的最顶峰退休。今天我们将探讨 Kelsey 步入科技界的非传统路径，以及他如何（往往在不知不觉中）不断为自己创造新机会。容器战争、**Puppet**、Docker、**Terraform**、**CoreOS** 的内幕故事，以及 Kubernetes 最终是如何胜出的。从一名 Google 的独立贡献者（IC）成长为高管级别，以及他是如何拒绝微软 CEO Satya Nadella 亲自发出的邀请，却依然让自己的薪水翻倍的。对于那些担心被 AI 商品化的软件工程师，他给出了接地气的务实建议，还有更多精彩内容。如果你是一名正在思考长期职业发展轨迹的工程师，无论是想晋升到 Staff+ 级别、走向独立，还是甚至在悄悄计划离开这个行业，这期节目都是为你准备的。坦率地说，这期节目比正常的节目要长，因为我大部分时间都紧紧地贴在椅子上，听着 Kelsey 的故事并陷入思考。本期节目由 **Antithesis** 赞助播出。无需人工审查或传统的集成测试即可验证系统的正确性，避免 bug 或宕机。在开始之前，我想提一下我们的展示赞助商 Antithesis，并顺便讲一点历史。在过去的二十年里，软件开发经历了一次思维方式的转变，从命令式（imperative）方法转向了声明式（declarative）方法。基础设施就是一个完美的例子。想想像 Puppet 和 Ansible 这样的工具是如何允许声明单个服务器应该如何配置的。然后出现了 Terraform，它能够声明整个基础设施（服务器、网络、数据库及其相互关系）的期望最终状态。接着随着 Kubernetes 的出现，我们不再编写容器生命周期的脚本。相反，我们编写清单（manifests），声明诸如“我希望在这个服务后面暴露这个应用程序的副本，并配置这么多 CPU 和内存”这样的内容。一旦我们不再需要具体说明基础设施的每一个小细节，部署软件的速度就变得快得多了。但随后的瓶颈变成了我们能多快地测试和验证要部署的代码。测试仍然是命令式的。我们必须为每一个小细节编写测试。而现在有了大语言模型（LLMs），我们在代码编写方式上也处于声明式转变的边缘。只需告诉模型你想要什么，让它去搞定细节，而这将会让验证瓶颈变得严重一百万倍。Antithesis 是一个声明式的测试工具，能够跟上你的 AI 编码代理的步伐。你声明你希望软件具有的属性，Antithesis 会帮你找出如何检查它们。以代理编写代码的速度验证你的代码，并带着极大的信心发布。前往 antithesis.com/pragmatic 了解更多。

<details>
<summary>Original English</summary>

**Host**: Kelsey High Tower is known as one of the most influential voices in the Kubernetes community, but you wouldn't guess from how his career started. At 19, he dropped out of college to be a DSL model installer, became a self-taught developer, and still went on to become a distinguished engineer at Google. At age 43, he then retired at the very top of the industry. Today we cover Kelsey's unconventional path into tech and how he kept creating new opportunities for himself often unknowingly. The inside story of the container wars, puppet, Docker, Terraform, Coros and how Kubernetes eventually won. Going from a Google IC to executive level and how he rejected a Microsoft offer from Sachio Nadella himself and still doubled his compensation. His grounded on pragmatic advice for software engineers worried about being commoditized by AI and so much more. If you're an engineer thinking about your long-term career trajectory, whether that's getting into a staff plus level, going independent, or even quietly planning to leave the industry, this episode is for you. This episode is longer than a normal episode, frankly, because I was so glued to my chair, mostly listening to Kelsey's stories and thinking. This episode is presented by Anticys. Verify your systems correctness without human review or traditional integration tests and avoid bugs or outages. Before we start, I'd like to mention our presenting sponsor, Antithesis, and maybe offer a little history lesson. Over the last two decades, software development has gone through a mindset shift from an imperative approach to declarative one. Infrastructure is a perfect example. Think about how tools like Puppet and Ansible allow declaring how individual servers should be configured. Then came Terraform, the ability to declare the desired end state of your whole infrastructure, servers, networks, databases, and their relationships. And then with Kubernetes, we stop scripting container life cycles. Instead, we write manifests that say things like, I want the replicas of this application exposed behind a surface with this much CPU and memory. Once we didn't have to specify every little detail of our infrastructure anymore, deploying software became much faster. But then the bottleneck became how quickly we could test and verify the code to be deployed. Testing remained imperative. We had to write tests for every little detail. And now with LLMs, we're on the verge of a declarative shift in the way code is written as well. Just tell the model what you want and let it figure out the details, and it's going to make the verification bottleneck a million times worse. Anthesis is a declarative testing tool that can keep up with your AI coding agents. You state the properties you want your software to have, and antithesis figures out how to check them for you. Verify your code as fast as agents can write it and ship with Growlin confidence. Head to insys.com/pragmatic.

</details>

**主持人**: Kelsey，欢迎来到播客。很高兴能见到你本人。

<details>
<summary>Original English</summary>

**Host**: Kelsey, welcome to the podcast. It's so nice to see you in person.

</details>

**Kelsey Hightower**: 是的，我其实很高兴能来这里，主要是因为这些年来我一直有关注你的内容。所以，很荣幸也能来到阿姆斯特丹。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: Yeah, I'm actually happy to be here mainly because I kind of look at your stuff over the years. So, it's honor to be here in Amsterdam as well.

</details>

### 第一份工作与早期责任感

**主持人**: 你的第一份工作是如何赚到第一块钱的？

<details>
<summary>Original English</summary>

**Host**: How did you make your first dollar at a job?

</details>

**Kelsey Hightower**: 哦，我工作赚到的第一块钱是在麦当劳，对吧？那也算数。在高中时，你通常会找离你最近的工作。所以，那份工作离我家只有步行距离。我一到法定年龄，嗯，14岁，就拿到了工作许可证。我去了那里，那是一种你当天去填申请表，通常当天就能得到回复或者直接被录用的工作。他们问我什么时候能开始？我说，就现在。他们就去后面给你拿了件衬衫。你穿多大码？嗯，男士大码。那份工作我喜欢的一点是，你在与真实的人打交道，而他们都很匆忙。我想这份工作不好的一点是，很多人并不尊重做这份工作的人。所以他们看你就像是看着他们和他们想要的东西之间的一个中间媒介。但像那样的餐厅里有很多门道。它非常高效。嗯，你知道，人们是有期望的。而我学会了如何运营整家店。所以，到我 15 岁时，我已经是助理经理了。所以在晚上和周末，你知道的，其他经理会离开。他们会把钥匙交给这个 15 岁的孩子。我懂得如何处理那里的一切事务，包括关店，对吧？所以你必须清点所有的钱。每天晚上你还得把一张巨大的电子表格传真给公司总部。然后我妈妈会来接我。所以，在那个年纪就能学会如何真正承担起即使是对成年人来说也很重要的责任，这真的很棒。这就是我赚到第一块钱的方式。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: Oh, my first dollar at a job McDonald's, right? That counts. So, in high school, you get the job that's closest to you. So, it was in walking distance of my house. As soon as I turned legal age, uh 14, get a work permit. And I went there and it was one of those jobs where, you know, you go, you fill out the application the same day. You typically get your information or you're going to get hired the same day. When can you start? I'm like, right now. They go get a shirt for you in the back. You What size do you wear? Uh, men's large. And the one thing I liked about that job is you're dealing with real people that are in a hurry. I guess one bad part about the job, you know, a lot of people don't respect people who have that job. So, they kind of look at you as just like this intermediary thing between them and what they want. But there's so many things that go into a restaurant like that. It's very efficient. Um, you know, people have expectations. And I learned how to run the whole store. So, by the time I turned 15, I was a assistant manager. So, nights and weekends, you know, other managers would leave. They would give this 15-year-old the keys. And I knew how to do everything there, including close out the store, right? So, you have to count all the money. You have to fax this huge spreadsheet to corporate every night. And then my mom would pick me up. And so it was really good learning how to really be responsible even for adults at that age. So that's how I got my first dollar.

</details>

### 初探编程与科技世界

**主持人**: 你是如何进入科技行业的？你是如何接触到编程的？

<details>
<summary>Original English</summary>

**Host**: How did you get into tech? How did you get into programming?

</details>

**Kelsey Hightower**: 在高中时，因为我从加州搬到了亚特兰大。所以对吧，你从这个国家的一端搬到了另一端。嗯，我大概错过了 3 到 6 个月的课程，为了能按时毕业，我必须多修一些课。作为一个参加体育运动、练田径、打橄榄球、打篮球的人来说，当时有这种计算机编程……不是，你知道的，计算机俱乐部、技术学生协会。这其中包含课堂部分，还有课后的部分。我当时想，我不知道，伙计。这些计算机的东西是给那些……你知道的，我正努力想当个酷小孩。但我确实做了一件事，我非常喜欢它，对吧？我对 **AutoCAD** 产生了兴趣。我甚至参加了 AutoCAD 的州级比赛。我们开车去那里参加比赛。他们给你一个任务，你坐在电脑前。那是我第一年参加，但我真的很喜欢这种感觉：接受一个规范说明，进行设计，如果我能让产品真正运作起来，我可能会拿到第一名，因为你还必须把它打印出来，以便评委们审查你的作品。所以我拿了第二名，尽管我并没有完全搞定。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: In high school since I moved from California to Atlanta? So right, you're going from one side of the country to another side of the country. And uh I missed maybe 3 to 6 months of school and in order to graduate on time, I had to take some extra classes. And so as someone who played sports, ran track, uh played football, played basketball, and it's like, you know, there's this computer programming not, you know, computer club, technology student association. There was a class component and then there was after school component. And I was like, I don't know, man. This computer stuff that's for the, you know, you know, I'm trying to be a cool kid. But the one thing I did, I really enjoyed it, right? So I I had a liking to AutoCAD. I even competed at the state level in AutoCAD. So we we drove down and you compete. They give you a task and you sit in front of the computer. It was my first year doing it, but I really like the idea of like taking a specification, designing it, and I probably would have gotten first place if I would have got the product to work because you also have to print it out so that the judges can review your work. So I got second place even though I didn't.

</details>

**主持人**: 这是指 3D 建模吗？

<details>
<summary>Original English</summary>

**Host**: This is the 3D modeling.

</details>

**Kelsey Hightower**: 是的。AutoCAD，你知道的，就是 AutoCAD。对。课程的一部分是，你知道，你设计桥梁。我们和一个团队做过一个项目，里面涉及盾徽，你会像在进行辩论一样。所以你学到了所有这些与商业相关的知识，但 CAD 是我最喜欢的东西之一。同样在那门课上，我的一个同学教了我 **TI-BASIC**。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: Yeah. AutoCAD, you know, just AutoCAD. Yeah. So part of the curriculum was, you know, you build bridges. We did this thing with um chapter team where you know you have a code of arms and you're kind of doing like a debate. Do you kind of learn all of these things uh related to business but CAD was one of the things I like most? Also in that class one of the classmates taught me TI basic.

</details>

**主持人**: 那是 BASIC 的一个版本吗？

<details>
<summary>Original English</summary>

**Host**: Is that a version of of basic?

</details>

**Kelsey Hightower**: 嗯，所以 TI-BASIC，你知道的，就是那种图形计算器，比如 **TI-86**。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: Well so TI basic so you know the graphing calculator it's like a TI86.

</details>

**主持人**: 哦，对。

<details>
<summary>Original English</summary>

**Host**: Oh yeah.

</details>

**Kelsey Hightower**: 你可以对它进行编程。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: You can program it.

</details>

**主持人**: 哦，对。

<details>
<summary>Original English</summary>

**Host**: Oh right.

</details>

**Kelsey Hightower**: 所以在课上他们说，嘿，你知道这不是一个普通的图形计算器，你实际上可以对它编程。我当时想，那是什么？他们说看，我们可以，你知道，那时你会编写贪吃蛇游戏，对吧？基本上就是找一本杂志，复制粘贴代码，然后运行它，现在你就在玩基于你自己写的代码的贪吃蛇了。你会玩味这个概念，所以那可能是我对编程的第一次接触，字面意义上的对我的 TI-86 计算器进行编程。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: So in class they're like hey you know it's not just a graphing calculator you can actually program it. And I was like what's that? And it's like look we can you know every at that one at that time you would create the snake game right so it's basically get a magazine copy and paste the code and then you run it and now you're playing snake uh based on the code you wrote and so you would toy around with this concept so that was probably the first introduction to programming was literally programming my my TI86 calculator.

</details>

### 大学教育与寻找替代路径

**主持人**: 高中毕业后，你上了大学还是考虑过上大学？

<details>
<summary>Original English</summary>

**Host**: And after high school did you go to college or you considered college right?

</details>

**Kelsey Hightower**: 我考虑过上大学，因为在乔治亚州，当时以及现在都有一个叫 **HOPE 项目**（HOPE program）的东西。如果你有 B 级或以上的平均成绩，你可以免费去任何一所公立学校。乔治亚州的公立学校包括佐治亚理工学院（Georgia Tech）、佐治亚州立大学。这些都是非常好的大学。它们非常好。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: I considered college because in Georgia at the time and still today there's a thing we're called the hope program. So if you have a B average or above, you can go to any public school for free. And public schools in Georgia include Georgia Tech, Georgia State. These are pretty good universities. They're really good.

</details>

**主持人**: 所以你决定去了离你近的一所。

<details>
<summary>Original English</summary>

**Host**: And so you decided to go to one that was near me.

</details>

**Kelsey Hightower**: 头两个星期我想，嗯，这太慢了。这不……这不是我想要的前进节奏。另外请记住，我毕业的那年是 1999 年。所以当你打开电视时，人们正排队购买下一个版本的 Windows。到处充满了狂热。AOL 开始逐渐退出舞台，我们开始接触高速互联网。我当时想，哟，看看这个发展速度，而且你听到了各种说法。比尔·盖茨从大学辍学了。这些人不再必须将学位美化了。一切都关乎技能。但对我来说不幸的是，我不认识任何做程序员的人。我不认识任何系统管理员，因为在那个时候，所有的系统都还是像 Sun Microsystems 或 IBM 巨型机那种，这些仍然是企业里的东西。所以当我查看招聘职位时，我看到了很多我甚至不知道如何获取的技能要求。因此，我没有去上大学，你知道我当时还在做快餐行业，在那时的必胜客送披萨。我记得去了一家书店，他们有 **A+ 认证**指南，我看了看，有些招聘启事上写着：“嘿，你需要有 A+ 认证才能胜任这个支持职位或其他什么职位。”我当时想，“你知道吗？这不需要上大学。这本书只要 35 美元。”我记得买了那本书，这是一个官方的认证过程。它看起来像是就业市场的一部分。我记得买了那本书，一遍又一遍地从头读到尾。你在学习所有的基础知识，对吧？你在学习关于主板、内存以及所有这些东西是如何工作的，有一个操作系统部分，然后在书的后面有一个小型的模拟考试。所以对于像我这样的人来说，有这种快速反馈循环——你把 CD 放进去，参加考试，尽管那是多选题，你总觉得如果做错了什么，你只要回到书里确保你理解了那里的内容，然后再去考一次。它有一点随机性，所以你不能仅仅依靠死记硬背所有东西。我记得去考试中心参加考试，你知道你在那个小房间里，他们想确保你不作弊。所以有个摄像头指着你，你就一直做题。这些考试的好处是没有陷阱题。你要么知道，要么不知道。我想他们可能给了你一个小时，一个半小时。我记得我在 10 分钟内就做完了那东西。当我走下来时，你知道，你在等待，拨号网络连上了，他们计算了你的分数并说：“嘿，你通过了。”然后你走出去，你就是 A+ 认证的了。那是我职业生涯中第一次感觉到，哦，所以如果你付出了努力，你就能获得证书。当我拿到那个证书后，我记得有一个招聘会，上面写着，嘿，任何有 A+ 和 Network+ 认证的人，都可以成为在那个时候帮人们把拨号上网替换成 DSL 的承包商团队的一员。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: The first two weeks I was like, um, this is too slow. This is not this is not the pace that I want to move at. And also remember it's 1999 when I'm graduating. And so when you turn on the TV, people are standing in line for the next version of Windows. There's a lot of euphoria. AOL is starting to phase out and we're starting to touch on highspeed internet and and I was like, yo, look at look at the pace this is moving, but also you're hearing the narratives. Bill Gates drops out of college. These people are not necessarily glorifying the degree anymore. It's all about the skill. Now, unfortunately for me, I didn't know anyone that was a programmer. I didn't know anyone that was like a system administrator because at that time all the systems with like Sun Micros systemystems or IBM mainframe those are still the things that are in the enterprise. So when I looked at the job openings I'm seeing a bunch of skills that I don't even know how to acquire. And so instead of going to college you know I'm still doing fast food delivering pizzas at this time at Pizza Hut. And I remember going to a bookstore and they had the A+ certification guide and I looked and some of the job postings said, "Hey, you need to be A+ certified to take this support role or whatever it was." And I was like, "You know what? That doesn't require college. The book is only $35." And I remember buying the book and it is an official certification process. It looks like it was part of the job market. And so I remember buying that book and reading it cover to cover over and over again. and you're learning all the fundamentals, right? You're learning about, you know, how motherboards and how memory and all these things work and there's an OS component and then there's a little practice exam in the back. And so for someone like me, having that fast feedback loop of like you put the CD in, you take the exam and even though it was multiple choice, you kind of felt like if I got anything wrong, I would just go back to the book and make sure that I understood what was written there and then you go take the test again. and it had a little randomization to it so you couldn't just rely on absolute remembering everything. And I remember going to the facility to take the test and you know you're in that little room and they want to make sure you don't cheat. So there's a camera pointed at you and you're just going through it. And so the nice thing about those tests, there's no trick questions. Either you know it or you don't. And I think they maybe give you an hour, hour and a half. And I remember finishing that thing in like 10 minutes. And when I walk down, you know, you wait, the dialup goes and they calculate your score and say, "Hey, you passed." And then you walk out and you're like A+ certified. And that was like the first time in my career that I felt like, oh, so if you put the effort in, you can gain the certificate. And when I got that certificate, I remember there was like a job fair where, hey, anyone that has A+ and network plus certification, you can be part of the contractors that were replacing people's dialup with DSL at the time. 

</details>

**主持人**: 好的。

<details>
<summary>Original English</summary>

**Host**: Okay.

</details>

**Kelsey Hightower**: 我想我就是这样正式进入科技行业的。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: And so that's how I I guess officially got into tech.

</details>

**主持人**: 可以说你当时看到这可能是当时进入科技行业最有效的方式吗？

<details>
<summary>Original English</summary>

**Host**: Is it fair to say that you saw that this could be the most efficient way to get into tech at the time?

</details>

**Kelsey Hightower**: 我觉得我把它看作是**唯一**的方式。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: I think I said I saw it as the only way.

</details>

**主持人**: 为什么大学从来没有像……告诉你说，好吧，那可能是一条路。仅仅是因为你没有看到先例还是……

<details>
<summary>Original English</summary>

**Host**: Why was college never like telling you like, okay, that could be a way. Was it just you didn't see examples or...

</details>

**Kelsey Hightower**: 是的，我从未见过先例。我从未见过最终的成功画面。他们教授的很多课程内容，看起来不值得你付那么多钱。听着，也许那不是一所好学校，也许我选错了课，有很多因素可能导致这种情况。但当我看的时候，当时我仰慕的人，似乎都没有走这条路。所以我对学校已经受够了，对吧？如果你在那时 18 岁，你会想，听着，这已经够了。因为在那个时候，我觉得学校是因为对我来说太简单了实际上。你知道，拿全 A 很容易。我不觉得有什么严重的挑战。所以我想，嘿，我想再花四年时间做这个吗。后来我才了解到，本科学位的很多内容类似于你 K 到 12 年级经历的东西，你也是在记东西，听课，但硕士学位你需要挑战这些材料，当然如果你能读到博士，理想情况下你要为这个领域增添一些新东西，而我从未见过任何人能走那么远。所以我从未把它放入我的计算中。但是，仅仅拥有那种即时反馈循环——获得这个 A+ 认证，感觉就像是，哦，我准备好参与实际的经济运作，参与到生态系统中去了。所以，对我来说，我想，这似乎是一条更好的路。而且它感觉像是一条我能控制的路径。

<details>
<summary>Original English</summary>

**Kelsey Hightower**: Yeah, I never saw the examples. I never saw the endgame. A lot of the stuff that they were teaching the curriculum, it didn't make sense that you would pay all that money. You know, look, maybe it wasn't a good school. Maybe it was the wrong class that I took. There's so many factors that could have went into this. But when I looked at it, none of the people that at the time that I was looking up to, this is not the path that they seem to be taking. And so I had enough of school, right? If you're 18 at that time, you're like, look, that that's enough of this. Because at the time, I kind of felt school was this because it was so easy for me actually. You know, it's like it was easy to get straight A's. I didn't feel like there was a serious challenge. So it's like, hey, I want to go and do four more years of this. And I would later learn that look bachelors is a lot of the similar that you go through through K through 12, you kind of remember stuff, you listen to the lessons, but then masters you challenge the material and of course if you make it to PhD ideally you're adding something new to the field and I never saw anyone that has made it that far. So I never put that in part of my calculus. So, but just having that immediate feedback loop of like getting this A+ certification and feeling like, oh, I'm ready to participate in the actual economy, the ecosystem. So, to me, I was like, this seems like a better path. And it felt like a path that I would control.

</details>