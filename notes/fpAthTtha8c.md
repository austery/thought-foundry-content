---
author: Latent Space
date: '2026-06-25'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=fpAthTtha8c
speaker: Latent Space
tags:
  - scaling-laws
  - reinforcement-learning
  - benchmark-overfitting
  - research-taste
  - agi-path
title: 与OpenAI首席研究官Mark Chen的烹饪对话：AGI、o1、评估与扩展定律
summary: 在轻松烹饪韩式豆腐汤的过程中，OpenAI首席研究官Mark Chen深入探讨了从交易员到研究负责人的职业转型、研究品味的培养、强化学习的适用边界、评估危机与基准过拟合、o1推理模型的诞生历程、预训练是否已死、以及通往AGI的路径。他强调了扩展定律的持续有效性、高风险研究赌注的重要性，以及未来研究将越来越依赖模型自主执行与人类提出创意的协作模式。
insight: ''
draft: true
series: ''
category: ai-ml
area: tech-engineering
project: []
people: []
companies_orgs:
  - OpenAI
products_models:
  - o1
  - Codex
  - AlphaGo
media_books: []
status: evergreen
---
### 开场与汤的故事

**[主持人]**: 嘿，各位，欢迎来到 Latent Space 烹饪系列，我们邀请创始人和研究人员，然后让他们自由发挥。今天，我们有一位非常特别的嘉宾，OpenAI 的首席研究官，Mark Chen。欢迎，Mark。

<details>
<summary>Original English</summary>

**[Host]**: Hey guys, welcome to the Latent Space cooking series where we invite founders and researchers and just let them cook. Today, we have a very special guest, the chief research officer of OpenAI, Mark Chen. Welcome, Mark.

</details>

**[Mark Chen]**: 谢谢邀请，Alan。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Thanks for inviting me, Alan.

</details>

**[主持人]**: 谢谢你能来。我的意思是，这一切的灵感始于一个故事：Mark Zuckerberg 会做汤来吸引研究人员，而作为回应，你给研究人员带去了汤。这是真的吗？发生过吗？有效吗？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, thank you for coming. I mean, to begin, this all started from the inspiration after hearing the story that Mark Zuckerberg would make soup to try to poke researchers and in response, you brought soup to researchers. Is this true? Did this happen? Did it work?

</details>

**[Mark Chen]**: 哦，你知道，这绝对是一个真实的故事。我确实给我们的研究人员带过汤。我觉得事情稍微平息了一点。我认为我们最终占了上风，但没错，在AI发展的疯狂历程中，这仍然是一个非常有趣的故事。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Oh, you know, it's absolutely a true story. And I have brought soup to our own researchers. I think that matters calmed down a little bit. I think we came out on top, but yeah, still a very funny story in the craziness of how AI is involved.

</details>

**[主持人]**: 你多久做一次饭？你对做饭熟悉吗？

<details>
<summary>Original English</summary>

**[Host]**: How often do you cook? Is it something you're familiar with?

</details>

**[Mark Chen]**: 嗯，你知道，我确实喜欢做饭，但我没有那么多时间享受这个。所以，我通常每周每晚都有工作晚餐，也许在AGI之后，这将成为我的爱好。我一直开玩笑说，等这一切结束后，我要开一个面摊。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Well, you know, I do enjoy cooking, but I don't have the luxury of doing that so often. So, I usually have a work dinner every night of the week and, you know, maybe post AGI, this is going to be my hobby. I've always joked that I'm going to start a noodle stand once it's all over.

</details>

**[主持人]**: 是的，是的，你知道，AGI之后，希望那还会存在，但很好。我猜看看我们面前的东西，你大概知道我们要做什么吗？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, yeah, you know, post AGI, hopefully that'll, you know, still be there, but great. And I guess looking at what we have in front of us, do you have an idea generally of what we're probably making?

</details>

**[Mark Chen]**: 呃，韩式豆腐汤，也许？

<details>
<summary>Original English</summary>

**[Mark Chen]**: Uh Korean tofu soup, maybe?

</details>

**[主持人]**: 是的，是的，大体上就是这个。所以，我们的灵感来自于你给研究人员带汤的故事。所以，我们正在做韩式豆腐炖菜，还有一些虾，我来烹饪。你准备好了吗？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, yeah, that's generally what it is. So, we inspired off of the story of you bringing soup to researchers. So, we're making a tofu Korean stew and we have prawns that I'll be cooking. Are you ready to go?

</details>

**[Mark Chen]**: 是的，开始吧。开始吧。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Yeah, let's do it. Let's do it.

</details>

### 从交易员到研究员

**[主持人]**: 太好了。好的，第一件事我们可能要做的是把蔬菜分开，然后切一下。基本上，我们想做的就是切掉带泥土的脏的部分，然后，对，把它们分开。你可以做这个。与此同时，我想我可以多问问你的背景。所以，在上一份工作中，你曾经是一名交易员。甚至Sam，我想，去年四月也发推文说，如果你是一名高频交易员，你应该考虑加入OpenAI，因为，你知道，要构建AGI。那么，你认为交易员和研究员之间有关系吗？还是你认为这只是一个非常技术和竞争激烈的领域，很多优秀的员工可能来自这里？

<details>
<summary>Original English</summary>

**[Host]**: Great. Okay, so the first thing we should probably do is we'll separate the veggies and then we can cut them. And basically, what we want to do is just cut the dirty part off with the dirt and then, yeah, separate that across. So, you can do that. And while that's going, I guess I could ask more about your background. So, in a previous life, you were once a trader. And even Sam, I think, last year in April also tweeted about how if you're a high frequency trader, you should consider joining OpenAI because, you know, build AGI. So, do you think there's a relation between being a trader and being a researcher, or do you think it's just like a very technical and competitive area where a lot of great employees can come from?

</details>

**[Mark Chen]**: 我认为真正重要的是，有很多研究人员刚开始时并没有接受过机器学习或AI研究的正式训练。我们非常相信培养人来做这件事。我认为真正的难点是创造性地解决问题和跳出框框思考的能力。这并不那么关乎你是否需要读博，尽管那确实能带来宝贵的技能。具体到交易，我不认为它是一个特别特殊的职业。我们有过很棒的数学家加入，也有过很棒的物理学家加入，但交易是一个……它非常难以破解。你无法欺骗现实世界，对吧？它是一个很难优化的指标。而且它还有很多特点，比如这是一个细节决定成败的领域。这是一种残酷的硬优化，榨干一个系统的每一分价值。其中一些技能是可以迁移的。

<details>
<summary>Original English</summary>

**[Mark Chen]**: I think really the most important thing is there are a lot of researchers who just started out without a formal training in machine learning or AI research. We've very much believed in training people up to do this. I think the real hard thing is the ability to creatively solve problems and think outside of the box. It's not so much you have to do a PhD, even though that does bring a valuable skill set. With trading in particular, I don't know that it's that special of a profession. I kind of think of it as, we've had great mathematicians join, we already had great physicists join, but trading is something where it's very unhackable. You can't kind of cheat the real world, right? It's a hard metric to optimize. And there's also a lot of characteristics like it's a field where attention to detail really matters. And it's kind of the brutal hard optimization and squeezing out the juice of a system. And some of those skills transfer over.

</details>

**[主持人]**: 明白了。是的，我猜对于那些想进入研究领域，但比如说没有博士学位的人，你认为他们可以学习或培养研究品味的主要特质或东西是什么？因为我认为这是进入这个领域的主要部分，可能对他们来说非常陌生。

<details>
<summary>Original English</summary>

**[Host]**: Got you. Yeah, and I guess for people who want to get into research, who let's say don't have a PhD, what do you think are the main attributes or things that they can learn to develop research taste? Because I guess that's the main part of getting into this field that may be very foreign to them.

</details>

**[Mark Chen]**: 是的，我认为这有点被高估了。这是你必须培养的东西，但我发现培养它的最佳机制其实就是**复现**。所以，我认为你应该找那些你真正敬仰的论文，然后尝试完全复现它。我脑海中浮现出很多应用。你知道，回到2018年，有像**ResNet**、**Pixel CNN**这样的工作，我通过尝试精确复现训练曲线，达到论文中暗示的精确训练损失或困惑度，学到了很多东西。你会看到很多人们通常不会谈论的技巧，但一旦你深入几层，你就会学到这些技巧。而且，是的，我认为真正让我进入这个领域的第一件事是**AlphaGo**对阵**李世石**的比赛。我认为那是很多人的转折点。那非常鼓舞人心。我真正投入的第一个大项目是：我能让**DQN**跑起来吗？

