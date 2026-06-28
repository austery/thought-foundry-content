---
author: The Pragmatic Engineer
date: '2026-06-24'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=xafwfGVBxos
speaker: The Pragmatic Engineer
tags:
  - prompt-engineering
  - systems-thinking
  - career-development
  - effort-vs-shortcut
title: 人工智能时代编程面试的演变与工程师的核心竞争力分析
summary: 文章探讨了随着AI发展，传统编程面试（如数据结构和算法）的地位变化。核心观点认为，虽然日常工作已转向提示词工程，但对系统性思维、领域专长以及主动解决问题的能力的需求依然存在。作者强调在AI普及的背景下，努力本身正成为差异化优势，而软技能和驱动力（agency）比单纯的代码实现更重要。
insight: ''
draft: true
series: ''
category: tech-trends
area: tech-engineering
project: []
people: []
companies_orgs: []
products_models: []
media_books: []
status: evergreen
---
<!-- chunk 1/13 -->

### 播客开场片段

**Host**: 已经有太多预测说编程面试将会消亡。

<details>
<summary>Original English</summary>

**Host**: There's been so many predictions that coding interviews will be dead.

</details>

**Neet**: 以前面试中出现过作弊工具。现在谷歌基本上已经恢复了现场面试，回到了传统的白板面试。总会有人盯着你写代码，你可能无法通过作弊蒙混过关。

<details>
<summary>Original English</summary>

**Neet**: There's been cheating tools for interviews. Google has pretty much gone to on-sites at this point, back to the traditional whiteboard. Somebody's going to be watching you code, and you're probably not going to be able to cheat your way through that.

</details>

**Host**: 你的一个犀利观点是关于 2026 年的。现在构建东西前所未有地容易，但我认为这反而让创造真正的价值变得困难十倍。你曾说，性格特质现在比编程技能更重要。[音乐]

<details>
<summary>Original English</summary>

**Host**: One of your hot takes is 2026. It's never been easier to build things, but I would say that it just makes 10 times harder to actually build value. You said that personality traits are now more important than coding skills. [music]

</details>

**Neet**: 我几个月前雇了一个人，他们甚至还没毕业。每次我给这个人布置任务，哪怕他们完全不知道从何着手，一周之后，他们就能把所有相关知识都学会。这才是最关键的。

<details>
<summary>Original English</summary>

**Neet**: I hired somebody a few months ago. They still haven't even graduated. Anytime I give this person a task, even if they have no idea how to start it, a week later, they'll have learned everything about it. That matters the most.

</details>

**Host**: 你还有一个相当有争议的犀利观点，那就是有些人干脆应该放弃科技行业的职业生涯。

<details>
<summary>Original English</summary>

**Host**: You've had a pretty contentious hot take, which was some people should just give up on tech careers.

</details>

**Neet**: 你应该清楚自己将要面对的是什么，因为——

<details>
<summary>Original English</summary>

**Neet**: You should know what you're getting yourself into because

</details>

### 嘉宾介绍与赞助商播报

**Host**: 是什么让优秀的工程师脱颖而出？Neet Dhiman Singh，[音乐] 或者大家都叫他 Neet，他创立了 NeetCode，这是一个面试准备平台，帮助了无数开发者在大型科技公司找到了工作。[音乐] 在今天的节目中，我们将讨论如何准备数据结构和算法面试，以及这些知识在实际工作中的用处，还有为什么思维方式比算法本身更重要。我们将探讨那些在没有 AI 辅助的情况下依然能独立思考的工程师与离了 AI 就无所适从的工程师之间日益扩大的差距。

<details>
<summary>Original English</summary>

**Host**: What separates strong engineers from everyone else? Neet Dhiman Singh, [music] or as many call him Neet, he created NeetCode, the coding preparation platform that helps countless devs get hired [music] at big tech. In today's episode, we cover what preparing for data structures and algorithms interviews that's [music] useful on the job, and how it's more about mindset than the algorithms. The growing difference between engineers who can still think without AI at their fingertips

</details>

**Host**: [音乐] 以及 Neet 那个极具争议的观点：有些人干脆应该放弃科技行业的职业生涯，[音乐] 以及更多精彩内容。如果你想了解哪些入门技能可以在职业生涯中不断复利，而哪些技能正在被 AI 悄然侵蚀，这期节目就是为你准备的。

本期节目由 Antithesis 赞助播出。[音乐] Antithesis 能在模拟的敌对环境中运行你的整个系统，赶在你的用户发现之前找出所有 bug。[音乐] 听起来像科幻小说，但这其实是硬核的工程技术。前往 antithesis.com/pragmatic 了解它是如何做到的。

本期节目也由 Sentry 赞助。Sentry 是我以前在 Uber 工作时用来进行应用监控的工具，现在我也把它用在我的所有项目中，包括 Pragmatic Engineer 的后端。Sentry 的一个我很喜欢的新功能是他们的 Sear AI 智能体，它能帮助调查生产环境的错误。例如，这里有一个我的应用中真实发生的错误。我只需询问 Sear 根本原因可能是什么，它就会提供上下文，并能直接在网页界面上制定一个修复计划。哦，而且它在 Slack 里也能用，不仅仅局限于网页端。

我发现 Sentry 更方便的一个使用场景是，通过 Sentry MCP 在 Code X 或 Cloud Code 中使用它。连接 MCP 服务器后，你可以做一些非常实用的事情。比如，当一个已经解决的 Sentry 问题再次出现时，你可以启动一个智能体来调查回归原因，阅读相关代码，并提交一个包含建议修复方案的 PR（Pull Request）。要让所有这些运转起来需要一点工作量：将 Sentry 连接到你的代码库，将 Sentry MCP 添加到 Cursor 中，为 Cursor 的智能体定义调查指令，配置启动自动化的触发器，并测试一切是否正常。但是一旦你配置好并运行起来，你就能更快地修复回归问题，同时仍然可以对所有修复进行审查。

我并不喜欢为了用 AI 而用 AI，但我真的很喜欢这种能让我以更多上下文、更快地修复错误的实用集成。访问 sentry.io/pragmatic 了解 Sentry，今天就开始监控和修复回归问题吧。

<details>
<summary>Original English</summary>

**Host**: [music] and those who freeze without it. Neet's contentious hot take that some people should just give up on tech careers, [music] and many more. If you want to understand which entering skills compound over a career and the ones that AI is quietly eroding, this episode is for you. 

This episode is presented by [music] Antithesis. Antithesis runs your whole system in a hostile simulation and finds every bug before [music] your users do. It sounds like science fiction, but it's actually hardcore engineering. Understand how at antithesis.com/pragmatic. 

This episode is brought to you by Sentry. Sentry is a tool I used for application monitoring back when I worked at Uber, and I now use it on all my projects, including the Pragmatic Engineer backend. One new feature I'm really liking about Sentry is their Sear AI agent, which helps investigate production errors. For example, here's an actual error I had in my application. I can just ask Sear what might be the root cause and it brings context and it can also make a plan to fix it all from the web interface. Oh, and it also works in Slack as well, not just the web. 

One place that I find even more handy to use Sentry is from code X or cloud code using Sentry MCP. After you hook up the MCP server, you can do some very useful things. For example, when an already resolved Sentry issue resurfaces, you can kick off an agent to investigate the regression, read the relevant code, and open a PR with a suggested fix. There's a little work involved to get all of this going. to connect Sentry to your code repository, add Sentry MCP as a cursor, define the instruction for cursor's agent to investigate, configure the trigger that launches the automation, and test that it all works. But once you have it up and running, you can get regressions fixed faster while still reviewing every and all fixes. I'm not a fan of using AI tools just for the sake of it, but I really like the practical integrations where I can fix errors faster and with more context. Check out Sentry at sentry.io/pragmatic and start monitoring and fixing regressions today.

</details>

### 关于 AI 时代的编程面试

**Host**: Neet，欢迎来到播客。

<details>
<summary>Original English</summary>

**Host**: Neat. Welcome to the podcast.

</details>

**Neet**: 谢谢，很高兴来到这里。

<details>
<summary>Original English</summary>

**Neet**: Yeah, I'm happy to be here.

</details>

**Host**: 很高兴能邀请到你。让我们从我最近一直在思考的一个问题开始吧。之前有很多人预测，一旦 AI 强大到能够编写代码，你知道的，编程面试就会消亡，因为我们在日常工作中将不再编写代码。现在，大多数工程师不再是手写代码，而是在工作中写提示词（prompting）。然而在这些相同的公司里，编程面试依然没有消亡。对此你怎么看？

<details>
<summary>Original English</summary>

**Host**: It's awesome to have you here. Let's start with something that I've been thinking about. So, there's been so many predictions that if if and when AI will be good enough to like write code, you know, coding interviews will be dead because uh on the day-to-day we will not be writing code. Now, most engineers are not writing code, they're prompting at work. And yet at the same companies, coding interviews are still not dead. What is your take on this?

</details>

**Neet**: 是啊，我觉得这非常有趣。考虑到过去几年，尤其是过去几个月里编程方式发生了如此巨大的变化，令人惊讶的是，编程面试竟然是唯一一个基本保持不变的领域。我知道有些人说面试方式改变了很多，但目前为止，变化其实只是一点点，比如一些公司在尝试 AI 辅助的编程面试。但令人惊讶的是，数据结构和算法的编程面试形式真的非常有粘性。

这让很多人感到困惑，包括我在内，因为我们已经到了这样一个阶段：你可以向 AI 机器人询问关于代码库的任何问题，它都能给你一个相当不错的回答。你可以要求它实现某个功能，几乎无所不能。它可能无法做到 100% 完美，毕竟连人类都写不出无 bug 的代码，但它至少能完成 90%，非常接近了。所以这让很多人感到困惑。

我认为这要回到一个根本问题：你到底如何评估一个人是否是一个好的雇佣对象？其中一个方面是：他们有硬技能吗？他们有技术实力吗？他们会思考吗？而数据结构与算法（DSA）面试从来都不是评估这些的最佳方式。嗯，评估思考能力或许可以，但就这项技能是否能转化为你在工作中的实际表现而言？它从来没有真正转化过。它更多的是评估一个人是否具备思考能力。所以我认为这是面试形式保持不变的第一个原因。

第二个原因是，公司根本不知道该如何评估，而且他们可能从来都不知道。我想起我和我的朋友 Steve（在亚马逊工作）聊天时，他提到他们做过一些研究。结果发现，当你雇佣一个人时，无论你拥有多少数据，无论你是怎么设计面试流程的，你都很难预测这个人真正在工作中的表现会如何。

<details>
<summary>Original English</summary>

**Neet**: Yeah, I think it's really funny with how much coding has changed the last few years and especially the last few months that coding interviews are the one area that have surprisingly stayed pretty consistent. I know some people like talk about them changing a lot and so far they're kind of like changing a bit with like AI-assisted coding interviews, companies are trying that. But surprisingly, the coding interview format of data structures and algorithms is really really sticky. 

And it's confusing to a lot of people, myself included, because like we've gotten to a point where you can ask like an AI bot any question about a code base it can give you a pretty good answer. You can ask it to implement some feature, you can uh do anything pretty much. And it might not get 100% of the way there like even humans can't write bug-free code but it can get at least 90% of the way there like pretty close. So it's confusing to a lot of people and I think that it goes back to like how do you even evaluate if somebody's a good hire or not there's one aspect of it which is like do they have the hard skills do they have the technical skills can they think and DSA interviews were never the best for that. Well, thinking sure but in terms of like does that skill translate to what you're doing on the job? It never really translated to that. It was more about evaluating like does somebody think? 

So I think that's one of the reasons and the second reason that's stayed sticky is that companies just have no idea how to evaluate like and they probably never did. I think I was talking to a friend of mine Steve from Amazon and he he mentioned that like they've ran some studies and it's like very hard to know like whether somebody like when you hire somebody no matter how much data you have no matter how like you've run the interview process that it's just very hard to know like how somebody's actually going to perform on the job. So

</details>

**Host**: 就是很难判断他们是否能胜任工作，对吧？

<details>
<summary>Original English</summary>

**Host**: If if if they're going to work out right?

</details>

**Neet**: 这是一个非常困难的问题。因为即使一个人能力很强，你怎么知道他们是否有动力？你怎么知道他们会喜欢团队环境、氛围和所有这些因素？所以我觉得这真的很复杂。

<details>
<summary>Original English</summary>

**Neet**: It's a very hard problem because even if somebody is good how do you know they're going to be motivated? How do you know they're going to enjoy the team environment the vibe and all that stuff. So I think it's just really complicated.

</details>

**Host**: 那会不会有另一个原因，它之所以一直这么有粘性，并且现在依然如此，仅仅是因为大家有一种“如果没有坏，就不要修”的心态？

<details>
<summary>Original English</summary>

**Host**: And could another reason be that it has been so sticky and it's still a sticky that maybe it's just simple as there it's kind of like if it if it ain't broken don't fix it type of mentality?

</details>

**Neet**: 我觉得是这样，因为每当你试图改变某些东西时，你都面临着让情况变得更糟的风险。所以，首先，在大型公司改变这个流程是一项庞大的工程，非常官僚。那将需要大量的重新培训。我们已经开始看到 Meta 这样的公司在尝试运行 AI 编程面试了。这种培训真的很难落实，因为面试官往往并不是很优秀。大部分面试官其实根本不喜欢面试，他们讨厌做这个。

<details>
<summary>Original English</summary>

**Neet**: I think so because anytime you try to change something you risk making it worse and so it's like first of all it's a lot of work to change that process at big companies like it's very bureaucratic. There's going to be a lot of like retraining and we're already kind of seeing that with companies like meta trying to run AI coding interviews. The training is really hard to get get down cuz it's like Interviewers are just not good. Like the most Interviewers do not like interviewing. They hate it.

</details>

**Host**: 当你说培训的时候，你指的是对面试官的培训，就像在一家拥有上千名面试官的大公司里，培训他们保持一致的评判标准。

<details>
<summary>Original English</summary>

**Host**: when you're saying training, you mean interviewer training, like training your interviewers like at a large company like a thousand of them to like be similar.

</details>

**Neet**: 完全正确。因为在一家大公司里，你希望流程是标准化的。你希望每个人经历的流程都一样。而总的来说，这一点本来就很难做好。当你引入更多变量时，比如引入一种新的评估流程，或者用不同的方式培训面试官，这就更难做到了。现在你还要去检查 AI 的提示词，还有所有这些变量。所以，这不是一门精确的科学，很难去衡量这些东西，实际上是不可能的。

所以，我确信我们会看到公司尝试不同的东西。我们大概率也会看到引入不同的面试形式。我只是认为，这个过渡期会比大多数人想象的要缓慢得多。

<details>
<summary>Original English</summary>

**Neet**: Exactly, yeah. Because at a big company, you want the process to be standardized. You want it to be the same for everybody. And that's very hard to get right in general. And it's even harder to get right when you have like more variables introduced, like a new evaluation process, training interviewers differently. Now you got to check the AI prompts, like all these variables. And so, it's not like an exact science. It's hard to measure these things. It's It's practically impossible. So, I think we're definitely going to see, I think, companies trying different things. I think we probably will see different interview formats introduced. I just think it is going to be a slower transition than most people think.

</details>

### Neet 的科技行业启蒙

**Host**: 我想把话题倒回很多，聊聊你早期的经历。你是怎么进入科技行业的？你第一次接触编程是什么时候？

<details>
<summary>Original English</summary>

**Host**: I want to rewind a lot back into into your early days. Like how did you get into tech? What was your first introduction with programming coding?

</details>

**Neet**: 嗯，我上大学的时候其实是在学电气工程。因为我非常喜欢数学和物理。我知道很多程序员不喜欢这些——当然有些人喜欢，但很多程序员并不喜欢。但他们非常喜欢编程。所以，当我接触到编程的时候，我……

<details>
<summary>Original English</summary>

**Neet**: Yeah, I was actually studying electrical engineering when I was in college. Because I really liked math. I really liked physics. I know a lot of programmers don't. Some Some of them obviously do, but a lot of programmers don't. But they really like programming. And so, when I got into our programming, I was

</details>

<!-- chunk 2/13 -->

### 初涉编程与走向商业现实

**Speaker A**: 刚开始上 C 语言入门课的时候。这是电气工程的必修课。我其实不太想上。而且一开始我也学得不太好。我记得当时在努力学习 `printf` 和，你知道的，`%s`，`%c`，我也不知道为什么。我环顾四周。周围的每个人都学得好快。对我来说，这完全是一种不同的思维方式。尽管它和数学有点关系，你可能会觉得它很容易上手，但一开始对我来说真的不是。但是后来，我想大概过了几个月，我们学习了变量、条件语句、循环、函数以及所有这些概念。然后，真的就像是突然开窍了一样，一开始，编程感觉有点无聊。就像是只有变量和数字。但是当你引入了所有这些东西，你就会意识到这其中可以引入无限的复杂性。你可以从今天构建的所有软件中看到这一点，就像是你拿着这些简单的基础元素，这些0和1，突然之间你就拥有了这个庞大的软件宇宙，解决着极其疯狂的问题。像 Google Spanner 这样的数据库，它们不仅需要编程，还需要物理学，需要原子钟和 GPS 系统等等这些东西，它们解决的是一些非常难的问题。所以，我想回到我的故事，一旦我真正开始享受编程，我就深深地爱上了它，我当时觉得，“好吧，我余生都要做这个。我会热爱它的。”然后我经历了一个转变，当我真正进入现实社会后，我意识到编程不是你可以仅仅按照自己喜欢的方式去做的事情。归根结底，这是一门生意，所以这在很多方面剥夺了我对它的乐趣，就像是你不能用你喜欢的语言工作，不能解决你喜欢解决的问题。你必须专注于业务问题。所以，是的，因为这个原因，我对编程有一种爱恨交织的感情。我想很多人都是如此。

<details>
<summary>Original English</summary>

**Speaker A**: just taking our intro to C class. It was required for electrical engineering. I didn't really want to take it. And I was not very good at it initially. I remember trying to learn printf and the you know, percent S, percent C, like I don't know why. Like I looked around. Everybody around me was learning it so quickly. And to me, it was just a very different way of thinking. Even though it's kind of related to math, you'd think it'd be easy to pick up, but it really wasn't initially for me. But then, I think a couple months went by and we learned about variables, conditions, loops, functions, and all these kind of concepts. And then it really like something just kind of clicked where it's like initially, programming felt kind of boring. It's like you just have variables and numbers. But then when you introduce all these things, then you realize there's like this infinite complexity that can be introduced. And and you see that with like all the software that is built today, where it's like you took these like simple primitive things, these zeros and ones, and all of a sudden you just have this enormous like universe of software solving insane problems. You have databases like Google Spanner, which not only take programming, but they take physics, they take like atomic clocks and GPS systems and all these things, and they solve like these really hard problems. And so, I I I guess to go back to my story and well once I really started enjoying programming, I just fell in love with it and I was like, "Okay, I'm going to I'm going to do this for the rest of my life. I'm going to love it." And then I went through a transition where once I got into the real world, I realized that programming is not something you can just kind of do the way you enjoy. Like it's a business at the end of the day, and so that in a lot of ways took some of the fun out of it for me, where it's like you don't get to work on the languages that you like, the problems that you enjoy solving. You have to focus on like the business problems. And so, yeah, I I I I have a love-hate relationship with programming because of that reason. And I think a lot of people do.

</details>

### CAP 定理的局限与深究技术的偏好

**Speaker B**: 有趣的是，你知道，你一开始觉得无聊，然后你对它的复杂性和可能性感到兴奋，接着你又算是回到了现实。在开始录播客之前，我们刚聊到的一件事是 CAP 定理。关于你对它也有一种类似奇怪的关系。我们能谈谈这个吗？同时为了那些在听但不知道 CAP 定理具体是什么的听众。让我们从这个开始吧。

<details>
<summary>Original English</summary>

**Speaker B**: It's interesting how you know, you you got really excited it was boring, and then you got excited about the complexity and the possibilities, and you kind of came back to down to earth. One thing we were just talking about before we started the podcast is the CAP theorem. On how you also had a similarly weird relationship with it. Can we talk about it? And also for those of us those listening who who don't know exactly what the CAP theorem is. Let's start with that.

</details>

**Speaker A**: 是的，当然。这其实是一个非常简单的定理。有时候它的描述有点别扭，就像是你面临三个选择，你只能选其中两个。有“一致性”（Consistency），那是数据一致性，比如在一个分布式系统中，你的数据可能被分区在不同的区域之类的。它可能会失去同步。比如一个数据库可能比另一个更前沿。然后是“可用性”（Availability），也就是这两台服务器或数据库是否都可以读取，或者也许其中一台宕机了。然后第三个是“分区”或者叫“分区容错性”（Partition tolerance）。所以这基本上意味着在一个分布式系统中，如果出现分区，如果可能系统断开了连接，某个东西宕机了，它会如何表现？所以这种“三选二”的框架被经常使用。但它不是非常准确。而且整个定理非常不完整。所以当我第一次学习它的时候，我想，你知道我喜欢深入研究事物，我喜欢真正透彻地理解事物。这就是我喜欢编程的原因，它是确定性的。就像如果你真的想，你可以深入到确切的代码行、汇编代码行、0和1，去确切地知道发生了什么。所以 CAP 定理对我来说感觉有点敷衍，我不太喜欢那样，这就回到了为什么我不喜欢工作中的某些事情，因为我觉得你没法深入到你想要的程度，你必须解决业务问题，哪怕这意味着你并没有真正理解某些技术细节。但这也没关系。但后来，当我看到 Martin Kleppmann 的一篇博客文章，谈论他有多么不喜欢 CAP 定理时，我感到非常有底气。实际上这还有点争议，因为那篇博客的评论区里有很多聪明人说，你知道，也许他在技术上是对的，但也许他有点吹毛求疵了，我认为这就像是一种个人偏好，但我只是觉得，像他这样的人同意我的观点，让我感到非常被认可，而且我觉得这有点好笑，因为我觉得我以前从来没见过有人这么说 CAP 定理，比如我看 Stack Overflow 上的帖子，没几个人真正提到它是不完整的。所以之后出现的是 PACELC，它指的是如果存在分区，你可以在可用性或一致性之间做出选择，但如果没有分区，那么你仍然需要做出权衡，也就是在延迟（latency）和一致性之间。所以它完整得多。我不明白既然有那个定理存在，为什么还会有人去学 CAP 定理，因为它就是更完整。而且它也没有复杂多少。我觉得它反而更容易理解。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, of course. Uh so, it's a pretty simple theorem. It's kind of described awkwardly sometimes, where it's you have like three choices, and you can pick two of three. There's consistency, uh and that's data consistency, so in like a distributed system where you have data that's like partitioned in different regions or something. It can go out of sync. Like one database might be more up-to-date than the other. And then there's availability, where are both of these uh you know servers or databases available to read or maybe one went down. And then the third one is a partition or partition tolerance. And so that basically means in a distributed system if there's a partition if maybe the system becomes disconnected one thing goes down the how is it going to behave? And so the two out of three framing is used a lot. It's not super accurate. And the entire theorem is very like incomplete. And so when I was learning it for the first time I thought you know I like to go deep into things I like to really really understand things. That's what I love about programming it's deterministic. Like if you really want to you can go down to the to the exact line of code the line of assembly the zeros and ones to know exactly like what was happening. And so CAP theorem felt like hand-wavy to me and I didn't really like that and that that goes back to why I don't like certain things about working on the job because I think like you don't get to go as deep as you like you have to solve the business problem even if it means you don't really understand some of the technical details. But that's fine. But later on I felt so validated when I saw a blog post from Martin Kleppmann talking about how much he didn't like CAP theorem. And it was actually a little bit controversial where I think there were plenty of smart people in the comments of that blog post that said that you know maybe he's like technically right but maybe he's you know being a little little bit nitpicky and I think that's like a personal preference but I just felt very validated that somebody like him agreed with me and I think it's it's kind of funny because I think I never saw anybody mention that about CAP theorem before like I saw like posts on Stack Overflow nobody really mentioned it's kind of incomplete. And so the the thing that came after it is like PACELC which is like if there's a partition you can choose either availability or consistency but if there's not then there's still a trade-off to be made which is latency and consistency. So it's much more complete. I don't understand why anybody would learn the CAP theorem when that theorem exists because it's just more complete. It's not that much more complicated. I think it's more simple to understand.

