---
author: The Pragmatic Engineer
date: '2026-05-20'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=q9xD36NCtZ8
speaker: The Pragmatic Engineer
tags: []
title: Rust 的核心魅力
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
# Why Rust is different, with Alice Ryhl

**视频标题**: Why Rust is different, with Alice Ryhl
**视频链接**: [https://www.youtube.com/watch?v=q9xD36NCtZ8](https://www.youtube.com/watch?v=q9xD36NCtZ8)
**发布日期**: 2026-05-20

---

### Rust 的核心魅力

**主持人**: 对于为什么要关注 **Rust** 或者使用 Rust 进行开发，你的推介词（pitch）会是什么？

<details>
<summary>Original English</summary>
**Host**: What would your pitch be on why it's worth checking out Rust or working with Rust?
</details>

**Alice Ryhl**: 你需要一种可靠的语言，它的 **Bug** 尽可能少。这就是 Rust 的核心理念。

<details>
<summary>Original English</summary>
**Alice Ryhl**: You need a language that's reliable that's going to have as few bugs as possible. That's the idea of Rust.
</details>

**主持人**: 什么是 **所有权模型 (Ownership model)**？

<details>
<summary>Original English</summary>
**Host**: What is the ownership model?
</details>

**Alice Ryhl**: 它的核心思想是，如果你有一个包含某个对象的变量，那么该对象就只存在于那里。所以，它在某种程度上是**独占**的。

<details>
<summary>Original English</summary>
**Alice Ryhl**: The idea that if you have a variable containing some object, then the object is only there. So, it's kind of exclusive.
</details>

**主持人**: 我们谈到了**内存安全**，但 Rust 中有一个关键字叫 `unsafe`。

<details>
<summary>Original English</summary>
**Host**: We talked about memory safety, but there is a keyword in Rust called unsafe.
</details>

**Alice Ryhl**: 通常情况下，使用 `unsafe` 是为了给语言添加新特性。只要你的 **API** 设计得当，你就可以通过使用 `unsafe` 来添加新的语言特性。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Generally, when unsafe is used, it's to add a new features to the language. As long as you design your API right, you can add new language features by using unsafe.
</details>

**主持人**: 什么是 **版本 (Additions)**？

<details>
<summary>Original English</summary>
**Host**: What are additions?
</details>

**Alice Ryhl**: **Additions** 基本上是 Rust 在不破坏现有代码的情况下进行**破坏性更改 (breaking changes)** 的方式。因为他们可能会改变语言的语法。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Additions are basically the way that Rust makes breaking changes without breaking people because they might change the syntax of the language.
</details>

**主持人**: 在你为 Rust 项目做贡献的日常工作中，你会使用任何 **AI 工具** 吗？

<details>
<summary>Original English</summary>
**Host**: Do you use any of the AI tools for your day-to-day work contributing to Rust projects?
</details>

**Alice Ryhl**: 我一直在尝试使用它们。老实说，我还在学习。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So, I have been trying to use them. Honestly, I'm still learning.
</details>

---

### 访谈背景与嘉宾介绍

**主持人**: **Rust** 正悄然成为构建可靠且高性能应用程序的首选语言。但它究竟有何不同？**Alice Ryhl** 是谷歌 **Android Rust** 团队的一名软件工程师，也是 **Tokio**（Rust 事实上的异步运行时）的核心维护者，同时还是 Rust 语言团队的顾问。

在今天的对话中，我们将涵盖：为什么要考虑 Rust（无论你现在使用的是 TypeScript 还是 C++）；**所有权**、**借用检查器 (Borrow Checker)** 和 `unsafe` 关键字等概念是如何运作的；新手在学习 Rust 时通常会遇到哪些挫折；在没有“仁慈的独裁者”的情况下，这种语言是如何治理的；以及 **RFC** 和 **Additions** 是如何运作的等等。如果你想了解 Rust 的独特之处，以及为什么这么多工程师说“只要它能编译通过，就能正常运行”，那么这一集就是为你准备的。

本集由 **Antithesis** 赞助。无需人工审核或传统的集成测试即可验证系统的正确性，避免 Bug 或停机。本集还由 **Sentry** 提供。Sentry 是由开发者为开发者构建的应用程序监控软件。我第一次使用 Sentry 是在 10 年前的 Uber，当时它帮我们真实地监控服务在何时何地崩溃。我现在也使用 Sentry 来帮助我了解我为 *The Pragmatic Engineer* 构建的服务和 API 是否健康。Sentry 可以展示问题的完整上下文、堆栈跟踪、用户操作、环境详情，甚至导致问题的具体代码行。它几乎支持所有现代技术栈：TypeScript、JavaScript、Python、Go 等。它适用于后端、前端和移动端。Sentry 推出的一个新特性是 **Seer**，他们的 AI 调试助手。让我展示一下：我打开 Seer 助手，询问我的后端发生了哪些重复错误。Seer 发现一个重复问题是网络调用失败。然后我可以询问更多细节，并利用这个集成在 Sentry 中的 AI 助手更高效地进行调试。Seer 是修复那些难以调试的棘手问题的利器。请访问 `centry.io/pragmatic` 立即开始监控。

Alice，欢迎来到我们的播客。

<details>
<summary>Original English</summary>
**Host**: Rust is quietly spreading as a language of choice to build reliable and performant applications. But what makes it different? Ellis Real is a software engineer working on Google's Android Rust team, a core maintainer of Tokyo, the de facto async runtime for Rust, and is a Rust language team adviser. In today's conversation, we cover the pitch on why Rust is worth to consider whether you're using TypeScript or C++ today. how concepts like ownership, the borrow checker, and the unsafe keyword work, and what are things that trip up newcomers to Rust, how the language is governed without a benevolent dictator, and how RFC's and additions work, and many more. If you want to understand what makes Rust different and why so many engineers say once it compiles, it works, this episode is for you. This episode is presented by Antithesis. Verify your systems correctness without human review or traditional integration test and avoid bugs or outages. This episode is brought to you by Sentry. Centry is application monitoring software built by developers for developers. The first time I used Sentry was 10 years ago back at Uber where Sentry helped keep us honest on when and where our services were breaking. I also use Sentry today to help me understand if the services and APIs I built for the pragmatic engineer are healthy or not. Sentry shows you the full context on issues, stack traces, user actions, environment details, and even the exact line of code that caused the issue. It supports pretty much every modern tech stack. TypeScript, JavaScript, Python, Go, and others. It works on back and front and mobile, you name it. One new feature Sentry launch is Seir, their AI debugging agent. Let me show you. I open the Seir agent and ask about what are some repeated errors happening on my back end. Seir figures out that a repeated issue is a network call failure. I can then ask for more details and debug more efficiently with this AI agent integrated neatly in this entry. Sierra is a neat tool to fix the hard issues, the ones that are just hard to debug. Check out Sentry at centry.io/pragmatic and start monitoring today. Alice, welcome to the podcast.
</details>

**Alice Ryhl**: 谢谢你邀请我。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Thank you for having me.
</details>

---

### 从 Minecraft 到谷歌

**主持人**: 很高兴你能来。你是如何进入软件工程领域的？

<details>
<summary>Original English</summary>
**Host**: It's really nice to have you here. How did you get into software engineering?
</details>

**Alice Ryhl**: 实际上这一切都始于 **Minecraft**（我的世界）。

<details>
<summary>Original English</summary>
**Alice Ryhl**: It actually all started with Minecraft.
</details>

**主持人**: 不会吧。

<details>
<summary>Original English</summary>
**Host**: No way.
</details>

**Alice Ryhl**: 当时我想为 Minecraft 写自己的 **Mod**，所以我学习了 **Java**。虽然我在 Mod 开发上没走多远，但那是起点。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I wanted to write my own mod for Minecraft, so I learned Java. I didn't get very far with the Minecraft modding, but that's where it started.
</details>

**主持人**: 后来你是如何继续的？去读大学了吗？

<details>
<summary>Original English</summary>
**Host**: How did you continue? Did you go to university?
</details>

**Alice Ryhl**: 那是在我上高中之前。高中毕业后，我有一年的时间在全职做软件工程师。然后我开始读本科，读了 3 年，接着又读了 2 年的硕士。

<details>
<summary>Original English</summary>
**Alice Ryhl**: This was just before I started in high school. And then after high school, I had a year where I worked full-time as a software engineer. And then I moved on to starting my bachelor. Did that for 3 years and then I did a masters for 2 years.
</details>

**主持人**: 你是怎么去 **谷歌** 的？是大学毕业直接去的吗？

<details>
<summary>Original English</summary>
**Host**: How did you end up at Google? Was that straight out of university?
</details>

**Alice Ryhl**: 实际上我在读研期间就开始兼职工作，毕业后转成了全职。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Actually started part-time at the same time as when I started my masters and then I switched to full-time after I finished.
</details>

---

### 投身 Rust 社区与 Tokio

**主持人**: 你是如何参与到 Rust 社区的？是在谷歌之后还是之前？

<details>
<summary>Original English</summary>
**Host**: How did you get involved with the Rust community? Was was it at Google? Was it before Google?
</details>

**Alice Ryhl**: 哦，在那之前很久。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Oh, way before.
</details>

**主持人**: 很久之前？

<details>
<summary>Original English</summary>
**Host**: Way before.
</details>

**Alice Ryhl**: 我接触 Rust 已经很长时间了。上学时，我花了很多时间在 **Rust Users 论坛**上。其实我一直在那里回答问题，可能发过 10,000 个帖子之类的。后来我也开始在一些聊天服务器上活跃，比如 **Tokio** 的 Discord。我坚持回答问题，当我看到常见问题时，我就会去修复文档。这就是我进入 Tokio 团队的过程，现在我是其维护者之一。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I've been doing Rust for a long time. When I was in school, I spent a lot of time on the what's called the Rust users forum. Well, I was answering questions really. I have maybe 10,000 posts on there or something. At some point, I also started being active in some chat servers, the Discord server for something called Tokyo. I kept doing that, answering questions. When I saw common questions, I would uh fix the documentation. That's how I got into Tokyo, which I'm now one of the maintainers of.
</details>

**主持人**: 对于我们这些不熟悉 Rust 和 Tokio 的人来说，Tokio 在 Rust 中是什么，为什么它很重要？

<details>
<summary>Original English</summary>
**Host**: And then for those of us not as familiar with Rust and and Tokyo, uh what is Tokyo inside of Rust and why is it important?
</details>

**Alice Ryhl**: Tokio 是 Rust 的**异步运行时 (asynchronous runtime)**。你可以把它看作是使用异步编程时的 Rust 标准库。如果你拿它和浏览器中的 **JavaScript** 比较，你可以把 Tokio 类比作浏览器本身。例如，在 JavaScript 中有一个**事件循环 (event loop)**，其中包含所有可以运行的任务，它们被一个接一个地执行。特别是如果你使用 `await`，可以让任务暂停，然后在同一个线程上运行另一个任务。Tokio 做的也是类似的事情：它有一个可以运行的任务队列，然后去运行它们。但与 JavaScript 不同的是，Tokio 可以是**多线程**的，所以你可以有多个并行运行的队列。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So Tokyo is well, it's an asynchronous runtime for Rust. You can think of it as the standard library for Rust when you're using async. I mean, if you compare with something like JavaScript in the browser, you might compare Tokyo with the browser itself. For example, in JavaScript, you have this loop, this event loop which has all the tasks that are able to run and then they get executed one after the other. And especially if you use the await stuff, then you can have tasks pause and then another task start running on the same thread. And Tokyo does something similar. It has a queue of things that are able to run and then it will run them. So unlike JavaScript, Tokyo can be multi-threaded. So you can have multiple cues running in parallel.
</details>

---

### “只要能编译通过，就能正常运行”

**主持人**: 这似乎是 Rust 语言和生态系统中非常核心的部分。你是如何倾向于这个领域的？听起来你最初是在论坛上潜水，到处帮帮忙。是什么吸引你关注这个语言或生态系统的？

<details>
<summary>Original English</summary>
**Host**: This seems like a pretty core part of of Rust as a language, as a as a ecosystem. How did you gravitate towards this? Cuz it sounded like you were, if I understand, you were lurking on the Rust forums. You were helping out here and there. What drew you to this part of the language or or the e ecosystem, should I say?
</details>

**Alice Ryhl**: 我想我对 Rust 的喜爱部分源于这种感觉：当你写好代码，**只要它能编译通过，就能正常运行**。当然，这得打个引号，因为肯定还是会有 Bug，但这是很多使用 Rust 的人都会说的话。虽然这在字面上不一定完全正确，但人们这么说是有原因的。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I think part of what I liked about Rust is this feeling that as you write the code when it compiles it works. I mean this has to be in quotes right because obviously it's possible that there are bugs but this is something a lot of people say about Rust and there's a reason people say it even though it's not necessarily literally true.
</details>

**主持人**: 其他语言相比之下又是怎样的？

<details>
<summary>Original English</summary>
**Host**: How do some other languages compare to begin with?
</details>

**Alice Ryhl**: 首先，要拥有一种带给这种感觉的语言，你必须有一个**类型系统 (type system)**。这是所有一切的起点。我认为即使与其它带有类型系统的语言相比，Rust 做得也比很多语言要好。最经典的例子就是 **Java** 的 `null`。是 **Tony Hoare** 发明了 `null`，他称之为自己的“**十亿美元错误**”，因为在程序中发生崩溃太容易了——每次调用函数都可能导致崩溃。在 Rust 中，他们非常擅长确保当你调用函数时，它绝对不可能是 `null`。那个问题根本不存在，所以你不会遇到那种崩溃。你必须显式声明这个对象可能是空，然后**编译器**会强制你在使用它之前检查 `null`。你不会像在 Java 中那样遗忘。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I think to have a language that feels this way you have to have a type system. That's where it all starts. Yeah, I do think that even compared to other languages with type systems, I think Rust does a better job than many languages, even others with type systems. I mean, the the classic example is Java's null. It was Tony hair who invented uh the null and he called it his billiond dollar mistake because it's so easy to have I mean every time you call a function you might have a crash in your program and in Rust I think they're really good at making sure that when you call a function there's no chance that it might be null right that problem just doesn't exist so you can't have that kind of crash and so you have to explicitly say this object might be null and then the compiler will force you to check for null before you use it. So you can't forget like you can in Java.
</details>

---

### Rust 的普及与普及策略

**主持人**: 我们能整体聊聊 Rust 吗？这种语言创建于 20 年前的 2006 年（译注：Graydon Hoare 开始开发），感觉随着时间的推移它变得越来越流行。你知道 Rust 现在的规模吗？比如在使用量、流行度或 Rust 社区已知的相关数据方面。

<details>
<summary>Original English</summary>
**Host**: Can we talk about Rust as a whole? This was a language that was created in in 20 years ago in 2006 and it feels like it's become a lot more popular over time. Do you know of like the scale that Rust is at in terms of usage or popularity or or things that among the Rust Rust community numbers that are known there?
</details>

**Alice Ryhl**: 我发现一件挺有趣的事，我前几天查了一下，我们在 **TIOBE 指数**上已经超过了 **PHP** 和 **Go**。

<details>
<summary>Original English</summary>
**Alice Ryhl**: One thing I found kind of funny, I I checked here all the day and uh we have actually overtaken PHP and Go on the Tyobi index.
</details>

**主持人**: 哦，就是那个试图估计编程语言使用量或流行度的指数。

<details>
<summary>Original English</summary>
**Host**: Oh, this that that index tried to estimate the the usage of languages, right? Usage or popularity or something like that.
</details>

**主持人**: 哇。因为我普遍的感觉也是 Rust 正在出现在越来越多的地方。越来越多的公司在基于 Rust 构建。**Oxide** 就是一个很好的例子，他们决定全身心投入 Rust。感觉 Rust 正在成为构建高性能应用程序的流行选择，甚至越来越多地为**内核 (kernel)** 做出贡献。作为一个可能熟悉 TypeScript、Java 等语言的工程师，你会如何向别人推销 Rust，为什么值得尝试或使用 Rust？

<details>
<summary>Original English</summary>
**Host**: Wow. Cuz the feeling I have again in general is that Rust is popping up in more and more places. More companies are building on Rust. Oxide is a good example. they decided to go all in on Rust and like there's a sense of of Rust is is becoming a popular place to build I guess high performance applications even increasingly contributing to to the kernel as an engineer who you know might know other languages from like Typescript Java etc. What would your pitch be on why it's worth checking out Rust or working with Rust?
</details>

**Alice Ryhl**: 这在很大程度上取决于你来自哪种语言背景。

<details>
<summary>Original English</summary>
**Alice Ryhl**: That depends a lot on which language you're coming from.
</details>

**主持人**: 那就假设是从 **TypeScript** 转向 Rust 吧，那是目前最流行的语言之一。相比 C++，针对 TypeScript 用户的推介词肯定大不相同。

<details>
<summary>Original English</summary>
**Host**: Oh, let's come from Typescript. It's it's one of the most popular languages right now. The pit from TypeScript would be a lot different than the pit from C++. But okay, so to begin with, I think when it comes to TypeScript, Rust fits in as the backend language. That's where I would put it.
</details>

---

### 给 TypeScript 开发者的推介词

**Alice Ryhl**: 对于 TypeScript 用户，我认为 Rust 的定位是**后端语言**。我不会把它用在前端。它非常适合后端和 **API 服务器**。一种表达方式是：你不想在深夜因为 Web 服务器出问题而被叫醒。你需要一种可靠的、Bug 尽可能少的语言。当然，最好是零 Bug，但这很难做到，但我们要追求尽可能少。这就是 Rust 的理念。我之前提到了 `null`，但它还做了很多类似的事情。它有这种 **枚举 (Enum)** 类型，我觉得 TypeScript 也能做类似的事情，它在这方面做得其实挺好。

但我认为另一件非常棒的事情是**错误处理 (error handling)**。一方面，Rust 并不真正使用异常（exceptions），它实际上将错误作为**值 (value)** 返回。你会返回一个枚举值，要么是结果 (Result)，要么是错误 (Error)。处理方式是使用 `?` 运算符——你在函数调用后面写个问号，这意味着“如果这个函数失败，就返回该错误”。处理错误非常容易，而且它是显式的。另一方面，如果你忘了放问号，那就是一个**编译错误**。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I wouldn't use it in the front end. I think it's a pretty good fit for backends, API servers. One way to put it is you don't want to be waking off at night because there are problems with your web server. You need a language that's reliable, that's going to have as few bucks as possible. I mean, obviously, it would be nice if it had zero bucks, but you know, it's going to be hard to get there, but as few bucks as possible. That's the idea of Rust. I mean, I already mentioned null, but it does a lot of stuff like that. So there's no null checking and and this is done through you know it has this enum type which I mean I think Typescript can do something similar. TypeScript is actually kind of good on that front but but okay the other thing I think is quite good is uh error handling. So on one hand Russ doesn't really use exceptions. So it actually returns the error as a value. So you return a value that's either using an enum either the result or the error. And the way this is done is that there's an operator question mark which says so you write my function and then question mark at the end. And this means if this function fails return the error. So it's really easy to handle errors but it's not zero characters like like it is with exceptions right? So it's explicit on the other hand and if you forget to put the question mark that's a combination error.
</details>

**主持人**: 太棒了。

<details>
<summary>Original English</summary>
**Host**: Wonderful.
</details>

**Alice Ryhl**: 所以你必须检查它。这就是为了避免那种“你写了一些代码，却没考虑到某些隐式错误条件，结果导致服务器宕机”的情况。

另一件我非常喜欢的事情是它的**文档处理**。当你写注释时，用三个斜杠（`///`）而不是两个，它就变成了文档注释。关键在于，你可以在文档中编写代码示例，而 Rust 会将所有的示例都转化为**测试 (Tests)**。这意味着如果你修改了底层代码，你的测试就会失败。因此，你绝对不会忘记更新文档中的示例。此外，还有像“能否在 Rust 中忘记初始化变量”这样的事情。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So you have to check it. Yeah. Right. And of course you can also handle that manually. But but the point is it's this idea of there are these things where you write some code and there's some implicit error condition you didn't think of and now you just you know took down your server or something. Another thing I would I quite like is how it handles documentation. How does it for one when you have a comment you make it into a documentation comment by having three slashes instead of two. Now the thing is you can of course write examples in your documentation and Rust makes all examples into tests. This means that if you change the underlying code now your test fails. And so this means that you can't even you can't forget to update your examples in your documentation. Yeah. And I guess there's also things like you can you forget to initialize a variable in Rust?
</details>

**主持人**: 应该不行，对吧？

<details>
<summary>Original English</summary>
**Host**: I mean, no,
</details>

**Alice Ryhl**: 不允许这样做，你必须在第一次使用变量之前设置一个值。

<details>
<summary>Original English</summary>
**Alice Ryhl**: it doesn't allow you, right? The comp you have to set a value before you use it for the first time.
</details>

**主持人**: 还有检查传入 **JSON** 格式这类事情，它也会强制你去做。

<details>
<summary>Original English</summary>
**Host**: Yeah. And I guess the things with uh checking the format of incoming JSON, it also forces you to do that.
</details>

**Alice Ryhl**: 是的。Rust 中有一个非常酷的库叫 **Serde**。你先定义你的结构体（类型）和字段，然后你可以说我想能够从 JSON 解析它。Serde 是一个**宏 (Macro)**，它会生成代码来检查 JSON 格式是否匹配、是否包含所需的字段、类型是否正确。它会生成针对该特定 JSON 形状的本地代码，因此速度非常快。

这也帮你避免了错误。还有一件事我最近才通过你了解到，就是 **Switch 语句**（在 Rust 中叫 `match`）。在几乎所有语言中，你对枚举进行 Switch 操作，处理各种 Case，然后可能会有一个 `default`。有时你漏掉了一个 Case，这可能没啥，但也可能是大问题。但在 Rust 中，你也不能这样做，对吧？

<details>
<summary>Original English</summary>
**Alice Ryhl**: Yeah. So there's a pretty cool library called Surya in Rust where you you have your strct so your type you know with fields and then you can say I want to be able to pass this from for example JSON and then SA will it's a macro it will generate code which checks the JSON that it's in the same format it has all the fields you need and they have the right types and it generates native code that's specific to that particular shape of JSON. So the charge are really efficient and again yeah so it helps you avoid errors and there's this thing which again I I learned just very recently thanks to thanks to you as we're talking ahead of this is the switch statement right so in almost every language you have a you have a switch for an enum and you handle cases and then you might have a default or you know everything else and sometimes you forget one of them it's not a big deal or maybe it's a big deal but in Rust you cannot do that either right
</details>

**Alice Ryhl**: 没错。在 Rust 中它不叫 Pitch（推销），它叫 **Match**，但理念是一样的。你可以对枚举进行匹配，为每种可能性都设置一个分支。如果你漏掉了一个，那就是编译错误。当然，如果你愿意，你可以有一个捕获所有情况（catch-all）的分支。但大多数时候你会列出所有情况，这样未来当你添加新的变体时，编译器会告诉你：“嘿，你需要更新这里、这里和这里的代码。”

我认为这引出了 Rust 帮助提高可靠性的另一种方式：**重构 (Refactoring)**。Rust 非常擅长告诉你所有需要更新的地方。我有时进行重构，更改代码或返回类型，然后我只需要不断修复编译器报错，直到编译器不再抱怨为止。只要编译器通过了，我就更新了所有需要更新的地方。

<details>
<summary>Original English</summary>
**Alice Ryhl**: that's right so in rust it's not called pitch it's called match but it's the same idea you can match on your enum and then you can have a branch for each possibility at rank B and if you are missing one that's a compiler error of course you can have a catch all case if you want to but most of the time you would just list all the cases and then in the future when you add a new variant the compiler will tell you oh you need to update your code here here and here and I think this is kind of leads to another way that Rust really helps with reliability, which is that if you're refactoring, I think Rust is really good at telling you all the places you need to update. I've done this sometimes where I would refactor something. I change the code. I change the return type or whatever it is, and then I just fix the compiler errors and until the compiler stops shouting. And then once I've done that, I've updated every place I need to update.
</details>

**主持人**: 我感觉到语言设计者深入思考过其他编程语言中典型的出错方式，并试图通过编译器来修复它们。比如文档的例子，我仍然觉得很惊艳——因为这种情况总是在发生，你有个注释示例，结果它和代码不同步了，大家总在抱怨却不知道怎么修。我抱怨这种事都超过十年了，而 Rust 是我听到的第一个真正给出解决方案的语言，尽管它可能并不完美。这种模式随处可见，如果你弄糟了，要么编译不通过，要么至少会有个 **Lint** 检查出来。他们就在编译时捕捉了大量的错误。

刚才我们聊了针对 TypeScript 或类似语言用户的推介。那么针对 **C++** 用户的推介呢？

<details>
<summary>Original English</summary>
**Host**: I I get a sense that the language designers have thought really hard of what are ways that typically go wrong in a lot of other programming languages and they just try to fix it through the compiler. Like the documentation example is is the one where I'm still like wow like it happens all the time like you you have a comment example or not and then it gets out of sync and we always complain about this and we don't know how to fix it. I think we've been I I know I've been complaining or like for you know like a decade plus this dross is the first language where I hear a like an actual solution even if it's not a perfect one and I really think this pattern just every where you look you have this kind of thing again and again that oh if you messed up they you know either it won't compile or at the very least there's a lint for it they just catch a lot of cases at compile Now, we've had the pitch from Typescript or similar languages. What about the pitch from C++?
</details>

---

### 给 C++ 开发者的推介词：内存安全

**Alice Ryhl**: 在这种情况下，我认为推介词甚至更强有力。在 JavaScript 中，如果你犯了错，也许只是让服务器宕机，这已经够糟了；但在 C++ 中，如果你犯了错，通常会演变成一个**安全漏洞 (security vulnerability)**。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So, here I actually think it's even stronger. The thing with C++ is that if you make a mistake, right, in in JavaScript, maybe you take down your server, which is already bad enough, but in C++ when you make a mistake there, now it's actually a security vulnerability most of the time.
</details>

**主持人**: 嗯。即使是像数组索引越位这种微小的错误，也会变成安全漏洞，而且这种情况屡见不鲜。

<details>
<summary>Original English</summary>
**Host**: Mhm. If you do something as trivial as you did an off by one in your IRA or whatever it might be, that's a security vulnerability and that this just keeps happening.
</details>

**Alice Ryhl**: 小错误会变成安全漏洞。而 Rust 是**内存安全 (memory safe)** 的。我们刚才谈论了各种提高可靠性的方式，甚至还没触及内存安全。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Small mistakes become security vulnerabilities. And in Rust, so Rust is memory safe, right? I mean, we talked a bunch about different ways that Rust is more reliable. And we didn't even touch memory safety.
</details>

**主持人**: 让我们聊聊内存安全。

<details>
<summary>Original English</summary>
**Host**: Let's talk about memory safety.
</details>

**Alice Ryhl**: 内存安全的核心思想是：无论你写的代码多么愚蠢，它都不会出现某一特定类别的 Bug。这种 Bug 通常会导致安全漏洞，比如读取数组越界而查看到随机内存，或者销毁了一个对象后又继续使用它，从而触碰到了另一个随机对象的内存。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Memory safety is this idea that no matter how stupid the code you write is, it's not going to have a certain class of bugs. And this is the, you know, the kind of bug that usually leads into security vulnerabilities. You know, the kind of thing where you read past the array and you just look at random memory or you destroyed an object and then you used it afterwards. So now you actually touched the memory of some other random object.
</details>

**主持人**: 是的。如果攻击者发现了这一点，他们就可以在那里填充某些内容，最终让代码执行某些操作，或者读取配置。内核中一个经典的例子是：假设你有一个对象，你设法让该内存被重复使用（因为原始对象已消失），现在那里存放的是一个叫 `task_struct` 的东西，它基本上代表了你的进程，其中有一个字段叫 **User ID**。代码向内存写零是很常见的，但如果你向 User ID 字段写了个零……

<details>
<summary>Original English</summary>
**Host**: Yep. And then attacker who figures this out could populate something there eventually get that code somehow executed or configuration read and then boom like the classic example in the kernel is let's say you have some object and you manage to make it so that the object that's actually there right because the original object is gone so the memory got reused and now it has a task strct it's called and that's basically your process and it has a field called user ID. And it's pretty common for code to write zero zeros to memory. But if you write a zero to the user ID,
</details>

**Alice Ryhl**: 那你就变成了 **Root**（超级用户）。

<details>
<summary>Original English</summary>
**Alice Ryhl**: now you're root.
</details>

**主持人**: 那就是 Root 用户了。

<details>
<summary>Original English</summary>
**Host**: That's a root user.
</details>

**Alice Ryhl**: 是的，那是利用这类漏洞的一种非常经典的方式。一旦攻击者成功做到这一点，他们就能接管你的服务器或正在运行的任何程序。从那以后，情况就会失控。一旦你拿到了 Root 权限，一切都完了。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Yeah, that that's a really classic way of exploiting this kind of vulnerability. And then once an attacker manages to do that, they can take over the whatever your server or whatever is running. And then of course from there on it can just spiral out of control, right? Once you're rooe, you're lost.
</details>

**主持人**: 所以我理解，Rust 的一个非常强大的推介点（特别是对于来自 C++ 的人）是内存安全。它消除了这一整类 Bug，而这些 Bug 可能会演变成安全漏洞，这是任何软件面临的最严重威胁之一。

<details>
<summary>Original English</summary>
**Host**: Yeah. Do I understand that a very strong pitch of rust, especially coming from C++, is memory safety eliminates this whole class of bugs, which which are which can turn into security vulnerabilities, which are one of the most serious threats any any software can have.
</details>

**Alice Ryhl**: 此外还有我在开头提到的所有可靠性优势。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Lost all of the reliability ones I mentioned in the beginning.
</details>

---

### 关于可靠性与赞助商

**主持人**: 这是一个非常好的推介。我们刚才谈到了 Rust 如何提供多种安全特性，如内存安全、错误处理和类型系统。这是因为可靠性不是单一因素决定的，而是由多个方面共同构成的。这里我需要提一下我们的赞助商 **Antithesis**。就像 Rust 的设计者一样，Antithesis 也相信提高可靠性没有“银弹”。你需要许多不同的工具和方法。这就是为什么他们发布了 **Hegel Rust**，这是一个免费开源的、基于属性的 Rust 测试库，由 **Hypothesis** 团队构建。Rust 编译器在编译时捕获各类 Bug 的能力非常出色，但在边缘情况、诡异的输入组合或最终无法成立的假设面前，运行时 Bug 需要不同的工具。Hegel 为快速本地开发提供了强大且符合人体工程学的基于属性的测试。它会检查你从未想到的边缘情况，并在这些未知数拖垮生产环境之前捕捉它们。如果你尝试并喜欢 Hegel，你的 Hegel 测试可以原封不动地在 Antithesis 上运行，这样你就能轻松为你的可靠性武器库增加决定性因素和世界上最彻底的运行时验证。请访问 `hegel.dev` 了解更多信息。

我还想提到今年的两场会议，我将在会上发言，我们可以在那里见面。6 月 4 日，我将在匈牙利布达佩斯的 **Craft Conference** 做主题演讲。这是欧洲最好的关注软件工艺的会议之一，我是那里的老面孔。更多详情请访问 `craft--comf.com`。此外，9 月 15 日和 16 日，我将在纽约的 **LDX3** 做主题演讲。这是现代工程领导力的盛会。去年我在伦敦参加了 LDX3，这次很高兴能回到纽约。关于该会议的更多详情，请访问 `leadub.com`。如果你在其中任何一场会议现场，我们到时见。

现在，让我们回到 Rust，回到 Alice 这里。我想问为什么 Rust 变得如此流行，但我想我们已经开始回答这个问题了，对吧？

<details>
<summary>Original English</summary>
**Host**: That that is a pretty good pitch. We just talked about how Rust offers several safety features like memory safety, error handling, and a type system. This is because reliable is not about one thing but several things at once. This is where I need to mention our presenting sponsor antithesis. Like the designers of Rust, antithesis also believes there's no one silver bullets for reliability. You need many different tools and approaches. This is why they've released Hegel Rust, a free open- source property based testing library for Rust built by the team behind Hypothesis. Rust compiler is brilliant at catching whole categories of bugs at compile time, but at the edge cases, the weird input combinations, the assumptions that turn out not to hold, those runtime bugs need a different tool. Hegel provides powerful ergonomic property based testing for fast local development. It'll check edge cases you never thought of and catch unknown unknowns before they bring down production. And if you try Hegel and like it, your Hegel test will run an antithesis as written, so you can easily add determinism and the world's most thorough runtime verification to your reliability arsenal. Go to hegel.dev to learn more. I'd also like to mention two conferences this year where I'll be talking and where we can also meet. On the 4th of June, I'll be doing a keynote at craft conference in Budapest, Hungary. This conference is one of the very best ones in Europe focused on software craftsmanship and one where I'm a returning speaker. For more details, check out craft--comf.com. And on the 15th and 16th of September, I'll be doing a keynote at ldx3 in New York. This is the festival for modern engineering leadership. Last year, I was at LDX3 in London. And so, I'm excited to be back this time in New York. For more details about this conference, head to leadub.com. If you'll be at either of them, I'll see you there. And with this, let's get back to Rust and to Alice. I wanted to ask why Rust is getting so popular, but I think we're starting to answer this question, right?
</details>

---

### 垃圾回收 vs. 确定性清理

**Alice Ryhl**: 我认为 Rust 的独特之处在于多种特性的结合。一方面，它没有**垃圾回收器 (Garbage Collector)**，因此它可以用于 Linux 内核或固件等低级上下文。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I think where Rust is really unique is in the combination of things. So on one hand, it it doesn't have a garbage collector and it it's usable in low-level context like the Linux kernel or firmware or whatever.
</details>

**主持人**: 拥有垃圾回收器是好事还是坏事？Java 有垃圾回收器，C# 也有。

<details>
<summary>Original English</summary>
**Host**: Why is it a good or a bad thing to have a garbage collector? Java has a garbage collector. C# has a garbage collector.
</details>

**Alice Ryhl**: 垃圾回收器意味着当你使用完对象后，会有一小段代码检查你所有的对象，确定哪个不再被使用了，然后清理它。而在像 Rust 或 C++ 这样的语言中，变量在作用域结束时就被清理了。在另一种语言中，它们必须在事后检测。这种每隔一段时间运行一次、检查所有对象的代码，对于**嵌入式 (embedded)** 用例来说，可能根本无法实现或不可接受。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So, a garbage collector says once you've done using your objects, there's going to be a little piece of code that checks all of your co your objects and says this is not used anymore and then it cleans it up. Whereas in languages like Rust or C++, the variable is cleaned up at the end of the scope when it goes out of scope. And in the other one, they have to detect afterwards. And this kind of little piece of code that runs every so often to check all your objects. For embedded use cases, this might simply be not possible or unacceptable.
</details>

**主持人**: 是因为性能开销，以及你无法像那样精准控制内存。

<details>
<summary>Original English</summary>
**Host**: The the performance overhead the the fact that you cannot you will not be able to control the memory as much.
</details>

**Alice Ryhl**: 即使对于后端，它也可能是一个问题。因为如果一个请求恰好在它检查所有对象时进来，你就会遇到**延迟尖峰 (latency spike)**，响应时间会变得长得多。所以这是它在后端也很有帮助的原因之一。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Even for back end, it can be a problem because if you have a request incoming right when it checks all of your objects like you have some sort of latency spike where you it takes much longer to to reply. So that's one of the reasons it can be helpful in in back end as well.
</details>

---

### 学习曲线与数据结构设计

**主持人**: 对于还未见过 Rust 代码的人，你会如何描述它？它和 TypeScript 相比如何？

<details>
<summary>Original English</summary>
**Host**: For someone who has not yet seen Rust code, how would you describe it? how it compares to for example TypeScript.
</details>

**Alice Ryhl**: 在很多情况下，Rust 代码与许多其他语言相似。它使用花括号，不像 Python 那样使用缩进。它有分号等等。所以即使你不懂 Rust，如果你了解一些类似的语言，你也能看懂大概意思。我想你能搞明白，它并不那么陌生。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I mean in many cases Rust code is similar to many of the other languages. It has braces. It's not like Python where you know you use indentation. It has braces. It has semicolons and so on. So so it's pretty easy to read even if you don't if if if you know some similar languages you can look at it and you can get a rough idea. Yeah, I think I think you'll figure it out. It's not that it's not that foreign.
</details>

**主持人**: Rust 的学习曲线在较难学习的语言之列。你认为新手通常会纠结于什么？是什么让他们恍然大悟？

<details>
<summary>Original English</summary>
**Host**: Rust has a a learning curve on the side of the more difficult languages to learn. What do you see devs typically struggle with who are new to Rust and and what are the things that just makes it click for them?
</details>

**Alice Ryhl**: 我认为人们遇到的最棘手的事情是：如何构建你的**数据结构**？对于代码逻辑，你大多可以做和其他语言一样的事情。但重头戏确实是数据结构。

举个例子，假设你有一个“书 (Book)”对象，它有一个“页面 (Pages)”数组，每个页面也是一个对象。如果我用 TypeScript 写，我可能会在页面中放一个引用指向书，而书当然也引用了页面，对吧？所以它是**循环引用 (cyclic)** 的：书指向页面，页面指回书。但在 Rust 中，你通常必须设计你的对象使其不是循环的。它必须是一棵**树 (Tree)**，或者是一个 **DAG**（有向无环图）。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I think the most tricky thing people run into is how should you put together your data structures? I mean for your code you can mostly do the same things as you can in other languages. I mean that's not entirely true but the big thing is really the data structures. So if you have I don't know what would be a good example let's say some sort okay let's just say you have a object for a book and it has an array of pages and then you have an object for each page if I was writing typescript I would probably have a book field in the page that references the book and then the book of course also references the page right so it's cyclic so the book goes to the page goes back to the book and in Rust you usually have to design your objects so that they're not cyclic. It has to be a tree or a deck if you know what that mean.
</details>

**主持人**: 是的，有向无环图。

<details>
<summary>Original English</summary>
**Host**: Yeah. Yeah. The di as graph.
</details>

**Alice Ryhl**: 如果你非要使用**引用计数 (reference counting)**，构建循环对象也是可能的，但正如你提到的，会涉及到一些“垃圾”。人们在学习这门语言时，往往尝试在不使用这类工具的情况下创建循环对象。结果就是行不通，他们在构造对象时会遇到各种问题。他们可能会得到编译器错误，然后尝试更改代码，结果又得到另一个错误。很多人纠结的地方在于，他们一直试图更改代码逻辑，而真正的解决方案是**更改结构定义 (struct)**。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So if you go out and actually start to use reference counting, it becomes possible to have cyclic objects with some cabbage like you mentioned. But what people end up doing when they're langu learning the language is that they try to make cyclic objects without anything like that. and then it just doesn't work and they're going to run into all sorts of problems in their code while they're constructing. They're maybe creating their thing and then they get a compiler error and then they try to change the code and they get a compiler error again. But the the thing that a lot of people struggle with is that they keep trying to change the code when the solution is to change the strct.
</details>

**主持人**: 我能想象那有多让人沮丧。

<details>
<summary>Original English</summary>
**Host**: I can see how that's uh frustrating.
</details>

---

### 所有权与引用计数

**主持人**: Rust 还有另一个模型，对于来自其他语言的人来说可能很陌生，那就是 **所有权模型 (Ownership model)**。所有权模型是什么？

<details>
<summary>Original English</summary>
**Host**: Rust has another model that might be new for especially for for people coming from language types is Rust's ownership model. What what is the ownership model?
</details>

**Alice Ryhl**: 所有权的核心思想是：如果你有一个包含某个对象的变量，那么该对象就只存在于那里。它具有某种独占性。

例如，如果你有一个变量 `let A = your_string`，然后执行 `let B = A`，这就是一次 **移动 (Move)**。这意味着之后再使用 `A` 就会产生编译错误，因为它的内容已经移动走了。当我们没有垃圾回收器时，这一点非常重要，因为当 `B` 超出作用域时，它必须清理字符串。如果 `A` 仍然有效，那么当它们两个都超出作用域时，它就会清理字符串两次，这是不合法的。在大多数其他语言中，垃圾回收器负责处理这个问题：A 和 B 超出作用域时什么都不做，稍后由 GC 清理。但在 Rust 中，我们必须在超出作用域时执行清理。所有权模型允许你将值从 A 移动到 B，然后 A 变得非活动或不可用，不会被清理，因为它已经没有值可以清理了。

<details>
<summary>Original English</summary>
**Alice Ryhl**: The ownership is just the idea that if you have a variable containing some object then the object is only there. It's kind of exclusive. So for example, if you have a variable let A equals your string or whatever and then you do let B equal to A, then this is a move. And so this means that using A afterwards is now a compiler error because its contents have been moved away. And of course this is important when we don't have a garbage collector because then when B goes out of scope, it has to clean up the string. Now if A was also valid then when they both went out of scope it would clean up the string twice which is not legal. In most other languages the garbage collector takes care of this. A and B just go out of scope do nothing and then later it cleans up the string. But here we actually have to do it when we go out of scope. And the ownership model allows you to move from A to B and then A becomes inactive or unusable and does not get cleaned up because it doesn't have a value to clean up anymore.
</details>

**主持人**: 那么引用计数与这一切有什么关系？

<details>
<summary>Original English</summary>
**Host**: And how does reference counting relate to all all of this?
</details>

**Alice Ryhl**: 在 Rust 中，我们有一堆不同的类型，本质上是不同种类的指针。其中一种指针叫 **`Arc`**，它是**引用计数器 (reference counter)**。核心思想是：你有一个对象，然后你有一个指向它的 `Arc` 指针。你可以对 `Arc` 调用 `clone`，这会增加计数器，现在你就有了两个指向同一块底层内存的 `Arc`。即使对象非常大，这两个 `Arc` 也是共享同一块内存的。当它们超出作用域时，计数器就会递减；当计数器归零时，对象被清理。这是一种表达“这个对象实际上需要在多个地方存在，没有单一所有者”的方式。你可以通过计数器知道有多少个所有者。当最后一个所有者离开时，它就被清理了。

<details>
<summary>Original English</summary>
**Alice Ryhl**: In Rust, we have a bunch of different types which are essentially different kind of pointers. And one of the pointers is it's called arc. It's and it's reference counter. And so the idea is you have some object somewhere and then you have an arc to the object and what you can do is you can call clone on the arc and this increments a counter and now you have two arcs to the same underlying memory. So the object might be really big but you have two arcs that share the same memory and when they go out of scope the counter is just decremented and when the counter reaches zero the object is cleaned up. So this is a way of saying this object actually needs to be in multiple places. There's no one place that owns it. And so this way you can use a counter to know how many owners are there. And then when the last owner goes away, it gets cleaned up.
</details>

---

### 借用检查器与“对抗”

**主持人**: Rust 还有另一件对我来说很新鲜的事，就是 **借用检查器 (Borrow Checker)**。

<details>
<summary>Original English</summary>
**Host**: And on Rust also is another thing that was new to me, the borrow checker.
</details>

**Alice Ryhl**: Rust 中的另一种指针类型叫 **引用 (Reference)**。引用基本上就是一个指向对象的指针，仅此而已。我们在运行时不做任何检查。当然，这意味着在编译时，我们必须确保引用的最后一次使用必须在对象超出作用域之前。创建一个引用的过程叫作**借用 (Borrowing)**。所有者拥有值，而现在我们对该值进行了借用。借用检查器会检查引用的最后一次使用是否早于对象失效。

比如，你有一个不可变引用正在读取一个 **Vector**（向量）的第 5 个元素，然后你修改了 Vector（例如调用了 `clear` 清空它）。借用检查器会确保你之后不能再使用指向第 5 个元素的引用。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So another pointer type we have in Rust is called the reference. And a reference is basically all it is is that it it's a pointer to the object and that's it. So we do no checking at runtime. So of course this means at compile time we have to make sure that the last use of the reference has to be before the object goes out of scope. And creating a reference is called borrowing. Right? The owner owns the value. And now we have a borrow of the value. the the reference and the borrow checkout checks that the reference is like the last use of the reference is before the object goes out of scope. So if you have say a let's say you have an immutable reference you're reading then if you change the object let's say it's in vector. So I have a mut an immutable reference I'm reading element five and then I change the vector I call clear. Then the borrow checker also ensures that you can't use the reference to object five afterwards.
</details>

**主持人**: 是的，因为一旦你改变了它，它就失效了。

<details>
<summary>Original English</summary>
**Host**: Yes. Because now it has been as soon as you change it it it went out of scope. It's it's now cleared.
</details>

**Alice Ryhl**: 没错。它的工作原理是：如果有可变借用，它会确保该可变借用与之前的借用互不重叠。所以你在同一时间只能有一个写者，或者任意数量的读者。它会在函数内部的作用域中检查这一点。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Right. Yeah, the the the way it works is that if there are mutable borrows, it ensures that the mutable borrow uh ends or starts before or after the previous borrows have ended basically. So they don't overlap. So you can only have one writer at a time or you can have any number of readers. It checks that on the scope like in a function.
</details>

**主持人**: 这个概念对我这个没用过 Rust 的人来说确实很新鲜，非常有趣。我读过一些论坛上的抱怨，说是在“**对抗借用检查器 (fighting the borrow checker)**”。什么情况会让它变得具有挑战性？

<details>
<summary>Original English</summary>
**Host**: This concept is is is new to me as someone who's not used ROS for sure. It's very interesting. One thing I've read is on forums people complaining about fighting so-called fighting the borrow checker. What can make it challenging?
</details>

**Alice Ryhl**: 当你写出的代码以不符合上述规则的方式使用对象时，就会产生编译错误。所谓的“对抗”就是当你无法摆脱那些编译错误。我认为很多时候这与**结构体设计**有关。我常见的一个错误是：如果你在一个结构体中放了一个引用，Rust 会假设它可以仅通过查看单个函数来检查该引用的作用域。但如果你将这个结构体跨函数传递，这种分析可能就无法进行了，于是你就会得到编译错误。在这种情况下，解决方案可能是使用不同的指针类型。例如，引用计数指针类型通常能解决这类 Bug。所以解决方案又是——**更改数据结构**。

<details>
<summary>Original English</summary>
**Alice Ryhl**: When you write a some code that uses the object in a way that doesn't follow the rules I mentioned, that's a compiler error. And fighting the borrow checker is when you, you know, can't get out of those compiler errors. I guess I think a lot of the time this has to do with the strruct. One common mistake I see is that if you have a strct with a reference in it, Rust kind of assumes that it can check the scope of that reference like by just looking at a single function. But if you have your strct and you're passing it over functions that it might not be possible to make that analysis and so you just get a compiler error. And so in this case the solution is maybe to use a different pointer type. For example, the reference counterp pointer type often solves this kind of bug, right? So the solution is again to change the data structure.
</details>

**主持人**: 是的，我开始理解为什么你提到数据结构是从其他语言转来时的学习重点。很多时候，解决方案似乎只是重新思考你的数据结构，理解它们并以“Rust 的方式”来处理。

<details>
<summary>Original English</summary>
**Host**: Yeah, I'm I'm starting to understand why you mentioned that data structures were a a a place of learning coming from other languages. Often times the solution seems to be just think about your data structures, understand them and do it in in the Rust way, right?
</details>

---

### Unsafe Rust：逃生舱口

**主持人**: 我们谈到了内存安全，但在 Rust 中有一个关键字叫 `unsafe`。它是做什么用的？通常在什么情况下使用？它为什么存在？这只是我作为一个外行问的幼稚问题。

<details>
<summary>Original English</summary>
**Host**: We talked about memory safety, but there is a keyword in in Rust called unsafe. What does this do and in what cases do people typically use? When does it make sense to to to use and why does it even exist? That's just a naive question from me.
</details>

**Alice Ryhl**: 让我先从“是什么”开始，然后再说“为什么”。`unsafe` 本质上是一个**逃生舱口 (escape hatch)**。我之前解释过，Rust 确保只要你不使用 `unsafe`，无论你的代码多笨，都不会出现某些特定类别的 Bug（通常是安全漏洞）。如果你使用了 `unsafe`，虽然仍有一些保证，但会稍弱一些，因为每种 `unsafe` 操作都有对应的规则。如果你违反了这些规则，就可能导致严重的 Bug。但如果你遵守规则，那是没问题的。

有趣的是，`unsafe` 并不禁用借用检查器之类的东西。它只是给了你一些通常情况下不安全的操作权限。所以你必须自己检查：在这种特定情况下，这样做是否真的没问题。

再拿 Vector 的例子来说。通常当你访问索引 5 时，它会检查长度。如果长度至少是 6，那就没问题；否则程序就会崩溃。但如果你在编写超高性能的代码，想要避免每次循环中的这种检查，`unsafe` 就可以绕过这些检查。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So let let me begin with the what and let's take the why afterwards. So the what is unsafe is the escape hatch essentially. So I explained before how there are certain bugs where if your program has one of those bugs that's usually a security vulnerability. What Rust ensures is that if you have no use of unsafe, then no matter how stupid your code is, you will never have one of those bugs. Now, if you do use unsafe, then there are still some guarantees, but it's a bit weaker because each unsafe operation that you can perform has a list of rules. And if you violate these rules, then you might end up with one of these bad bugs. But of course, if you don't, then you it's okay. And it's interesting to point out here that unsafe does not disable the borrow checker or anything like that. It just gives you a few more operations you can perform that are not safe in general. And so you have to check yourself. Yeah, this is actually okay in this particular case to I mean let's take the vector example again. Normally when you index index five it will say oh let me check the length. So if the length is at least six then it's okay otherwise you get a crash but maybe you're writing some super high performance code and you want to avoid this if you want to avoid this check or if you're in a loop every time. So so un unsafe will just avoid checks.
</details>

**主持人**: 这种绕过是针对运行时还是编译时的检查，还是两者都有？

<details>
<summary>Original English</summary>
**Host**: uh may may that be is it runtime or compile time checks or both?
</details>

**Alice Ryhl**: 这么说吧，Vector 有两种获取值的方式。一种是普通的方括号运算符，它会进行检查，如果你弄错了就会让程序崩溃。另一种函数叫 `get_unchecked`。如果你写 `vec.get_unchecked(5)`，它会直接给你第 5 个元素而不检查长度。这个函数的签名被标记为 `unsafe fn`。你只能从 `unsafe` 代码块中调用这个函数。所以 `unsafe` 代码块所做的，就是允许你调用那些被标记为 `unsafe` 的函数。

<details>
<summary>Original English</summary>
**Alice Ryhl**: What I would say here is that vector has two different ways of getting a value. There's the you know normal bracket operator we'll use for other languages which will do the check and crash your program if you get it wrong. But there's another function called get unchecked. And so if you do write veget get unchecked five then it will give you element five without checking the length. And this function like in the function signature it says unsafe fn. That's the function signature. And so you can only call this function from an unsafe block. And so all that the unsafe block let you do is call functions marked unsafe.
</details>

**主持人**: 在实践中，`unsafe` 的合理用例通常与高性能代码有关吗？或者你见过哪些“合法”的优秀用例？

<details>
<summary>Original English</summary>
**Host**: Got it. And then in practice for sensible use cases of unsafe is it usually to do with high performance code typically or have you se like what what cases have you seen which are like legitimate? This is a great use case for for unsafe.
</details>

**Alice Ryhl**: 通常它不会出现在后端服务器代码中。在那里你应该零使用 `unsafe`。一般来说，`unsafe` 是用来为语言添加新特性的。

假设语言本身没有 Vector。语言仍会有分配内存、释放内存、读取某个指针地址的函数。那么你可以写一个 `struct Vec`，包含一个原始指针（使用它是 `unsafe` 的）、长度和容量。通过字段私有化和良好的 API 设计，你可以为语言添加一个 Vector（如果它还不存在）。如果 `unsafe` 被妥善封装在这种不允许出错的 API 内部，那么你就可以在安全代码中使用一个安全的 Vector，无论你在外部对该 Vector 做出多么愚蠢的操作，都不会导致严重的系统破坏，最多只是让程序按预期逻辑（正确检查长度后）崩溃。只要你设计得当，你就可以利用 `unsafe` 添加新的语言特性。另一个经典的例子是调用 **C 语言库**。你可以编写一个调用 C 的库，甚至提供一个安全的 API，并强制要求只能以正确的方式调用 C API。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So usually it will never show up in say a backend server. You would have zero uses of unsafe there. Generally when unsafe is used, it's to add a new feature to the language. Let's say the language didn't have a vector. The language still has a function to allocate memory, a function to free memory, a function to read at this pointer address. Then you could write strct ve the pointer is here and this is a raw pointer so it's unsafe to use. The length is this. The capacity is this. So I might and then you can write your little API. Of course the fields are private so you can't access them from outside the module. I mean if I could do ve.length equal 20 just access the field that would be pretty bad. And so you can write your own vector API and using field privacy and good API design, you can add a vector to the language if it doesn't already exist. and unsafe if encapsulated properly in this kind of API that doesn't permit you to mess it up. Then you can have a safe vector that you can use from safe code and no matter how stupid the thing you do with that vector is it's not going to do something bad. It's just going to crash or whatever check the length properly. As long as you design your API right, you can add new language features by using unsafe. The other classic example would be to call into a C library. You can write a library that calls into C and you can even have an safe API and then you can enforce that you only call the C API in the right way.
</details>

---

### Rust 生态系统：Crates 与 Cargo

**主持人**: 我们聊聊 Rust 生态系统吧。大家首先会接触到的通常是 **Crate** 生态。Rust 的包管理器是什么？Crate 是什么，它和 **npm** (Node) 或 **pip** (Python) 相比如何？

<details>
<summary>Original English</summary>
**Host**: Can we talk about the the Rust ecosystem, the broader ecosystem and when it comes to this the first thing that people come across include myself is the crate uh ecosystem. Rust is package man manager. What is crate and h how does it compare to other package managers in like places like npm or or pip and in python?
</details>

**Alice Ryhl**: **Crate** 只是 Rust 对“包 (package)”的称呼。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So create is just the Rust word for a package. So it's just a package right of of your code.
</details>

**Alice Ryhl**: Rust 有一个工具叫 **Cargo**，它非常强大，是一个全能型的工具。你可以用它运行代码（`cargo run`），它会自动编译代码。你有一个叫 `Cargo.toml` 的文件来指定依赖项和其他元信息。当你运行 `cargo run` 时，它会从名为 **Registry** 的注册表下载依赖。

此外，你还可以运行 `cargo test` 执行测试，`cargo doc` 生成文档（`cargo test` 也会运行文档测试），甚至还有基准测试和示例。所以它提供了全套工具，你不需要不同的工具来获取依赖、运行代码和生成文档。与 `pip` 最大的区别在于，它是**本地化**的。使用 `pip` 你可能需要全局安装或使用虚拟环境，而使用 Cargo，一切都是项目本地的。唯一共享的是 Registry，那只是为了避免重复下载相同的包。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So the way it works is that Rust has a tool called cargo and cargo is kind of um it does a lot of stuff. It's it's actually pretty neat tool that's kind of all in one. So it will do it's both what you use to run your code. You do cargo run and it will compile your code. You have this thing called cargo tunnel where you specify your dependencies and other information about your crate. And when you do cargo run, it will download the dependencies to something called a registry, which is basically just a directory with all the crates you've ever downloaded. And you can also do cargo test. It will run all your tests. Cargo doc, it will generate your doc. Cargo test will also run your doc tests. There's even benchmarks and examples. So, so it's it it it does all the whole suite, so to say. So you don't need different tools to fetch dependencies and run your code and generate docs. I think the biggest difference from something like pip would be that they're not installed to your machine, right? With pip you either install things globally or you have these virtual environments. So so with cargo it's all local. You just run cargo run and it's only local to this. The only thing that's shared is this registry which is just to avoid downloading the same thing twice.
</details>

**主持人**: 你曾跟我讲过一个关于 **Linus Torvalds** 对 Rust 和 Cargo 反应的趣事。

<details>
<summary>Original English</summary>
**Host**: You told me a funny anecdote about Linux tour worlds and his his reaction or what he told you about Rust and car and cargo
</details>

**Alice Ryhl**: 我第一次参加 **Linux Plumbers Conference** 时，Linus 直到最后才露面。在最后的社交活动上，我过去打了个招呼，提到我在做 Rust 方面的工作。他立刻就开始跟我说他不喜欢 Cargo，原因是 Cargo 会像其他包管理器一样从互联网下载代码并运行。他不希望他电脑上的任何代码这样做（除了发行版的包管理器），他不信任任何其他人。

<details>
<summary>Original English</summary>
**Alice Ryhl**: the first time I was at the Linux plumbers conference at the very end. So Linux wasn't anywhere to to be seen throughout the entire conference but the at the very end of the social event he showed up and I went over to say hi. I mentioned I worked on Rust and immediately he started telling me about how he didn't like cargo and so the reason for that is that cargo downloads code from the internet and runs it like any package manager. And he doesn't want any any code on his computer to do that other than his uh distributions package manager. He doesn't trust anybody else to do that.
</details>

**主持人**: 在 Node 领域，我们看到包中被注入漏洞的问题越来越多——坏人接管了包，放入加密货币挖矿代码或安全漏洞。Cargo 也有这类互联网包管理器的共性问题吗？

<details>
<summary>Original English</summary>
**Host**: In the node world, we're seeing more problems with vulnerabilities being injected into packages. Um, just a bad actor overtaking packages, you know, that they they put in whatever code might be from crypto, which is I guess the better part to security vulnerabilities. Does Cargo have this problem as well? Just like any package manager that is on the internet?
</details>

**Alice Ryhl**: 原理上是有的。如果你拿到了我上传新版本 Tokio 的密钥，你就能上传恶意版本。我觉得相比 **npm**，我们在这方面遇到的问题不算多，但我也不知道为什么。这是一个难题，对吧？如果有人能冒充库的维护者，那确实很糟。不过，他们确实会做一些清理恶意 Crate 之类的工作。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I mean, in principle, yeah. I mean, ultimately, if you somehow got a hold of, you know, my keys to upload new Tokyo versions, you could upload a malicious one. I don't think we've had much problems with it compared to something like npm, but I don't really know if we I mean, it's a hard problem, right? It's a hard problem. somebody can impersonate the maintainer of a library then I mean I think they do do stuff like delete uh people scratting malicious crates and stuff like that.
</details>

---

### 生态成熟度与治理模式

**主持人**: 你认为 Rust 生态系统目前在哪里最成熟，在哪里最不成熟？

<details>
<summary>Original English</summary>
**Host**: Yeah. Where where do you see the Rust ecosystem being the most mature and the less m and the least mature right now?
</details>

**Alice Ryhl**: 我认为最不成熟的领域是**前端**。虽然有一些尝试将 Rust 编译为 **Web Assembly** 并在 Web 前端运行以替代 TypeScript，但如果我要写 Web 服务器，我绝对会后端用 Rust，前端用 TypeScript。我不会真的去走 WASM 路线。

另一方面，它非常适合后端、命令行工具。现在我们也正在扩展到 Linux 和许多嵌入式项目。甚至一些 C 语言代码库也开始说：“嘿，既然 Rust 已经进入 Linux 了，也许我们也该开始用了，我们也该拥有一种内存安全的语言。”我知道 **Git**、**CPython** 都在讨论这件事，可能还有 **QEMU** 等。

<details>
<summary>Original English</summary>
**Alice Ryhl**: My opinion is that the least mature area is front end. There have been some attempts to compile Rust to Web Assembly and then run it on the web as a front end as a replacement for TypeScript. But if I was writing a web server, I would totally use Rust for the back end and TypeScript for the front end. I would not really go the web assembly route. On the other hand, for for back end, I actually think it's a pretty great fit. And there's also stuff like command line tools. I think it's really really great fit for that. And then of course we have we are expanding into Linux and we are also expanding into a lot of embedded projects and there are even projects that are like C code bases that are starting to say hey it's went into Linux maybe we should start using it too. Maybe we should have a memory sake language too. I know that git is talking about it. I know that CPython is talking about it. There are probably others. Qo maybe.
</details>

**主持人**: 我们能聊聊这种语言是如何构建的吗？谁在构建 Rust？流程是怎样的？与 Linux 这样的大型开源项目相比如何？

<details>
<summary>Original English</summary>
**Host**: Can we talk about how the language is is built? Who builds Rust? What the process for for for doing it? How does it compare to a project like Linux? I know it's not a language, but but it's still a large open source project.
</details>

**Alice Ryhl**: 它确实是一个彻底的开源项目。你可能知道它最初起源于 **Mozilla**，但现在它已经完全不再是 Mozilla 的项目了。今天，Rust 项目由许多不同的团队组成：有处理语言本身的语言团队，有决定标准库 API 的库 API 团队等等。

这些团队管理着这种语言。与 Python 或 Linux 不同，它们有“**仁慈的独裁者 (Benevolent Dictator for Life)**”，而 Rust 没有。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I mean, it's really an open source project. I mean, you may know that MOS that it originally originates from Masilla, but it's not a Masilla project anymore at all. So today there's the rust project which has a bunch of different teams. There's the language team there's the which you know deals with the language. There's the library API team which deals which decides on the API of the standard library. And these teams kind of govern it. So it's the people who are these teams that run the language. And one interesting difference compared to some other popular languages like like Python or projects like like Linux is they have a benevolent dictator for life and Rust does not.
</details>

**主持人**: 这是如何运作的？特别是在有争议或需要有人拍板做决定时，决策是如何做出的？

<details>
<summary>Original English</summary>
**Host**: How is this working and and how are decisions made when especially when they're contagious or when it could help for you know some just someone to just make a decision?
</details>

**Alice Ryhl**: 老实说，如果团队没有签字同意，事情就不会发生。如果某件事真的很有争议或非常重大，通常最终会在会议上讨论。例如，有一个叫 **Rust Week** 的会议，其中有一个 **Rust All Hands** 活动，基本上把所有的 Rust 开发者都召集到一起讨论。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Honestly, if the team doesn't sign off on it, it doesn't happen. I mean if something is really contentious contentious or really big it will probably end up being discussed at a conference for example. So there's a conference called Rust week where they have an event called the Rust all hands where they're basically taking all of the Rust developers and putting them in one place. So if there was a problem like that they would probably discuss it there.
</details>

**主持人**: 这些团队是如何组织的？比如编译器、语言、库和开发工具团队。他们如何定义边界？是因为没有自上而下的强制力，所以大家自发组织并达成一致吗？

<details>
<summary>Original English</summary>
**Host**: And how are these teams structured? So like you said there's a compiler language library and and dev tools at at the very least. How do they define the boundaries? Is it just a team kind of roughly defining them and then you just kind of agree? Because as I'm thinking at a corporate level like as as a company would run there's typically teams are are founded often top down leadership doesn't mandate this will be this team that team there's bottoms up happening but often times it's top down just because it's easier but here as I understand there is no top down it's it's people self-organizing
</details>

**Alice Ryhl**: 是的。涉及到语言设计时，团队就是核心。我观察到这些团队在**授权 (delegating)** 方面做得非常好。我见过他们有时会说：“我们认为这是一个库 API 团队的决策，我们会遵循该团队做出的任何决定。”

<details>
<summary>Original English</summary>
**Alice Ryhl**: yeah really when it comes to the design of the language the teams are really that's really it teams have been pretty good as far as I've seen at delegating So I've seen them sometimes say we think this is a lips API decision and we will go with whatever lips API decides.
</details>

---

### RFC 流程与决策机制

**主持人**: 值得聊聊 **RFC (Request for Comments)** 流程。这是 Rust 项目做重大决策的方式。

<details>
<summary>Original English</summary>
**Host**: One thing that is interesting to talk about is the RFC process. So there's requests for for process. RFC request for comment is the way the ROS project makes big decisions but you know big ones is important to say.
</details>

**Alice Ryhl**: 假设你有一个比较大的语言特性，比如我曾提交过一个叫作 `derive_smart_pointer` 的提案（旨在让标准库中的某些类型不那么特殊）。理想流程是先写 **RFC**。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Basically the way it works is let's say you have a language feature that's kind of big. For example, I had one called derive smart pointer which basically makes some types in the standard library less special. So I mean sometimes people begin implementation already but the idea is that you write the RFC first.
</details>

**主持人**: 顺便说一下，这在公司内部也没什么不同。在 Uber 我们也有 RFC 流程。通常大家都遵守它，但有时工程师会先动手构建，然后才补文档。工程师到哪里都一样，都爱直接上手写代码。

<details>
<summary>Original English</summary>
**Host**: By the way that that's no different inside of like at U we had RFC process and same thing usually you follow it but sometimes you kind of start to build it and then just the idea is you write the the RC first. Yeah, I I know. It's just funny how it happens everywhere where there's engineers. I think it's is to build.
</details>

**Alice Ryhl**: 这种文档有一个模板，我觉得那个模板设计得非常好。第一部分是**动机 (Motivation)**，解释为什么要这个特性。然后有两个非常有趣的章节：**指南级解释 (Guide-level explanation)** 和 **参考级解释 (Reference-level explanation)**。

在指南级解释中，你要像是在编写教程一样，假设该特性已经存在，向用户解释它。在参考级解释中，你也要假设它已存在，但要以“语言参考手册”的方式进行正式定义。

<details>
<summary>Original English</summary>
**Alice Ryhl**: You write this doc and it has a template and I think it's actually a pretty good template. The idea is the first section is I think motivation. Well, the first one is summary, but the first important one is motivation. So, you explain why this feature and then I think they have two really interesting sections. They have the guide level explanation and the reference level explanation. And what this is is that in the guide level explanation, you explain your feature as if you were writing a guide as if the feature already existed. And in the reference level explanation, you explain your feature again as if it already existed, but as if it would be in the language reference instead of a tutorial.
</details>

**主持人**: 这真的很有趣。亚马逊也有类似的做法，要求人们在开发特性前先写一份**新闻稿 (Press Release)**。我喜欢这种方式，因为它逼着你从用户的角度出发思考。其他部分还有基本原理（Rationale）、替代方案、现有实践（Prior Art）和未来可能性，对吧？

<details>
<summary>Original English</summary>
**Host**: This is really interesting. You know, Amazon does just related to this. When they ask people to build a feature, they have a press release. like imagine if you announced this. I just love how like both this and and what you're saying it forces you to just think from a very different perspective right from from how people will use this feature and then and then other sections there's uh I think you mentioned uh rationale alternatives prior art future possibilities
</details>

**Alice Ryhl**: 是的。基本原理和替代方案非常重要，因为这让你在别人提问前就回答了问题，解释了为什么选择这个设计而不是另一个。查看 C++ 是怎么做的，以及未来能做什么，也很有帮助。

一旦你写好了 RFC，你就把它提交到 RFC 仓库开启一个 **PR (Pull Request)**。人们会进行讨论。如果该文档还没放入 RFC 目录，我们称之为 **Pre-RFC**。

<details>
<summary>Original English</summary>
**Alice Ryhl**: yeah so that you know you get to explain so rational and alternatives I think is a pretty important section because you get to answer all of the questions before they get asked and you get to explain why did you pick this design and then some other design and I think that's usually a pretty big part of an IFC and then of course it's good to look at what did C++ do and what can we do in the future as well and once you have the RFC you send it out what happens then well somehow people you get people to look at it there is an RFC's repository and you can open a pull request there with your markdown document with RFC and people can discuss it you might also write up your doc somewhere else then we call it a prefc if it's not in the IFC directory but it's kind of the same thing.
</details>

**Alice Ryhl**: 假设语言团队对该 RFC 感到满意，他们会使用一个适用于几乎所有决策的流程，叫作 **最终意见征集期 (Final Comment Period, FCP)**。他们会告诉 **机器人** 开启审批流程，随后 GitHub 上会生成一条评论，列出每个团队成员的复选框。成员们会勾选自己的复选框。一旦除了最多两名成员外，其他人都勾选了，就会进入为期两周的 FCP。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Let's say that the language team like it's a language team IFC and they're happy with it. So I said the IFC was how the language makes big decisions but then they actually use a process that comes up for all decisions essentially called the final comment period. And so the idea is they tell the bot to please start the approval process and then it will create a comment on GitHub with a checkbox for every team member. And then team members check their own checkbox. And once everybody from the team except for at most two have checked their checkbox then the final comment period will begin which is 2 weeks.
</details>

**主持人**: 噢，所以当只剩下两个框没勾时，两周的倒计时就开始了。这么做的原理是什么？

<details>
<summary>Original English</summary>
**Host**: Oh. So when it's only two check boxes left then two weeks starts. What what's the rational for this? This is very interesting.
</details>

**Alice Ryhl**: 假设每个人都立刻勾选了，而另外两个人还没来得及看。这确保了每个人都有机会看到它。同时也能让进度保持在一个合理的节奏上。还有一个机制叫 **顾虑 (Concerns)**，团队成员可以提出 Concerns，这会暂停流程直到问题解决。一旦两周过去，提案就被接受。

这不只针对 RFC。如果一个 PR 更改了参考手册中的内容，团队也会用同样的方式确保大家达成共识。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I mean you know let's say that everybody checks that box immediately and then the two other people didn't get to a chance to look yet. So it's to make sure that everybody has a chance to see it. Yes, I understand. And also to keep things moving at a sensible pace. So there's another part of the process which is concerns. Team members can file a concern which basically pauses the process until it's resolved and then once the two weeks pass it's accepted. So that's essentially how the team makes decision and this is not just IFC's. If you have I don't know a pull request changing something in the reference then the language team might say oh we need to make sure that everybody is on board with this change. they'll tell the bot to start an FCP on this random PR or some random issue or what wherever it might be. The same process applies
</details>

---

### 特性稳定化与发布周期

**主持人**: 提案通过后，特性就开始构建。你提交 PR 并进入语言开发。

<details>
<summary>Original English</summary>
**Host**: and then once let's say it says lang language feature okay the RFC is accepted we know what we're going to build then the feature is just built you start to open your pull requests and get into a language pretty much
</details>

**Alice Ryhl**: 但你会把特性放在**特性标记 (feature flag)** 后面。在 Rust 中我们称之为 **Nightly 特性**。只有使用 **Nightly 构建版**的编译器才能使用它。一旦特性实现并合并，人们就可以实验性地开始使用它。

在某个时间点，你觉得特性成熟了，就要编写一份**稳定化报告 (stabilization report)**，放在那个移除特性标记的 PR 中。报告会说明特性的使用情况、危险的边缘情况及对应的测试。接着团队再次通过 FCP 流程同意将其稳定化。之后它就进入了主分支，没有了标记。

<details>
<summary>Original English</summary>
**Alice Ryhl**: but you you put the feature behind a feature flag in Rust we have this thing called nightly features which basically means that you can't use it normally but if you use the nightly build of the compiler You can once you have your you know your feature I mean you might begin but you know once you have your accepted RFC you start submitting pull requests uh you implement your feature it gets merged and people start using it experimentally on a nightly build. Yeah. And then at some point you might say okay I think this feature is ready and this is kind of a recent invention but we have come up with this idea of a stabilization report in the pull request that change that removes the feature flag. We write up a little report saying for example how it's been used and explaining like oh here are the dangerous edge cases here are the tests for each of the dangerous ed. So that kind of stuff and then they use the FCP process again to agree to stabilize it and then it's merged and so now you have a feature without a feature flag.
</details>

**主持人**: 之后它就会进入 **Stable** 分支。

<details>
<summary>Original English</summary>
**Host**: Yeah. In the main branch. Yes.
</details>

**Alice Ryhl**: 大约 0 到 6 周后，它会进入编译器的 **Beta** 版本，再过 6 周，Beta 版就变成了下一个 Stable 版本。Rust 有严格的**六周发布周期**。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Between 0 days and 6 weeks from that there will be a beta release of the compiler and it will be and it will be in it. Yeah. It will be in it and then 6 weeks later the beta release becomes the next stable release. Okay. So, so like Rust has a strict six week release cycle unlike with Linux. Well, Linux also has a a rough emo, but here you just take the state stable bash. You're not doing any special.
</details>

**主持人**: 所以没有“只有 Beta 版可用的 Beta 特性”这一说。

<details>
<summary>Original English</summary>
**Host**: Yeah. And so we don't really have a concept of beta features that are only available a available on beta.
</details>

**Alice Ryhl**: 要么是 Nightly，要么是 Stable。Beta 的主要目的是测试下一个 Stable 版本，希望能在发布前发现并修复问题。

<details>
<summary>Original English</summary>
**Alice Ryhl**: You you have the nightly pretty much nightly or people can get on to the latest branch which is not yet cut. Yeah. The main purpose of beta is to test like you get six week to test the stable release. So hopefully if there's any problems we can fix them before it goes out into a stable release.
</details>

---

### 版本 (Editions) vs. 兼容性

**主持人**: 你提到 RFC 仅针对重大决策。那么想要达成共识的小决策呢？

<details>
<summary>Original English</summary>
**Host**: And you mentioned that RFC's are only for large decisions that need to be made and you've you haven't written that many either just because they're large. What about smaller decisions that you also want to get consensus on?
</details>

**Alice Ryhl**: 库团队有 **ACP (API Change Proposal)**，本质上就是 GitHub 上的一个 Issue，描述 API 接口及其必要性。这比 RFC 小得多。类似地，编译器团队有 **MCP (Major Change Proposal)**，尽管叫“Major”，其实是针对那些需要开 Issue 但不需要 RFC 的中型特性，比如一个新的编译器标志位（flag）。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So here there are a few different ways to do it. So let's say you want to add a new function in the standard library or a new type. Then the library team actually has this thing called an ACP an API change proposal which is basically just an issue on GitHub. So you open your issue, you describe your API, describe what the interface is and explain why you should have it. uh and it's much smaller than an RFC would be and then the library team can say this is okay with us and then you can implement it on unstable or nightly and then later you can then stabilize it and similarly the compiler team has it's kind of what major change proposals which for the small smaller features Yeah, even though it's called major, right? It's it's big enough that they need you to put up an issue, but not big enough to need an RFC. And for the compiler team, the classic example would be a new compiler flag.
</details>

**主持人**: Rust 每六周有新版本，但它还有 **Editions (版本年代)**，如 2015、2018、2021、2024。什么是 Editions？

<details>
<summary>Original English</summary>
**Host**: Now, Rust has new new builds every 6 weeks, right? But it also has additions. There's one in 2015, 2018, 2021, 2024. What are additions?
</details>

**Alice Ryhl**: **Editions** 与常规版本号不同。即使你用的是 1.90 版本的编译器，不同的 **Crate**（包）可以使用不同的 Edition。Rust 有极其强大的**向后兼容性保证**，你的代码应该永远能运行下去。

Editions 是 Rust 在不破坏现有代码的情况下引入**破坏性更改**的方式。比如，他们想改变语法——`async` 和 `await` 是在后来的 Edition 中添加的。在旧 Edition 的代码中，你可以把 `async` 用作变量名，但在新 Edition 中不行。关键是你可以**混合匹配**使用不同 Edition 编写的代码，它们可以无缝协作。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So the thing about additions that is different from versions is that if you're using version 1.90 of the compiler, everything is using that version. But different crates can use different editions. And so I might have a crate using the 2025 edition of the language and I can keep using that forever because Rust has a really really high backwards compatibility guarantee. So you write all of your code and the guarantee is that it's going to keep working forever. That's the idea anyway. Additions are basically the way that Rust makes breaking changes without breaking people because they might change the syntax of the language. For example, async a weight was added in addition and so code using the old edition can't use async await there. You could have a variable called async if you want. lead as evil 5 and then in the new edition you can't but you can still mix and match code written in different editions so they work together.
</details>

**主持人**: 很有趣。所以我的库可以用 2021 版，而你的项目可以用 2024 版，我依然能引用你的库。为什么 Rust 选择 Edition 这种方式，而不是像 Java、PHP 或 Ruby on Rails 那样直接用主版本号（Major Version）？听起来 Edition 几乎等同于其他语言的主版本号升级。

<details>
<summary>Original English</summary>
**Host**: Oh interesting. So I might have a library written in the 2021 edition and you can write your library in 2024 edition or your binary project and then you can still use my library. Why do you think Russ decided on additions which feels a bit more confusing to me as a developer as opposed to versions? Like when I look at Java's versions or PHP's versions or even Ruby on Rails versions, you know, there's always a m there's a major number. And I might be wrong, but it sounds to me that an addition is almost an equivalent of a of a major version at other languages. Is that putting it correctly or am I missing some details here?
</details>

**Alice Ryhl**: 核心理念是：我们希望**旧代码继续有效**，但我们仍想改变语言。这与其他语言的升级（比如 Python 2 到 Python 3）不同，你可以完全随意地混合使用不同 Edition 的代码。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Really the big idea is to say we want the old code to continue working but we still want to change the language. And so the the difference from other kinds of versions of languages I mean Python 2 version Python 3 comes to mind is that you can totally mix and match in any way you want.
</details>

---

### 语言团队顾问与企业影响力

**主持人**: 你最近成为了 **语言团队顾问 (Language Team Adviser)**。这是个什么样的角色？

<details>
<summary>Original English</summary>
**Host**: You are a language team adviser uh or you recently became one. What is a language team adviser and and what do you do as part of this role?
</details>

**Alice Ryhl**: 语言团队每周都有会议。顾问角色是成为“**语言团队轻量版**”成员的一种方式。团队表示“我们信任这个人的意见”，但你不必参加每一场会议。你没有 FCP 的勾选权，但你仍可以提出顾虑。这是一种无需全额投入即可参与并帮助团队的方式。对我来说，如果成为正式成员，就意味着每周三晚上得去开会，没法正常吃晚饭了。

<details>
<summary>Original English</summary>
**Alice Ryhl**: We have of course the language team which you know they meet they have meetings every week and they do a lot of stuff and so on and so forth. The language team advisor role is a way to be part of the language team light in some sense. So you're someone that they've said, "Okay, we trust this person's opinion, but you don't necessarily go to every single meeting." Like there's no checkbox for you on an FCP, though you can still file a concern. So yeah, it's really a way to participate in or help the language team without full membership. And full membership might entail a lot of things, right? For example, for me, it would entail going to meetings every Wednesday evening instead of like when I would normally have dinner.
</details>

**主持人**: 根据你的观察，**企业影响力**对 Rust 的影响如何？比如在 Linux 领域，大约 80% 的频繁贡献者是由公司雇佣的。在 Rust 领域，人们通常像你一样由雇主支付薪水吗？还是说有基金会支持全职工作？

<details>
<summary>Original English</summary>
**Host**: from your observation how what is the corporate influence like on on Rust in the sense that when I talk with with Greg KH he was telling me that in practice about 80% of the frequent Linux contributors are typically employed by a company which sees value in um adding their their features or or maintaining their features in in Linux which which turns out to be like a nice kind of I guess symbiosis in some ways for for Rust the the people working on it? Are they usually paid by their employers like you are? I I'm I'm sure there's people who are just every now and then contributing, but people who are spending more time on this. Do you see a pattern of corporations actually supporting this or is there a foundation that also supports people to work on this full-time or close to full-time?
</details>

**Alice Ryhl**: 我认为 Linux 内核在“让成千上万人利用工作时间进行贡献”这方面是真正独特的。Rust 项目做得也不错，有很多被雇佣的贡献者，但远未达到 Linux 的规模。

此外，**Rust 基金会**有一些**资助金 (Grants)**。例如，如果你是一名学生，想在某些方面开展工作，你可以从基金会获得资金。我觉得基金会在这方面做得非常酷。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I would say here that the Linux kernel is truly unique in this particular aspect in that they have thousands of contributors doing it on work time. I actually think that the Rust project is doing pretty well at having people do it and get paid for it like by their employer, but it's nowhere near the to the same extent as as the Linux kernel. The Rust project also has a few other interesting things. So the Rust Foundation have some grants that allow I mean for example if you're a student and you want to work on something you might be able to get a a grant some money from the Rust Foundation. I think that's a super cool thing that the foundation is doing especially I think getting people involved students involved or or you know the people who would find it harder or more daunting to to get involved in a project like this.
</details>

---

### 如何为 Rust 做贡献

**主持人**: 对于想要为 Rust 生态做贡献的软件工程师，你有什么建议或资源吗？

<details>
<summary>Original English</summary>
**Host**: Speaking of which, for a software engineer who would be interested to contribute to the Rust ecosystem, what would your suggestion be in terms of both resources or or ways to get started?
</details>

**Alice Ryhl**: 显然你可以去 Issue Tracker 寻找感兴趣的问题。我认为最好的切入点是如果你自己想改变某些东西。如果你想为 Rust 语言本身做贡献，大部分沟通发生在 **Zulip**（一种聊天服务器）上，你可以去那里和人们交流。

**Rust for Linux** 项目也有一个非常好的贡献页面 (`rustforlinux.com`)，上面有一些你可以参与的驱动开发链接。另一件很酷的事是，你可以“不通过给 Linux 内核做贡献来为 Linux 内核做贡献”——比如你实现了一个 Linux 所需的 Rust 语言特性，你就间接贡献了。或者你可以参与 **Rust in GCC** 项目。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I mean, obviously you can go to the issue tracker and look for issues that interest you. I think that often it's I mean, the best way to contribute something is if you have something you want to change about it. I think that's often a pretty good starting point. So if you wanted to contribute to the Rust language itself, Rust does a lot of its stuff on uh something called Sulip which is a chat server where people talk and you you could go there and talk to people. So the Rust for Linux project has a pretty nice contributing page. So, rustforlin.com and there's a contributing page there with for one some of there are a few different um drivers you might be able to contribute to and they have links to the issue tracker there. Another thing that's really cool is you can contribute to the Linux kernel without contributing to the Linux kernel, right? because you might take a Rust language feature we need and implement it and now you've contributed to the Linux kernel indirectly or maybe you want to work on the Rust in GCC project and help move that forward and so I think there are a lot of different projects other than the Linux kernel that would help Rust in the Linux kernel a lot to contribute there.
</details>

---

### Linux 内核中的 Rust：从实验到正式

**主持人**: 能聊聊 Rust 在 Linux 内核中的演进吗？你是如何参与其中的？内核开发者对 Rust 的态度是否有所缓和？我记得早些时候这是一个非常激烈的讨论话题。

<details>
<summary>Original English</summary>
**Host**: Can we talk a little bit about Rust in the Linux kernel on on how that has evolved? How you got involved in in writing Rust in in the Linux kernel? And have you seen the approach of of especially Linux kernel devs uh change or soften towards Rust? Because I I know it was a very heated topic earlier on.
</details>

**Alice Ryhl**: Linux 有个会议叫 **Linux Plumbers**。过去几年我一直以 Rust for Linux 成员的身份参加。一个显而易见的现象是，每一年参会，你都会发现情况比去年发生了天翻地覆的变化。这种感觉我已经连续经历四次了。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Linux has this conference called Linux plumbers which you know as part of my work on rest for the Linux kernel I've been going to for the past few years and one thing I think has been really obvious is every time I've gone you can say things have totally changed since last year. I've experienced this like four times in a row.
</details>

**主持人**: 那太酷了。

<details>
<summary>Original English</summary>
**Host**: That's kind of pretty cool.
</details>

**Alice Ryhl**: 发生了很多事情。某一年我去参会，人们可能还觉得“喔，你们那个小东西挺有意思的”；到了下一年，他们就在自己的子系统中引入了 Rust 代码。

最重大的消息来自 2025 年 12 月的 Linux Plumbers 会议。在 Linux 内核维护者峰会上，我们达成共识：**Rust 在内核中不再是实验性的 (no longer experimental)**。与前一年相比，这对我们来说意义重大。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Yeah. I think there's really a lot of stuff that's happening. I mean, one year I might go and people think, "Oh, that's some nice little thing you have there, right?" And then the next year now they have Rust code in their subsystem. It it kind of keeps going. The the the most recent Linux plumbers from December 2025 was there. The big news were that at the Linux kernel maintainer summit, we agreed that Rust is no longer experimental in the kernel. That was really big for us compared to the previous year.
</details>

**主持人**: 所以现在这意味着 Rust 拥有了与 C 语言同等的地位，对吧？

<details>
<summary>Original English</summary>
**Host**: Yeah. So, so now that means that it's official like like Rust has the same status as C, which is the lang the language that the kernel is written in, right?
</details>

**Alice Ryhl**: 也许不是完全相同的地位，但不再是“实验性”清楚地标志着它更加稳定了。这证明了它确实行得通。

基于你所说的内存安全，加上在需要时能使用 `unsafe`，这已经展现了巨大的前景。而且现在也有相关的法规出台，比如**美国国防部**通过规定，由于安全顾虑，将不再允许机构使用非内存安全的语言。这实际上意味着 Rust 和其他内存安全语言可以被使用，而 C/C++ 将面临更严格的审查。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I guess. Well, not the same status, but but not not being experimental. It it clearly marks that it's more stable. Experimental sounds like it's it's not as stable. Basically, we've proved this is going to work. I mean based on what you've laid out with just with memory safety and of course being able to use unsafe when you need to that already like shows a lot of I guess promise plus there's there's some regulation as well right there's I think the US Department of Defense passed some regulations saying that they will not allow their agencies to use non-memory safe languages for the concern of security vulnerability. ilities and you know this would practically mean that Rust and other memory safe languages could be used but C, C++ or maybe one day systems that are built in this one might see larger scrutiny.
</details>

**Alice Ryhl**: 是的，多个政府都有类似的举动。他们在说：“你们在这个项目中用 C/C++，导致了无法接受的内存安全漏洞，而如果你们不用这些语言，这些问题根本就不会发生。那为什么不干脆别用了呢？”

<details>
<summary>Original English</summary>
**Alice Ryhl**: Yeah, there have been different stuff like that from multiple different governments, right? These governments are saying, "You guys are using C or C++ in this project and it's causing an unacceptable amount of memory safety vulnerabilities that simply don't happen if you just don't. So what if you didn't do that?"
</details>

---

### AI 与 软件工程的未来

**主持人**: 在这段对话中，我们竟然坚持了这么久没提到 **AI**，考虑到现在的世界局势，这简直令人印象深刻。

我很想知道，你在构建 Tokio 或为 Rust 做贡献的日常工作中，会使用 AI 工具吗？你觉得需要它们吗？

<details>
<summary>Original English</summary>
**Host**: in in this conversation, we managed to go for a very long time without even mentioning AI once, which uh given where the world right now is and and how these tools are are spreading. That that that's pretty impressive. I I was interested, do you use any of the AI tools for your day-to-day work building Tokyo, uh contribute contributing to Rust projects? Have you found a need for them at all?
</details>

**Alice Ryhl**: 我一直在尝试使用它们。我挺喜欢 **Gemini 命令行界面 (CLI)**，我觉得它很简洁。这些工具在根据 Prompt 输出代码方面非常在行。但在你的日常工作中，你实际打代码的时间占多少？相比之下，评审代码、思考方案、制定计划的时间又是多少？听起来在 RFC 流程中，大部分时间花在思考、达成共识和确保正确性上，代码编写反而是次要的。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So, I have uh been trying to use them. Honestly, I'm still learning how to use these tools, but I have used them. I I quite like the Gemini command line interface. I think it's uh pretty neat. These tools are pretty proficient at outputting code or, you know, giving a prompt and it it putting out code. But in your day-to-day work, how how much code do you actually type as opposed to reviewing code, thinking about what to do, making a plan? Does it sound like as we're talking about the RFC, for example, the RFC process, my sense was most of that was thinking about what to build, getting a consensus, making sure it's right, and it almost sounded like the actual code itself would be the I don't know, lesser. Of course, you know, there's a lot of work involved, but you see what I mean. the the actual time spent will probably be less than everything else around it.
</details>

**Alice Ryhl**: 编写代码仍是流程中重要的一部分。很多人谈到使用 AI 时，编写**测试**非常重要，因为这样 AI 才能判断自己是否做对了。我之前提到的重构故事，我只是按照编译器的指示操作。同样的原则也适用于 **Agent**，它们可以和编译器对话，编译器会告诉它们如何修复。

因此 Rust 可能是 AI Agent 的一个非常有前途的候选语言，因为它们能获得更多的反馈，而且在 Rust 中发布某些类型的 Bug 很难甚至不可能。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I think it's still an important part of the the process. I mean, a lot of people talk that about that when you use AI, it's really important to write tests and that kind of thing because then the AI is actually able to tell if it did it right. I explained this story from before about how I was refactoring something. I just told did what the compiler told me. I think the same kind of principle applies with agents in that they can talk to the compiler. It will tell them what to fix. So I guess this could be a case. We we'll see. But Rust could be a pretty promising candidate for to use for agents because they can get more feedback and it's just hard it's harder to to ship certain type of bugs or maybe impossible to have certain type of bugs.
</details>

**主持人**: 对于像 Linux 内核这样正确性和可靠性极其重要的地方，已经有了多层人工评审。你认为 AI 生成的代码在这些领域会有真正的帮助吗？或者这里反而不需要太多 AI，因为变更传播速度较慢是有意为之的？

<details>
<summary>Original English</summary>
**Host**: Yeah, I think there is a aspect of that for places like the Linux kernel where I mean correctness is extremely important, reliability is very important. There's already multiple layers of human review which which is is in place. Do you see potential for AI generated code to prove helpful somewhere like actually truly helpful like again assuming that these things can generate you know as per specification or as per what what you need or or could could this be a place where it might be one of the places where we might not need that much because it it already feels a kernel to me it feels like a place where there's a lot of people coming in contributing and and there's there's a reason that change can propagate slower
</details>

**Alice Ryhl**: 在 Linux 内核维护者峰会上，我们讨论过使用 **AI 进行代码评审**。有些维护者设置了机器人，当你发送邮件到邮件列表时，它会喂给 AI Agent 进行评审。Linus 和其他人提到，这些评审对内核代码来说其实非常令人印象深刻。

这不会是替代方案，而是另一种获取反馈的方式，更快速，是一个额外的安全网。即便你是顶尖程序员，也会犯一些低级错误，而内核中有无数个可能犯错的地方。如果 AI 能抓住其中的大部分，那就非常好了。

<details>
<summary>Original English</summary>
**Alice Ryhl**: when I was at the Linux kernel maintainer summit, one of the topics that came up was using AI for code review and there were some people there who had for example set up bots that would say when you send an email to the mailing list, it would feed it into an AI agent which would leave a review. That kind of stuff. And for example, Linos and others were talking about how these reviews were actually really impressive for kernel code. At least what's being discussed in the kernel community, that kind of use case seems like something people are excited about. And it it sounds like this would not be a replacement obviously, but just one more way to get feedback, maybe doing it quicker and and just an additional safety net, if you will, right? I mean, that's the thing with memory safety, right? You make some sort of trivial mistake. It it's not some complex thing. It's just you make some trivial mistake and there's a bajillion places you could make it. So even if even if you're a really good programmer and only make it.1% of the time or whatever, it's still going to happen, right? And so if the AI can catch a lot of those, then you know that's pretty good.
</details>

---

### AI 处理繁琐工作 (Toil)

**主持人**: AI 也可以帮着寻找缺失的边缘情况测试。相比于初创公司强调的“更快”，我更喜欢我们今天讨论的如何利用 AI **提高质量**。

<details>
<summary>Original English</summary>
**Host**: Well, and I guess some creative use cases could be for example there tests are are a big thing, but AI might be able to help figure out if there's edge cases missing again if if the language itself does not support it. There could be what I understand and there's there could be a lot of potential to add more safety nets that do not exist today. I think that's right. I like this approach. So this is this is one of the first conversations I'm having where we're talking about AI where we're talking about how to increase quality wi with AI because in again in startups or whoever is building there's a lot of talk about how it can make it faster faster restoration and there's usually a quality trade-off that we usually do not talk about but I I love that we're actually talking about the things that can increase quality or or at least keep it at the same level.
</details>

**Alice Ryhl**: 我自己也用 AI 写过一些补丁，效果还行，但发送前肯定需要人工评审。

还有一个我记忆犹新的例子：我提交了一个让 **Binder** 变快的补丁，评审反馈让我跑个基准测试（Benchmark）。我想：“天哪，我还得写个基准测试。”但我让 AI 帮我写了。它非常聪明，找到了一个现有的基准测试并进行了巧妙的修改，然后跑了测试，接着写了个 Python 脚本分析数据文件，最后呈现出一个精美的表格。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I mean I have actually written a few patches with AI myself. It worked okay some I mean it definitely required my review before sending it out to the list. really did sometimes. But you know, another place I remember using it was I had this commit that ma made binder faster in some way and one of the review comments I had received was, "Hey, can you run a benchmark?" I said, "Oh my god, now I have to write a benchmark." But then I got the AI to benchmark it for me. And what it did, what it actually went and found an existing benchmark and modified it a little bit in a quite clever way. and then it ran it for me and then it wrote a Python script to analyze the text file with the numbers and presented it in a nice table.
</details>

**主持人**: 听起来这属于那些你可以做但非常枯燥的**繁琐工作 (Toil)**。

<details>
<summary>Original English</summary>
**Host**: So it sounds like this was toil work that you could have done but
</details>

**Alice Ryhl**: 是的，而且如果没有 AI，我可能不会做得那么好，可能找不到现有的工具。它至少帮我节省了大量时间。

<details>
<summary>Original English</summary>
**Alice Ryhl**: yeah of course you might have not done as good of a work because you might have not found that utility you might not not figure out to do that. I mean at least in that instance it saved me time if nothing else.
</details>

---

### 学习资源与专家建议

**主持人**: 对于想要精通 Rust 的资深工程师，你有什么学习建议？

<details>
<summary>Original English</summary>
**Host**: for a senior engineer who would like to learn Rust or you know just build with it what would your suggestion to be to get started of of course for AI might be one of the things which makes it a lot easier just to to get started but if if you would like to learn what do you recommend for for people who actually want to become proficient at the language.
</details>

**Alice Ryhl**: 首先，官方网站上的 **《Rust 权威指南》 (The Rust Book)** 非常出色，它是免费的。此外，学习一门语言最好的方式就是做一个**实际的项目**，比如写一个 Web 服务器。

<details>
<summary>Original English</summary>
**Alice Ryhl**: So for one, I would say that the Rust book which is so it's on the official Rust website is actually really good, right? And you don't have to it's freely available online. Rust has this idea of calling tutorials for books for some even though they're online which is kind of funny. But anyways, I think the Rust book is really good. Other than that, I think honestly the way you learn a language is you have you have a project. You you implement some sort of project with it. I mean maybe some sort of web server or something.
</details>

**主持人**: 再多问一点关于 AI 的事。现在学语言变容易了，因为你可以让 AI 写这写那。但在 Rust 案例中，这是否会产生一种“理解的错觉”？特别是我们之前讨论过理解结构、理解编译器报错的重要性。

<details>
<summary>Original English</summary>
**Host**: And one more thing on AI. So it's easy to get started with languages these days because you can just prompt the AI to like write this or that. In the case of Rust, do you think that could create a false sense of understanding especially we talked about the importance of understanding structures of understanding compiler issues which are there for a reason. You know tools could just like generate through this and create code that that runs.
</details>

**Alice Ryhl**: 这确实是一个风险。我最近尝试在非 Rust 场景下使用它——我写 **Makefile**，想在 Linux 内核构建系统中添加一个特性。它确实在 Makefile 中添加了必要的 Rust 标志，但它同时也给 C 语言那边添加了一些不必要且被误用的标志。任何人类看到这代码都会觉得奇怪。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Yeah, it it's totally a danger. I recently tried using it for something where I guess I was not writing Rust code. I was writing make files. I wanted to add some support in the Linux kernel build system for for some feature and it went into the make file and added the Rust flags necessary to do it. But then I looked at the code and it was it had added the necessary build flags but to the C side it was passing a few more flags which were not required per se but they were there for a reason and it had just ignored them. Any human looking at this would be like why did you add Rust versions of all the flags?
</details>

**主持人**: 你最喜欢的 Rust 特性是什么？

<details>
<summary>Original English</summary>
**Host**: What is your favorite Rust feature if there is one?
</details>

**Alice Ryhl**: 我目前正在开发一个新特性，非常令人兴奋。我们在 Linux 内核中遇到了**就地初始化 (In-place initialization)** 的需求，即在构造值时就知道它是在哪里构造的，这样之后它就不会被移动。目前这还在进行中。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I'm currently working on a new feature which I think is really exciting. It's something that that we ran into in the Linux kernel where we needed in place initialization, the ability to construct values while knowing where they're being constructed so they don't get moved afterwards. I'm pretty excited about our work to put that into the language, but it's very much ongoing. I I think that's pretty cool stuff.
</details>

**主持人**: 最后，你有哪些推荐的读物？

<details>
<summary>Original English</summary>
**Host**: And as as closing, what are what are books you would recommend that you've enjoyed and and why?
</details>

**Alice Ryhl**: 除了官方的《Rust 权威指南》，我还推荐 **John Gjengset** 的那本书，它面向**中阶开发者**，适合那些已经有了一些 Rust 经验但想更进一步的人。

此外，**Rustlings**（一个练习项目）也非常棒，它给你一些不完整的代码让你去修复，这是学习语言的一种非常酷的方式。

<details>
<summary>Original English</summary>
**Alice Ryhl**: I already mentioned the the official Rust book. I also think that so John Ganget has another book that I think is really good and this book is kind of aimed at the intermediate Rust developer. The the Rust developer who has gotten some Rust experience but wants to go further. I think that's also a pretty good book for for that audience. Some other resources which are not books but which I think are also really good is there's this thing called rustlings and the idea is that they give you some unfinished rust code and your task is to finish it.
</details>

**主持人**: 太棒了，Alice。非常感谢。我学到了很多。

<details>
<summary>Original English</summary>
**Host**: Oh, nice. Awesome, Alice. Thank you. Thank you. Thank you so much for this. This was really interesting and I've learned a bunch.
</details>

**Alice Ryhl**: 谢谢你邀请我。

<details>
<summary>Original English</summary>
**Alice Ryhl**: Thank you for having me on.
</details>

---

### 结语与总结

**主持人**: 希望你们像我一样享受这段关于 Rust 细节的探讨。我感触最深的一点是 Rust 的设计是如此缜密，它是围绕着“程序员实际上一直在犯哪些错误，以及我们如何消除这些错误”来设计的。例子包括内存安全、没有 `null`、将错误作为不可忽略的值。**文档测试 (Doc Tests)** 也是一个绝妙的主意——如果文档里的示例代码坏了，整个构建就会失败。这是我第一次听说将如此聪明的理念内置于语言中。最后，Rust 之所以流行，是因为它开辟了一个以前不存在的范畴：一种既**可靠**又**高性能**的语言。这使得它既能用于内核开发等高性能计算场景，也是高级后端语言的一个优秀替代方案。

请查看节目单，了解更多关于后端主题以及 Kotlin、Swift 等语言构建故事的深度文章。如果你喜欢这个播客，请在各大平台订阅。如果你能给节目打分，不胜感激。

<details>
<summary>Original English</summary>
**Host**: I hope you enjoyed getting into the details about Russ as much as I did. One thing I appreciated talking about is how deliberately Rust seems to have been designed around the question, what mistakes do programmers actually keep making and how do we eliminate those mistakes. A few examples include memory safety, not having a null, and the errors being values that you cannot ignore. The documentation example is also an interesting one. Documentation tests or doc tests are automatically run as tests. If your example breaks, then your build breaks. This is the first time I've heard this clever idea implemented in a way that's easy to use in a language. Finally, the question on why Rust is becoming so popular might be because it's in a category that did not exist before, a language that's reliable and also performant at the same time. This makes it usable for high performance computing cases like kernel work while also being a good alternative for higher level back-end languages. Do check out the show notes for related the pragmatic engineer deep dives that go even deeper into back-end topics and stories of building languages like Cotlin and Swift. If you've enjoyed this podcast, please do subscribe on your favorite podcast platform and on YouTube. A special thank you if you also leave a rating on the show.
</details>