<details>
<summary>Original English</summary>

**[Mark Chen]**: Yeah, I mean, I think it's a little bit overrated. It is something you have to develop, but the best mechanism I've found for developing that is really just replication. So, I think you should take papers that you really look up to and just try to fully replicate it. I think a lot of applications stood out in my mind. Back in 2018, there is like ResNet, there were Pixel CNNs, and I learned so much just trying to replicate the training curves exactly, get to the exact amount of training loss or perplexity that the papers hinted towards. You just see a lot of techniques that people don't really talk about, but once you dive in a couple of layers deeper, you learn those techniques. And yeah, I think really the first thing that got me into the field was when AlphaGo played Lee Sedol. And I think that was a turning point for so many people. It was inspirational. And the first big project that I really went after was can I get a DQN working?

</details>

**[主持人]**: 是的，是的，那是真的。我想是第37手，或者类似的一局棋，看着它发生，看到所有的发展，以及我们今天所达到的位置，尤其是在研究方面，真是太疯狂了。

<details>
<summary>Original English</summary>

**[Host]**: Yeah, yeah, that's true. I think it was move 37 or something like one of the games that was pretty insane watching it happen and seeing all that development and seeing also where we have gotten to today, especially with the research.

</details>

**[Mark Chen]**: 我的意思是，你现在几乎在每个领域都能看到“第37手”，这难道不疯狂吗？就像数学里有“第37手”，计算机科学和编程里也有。我认为，甚至，是的，感觉就像今年年初很多人醒来，然后说，天哪，**智能体**在我的职业领域里起作用了。他们本质上意识到这些模型可以为他们做长周期、有意义的工作。

<details>
<summary>Original English</summary>

**[Mark Chen]**: I mean, isn't it crazy that you're seeing move 37s in almost every field now? It's like there's move 37s in math, there's in computer science and coding. I think even yeah, just it feels like a lot of people woke up at the start of this year and were like, man, agents are working in my profession. And they're essentially realizing that these models can just do long horizon meaningful work for them.

</details>

### RL的边界与评估难题

**[主持人]**: 是的，没错。看到这个确实令人印象深刻，我甚至在自己的工作中也在使用它。但是，好的，下一步很简单，就是切洋葱。我们要做的就是把它切丁。你认为有没有一些工作是**强化学习（RL）**可能更难切入的？例如，编程可能更容易，因为很多上下文可以通过代码库或你正在做的工作来获取，但假设你试图做一个初级顾问的工作，所有的上下文都比较分散，可能就更难了。你如何看待这些不同的场景？有没有一种方法可以评估什么是正确的方法？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, no, that's true. It is very impressive to see, like I'm even just using it in my own work. But okay, the next thing we could do is just as simple as cutting the onion. So, what we have to do here is just like dicing it. Do you think there's jobs that RL maybe will have like a much harder time to kind of break into? So, for example, coding maybe easier since a lot of context is accessible either through the code bases or even the work you're trying to do, but let's say if you're trying to do the job that a junior consultant may do, where all the context is a little scattered, maybe it more difficult. How do you view through like those different scenarios? Is there a way that you kind of assess what can be the right approach?

</details>

**[Mark Chen]**: 是的，我认为RL传统上在那些更主观而非客观的领域会遇到阻力。所以，如果你想想，一个例子是**创意写作**。你可以拿两篇创意写作作品，两位专家可能会有截然不同的意见。所以，在这些难以评分的领域，RL直接应用的能力最弱。我知道很多人正在开发在这些环境中应用RL的技术，但就目前而言，只有在存在冷酷、硬性真理的地方，比如数学和计算机科学，你可以证明它对或错，你才会看到它真正起飞。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Yeah, I mean, I think RL's traditionally had headwinds when it's come to fields that are more subjective than objective. So, if you think of one example of this is creative writing. Where you could take two pieces of creative writing and two experts can have wildly different opinions. So, it's these fields where things are hard to grade. Where RL has the least amount of ability to go and directly apply there. I know a lot of people are developing techniques to apply RL in these settings, but for now, it's just where there's cold hard truth, things like math and computer science, where you can prove it correctly or wrong. That's where you kind of see it really taking off.

</details>

**[主持人]**: 是的。这实际上引出了一个关于评估这些领域的想法。所以，随着模型变得越来越强大，甚至在解决像**IMO**问题这样的任务上达到饱和，你如何看待评估**超人类智能**？当它变得如此擅长，甚至只有顶尖的0.01%的人类才能做到的事情，我们如何推动超越那个智能前沿？

<details>
<summary>Original English</summary>

**[Host]**: Yeah. No, that actually brings up a thought on in terms of evaluating those fields. So, as models get much much more powerful and even saturate, for example, solving like the IMO questions. How do you view evaluating like superhuman intelligence? Like it gets to a point where it's so good at things that even the top 0.01% of humans can do, how can we push past that frontier of intelligence?

</details>

**[Mark Chen]**: 不，这有点疯狂，我觉得很多都集中在与现实世界的交互上。当我们过去思考如何超越像编程竞赛这类事情时，我认为我们最初采取的方向是应该将其转移到**现实世界的研究**中。我们已经看到模型在发现新颖定理和推动硬科学前沿方面变得好多了。但即使在今天，这也不再是惊喜了。我认为我们几乎已经认为这些模型能解决非常非常困难的问题是理所当然的。它们可以做出贡献，甚至在领域之间建立新颖且有洞察力的联系。所以，我认为我们把**编码协作**视为一个真正测试模型能否在高上下文和现实世界长周期环境中学习的领域。

<details>
<summary>Original English</summary>

**[Mark Chen]**: No, it's kind of crazy, and I feel like a lot of it centers in on interfacing with the real world. And when we've thought about how to evolve past things like programming contests in the past, I think a lot of the initial direction we took was you should move it to real-world research, right? And we've seen that the models have gotten a lot better at discovering novel theorems and pushing the frontiers of hard sciences. But even today, that's no longer a surprise. I think we almost take it for granted now that these models can solve very very difficult problems. They can make contributions and even draw relationships between fields that are novel and insightful. So, I think we think of coding co-working as really a domain for that that tests whether our models can learn in high-context settings and in real-world long-horizon settings.

</details>

### 预训练未死与扩展定律

**[主持人]**: 明白了。好的，是的，有道理。既然你切完了所有的蔬菜，我们现在可以下一步了，就是炒一下。我们可以用这个电磁炉，我们以前见过，非常强大。我把它打开。我们加点油炒一下。这些炉子很酷。是的，你可以倒点油。然后，我们打开炉子。按一下，然后转动旋钮。太好了。在加热的时候，我们可以等一下，然后加入蔬菜。但是，是的，我猜更多的是关于研究的观点，有没有一些普遍接受的观点是你不同意的？比如**预训练已死**，或者**语言模型永远无法带我们到达AGI**。我认为外面有很多观点非常模糊，显然还没有被证实。从你作为OpenAI研究领导者的角度来看，像这样的事情呢？

<details>
<summary>Original English</summary>

**[Host]**: Got you. Okay, yeah, that makes sense. And since you're done with all the vegetables, we can now do the next step, which is sauteing it. So, yeah, we can use the impulse stove, which we've seen before and very powerful. Let me just turn it on. And yeah, so we'll just saute it with some oil. So, yeah, put the pan in the front burner and then... These are cool stoves. Yeah, you can use oil to pour some in. And then, yeah, just a good dollop. Perfect. And yeah, and then we can turn on the stove. So, just press it. And then, yes, spin the knob. Great. Perfect. And then while that heats up, we can just wait and then add the vegetables. But yeah, I guess more so on views for research, are there commonly accepted ideas that you disagree with, whether it be like pre-training is dead or language models will never get us to AGI. I think there's a lot of takes out there that are very ambiguous and obviously haven't proven out yet. And I guess from your perspective as the research leading things in OpenAI. Like things like those?

</details>