</details>

**Speaker B**: 我在想，是不是只有一小部分人会真正深入研究。你知道，像 CAP 定理，你实际上是觉得，好吧，让我把整个事情弄明白，然后你发现它是不完整的。但大多数人可能只是看了一眼，你知道，就接受了，好吧，这是定律，三选二，很简单，然后就翻篇了。我想在他们生命的大部分时间里，这就够了，或者他们甚至可能用不到它，或者到了时候，他们自以为懂，但实际上并不完全懂。所以这很有趣，因为我们在谈论软件工程师，你会认为大多数软件工程师都会深入研究细节，但我猜也许并非如此。

<details>
<summary>Original English</summary>

**Speaker B**: I wonder if it's only a smaller subset of people who actually go deep. You know, CAP theorem, you actually like, all right, let me understand the whole thing and then you realize it's incomplete. But most people might have just like looked at it, you know, took it, okay, it's the law, two out of three, simple enough, move on. And I guess in in most part of their lives, it's enough or they might not even use it or if when they they think they know, but they don't know it exactly. So, it's interesting cuz we're talking about software engineers and you would think that most software engineers go into the details, but I guess maybe not.

</details>

### 从深度优先搜索到智能体编程的转变

**Speaker A**: 是的，我认为这又回到了解决业务问题上，就像这就是我刚开始从事专业工作时不喜欢的地方，因为，好吧，比如你要看文档，对吧？你在参加入职培训。像在 Google，有那么多文档，有那么多内部工具。而我想要深入。我想对所有的文档链接进行深度优先搜索。就像，你知道，你有一篇博客或者一个网站，它引用了另外五个。那个又会引用另外五个。我想把每一个都看一遍，对所有的东西都有一个完整的了解。但这在工作中根本行不通。甚至是一个代码库，没有任何一个人能理解这么庞大的代码库，除非全是你自己写的，而公司根本不是这样运作的。现在我们算是看到了类似的转变，我想很多人现在也在经历智能体编程（agentic coding）的转变，因为它的概念有点类似，就像现在你甚至可能根本不看你自己实际生成的代码。所以，这有点类似，我觉得这整个转变有点让我想起那个，就是你没法做一些你曾经享受的事情，但这就是生活，[哼笑]这就是生意。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, I think it goes to like solving the business problems and just like this is what I didn't like when I started working professionally because okay, so you go through like documentation, right? You're going through onboarding. Like at Google, there's so much documentation, there's so many internal tools. And I want to go deep. Like I want to do depth-first search on all the document links. Like, you know, you have one blog or you have one site and it has it references like five others. That one is going to reference five others. Like I want to go through every single one, have like a complete understanding of everything. But that's just not how it works at jobs. Even a code base, no one person is going to understand this massive code base unless you like write all of it by yourself, which is just not how companies work. And now we're kind of seeing a similar transition I think a lot of people are going through now with like agentic coding because it's kind of a similar concept where it's like now you might not even be looking at the code that you're actually producing yourself. So, it's it's kind of similar and I think this whole transition kind of reminds me of that where it's like you don't get to do some of the things that you used to enjoy, but it's it's still you know, that's that's life, [snorts] that's business.

</details>

### 大厂入职与闪电离职

**Speaker B**: 所以，你从华盛顿大学毕业，然后开始在西雅图最理所当然的选择里工作。我想在西雅图，两个最理所当然的选择就是亚马逊或微软，然后你进了亚马逊，这本应该是一帆风顺的。就像你，你成功进入了大型科技公司，进入了顶级联赛，但两个月后你就辞职了。那里发生了什么？

<details>
<summary>Original English</summary>

**Speaker B**: So, you graduated from University of Washington and you started work at the most obvious choice in Seattle. I guess the in Seattle the two obvious choices are Amazon or Microsoft and you got into Amazon and it should have been a smooth ride. Like you you made it into big tech into the big leagues and then you quit after 2 months. What happened there?

</details>

**Speaker A**: 是的，首先我想说我实际上上的是华盛顿州立大学（Washington State University），因为我……是的，我实际上没有被华盛顿大学（University of Washington）录取。我想去那里，但我在高中不是最好的学生。所以我很幸运，为了面试我拼命刷题，而且 GPA 也不错。所以我在亚马逊得到了一些面试机会，而且是和数据结构与算法（DSA）相关的，所以我能够，你知道，搞定那些。然后一旦我真正进入职场，这是我对自己很有自知之明的一点，就是我……

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, first I want to say I actually went to Washington State University because I Yeah, I was actually not accepted to University of Washington. I wanted to go there, but I was not the best student in high school. So, I was fortunate enough that I grinded super hard for interviews, had a pretty good GPA. So, I got some interviews at Amazon, and it was DSA related, so I was able to, you know, crank that out. And then once I actually got into the world, and this is something I was self-aware about where I

</details>

<!-- chunk 3/13 -->

### 亚马逊的艰难开局

**Guest**: 我当时就非常清楚，自己在人际交往、社交技巧以及这方面的事情上，绝不是一个面面俱到的人。我能够独自坐着，仔细研读说明文档，埋头苦干处理各种事务，但是要和其他人一起共事，对我来说真的是一件非常非常困难的事情。在亚马逊（Amazon），我当时所在的部门是 Alexa。据我现在的了解，在大型语言模型（LLMs）的冲击下，这个部门几乎已经被掏空了。但我当时具体所在的那个团队，以及我认为整个 Alexa 部门，总体来说都不是一个理想的工作场所。它并不是一台运转良好的机器，有很多事情都需要手工去处理。那是一个让人感到非常充满压力的工作环境。我记得我刚加入的时候，在内部通讯工具上看到了一条消息。我记得当时他们用的是 Chime，有个人在上面说：“这感觉就像是一份吃力不讨好的工作。”我当时正在翻阅团队频道的历史记录。那是我入职前大概一周的事情。我当时的反应是：“哇，好吧。所以，目前这显然不是一个积极向上的团队环境。”我觉得他们其实都是很好的人，我绝对不怪他们中的任何一个。我甚至对亚马逊也没有任何怨恨。那纯粹只是一个很糟糕的处境而已。所以，事后回想起来，如果我必须重来一次的话，我可能也能生存下来。因为我现在多多少少懂一些职场的生存之道了。无论如何，那都会是一段充满压力且糟糕的经历，但我应该能够挺过去。但在当时，我真的什么都不懂。而且，我当时还有很多个人的问题需要去处理。因此，不管出于什么原因，我当时就是非常冲动地做出了直接辞职的决定。辞职之后，我有点后悔了。因为，你知道的，我一开始确实感到了一丝解脱，但紧接着我感觉更糟了，因为我心想：“好吧，那我接下来该怎么办呢？”

<details>
<summary>Original English</summary>

**Guest**: knew I was not a well-rounded person in that like working with people, people skills, and just anything of that. Like I could sit by myself, go through like documentation, work on things, but like working with other people was very very like difficult for me. At Amazon, the org I was in Alexa, which is kind of been gutted from what I hear nowadays with LLMs, but the team I was specifically in and I think Alexa the org in general was not the best place. It was not a well-oiled machine, a lot of manual stuff going on. It was a really stressful environment. I think when I joined I saw a message on the internal thing. I think it was I think they use chime at the time, but he said, "This feels like a thankless job." And I was like I was going through the history of the the team channel. This was like a week before I joined. I was like, "Whoa, okay. So, this is like clearly not like a positive team environment right now." I think they were all like decent people. I don't blame any of the individuals. I don't even hold a grudge against Amazon. It was just a crappy situation. And so, I think in hindsight, like if I had to do it over again, I'd probably be able to survive. Like I kind of know things. It would have been stressful and and crappy either way, but I would have been able to get through it. But at the time, I just didn't really know. And like I had a lot of like personal issues at the time. And so, for whatever reason, I just made a very like impulse decision to just leave the job. Afterwards, I kind of regretted it because like, you know, I felt like a little bit of a relief, but then I just felt a lot worse because I was like, okay, now what do I do?

</details>

**Host**: 那么，你能不能给我详细讲讲，刚加入的时候具体是什么感觉？你知道，比如第一印象是什么，入职培训（onboarding）是怎么样的，还有哪些事情让你觉得根本说不通？

<details>
<summary>Original English</summary>

**Host**: And then can can you tell me through on like what it felt joining, you know, like the the first impressions, what the onboarding was like, and what were the things that were just were like not adding up?

</details>

### 高压环境与入职体验

**Guest**: 那真的是非常紧张和高压的。我们开了一个会，因为有大概五六个应届毕业生在短短一两周的时间内相继加入了公司。是为了同一个团队？是的。而且我记得当时团队里已经有大概四位经验丰富的工程师了。所以，他们等于是把团队规模扩大了一倍多，而且大部分都是新人。按理说你会想：“好吧，如果引进了这么多新人，显然需要对他们进行入职培训，让他们快速进入工作状态。”但他们当时有很多截止日期（deadlines）需要应对，所以情况有点像：那些有经验的工程师都在埋头苦干，而我们剩下的这些新人就只能靠自己了。然后我们开了一个会，就是那种用来向大家介绍新人的会议，对吧？然后，我还是要强调，我不怪任何一个人，但当时的情况是，没有人说一句话。那些有经验的工程师，他们就是一言不发。经理不得不一直像是在催促或者引导他们说话，让他们表现得友好一点之类的。我觉得他们当时只是想让这个会议赶紧结束，这样他们就能回去继续完成他们的工作，因为他们有截止日期要赶。我看到有人，我不是只针对某一个人，是团队里每一位有经验的工程师，都在凌晨三点提交代码（committing），而我们第二天早上八点或九点还要开会。而且有些人甚至在同一时间（凌晨三点）还在审查代码合并请求（PRs）。所以，我不知道这是否是一种既定的文化。我不认为经理会直接告诉他们：“你们必须这样做。”我觉得这是一种心照不宣的潜规则。意思就是，你知道现在是一个高压的环境，如果你是那个唯一没有在凌晨三点工作的人，那你可能就会成为第一个被公司踢出门的人。

<details>
<summary>Original English</summary>

**Guest**: It was very intense. So, we had a meeting cuz there were like five or six new grads who joined like within a one to two-week period. For the same team? Yeah, and I think there were like four experienced engineers already. And so, like they over doubled the team and mostly new people. So, you'd think, okay, well, if you introduce a bunch of new people, you're going to obviously onboard them, like get them up to speed. But they had a lot of deadlines that they were dealing with, so it was kind of like the the experienced people were just working and the rest of us were kind of just like on our own. And so, we had a meeting where it was like one of those where you're just kind of like introducing the new people, right? And like again, I don't blame any of the people, but they were like nobody said anything. The experienced people, like they did not like say anything. The manager had to like kind of keep like prompting them to like talk and to be friendly and stuff. And I think they just wanted the meeting to end so they could go back and like finish their work because they had deadlines to meet. I saw people, and I'm not saying one person, every one of the experienced engineers was committing 3:00 a.m. and we have like 8:00 a.m. or 9:00 a.m. meeting in the morning tomorrow. And some people are reviewing the PRs at the same time. So, I don't know if it's this culture where like I don't think the manager told them you have to do this. I think it's like implicit where it's like you know, you kind of know that it's a stressful environment right now. If you're one person who's not doing it at 3:00 a.m., you're going to be the first in line to maybe get kicked out of the company.

</details>

**Host**: 是的，而且我想说，亚马逊在那个时候，他们有一个目标，就是每年要有 6% 的无遗憾离职率（unregretted attrition）。这意味着在这个级别的经理或总监，必须要让 6% 的人离开公司，并且被标记为无遗憾离职。这就意味着，要么是员工自己主动辞职，然后你说：“哦，其实这个人表现不太好，走了不可惜（无遗憾）”；要么就是你需要把一些人放进绩效改进计划（PIP）里，然后让他们离职，并宣称：“是的，这就是无遗憾离职。”所以，在亚马逊的一些部门，甚至大多数部门里，竞争是相当残酷的。

<details>
<summary>Original English</summary>

**Host**: Yeah, and also, I mean, Amazon at the time, they had a target of 6% unregretted attrition every year, which meant that managers or like directors at their level had to have 6% of people leave the company unmarked as unregretted, which meant that either people quit on their own and you said like, oh, actually, this person was not great, unregretted, or you need to put people on performance improvement plans, and then have them leave and say like, "Yep, that was unregretted attrition." So, it's somewhat cutthroat in some of the orgs or most of the orgs.

</details>

### 离职与文化不适应

**Guest**: 是的，我对这件事甚至有一点阴谋论的猜想。因为我记得我实际上递交了三次辞呈，他们才最终在某种程度上接受了它。这让我感到非常惊讶。我当时就想：“为什么他们甚至在第二次的时候都不肯接受我的辞职？”我心里琢磨，也许这是因为如果是这样的话，它看起来会很糟糕。因为这样算作是有遗憾的离职（regretted attrition），情况就变成了不是你们解雇了他们，而是他们自己选择离开。而且，因为我入职的时间太短了，我觉得当时的时间还不足以让我被放进 PIP。我想你可能要在入职 3 到 6 个月左右才会被放进那个计划。但我才入职 2 个月就离开了。我再说一次，我不怪任何一个人。我对任何经理都没有怨恨，甚至包括我的隔级经理（skip manager），因为我记得在我准备辞职的时候，他们对我说：“是的，有时候我们确实会让一些人离开之类的，但我并不这么看。我只是把这看作是文化上的不契合。”所以，他们试图表现得很友好。但话又说回来，他们甚至都没有试图去掩饰这一点。很明显，那里的文化就是非常高压的。有些人可能会用“有毒（toxic）”这个词。为了说得稍微客气一点，我用了“高压（intense）”这个词，但事实就是如此。

<details>
<summary>Original English</summary>

**Guest**: Yeah, I almost have like some conspiracy theories about that because I think I gave my resignation actually three times before they finally like accepted it in a way, which was surprising to me. I was like, "Why don't like they accept the resignation even after like the second time?" I was thinking like maybe this is like because like it looks bad because it's regretted attrition where it's like you didn't let them go, they chose to leave. And and since it was so early, I think it was too early for me to even be on PIP. I think you get that like within 3 to 6 months or something. I left like 2 months in. And again, I don't blame any of the people. I have no grudges against any of the managers, even the skip manager, because I remember when I was quitting, they told me like, "Yeah, like sometimes we do get let people go and stuff like that, but I don't see it that way. I just see it as like a bad culture fit." And so, they were trying to be nice about it, but again, it was it was they weren't even trying to hide it. Like it was obvious that the culture is like intense. And some people would say toxic. I'll use the word intense to be more generous, but yeah.

</details>

### 从亚马逊到谷歌

**Host**: 后来，在过了很多个月之后，你成功入职了谷歌（Google）。相比于亚马逊，加入谷歌的感觉如何？

<details>
<summary>Original English</summary>

**Host**: Later on, you were able to get into Google many months later. How did joining Google feel compared to Amazon?

</details>

**Guest**: 那是完全相反的体验。在很多方面，它们是两家截然相反的公司。比如商业文化，甚至技术文化，以及所有相关的方面。但我当时有点像是处于一种“亚马逊创伤后应激障碍（PTSD）”的模式中。我就觉得：“好吧，那是我第一次算是真正的职业经历。”我把那种经历外推了，认为在所有大型科技公司，甚至普遍的职场环境中，都是那样的。所以我就想：“好吧，你不应该去问问题，你不应该和别人交流，你甚至都不应该表现得友好，你就应该拼命工作，并且尽可能地保持那种紧绷的高压状态。”但是，那里的人对我非常友好，所以我也就顺理成章地对他们做出了友好的回应。可是，我还是没有提问，我非常害怕去问问题。所以在大部分时间里，我都是在独自工作。后来，我的经理交给我一个项目，结果证明这个项目比它原本应该有的难度要大得多。但我依然处于那种“我必须把它搞定”的模式里。我就觉得：“这是我的项目。我必须独立完成它。”在这方面，我非常幸运，因为我确实遇到了一位非常支持我的经理，以及一个非常支持我的团队。因为我选择几乎由自己包揽了所有的工作，经理和团队就把我看作是一个非常独立自主的人，而这正是你从初级工程师晋升到中级工程师所必须具备的特质。正因为如此，我非常幸运地获得了非常快速的晋升。这极大地帮助我建立起了自信心。这也让我意识到：“好吧，我现在可以开始提问了。”这其实挺搞笑的。就是说，在我获得晋升之后，我才感觉可以更加心安理得地去问问题了，但通常情况下，你会更期望一个初级工程师去多提问。

<details>
<summary>Original English</summary>

**Guest**: It was the opposite experience. And they're kind of opposite companies in a lot of ways. Like the business culture, even the tech culture, and all that. But I was kind of in like Amazon PTSD mode where I was like, "Okay, like that was my first kind of like real professional experience." I extrapolated that to be like everywhere in big tech or even just professionally in general. So, I was like, "Okay, you you're supposed to not ask questions, you're supposed to not talk to people, you're supposed to not even be friendly, you're supposed to just like work, and and just be as intense as possible." But people were very friendly to me, and so I kind of reciprocated that. But I didn't ask questions. I was very scared to. So, I worked on my own for the most part. And I was given a project uh from my manager that turned out to be more difficult than it was supposed to be. But I was still in the mode where I was like I just got to get it done. Like this is my project. Like I have to do it independently. And so that I was very fortunate in that where I did have like a very supportive manager, a very supportive team. And because I chose to do pretty much all the work by myself, the manager and team saw me as like independent, which is what you need to do to get promoted from like junior to mid-level. I was very lucky to get promoted like very quickly because of that. And that helped me build my confidence a lot. That made me realize like okay, like I can start asking questions now, which is funny. Where like after I got promoted is when I was like more comfortable like asking questions when like you'd expect that from a junior engineer more.

</details>

### 企业文化的延续与冲突

**Host**: 这太有意思了，因为当你又过了 6 个月左右加入谷歌的时候，你在亚马逊实际上只有大概 2 个月的专业工作经验。然而，当你进入一家新公司时，你的内心却已经根深蒂固地形成了很多条件反射。所以你几乎可以想象，像另一位工程师，如果他之前有过两三份工作，你知道，他们可能已经积累了所有这些从其他公司文化或他们以往的经验中带来的固有思维和行为模式。当他们加入新公司时，他们可能很难去适应这家新公司的文化。是的，我不确定我们在整个行业里是否充分考虑过这个问题。

<details>
<summary>Original English</summary>

**Host**: This is so interesting because you've only at that point had maybe 2 months of professional experience working at Amazon when you joined Google another 6 months or so later. And how you can have a lot of reflexes ingrained in you coming into a company. So you can almost imagine like another engineer who had like two or three jobs before, you know, they might have built up all these onset things that are coming from other companies' cultures or what they've learned. And they when they join, it it can be hard for them to adapt to to the company. Yeah, I'm not sure we think about this in the industry.

</details>

**Guest**: 是的，我觉得你提到这个挺有趣的，因为我当时在谷歌云（Google Cloud）部门，那里有很多领导层的人都是从其他公司跳槽过来的，比如亚马逊。我们有一位副总裁（VP）或者总经理（GM）。他是从亚马逊跳槽过来的，只待了几个月。然后，在很短的时间之后，他实际上也离开了。我不知道这背后确切的故事，但我认为在整个行业里，确实有很多文化是会被“映射”或者说带到新环境中的。很多在谷歌的人并不喜欢亚马逊带来的这种风气。

<details>
<summary>Original English</summary>

**Guest**: Yeah, I think it's kind of funny you mentioned that because I was in Google Cloud where a lot of the leadership was from other companies like Amazon. And we had a VP or or GM. He joined it from Amazon for a few months. And he actually left shortly after that as well. Like I don't know the exact stories behind that, but I think there is a lot of like in the industry a lot of culture can get like mapped. A lot of people at Google didn't like the Amazon

</details>

<!-- chunk 4/13 -->

### 谷歌的晋升与企业文化

**Guest**: 经理们会想，哦，他们不太可能会带我们去旅行或者为我们买单，因为他们知道亚马逊有这种节俭的文化，而谷歌没有。但是慢慢地，当我在那里的时候，情况开始逐渐朝着那个方向发展，特别是在裁员之类的事情发生之后。

<details>
<summary>Original English</summary>

**Guest**: managers because it's like oh, they're going to be less likely to like take us on a trip or pay for us because they know that Amazon has like the frugality and Google doesn't. Uh but slowly like while I was there, it slowly started to get going that direction, especially with the layoffs and all that.

</details>

**Interviewer**: 在谷歌获得晋升，需要具备什么条件？这意味着什么？我知道有晋升材料，也知道有评估委员会。从你的角度来看，你观察到了什么？

<details>
<summary>Original English</summary>

**Interviewer**: Getting promoted at Google, what does it take? What does it mean? I know there's promotion packets. I know there's committees. What did you see from your perspective?

</details>

