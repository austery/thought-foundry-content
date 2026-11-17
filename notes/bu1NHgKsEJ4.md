---
author: New York Times Podcasts
date: '2026-11-16'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=bu1NHgKsEJ4
speaker: New York Times Podcasts
tags:
  - system-outage
  - root-cause-analysis
  - digital-infrastructure
  - air-traffic-control
title: FAA与微软接连发生系统故障暴露数字基建脆弱性；特朗普访华前夕的谍战风波
summary: 本期要闻报道了全美航空系统因FAA路由器升级失误陷入瘫痪，以及微软全球服务中断，凸显关键数字基础设施的脆弱性；同时涵盖特朗普访华与英伟达CEO离职相关的间谍疑云、Medicaid工时要求推迟、留学生入学率骤降及乌鸦认知能力的最新研究。
insight: ''
draft: true
series: ''
category: debugging
area: tech-engineering
project: []
people:
  - Shawn Duffy
  - Donald Trump
  - Jensen Huang
companies_orgs:
  - Federal Aviation Administration
  - Microsoft
  - Nvidia
  - L3Harris
products_models: []
media_books:
  - The New York Times
  - Science
status: evergreen
---
这里是《纽约时报》头条新闻。我是特蕾西·芒福德（Tracy Mumford）。今天是 11 月 16 日，星期一。以下是今天的重点关注内容。

<details><summary>Original English</summary>
[music] From the New York Times, it's the headlines. I'm Tracy Mumford. Today is Monday, [music] November 16th. Here's what we're covering.
</details>

### FAA 通信系统升级受挫引发全美航班停飞

>> 部长先生，您能保证周五发生的事情不会再次发生吗？

<details><summary>Original English</summary>
>> Can you guarantee that what happened on Friday won't happen again, Mr. Secretary?
</details>

>> 呃，首先我们必须查明到底发生了什么。这是 L3 Harris 在施工时安装失误导致的吗？

<details><summary>Original English</summary>
>> Well, first we have to figure out what what happened. Was this a faulty installation by L3 Harris that was doing?
</details>

>> 交通部长肖恩·达菲（Shawn Duffy）表示，本周末的机场混乱是由一次更新美国联邦航空管理局（FAA）陈旧通信系统的尝试引发的。

<details><summary>Original English</summary>
>> The Secretary of Transportation Shawn Duffy says that this weekend's airport chaos was set off by an attempt to update the FAA's antiquated communication system.
</details>

>> 这要追溯到 20 年、25 年、30 年前长期缺乏投资，也缺乏那种——你知道的——站出来大声疾呼说“嘿，这是个问题，我们来解决它”的担当。他们当初为什么没有那么做，我不知道。

在 FAA 于周五发布了罕见的全美地面停飞指令后，数千架次航班被取消，导致数万名旅客滞留，航空出行连续数日陷入混乱。以下是目前已知的事故起因：官员表示，起因是一名承包商对阿肯色州一处无线电设施的路由器进行了升级，这是将传统铜线系统替换为光纤电缆工程的一部分。在此过程中，官员注意到该设施以及德克萨斯州另一处近期完成升级的设施，开始以异常高的频率向 FAA 通信网络发送 Ping 请求，实际上是用海量数据冲垮了系统。据 FAA 首席技术官称，这引发了网络其他部分的连锁故障，迫使官方宣布地面停飞。FAA 的电信和基础设施系统中存在脆弱性，这意味着一旦发生故障，并不一定有缓冲或保护机制。FAA 局长布赖恩·贝德福德（Brian Bedford）周六上午表示，该系统根本没有“备用的备用方案”。《时报》负责报道航空与交通的记者 Karen Demergent 表示，外界一直对特朗普政府如何推进这项急需的空中交通管制网络现代化工作存有担忧。今年秋季早些时候，一个无党派政府监督机构就曾警告，政府在改造如此脆弱的系统时推进得过快。这是一个重大工程，两党一致认为必须予以解决；但在现任政府推进该工程的方式，以及他们审视潜在故障点（或是如周五所见实际发生的故障点）的方法是否真正充分考虑了这些风险上，各方存在分歧。

刚过去的周末，达菲呼吁国会在年底前快速审批 500 亿美元的新资金，用于空中交通管制系统的升级。这笔款项大幅超过了他此前要求的金额，并引来了部分议员的严厉批评。负责监督 FAA 的众议院专门小组中的两位资深民主党人发表声明指出，国会此前已经拨给该机构用于现代化改造的资金，大部分至今仍未支出。[音乐]