**[Mark Chen]**: 我的意思是，我坚信指数增长和**扩展定律**。所以，我认为任何这些看跌的观点，我都相当强烈地不同意。当谈到“预训练已死”时，我认为有趣的是，这个说法只是在过去一两年左右才开始更广泛地传播。在LLM发展的历史中，人们多次说过这个，对吧？总会有一些瓶颈，人们会说，“你无法超越这个，因为存在这个瓶颈。”而我们总是能找到某种技术，无论是更好的工程还是新的研究洞察，来帮助你突破界限。所以，我认为这只是同样的事情的延续，对吧？更仔细的研究工程，更仔细的数据工程，更仔细的扩展。它总是能解锁下一步扩展的能力。所以，它已经持续了将近10个数量级，但没有理由它不应该继续持续下去。

<details>
<summary>Original English</summary>

**[Mark Chen]**: I mean, I firmly believe in exponent being on the exponential and in scaling laws. So, I think any of these bear takes, I fairly strongly disagree with. When it comes to pre-training is dead, I think the funny thing is this narrative only started spreading more widely after, let's say, the last one or two years or so. In many times in the history of developing LLMs, people have been saying this, right? And there've always been some bottlenecks that people will say, "Well, you can't scale past this because of this bottleneck." And we've always found some kind of technique, whether it be better engineering or some new research insight that helps you break past the boundary. And so, I think it's just more and more of the same, right? Like more careful research engineering, more careful data engineering, more careful scaling. And it always unlocks that next ability to scale further. So, it's held for almost 10 orders of magnitude, but there's no reason it should not keep holding.

</details>

**[主持人]**: 是的，这是一个非常公平的观点。我猜在那些帮助你超越极限的研究赌注中，有没有你记得的早期具体想法，当时每个人都说这行不通？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, that's a very fair point. I guess on research bets that have helped you scale beyond, were there specific ideas that you can even remember in the early days that everyone was saying that this is not going to work?

</details>

**[Mark Chen]**: 嗯，是的，我认为**推理**是这方面最大的例子之一。我们向世界推出的第一个突破是**o1**，但让它起步并不容易，因为当时我们生活的世界是一个预训练加后训练的世界，对吧？那感觉是一个非常有前途的范式。所以，即使在像OpenAI这样的公司，你也会自然地听到人们问，当你有一台能工作的机器时，为什么要做别的事情？从根本上说，这要归功于**Yakub**、**Ilya**以及许多在这个领域有坚定信念和远见的人，我们才开始认真推动这件事。即便如此，也花了很多引导才让整个公司支持这个作为基本赌注。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Well, yeah, I mean, I think of reasoning as one of the biggest examples of this. The first breakthrough that we launched to the world here was O1, but it wasn't easy to get that off the ground because the world we were back living in back then, it was one where pre-training plus post-training, right? That felt like such a promising paradigm. And so, even at a company like OpenAI, you would have people ask naturally, why do something when you have a machine that works? And fundamentally, it's to the credit of Yakub, Ilya, many of the people who really had conviction and vision in the space that we started pushing on this in earnest. And even then, it took a lot of steering to get the whole company behind this as a fundamental bet.

</details>

### 研究管理与文化

**[主持人]**: 明白了。你如何培养那种激励研究者的能力？因为我认为这是很大一部分，你知道，承担很多赌注，有些不会成功，但仍然在团队中建立信任，让他们知道最终其中一些会产生幂律效应。

<details>
<summary>Original English</summary>

**[Host]**: Got you. And how do you kind of develop that ability to motivate researchers? Cuz I assume that's a big part of taking a lot of bets and some won't pan out, but still building the trust in the team to know that eventually some of these will actually have power law effects.

</details>

**[Mark Chen]**: 你知道，OpenAI真正酷的一点是，研究感觉像是一个**精英管理**的地方。所以，很多时候，研究经理是那些过去实际做过最好研究的人。因此，我认为很多引导可以是自上而下的。如果你的经理说，“嘿，我真的相信这是前进的道路。”通常人们会认真考虑这一点。就像，这个你长期以来因其研究品味和执行而尊敬的人，现在对这个想法感到非常兴奋。这绝对是人们会考虑的事情。所以，我认为有很好的自上而下的引导。同时，OpenAI真正酷的一点是，也有自下而上的元素。我们喜欢被说服我们错了，对吧？有人可以带着冷酷、确凿的证据来。很多这样的事情已经变成了我们研究路线图的核心部分。就是那些没有人真正试图引导，但某个一线研究员有坚定信念的事情。看到这些也是一件非常令人高兴的事。

<details>
<summary>Original English</summary>

**[Mark Chen]**: You know, what's really cool about OpenAI is research feels like a meritocracy. So, often times the research managers are the people who have done the best research in the past. And so I think a lot of steering can come top-down, right? Like if your manager says, "Hey, I'm really convinced this is the path forward." Generally people will take that into heavy consideration. It's like, this person who you've respected for their research taste and execution for so long is now very excited by this idea. It's definitely something that people take into account. So, I think there's good top-down steering. At the same time, I think one really cool thing about OpenAI is there are bottom-up elements. Like we like to be convinced that we're wrong, right? And someone can just come with cold, hard evidence. And many things like that have turned into core parts of our research roadmap. Just things that no one was really trying to steer, but some researcher on the ground had a heavy conviction in. And that's also a really big delight to see.

</details>

**[主持人]**: 是的，绝对如此。我在你最近的一次采访中听到，你们的内部研究路线图并没有真正改变，即使经历了我们看到的所有模型开发和其他公司的情况。我猜你们多久评估一次，重新评估一次，甚至主动采取行动？我认为这不是很多被动的决策，比如其他模型发布时。但你是如何思考这个过程的，尤其是当你周围的一切都在不断变得更好？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, no, absolutely. I heard in a recent interview that you gave that your internal research roadmap hasn't really changed even through all that we've seen with model development and even other companies. I guess how often do you guys assess that, reassess that, even like act proactively? I assume it's not a lot of reactive decision-making as other models come out. But how do you think through that process, especially as everything around you just continues to get better?

</details>

**[Mark Chen]**: 是的，所以我认为高层次的研究路线图应该是稳定的。我认为人们需要一些可以扎根的东西。人们需要看到我们正在构建的东西的路径。我很高兴我们坚持了一段时间。但**实施细节**会随着时间改变。顺序很重要，相对资源分配很重要，地面上确切的具体步骤也很重要。所以，我们所做的是，我们有一些时间点迫使我们重新考虑这些事情。一个例子是当我们分配**算力**时。工作的一个部分就是弄清楚如何在项目之间分配算力。这是一个质疑我们是否真的把算力用在了最高优先级的赌注上的时刻。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Yeah, so I think the thing is the high-level research roadmap should be stable, right? I think people need something to ground in. People need to see a path to what we're building. And I've been very happy that we stayed the course for a while. But the implementation details can change over time. The sequencing will matter, the relative resourcing will matter. And the kind of exact steps on the ground will matter. So, what we do is we have kind of points in time that force us to reconsider these things. So, one example is when we do compute. One of the parts of the job is just figuring out how to allocate compute to projects. And it's a time to kind of question like are we really putting compute to use at the highest priority bets?

</details>

**[主持人]**: 是的。我猜你能不能再澄清一下你所说的更高层次与更多实施细节之间的区别？比如，高层次是像AGI那样笼统吗？那是我们的北极星，还是比那更具体？

<details>
<summary>Original English</summary>

**[Host]**: And I guess could you clarify more what you mean by higher level versus like the more implementation detail. Like is high level as general as like AGI? That's like our North Star or is it more like granular than that?

</details>

**[Mark Chen]**: 嗯，在最顶层，我们有一个专注于**预训练**的组织，也就是给模型大量的世界知识。我们专注于**强化学习（RL）**，教模型如何用这些知识进行推理，如何将小的洞察串联起来。最后是**对齐**和**后训练**。我们总是在关注如何扩展每个领域的主线，以及那些能从根本上解锁不同或更激进扩展属性的新赌注。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Well, at the very highest level, we have an org that focuses on pre-training, which is giving models a lot of world knowledge. We focus on RL like teaching the models how to reason with that knowledge, how to chain the little insights together. And then finally alignment and post-training. And we're always looking at both how to scale the mainline in each of these domains and also new bets that fundamentally unlock either different scaling properties or more aggressive scaling properties.

</details>