**Guest**: 我觉得非常直接明了。从初级晋升到中级可能比从中级晋升到高级更容易，越往上走就越难。就我的情况而言，主要还是看能否独立工作。然后，我有幸在大概一年，几乎整整一年的时间里获得了晋升，这在谷歌是非常罕见的。我可以坐在这里，可能还带着点凡尔赛地表现得好像我就是个超级天才。但我认为，实际上你必须首先投入努力，其次要相当聪明，不过我觉得绝大多数人都足够聪明。我认为这还涉及到了其他方面，也就是合适的团队、合适的项目，因为如果你没有遇到合适的项目，你就无法证明自己。你可能是一个 10 倍甚至 100 倍效率的工程师，但如果你做的都是些相对简单的工作，你很难说自己解决了一个真正困难的问题。所以，我认为很大程度上取决于这些。谷歌有大量的文档工作，每一件事都需要用一些指标或者文档记录来支撑，比如设计文档。所以他们有这样一种文化，可能会为非常简单的事情编写过多的设计文档。有些人不喜欢这样，但我认为就流程而言，在谷歌这只是一个“必要的麻烦”，因为否则的话，有些工程师可能就会只做他们想做的事情，对业务没有任何影响，而这样就很难去量化他们的贡献了。

<details>
<summary>Original English</summary>

**Guest**: Pretty straightforward, I think. Like going from junior to mid-level is probably easier, I think, than from mid-level to senior and as you get higher and higher. In my case, it was mostly just about like working independently. And then once like I was lucky to get promoted, I think in about a year, almost exactly a year, which is very uncommon at Google. And I could sit here and probably humble brag and act like I'm just like this super genius. But I think it was really I think there's like you have to one put in the work, two be reasonably smart, but I think vast majority of people are reasonably smart enough. I think it's it goes into the other things where it's just right team, right project, cuz if you don't get the right project, there's no way you can prove yourself. You could be a 10x, 100x engineer, and if you're working on relatively easy stuff, you can't really say that you solved like a really hard problem. So, I think it takes a lot of that. Google has a lot of like documentation where it's like every single thing needs to be supported with like some metrics or some artifact, like some design doc. And so, they have like this culture of probably producing too many design docs for really simple things. Some people don't love that, but I think in terms of like processes, it's just a necessary evil at Google because otherwise, some engineers might just like work on stuff that they just feel like working on, there's no impact to the business, and so it's hard to kind of like quantify that.

</details>

### NeetCode 的起源与发展

**Interviewer**: 然后在业余时间，甚至在加入谷歌之前，你就创办了现在被称为 NeetCode 的项目，很多观看或收听节目的观众都会因为这个项目而认识你，甚至熟悉你的声音。你能告诉我这一切是如何开始的，以及你在谷歌工作期间是如何坚持下去的吗？

<details>
<summary>Original English</summary>

**Interviewer**: And then on the side, even before Google, you started what is now known as NeetCode, and a lot of people watching or listening will know you for you or even your voice from there. Can Can you tell me how that all started and how it continued as you were working at Google?

</details>

**Guest**: 是的，其实最初是在我离开亚马逊之后开始的，大概是六年前吧。我做这个纯粹是为了好玩，也是出于对这件事的热爱，因为……

<details>
<summary>Original English</summary>

**Guest**: Yeah, so I initially started after I quit Amazon, I think, in like 6 years ago. And I was doing it really just for fun and for the love of the game because of

</details>

**Interviewer**: 你当时在录制视频，对吧？

<details>
<summary>Original English</summary>

**Interviewer**: You were recording videos, right?

</details>

**Guest**: 是的，我当时在做这些教程类的视频。我心想：“我现在正在学这些，反正闲着也是闲着，还不如帮帮其他人。”而且我发现这非常困难，因为当时并没有什么真正的教程，只有很多论坛上的帖子，里面全是非常复杂的解决方案。我就坐在那里，绞尽脑汁地想要去理解。我认为大多数人其实都不理解那些解决方案，因为确实很难。我觉得大部分人只是看了看算法，有一个大概的高层次理解，并不完全知道它为什么有效，但这通常已经足够了，如果在面试中遇到那道题，你很可能就能通过面试。而这又回到了“深度思考”的问题，我认为这是一种技能，对我来说更像是一种性格特征，但我觉得这在刷 LeetCode 时帮了我大忙。我对那些在当时看来毫无意义的事情进行了非常深入的研究，比如你做了一个只有 50 个人看的视频，你做得非常好，但很明显，这不值得你花好几个小时去做。但我还是坚持做了，因为我喜欢。大概在我开始持续制作视频一年后，我确实进入了谷歌。能做到这一点我感到非常幸运。那时候面试过程已经变得相当容易了，谢天谢地。所以我有点放缓了做视频的节奏。我当时觉得，这挺好玩的，但我现在在谷歌了，我余生都会……

<details>
<summary>Original English</summary>

**Guest**: Yeah, I was making these like tutorial videos. I was like, "I'm studying this right now. I got nothing better to do. I might as well like help some other people." And I found it very difficult because there weren't really tutorials at the time. There was just a lot of like forum posts of these really like complex solutions. And I'm like sitting there banging my head against the wall trying to understand it. And I think most people didn't understand the solutions because it's it's very hard to. Like I think most people just looked at the algorithm, kind of had a high-level understanding of it, didn't quite know why it worked, but it was good enough usually to if you saw that question in an interview, you could probably pass the interview. And uh this goes back to like deep thinking, which I think was a skill that it's more of a personality trait for me, but I think it helped me a lot with like the LeetCode stuff. I went really deep into things that at the time felt kind of meaningless, where it's like you make this video for 50 people watching, and you you you you did a great job, but it like clearly like it's not worth the several hours it takes to do that. But I kept doing it cuz I enjoyed it. About a year after I started making the videos consistently, I think I did get into Google. Very fortunate to do that. Interview process was pretty easy at that point, thankfully. So I kind of backed off the videos. I was like, this is kind of a like like it was fun, but I'm a like I'm at Google now for the rest of my

</details>

**Interviewer**: 你没有拿到你的……是的。

<details>
<summary>Original English</summary>

**Interviewer**: your You didn't have your yes.

</details>

**Guest**: 是的。后来我看到，其实我发了一个视频告诉大家：“伙计们，顺便说一下，我进谷歌了。你们可能不会那么经常看到我了。”有趣的是，在那之后，频道数据开始呈指数级增长，因为我认为这增加了极大的可信度。大家会觉得：“好吧，这家伙不是在进入谷歌之后才做这些视频的，他是在进去之前做的。”所以，这就是他的经历，然后他进去了。所以，这就像是世界上最好的推销。就像我证明了它，我实现了从零到一的突破。所以，我想这是一个非常好的卖点。这其实让我个人有点困扰，因为视频内容并没有变，对吧？只是品牌变了，但这却产生了巨大的影响。对，所以在数据呈指数级增长之后，我就想：“好吧，也许我会做一个网站。”那时候网站是完全免费的，基本上就是视频的目录，方便大家使用。而且那个网站也火了。后来在获得晋升后不久，我就在想：“嗯，也许我可以尝试全职做这个。”因为我真的很喜欢它。在谷歌我没法像我希望的那样深入研究，我必须去解决业务问题，但对于算法和数据结构，我可以钻研得非常深，比大多数人愿意去了解的程度都要深得多，但我有理由这么做，因为：“好吧，我可以把这些东西解释给别人听。”所以是的，我想这对我来说恰好是个合适的时机。后来，谢天谢地，至少到目前为止，一切都很顺利。但是……

<details>
<summary>Original English</summary>

**Guest**: Yeah. And then I I saw that actually like I made a video telling people like, "Hey guys, I got into Google, by the way. You might not see me as much anymore." And and funny enough, after that, the channel like went exponential because I I think it added like so much credibility. It's like, "Okay, this guy didn't make these videos after he got into Google. He actually made it before." And so like this is what he did, and then he got in. So it's like it's like the best sales pitch in the world. Like I I proved it. Like I went from zero to one. And so it was I guess a really good selling point. And it kind of bothers me personally because it's like the videos didn't change, right? Like the branding changed, but that made like a really big difference. Yeah, and so so after it went exponential, I was like, "Okay, maybe I'll make like a website." And then the website was completely free at the time, which is really a catalog of the videos to make it easy to use. And um that went viral as well. And then so pretty shortly after I got promoted, I was like, "Huh, like maybe I can like try this full-time." cuz I really loved it. I I couldn't go as deep as I wanted to at Google. I had to solve business problems, but with algorithms and data structures, I can go super deep, more deep than most people would ever want to go into those things, but I had a reason to because it's like, "Okay, I can explain these things to people." And so yeah, I think it was just it was like the right timing for me. And then afterwards, uh thankfully it's like worked out so far. But

</details>

### 在谷歌和创业之间的抉择

**Interviewer**: 你当时在谷歌，刚刚晋升到 L4，这仍然算是中级，但你现在有了通往 L5 的路径，我的意思是，那时候 L5 算是终端职级。现在 L4 已经是终端职级了，但你知道，在谷歌你可以升到 L6、L7、L8，成为首席科学家。你当时有继续留在谷歌做这些事情的路径，也有选择创业，或者把这件事变成你的事业并深入算法编程的路径。你当时是如何考虑这两个选择的？你会放弃什么？或者说，你知道，这两种选择分别有多大的风险？

<details>
<summary>Original English</summary>

**Interviewer**: you you were at Google. You just got promoted to L4, which is still mid-level, but you now had a path to L5, which I mean, it used to be the terminal level at the time. Now L4 is a terminal level, but you know, in Google you could go to L6, L7, L8, principal scientist. You had that path of like staying inside Google, do this stuff or start your business or turn this into business and go deep into algo coding. How were you thinking of the two options and what you would give up or what kind of, you know, how much risk would one or the other have?

</details>

**Guest**: 是的，我想了很多，因为尽管我不喜欢谷歌的某些方面，但我其实还是很喜欢这家公司的。我喜欢那里的同事，而且那里并不是一个压力极大的环境。当我离职的时候，我的技术主管——当时他基本上就是我的经理，因为我的经理已经……

<details>
<summary>Original English</summary>

**Guest**: Yeah, I thought about that a lot because even though I I didn't love certain things about Google. I actually really liked the company. I liked the people and it wasn't this super stressful environment. And when I was leaving, my TL, who was basically my manager at the time because my manager had

</details>

**Interviewer**: 还是技术主管，对吧？

<details>
<summary>Original English</summary>

**Interviewer**: Still being tech lead, right?

</details>

**Guest**: 对，技术主管。他当时有点疑惑地问我。他说：“我很不解你为什么要走，因为你晋升得非常快，而且你很可能还能再次晋升。”我确实认真考虑过这个问题，因为看起来……因为那就是我下半辈子要做的事情。我会在谷歌工作，我会获得晋升，我会成为我能成为的最优秀的工程师，但我只是觉得，这就像是一个时机，我有机会自己去尝试一些东西。也许这样的机会不会永远存在。即使到今天，谷歌也让员工离职变得很容易，如果你离职了，只要你和团队的关系还不错等等，通常你可以在一年内回来，谢天谢地，我当时也是。所以这让我的决定变得稍微容易了一些。我经常有朋友在做同样的决定。他们会问我：“我应该离开谷歌吗？”上周我刚有一个朋友问过。她想全职做内容创作。我觉得现在这几乎成了一种趋势，每个人都辞掉工作去做自己的事情，但是……

<details>
<summary>Original English</summary>

**Guest**: Yeah, tech lead. And he he kind of asked me. He said, "I'm a bit perplexed that you're leaving because you got promoted very quickly and you could probably get promoted again." And like, I did think about that a lot because it seemed like because that was what I was going to do the rest of my life. I was going to work at Google. I was going to, you know, get promoted. I was going to be like the best engineer I could be, but I just felt like the the timing of it like I had a chance to to try something by myself. Maybe that opportunity isn't going to be there forever. Google does make it easy for people even to this day, if you leave, you can usually come back within a year if you're on like good standing with your team and stuff like that, which thankfully I was. So that kind of made it a little bit easier. I have friends all the time that are making like the same decisions. They're asking me like, "Should I leave Google?" I just had a friend last week. Uh she wanted to like do content creation full-time. I think it's like a trend almost these days where everybody's quitting their job to do their own thing, but

</details>

**Interviewer**: 嗯，我的意思是，我认为这是一种趋势，就像我们总是生活在各自的信息茧房里，对吧？但在某些圈子里，确实如此。这个转变的过程是怎样的？你能告诉我，比如你当时其实已经……好吧，你做出了决定，你从那种有非常有条理的工作日程、有团队、一切都安排妥当的状态中跳出来了。谷歌有惊人的内部基础设施。你只需要专注于……好吧，当时业务上的问题还是写代码。而现在你就像，好吧，你有网站，你有 Git 仓库。这个转变是怎么样的？然后你觉得，什么……

<details>
<summary>Original English</summary>

**Interviewer**: Well, I mean, I think a trend that in like we always live in bubbles, right? But but but in in like certain bubbles it it is. How was the switch? Can you tell me like you actually went from like okay, well, you made the decision, you went from like having a really structured work day, a team, everything was figured out. Google has amazing internal infra. You can just focus on okay, the business problem was still coding. And now you're like okay, you have the website, you have Git repository. What What was the switch like? And and you're like What

</details>

<!-- chunk 5/13 -->

### 离开谷歌后的挑战与工具转换

**Interviewer**: 之前在谷歌工作的时候，有什么有趣的地方，或者觉得很好、很好玩的事情吗？又有哪些困难？

<details>
<summary>Original English</summary>

**Interviewer**: was interesting about it or like good and fun? What was difficult?

</details>

**Neet**: 我在谷歌的时候，在学习曲线上遇到了一段比较艰难的时期，但在我离开之后，我发现想要摆脱他们的一些工具也很困难，因为你很快就会习惯它们。比如大家都用的 GitHub，我就不是特别喜欢。我知道现在有很多人在抱怨它，比如它的正常运行时间问题等等。但我对它还有其他方面的不满，比如用户体验之类的问题。我觉得谷歌有一些内部工具确实不怎么样，但也有一些内部工具简直好得不可思议。而且有很多公司的创立，仅仅是因为有些人在谷歌工作时参与构建了某些工具，然后他们觉得：“嘿，我们可以把它做成一个公开的产品。”于是他们离职，创办了像 Cockroach Labs 这样不可思议的公司。

<details>
<summary>Original English</summary>

**Neet**: I had a tough time with the learning curve at Google, but once I left, I had a tough time like transitioning away from some of the tools because you get used to it very quickly. Like they have like GitHub, I'm just not a huge fan of it. I know a lot of people are hating on it nowadays with like the uptime issues and stuff like that. But I have other issues with it around like UX and stuff. I think Google has certain internal tools that aren't so great, but they have some that are just like super super good. And there's have been a lot of companies that have been started just because like some that you had at Google built something and then they're like, "Hey, we could make this public." So, then they leave and then they start like Cockroach Labs or something crazy.

</details>

### 团队管理与领导力的感悟

**Interviewer**: 那你从在一个团队中工作，变成现在必须独自一人包揽所有事情，这种转变对你来说是个问题，还是你觉得很自然？

<details>
<summary>Original English</summary>

**Interviewer**: What about like you went from from working on a team and now you just had to do everything by yourself. What was that an issue or that was kind of natural to you?

</details>

**Neet**: 是的，那对我来说其实是一个巨大的挑战，建立团队很难，与人合作也很难。就像我一开始说的那样。直到最近，我想大概是过去 6 个月内，我才开始习惯，现在我终于觉得在分配任务和管理人员方面感到自如了。我花了好长的时间才终于开窍，要知道，你会经历很多事情。你招了一些人，然后又不得不解雇他们。你得弄清楚什么是行之有效的，什么是合适的人选，甚至只是如何去激励别人。与人合作是一件非常不同的事情，因为每个人都不一样。他们不像 AI 智能体那样，你给它一个任务，它就像机器一样去执行，直接把代码吐出来。人就是人。所以这类事情对我来说是一个巨大的学习曲线。虽然我以前很讨厌这些，但现在我其实非常喜欢，因为当它真的奏效时，当你找到一个合适的人，并且你觉得你可以为他们的成长做出贡献。你可以稍微引导他们一下，你可以掌控一下方向，然后你会看到这对他们产生了多大的改变。现在当领导力发挥作用的时候，我终于明白它意味着什么了。就像当你是一个高效的领导者时，你甚至能在一个小团队里产生巨大的影响，我能想象如果你到了更高的管理层，那将带来多么巨大的改变。你有时也会在公司 CEO 身上看到这一点，当一位新 CEO 接管整个公司时，公司要么蒸蒸日上，要么可能会走向另一个方向。所以。

<details>
<summary>Original English</summary>

**Neet**: Yeah, that was actually a huge thing for me where I It was hard to build a team. It was hard to like work with people. Like I kind of said at the beginning. And I've only just recently, I would say within the last like 6 months, gotten used to it where now I finally feel comfortable like delegating things and like managing people. And finally like it it took a long time for me, but once it finally does click, you know, you go through like so many experiences. You hire some people, you have to let them go. You figure out what works, what's a good fit. And even just how to like motivate people. It's a very different thing like working with people cuz everybody's different. They're not like agents where you just give them the task and they're a machine. They're just going to spit out the code. Like people are people. And so those types of things there was a huge learning curve for me. But now and I hated it before, but now I actually really love it because it's like when it does work when you find somebody and they're a good fit and you feel like you can contribute to their growth. You can like guide them a little bit. Like you can steer the ship a little bit and you see like how much of a difference that makes to them. Like now I finally understand what leadership means when you like when it works. Like when you're an effective leader like you can make a magnitude of difference in like even like in a small team, but I imagine like as you get to higher and higher levels it can make a huge difference. And you see that with CEOs sometimes when a new CEO takes over the entire company either can go like up or maybe it goes in the other direction. So

</details>

### 早期技术栈与产品核心价值

**Interviewer**: 当你刚起步的时候，比如你从谷歌辞职，你有一个列出你视频的网站，我猜就是非常简单的 HTML、CSS，也许还有一点 JavaScript。你当时构建了什么？背后的技术栈是什么？

<details>
<summary>Original English</summary>

**Interviewer**: When you started so like you quit Google you had a website that listed your videos I guess very simple HTML CSS maybe a bit of JavaScript. Uh what did you build and what what was the tech stack behind it?

</details>

**Neet**: 是的，最初我做那个免费网站的时候，我还在谷歌工作。所以我直接随便选了一些谷歌的工具。我当时用了 Google Cloud Firebase，因为它用起来太简单了。我现在有点后悔那个选择，因为现在我认识了那么多人，我就会想，哦，也许我现在应该用 Convex。我当时本该尝试一些不同的东西，但我当时也用了 Angular，那是我在谷歌时用的技术。所以我当时觉得这样也挺合理，也许我还能顺便学习一下。这个选择我也后悔了。不过幸好我们现在有了大语言模型 (LLMs)。所以迁移东西变得相对容易了。所以也许那是我将来会去做的事情。但就构建应用程序本身而言，不知为什么，我就是没觉得那有多大意思，因为通常并没有那么多深层次的问题。我觉得有趣的事情来自于创新，以及用人们在意的方式做事。因为没有谁会特别在乎我网站的性能、我用的技术栈，或者任何这类细枝末节的东西。他们会在乎用户体验，比如我在视频里把一个问题解释得好不好？因为如果解释得很烂，根本没人在乎网站看起来有多漂亮。

<details>
<summary>Original English</summary>

**Neet**: Yeah, so initially when I made the free site I was still working at Google. So I just chose some like random Google tools. Uh I was using Google Cloud Firebase uh because it was so easy to use. I regret that one because now I meet so many people. I'm like oh maybe I should do Convex now. I should have done you know something different, but um I also did Angular at the time which is what I used at Google. So I was like it makes sense. Maybe I can just learn it at the same time. Regret that one as well. But thankfully we've gotten to a point now with LLMs. So like migrating things has become relatively trivial. So like maybe that's something I'll do. But in terms of like building the application itself for whatever reason like I I just didn't find that super interesting because there's usually not that many deep problems. I think the interesting things came from like innovating and like doing things in a way that like people care about. Like nobody's going to care that much about like the performance of my site or or the tech stack I use or like any of these like little things. They're going to care about like the UX, like how well did I explain something in a video? Cuz if the explanation sucks, nobody cares like how pretty the site looks.

</details>

**Interviewer**: 视频就是产品，或者说是产品的主要部分，对吧？

<details>
<summary>Original English</summary>

**Interviewer**: the video was is the product or or most of the product, right?

</details>

**Neet**: 是的，因为这是教育。如果教育内容本身很差，那就没有人会真的在乎。虽然我非常不擅长构建网站，但我认为我的想法、概念和价值足够好，以至于无论网站看起来多么糟糕，我做出的技术选择多么差劲，其商业价值都已经超越了其他一切。这才是更重要的。这也教会了我很多关于如何优先处理真正重要的事情的道理，然后你可以在那些不重要的事情上走捷径。我想我看到埃隆·马斯克有一个优化工作流程和流程的四步或五步法则，你知道的，你开始剔除一些东西，有时你剔除得太多了，你意识到自己犯了错误，然后你就可以慢慢地把那些东西再加回来。所以我采取了那种方法，因为我大部分时间都是一个人在工作。我大概本应该雇人来提高速度，但我没有。所以正因为如此，我走了很多捷径，而且我今天依然在走捷径，因为这其中有太多的价值。我有一个故事可以说说，虽然大家听了可能会生气，但至少目前对我来说是奏效的。所以我一直坚持那样做。

<details>
<summary>Original English</summary>

**Neet**: Yeah, because it's education. So it's like if the education is bad, then nobody really cares. And and I I was very bad at building, but I think the idea, the concept, the value was good enough that no matter how crappy the site looked and like how bad like tech choices I made, the the business value like exceeded everything else. Like that mattered more. And so that taught me a lot about like prioritizing things that actually matter and then you can take shortcuts on the things that don't matter. I think I saw Elon Musk has like this four-step or five-step process for optimizing like a workflow and like a process where, you know, you start you start cutting things out and sometimes you cut too much out and you realize you made a mistake and then you can like slowly introduce that back in. And so I took that kind of approach because I was mostly working by myself. I probably should have hired people to move faster, but I didn't. And so because of that, I took a lot of shortcuts and I still take shortcuts today because there's just so much value in it. Like I have a story I can tell that people probably get mad about, but it's worked so far for me. So I I stick with that.

</details>

### 用 AI 写代码与接受不完美

**Interviewer**: 是什么故事？

<details>
<summary>Original English</summary>

**Interviewer**: What what's the story?

</details>

**Neet**: 是这样的，我有一个服务，我每个月大概要付 3000 美元的费用。然后我想应该是在去年年底到今年年初那会儿，当那种 AI 辅助编程 (vibe coding) 变得非常疯狂的时候，我还很陌生。我就在想我或许可以自己写一个这个服务的替代版本。

<details>
<summary>Original English</summary>

**Neet**: So I have this service that I was paying like 3,000 a month for service and then I think late last year early this year when like the AI vibe coding stuff went really crazy, I was I was new. I could probably write my own version of this service.

</details>

**Interviewer**: 是个什么服务？

<details>
<summary>Original English</summary>

**Interviewer**: What service was it?

</details>