<details><summary>Original English</summary>
>> Goes back 20, 25, 30 years of a lack of investment, a lack of, you know, waving the flag to say, "Hey, this is a problem. Let's fix it." Why they didn't do that, I don't know. After the FAA issued a rare nationwide ground stop on Friday, thousands of flights were cancelled, stranding tens of thousands of passengers and snarling air travel for days. Here's what we know so far about what set everything off. Officials say it began when a contractor upgraded a router in a radio facility in Arkansas, part of an effort to replace old school copper wire systems with fiber optic cable. In the middle of that, officials noticed that the facility and another recently upgraded one in Texas had started to ping the FAA communications network at an abnormally high rate, basically overwhelming the system with data. According to the FAA's chief technology officer, that set off failures in other parts of the network and forced officials to declare the ground stop. There are vulnerabilities in the FAA's telecoms and infrastructure systems that mean that when something goes wrong, there isn't necessarily a buffer or a cushion there. The FAA administrator, Brian Bedford, on Saturday morning said there are no backups to the backup. Karen Demergent covers aviation and transportation for the Times. She says there have been concerns about how the Trump administration is handling the muchneeded effort to modernize the country's air traffic control network. Earlier this fall, a nonpartisan government watchdog warned that the government was moving too quickly to overhaul such a fragile system. It's a major project. It's something that there is bipartisan agreement has to be tackled. But there is disagreement about whether the style in which this administration is tackling this and the way in which they are looking at these potential points of failure or actual points of failure as we saw on Friday is really adequately taking these risks into consideration.

Over the weekend, Duffy called on Congress to fasttrack $50 billion dollar in new funding for air traffic control upgrades by the end of the year. That's a drastically larger sum than he's asked for before, and it drew sharp criticism from some lawmakers. Two top Democrats on House panels overseeing the FAA put out a statement pointing out that the agency still hasn't spent the majority of the funds Congress already gave it for modernization. [music]
</details>

### 特朗普访华前夕的间谍风波与中美博弈

本周，特朗普总统将前往中国出席一场原定旨在延长贸易战休战协议的会晤，但现在出现了一个新转折。

<details><summary>Original English</summary>
This week, President Trump is headed to China for a meeting that was intended to be about extending a trade war truce, but now has a new twist.
</details>

>> 您在与习主席会面时，会提及黄仁勋的事情吗？

<details><summary>Original English</summary>
>> Are you going to bring up the case of Jensen Wong with President Xi when you visit with him?
</details>

>> 不，我认为不会。我的意思是，也许——我相信习主席会问起我这件事。我非常了解 Jensen。我只是觉得他是一个非常正派的人。我的意思是——

<details><summary>Original English</summary>
>> No, I don't think so. I mean, maybe I'm sure President Xi will ask me about it. I just know Jensen very well. I just think he's a very honorable man. I mean,
</details>

>> 特朗普启程之际，黄仁勋从英伟达辞职引发的震动依然历历在目。尽管围绕此事出现了地缘政治风暴，特朗普已向记者表示，他自己并不打算主动提及黄仁勋以及他与一名被美国情报官员认为是“中国间谍”的女性有染的事宜。

<details><summary>Original English</summary>
>> Trump will be making the trip with the shock of Jensen Huang's resignation from Nvidia still fresh. And despite the geopolitical storm around it, Trump has told reporters he doesn't plan to bring up the issue himself of Hong and his affair with a woman who US intelligence officials believe is a Chinese spy.
</details>

>> 他应该辞职吗？[叹气]

<details><summary>Original English</summary>
>> Should he have stepped down? [sighs]
</details>

>> 嗯，最关键的问题是，那个女人到底是不是间谍？而我不知道这一点是否已经有了定论。

<details><summary>Original English</summary>
>> Well, the big thing is, was the woman a spy? and I don't know if that's been determined yet.
</details>

>> 总统表示，他不记得自己曾听取过关于该情报的简报，并淡化了对此事的担忧。但我的同事、负责报道中国的戴维·皮尔森（David Pierson）表示，这种情况突显了美中两国在幕后的真实暗流。

<details><summary>Original English</summary>
>> The president has said he doesn't remember being briefed on the intelligence and has downplayed concerns about it. But my colleague David Pearson, who covers China, says the situation has underscored what's happening between the two countries behind the scenes.
</details>

>> 在习近平的领导下，中国强化了其间谍行动。中国将其被称为国家安全部的情报机构，从过去那种仅仅在使馆晚宴上打探传闻的不成熟运作，转变为利用人工智能工具，以及——你知道的——动员公众协助全面搜集情报。与此同时，美国也认识到必须将情报搜集的范围扩大到中国企业，因而加大了对华间谍行动的资源投入，因为当今美中之间的竞争很大程度上是经济竞争。因此，从表面上看，两国领导人似乎正在推动双边关系稳定，而且在某种程度上确实也是如此。但在水面之下，两国之间仍在进行着一场激烈的间谍战。[音乐]