**[主持人]**: 明白了。我还听说，每一到两个月，你们会审查大约300个可能跟进的研究项目。有没有一种方法可以磨练这种决策能力，我猜当你决定真正加倍投入什么、放弃什么时，因为我想有很多有才华的研究人员提供了可能追求的想法。

<details>
<summary>Original English</summary>

**[Host]**: Got you. And so even in that I heard that every one to two months you go through what? Like 300 projects like research projects that could be followed through on. Is there a way that you kind of hone that decision making I assume as you decide what to actually double down on and what not to since I assume there's a lot of talented researchers who provide possible ideas to pursue.

</details>

**[Mark Chen]**: 所以我认为这实际上是关于**专注**的精神。你可能听说过一个说法，我们正在OpenAI集中我们的赌注，我们也在尝试进行更**指导性的算力分配**。我不喜欢微观管理我的经理。我认为重要的事情是授权给他们，但只是把大块的算力分配给你想要下的大赌注。但同时，也给他们一些灵活的算力池，让他们可以自由分配给他们相信的事情，或者对我们规定的分配进行微调。所以，我认为就是从每个组织中选择少数几个赌注，比如三到五个，纳入主要研究路线图，然后让经理和组织负责人去执行。

<details>
<summary>Original English</summary>

**[Mark Chen]**: So I think really in the spirit of focus. So one narrative you might have heard is we're really focusing our bets at OpenAI and we're also trying to do a little bit more directive compute allocation as well. So I don't like micromanaging my managers. I think one important thing is to empower them but to just kind of give big swaths of compute to the big bets you want to make. But then also give them kind of flexible pools of compute which they can freely allocate to things that they believe in or just kind of fudge with the allocations that we prescribe. So, I think it's just tying a small number of bets, say three to five bets from each org into the main research roadmap and then really letting the managers and org leads take things from there.

</details>

### 识别优秀研究员

**[主持人]**: 明白了。好的，有道理。我猜对于初露头角的研究员，比如在面试环境中，有没有特定的迹象或方法可以让你识别出，“好吧，这个人有潜力成为能以一种特定方式影响组织的研究员”？还是说只是看他们之前做过什么研究，这很大程度上决定了他们是否能继续下去？

<details>
<summary>Original English</summary>

**[Host]**: Got you. Okay, that makes sense. And I guess for rising researchers, so let's say in an interview setting, are there specific tells or ways that you can identify, okay, this person has some potential of becoming a researcher to impact an org in a specific way or is it like just looking at the previous research that they've done and then that is what heavily dictates whether they can actually continue on?

</details>

**[Mark Chen]**: 嗯，在一个人来到OpenAI之前，这是一个难题。我认为这确实是事实。我认为对于很多最好的研究经理来说，他们与这么多研究员合作过，久而久之你会培养出一种直觉，比如他们说的话，他们提出的想法，是否达到了同样的标准，或者是否是你自己也会思考的事情。所以有一种直觉检查，比如，他们的直觉是否与你拥有的直觉相匹配？但一开始真的很难判断。通常，在六到十二个月后，谁有最强的轨迹，谁会产生很大的影响，就非常清楚了。所以，老实说，这是一个难题，但只是见过很多人在OpenAI经历研究发展，你会培养出一种直觉，知道谁在哪些领域更有冲劲。还有一点要提的是，并非每个研究员都一样。我认为有很多不同类型的**影响力**。有些人就是接受一个想法，非常清晰，然后会在其他人之前实现它。也有些人会提出那种疯狂的想法，几乎太疯狂了，但不知何故又没那么疯狂，他们以一种不同的方式说服你，让你看到世界或另一个完全不同的项目类型。所以，有很多方式可以产生影响。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Um, it's a hard problem before someone comes to OpenAI. I think that's genuinely true. I think for a lot of the best research managers, they work with so many researchers over time where you kind of develop an intuition like the things that they say, the ideas that they bring up. Are those kind of do they hit the same mark or are they the things that you would be thinking about personally too? And so there's this gut check of, does their intuition match the same intuition that you have? But it is really hard to tell out of the gate. Usually in six months to a year, it's pretty clear who has the strongest trajectory and who's going to make a lot of impact. So, honestly, I think it's a hard problem, but just having seen a lot of people go through research development at OpenAI, you develop an intuition for who's more peppy in different areas. And one thing to mention is not every researcher is the same. I think there's a lot of different types of impact. There are the people who just take an idea, it's very clear, and they'll just implement it before anyone else. They're also the people who come up with the kind of crazy, almost too crazy, but somehow not that crazy ideas and they really convince you in a different way of seeing the world or another completely different type of project. So, there's a lot of ways to make an impact.

</details>

**[主持人]**: 是的，这很有帮助。那么，我猜进一步阐述一下，你会说顶尖工程师和顶尖研究员之间有相似之处吗？我经常听说顶尖工程师，即使在小型公司和初创公司，是那些能把一个想法的苗头一直带到生产环境的人。我猜在研究领域，是从提出想法一直到如何通过产品交付给最终用户。还是你认为他们更专注于研究本身，而不考虑最终设计、客户如何使用它？

<details>
<summary>Original English</summary>

**[Host]**: Yeah. No, that's helpful. And so, I guess elaborating on that, would you say there are similarities that you would see between, let's say, like top engineers and top researchers? Like I often hear top engineers, even at like small companies and startups, are ones who can take an iota of an idea all the way to production. I assume in research it's like coming up the idea all the way to how it's delivered to the end user through like the product. Or do you think it's more so they're focusing solely on the research and not considering like the end design, how it's used by the customer?

</details>

**[Mark Chen]**: 嗯，关于研究，很多时候前进的道路是不清晰的。所以，研究员的区别在于他们**多频繁地指向正确的方向**，以及像你说的，**品味**。我认为在工程中，有一些行之有效的模式。比如，如果你想构建一个看起来这样的产品，工程原理可能非常相似。但对于研究，我认为稍微不同的是这种能力，即拥有良好的研究品味来说服其他人你所做的事情是有前途的，然后将其整合到核心研究路线图中。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Well, the thing about research is many times the path forward is unclear. And so, what differentiates researchers is how often they're pointed in the right direction and how like you say taste, right? I think in engineering there are certain patterns that work. Like, if you want to build a product that looks this way, the engineering principles can be pretty similar. But for research, I think the thing that's slightly different is just this ability to have good research taste to convince other people that what you're doing is promising. And then to just kind of integrate it into the core research roadmap.

</details>

### 评估危机与基准过拟合

**[主持人]**: 太好了。好的，看起来我们蔬菜搞定了，现在我们要多任务处理了。我们要往锅里倒些水来做汤底。在右上角，是的，这里。拧开它。我倒一些在这里。你也可以用一些。在我们让它慢炖的同时，我们会加入蔬菜，在这里烹饪虾。好的。让我快速清理一下。看起来到目前为止一切顺利。我觉得炒菜让洋葱和蘑菇上色了。所以，我们把它打开。我猜一个看起来非常有趣的方面是**评估**。更具体地说，有没有这样的情况，你通过感觉检查觉得模型很好，但在实际基准测试中表现非常差？或者你认为它们是高度相关的，如果你的**Sweet Bench Pro**分数很高，那么你对它执行编码任务的感觉检查也非常非常高？

<details>
<summary>Original English</summary>

**[Host]**: Great. Okay, it seems like we're done with the vegetables, so now we have to multitask. So, we're going to pour some water into our pots to get the base of the soup going. So, in the top right, yeah, here. And then just twisting this off. So, I'm going to pour some here. And you can use some as well. And while we have this simmer, and we'll add the veg, we'll cook our prawns here. Okay. Yeah, so let me clean this up real quick. Looks like it's going great so far. I feel like saute got some color on the onions and mushrooms. So, yeah, let's turn this on. I guess one aspect or area that seems very interesting are evals. And more specifically, have there been instances where you've seen through just vibe checks that it was a really good, but on the actual benchmark it performs very poorly? Or do you think it's like heavily correlated that, if your Sweet Bench Pro is a high number, then your vibe check on it doing coding tasks is also really, really high?

</details>