**Neet**: 是用于代码执行的服务。所以我当时想，我可能可以在一两个月内写出自己的版本，但是省下每月 3000 美元的机会成本，相比于我本来可以去做的其他更有影响力的事情而言，其实并不划算。但我又想，好吧，有了这种基于 AI 的编程方式，也许我能用更少的时间搞定，如果运气好的话，也许几周就行了。结果我实际上只用了两三天就完成了。但这确实需要编程技能，如果我不懂编程，我也是做不到的。但我确实用三天左右做完了。然后我就部署了这个服务。所以现在我自己管理它，每个月的成本只有大概 200 美元，而不是 3000 美元。但这个服务里有一个 Bug。我觉得是内存泄漏或者类似的问题。所以现在的情况是，我部署了这个服务，每隔几天就会有一两个实例崩溃，对吧？所以显然有个问题存在，有一个生产环境的问题。我可以花时间去深入研究并修复它。这就是那种，你沉浸在这种通过 AI 快速写代码的过程中，然后遇到了一个问题，这时候你就得说，好吧，现在你不得不真正深挖细节，去搞清楚问题到底出在哪里。所以我认为，要找出这个问题，实际上可能要花费我比三天多得多的时间。所以我就干脆没去管它，因为我想，好吧，如果一个实例挂了，我就同时运行好几个实例就行了，对吧？我就跑四个实例。所以如果挂了一个也没事，而且它崩溃得也没有那么频繁。

<details>
<summary>Original English</summary>

**Neet**: It was like for code execution. And so I thought like probably I could write my own version of this for like within like a month or two, but the 3,000 a month opportunity of that versus like other things I could be working on, there were other more impactful things that I could be doing. But I thought, okay, with vibe coding like maybe I could get this done in less time, maybe a couple weeks if I'm lucky. And so, I actually got it done in like two or three days. And it did take coding skills. Like if I didn't know how to code, I would not have been able to do it. But I got it done in like three days. And then so I deployed the service. And so now that I'm managing it, it costs me like 200 a month versus like 3,000. But there's a bug in the service. I think there's a memory leak or something. And so so what happens is I have this service deployed. Every couple days, like one or two instances will crash, right? So there's clearly an issue, there's a production issue. I could spend the time to go into that and fix it. This is like one of those things where it's like you get into to vibe coding coding uh and you run into an issue and it's like, okay, now you're going to have to actually dig into the details to really understand like where the issue is coming from. So I think it would actually take me much longer than three days probably to find the issue. So I haven't even bothered with that because I'm like, well, okay, if one instance goes down, like I'll just have several instances running at the same time, right? I'll have like four. So if one goes down, and it doesn't happen that frequently.

</details>

### Google Cloud Run 赞助商插播

**Interviewer**: Neet 刚才正好谈到了运营一个服务时，你不得不管理自己的基础设施，并在某个实例崩溃时处理启动新实例的问题。这正是谈论我们本期节目赞助商 Google Cloud Run 的绝佳时机。作为软件工程师，我们真的只想写代码，而不是去管理服务器，或者应付复杂的扩展和配置。Google Cloud Run 是一个完全托管的平台，旨在让你在谷歌世界级的基础设施上运行任何代码，且管理开销为零。无论你运行的是 Web 服务、批处理作业、智能体，还是微调后的大语言模型，部署都非常简单，只需输入 `gcloud run deploy` 或连接你的 GitHub 仓库即可。让 Google Cloud Run 脱颖而出的一个特点是它的自动伸缩和内置冗余。Cloud Run 可以瞬间进行扩容以应对巨大的流量激增，并在闲置时缩减到零，这一切都不需要任何人工

<details>
<summary>Original English</summary>

**Interviewer**: Neet was just talking about operating a service when you have to manage your own infra and taking care of spinning up new instances when one crashes. This is a perfect time to talk about this episode's sponsor, Google Cloud Run. As software engineers, we really just want to write code, not manage servers or wrestle complex scale and configurations. Google Cloud Run is a fully managed platform built to let you run any code on Google's world-class infrastructure with zero management overhead. Whether you're running web services, batch jobs, agents, or fine-tuned LLMs, deploying is as simple as typing gcloud run deploy or connecting your GitHub repository. One thing that makes Google Cloud Run stand out is auto scaling and built-in redundancy. Cloud Run scales up instantly to handle massive traffic spikes and scales down to zero when idle, all with no manual

</details>

<!-- chunk 6/13 -->

### 云服务权衡与商业决策

**Host**: ……干预。这意味着你完全不需要为安静的项目付费。就个人而言，我最喜欢的功能是 Cloud Run 如何开箱即用地为你处理区域冗余和自动故障转移。在你认为这可能是你不需要的东西而将其忽略之前，我最近刚刚报道了 Coinbase 因为没有为其全球交易服务设置区域冗余而宕机了 10 个小时。而他们很可能没有设置的原因是因为，即使在区域级别构建自动故障转移也是一项巨大的工作。我个人说不出还有多少其他基础设施服务能开箱即用地提供这种故障转移。所有这些功能让你能专注于你的代码，而由 Google 管理基础设施和运营。停止为基础设施担忧，开始部署吧。今天就在 cloud.run 尝试 Google Cloud Run。我还想提一下我们的主要赞助商 Antithesis。Neet 在一个系列中谈到了内存泄漏，他知道有这个问题，但就是没有时间去追查。如果你从事分布式系统工作，你肯定经历过。你知道那里有很深的 bug。你无法找到根本原因，所以你只能祈祷没有什么真正的灾难发生。有了 Antithesis，你不再需要依靠希望了。Antithesis 让你能轻松高效地修复和发现各种 bug，这样你就不再需要在交付质量和快速交付之间做出选择。让我解释一下它是如何工作的。Antithesis 在一个恶劣的模拟环境中运行你的整个系统。通过这样做，它能在你的用户发现之前找到每一个 bug。而且因为模拟是完全确定性的，Antithesis 不仅能找到 bug，它还能为你提供每一个问题的完美重现。我知道这听起来有点像科幻小说，但这在底层实际上是硬核工程。Jane Street、Flight Data IO 和 etcd 社区在发布 agent 编写的代码时充满信心，因为他们知道这些代码已经被 Antithesis 验证过了。想看更多案例研究和细节，请前往 antithesis.com/pragmatic。也就是 antithesis.com/pragmatic。接下来，让我们回到 Neet 的故事，听听为什么他很乐意留下一个生产环境的 bug 不去修复。

<details>
<summary>Original English</summary>

**Host**: intervention. This means you pay absolutely nothing for quiet projects. Personally, my favorite feature is how Cloud Run handles zonal redundancy and automated failover for you out of the box. And before you dismiss this as something you might not need, I just recently covered how Coinbase was down for 10 hours because they did not have zonal redundancy in place for their global trading service. And the reason they most likely did not have it is because it's a ton of work to build automatic failover even for a zone level. And I personally cannot name many other infra services where you get this kind of failover out of the box. All these capabilities let you focus on your code while Google manages the infrastructure and operations. Stop worrying about infrastructure and start deploying. Try Google Cloud Run today at cloud.run. I also want to mention our presenting sponsor Antithesis. Neet talked about memory leaks in a series that he knows about but just doesn't have the time to chase it down. If you work on distributed systems, you've been there. You know there are deep bugs there. You have no way to root cause them so you can only hope there's nothing really catastrophic. With Antithesis, you no longer have to rely on hope. Antithesis lets you fix and find all sorts of bugs easily and efficiently so you no longer have to choose between shipping quality and shipping fast. Let me explain how. Antithesis runs your whole system in a hostile simulation. By doing so, it finds every bug before your users do. And because the simulation is fully deterministic, Antithesis doesn't only find bugs, it gives you a perfect reproduction of every issue. I know this sounds closer to science fiction but it's actually hardcore engineering under the hood. Jane Street, Flight Data IO, and the etcd community ship agent written code with full confidence because they know it's been verified by Antithesis. To see more case studies and details, head to antithesis.com/pragmatic. That's antithesis.com/pragmatic. And with this, back to Neet and his story on why he's happy leaving a production bug unfixed.

</details>

**Neet**: 这是一个有趣的权衡，像我内心的工程师会讨厌那样，因为就像，那里有一个问题。那就修好它。但商业价值却没有区别。像我们几乎是零宕机。我的宕机时间比 LeetCode 还少，而且我只有几个人在做这件事。所以就像，我只是觉得这是一个权衡。人们可以争论是这样还是那样，但我认为现在对我来说不修复它才非常有意义。

<details>
<summary>Original English</summary>

**Neet**: It's an interesting trade-off where like the engineer in me hates that because it's like there's an issue. Like fix it. But the business value makes no difference. Like there has been practically zero outages. I have less outages than LeetCode and I'm like a couple people doing it. So it's like I just think it's like a trade-off. And people could argue one way or the other, but I think it just makes so much sense right now for me to not like fix it.

</details>

**Interviewer**: 但这太有趣了。所以，你花钱买了一个引擎或者获得了授权，如果我没理解错的话，它是在执行代码，对吧？所以，当人们在你的编辑器里输入东西时，它会运行，然后你可以检查它。它可以像运行其他解决方案一样运行你的问题。你在 AI 的辅助下使用它，你知道你想构建什么。你以你认为它应该工作的方式构建了这个引擎。你测试了它。它似乎在任何地方都能工作。所以，你部署了它，这花了你两三天时间。现在你有这个质量退化的问题，但这并没有对整个事情产生巨大的影响。但我想在这方面逼问你一下。你难道不认为这有点像我们看到的 AI 辅助编程或 AI 编程的典型情况吗？很多人会说，哦，我公司花钱买了这个 SaaS。我是一个创始人。我为此付钱。我可以替换它。然后你构建了一些不够好的东西，你算是勉强过得去。然后又一次，修复它在商业上没有意义，或者现在修复它太难了，因为这不全是你写的代码，当然它速度更快。

<details>
<summary>Original English</summary>

**Interviewer**: But this is so interesting. So, you paid for an engine or licensed it that if I understand it, it was executing code, right? So, when people like type out stuff in your editor, it runs it and you can check it. It can like run your problems as well as other solutions. You used with AI assistance, you knew what you wanted to build. You built this engine in a way that, you know, you think it should work. You tested it. It seems to work everywhere. So, you deployed it and it took you 2 or 3 days. And now you have this quality regression, but it doesn't make a huge difference to the thing. But I want to push you on this. Like do you not think this is a little bit typical of what we're seeing with AI-assisted coding or AI coding of like a lot of people are like again, like oh, there's this SaaS that my company is paying for. I'm a founder. I'm paying for it. I can replace it. And you build up something that is subpar and you kind of get by. And then again, it makes no business sense to fix it or it's now too difficult cuz you didn't write all of it, but of course it was faster.

</details>

**Neet**: 所以，我的想法是，如果我修复了这个问题，我可能可以分配一个更小的服务器池。所以，也许我还能多省个几百块钱。我确实想过，好吧，这真的有影响吗？我其实想过很多。我在想我是不是应该直接修复它，因为以后这会成为一个问题吗？我最初测试它的时候，我只向这个服务发送了很少量的流量，而且我仍然把大部分流量发送到原来的服务。所以，我只运行了几个星期，我想，我会这么写代码。我很确定会有问题。但我发现实际上完全没有问题。它就是运行着，好吧，偶尔服务器会宕机，其中一个服务的服务器会宕机，但几分钟内就会被替换。这就是我的想法。就是，这根本不重要。我的服务在技术上更快，因为我在更好的硬件上运行它。是的，我只是看到，根本没人在乎。像，没有用户向我提过关于这个的任何事情。现在更好了。

<details>
<summary>Original English</summary>

**Neet**: So, the way I think about it is like if I did fix the issue, I could probably allocate like a smaller pool of servers. So, maybe I could save like a couple hundred bucks more. And I do think about like okay, does this actually make a difference? Like I've actually thought about it a lot. I'm like should I just fix it because like is it going to be an issue later on? And I initially tested it. I was only sending like a small amount of traffic to this service and I still had most of it going to the original one. So, I just ran it for a couple weeks and I was like I would have coded this. Like I'm pretty sure there's going to be issues. And I saw like literally no issues. Like it's just up like okay, once in a while the servers will go one of the services servers will go down, but then it just replaced in like a couple minutes. That's just how I think about it. It's like it just doesn't matter. Like my service is technically faster because I run it on like better hardware. Yeah, I just see that like nobody cares. Like, no user has mentioned anything about that to me. It's better now.

</details>

**Interviewer**: 所以，是的。所以，我想也许换个更好的角度来看，就是它整体上更好了，因为它更便宜，它更快，是的，当然，这里有权衡。比如，在工程领域，现在有一个会导致其中一台服务器崩溃的退化问题。所以，你就额外运行一台。如果你愿意，就把它当成你有了副本。但整体上它仍然更便宜。所以，当你把它打包来看，它比以前更好了。看吧。这可以说是一个显而易见的商业决策。我想在工程学中，有一个问题是，当一个问题已经解决并且足够好时，你需要做到多么完美主义。

<details>
<summary>Original English</summary>

**Interviewer**: So, yeah. So, I guess maybe to look at a bit better is it's overall like better because it's cheaper, it's faster, and yeah, there is of course, there's trade-offs. Like, within engineering, there is now a regression that crashes one of the servers. So, you run an additional one. You have like replication if you will. And it's still cheaper overall. So, like overall as you package it, it's better than before. Boom. Like, it is kind of a obvious business decision. And like I guess in engineering, like you there's a question like how perfectionist you need to go when a problem is already solved and is good enough.

</details>

**Neet**: 是的，没错。我在一开始就提到过，不能深入研究这一点让我很烦。所以，即使是对于这件事，它确实让我很烦。但是，我想我已经习惯了，在某种意义上就是优先考虑商业，只去考虑实际的价值，人们关心什么，到底什么会产生影响，不只是在短期内，也在长期内。

<details>
<summary>Original English</summary>

**Neet**: Yeah, that's right. I mentioned at the beginning that it like bothers me that you can't go super deep. And so, even for this, it actually does bother me. But, I guess I've gotten used to it in the sense of like prioritizing the business and just thinking about like the actual value, what do people care about, what's actually going to make a difference, like not just in the short-term, but also in the long-term.

</details>

### 面试准备的实际价值

**Interviewer**: 我们来谈谈这个，关于你如何——尤其是作为一个创始人，但即使作为一个软件工程师——像在某个时刻你需要开始考虑商业。但是，人们为了进入大型科技公司而使用 NeetCode 准备面试，你知道，他们首先需要跳过编程面试这个圈套。你认为准备这些数据结构和算法的编程面试，能给人们带来什么在工作上实际有用的东西？我说的不是算法，而是你通过准备获得的实际的其他东西。

<details>
<summary>Original English</summary>

**Interviewer**: Let's talk about this, the how like as especially as a founder, but even as a software engineer, like at some point you need to start to think about the business. But, the interviews that people are taking with NEET code in order to get into big tech, you know, they you first you need to jump the hoop of coding interviews. What do you think preparing for these data structures and algorithms coding interviews gives to people that is actually useful on the job? And I'm not talking about the algorithms, but the actual the other things that you gain by preparation.

</details>

**Neet**: 是的，我想是的。至少从我的角度来看，我完成了这四年的学位。我没有在学习中作弊。所以我确保我理解了所有的基础知识和类似的东西。然后我进了亚马逊，然后我离开了。然后，在进 Google 之前的那一年里，我真的只是在做 NeetCode。我当时在做讲解视频，这在某种程度上教会了我演讲和沟通，以及深入思考一个问题，也许还会思考算法和数据结构之间的权衡等等。但我并没有做太多的开发工作。所以，当我进入 Google 后，我仍然能够获得晋升，即使我认为就常规的纯编码和编码经验而言，与大多数人相比，我可能低于平均水平。但我仍然能够做到，对于一个我不知道如何解决的难题，比如使用我以前从未使用过的内部工具，我拥有这样的技能，好吧，我可以坐下来，我可以过一遍这些资料，我可以大体制定一个计划，看看我将如何尝试。我在沟通方面下了很大功夫，这样我就可以去找我的经理说，“好吧，我的想法是这样的。” 就像你在面试里做的那样，对吧？比如，“好吧，我考虑的方法是这样的。比如，我会先去做，只是为了让你和我在同一频道上。比如，也许你有时间去了解一下并给我反馈，或者也许你没有。但是，为了让你和我在同一频道上，这（计划）就是我将要做的。” 所以，有趣的是，我确实认为我在数据结构和算法上学到了很多，就在思考方式而言。另外，在……

<details>
<summary>Original English</summary>

**Neet**: Yeah, I think so. From my perspective at least, I like went through this four-year degree. I didn't cheat through it. So, I made sure I understood like all the fundamentals and things like that. And then I got in Amazon, and then I left. And then so, for that like year before I got into Google, I was really just doing NEET code. I was making the explanation videos, and that kind of taught me about like speaking and communicating, and like thinking deeply about like a problem and maybe like the trade-offs between like algorithms and data structures and stuff like that. But, I didn't really do much development. And then so, when I did get into Google, I was still able to get promoted even though I think like in terms of just regular like raw coding and coding experience, I was probably sub par compared to most people. But, I was still able to like for a hard problem that I had no idea how to solve like using internal tools I've never used before, I had the skill of okay, I can sit down, I can go through this stuff, I can kind of make a plan of how I'm going to try things. And I worked a lot on my communication so that I could go to my manager and say, "Okay, so this is what I'm thinking." Kind of like you do in an interview, right? Like, "Okay, this is the approach I'm thinking. Like, I'm going to go ahead and do it just so you're on the same page. Like, maybe you have time to like look into it and give me feedback or maybe you don't. But, just so you're on the same page, like this is what I'm going to be doing." So, funny enough, like I do think I've gained a lot from algorithms and data structures in terms of like just thinking. Also on the...

</details>

<!-- chunk 7/13 -->

### 沟通与权衡：工程的本质

**Speaker A**：沟通方面也是如此。还有权衡方面，我认为这才是工程的真正意义所在。这就又回到了人们在AI辅助编程等方面的体验。一切都是权衡。在工程领域，并没有像数学或科学里那样绝对正确的答案。工程在于找到当下的最佳解决方案。就像我们在谈论我的服务中出现的内存泄漏问题，对吧？这就是一种权衡。并没有绝对正确的答案，尤其是在商业中，没有绝对正确的答案。所以，我认为这就是现在很多人可能忽略的地方，他们可能过于关注硬技能，比如“好吧，我能写这个循环吗？我了解这个特定的数据结构吗？我了解所有这些细枝末节吗？”我觉得他们忘记了要退一步，从宏观上审视工程到底是怎么一回事。因为在现实世界中你会看到，一个非常优秀的工程师或者一个非常聪明的人，从一个领域跨界到另一个领域，你看到这种现象，就会想：他们到底拥有什么别人没有的东西？通常并不是某种非常具体的技能，比如他们把某种编程语言掌握得超级好。通常是与之相关的东西，可能与数据结构和算法有关，或者是某种硬技能。这其实是你从总体上能从中获得的东西。我认为这就是教育的普遍意义，就像你花了20年的人生学习各种各样的学科，这在某种程度上塑造了你，虽然这种塑造很难用语言准确表达。很难精确地说，你通过学习数学、物理、演讲、写作和历史到底获得了什么，但很显然，其中蕴含着巨大的价值。

<details>
<summary>Original English</summary>

**Speaker A**: communication side. And also on the trade-off side, which I think is really what engineering is about. And it goes back to like what like people are experiencing with like agent to coding and stuff. Everything is a trade-off. It's not really In engineering, there's no correct answer like there is in math or science. Engineering is about the best solution at the time. Like like we're talking about like the the the memory leak issue with my service, right? It's a trade-off. Like, there's no correct answer, especially in business. There's no correct answer. And so, I think that's what a lot of people are maybe like missing nowadays where they're focusing maybe too much on the hard skills of like, "Okay, like can I write this loop? Do I know this particular data structure? Do I know like all these like little things?" When I think they're they're forgetting to like zoom out and look at the bigger picture of like what engineering is even about in general. Because what you see in the real world is you'll see a really good engineer going from like one domain to another or really smart person like going from one to another and you you you see that and you think like what do they have that other people don't? It's usually not some like very specific skill that like they know this programming language super well. It's usually something related to that like it could be whether it's a data structures and algorithms or like some hard skill. It it's like what you gain from that in general and I think that's like education in in general as well where like you go through like 20 years of your life learning about all sorts of subjects and that like molds you in a way that's very hard to articulate. It's very hard to be precise about like what exactly did you gain by like learning math and physics and speaking and writing and history but clearly there's a lot there.

</details>

**Speaker B**：听起来你的意思是，学习付出的努力，经历那些当下可能看起来毫无意义的艰难事情，或者解决那些可能是抽象的、并不针对某个具体事物的问题，这些努力随着时间的推移会慢慢积累起来产生作用？

<details>
<summary>Original English</summary>

**Speaker B**: Sounds like you're saying that the effort of learning, the effort of going through doing hard things that might be pointless at the time or like solving problems that are maybe abstract or not for a specific thing, they add up over time?

</details>

**Speaker A**：我非常同意这一点。这其实让我想起了我之前和Chip (Heath) 的一次谈话。我想你们的播客也曾邀请过她。当时因为现在没人知道AI到底会怎么发展，所以我们在讨论这个话题。她提到，在她看来，很难知道哪些硬技能将会变得重要，对吧？比如，你今天应该学习哪种编程语言？你应该学到多高深的程度？你甚至还需要知道怎么写代码吗，对吧？但正如她所说，虽然这些都是无法回答的问题，但她确切明白的一点是：系统性思维，这种适用于工程和计算机科学，同时也适用于许多其他学科的宽泛概念，是非常重要的。为了便于理解，我用建筑行业来举个例子，对吧？比如你四处走动，看到所有这些正在建造的建筑，你看到了工人们。每当我看到这些，我就会看到一个庞大复杂的工程，所有这些人都在做各种各样细小的工作。然后到最后，你就拥有了这座如此复杂的宏伟建筑。可能没有任何一个人能单凭自己完成这件事，但这又要回到你所看到的，有工人们在做具体的工作。但同时你拥有这整个系统，而且有人建立了那个系统。有人制定了那些规则：好，某个工人要做这个，这里需要有这样的程序，我们要检查这些东西以确保没有问题，我们要验证各项事务。我们要有这样一个庞大的流程，一个建造建筑的系统，来确保在整个过程中不会出差错。我认为这就是一种没有针对性课程可以学习的技能，对吧？因为那确实是一件很难的事情。大多数人并不是在构建系统。他们就像是工蜂。他们不是那个架构这整个系统的人。但我认为这种技能之所以如此重要，是因为所有的价值都是从这里产生的。你拥有这些工蜂，但如果没有系统，就什么也做不成。所以，我认为这种思维方式是不会消失的。它也是无法简单学到的，但我认为要达到那种水平，需要积累很多东西。

<details>
<summary>Original English</summary>