<details><summary>Original English</summary>
>> Under shei, China has intensified its spying operations. It has transformed its spy agency known as the Ministry of State Security from really an unsophisticated operation just you know dealing with rumors at embassy dinner parties to using AI tools to you know employing the public to help them in all intelligence gathering. Now, at the same time, the United States is also stepped up its resources and spying on China, recognizing that it has to expand the scope of its intelligence gathering to include Chinese businesses uh because so much of the competition between China and the United States is economic today. So, on the surface, it looks like the two leaders are helping stabilize relations and and on some level it really is like that. But just beneath the surface, there's still a furious spy war going on between the two countries. [music]
</details>

### 特朗普政府政策动向：Medicaid 工时要求延期与国际生人数下滑

接下来是关于特朗普政府的另外两条简讯。首先，联邦官员推迟了一项影响数百万 Medicaid 受益人的关键截止日期。截至 1 月 1 日，许多 Medicaid 受益人原本必须填写表格，证明自己处于工作或志愿服务状态，以保留其医疗保险资格。许多医院曾开足马力，试图及时提醒患者即将发生的变化。现在，政府表示各州可以推迟到今年夏天再开始执行这项工作要求规则，并承认构建用于追踪更严格资格要求的新软件系统难度极大。尽管如此，新规的最终推行预计仍将对患者和医疗体系产生广泛影响。据政府估算，在未来几年内，这些规则将导致大约 500 万美国人失去医疗保险，其中包括许多被繁琐的表格申请流程难倒的人。

今天公布的一项新调查显示，随着特朗普政府的政策似乎正在驱离外国留学生，美国大学的国际学生入学人数持续大幅下降。根据国际教育协会（Institute of International Education）的数据，今年秋季国际新生入学人数下降了 15%。在此之前，去年的降幅已达到 18%。尽管美国仍是全球留学生的首选目的地，但签证政策的变动以及对白宫打击移民力度的担忧，已促使一些学生决定前往其他国家接受高等教育。这已经对各大学的财务底线造成了沉重打击。许多留学生缴纳全额学费，这实际上补贴了美国本土学生的费用。全美多所院校已经将留学生带来的收入损失，列为其被迫裁员、削减预算和关闭项目的原因。

<details><summary>Original English</summary>
Now, two other quick updates on the Trump administration. First, federal officials have pushed back a key deadline that affects millions of people on Medicaid. As of January 1st, many Medicaid recipients were going to have to complete forms proving they were working or volunteering to keep their insurance coverage. and a lot of hospitals had gone into overdrive trying to alert patients to the upcoming changes in time. Now, the administration says states can wait until this summer to start enforcing the work rules, acknowledging how difficult it's been to build new software systems to track the stricter eligibility requirements. Still, the eventual roll out of the new rules is expected to have a widespread impact on patients and health care systems. According to a government estimate, over the next few years, the rules will mean that about 5 million Americans lose their health insurance, including many who get tripped up by the new paperwork challenges.

And a new survey out today shows that international student enrollment at American universities is continuing to plunge as Trump administration policies appear to be driving foreign students away. According to data from the Institute of International Education, new international student enrollment dropped by 15% this fall. That's on top of an 18% drop last year. While the US is still the top destination for international students worldwide, changing visa policies and fears over the White House's crackdown on immigrants have made some students decide to go elsewhere for their higher education. That is already taking a major toll on university's bottom line. Many international students pay full tuition, effectively subsidizing the cost for Americans. And schools around the US have already cited a loss of revenue from international students as the reason they've had to lay off employees, cut budgets, and close programs.
</details>

### 微软全球服务中断与数字基础设施脆弱性

下面是一条关于过去几天内让人们陷入混乱的另一起技术故障的消息。这次不是 FAA，而是微软。

<details><summary>Original English</summary>
News now on the other recent tech outage that left people scrambling over the past few days. Not the FAA, but Microsoft.
</details>

>> Outlook 瘫痪了。Exchange Online 瘫痪了。Teams 瘫痪了。Copilot 也瘫痪了。

<details><summary>Original English</summary>
>> Outlook is down. Exchange online. Teams down. Copilot is down.
</details>

>> 从周四开始，全球数以百万计的人无法使用电子邮件、视频会议及其他功能。

<details><summary>Original English</summary>
>> Starting on Thursday, millions of people worldwide were cut off from email, video meetings, and other features.
</details>