**[Mark Chen]**: 不，不。我认为确实存在这种现象。我不知道这是否是外部使用的词，但内部我们称之为**“刷榜”**。我认为你可以在某种程度上过拟合到特定的分布。这并不能反映你泛化得有多好。因为简单的做法是，你拿一个基准测试，然后找到与基准测试非常、非常相似的实例类型，并在这些实例上过度训练。除此之外，该领域另一个可怕的事情是，**规范的黄金标准基准测试数量很少**。我们确实处于一种**评估危机**中，对吧？所有我们成长过程中知道的伟大评估，比如参加SAT考试，都已经完全饱和了。我们真的需要找到新的好方法来对模型进行基准测试。我认为像**Codex**这样的工具的一个伟大之处在于，它们真正实现了评估的快速迭代。我们可以让一个人非常快速地整理出一个高质量的评估。另一个有趣的事情是，能够部署你的模型，你就可以看到人们在使用它们时对它们的评估。在数学、编码和软件方面，你可以从这种广泛部署中感受到它们在哪些方面会失败，以及它们能完成的任务范围。

<details>
<summary>Original English</summary>

**[Mark Chen]**: No, no. I mean, I think there is this phenomenon. Internally, I'm not sure if this is an externally used word, but yeah, just like bench maxing, you know? I think you can kind of overfit onto certain distributions. And it won't be reflective how well you generalize. Because easy ways to do this are, you take a benchmark and you just find very, very similar types of instances to the benchmark and you overtrain on these instances. Beyond that, the other scary thing in the field is the number of canonical gold standard benchmarks is low. And we really are kind of in an evals crisis, right? Where all the really great evals that we all know like growing up like taking the SAT or those are all fully saturated. And we really need to find good new ways to benchmark the models. I think one great thing about tools like Codex is they really enabled the fast iteration of evals. Like we're able to just kind of have one person just very quickly put together a very high-quality eval. Another kind of interesting thing of just being able to deploy your models is you can just see them eval as people are doing things with them. In math and coding and software, you get a sense for where they fall over, what the task horizon they can do from this general very broad-based deployment.

</details>

**[主持人]**: 是的，这很有帮助。现在，我们只需把虾放进油里，让它上色。我猜深入探讨一下，你如何平衡在基准测试中表现出色，但同时又不“刷榜”？因为我认为你想最诚实，不欺骗系统。但如果你得分比竞争对手或其他模型低，消费者可能会想，“等等，你的分数没那么好，所以模型可能没那么好。”你如何平衡这两种矛盾？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, no, that's helpful. Now, we'll just add the prawns to the oil and get some color on it. Yeah, and so I guess double-clicking onto that how do you balance both doing well on these benchmarks but also not benchmark maxing as you said. Cuz I assume you want to be most honest and not kind of cheat the system. But if you have lower scores than a competitor or from other models, to the consumer maybe like, "Wait, your score isn't that great, so the model just probably isn't that good." How do you balance both of those dichotomies?

</details>

**[Mark Chen]**: 是的，我认为关键在于，你必须在**具有代表性的评估组合**上进行操作，并始终投资于创建新的评估。有一种理念是，一旦一个评估被公开，它就已经不是一个好的评估了。还有一点是，与**外部组织**合作创建评估。在许多硬数学和科学评估中，我们与外部组织合作，他们为我们制定了黄金标准。所以，有一种有趣的理念是，将**创建评估的团队**与**优化模型的团队**分开。因为这样你就不会让他们产生共同的利益。评估团队的工作方式是，他们试图构建对模型来说很难的评估。所以，这是一个固有的对抗过程，你不会欺骗自己。两个团队之间的激励在某种程度上是以正确的方式对齐的。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Yeah, I mean, I think the thing is, you just really have to operate over representative mixtures of evals and always investing in creating new evals. And there's this philosophy of once an eval is out in the world, then it's just already not a good eval. And one thing is, also just kind of partnering with external organizations to create evals. So, in many of the kind of hard math and science evals, we've partnered with external organizations and they've been able to kind of craft gold standards there for us. So, there's a kind of interesting philosophy of separate the teams that are creating the evals from the teams that are optimizing the models themselves. Because that way you don't like coincentivize them. The way the evals team can work is they're trying to build evals that are hard for the models. So, there's this inherently adversarial process where you're not kind of cheating yourself. The incentives are somewhat aligned in the right way between the two teams.

</details>

**[主持人]**: 是的。你也参与并帮助构思过程，甚至决定应该与第三方合作开发哪些评估吗？

<details>
<summary>Original English</summary>

**[Host]**: Yeah. Do you kind of also contribute and help in the ideation process or even deciding what Evals you should work with a third party on to develop.

</details>

**[Mark Chen]**: 是的。所以，我认为**Yakub**和我做的很多工作也包括引导评估的方向。我们会注意到某些差距，或者我们想要的某些能力。而能力清单上的每一项都是一个评估，对吧？你需要某种评估来衡量你是否准确地激发了你想要的东西，并且你希望它表现良好。所以，这需要大量的引导，让每个人在评估上达成一致也是一项艰巨的工作。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Yeah. So, I mean, I think a lot of the work that Yacoub and I do also involves just kind of steering the direction that Evals go. We'll notice certain gaps, or certain kind of capabilities that we want. And every capability on the foot side is an Eval, right? You need some kind of Eval that measures if you elicited exactly what you want and you want it well. So, it takes a lot of steering and just to get everyone on the same page with Evals is also a lot of tough work.

</details>

### Yakub的趣事与“锯齿形前沿”

**[主持人]**: 是的，这很公平。我猜关于Yakub，你在之前的一次采访中说他是个非常有趣的人。你有没有什么没分享过的关于和他一起工作的趣事？因为你也说你们非常合拍。所以你们在讨论，甚至是研究讨论，都非常高效，对推动前沿有很大帮助。我猜在非常有趣的反面，有没有什么事情是你们……

<details>
<summary>Original English</summary>

**[Host]**: Yeah. No, that's fair. I guess on Yacoub, you said in a previous interview that he's a very funny guy. Do you have any fun stories that maybe you haven't shared about working with him? Cuz you also state that you guys align very well. So, your discussions even on research are very efficient and help a lot when driving towards the frontier. I guess like on the opposite side of being very funny, are there things that you're...

</details>

**[Mark Chen]**: 你问了一个有趣的故事。他昨天给我讲了个笑话，我觉得非常好笑。在很多方面，我们共同管理研究工作。你知道，显然有个研究员走到他面前说，“你知道吗，我感觉我现在有了一支由非常愚蠢的IOI（国际信息学奥林匹克竞赛）形式主义者组成的大军。”然后Yakub说，“那感觉就像我已经身处的处境。”他就是那种极其讽刺和有趣的人。

<details>
<summary>Original English</summary>

**[Mark Chen]**: You asked about like a funny story. Well, he told me this joke yesterday, which I thought was very funny. I mean, in many ways we kind of jointly manage the research efforts. And apparently some researcher came up to him and was like, "It feels like I now just have an army of really dumb IOI like formalists." And Yacoub was like, "That feels like already the situation I'm in." He's just like brutally sarcastic and funny.

</details>

**[主持人]**: 是的，那太好了。在工作场所有幽默感很好，尤其是在你推动前沿做非常重要的工作时，这有助于放松。但这也让我想到一个奇怪的情况：模型可能在IMO甚至IOI上表现得非常好，但在一些人类轻易就能完成的更平凡的任务上却可能挣扎。你对此怎么看？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, that's great. It's great to have humor in the workplace and it's good to bounce out, especially as you're pushing the frontier on very important work. But that also brings to mind one kind of weird scenario of how models can perform very well on, let's say, the IMO or even the IOI, but may struggle with some more mundane tasks that a human can easily do. So, I guess how do you feel about...

</details>

**[Mark Chen]**: 是的。最终，我认为对模型来说直观的东西，对人类来说往往不那么直观。有很多关于**“锯齿形前沿”**的类比，模型在某些事情上天生就擅长，可能是基于它看到的数据或我们更容易教它的东西。我实际上认为，很多也归结于**上下文**。模型没有很多上下文可以利用。当然，**视觉**是人类更自然的生物本能。所以，模型在某些能力上比人类强，反之亦然。但我也认为，能够从单个任务中学习经验并应用到未来任务的能力，是现在很多AI研究人员正在努力的方向。这对人类来说非常自然。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Yeah. Ultimately, I think what's intuitive for the models is often not that intuitive for the humans. There's a lot made of this jagged frontier analogy where there's some things that the models just inherently, based on maybe the data it sees or the things that we can teach it more easily, it's just good at. I actually think a lot of it boils down to also just context. The models don't have a lot of context that it can use. Vision, of course, is something that's more naturally biologically wired for humans. And so, there are just certain kind of jagged capabilities that models are better at than humans and vice versa. But I also think, context, just being able to take a single task, learn lessons from it, and apply them to future tasks, that capability is something that a lot of people in AI are working towards right now. But it's very natural for humans.