**Speaker A**: I think so a lot and this actually reminds me of a conversation I was having with Chip uh Heath. I think you've also had her on the podcast and uh she was cuz every nobody knows what like what's happening with AI. So we were talking about it and she mentioned that in her opinion it's very hard to know like what hard skills are going to be important, right? Like which programming language should you learn today? Like how high level should you go? Do you even need to know how to code, right? But as she mentioned that okay, like those are like impossible questions to answer but the one thing that she did understand is that systems thinking, this like broad concept that applies to engineering and computer science but also to many other disciplines as well. And the way I kind of understand it to use an example is like maybe in a construction, right? Like you walk around, you see like all these buildings being built, you see the workers and whenever I look at that I see like this big complex thing and all these like people doing all these like little things and then at the end of it, you have like this big building built that's like so complex. No one person could probably do that themselves, but it goes back to you have like the workers working on like the individual thing. But then you have this entire system, and somebody set up that system. Somebody set up those rules that, okay, a worker is going to do this. There's going to be this procedure. This is what we're going to check to make sure that there's no issues. We're going to verify things. We're going to have like this big process, this system of like making buildings, making sure that you don't have issues with that. And I think that is a skill that there's no like course for that, right? Like there's no Like that's a hard thing. Like most people aren't building the system. They're They're like the worker bees. They're not like the ones architecting this whole system. But I think that's the skill that is so important because that's where like all the value comes from. You can You have these worker bees, but without the system, like nothing's going to get done. And And so, I think that type of thing is not going away. And it it it's impossible to learn, but I think it takes like a lot of things to get there.

</details>

### 系统性思维与领域专长

**Speaker B**：但在这个观点上，我想稍微反驳你一下。这真的只是系统性思维，还是说其实是成为一个领域的专家？因为系统不会在真空中存在，你明白吗？比如，农业系统是非常特定于农业产业的运作方式的。如果在法律行业，它是基于你所在的任何国家的法律体系的。如果你在一家医疗保健领域的法律科技初创公司，那么这家公司在美国、在英国或者在罗马尼亚等地，情况看起来会非常不同。那些在一个领域成为优秀系统思考者的人，通常只是因为他们真正深刻地理解了那个领域。你知道，支付行业就是我曾经工作过的一个例子，它是一个非常有趣且复杂的领域。一旦你深入进去，人们就会开始在里面转圈子，因为你已经身在其中了。所以，我在想这其中是否有一种抽象层面的系统思维，但也同时需要成为一个领域专家。这两者在某种程度上也是重叠的，因为如果你是一个领域专家，你就必须理解那个领域的系统。也许如果你能理解多个领域，你在抽象层面的系统思考能力也会变得更好。

<details>
<summary>Original English</summary>

**Speaker B**: But I I'm going to push you a bit on that. Like is is is it Is it really systems thinking, or is it being learning a domain? Because systems don't exist in a vacuum, you know? You will have agricultural systems that are very specific to how the agriculture industry works. You You will You will have If you're in a legal industry, like it is based on whatever country you're operating in. If If you're in a legal tech startup and healthcare, a healthcare tech startup looks very different in the US versus like the UK versus in Romania, etc. The people who are who are great system thinkers in one domain often are are they just really understand the domain. And you know, payments is one example where I worked in, which is very interesting complex Once Once you get into it, like people start to move around in it because you go there. So, I wonder if it's There's There's There's abstract level system thinking, but there is also becoming a domain expert. And somehow they kind of overlap as well cuz if you are a domain expert, you must understand the system of that domain. And maybe if you understand multiple domains, you can get better at abstract level system thinking as well.

</details>

**Speaker A**：是的，没错，我完全同意这个观点。我觉得对我来说，这绝对很难量化和清晰地表述出来，因为它往往是很模糊的。但我认为你绝对说对了一点，那就是那些技能，那些硬技能，比如关于某些行业细节的知识等等，这些肯定是很重要的。但我不知道，我想当思考这个问题的时候，我也会想到可能你也认识这样的人。有些工程师，他们可以从一个领域跨界到另一个完全不同的领域，而你就是非常信任他们。仅仅通过和他们一起工作，你就知道他们很聪明。他们的思维方式使得他们能够从支付领域跨界到诸如房地产之类的完全陌生的行业。当然，他们肯定会经历一个学习曲线。但是有些人，不知什么原因，他们就是学得更快，领悟得更快，表现得更好。我不认为这是某种天生的东西，或者是上帝赋予的，注定某些人就是比其他人聪明。我认为这里面有很多因素在起作用。我可能无法很好地把它阐述清楚，但我认为很多人可能会说，比如，哦，学习这门课是浪费时间，因为我在工作中根本用不到那些细节。我认为这种想法是错误的。而且我认为现在很多人在面对AI时也是这种心态。比如，嘿，如果几年后我都不需要写for循环了，那我还学它干嘛。嗯，我不认为学习这些东西是在浪费时间。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, no, I completely agree with that. And I think for me it's definitely hard to like quantify and articulate because it's very kind of like vague and I think you're definitely right though that like the the skills, the the hard skills, like the knowledge and like the details of like certain industries and things like that that definitely matters. But I don't know. I guess like when I think about it, I think of it maybe you know people like this as well. Like there's certain engineers that are like they could go from one domain to another and you just trust them. Like you just know from working with them they're smart. Like they think in a certain way where like they could go from payments to like some completely other industry, real estate or something. And there there will be like that learning curve for them. But some people for whatever reason they just learn faster, they just get it faster, they just perform better. And I don't think that this is something that was innate, that this was just handed down by like God that some people are just smarter than others. I think there's a lot that goes into it. I I can't probably articulate it super well, but I think a lot of the things that people might say that like oh, it was a waste of time to learn this subject cuz I didn't actually use like those details on the job. I think that's wrong way to think about it. And I think that's what a lot of people are doing now with AI. Like hey, what what if I'm not going to be writing for loops a couple years from now. Um I don't think those things are a waste of time.

</details>

**Speaker B**：听起来……听起来你的意思是，你不认为深入钻研并透彻理解事物是在浪费时间。

<details>
<summary>Original English</summary>

**Speaker B**: It sounds like it sounds like you're saying that it's you don't think it's a waste of time to go deep and understand things.

</details>

**Speaker A**：是的，绝对不浪费。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, absolutely.

</details>

**Speaker B**：尤其是当做这件事很难的时候。

<details>
<summary>Original English</summary>

**Speaker B**: Especially when it's hard to do so.

</details>

**Speaker A**：绝对是，没错。

<details>
<summary>Original English</summary>

**Speaker A**: Absolutely, yeah.

</details>

### 科技大厂的招聘门槛

**Speaker B**：我们来谈谈FAANG（Meta, Apple, Amazon, Netflix, Google）以及其他科技大厂的招聘门槛吧。有很多人在使用NeetCode来为这些面试做准备。你从他们那里获得了反馈，你知道，当他们成功时会写信给你，或者在经历了几个月的失败后，他们会沮丧地写信给你。所以你能从这里获取很多信号。就纯粹的算法部分，也就是编程面试而言，你观察到了什么趋势？情况是保持不变，变得更难了，还是变容易了？

<details>
<summary>Original English</summary>

**Speaker B**: Let's talk about the hiring bar at at Fang and companies the the the big tech companies. A lot of people are using NEET code to prepare for these interviews. You're getting feedback from them of you know, like they will they will write to you when they succeed or they will write in frustration after many months they haven't. So you get a bunch of signal here. What are you seeing in terms of the just the algorithmical part, you know, the coding interview? Like are things staying the same, getting harder, getting easier?

</details>

**Speaker A**：就面试形式而言，尤其是在像初级职位这种早期阶段，面试形式本身仍然主要包含大量的算法和数据结构。根据一些坊间传闻，我确实看到人们在说面试变得更难了。但与此同时，从那些确实通过了面试的人来看，他们仍然在，就像在……

<details>
<summary>Original English</summary>

**Speaker A**: In terms of the format, like especially like at the early levels like juniors and stuff, it's still a lot of like algorithms and data structures, the format itself. I've definitely seen, I think, anecdotally, like people are mentioning that it's getting harder. At the same time, from the people who do pass the interviews, they still, like at

</details>

<!-- chunk 8/13 -->

### 大厂面试难度的变化与防作弊机制

**NeetCode**：至少在像 Google 这样的大型科技公司，我得说面试的难度和以前相比并没有太大的差别，至少在美国是这样。我认为这因国家而异。比如，你会看到像印度等一些国家的情况就非常不同。那里几乎全都是算法题。都是些 LeetCode 难题和超级难题之类的。但是在美国，我觉得还没有那么夸张，嗯，确实没那么夸张。

<details>
<summary>Original English</summary>

**NeetCode**: At least at big tech companies like Google and stuff, I'd say the difficulty is not that different from what it was before, at least in the US. I think it varies by countries. Like, you'll see like some countries, like India, it's very different. Everything's pretty much algorithms there. It's like LeetCode hards and super hards and stuff like that. But, in the US, I don't think it's that crazy, but it's uh yeah, it's not too crazy.

</details>

**Speaker A**：是啊，但我猜，要在没有任何辅助的情况下在白板上写代码，为这样的面试做准备真的很难。这从来都不是件容易的事。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, but I guess like, you know, going without any support like in a whiteboard, it's so hard to prepare for that. It's never been easy.

</details>

**NeetCode**：是的，绝对如此。而且我认为经常发生的一件事是，现在有了很多用于面试的作弊工具。因此，在过去大概五六年里，我们主要是进行远程面试，而现在这种情况正在发生一些改变。我觉得 Google 此时基本上已经恢复了现场面试，回归到传统的白板模式。当然，如果你愿意，他们也会允许你在笔记本电脑上写代码，但这将会是面对面的。会有人看着你写代码，这样你大概就不可能蒙混过关了。

<details>
<summary>Original English</summary>

**NeetCode**: Yeah, absolutely. And I think the one thing that's happened a lot is people like there's been cheating tools for interviews. And so, we've had like yeah, mostly remote interviews for the last like 5-6 years, and that's been changing a bit. I think Google has pretty much gone to on-sites at this point, back to the traditional whiteboard format. And they'll let you code on a laptop if you want to, as well, but it's going to be in person. Somebody's going to be watching you code, and you're probably not going to be able to cheat your way through that.

</details>

### 中小企业的新型面试模式与开源招聘

**Speaker A**：你观察到了哪些正在被尝试的面试形式？特别是当我们谈论其他公司，尤其是较小规模的公司在做哪些实验时。你看到或认为有哪些面试形式实际上是相当有潜力的？比如，如果你正在运营一家中小型公司，你可能会实际考虑采用什么形式，而不是——我知道你在这里有点像是在反对自己过去的业务。但是，如果你不得不抛弃数据结构与算法（DSA）面试，那么特别是随着 AI 作为工具的普及，什么方式是更有前景的？

<details>
<summary>Original English</summary>

**Speaker A**: What are interview formats that you're seeing, you know, where we're talking about other companies, especially smaller ones, experimenting? What are interview formats you're seeing or you think they're actually kind of promising? Like, if you were running a small smaller mid-size company, you might actually consider instead of the... And I know you're talking about against yourself here. Like, against... but if you had to throw away the DSA interviews, what is giving promise, especially with AI as tools?

</details>

**NeetCode**：任何标准化且极易规模化的流程，总是会有被钻空子的方法。而绕开这个问题的最佳方法就是招个实习生，通过观察他们的实际表现来评估。过去一周里我跟许多公司交流过，我发现很多能做到这一点的初创小公司都在实行类似试用期的制度。这可能是几天，也可能是一个月，甚至可能是几个月的时间，感觉就像是实习一样。但我也和其他公司聊过，他们说这对他们来说很难操作，因为如果你试图招聘一个已经有工作的人，这就变得不可行了。你很难真的那么做。不过信不信由你，我现在确实更倾向于这种方向，也就是我可以非常快速地判断出一个人的代码能力。比如我不会花上四轮面试去问候选人数据结构和算法相关的东西。我只会让他们做一些与未来实际工作类似的任务，或者甚至仅仅是和他们交流一下。看看他们是如何思考的。比如，他们能权衡利弊吗？我甚至不在乎他们对某个问题给出的具体答案是什么。我关心的是他们为什么会那么说？他们能说出些什么？他们是在复述在 ChatGPT 提示词里看到的东西，还是真的能把逻辑讲清楚？然后，当你审视他们正在做的工作时，也是同样的情况。我会问他们相关的问题。比如你为什么要用这种方式实现？这个方案有什么优点？有什么缺点？还有哪些可以改进的地方？我认为这种面试形式对于大公司来说很难规模化。这就是为什么我认为在大型科技公司不会发生这种转变。但这对我有效。它对较小的公司也有效。可一旦公司达到了一定规模，这就变得很难执行了。

<details>
<summary>Original English</summary>

**NeetCode**: Any process that you have that's going to be standardized and super scalable, there's always going to be ways to game that. And the best way to get around that would be like hire somebody who's an intern and you saw how they performed. And what I've spoken to a lot of companies about the last week is that there a lot of small companies that can get away with it are doing like trial periods. It could be a few days. It could be like a month. It could be even a couple of months, kind of like an internship. And I've spoken to other companies that say that that's difficult for them because if you're trying to hire somebody who already has a job, that's not going to be feasible. You can't really do that. But I've, believe it or not, have leaned in that direction where I can get a sense of somebody's code abilities pretty quickly. Like I'm not going to spend four interviews going through and asking somebody data structures and algorithm stuff. I just have them do work that might be similar to something I'd give them on the job or even just have a conversation with them. See how they think. Like can they think through tradeoffs? I don't even care about what answer they give me to a problem. I care about like what's like why did they say that? Like what can they say? Is it just something that they like saw in like a ChatGPT prompt and are just regurgitating it or can they actually like talk through it? And then when you look at like the work that they're doing, same thing. Like I ask them about it. Like why did you do it this way? Like what's good about this? Like what's bad about this? What could be improved? And I think it's a hard format to like scale for big companies. That's why I don't think that that's what's going to happen in terms of like big tech. But it's worked for me. It works for smaller companies. But once you get to a certain size, it's harder to do.

</details>

**Speaker A**：对，因为实际上是人在完成工作，所以他们使用什么工具并不重要。事实上，如果现在每个人都在使用 AI 代理之类的工具，那么他们同样也在使用，你实际上能获得他们在与其他人的对比中表现如何的信号。有趣的是，有一类公司其实并不缺乏招聘资源，那就是从事开源项目的公司。他们通常会直接招募那些已经在向他们的代码库贡献代码并开发了各种功能的人。所以，你知道，面试交流可能更侧重于软技能，因为我们会觉得，是的，我们已经看到了你的成果。你一直在无私地为我们的产品推送功能。这太棒了。我想这大概就是开源的优势之一。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, cuz you're basically people are doing the work and it doesn't matter what tools they use. In fact, if now everyone's using, you know, like AI agents, then yeah, they're using it as well and you actually get the signal of how they're doing compared to others. Interesting because one type of company that doesn't really have trouble hiring is the ones who are working in open source. And they will often end up hiring the people who are contributing to their repos and adding all the features already. And you know, the conversation will probably be more of a soft skills conversation cuz like yeah, we're seeing your work. Like you've been selflessly pushing features to our product. Awesome. And I guess that's kind of the upside of open source.

</details>

**NeetCode**：我觉得 Dax 提到过这一点，因为我跟许多和他共事的人聊过，他们就是这样获得机会的。他们要么是已经在贡献开源代码，要么就是 Dax 了解他们在自己的开源项目中所做的工作，然后他们就直接收到了 Dax 的私信，大概就是说：“嘿，你有兴趣来工作吗？” 所以他们其实已经有了可以展示的作品。如果你的工作是公开进行的，人们就能相当清楚地了解你的工作方式。

<details>
<summary>Original English</summary>

**NeetCode**: I think Dax mentioned this because I was speaking to a bunch of people that work with him that they just got that they were either contributing to open code already or Dax knew of them from open source work that they had done on projects of their own and they just got a DM from him and he's like, "Hey, would you be interested in working?" And so they already had this work that they could showcase and it's like if you're doing things in public, people can get a pretty good understanding of like how you work.

</details>

### AI 辅助编程与技术选型的权衡

**Speaker A**：说到你们在 NeetCode 业务中的工作方式，你和你的团队是如何协作的？你们使用什么工具？现在的代码中有多少是你们自己手动编写的？如果还有的话。

<details>
<summary>Original English</summary>

**Speaker A**: Speaking of how you work at NeetCode with your business, you and your team, how do you work? What tools do you use and how much code do you actually manually write these days if any?

</details>

**NeetCode**：是的，我得说在过去的六个月里，我们其实高速产出了许多功能和大量代码。目前大部分代码都是由 AI 编写的。而在此之前，情况并非如此。很长一段时间里，我其实是个非常排斥 AI 的人，甚至到现在人们有时还这么认为。有时候如果我表现出支持 AI 的态度，他们就会说：“NeetCode，你变了。发生什么事了？现在你成了一个为 AI 站台的托了。”但这真的不是。我只是试着务实地看待这个问题。因为我觉得，在以前我也一样会用这些工具，但它们那时候就是没那么好用。而现在，它们已经进化到了一个可以胜任我正在做的这种大部分属于增删改查（CRUD）工作的程度。除了代码执行服务之外，通常并没有那么多极其复杂的逻辑。那个代码执行服务可能是最有趣的一部分。但我使用的甚至是非常过时的技术。前端我用的是 Angular，这是一个没人喜欢的 Google 工具。后端我用的是 Firebase，还不算太糟，能完成任务，但现在看来已经有点老旧了。我还在使用 Google Cloud 和 TypeScript。但我可以说，最开始的头几年，当我负责写绝大部分代码的时候，代码质量其实非常非常差。我使用了 TypeScript，但我用的根本不是真正的 TypeScript。我的代码里充斥着大量的 `any` 类型。是的。我写了许多糟糕的代码。我直接写内联的 CSS。为了能尽快把东西做出来，我做了各种愚蠢的事情，因为我清楚整个代码库。我知道我能搞定某些特定的技术，所以为了加快开发速度，对我来说这是一种权衡。但现在有了 AI 之后，实际上，我回过头去看，我意识到当初的权衡是非常值得的。因为我用 AI 把那些糟糕的代码都清理干净了。这正是 AI 擅长的领域。它可以清理大量的冗余杂乱代码，它可以重构许多东西。如果我现在真的想做的话，我很可能可以通过 AI 极其快速地迁移到其他的技术栈上。所以回到权衡的话题上，我认为这只是一个思路问题。你可能会做出错误的决定，但即使你做了错误的决定，你也可以回头去尝试修正它，只要你花点心思去考虑它。

<details>
<summary>Original English</summary>

**NeetCode**: Yeah, so I would say over the last 6 months actually we've been cranking a lot of features out a lot of code out. Most of it has been written by AI at this point. And before that really wasn't the case. I was actually a really big AI hater for a long time and people still sometimes think I am and sometimes if I'm like pro AI they're like, "NeetCode, you changed. Like what happened? Like now you're an AI shill." But it's not. Like I just try to be pragmatic about it because I think before I was still using the tools but they just weren't as good. And now they've gotten to a point where the work that I'm doing which is mostly CRUD, usually there's not that much crazy interesting stuff other than like the code execution service. That's probably the most interesting one. But I'm using like pretty outdated tech even. I'm using Angular on the front end, a Google tool that nobody likes. And I'm using Firebase which isn't horrible. It gets the job done but it's a little bit outdated at this point. I'm using Google Cloud and TypeScript. But I would say initially actually like the first few years when I was writing most of the code very very bad code quality. I used TypeScript but I was not using like real TypeScript. I had a lot of any. Yeah. I had a lot of bad code. I was putting inline CSS. I was just doing all sorts of stupid stuff just to get stuff done as quickly as possible because I knew the entire code base. I knew like this certain tech that I can just deal with and so that was a trade-off for me just to move quicker. But with AI now actually, I've gone back and I realized that that trade-off was so worth it because I cleaned all of that up with AI because that's what it's for. Like it can clean up a lot of sloppy code, it can refactor a lot of things and if I really wanted to now, I could probably migrate to other tools very quickly with AI. So just to go back to the trade-offs, I think it's just about thinking like you might make the wrong decision, but even if you make the wrong decision, you can go back and then try to correct it just kind of by thinking about it.

</details>

### 容易构建功能并不等于容易创造价值

**Speaker A**：他也在社交媒体上发了她的一堆犀利观点。我不知道这是不是那种凌晨两点发的状态。但其中有一条，正如我引用你的原话说的：“现在的2026年，构建东西比以往任何时候都容易，但我也得说，这让真正创造价值变得困难了十倍。”

<details>
<summary>Original English</summary>

**Speaker A**: He sends a post a bunch of her hot takes on social media as well. I don't know if it's like a 2:00 a.m. thing or... But well one of them you said is as I'm quoting you, and now in 2026, it's never been easier to build things, but I would say that it just makes 10 times harder to actually build value.

</details>

**NeetCode**：是的，我认为是因为现在实现许多功能变得如此容易，而在过去人们并没有去实现那些东西，因为它们不值得花时间去做。以我自己的情况为例，刚才我谈到了代码质量的例子。我认为那件事是值得去做的，因为它很重要，它能帮助你开发得更快，让代码更易于维护。但是在功能方面，比如一个网站，你现在可以随意在里面堆砌一堆根本没人在乎的功能，并且你可以做得极快。就像每天都能上线一个新功能一样，但是人们真的在乎那个功能吗？那真的能让产品变得更好吗？这也可能会让事情变得更糟。

<details>
<summary>Original English</summary>

**NeetCode**: Yeah, I think because it's so easy now to implement a lot of things and people weren't implementing those things before because they just weren't worth doing. Like in my case, I went to the code quality example. I think that was worth doing because it matters, it can help you go faster, it's more maintainable. But in terms of like features, like a website like you can just throw features in there nowadays that nobody really cares about and you can do it so quickly. Like a new feature every single day, but do people actually care about that? Is that making it better? It could be making things...

</details>

<!-- chunk 9/13 -->

### AI时代的速度与质量平衡

**Speaker A**: 更糟。这可能会让事情变得更混乱。你会有一些杂乱无章的东西，由于你添加了这些甚至根本没人用的功能，现在你可能让网站的运行速度变得非常慢。所以我认为在商业中速度很重要，但我认为决策也同样重要。如果你走得太快，你就无法衡量你所做改变带来的影响，你没有时间去那么做，因为你只专注于发布产品。然后事情就会倒退，情况会变得更糟，最近我们在Anthropic就看到了这种情况。在过去的一个月甚至更长的时间里，情况出现了倒退，我想就在几天前，他们终于发布了一篇博客文章承认了这一点。但对他们来说，他们之前走得太快了，以至于都没有注意到。比如我看到Boris说，他在回复很多评论时在问：“我们还没怎么注意到这个，怎么其他人都能注意到？”而现在他们注意到了，我觉得这又回到了权衡取舍的问题上——或许现在他们意识到了：“好吧，也许我们应该放慢一点脚步，把更多精力集中在质量这类事情上，”或者也许也没有，但是……