>> 我刚才试图在 Outlook 中打开一封邮件，Outlook 就像看傻子一样看着我。技术故障迅速蔓延，波及全美及数十个其他国家的用户。新加坡税务机关无法接收信息；英国的药店在开具处方药时陷入困境；澳大利亚情报和警方部门表示，他们的行动也受到了影响。到周六，这家科技巨头终于完全恢复了服务。微软表示，此次宕机并非网络攻击，也与人工智能无关。相反，该公司称问题始于一次升级过程，与 FAA 的情况类似。专家表示，这两起出现差错的升级凸显了从银行业、医疗保健到交通运输等各领域众多数字系统的脆弱性。许多系统依赖于新旧硬件的结合，再加上需要频繁更新的软件。多年来，它们几乎变成了类似地质构造的产物，新层不断堆叠在旧层之上。一旦打破这种微妙的平衡，整个系统就可能轰然崩塌。微软目前尚未对升级过程中究竟出了什么差错给出明确的答复。[音乐] 它已承诺将发布一份完整报告，查明这起宕机事件所谓的“根本原因”。

<details><summary>Original English</summary>
>> I literally just tried to open up an email in Outlook, and Outlook looked at me like, "Are you stupid?" The technical issues ballooned to affect people across the US and dozens of other countries. Singapore's tax authorities couldn't receive messages. Pharmacies in Britain struggled to fill prescriptions and Australian intelligence and police forces said their operations were also affected. By Saturday, the tech giant was able to fully restore its services. Microsoft said the outage was not a cyber attack or related to artificial intelligence. Instead, the company said that the problems began during an upgrade, similar to the FAA. Experts say those two upgrades gone arry highlight how fragile many digital systems actually are in everything from banking to healthcare to transportation. A lot of them rely on a combination of new and old hardware plus software that needs frequent updating. Over the years, they've almost become like geological formations with new layers piling on top of old ones. Upset that delicate balance, though, and the whole system can come crashing down. Microsoft has yet to provide a clear answer for what exactly went wrong during the update. [music] It's promised to publish a full report identifying the quote root cause of the outage.
</details>

### 科学前沿：乌鸦的快速决策能力

最后，人类欠鸟类一个道歉。长期以来，研究鸟类的学者看着它们小小的脑袋，得出的结论是它们并不怎么聪明。因此有了“鸟脑子”（bird brain）这个词，这可不是什么夸奖。但越来越多的证据表明，它们脑子里发生的事情远比任何人以往所认为的要丰富得多。例如，某些物种能够区分癌细胞与非癌细胞，另一些物种能够辨识自己的影像、解决抽象问题，甚至能为未来做出规划。现在，发表在《科学》（Science）杂志上的一项最新研究显示，具体到乌鸦，它们做决定的速度其实比人类更快。这项研究让乌鸦面对屏幕上一团旋转的点阵，如果它们能准确判断出点阵是在向左还是向右移动，就会获得奖励。乌鸦啄出答案的速度始终是恒河猴或人类的两倍，而且完全没有牺牲准确率。该研究的作者之一表示，他甚至让自己实验室的所有人员——本科生、博士生、博士后——与乌鸦同台竞技，结果所有人都比乌鸦慢。这项研究突显出鸟类的大脑虽然体积小，却专为快速处理信息进行了高度优化。研究团队推测，这与飞行的风险性密切相关。为了在高空中生存下来，必须极其迅速地做出大量决策。

以上就是今天的头条新闻。[音乐]

在我们结束之前，我最喜欢的《时报》关于乌鸦的报道，依然是那项展示乌鸦多么擅长记仇的研究。[音乐] 事实证明，它们甚至能将仇恨代代相传，形成了大家大概可以称之为“跨代乌鸦之怒”的现象。[音乐] 我是特蕾西·芒福德。我们明天再见。

<details><summary>Original English</summary>
And finally, humans owe birds an apology. For a long time, scholars studying birds looked at their small brains and concluded they weren't all that bright. Hence the term bird brain, not a compliment. But evidence has been increasingly piling up that there's a lot more happening in there than anyone was giving birds credit for. For example, some species are capable of distinguishing between cancerous and non-cancerous cells, and others can recognize their own image, solve abstract problems, even plan for the future. And now, new research published in the journal Science shows that crows specifically can make decisions faster than humans. The research involved placing crows in front of a swirling mass of dots on a screen and rewarding them for answering whether the dots were moving to the left or the right. The crows reliably pecked their answers twice as fast as Reese's monkeys or humans and they did it without compromising accuracy. One of the authors of the study said he even put all of the people in his lab up against the birds, undergrads, PhDs, postocs, and they were all too slow for the crows. The research underscores how the aven brain, despite being small, is tuned for rapid processing. The research team suspects it has a lot to do with how risky flying is. In order to stay alive up there, you got to make a lot of decisions really quick.

Those are the headlines. [music] And before we go, my favorite piece of crow coverage from the Times remains the research that showed how good crows are at holding grudges. [music] It turns out they can even pass them down, creating what I guess you would call multi-generational crow [music] wrath. I'm Tracy Mumford. We'll be back tomorrow.
</details>