</details>

**[主持人]**: 关于上下文这一点，一个非常明显的例子是，很多人会说增加上下文窗口以提供更多示例，让模型表现更好。但你认为，即使有大的上下文窗口和很多上下文，也可能存在臃肿或所谓的“上下文腐烂”，你如何应对这个过程？

<details>
<summary>Original English</summary>

**[Host]**: And on the context point, a very low-hanging fruit example that many people will say is just to increase the context window to provide more examples so the model can perform. But do you think there's more complexity on how to actually enable, since even with a large context window and a lot of context, there could be bloat or even just a lot of context rot, as people have said. So, how do you go through that process of...

</details>

**[Mark Chen]**: 是的，所以我认为解决非常长周期学习的典型方法是，你只是天真地增加你的上下文窗口。这说得通。我认为**实现长上下文**和**很好地实现长上下文**之间是有区别的，就像你说的。有很多类似“大海捞针”的评估来衡量这一点。但我认为除此之外，在很多方面，你可以采取一些工程和研究上的捷径。比如，现在很多编码产品都有**压缩**功能。你可以压缩洞察或工作状态之类的东西，这大大简化了仅用原生长上下文构建时那些非常困难和昂贵的原语。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Yes, so I mean, I think there's kind of the canonical way you would solve for very long horizon learning, which is you just naively increase your context window. And that makes sense. I think there's a difference between implementing long context and implementing long context well, like you said. And there is a lot of needle-in-a-haystack style evaluations to measure that. But I do think beyond that, there are also a lot of, in some sense, engineering and research shortcuts that you could take. So, many coding products today have features like compaction, where you can compress either insights or working state and stuff like that, it just shortcuts a lot of the very brutally difficult and expensive primitives that you have to build with just native long context.

</details>

### 烹饪火焰与未来研究

**[主持人]**: 明白了。好的，现在我们要做有趣的部分了。我们把火调小一点，然后往锅里加一点油。然后我们要用火燎一下虾，让它们更有味道。我先在我的锅里做，给你看看样子。一次学习。等等，我没倒波本酒。好的，等一下。我们倒大约四分之一杯。然后倒进去。关火。然后点燃它。太棒了。好的，我想我明白了。好的，是的，你想自己试试吗？是的。所以，倒到四分之一杯的一半，然后你有了之后，我可以把这个给你。完美。好的，关火了。然后关火之后，你可以再打开。完美。好的。然后现在，你想拿着这个，按下这个按钮来点火。酷。完美。好的。我在烧它。有点轻，但还行。好的。然后我们可以再开火。然后我们把酒精煮掉。好的，很好。你感觉怎么样？基本上就是在煮所有东西。太棒了。

<details>
<summary>Original English</summary>

**[Host]**: Got you. Okay, now we're going to do the fun part. So, let's lower the heat a little bit and then add a little bit more oil to the pan. And then we'll torch the shrimp the prawns to get a little more flavor in there. So, I'll first do it on my pan to show you what it looks like. One shot learning. Wait, I didn't pour any bourbon. Okay, wait. So, let's pour like a fourth. Okay. And then pour it in. Heat is off. And then torch it. Awesome. Great. All right. Okay, I think I got this. Okay, yeah. So, do you want to do it yourself? Yeah. So, pour it to like half of the fourth cup and then once you have that, I can give this to you. Perfect. Great. So, it's off. And then once that's off, you can turn it back on. Perfect. Okay. And then now, do you want to hold on this and just press this button to fire it up. Cool. Yeah, perfect. Great. Okay. I'm burning it. It's a little light, but yeah. Great. And then we can turn on the heat again. Okay. And then we'll just cook off the alcohol. Okay. Great. Great. Great. Great. How are you feeling? Basically there cooking everything. So Okay. Awesome.

</details>

**[主持人]**: 是的，我猜在研究想法和努力方向方面，你认为是否仍然有很多容易摘取的果实，或者可以通过优化已实现工作的小部分来大幅改进的想法？还是说现在人们必须承担很多全新的研究赌注？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, and I guess in terms of research ideas and what to work towards, do you think there's still a lot of low-hanging fruit or ideas that can still be improved a lot through just optimizing small parts of already implemented work or do you think right now there has to be a lot of research that are completely new bets that people take?

</details>

**[Mark Chen]**: 嗯，这是一个非常好的问题。我觉得有新的赌注，但可能没那么多。在某种意义上，希望你觉得AGI即将到来。我认为每个人都看到这些模型变得非常强大。如果你真的想象一下这意味着什么，我们正越来越接近一个模型可以提出更多创新的世界。如果它们能做**自我维持的研究**，这是为我们研究工作设定的主要目标之一。所以，我认为真正重要的是，在那个时间点之前是否存在大的赌注？我认为窗口很小，但仍然有一些非常重要的想法我们正在尝试。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Um yeah, that's a really great question. I feel like there are new bets, but probably not that many. In some sense, hopefully you feel like AGI is coming soon, right? And I think everyone sees that these models are getting really capable. I think if you really imagine the implications of that, we're getting closer and closer to a world where the models can come up with more of the innovation. If they can kind of do self-sustaining research, this is one of the big goals that we've set for our research work. And so, I think what really matters is are there big bets before that point in time? And I think the window is small, but there are still like some pretty significant ideas we're trying out.

</details>

**[主持人]**: 是的。有些研究员说过，要达到AGI，我们还需要，比如说，两三个突破，比如**持续学习**或其他想法。你认同这种观点吗？还是你认为没有那么戏剧性，不需要提出三个完全不同的范式？

<details>
<summary>Original English</summary>

**[Host]**: Yeah. I mean, there've been some researchers who have stated that to get to AGI, we still need, let's say like two or three more breakthroughs, if you like continual learning or some other ideas. Do you follow that same view perspective, or do you think it's kind of more so like not as drastic as coming up with like three completely different paradigms?

</details>

**[Mark Chen]**: 嗯，我不知道。我不确定我是否有同样的框架。持续学习是一个你必须解锁的基本原语。有这么多不同的技术。我们正在尝试它的很多局限性。我不知道什么才算突破，什么不算，但我认为我们有很多射门机会，而且我很确定它们会成功。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Um yeah, I mean, I don't know. I don't know if I have that same framing. Like continual learning is a basic primitive that you have to unlock. There's so many different techniques. I don't know what would consider as a breakthrough versus not, but I think there are clearly many shots on goal, and I'm pretty sure they'll work.

</details>

### 多模态与“氛围研究员”

**[主持人]**: 好的。虾基本好了。太棒了。好的，你想再做一次火焰烹饪来上色吗？我们来做吧。好的。把火开大一点，我再加点油。好的，因为你想让它颜色深一点。我觉得我的已经好了。给你。好的，然后我们希望能再来一次。完美。你想先来吗？同样的量。好的。我们希望能成功，因为我觉得火候不够。好的，我想我们放进去了。是的，好了。按下按钮。好了。成了。纹理不错。是的。确实。而且能增加一些好味道。来，我试试。会很好。好的，我们看看会是什么样子。哦。成了。好的。我们进入最后阶段了。虾都熟了。是的。有点火。所以，现在我们稍微煮一下，然后我们应该把蔬菜加到水里。我对你的多任务处理能力印象深刻。你知道，我认为这实际上是我们的模型需要改进的一个方面。它应该能够像这样处理一个线程，同时还能和你聊天。

<details>
<summary>Original English</summary>

**[Host]**: Great. Okay, so the shrimp is basically done. Awesome. Okay, so, do you want to do the flambé thing again to get more color? Let's do it. Okay. Turn on the heat a little bit, and then let me get some more oil. Great. Yeah, cuz you want to get like some dark color. I think mine has. And here. Great. And then we can hopefully get another shot. Okay. Perfect. Do you want to go first? Same amount. Okay. We could hopefully get cuz I think the heat wasn't as... Yeah. Okay. I think we put it in. Yeah. I think There we go. Let's press the button. Great. There we go. There it is. It's good texture. Yeah. Indeed. And it's like add some good flavor. Here, let me try it. It'll be good. Yep. Yeah, let's see. Great. All right, let's see what it's going to look like. Ooh. There it is. All right. But we're in the final stretch. Okay. shrimp all cooked. Yep. Some fire. So, now we can kind of cook it off a little bit and then we should add our veg to the water. I'm impressed by your multitasking abilities. You know, I think that's actually one thing we need our models to get better at. Like it should just be able to do some thread like this and also just have a conversation with you at the same time.