<details>
<summary>Original English</summary>

**Speaker A**: worse. It could be making things more confusing. You have like things that are cluttered, you're maybe making the site perform really slowly now with all these features you're adding that nobody's even using. And so I think speed matters in business, but I think decisions matter as well. If you're going so fast, you're not measuring the impact of the changes that you're making, you don't have time to do that cuz you're just focused on shipping. And then things regress and things get worse and we've seen that at Anthropic recently, the last like month or maybe more than that where things have regressed and I think just a couple days ago they put out like a blog post acknowledging that finally but it for them they were just moving so fast that they did not notice like I saw Boris saying like he was replying to a lot of comments asking like we haven't really noticed this like why is everybody else noticing it and and now they have and I think it's again just goes back to trade-offs like now that maybe they've realized like okay maybe they should slow down a little bit focus more on quality and stuff like that or maybe not but

</details>

**Speaker B**: 我想这确实让人稍微松了一口气，因为你知道，在人工智能时代之前，很明显的情况是：如果你追求速度，通常就常常会把事情搞砸。你知道，Facebook甚至还有过这句著名的格言。你要么更谨慎行事，少犯些错，但它们几乎处在这个滑动标尺上——你移动得有多快，或者你有多鲁莽，对比事情的稳定性。这一直以来都还挺有道理的。而现在有了AI，我们曾一度认为：“嗯，也许这不成立了，也许你可以兼顾速度与质量。”但我们在Anthropic身上看到，他们走得很快，同时也把事情搞砸了。我的意思是，他们的业务在增长，别误会我的意思，但……但不管怎样，我猜这个真理并没有因为人工智能的出现而改变。

<details>
<summary>Original English</summary>

**Speaker B**: I guess it does give a little bit of relief that you know like we knew like pre AI it was pretty clear that if you move fast you typically you often break things you know Facebook even had this famous motto and so or you can be more deliberate and break fewer things but they're just almost at this slider like how fast you move or how reckless you are versus how stable things are and it was kind of true and now with AI we for a while thought like well you know maybe this is not true maybe you can move fast with quality but we're seeing with Anthropic like they're moving fast and they're breaking things and I mean their business is growing don't get me wrong but but still like I guess this truth did not change because of AI

</details>

**Speaker A**: 是的，这很有趣，因为即使是OpenAI，他们做了像Sora这样的产品，现在他们又把它关停了，因为他们意识到：“好吧，Sora成了个社交网络，对对对，就是那些到处可见的AI生成的猫咪视频。”所以他们意识到，实际上他们做得太多了，现在他们要做减法。现在他们有点重新聚焦在像编程这样能在较小范围内实际产生更多价值的事情上了。他们现在有点走Anthropic的路线，也就是发展速度相当快，但主要聚焦在编程上。所以我认为，看到这种现象在全世界发展最快的公司（比如OpenAI）这样最高层级的规模上实际上演，也很有意思。他们并没有试图包揽一切，现在他们正在重新聚焦，并试图稍微放慢一点脚步。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah it's funny because even OpenAI they did like Sora now they're shutting it down because they realized like okay so Sora is the social network yeah yeah yeah the AI videos like these cat videos that you're seeing all over the place and so they realized like actually like they're doing too much like doing less things now and now they're kind of refocusing on like coding in a smaller set of things that's actually producing more value now they're kind of going the Anthropic route where Anthropic is going like pretty quickly but they they were focusing mostly on coding and so I think that's interesting as well to see that like actually playing out at the highest of scales that like this uh like the fastest growing companies in the world like OpenAI are even doing this like they are not like trying to do everything they're they're refocusing now and trying to maybe slow down a bit

</details>

**Speaker B**: 尽管这有点矛盾，就好像我们几乎是在说，好吧，也许在观察AI时我们学到的一件事是：专注比在很多事情上快速执行更重要。哇哦。

<details>
<summary>Original English</summary>

**Speaker B**: This is a bit con contradictory though like we're we're we're almost saying that well, maybe one thing we're learning observing AI that focus is more important than executing quickly on a lot of things. Wow.

</details>

**Speaker A**: 是的，这很有趣。我觉得这就好像，甚至连开启这一切的那篇论文，比如那篇《Transformers》论文，它的标题就是“注意力机制是你所需要的一切（Attention is all you need）”。有趣的是，它强调的正是聚焦在特定的token上，也就是相关的token才最重要。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, it's funny. It's like like I think even the the paper that started it all like the Transformers paper was titled like attention is all you need where it was funny it was like focusing on like the certain tokens, the relevant tokens like mattered the most.

</details>

### AI生成与设计竞赛的得失

**Speaker B**: 是的。那么，你做过一个很有趣的尝试，就是你为NeetCode（我想是这个网站）举办了一场重新设计的比赛。你提供2500美元奖励给提交重新设计方案的人。你能跟我说说进展如何吗？

<details>
<summary>Original English</summary>

**Speaker B**: Yeah. Well, one one interesting experiment you did is you did a redesign contest for neatcode or I think the the site. You offered $2,500 for whoever submits a redesign. Can you tell me how that went?

</details>

**Speaker A**: 是的，所以我还会去评估结果，但就我目前所看到的而言，确实有点让人失望。我尽量不生任何人的气，或者针对任何人，但在我看来，很明显几乎所有的提交方案都是用AI生成的。这也没关系，比如如果你打算使用AI，这完全没问题。但是，就我目前与少数几个人交流的情况来看，当我问他们一些问题，比如：“好的，就你的设计而言，看起来你做了一些选择，对吧？你移动了一些按钮，删除了一些按钮，你删掉了一些内容，也添加了某些内容。你为什么要这么做？像这样做的利弊是什么？”他们回答不出来。如果他们给出了回答，那显然也是非常含糊的答案，说明他们根本没想过这个问题。就像我，只看了他们的网站5分钟，我就能比他们更好地阐述他们设计中的门道。这就让人很失望。我不觉得这是一个智力问题，我不这么认为。我觉得这关乎努力程度、关乎用心与否，可能也关乎技能储备。比如你是否具备设计的技能。我没有，我肯定不是个设计师。但对于一个网站来说，不管这是什么业务，你应该能够说出：“好的，这是一个关于编程面试的网站，我们可能是想向人们展示这很有趣，或者试图用一种非常清晰的方式来解释它。”没有人能说出这样的话。他们只是专注于设计看起来有多漂亮。他们会说：“哦，这上面的颜色，这种风格看起来简直疯了。”但这并不是我关心的。这也不是大多数人关心的。就像，如果人们不真正了解一个网站是干什么用的，或者它能给他们带来什么价值，那么没人会关心这个网站有多漂亮。我认为这才是用户体验（UX）的核心。它不在于某个东西有多好看。不过，我觉得公平地说，毕竟这是一场比赛……

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, so I'm still going to evaluate the results, but so far from what I've seen it's been a little bit disappointing. I'm going to try not to get like too mad at anybody or make it personal with anybody, but it's very obvious to me that practically all of the submissions are created with AI, which is fine. Like if you're going to use AI that's completely fine. But again, like with the few people so far that I've spoken to and asked them questions about okay, like your design like it looks like you made certain choices, right? You you moved some buttons around, you removed some buttons, you you removed some content, you added certain content. Why did you do it? Like what's the pros and cons of like maybe doing it this way? They can't answer it. And if they do answer it, it's clearly like a very vague answer where they didn't think about it. Like me looking at their site for 5 minutes, I can articulate things about their design better than they can. And it's just disappointing. It's like I don't think that's like a matter of intelligence. I don't think it is. I think it's a matter of like effort and caring and probably skill set as well. Like if you're if you just have the skill set of like designing things. Uh but but I don't. I'm certainly not a designer. But like in terms of a site, whatever like the business is, you should be able to say that okay, so like this is about coding interviews and we're trying to maybe show people that this is interesting or trying to explain it in a very clear way. Nobody can say that. They're just focused on like how pretty the design looks. They're like, "Oh, the the colors on this like the styling looks crazy." But, that's not what I care about. That's not what most people care about. Like, nobody cares how pretty a site is if they don't really understand what it's for or like what value it's going to give to them. I think that's what like UX is about. It's not about like how pretty something is. But, I guess in all in all fairness, right? Like, this was a contest

</details>

**Speaker B**: 是的。这就像你在说：“好吧，如果是获胜的设计将获得2500美元。”我想这在某种程度上稍微改变了激励机制，因为这并不意味着你会为了让人创建一个重新设计而付给他们2500美元。这意味着如果你赢了，你可能会得到那笔钱。当然，提交作品的人越多，获奖的几率就越低。因此，如果我只是按逻辑来分析，值得我投入的努力可能就取决于，比方说，如果有10名参赛者，可能值得投入的努力就相当于250美元左右，或者说像是125美元。所以到最后，当然，你只需要写个提示词（prompt），交给AI就行了。我想你看到的结果是，你收到了大量敷衍了事、缺乏努力的提交作品。然后你发现它们并没有达到标准。

<details>
<summary>Original English</summary>

**Speaker B**: Yeah. Where you're like, "Okay, if the winning design will get $2,500." I guess it kind of flips the incentives a little bit because this doesn't mean that you are paid $2,500 to create a redesign. It means that if you win, you could get that. And of course, the more the more the more people submit something, the the lower the chance. Therefore, if I'm just being logical here, like the effort that's worth me putting into it is let's say maybe if it's like 10 contestants, it's like maybe $250 or like if it's $125. So, in the end, of course, you just do a prompt, you give it to AI. And I I guess what you're seeing is you're getting a lot of low effort submissions. Uh and you're seeing there's like not not up to par.

</details>

**Speaker A**: 是的，我原本以为办一场比赛是实现这个目标的正确方式，因为那样我就不必去雇人，不必去筛选人员之类的事情。但事后看来，我觉得这可能并不是个好主意。我可能应该去寻找，甚至哪怕只是一个小圈子的人，然后预先支付他们费用，接着看看成果，然后再据此做出选择，因为我觉得确实有很多人敷衍了事。老实说，这让人很失望。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, I thought that a contest would have been the right way to do it because then I don't have to like hire, I don't have to like filter people and stuff like that. But, in hindsight, I think it probably wasn't. I probably should have just found like and maybe even just a small pool of people and then just paid them up front and then just saw the work and then maybe chosen based off that because I think there has been like a lot of low effort. It's been disappointing to be honest with

</details>

**Speaker B**: 好吧，活到老学到老（吃一堑长一智）。但我想这确实证明了，仅仅给AI一个提示词（这是一种低努力、低成本的做法），并不会带来什么神奇的付出结果，尤其是在设计领域。

<details>
<summary>Original English</summary>

**Speaker B**: Well, you you live and learn. But, but I guess it it does prove that just giving a prompt to an AI which is low effort, low cost, it will not result in magical effort, especially not with design.

</details>

**Speaker A**: 是的，我认为是这样。我觉得这很可笑，因为我觉得人们明明可以只用笔和纸，大体描述一下他们试图做的事情。比如，那些能让事物变得更好的主要选择。比如在我的网站上，即使是我用AI辅助编写的那部分代码，我也能准确地解释为什么所有东西要按特定方式摆放。我可以回顾并说：“好吧，从数据指标来看，这个功能使用得最多，所以我想把它做得显眼一点。我想……把这个做得和你在其他网站上看到的有些不同，这样它看起来就不会很无聊。”诸如此类的事情。但是，那些提交设计的人，他们无法向我阐述清楚这些细节中的大部分内容。我觉得，正如我所说，如果你只是在纸笔上构思好，然后把它交给AI，那么AI可以直接帮你实现出来。比如，我不在乎一个东西看起来有多漂亮。我告诉过他们我真正在乎的标准是什么。然而，我认为，有些参赛者就是没有遵守指示或者其他什么原因，不过我想这也没关系。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, I think so. And I think it's funny because I think somebody could just use pen and paper, just kind of describe like what they're trying to do. Like, the the main choices that make something better. Like, I on my site, even the parts that I've used AI to code, I can articulate exactly like why everything is positioned in a certain way. I can go back to like, "Okay, like metrics, like this is used the most, so I want to make this prominent. I want uh to make this like a little bit different than you've seen on other sites so it doesn't look boring, stuff like that. But, the people like submitting the designs, they can't really articulate a lot of these things to me. And I think, like I said, if you just do it on pen and paper and then give it to an AI, then the AI can just do it. Like, I don't care how pretty something looks. I I told them like what criteria I actually cared about. And uh I think, you know, some people just didn't follow the directions or whatever, and that's that's fine, I guess.

</details>

### 关于“编程终结”的探讨

**Speaker B**: 你几个月前抛出了一个颇具争议的观点：我们所熟知的编程即将终结。我们来聊聊这个吧。蒂姆·奥莱利（Tim O'Reilly）大概一年前写过一篇博客文章，他在文章中预测事物将会发生改变，而你对此做出了反思。

<details>
<summary>Original English</summary>

**Speaker B**: One of your hot takes from a few months ago, the end of coding as we know it. Let's let's talk about it. Uh Tim O'Reilly wrote a blog article that about a year ago where where he predicted that that things would change, and you were reflecting on that.

</details>

**Speaker A**: 是的，我觉得这真的是……

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, I think it's been really

</details>

<!-- chunk 10/13 -->

### 行业变化与不变的核心价值

**Speaker A**: 这很有趣，因为很多人并不太会回顾过去审视事情。他们只是一味地向前看。但是，我认为回顾并观察事情是如何发展的是很重要的，因为那也能帮助你预见事情在未来会如何演变。看看编程领域发生了多大的变化，模型变得多么优秀，这真的很有意思。但同时让我有些惊讶的是，我们现在似乎仍处于一种非常观望的状态。比如，各家公司依然在裁员之类。但从许多方面来看，事情并没有像我预期的那样发生剧变。就像我那些在大型科技公司的朋友，他们现在写代码的方式已经完全不同了。但就业务的运作方式而言，他们做的事情还是大同小异。比如，绝大多数人并没有被裁掉。大多数人仍然在职。他们还在工作。他们甚至做的工作比以前更多。而且我认为公司有时也意识到，他们可能在人工智能的方向上走得太远了，所以他们试图重新平衡。这仍然是一场关于权衡取舍的博弈。这仍然是一场“快速行动，打破常规”的博弈。我认为编程无疑将会继续深刻地改变，你知道，它甚至可能会变成一个完全不同的领域。但是，我认为许多围绕业务层面的东西——比如了解要创造什么样的价值，以及在工程决策上的权衡取舍——这些绝对不会消失。我认为永远不会。因为你怎样才能让一个大语言模型（LLM）来替你权衡取舍呢？我认为，评估在一般工程中究竟什么才是重要的，这是一件非常属于人类的事情。

<details>
<summary>Original English</summary>

**Speaker A**: interesting because a lot of people don't really go back to actually look at things. They're just like forward-looking. But, I I think it's important to like go back and see how like things played out cuz that can help you like see how things are going to play out in the future as well. And it's been interesting like with how much coding has changed, with how good the models have gotten. At the same time, it's kind of surprising to me that we're still in like a very wait-and-see mode. Like, companies are still doing layoffs and things like that. But, in many ways, things have not changed as much as I would have expected. Like, a lot of my big tech friends, they're still like they're they're coding completely differently now. But, in terms of like the way the business is working, they're kind of doing like similar stuff. Like, they're all like most people are not getting laid off. Most people are still employed. They're still doing work. They're doing more work than before. And I think companies are sometimes realizing that they may maybe moved too far in the direction of AI, so they try to rebalance. It's still like a game of tradeoffs. It's still a game of like move fast and break things. I I think programming is definitely going to continue to change definitively, and you know, maybe become a completely different field. But, I think a lot of stuff around like the business, knowing like the value to produce, and just like engineering decisions in terms of tradeoffs, that stuff is absolutely not going away. I I don't think ever. Because how can you have an LLM weigh like the trade-offs for you? I think that's a very like human thing to evaluate what's even important in engineering in general.

</details>

**Speaker B**: 是的，而且比如，在编程中当你思考我们究竟在编写什么时，你需要构建一个功能。你知道，任务是添加一个按钮，比如当用户点击它时，我不知道，它会提交一个投诉。或者类似这种，你知道的，这样他们就可以报告一个 Bug。这是一个简单的例子。你知道，那不仅仅是幕后简单的一句“如果点击按钮，就提交 Bug”，它会涉及一堆边缘情况。它需要检查状态。你需要了解上下文是什么。比如以及该说什么，用户是哪种类型，是免费用户，还是付费用户？这里有所有这些边缘情况、条件、领域知识、业务领域，所有这些东西，它们过去都被捕获在代码中，这意味着它们其实存在于你的脑海里。但现在你改成去提示（prompt）它了，那些上下文依然存在，还是需要有人知道那有多重要，比如……

<details>
<summary>Original English</summary>

**Speaker B**: >> Yeah, and also like for example, things like you know, in programming like when you think of like what is it that we code, you need to build a a feature. You need to you know, the task is add a button where I don't know when when the user hits it it I don't know, it's it files a complaint. Something, you know, like so they can report a bug report a bug. That's a simple one. You know, like that is not just a simple behind the scenes of of like if button hit file a bug, it will have a bunch of like edge cases. It will it will check the state. You will need to know what the context is. Like and what what what to say, what kind of users are free user, paid user? Like there's all these edge cases, conditions, the domain, the business domain, all of these things and they were all captured in code, which means it's captured in your head. But now that you're prompting it, the context is still there and someone needs to know how important it is like

</details>

### 应对变化与微软的买断裁员

**Speaker A**: 是的，我想“变化”本身可能是唯一不变的东西，因为变化一直在发生，我不是想讲双关语，但是，比如我刚刚看到，好像是昨天还是今天，微软正在进行我认为是自愿性的裁员，他们正在……

<details>
<summary>Original English</summary>

**Speaker A**: >> Yeah, I think like change is the one thing that's not changing because change is just keeps happening and I didn't mean to make that a pun, but um like I just saw I think yesterday or today Microsoft is doing I think voluntary layoffs where they are

</details>

**Speaker B**: 是的，买断离职（buyouts）。是的，所以基本上，如果有人愿意，他们可以选择离开公司并获得一笔遣散费。我看到了，我还没确认，但我问了一个朋友，他们说这是真的。买断离职是真的，但关于年龄的说法目前还不确定。但基本上，他们只向一部分人提供这个方案，这些人要达到一定的年龄，并在公司有一定年限的经验，这有点好笑。比如，如果你到了某个特定年龄（我不知道具体年龄），并且在微软工作了 10 到 15 年，他们就只向这群人提供这个选择。如果要推测的话，我认为这是因为也许那些人不太容易改变，他们可能不太愿意去学习一套全新的做事方法。所以微软向他们提供这个选择，因为现在他们必须朝着一个新的方向前进。我想当年萨蒂亚（Satya）刚接手时，他们也做过非常类似的事情。我不知道当时是不是自愿的，但他们确实进行了大规模裁员。主要都是针对……

<details>
<summary>Original English</summary>

**Speaker B**: >> Yeah, buyouts. Yeah, so basically if somebody chooses to they can leave the company and get like some severance. And I I saw I I haven't confirmed this, but I asked a friend and they they said it's true. The buyouts are true, but not like the age thing yet. But basically they're only offering this to a subset of people at like a certain age and certain amount of experience in the company, which is kind of funny. Like if you were like if you're like a certain age, I don't know the exact age and you have like 10 to 15 years at Microsoft, they're only offering it to those people, which I think to speculate I think it's because maybe those people are less prone to like changing, they're less willing to maybe learn a completely new way of of doing things. And so Microsoft is offering it to them because like now they have to move in a new direction. I think they did something very similar when Satya originally took over. I think they did I don't know if it was voluntary at the time, but they did a lot of layoffs. It was mostly to people

</details>

**Speaker A**: 2014 年的那次并不是自愿的，是的。

<details>
<summary>Original English</summary>

**Speaker A**: >> That that was not voluntary in 2014, yeah.

</details>

**Speaker B**: 是的，当时那次裁员就是专门针对很多经验丰富的老员工，而不是针对新人。所以我觉得，仅仅是愿意去改变，愿意用一种你可能并不喜欢的方式去做事——有点像我刚加入谷歌时，不得不去做一些无法像我期望的那样深入钻研的事情。我认为这种意愿将变得非常重要。

<details>
<summary>Original English</summary>

**Speaker B**: >> Yeah, and so that was to a lot of experienced people specifically and not to the new people. So I think just being willing to change, being willing to do things in a way that you didn't you don't maybe enjoy kind of like when I joined Google like having to to do things not going as deep as I would have liked. I think that's going to be pretty important.

</details>

### 程序员的未来与抽象的成本

**Speaker A**: 是的，而且你确实说过，即使编程方式发生改变，你也不认为程序员或编程会走向灭绝，对吧？

<details>
<summary>Original English</summary>

**Speaker A**: >> Yeah, and you you did say that you you don't think there will be an extinction of programmers or programming even if programming changes, right?

</details>

**Speaker B**: 是的，我想即使到了今天，这也是无法预测的。我的猜测和任何人的猜测一样，但我就是不认为“思考”会消失，我不认为“解决问题”会消失。我觉得它会发生剧烈的变化。有可能我们确实会需要更少的程序员，但哪怕到目前为止情况也并非如此。每一次出现重大的创新，比如云计算，比如更高级的编程语言，不知为何事情并没有……它并没有导致程序员的数量减少。而我原本预期它是会的。比如当你有了云服务，可以直接解决那些曾经非常棘手的巨大难题。像谷歌过去不得不费尽心思去解决某些分布式系统问题。而现在你可以直接使用 AWS 或 GCP，让它们替你搞定。所以你可能会想，我们现在拥有了无限的软件能力，我们什么都能做，而且一切都很简单，那我们就不需要那么多程序员了——但这并没有发生。所以基于这一点，我也说不准。你可以看到像 Replit 和 Lovable 这样的东西，现在任何人都可以成为程序员。所以我不知道我们是否正朝着一个极度高层次抽象的方向发展，但是……

<details>
<summary>Original English</summary>

**Speaker B**: >> Yeah, I think even to this point again it's like it's impossible to guess. Like my guess is as good as anybody else's, but I just don't see like thinking going away. I don't see problem solving going away. I think it'll change dramatically. It is possible like we might need like less programmers, but even to this point that hasn't been the case. Like every single time there's just like the big innovation like cloud computing, like higher level programming languages, for whatever reason things do not like it doesn't lead to fewer programmers. And I would have expected it would have. Like when you have cloud like cloud services that can just solve these huge problems that were so difficult to solve. Like Google had to work so hard to solve like certain distributed system problems. And now you can just use AWS or GCP and just have that taken care of for you. So you would think that we just have infinite software where we're just like just doing everything and everything is easy and now we don't need as many programmers, but it just hasn't happened. And so based on that I don't know. Like you see things like Replit and Lovable where anybody can be a programmer now. And so I don't know if that's the direction we're going to go in where it's just very very high level, but