</details>

**[主持人]**: 是的，是的。这也提醒了我。你认为图像、音频、视频甚至文本，所有这些都应该在一个模型下，还是说会分裂成专门的模型，比如专门的音频模型？

<details>
<summary>Original English</summary>

**[Host]**: Yeah. Yeah. No, I That also reminds me. Do you think images and audio and video and even text like that should all be one under one model or do you think it'll like break through like specific specialized like audio model or...

</details>

**[Mark Chen]**: 嗯，是的。我认为对于一个研究实验室来说，将它们统一在一个模型下有很多优势。例如，你只需要维护一个**基础设施栈**。我认为同时维护和扩展多个基础设施栈的成本是不容低估的。所以，我认为有很多好处，你在核心栈上做一些基础研究，然后这可以延续到你想要的任何模态或任何东西。因此，我们强烈倾向于尽可能少地使用不同的架构。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Well, yeah. I mean, I think for a research lab, I think there are a lot of advantages for it to be under one. You just have to maintain one infrastructure stack for instance. I think the cost of maintaining and scaling many infrastructure stacks at once is something that you shouldn't underestimate. So, I think there are a lot of benefits to just like you do some core research in your fundamental stack and that just carries over to whatever modality or whatever thing that you want. So, I think there's a strong bias for us to keep it in as few different architectures as possible.

</details>

**[主持人]**: 明白了。是的，这很有道理。我认为架构本身也是一个经常不被考虑的因素。这非常重要。但我最近经常看到的一个词，你也提到过，是**“氛围研究员”**。你知道，我们显然有“氛围编码者”。但我猜关于“氛围研究”，你认为最终状态是什么？你认为“氛围研究员”的主要价值在于提出正确想法的研究品味，还是更多地在于执行，即跟进实际研究？

<details>
<summary>Original English</summary>

**[Host]**: Got you. Yep. Great. No, that makes a lot of sense. I think like the architecture as well is something that isn't often considered. It's very important. But one also term that I've been seeing a lot that you've also kind of mentioned is a vibe researcher. You know, we have vibe coders obviously. But I guess on vibe researching, what do you think is like the end state? Do you think the main value out of a vibe researcher is just the research taste of coming up with the right idea or do you think it's more so the execution of going through and following through on the actual research?

</details>

**[Mark Chen]**: 嗯，是的，我认为我们实际上正在非常快地走向这个世界。在OpenAI和其他实验室，你开始看到很多工作变得主要**以编排为中心**。研究员提出想法，而模型足够强大，可以自己完成实现和执行。所以，当谈到提出想法的价值与执行的价值时，两者仍然很重要，但我感觉市场正在转向能够提出大量想法，然后模型可以为你执行和编排。我认为这将是做研究的未来。我们之前也说过，模型还没有完全具备品味。这就是为什么你仍然需要研究员来提出想法。教模型好的品味会很难。我们注意到了这一点，但在实际加速研究方面，已经看到了明确、切实的好处。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Um yeah, so I think we're actually moving towards this world very quickly. Both at OpenAI and our other labs, you're starting to see a lot of the work become mostly orchestration-focused. The researchers coming up with the ideas and the model's great enough to do the implementation execution by itself. So, when it comes down to is the value of coming up with ideas versus execution? Both are still important, but I just feel like there's this market shift towards just being able to come up with a lot of ideas and then the model can actually do the execution and orchestration for you. So I think that's going to be the future of doing research. We also said earlier, the models don't quite have the taste yet. And that's why you still need the researchers coming up with the ideas. It's going to be hard to teach the models good taste. We noticed that, but in terms of actually accelerating the research, there's clear tangible benefits already.

</details>

**[主持人]**: 是的。你认为模型在研究品味上最终会达到与人类同等的水平吗？

<details>
<summary>Original English</summary>

**[Host]**: Yeah. Do you think they'll ever be parity in terms of research taste with models?

</details>

**[Mark Chen]**: 我认为会。当我们看我们大约三年的路线图时，我们想要达到的最终目标是模型能够进行**端到端的研究**。我认为这个问题的一部分就是让模型能够提出好的品味。你指向某个通用的基准测试或什么东西，它就能找到正确的解决方案。

<details>
<summary>Original English</summary>

**[Mark Chen]**: I think so. I mean, when we look at our kind of three-year roadmap, the end goal that we want to reach is one where the models are just doing end-to-end research. And I think a part of that problem is just being able to have the model come up with good taste. You point at some generic benchmark or something and it finds the right solutions.

</details>

### 失败的价值与最终品尝

**[主持人]**: 是的，这很有帮助。在OpenAI由人类完成的研究方面，你们是如何进行所谓的“事后复盘”的，比如一个研究赌注结果不好？因为我认为很多都是承担这些巨大的赌注，有些结果并不好。

<details>
<summary>Original English</summary>

**[Host]**: Yeah, no, that's helpful. And in terms of research done by humans at OpenAI, how do you guys go about the postmortem process of a research bet that didn't turn out well? Cuz I assume that a lot of it is taking these vast bets and some don't turn out well.

</details>

**[Mark Chen]**: 嗯，我认为这是OpenAI的**阿尔法**（优势）的重要组成部分，因为我认为我们与其他实验室的区别在于我们承担了很多**高风险赌注**。我认为这正是让我们能够如此持续地保持在前沿的原因。但这也意味着一些赌注不会成功。一个艰难的推论是，当一个赌注不成功时，你不能自欺欺人地认为它会成功，而必须与之脱钩。所以，你必须做出一些判断，比如回头看，然后说，“嗯，这个想法在当时很有希望，但实际上它没有我们想象的那么重要”，或者“有其他方法效果更好”，或者“我们发现了别的东西”。但我认为这些工作很多也是富有成果的。我们意识到，即使有时人们未能证明一项技术，他们的**书面总结**也非常重要，因为这通常是一个很自然的想法，也许可以避免很多人经历同样的痛苦。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Well, I would say that is a big part of OpenAI's alpha because I think one thing that differentiates us from other labs is we take a lot of high-risk bets. And I think that's what's allowed us to stay at the frontier so consistently over time. But it also means that some of the bets are not going to pan out. A hard corollary of that is when a bet doesn't pan out, you have to not delude yourself into thinking that this is something that will work and kind of disconnect from it. So, I think there are certain calls that you have to make, like look back and be like, "Well, this was a promising idea at the time, but actually it's less important than we thought," or "There's some other approach that works better," or "There's something that we discovered." But I think much of that work is also very fruitful. So, what we realized is even sometimes when people fail at proving out a technique, their write-ups are very important because it'll often be a natural idea and you can perhaps save a lot of people from going through the same pain.

</details>

**[主持人]**: 是的。这很有帮助。那么，当谈到这种对失败的积极看法时，你如何平衡一个研究员承担了很多连续赌注，但都没有成功的情况？因为我认为在某个时候，你会希望一个研究员最终能做出实际有益的贡献，而不是只承担那些可能结果不好的赌注。

<details>
<summary>Original English</summary>

**[Host]**: Yeah. Well, that's helpful. So, I guess when it comes to this positive view on failure, how do you balance that with a researcher who takes a lot of bets, consecutive bets, and none of them pan out? Cuz I assume at a certain point you'd want a researcher to eventually have contributions that are actually beneficial compared to only taking bets that maybe pan out to being not good space.

</details>