</details>

**Speaker A**: 但这非常有趣，因为一方面，我们当然拥有像云计算这样越来越强大的底层基础设施（primitives）。你会认为在 AWS、Azure、GCP、Oracle 等等之间存在组合运作。所以，你知道的，价格显然会尽可能地低。但另一方面，你又会看到像 DHH（David Heinemeier Hansson）这样的人，他说：“好吧，我们在使用 AWS。我们每年要花几百万美元。你知道吗？抛弃亚马逊的服务，我们直接在本地自己弄。” 所有人都认为这会很昂贵诸如此类的。但他们去做了，而且他们现在节省了大量资金。所以，这就好像是，这些抽象往往变得运行起来更加昂贵。这对大多数人来说没问题。但是当你达到一定的规模时，你可能就会开始投资招募软件工程师，构建你自己的软件并维护它，仅仅是为了降低成本，这正是 37 Signals 所做的。所以我在想，在一定的规模下，也许永远都会有这样的价值存在，你知道，比如构建你自己的技术栈，或者深入到比你从那些预构建服务中得到的更底层的地方去。

<details>
<summary>Original English</summary>

**Speaker A**: >> But it's very interesting because on one end of course we have these primitives that are getting more and more capable like the cloud. You would think there's composition between AWS, Azure, and GCP, Oracle, and so on. And so, you know, the prices will obviously be as low as possible. But then, you have someone like DHH who is like, "Okay, well, we're in AWS. We're spending a few million dollars per year. You know, like get rid of the Amazon services and and just do it locally." Which everyone thinks is going to be expensive and and so on. And they do it, and they're now doing a massive saving. So, it's almost like the these abstractions are often becoming a lot more expensive to run. Which is fine for for most people. But when you get to a certain scale, you might start to invest in software engineers and building your own software and maintaining it to just reduce costs, which 37 Signals has done. So, I I wonder if if anything, there might always be a value in at certain scale, you know, like rolling your own stack or or go a level lower than what you're getting from what whatever pre-built stuff.

</details>

**Speaker B**: 是的，我也这么认为。我觉得从长远来看事情将如何发展总是很有趣的。工程不是一门科学。它里面包含了很多文化因素，你会看到有些公司——就像在云服务领域，为什么像 MongoDB 这样的公司能做这么大？我觉得技术可能只是一小部分原因，很大程度上其实就是销售、营销和文化。如果有一家公司在使用它，它就会产生滚雪球效应，然后你就会看到整个行业都在使用某一种特定的工具。然后也许他们会意识到，实际上我们在这个方向上走得太远了，我们不需要把所有东西都放在云端。它并没有更好。它也没有为我们省下那么多钱。在某些方面，我们已经看到云服务变得非常非常复杂。现在就像是“云驱动开发”。你面对着所有这些东西，就像是：“好吧，你解决了一个问题，但现在你又遇到了一个新的问题。”对于大语言模型（LLM）来说，也有点类似。甚至连人工智能的成本问题可能也会逐渐浮现，一旦补贴开始耗尽——我们已经开始看到这种迹象了，我认为这将成为一个非常严重的问题，也许所有那些拥抱 AI 编程的公司现在都将削减这方面的投入。

<details>
<summary>Original English</summary>

**Speaker B**: >> Yeah, I think so. I think it's always interesting to see how things play out like in the longer term. Engineering is not a science. Like there's a lot of culture that goes into it, and you have companies that like in the cloud, like why did a company like MongoDB get as big as it did? I think like the tech might be like a small part of it, but I think it a lot of it is just sales and marketing and culture. And if like one company's using it, it can snowball, and then like you have an entire industry using a certain tool. And then maybe they realize like actually like we went too far in the direction like we don't need to have everything in the cloud. Like it's not better. It's not saving us that much money. And some ways like we've seen cloud services get really really complicated. Now it's like cloud-driven development. And like you have all these things, and it's like, "Okay, you solved one problem, and now you got a new one." With LLMs, it's like kind of the same thing. And even the cost issue with AI is probably going to be like once the subsidies start running out, which we're starting to see, I think that's going to be a really big issue where maybe all these companies that embraced AI programming are now going to like cut back on it.

</details>

**Speaker A**: 是的。你搭上了一辆疯狂的列车……

<details>
<summary>Original English</summary>

**Speaker A**: >> Yeah. You had a wacky train

</details>

<!-- chunk 11/13 -->

### 关于AGI与技术极限的探讨

**Speaker A**: 我想聊一聊这个话题。这涉及到AGI。我不太喜欢谈论AGI，因为我觉得它很难……你知道的，很难讨论，很难定义。不过，我们还是来聊聊吧。就像你之前说的，假设会有一个AGI，或者说是一个神一般的奇点。这些模型会非常惊人，虽然我认为我们能看到它们还有局限性，但我们就假设直接跨越到那一步。关于我们如何追求它，你有什么想法？

<details>
<summary>Original English</summary>

**Speaker A**: I'd like to talk about it. It involved AGI. I'm not a huge fan of talking about AGI cuz I feel it's very like you know like hard to talk hard hard to define. But but let's talk about it. This this was like you were saying like let's assume that there would be an AGI or a god-like singularity. These models would be amazing which I think we can see they have limitation but let's let's just jump like forward. What was this thought on on like how we were chasing it?

</details>

**Speaker B**: 是的，我认为在哲学层面上，感觉就像是你试图触及无限，但你越靠近它，你离它的距离似乎依然没变，对吧？所以，这就让我觉得，随着技术变得越来越好，你可能会认为我们现在已经解决了生活中的所有问题。就像我们拥有了丰富的资源，就算还没有，我们距离为每个人提供足够的食物、水和住所也不远了。但是，关于生活，有些东西——也许是人性或者别的什么——它就是不会改变。你总是想要更多。比如，现在有了更高层次的编程。所以人们现在在更高层面上竞争，而且随着层次越来越高，人们还是会在某种层面上继续竞争。现在开发一个应用可能很容易，但在营销、边缘情况（edge cases）以及类似的事情上，又会有新的问题需要解决。

不过我也觉得，这也许是个政治问题，因为我认为面对技术，我们大家都应该为技术的进步感到高兴。如果AI不断进步，如果在某些方面它真的取代了所有的工作，那肯定是一件好事，因为现在你可以做一些以前做不到的事情，比如农业。我确信当那些农业工作消失时，很多人感到难过，但这总体上是一个净收益（net positive）。我认为它唯一不会成为好事的理由就是——如果你的生计依赖于此，而且在政治上，你知道的，你赚不到钱，然后政府又不打算照顾你。我觉得这才是问题的所在。这感觉更像是一个政治问题，而不是技术问题。

<details>
<summary>Original English</summary>

**Speaker B**: Yeah, I think like on a philosophical level like it feels like you're trying to get to like infinity and it's like the closer you get you're the same distance away from it, right? And it's like that's where I feel like it feels like as like technology has gotten better you would think that like we've solved life at this point. Like we have like abundant resources and if we don't like we're not that far away from having enough food, water, and shelter for everybody. But it's like something about life like maybe it's human nature or something it just doesn't change. It's like you want more like Okay, now there's like higher levels of like programming. So now people are competing at like the higher level and like as it gets higher and higher the people are still going to be competing like on some level. Like maybe it's easy to like build an app now but there's going to be a new problem to solve like on marketing and like edge cases and things like that. But I also think like maybe this is like a politics thing because I think there's like technology which we should all we should all be happy that technology is improving. Like if AI keeps getting better if it really does replace every job in some ways that has to be a good thing because now you could do something you couldn't do before like farming. A lot of people were sad about that when when that went away I'm sure but it's been a net positive and I think the only reason it wouldn't be a positive is because like if your livelihood depends on it and like politics you know you can't make money and then the government isn't going to take care of you. I think that's where it becomes an issue. It's like it's more of a politics problem than a technology problem.

</details>

**Speaker A**: 是的，但是我觉得，我有一个有趣的观察，那就是当我们看到AI可以让事情变得更好时，我仍在等待普通的报税软件能够变得让大众都易于使用。为什么我在我居住的每一个国家，都必须雇佣会计师来帮我报税，即便我的税务情况并不复杂？这只是其中一点，还有我们说到公共设施，当你的水管破了，当你想找个水管工的时候。所以，在一些日常事务上，我非常欢迎软件能让事情变得更简单，但是在过去的15年多时间里，我并没有看到多少进展。甚至现在有了AI也是如此。所以我会觉得，这可能是一个很好的契机，让我们能看到这些事情得到改善。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, but I I think know, my an interesting observation is like as we're seeing AI could make things better. I'm still waiting for the software to file taxes to be accessible to a normal person. Why do I in every country I live, I have to hire an accountant to file my taxes even though I don't have very complicated taxes. And that's one and we're talking utilities, when your pipe is broken, when you when you when you want to find a plumber. So there there's some everyday things where like I I I would welcome software making things easier and I but I haven't seen much progress in the past like 15 plus years. And not not even right now with AI. So like I'm like could be a nice trigger to like see those things improving.

</details>

**Speaker B**: 是的，我觉得这挺有趣的。因为你纵观历史，我认为我一直理所当然地以为的一件事，就是进步总是会发生的，事情总是会变得更好。但是，如果你看看过去几千年的大部分历史，事情并不总是越变越好。有时候你会看到文明变得极其伟大，然后它们又某种程度上崩溃了，随之很多技术也失传了。我不认为事情就是注定会不断地变得更好。我觉得，可能会有很多关于政治和政府方面的决策，相应的政策会被制定出来，我认为这将对真正关系到人们以及他们生活等方方面面的事情产生巨大的影响。

<details>
<summary>Original English</summary>

**Speaker B**: Yeah, I think it's funny because like you look at history and I think one thing that I always take for granted is that like progress always happens and that things always get better. But if you look at like most of history for thousands of years, things didn't always get better. Sometimes you saw like civilizations get really great and then they kind of collapsed and a lot of the technology from that was lost. I don't think it's like preordained that things are just going to continuously keep getting better. I think like there's going to be a lot of decisions probably on like politics and government side where like policies are going to get created and I think that's going to have like a really big impact on what actually matters to people and like their lives and stuff like that.

</details>

### AI工具对技能的侵蚀

**Speaker A**: 你的另一个尖锐观点是，过度炒作AI工具只会制造出“废料（slop）”，并且会侵蚀人们的技能。

<details>
<summary>Original English</summary>

**Speaker A**: Another one of your hot takes is how overhyping AI tools just create slop and erodes people's skills.

</details>

**Speaker B**: 是的，我认为很多人，特别是学生，不幸地正在通过大语言模型（LLMs）学习一切。所以其中的很大一部分并不算是真正的学习。他们只是在某种程度上作弊，而且他们就是这样完成所有事情的。然后他们就失去了很多技能。我认为从长远来看，这将会非常有趣，因为我们甚至在经验丰富的程序员身上也看到了这一点。我有一个朋友告诉我，他现在正在准备面试，而他已经好几个月没有怎么手写代码了。所以现在对他来说，要重新找回那种状态非常困难。

<details>
<summary>Original English</summary>

**Speaker B**: Yeah, I think a lot of people, especially students, are unfortunately learning everything through LLMs. So a lot of that isn't really learning. They're just kind of cheating and they're just doing everything like that. And then they lose a lot of their skills and I think long-term, that's going to be really interesting because we're seeing that with the even experience programmers. I had a friend tell me that he he he's like preparing for interviews now and he hasn't like handwritten much code in several months. So it's very hard for now him to get back into that.

</details>

**Speaker A**: 是的，这可能会是一个较长的时间周期，但我确实在想，这会不会带来一个副作用：更多的公司将会进行线下面试，因为这样你就排除了任何AI的辅助。你可以真真切切地和一个人交谈。然后在面对面的情况下，你能切实分辨出谁是投入了努力、能够思考、头脑敏锐、能够将事物融会贯通的人，谁又是在没有AI触手可及的情况下就会直接僵住的人。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, this will be a longer time frame, but I do wonder if one side effect of this could be that a lot more companies will be doing in-person interviews because you you eliminate any AI assistance. You can actually talk with a person. And then in-person, you can actually tell the difference between someone who has put in the effort and can think and is sharp and can put things together versus someone who gets like frozen without the AI being there at their fingertips.

</details>

**Speaker B**: 我觉得这非常有趣，因为我想也许公司们并不会在意。我觉得我可能就是那种会僵住的人之一。即便是在我工作的时候，我也很不擅长从头开始写代码，但如果我看着一个文件，我能看到所有的导入（imports），能看到装饰器（decorators）等等。像那样的代码我倒是挺擅长的。我有点像个“复制粘贴型”程序员，就是大量复制粘贴代码片段，然后替换掉其中的变量之类的。我想，我的尖锐观点也许是，可能有些东西实际上受到的测试会变少。比如，只要你能理解代码，人们可能就不会那么在意你是否真的能手写代码。这就是我在一些AI辅助评估中看到的现象。就像是，“好吧，如果你愿意，如果你有能力，你完全可以直接用AI来实现这一切。”但是，如果面试官问你，“好的，这个整数数组，在这个代码的上下文中，这些整数实际代表什么？可能它是某物的数据点，或者它是两点之间的最短距离，又或者是别的什么，对吧？”你必须能够将其清晰地表达出来，并把它弄清楚。所以，我觉得这很有趣。也许我在给出一个“我完全不知道”的类似回答，但看到正在发生的这些轶事真的很有意思。

<details>
<summary>Original English</summary>

**Speaker B**: I think it's really interesting because I think like maybe companies won't care. I think I'm probably one of those people that would get frozen. Even when I was working, I was very bad at like writing code from scratch, but if I'm like looking at a file, I see all the imports, I see the decorators and stuff like that. Like I'm pretty good at coding that. I was kind of a copy and paste programmer where I'm just like copy and pasting a lot of snippets and then just replacing the variables and things like that. I guess maybe my hot take is that like maybe certain things actually will be less test Like maybe like people just won't care that much if you can actually handwrite the code as long as you can understand. Like that's what I'm seeing with like some of the AI assisted assessments. It's like, "Okay, like you can actually just go ahead and like implement this with AI like all of it if you want to if you're able to do that." But then if the interviewer asks you, "Okay, this array of integers, what do the integers actually represent in the context of like this code? Like maybe it's like data points on something or it's like the shortest distance between something or whatever, right?" You you have to be able to like articulate that and like figure that out. So, I think it's interesting. Like maybe I'm giving the same answer where like I have no idea, but it's interesting to see like the anecdotes that are happening.

</details>

### 性格特质与能动性

**Speaker A**: 那么，你的另一个观点是，你提到你认为现在性格特质（personality traits）比编程技能更重要，或者说实际上比大多数技能都重要。

<details>
<summary>Original English</summary>

**Speaker A**: Well, one other take you have is you said that personality traits you think are now more important than coding skills or actually most skills.

</details>

**Speaker B**: 是的，或许“性格特质”不是最准确的表达方式，但我认为，你所雇佣的那个“人”身上有一些东西很重要。他们不是机器，对吧？他们不是说，好，你看着简历说，“好，Java程序员”或者别的什么。他们不是那样的。我认为人，尤其是在像软件开发这样非常开放性的领域里，决策至关重要，权衡（trade-offs）至关重要，沟通以及所有这些东西都至关重要。当我在招聘时——几个月前我招了一个人，他们具备某些技能。显然，他们还在读计算机科学学位，甚至还没有毕业。但他们比我以前雇佣过的几乎任何人都强得多，甚至比那些有经验的人，比那些我本可以招进来的、在大型科技公司工作且有着非常华丽简历的人还要强。然后我就问自己，究竟是什么让这个人如此出色，而另一个人很糟糕或者效率较低？归根结底还是在于这个人本身。我认为，在初创公司里，这个词叫做“能动性”（agency）。就像一个拥有高能动性的人，他就是会去把事情完成，永远不会对某项任务说“不”。我认为，这种“好的，如果我不懂某样东西，我就去学”的态度非常重要。就像，我不会说“那不是我的工作”，或者“我不打算深入研究那个”。比如，任何时候我给这个人分配一个任务，即使他们完全不知道该如何着手，一周之后，他们就能把关于这事的一切都学会。这对他们来说就像是一个全新的领域。他们就是能学习一切。我觉得，像那样的性格特质，很难去描述它。也许“能动性”是最好的词汇，但我……

<details>
<summary>Original English</summary>

**Speaker B**: Yeah, maybe personality traits isn't the best way to phrase it, but I think there's something about like a person that you're hiring. They're not a machine, right? They're not like Okay, like you look at the resume like okay, Java programmer or whatever. They're not that. I think people, especially in fields like software development, which are very open-ended and like like decisions matter, trade-offs matter, communication, all that stuff matters. When I'm hiring people, I hired somebody a few months ago and they had certain skills. Like obviously they were going through like their CS degree. They still haven't even graduated yet. But they are far better than practically anybody I've ever hired before, including people that are experienced, including people that I probably could have hired that are working at like big tech and like have like these really big resumes. And then I ask myself like what is it that makes like this person good and another person bad or or less effective? It just goes back to the person. I think like in startups the term is agency. Like somebody who's high agency who's just going to get things done, who's never going to like say no to something. I think like that attitude is really important of like okay, if I don't know something, I'll just learn it. Like I'm not going to say like that's not my job or I'm not going to like dig deep into that. Like anytime I give this person a task, even if they have no idea like how to start it, like a week later they'll have like they'll have learned like everything about it. It's like a completely new domain to them. They just like learn everything. I think like those types of personality traits, it's hard to describe that. Maybe like agency is the best term for it, but I

</details>

<!-- chunk 12/13 -->

### 掌握提问与主动性

**Speaker A**: 我认为那才是最重要的，因为现阶段你需要的任何信息，差不多都可以通过提示词来获得，对吧？就比如，我有一个非常具体的编程问题，只要你知道该问什么问题，你完全可以从提示词里得到答案。而知道该问什么问题，其实就在于你是否愿意投入精力。

<details>
<summary>Original English</summary>

**Speaker A**: think that matters the most because any information that you need at this point, you can kind of just prompt, right? Like Okay, like I have like this programming specific question. You can just You can just get it out of a prompt if you know the questions to ask. And knowing the questions to ask is just a matter of like I think putting in the effort.

</details>

**Speaker B**: 是的，所以我很看重主动性。虽然你没明说，但我能感觉到你指的是那种想要解决具体问题的精力、专注度。这确实很有意思。我最近和一些正在做初创公司的人交流过，显然，他们中很多人做的是 AI 相关的，或者在做 AI 基础设施。他们都在努力寻找产品市场契合点（PMF）。尽管现在他们的开发速度比以往任何时候都要快，但让团队采用他们的产品并没有变得更快，这时候一些看似简单的事情就显得至关重要了。例如，亲自去和潜在客户面谈，去参加技术聚会，住在科技中心或者能经常去交流的地方，去获取反馈，去大型公司内部争取你的第一个客户。而这些与代码本身完全无关。当然，他们创造了自己认为很酷、很创新、与众不同的东西，但现在市面上类似的产品太多了。顺便说一句，他们都有竞争对手。现在，他们必须去说服别人，为什么他们更值得信赖，为什么值得在他们身上押注，等等。而很大程度上，这确实需要一位极具个人魅力的创始人，他要善于说服别人：“来吧，试试我的产品。” 这其实非常有帮助。

<details>
<summary>Original English</summary>

**Speaker B**: Yeah, so I like agency. I'm also sensing you didn't mention it, but it's like energy, focus, wanting to solve something specific. And this is something interesting. I I I've been talking to a few of people who are building startups right now. Obviously, a lot of them are to do with AI or like they're building AI infra, and how they're struggling to find that product market fit. Even though, you know, they can build faster than ever, but it has not gotten any faster to get teams to adopt, and simple things start to matter. For example, talking to a potential customer in person, like going to a tech meetup, living in a tech hub or where you can go more regularly, getting feedback, getting your first customer inside of a big company. And none of these have to do with the the code itself. And of course, they created something that they think is cool and innovative and different, but there's now so many things that are similar. By the way, they all have like competitors. They now have to need to convince them why they are more trustworthy, they're worth being bet on, and so on. And it's it's it's it's a lot of it does have to do with like a charismatic founder who is good at convincing people, all right, try my stuff. It It actually helps.

</details>

### 从 YouTube 学到的沟通技巧

**Speaker A**: 是的，这也是我从做 YouTube 视频中真正学到的经验之一。因为如果你在做一个试图解释某件事的视频，根本没人在乎你有多“正确”，也没人在乎你有多聪明。就像在 LeetCode 论坛上，哪怕你有一个超级疯狂、令人印象深刻且性能极佳的解决方案，如果你无法向别人解释清楚，那就毫无意义。因为别人真正在乎的是你能给他们带来什么价值，你是否能用他们听得懂的方式来表达。当年我做那些视频的时候，我会把某些词咬得更重，去强调某些要点；我也会重复某些内容。我只是想方设法让视频变得非常通俗易懂。不管是深度优先搜索 (DFS)、滑动窗口还是其他任何算法，从技术上讲，任何人都可以写出正确的代码。现在甚至可以让大语言模型直接把代码给你吐出来。但我认为，这其中“人”的部分才是关键——也就是了解观众，弄清楚他们到底在寻找什么，他们真正关心的是什么。我认为这非常重要。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, that's one of the things I actually learned from YouTube as well, because if you're making like a video trying to explain something, nobody cares how correct you are. Nobody cares how smart you are. Nobody cares, like in the lead code forums, if you have this super like crazy like solution that's really impressive and really performing, if you can't explain it. Because what they care about is like the value you can give to them. If you can speak in a way that they can understand. When I was making those videos, I would enunciate certain things more I've like like emphasize certain points. I'd repeat certain things. I just tried to make the video just very digestible. Whether it's a DFS or sliding window or whatever algorithm, anybody can technically get it correct. You can at this point have an LLM just kind of spit it out to you. But I I think like the human part of it, just knowing like people, figuring out like what exactly they're actually looking for, what they actually care about, I think that's something that's Yeah, that's pretty important.

</details>

**Speaker B**: YouTube 确实很有意思，因为至少就目前的 YouTube 而言，我希望它的观众主要还是真实的人类。所以我希望每一次播放都是来自一个真实的人。我确信肯定有一些机器人在刷量，但谷歌一直在打击它们。这是一个真正的注意力经济，对吧？就像订阅数或观看量最高的 YouTuber Mr. Beast，他吸引了最多的眼球，占据了更多人的注意力，而这就成为了货币。全球大概有 80 亿人口，也许能接触到在线视频的人没有那么多，但这就像是一场游戏。如果是场游戏，你在软件工程这个利基市场里已经玩得相当出色了。你在 YouTube 上学到了哪些取得成功的经验？你是如何让人们愿意关注你，愿意把时间——这个可能对科技公司，尤其是初创公司非常重要且极具价值的货币——花在你身上的？

<details>
<summary>Original English</summary>

**Speaker B**: So YouTube is interesting because YouTube today at least it's I would hope it's mostly watched by humans, people. So, every single view I would hope is a human. I'm sure there's some bots there, but Google is fighting them. And it's a real attention economy, right? Like it's the you know, like the Mr. Beast who's the most subscribed or watched YouTuber, he captures more eyeballs, more people's attention, which is the currency. There's 8 billion or so or a bit more people, maybe fewer of them having access to the online videos, but it's kind of like almost a game. If if it's a game, you've been pretty good at it in this niche, which is software engineering. What is something that you've learned on what works in becoming successful on YouTube where people pay attention to you, they give you their time, which is an important valuable currency that might be relevant for tech companies, startups especially.

</details>

### 企业需要真诚与“人设”

**Speaker A**: 我觉得很多公司都在这方面苦苦挣扎。我曾和几个从事开发者关系的人聊过，他们也在做同样的事情，有时候这也像是一场游戏。它有点像政治手腕，关乎你如何“包装”，对吧？关乎你如何表达，如何展示事物，如何推销自己。但同时，我认为保持“真诚”也非常重要。我认为很多公司在这一点上做得不够好。有时候他们试图去模仿，比如你提到现在的 AI 实验室，像 OpenAI 还有负责 Codex 的人，他们整天都在 Twitter 上。他们与人互动，甚至与批评他们的人互动。我认为这很重要。这种真诚通常能起很大作用。人们能闻到虚假的味道，他们能分辨出来。甚至对我自己来说也是如此，如果我说了一些我并不是完全相信的话，那会显得非常明显，大家都能看出来。一旦他们察觉到了，就会失去兴趣。到那个时候，他们连你说的一个字都不会听了，你再说什么也没用了。你必须去建立他们的信任，这很难做到，需要时间去积累。但一旦你获得了信任，它就会产生巨大的影响。

<details>
<summary>Original English</summary>

**Speaker A**: I think a lot of companies struggle with that. I was speaking to a couple dev relations people that are working on the same thing where it's it's kind of a game sometimes where it's a little bit of like politicking where it's like, you know, like it's about packaging, right? Like how you say things, how you present things, how you kind of like present yourself. And it's also about I think being like authentic. I think that's a big thing that companies maybe don't always get right. And sometimes they try to like even with like the AI labs where you're saying that like nowadays like OpenAI and like the Codex people, they're on Twitter all the time. They're interacting with people. They're even interacting with people that sometimes criticize them. And I think that matters. Like that authenticity usually matters a lot. People can like smell the fakeness. They can they can tell. Like even for me, if I'm like saying something I don't quite like believe, I think it's so obvious. And people can tell. Then they just get turned off. Like they're not going to listen to a word you say at that point. And then so it doesn't really matter what you say. You have to like build their trust in a way that it's hard to build. It takes time to get there. But once you have it, it matters a lot. It matters a lot.

</details>

**Speaker B**: 这很有意思，因为我常常在想，如果 Claude Code 不是由 Boris 创造的，它还能不能像今天这么火。Boris 就是那位你经常能在 YouTube 频道上看到的工程师，他也来过我们频道。他是一个非常平易近人，且我认为很谦逊的人。至少在我接触到他的过程中是这样的。他在社交媒体上非常活跃，他分享自己如何使用 Claude Code。这就是非常鲜活的 Boris 个人形象。这个工具不仅仅是某个叫 Anthropic 的公司做出来的，不，它实实在在是 Boris 开发的，他在维护它，他在帮你修 Bug。当你说“哦，这有个 Bug”，他会在评论区直接回复你。我现在也注意到 OpenAI 也是这样，Codex 以前给人的感觉就是由 OpenAI 构建的，但现在有了 Tibo，他是 Codex 的负责人，他也会在网上回复别人，做着和 Boris 非常类似的事情。所以我在想，如果有了这种带有个人色彩的视角……哦，对了，Claude Code 从收入上看绝对是软件领域最大的业务之一。我想它的价值可能高达数十亿美元。具体多少很难估算。所以，这就等于是把一个庞大的商业帝国与一个具体的个人绑定在了一起。

<details>
<summary>Original English</summary>

**Speaker B**: It's interesting because I do wonder if Claude Code had been had become as big as it has if it was not created by Boris. Boris, the engineer who you can see on YouTube channels. He was on this channel as well. He's a very relatable and I think humble person. At least that's how I got got to meet him. He is on social media. He shares how he uses Claude Code. There's a lot of Boris. Like this is not just a tool that is like some by corporate called Anthropic. No, it's actually Boris created it and he's working on it and he's fixing your bugs and you say like, "Oh, it had this bug." And he reply He's in your mentions. And I I now notice OpenAI, it's Codex used to be this thing built by OpenAI, but now it's Tibo who is the the head of Codex and he replies and he does the same similar things as as Boris. So, I I do wonder if this, you know, like the the personal angle where it's it's here Oh, and Claude Code is one of the biggest businesses in the software world in terms of revenue. I think they cost multiple billions. It's hard to track how much. So, like it's a huge business tied to a person.

</details>

**Speaker A**: 是的，我其实挺反感“网红”这个词的，但现在似乎一切都在朝着这个方向发展，甚至对企业来说也是，他们现在必须得像一个真实的“人”。他们必须得有个性。他们必须得……

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, I hate the word influencer, but it does seem like everything is going in the direction of like even for companies like they have to be a person now. Like they have to be a personality. They have to

</details>

**Speaker B**: 平易近人，也许？

<details>
<summary>Original English</summary>

**Speaker B**: Approachable maybe?

</details>

**Speaker A**: 对，对，比如平易近人。对，能让人产生共鸣。得像个人类，对吧？而不仅仅是一个企业形象。甚至对 CEO 来说，有时这确实有帮助。尽管有时候也可能适得其反，我就不点名了，但是，嗯，我觉得这挺有意思的，而且我认为甚至很多公司都在刻意这么做。我觉得像 Meta……你在这方面可能比我了解得更多，但 Meta 有类似内部 Facebook 之类的东西，当你在那上面发布产品时，你得去展示它。你得去提及它，你甚至得稍微吹嘘一下。是的，确实就是去推销它。这是一种技能。我从没想过我有一天会成为一名所谓的网红或者 YouTuber，但这确实是一项技能，而且我认为每个人都应该去培养它。并不是每个人都非得做 YouTube，但无论是在 LinkedIn 还是 Twitter 上，我觉得大胆地展示自己、慢慢形成自己的观点、与他人互动等等，都是非常值得去做的。

<details>
<summary>Original English</summary>

**Speaker A**: Yeah, yeah, like approachable. Yeah, relatable. Like a human, right? Like not just a corporate figure. Even for CEOs sometimes like, you know, it helps the sometimes it does. Sometimes it can backfire, but I won't name any names, but um yeah, I think it's it's funny and I I I think even companies like some companies have that a lot. I think Meta, you probably know more about this than I do, but Meta has like a internal like Facebook or something where it's like when you ship you have like kind of Yeah, you have to like show it off. You have to like mention it. You have to like try to like brag about it. Yeah, exactly. Promote it. That's a skill. I didn't expect that I'd ever be, you know, an influencer or a YouTuber, but it's a skill and I think it's something that everybody should lean in towards. Like not everybody has to do YouTube, but whether it's like LinkedIn or Twitter, I think it's worth, you know, putting yourself out there and slowly forming opinions and like interacting with people and things like that.

</details>

### 关于放弃科技职业的争议观点

**Speaker B**: 是的，你刚才说也许不是每个人都必须去做，但说真的，你之前提出过一个相当有争议的激进观点，大意是有些人真的应该放弃科技行业的职业生涯。我们来聊聊这个吧，这是一个相当……

<details>
<summary>Original English</summary>

**Speaker B**: Yeah, well, you said like maybe not everyone has to do it, but really it is you've had a pretty contentious hot take, which was some people should just give up on tech careers. Let's talk about like that. It's a pretty

</details>

**Speaker A**: 这是一个……

<details>
<summary>Original English</summary>

**Speaker A**: It's a

</details>

**Speaker B**: 极具分量的声明。

<details>
<summary>Original English</summary>

**Speaker B**: big statement.

</details>

**Speaker A**: 这确实是一个措辞非常强烈的声明。而我绝对不是在鼓励大家去放弃。所以我首先要澄清这一点。我甚至在标题中提出这个建议的唯一原因是，我认为，如果你抱着一种不想努力的态度，或者你不想亲自动手做事，也不想去深入钻研问题，要知道在这一行，你必须得那样做。你必须得去完成某些事情。如果你不愿意这么做，我认为你应该清楚自己到底卷入了一个什么样的行业，因为很多人真的不清楚。他们浑水摸鱼地混完了大学学位，差不多是一路作弊过来的，然后他们就指望毕业后能顺理成章地找到一份工作。而我……

<details>
<summary>Original English</summary>

**Speaker A**: It's a very strongly worded statement. And I definitely don't encourage people to give up. So, I I want to make that clear. The only reason I suggested that even in the title was that I think if you have an attitude of like you don't want to try hard or you don't like you don't want to do things yourself and you don't want it to dig deeper into things, like you need to do that. You need to do certain things. And if you're not willing to do that, I think you should know like what you're getting yourself into cuz a lot of people don't know. Like they go through these college degrees, like they kind of just cheat their way through it, and then they expect to have a job at the end of it. And I

</details>

<!-- chunk 13/13 -->

### 努力的价值与持续学习

**Neet**: 我认为你必须评估一下，如果你打算成为那种这样做的人之一，因为这可能并不是最适合你的。不幸的是，人们只是养成了这样做的习惯。但是，就像当我制作那个视频时，有很多人对我感到生气，但令人惊讶的是，绝大多数人表示我可能本可以更温和一点，我认为这是真的。但他们实际上同意我的很多观点。很多人说，你知道吗，你是对的。我意识到我在完全依赖提示词（prompting）的方向上走得太远了。我的水平变差了很多。我现在做出来的产品和东西都更差了，而且我也不再那么享受这个过程了。这让我想要重新专注于学习，并且努力成为最好的自己。所以，我想你知道，我做那个视频时并没有想要冒犯任何人，但我发现没有其他人在谈论这件事，所以我只是觉得我必须站出来做这件事。我当时在我的笔记本电脑上录制了它，我没想过它会像后来那样火爆。我本以为大多数人都不会看到它。嗯，但是是的，我还是把那个视频留在了那里，尽管我可能因此在声誉上受到了一些打击，我不太确定，但我还是保留了那个视频。

<details>
<summary>Original English</summary>

**Neet**: think you have to evaluate that if you're going to be one of those people that does that because it might not be the best for you. People have unfortunately just gotten into the habit of doing it. But like when I made that video, I had a lot of people that were pissed off at me, but surprisingly, like the vast majority of people they said that maybe I could have been a little nicer, and I think that's true. But they actually agreed with a lot of my points. A lot of people said that like you know what, you're right. Like I realized I was going too far in the direction of just prompting things. I I got a lot worse at it. Like the products the things that I'm doing are worse now, and I'm not enjoying it as much. And it made me want to like refocus on like learning and being like the best that I can be. So, I think you know, I'm not trying to offend anybody when I did that, but I think I saw nobody else talking about it, so I just felt like I had to do it. And I I I it on my laptop. and think it was going to blow up the way that it did. I didn't think most people were going to see it. Um but yeah, I left that video up even though it maybe I took a reputation hit from that, I'm not sure, but I left that video up.

</details>

**Host**: 是的，但我认为这最终还是归结于努力，对吧？是的。作为建议，对于那些职业生涯早期、中期甚至后期的软件工程师，他们要么在公司工作，只是想被视为一位出色的工程师（当你想到你在谷歌共事的标准工程师或你认识的那些人时），要么在一家初创公司工作，你会给出什么建议？你认为在今天，要真正从一个拥挤的领域中日益脱颖而出，让你的工作自己说话，需要具备什么？这意味着什么？

<details>
<summary>Original English</summary>

**Host**: >> Yeah, but I I think it it goes back to effort, right? Yeah. And as as advice, what would you advise for software engineers, uh early career, mid career, maybe even later, who are either working at a company and they they just want to be seen as this awesome engineer you when you think of like the standard engineers that you work with either at Google or or the people who you know, or they're working at a at a startup? Uh what do you think it takes today to actually increasingly stand out from a from a crowded space uh to have your your work speak for itself? What does that mean?

</details>

**Neet**: 是的，我认为这是一个非常非常好的问题。我想可能有一些适用于大多数情况的一般性建议。我不知道我是否能想出那样的建议。所以，我要说的是，我认为就像你说的，努力很重要。即使在面试环境中，了解你的受众也很重要。你不是活在自己的世界里参加某种标准化考试。你是在和某个人交谈。你在观察他们对你所说的话有何反应。也许你们并不在同一频道上。有些捷径你是不能走的。比如，如果你在一个团队里，在一家公司里，你要了解你周围的人。了解他们关心什么。向他们提问。和他们开会。如果你不需要的话，不要仅仅做假设。比如我会去和他们交谈，弄清楚什么是重要的，对事情有一个整体的感觉，然后朝着你认为是正确的方向非常努力地推进。也许你需要重新调整一些事情。也许你会走得太远。也许你会犯一些错误。但我认为这就像是一个迭代的过程，一个反馈循环，也就是：好吧，弄清楚你应该做什么，然后非常投入地去完成它，并一直坚持下去。这需要大量的改变。这需要大量的路线修正，这是很困难的。没有人愿意那样做。我总是和我的经理做的一件事是，我总是问他们，如果你对我有反馈，请告诉我。我不会生气的。我想知道。我想知道我怎样才能做得更好。而我所有的经理对此的反应是，他们都非常惊讶。他们会说，首先，如果你刚加入公司就问这个问题，这是一个非常好的问题，因为这告诉我你真的很在乎，而且你真的想要进步。所以，我认为这方面非常重要，因为这样人们就知道你们在同一战线上。他们对你有所了解。他们不必去猜测你脑子里在想什么。你在以这种方式与人们进行沟通。

<details>
<summary>Original English</summary>

**Neet**: >> Yeah, I think it's a really really good question. I think there probably is some like general advice that would apply to like most cases. I don't know if I can think of that. So, what I'm going to say is I think like you said, like the effort matters. Like even in an interview setting, knowing your audience. It's not like you're not just like living in your own head taking like this standardized test. You're talking to somebody. You're seeing how they're reacting to what you're saying. Like maybe they're not on the same page. Like there's certain shortcuts you can't take. Like if you're in a team, you're at a company, know the people around you. Know what they care about. Ask them questions. Have meetings with them. Don't just make assumptions if you like if you don't have to. Um like I talked to them, figure out what's important, get a sense of things and then go very hard in the direction that you think is correct. Maybe you'll have to recalibrate things. Maybe you'll go too far. Maybe you'll make some mistakes. But I think it's just kind of like that iterative process of like that feedback loop of like, okay, figure out what you're supposed to be doing and then work very intensely to do that and then just keep doing that. It requires a lot of changing. It requires a lot of like course correction and that's difficult. Nobody wants to do that. Like one thing I always did with my manager, I always asked them like, if you have feedback for me, please tell me. Like, I will not get offended. I want to know. I want to know like what I could be doing better. And the way my like all my managers ever reacted to that is they were very surprised. They're like, well, first of all, if you just joined the company you're asking this, like, that's a very good question to be asking because like that tells me that you actually care and you actually want to get ahead. So, I I I think like that aspect of it and that matters a lot cuz then people know you're on the same page. Like, they kind of know about you. They they don't have to guess what you're thinking in your head. You're you're kind of like communicating that with people.

</details>

**Host**: 是的，所以我觉得在我们的谈话中，我们不断回到的一点就是努力。并且不要走捷径。我的意思是，当你有像业务成果这样的目标时可以走捷径，尤其是当你在建立自己的业务，或者你有一个要实现的目标时，但除此之外，就是要付出努力去下功夫。

<details>
<summary>Original English</summary>

**Host**: >> Yeah, so I I tried to like I I felt coming through our conversation is is we just keep coming back to it is is effort effort. Like like and and don't take the shortcuts. I mean, take the shortcuts when you have like a business outcome, especially when you're building your business or or you you have a goal that you're going to achieve, but otherwise just put in the work.

</details>

**Neet**: 这听起来很简单。在纸面上听起来真的很容易，但要付诸实践却很难。有时候，尤其是对我来说，我其实不是一个喜欢改变的人。我非常抗拒改变。我讨厌改变。我需要几年的时间才能做出改变。但是……

<details>
<summary>Original English</summary>

**Neet**: >> It it sounds simple. It sounds really easy on paper, but it's hard to like put into practice. Like, sometimes, especially for me, I am not a person that likes change, actually. Like, I am very resistant to change. I hate change. It takes me years to change. But

</details>

**Host**: 你的网站上现在还有 Angular。

<details>
<summary>Original English</summary>

**Host**: >> You still have Angular on your website.

</details>

**Neet**: 是的。但是它如此重要，而且当你实际去改变时，一切都是非常值得的。我认为这意义重大，它就像变成了一种生活方式。比如，一开始我在编码方面投入了大量努力，然后在职业生涯中我意识到，好吧，软技能也非常重要。我花了很长时间才学会这些。直到今天我还在学习，但这可能就是我获得晋升的原因。这也是我的团队喜欢我的原因。讨人喜欢是很重要的。你肯定不想被人讨厌。

<details>
<summary>Original English</summary>

**Neet**: >> Yeah. But um but it's so important and it's so worthwhile when you actually do it. And I think it just matters a lot and it's like it becomes a way of life. Like, you start like I put in a lot of effort on the coding side and then in professional life I realized, okay, like the soft skills matter a lot. Took me a long time to learn them. I'm still learning them to this day, but that's the reason why I probably got promoted. That's the reason why like my team liked me. It's important to be likable. Like, you don't want to be hated.

</details>

### 获取灵感的来源

**Host**: 作为结束，你平时都从哪些地方获取灵感？可以是书籍，可以是视频，也可以是 YouTube 频道。

<details>
<summary>Original English</summary>

**Host**: >> And as closing, what are places that you get inspirations from? This could be books, this could be videos, this could be YouTube channels.

</details>

**Neet**: 是的，我想你刚刚采访过 Martin Kleppmann。我是他的超级粉丝，也是他那本书的超级粉丝，因为他讲得非常深入。即使他已经讲得如此深入，在每一章的结尾你还会看到一百个参考文献。我非常喜欢这一点，因为我是那种总是会提出后续问题的人。我总是想更深入地了解事物。所以，看到像他这样的人，我发现我更容易与科学家、拥有博士学位的人以及研究人员产生共鸣，而不是单纯的工程师。所以我真的非常喜欢这一点。我认为拥有可以仰望并渴望成为其那样的人是很重要的。有很多能给我带来灵感的人，包括其他 YouTube 创作者，包括技术领域的人，也包括我过去共事过的人。我总是在观察一个人，试图发现他们身上我真正欣赏的品质，然后我也会尝试去复制和模仿他们。

<details>
<summary>Original English</summary>

**Neet**: >> Yeah, I think you just had Martin Clapton on. I'm a huge fan of him, huge fan of his book because he goes deep. And even like as deep as he goes, then you'll have a hundred references at the end of every chapter. And I just love that because I'm the type of person like I just always have a follow-up question. I always want to go a little bit deeper to understand things. And so, seeing people like him, like I relate more to like scientist, people like PhDs, researchers more than I do to engineers. So, I just really like that. I think it's important to have people that you can like look up to and aspire to be like. And I think there's there's plenty of people I take inspiration from, including other YouTubers, uh including technical people, including people I've worked with in the past. And I always I always look at a person and I I try to see like qualities about them that I really like and then I try to like replicate them and imitate them as well.

</details>

**Host**: 太棒了。能请你来到这里，特别是能当面交流，真是太棒了。

<details>
<summary>Original English</summary>

**Host**: >> Neat. It was awesome to have you here, especially in person.

</details>

**Neet**: 是的，这很棒。很高兴见到你。

<details>
<summary>Original English</summary>

**Neet**: >> Yeah, it was great. Great meeting you.

</details>

### 结尾总结与感悟

**Host**: 我很高兴我们终于能和 Neet 录制这期播客。我喜欢他的坦诚，我也希望这种坦诚能够传达给大家。我觉得 Neet 现在的招聘方式很有意思。[音乐] 他经营着最大的编程面试准备网站之一，但他招聘时看重的却是编程以外的技能。他看重动力，看重候选人是否能清晰解释自己的思路，最重要的是，他看重主动性（agency）[音乐] 或者说把事情做成的能力。和他探讨他对公司的看法也很不错，他认为公司根本不知道如何评估候选人，而且可能一直都不懂。LeetCode 式的面试之所以能存活下来，并不是因为它能预测工作表现——它就是不能——而是因为没有人找到能够规模化运作的更好方案。最后，[音乐] 我非常认同 Neet 的观察：正因为 AI 让其他一切都变得廉价，努力本身正成为一种差异化优势。任何人都可以通过提示词生成一个设计、一个功能或一个答案，但你无法通过提示词生成“在乎”的态度，也无法在别人问你“为什么你要这样做？”时，通过提示词生成为你自己的选择进行辩护的能力。请务必查看下方的节目说明，获取《Pragmatic Engineer》的相关深度分析，这些分析对技术面试相关话题有更深入的探讨。如果你喜欢这期播客，请[音乐] 务必在你喜欢的播客平台和 YouTube 上订阅。如果你还能为本节目留下评分，那就特别感谢你了。谢谢，我们下期见。

<details>
<summary>Original English</summary>

**Host**: >> I'm glad we finally got to record this episode with Neet. I love how honest he is and I hope this came across as well. I found it interesting how Neet hires these days. [music] He runs one of the biggest coding preparation sites and then he hires for skills outside of coding. He cares about motivation, whether the person can explain their own thinking, and most importantly, for agency [music] or for getting things done. It was also nice to talk with him about how he believes that companies have no idea how to evaluate candidates and they probably never did. The LeetCode style interview survived not because it predicts job performance, it just doesn't, but because nobody has found anything better that scales. And finally, [music] I appreciated Neet's observation that the effort is becoming a differentiator exactly because AI has made everything else cheap. Anyone can prompt a design, a feature, or an answer, but what you cannot prompt is caring and your ability to defend your choices when someone asks, "Why did you do it this way?" Do check out the show notes below for the related pragmatic engineer deep dives that go even deeper into tech interview related topics. If you've enjoyed this podcast, please [music] do subscribe in your favorite podcast platform and on YouTube. A special thank you if you also leave a rating on the show. Thanks and see you in the next one.

</details>