**[Mark Chen]**: 通过经验，我确实见过一些人陷入这种情况。但我也遇到过几个案例，一个接一个的赌注都不成功，就在你快要绝望的时候，你突然有了一个**巨大的成功**。这种情况发生得足够多，所以这真的取决于想法本身是否**合理**。它们可以很雄心勃勃，但仍然必须是合理的。有一种人就是会承担很多这样的想法，这没关系，因为他们处于风险较高的前沿。但他们只需要偶尔证明一次，就能让一切变得合理。这可能是一种非常交易式的世界观，但这就是我们的期望，他们需要增加价值。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Just through experience, I've definitely seen some people fall into this. But I've also had several cases where it's just like bet after bet, it doesn't pan out, and just when you're at the brink of frustration, you have something that's like a mega hit. And this happened enough, so it really just depends on are the ideas themselves sound? They could be ambitious, but they still have to be sound. And there's a certain kind of person who will just take a lot of those ideas, and it's okay because they're somewhat on the riskier frontier. But, they only have to justify it once in a while for it to make sense, right? It may be like a very trading like kind of lens on the world, but it's just on our expectation, they need to add value.

</details>

**[主持人]**: 是的，这很好。好的，我们基本上组装好了，现在是最后的润色。你可以尝尝你的汤，如果不够咸，我们就加酱油，如果太咸，我们可以加点水来稀释。但是，让我们看看我们的最终作品。味道怎么样？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, no, that's great. Okay, so we're basically assembled, now it's the finishing touches, so you can taste your soup, and then we just add soy sauce if it's not salty enough, and if it's too salty, we can add some water to lower this down. But, let's see our final creation. How is it?

</details>

**[Mark Chen]**: 相当不错。

<details>
<summary>Original English</summary>

**[Mark Chen]**: It's pretty good.

</details>

**[主持人]**: 好吗？

<details>
<summary>Original English</summary>

**[Host]**: Good?

</details>

**[Mark Chen]**: 我接受。我的不错。

<details>
<summary>Original English</summary>

**[Mark Chen]**: I'll take it. Mine is good.

</details>

**[主持人]**: 是的，我的需要加点水。你能把水递给我吗？当然。好的，感觉怎么样？

<details>
<summary>Original English</summary>

**[Host]**: Yeah, mine needs a little bit of water. Could you pass me the water? yeah, absolutely. Great. So, how was that? How did that feel?

</details>

**[Mark Chen]**: 嗯，我觉得这是一次**学生蒸馏**。你显然比我做得好。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Um I think this is a student distillation. You're clearly better than I am at this.

</details>

**[主持人]**: 不，不，不。我觉得你做得很好，尤其是虾和棕榈心。闻起来很棒。哇，好的，听起来不错。我猜更广泛地说，我有点好奇，有没有你认为目前被高估和被低估的研究或话题？你会怎么归类？

<details>
<summary>Original English</summary>

**[Host]**: No, no, no. I feel like you did a very good job, especially with even with the shrimp and palm hearts. Yeah. Smells great. Wow, okay, that sounds good. I guess just more generally, I'm kind of curious, are there any reason research or topics that you think are right now overrated and underrated? Like what would you categorize under?

</details>

**[Mark Chen]**: 嗯，如果你仍然持有“预训练已死”的世界观，那么我认为预训练绝对没有被低估。它没有被低估。它被低估了。而且，老实说，我认为**产品**和思考最终用途，以及如何将你在研究中构建的所有原语与现实世界中的**智能体用例**联系起来，这也是被低估的。你真的不能在一个真空中构建所有东西而不将其与实用性联系起来。

<details>
<summary>Original English</summary>

**[Mark Chen]**: Well, I think if you still have a pre-training is dead view of the world, I think pre-training is definitely not dead. It's underrated. And honestly, I think products and kind of thinking about end uses and how you tie all the primitives you build in research to real agentic use cases in the world. That's also underrated. I think you really can't just kind of build everything in a vacuum and not connect things to utility.

</details>

**[主持人]**: 是的，这很好。太棒了。我想我们准备好品尝了。我们试试吧？我们可以把这个移开，我觉得应该摆盘。是的，你想把这个盘子拿到这边来吗？好的。虾看起来很棒。但其他东西都在这里。好的。然后我们可以用这些锅。我们有虾。你想尝尝吗？干杯。干杯。我们看看。可能有点甜。有点太甜了。因为我们找到了弥补的方法。对我来说，我喜欢甜的东西。不错。好的，很好。Sean，你想来尝尝我们的松露汤吗？顺便说一句，刚才那太好了。你们闻不到，但是……我们假装你是一个想升职的研究员。我是Zach，他试图让你……所以你想拿那边的勺子吗？汤真的会左右这里的决定。汤的质量。好的。我来。好的。这里的艺术方向是什么？嗯，艺术方向。是模仿。我认为模仿中有伟大的艺术。是的，就让他们自由发挥吧。好的。哇，是的。味道浓郁。我的意思是，我绝对喜欢咸味和辣味结合在一起，然后还有那种海鲜味。是的，真的很入味。好的。我的味道非常突出。赢家还是什么？不，不，不。你应该尝尝然后……不，你来选赢家。好的。这就像评估？是的。所以，它很贵。外部评估。好的，我得说，我觉得这里面水太多了。我觉得……我也觉得是锅的问题。因为这是个很大的锅。是的。等等，好的。嗯，我得选这个。好的。就像你是我们尊敬的客人，但我想客观一点。当然。当然。是的。是的。是的。嗯，我觉得浓度真的……味道真的……我放一半水？一半的水？可能吧。好的，听起来不错。我的意思是，我认为这很个人化，对吧？是的，我认为这也很个人化。品味，你知道，你提到了……你经常做饭。品味。不。不。不。好的，我知道几个食谱。我严格照着做。如果你告诉我，“哦，做点稍微不同的东西。”我完全不知道。我完全迷失了。是的。有忙碌的烹饪。GPT可以告诉你。嗯，是的。哦，我不撒谎。我查过ChatGPT几次。所以对你来说，就像，“哦，只是准备。”但没关系。但很高兴你能来。我觉得你一直在用很多研究品味引领这个领域，看到你的工作很棒。希望这很有趣。是的，非常有趣。非常感谢。

<details>
<summary>Original English</summary>

**[Host]**: Yeah. No, that's great. Awesome. I think we are ready to taste. So, do we want to give it a go? Let's do it. We can move this and I think there should be some plating. Yeah, do you want to take this plate over here? Okay. Okay. Shrimp looks great. But everything else is here. Great. And then we could just use these pots. So, we have our shrimp. Yep. Do you want to try it? Cheers. Cheers. Let's see. Maybe a little sweet. That's a little too sweet. Cuz we found a way to make it up. for me. I like sweet things. It's good. Okay, great. Sean, do you want to come and taste our truffle soup? That was so good by the way. You guys can't smell it, but um... We'll pretend you're a researcher that's trying to get a promotion. And I'm Zach and he's trying to get you so do you want to grab the spoon over here? soup is really going to sway the decision here. The soup quality of soup. Yeah. Great. I'll do it. All right. What was the artistic direction here? Um artistic direction. Well, it was mimicry. I think there's great art in mimicry. Yeah. Just letting them cook. Mhm. Good. Wow. Yeah. Strong. I mean, I think one thing I definitely like like savory and spice that goes together, but then also like the sort of sea seafoodness. Mhm. Um... Yeah. Kind of really goes into it. Great. Okay. Mine's mine's very dominant. winner or what? No, no, no. You're supposed to try it and then... No, you do pick a winner. Okay. This is like evals? Yes. Yeah. So, it's expensive. External evals. Okay, I got to say I feel like there's too much water in this. I think like the the... I think it's also a pot. Cuz this is a big pot. Yeah. Wait, okay. Um I would say I have to go for this. Okay. Okay. Just like you're our respected guest, but I want to be objective. Of course. Of course. Yes. Yes. Yes. Um and like yeah, the density I think really a flavor really... I'll do half water? Half the water? Probably. Okay. That sounds good. I mean I think it's very personal, right? Yeah, I think it's also very personal. Taste, you know, you were mentioning... You do a lot of cooking. Taste. No. No. No. Okay. I know a couple recipes. I follow them to the T. I can't Like if you tell me, "Oh, cook something slightly different." I have no idea. I'm completely lost. Right. Right. Yeah. There's busy cooking. GPT can tell you. Mhm. Yeah. Yeah. Oh, I'm not going to lie. I kind of looked up in ChatGPT a couple of times. So for you, it's like, "Oh, just as prep." But No worries. But yeah. It was great having you. I feel like you're always leading the field with a lot of research taste as well, and it's great seeing your work. So hopefully It was fun. Yeah, a lot of fun. Thank you so much.

</details>