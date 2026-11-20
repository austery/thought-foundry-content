---
author: Veritasium
date: '2026-11-18'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=uXuQF_PPg5U
speaker: Veritasium
tags:
  - random-number-generator
  - pseudorandomness
  - quantum-entanglement
  - bell-test
  - monte-carlo-method
title: 真随机为何近乎不可能：从赌博机破解到量子纠缠随机数
summary: 视频探讨了真随机数生成的极高难度。从早期核武器研发中的蒙特卡洛模拟，到线性同余生成器与梅森旋转算法的可预测性缺陷及其在游戏与赌场中的漏洞利用，再到加密级伪随机；最终介绍了美国国家标准与技术研究院如何利用量子纠缠与贝尔测试，提纯出经数学认证的真正不可预测性。
insight: ''
draft: true
series: ''
category: science
area: knowledge-meta
project: []
people:
  - Stanislaw Ulam
  - John von Neumann
  - Matthew Bolan
  - David Kaiser
  - Pierre-Simon Laplace
  - Albert Einstein
companies_orgs:
  - Los Alamos
  - IBM
  - Cloudflare
  - National Institute of Standards and Technology
  - University of Colorado Boulder
products_models:
  - ENIAC
  - Minecraft
media_books: []
status: evergreen
---
### 赌场里的异常赢家

在圣路易斯的 Lumière Place 赌场，一名男子举着手机对着一台老虎机，记录下屏幕上的每一次旋转。他玩了几轮，有赢有输，然后起身上前走开了。五分钟后，他又回到同一台机器前继续玩，但这一次，他几乎次次旋转都在赢钱。

赌博不到一个小时，他带着大约 10,000 美元的收益走出了赌场。
<details>
<summary>Original English</summary>
- At the Lumière Place
Casino in St. Louis,
a man holds his phone
up to a slot machine,
and he records the spins on the screen.
He played a few rounds.
He won some, lost some,
and then he got up and walked away.
Five minutes later,
he was back playing the same machine,
but now he was winning on spin after spin.
(machine chiming)
(coins clattering)
After less than an hour of gambling,
he walked out of the casino
roughly $10,000 richer.
(dramatic music)
</details>

在密苏里州、伊利诺伊州和加利福尼亚州的至少 10 家赌场中，同样的事情接连发生。赌客们会在一台老虎机前玩上一会儿，然后离开，几分钟后返回并开始赢钱。调查人员介入调查，但当他们检查这些老虎机时，机器看起来全部运转正常。

于是他们把注意力转向监控录像，并发现了一些诡异之处。这些玩家回来后，下注方式与普通赌徒截然不同。他们会把手悬停在旋转按钮上方等待，然后在一个极其特定的瞬间按下去，仿佛他们知道什么时候按下去就能赢。
<details>
<summary>Original English</summary>
At least 10 casinos across
Missouri, Illinois, and California
saw the same thing.
Gamblers would play on a
slot machine for a while
and then leave, and minutes later,
they would return and start winning.
Investigators were brought in,
but when they examined the slot machines,
they all seemed to be working fine.
So they turned their attention
to the security footage,
and they noticed something strange.
When these players came back,
they didn't play like normal gamblers.
They'd hover their hand
over the spin button, wait,
and then press at oddly specific moments
as if they knew when to press to win.
</details>

也许这说得通。或许真有某种方法可以预测接下来会出现什么，因为那些转轮的结果实际上是由机器内部的一台计算机决定的。赌博固然是个糟糕的主意，但赌场为研究随机性提供了一个理想的场所，因为从理论上讲，那台计算机在每次旋转时都会使用一个随机数。

那么，那些数字真的是随机的吗？

这个看似简单的问题，事实证明与在《我的世界》（Minecraft）中寻找钻石、第一批核武器的研制，乃至整个数字世界的安全性都紧密相连。这是一个关于创造真正随机性近乎不可能的视频。
<details>
<summary>Original English</summary>
And maybe that makes sense.
Perhaps there's some way to
predict what was coming next
because the outcomes of
those spinning wheels
are actually decided by a
computer inside the machine.
Now gambling is a terrible idea,
but the casino provides an ideal venue
for investigating randomness,
because theoretically, that computer
uses a random number for every spin.
So are those numbers actually random?
Well, that seemingly simple question
turns out to connect finding
diamonds in Minecraft,
to the development of the
first nuclear weapons,
to the security of the
entire digital world.
This is a video about
the near impossibility
of creating true randomness.
</details>

### 核武器研发与蒙特卡洛方法

早在 20 世纪 40 年代，物理学家就发现概率在核弹内部发生的过程中扮演着极其重要的角色。其原理大致如下：以一个铀-235 核心为例，当中子击中 U-235 原子核时，会引发原子核裂变，从而释放出能量以及大约两到三个额外的中子。如果平均每次裂变能引发一次以上的后续裂变，就会产生失控的链式反应。

但这是否会发生，取决于那些中子所走的路径。每个中子在击中原子核前能移动多远？它是弹开、被吸收，还是会引发另一次裂变？到 1945 年，在洛斯阿拉莫斯工作的科学家们已经测算出了这些事件各自发生的几率，但这些几率会根据中子的速度及其穿过的物质等条件而发生变化。面对数以万亿计的中子，可能性实在太多，根本无法逐一进行计算。
<details>
<summary>Original English</summary>
Back in the 1940s,
physicists discovered that chance
plays a surprisingly important role
in what happens inside a nuclear bomb.
It works something like this.
Take a core of uranium-235.
When a neutron hits a U-235 nucleus,
it can cause the nucleus to split,
which releases energy
and around two or three more neutrons.
Now, if on average each split triggers
more than one more split,
you get a runaway chain reaction.
(explosion roars)
(ground rumbling)
But whether that happens
depends on the path those neutrons take.
How far does each one travel
before it hits a nucleus,
or does it bounce off, or get absorbed,
or does it cause another to split?
By 1945, scientists working at Los Alamos
had measured the odds of each
of these events happening,
but those odds changed
depending on things like
the neutron's speed and
what it was passing through.
And across trillions and
trillions of neutrons,
there were far too many possibilities
to calculate one by one.
(dramatic music)
</details>

当时致力于解决这个问题的数学家之一是斯塔尼斯瓦夫·乌拉姆（Stanislaw Ulam）。但在 1946 年 1 月的一个早晨，乌拉姆醒来后无法说话。那是脑炎，一种几乎要了他命的脑部炎症。幸运的是他活了下来，但康复过程十分缓慢。于是他在医院里度过了数周，玩了大量的单人纸牌游戏，并且开始琢磨：“赢下一局游戏的几率有多大？”

起初，这听起来可能像个简单的问题，但一副 52 张的扑克牌有 52 的阶乘种洗牌方式，也就是大约 8 乘以 10 的 67 次方种不同的排列。而这里的每一种洗法所展开的游戏过程都截然不同。乌拉姆花了很多时间试图用解析法算出答案，却一无所获。
<details>
<summary>Original English</summary>
One of the mathematicians
working on this problem
was Stanislaw Ulam.
But then one morning in January 1946,
Ulam woke up and couldn't speak.
It was encephalitis,
an inflammation of the brain
that nearly killed him.
Luckily, he survived,
but his recovery was slow.
So he spent weeks in a hospital playing
a lot of solitaire,
and he started to wonder,
"What are the chances of winning a game?"
(light curious music)
Now, at first, that might
sound like a simple question,
but a deck of 52 cards can be
shuffled in 52 factorial ways,
and that's about 8 times
10 to the power of 67
different arrangements.
And every one of those shuffles
is going to play out differently.
Now, Ulam spent a lot of
time trying to work out
the answer to his question analytically,
and he got nowhere.
</details>

随后他想到了一个简单得多的点子：“我琢磨着，更实用的方法会不会是把它排开，比方说 100 次，然后直接观察并统计获胜局数的数量。”这能为他提供答案的某种统计近似。假设你在 100 局中赢了 8 局，那么你整体的获胜几率可能就在 8% 左右。

就在那一刻，乌拉姆意识到他可以将完全相同的想法应用于中子。因此，他无需尝试计算每条可能的路径，只需从 100 个中子开始，利用随机数去模拟每一个中子会发生什么。
<details>
<summary>Original English</summary>
But then he had a much simpler idea.
"I wondered whether a
more practical method
"might not be to lay
it out, say, 100 times
"and simply observe and count the number
"of successful plays."
That would give him some sort of
statistical approximation of the answer.
So say you win 8 games out of a 100.
Well, then your overall chances of winning
are probably around 8%.
And that's when Ulam realized
he could use exactly the same idea,
but for neutrons.
</details>

假设一个中子击中了一个原子。如果我掷出 1、2 或 3，它会从原子核上弹开；如果掷出 4 或 5，它会引发原子核裂变；如果掷出 6，它就会被吸收。接着，我只需用更多的随机数跟踪该中子及其产生的任何其他中子的后续情况，以此决定它们的命运。

这只是一些作为例子的几率。在真实的模拟中，科学家们使用的是他们已测出的概率，来决定哪些随机数对应哪些结果。在每次相互作用之后，中子的速度或方向也可能发生变化，因此在下一步中，他们会采用对应新情况的概率，再使用一个随机数，继续追踪后续发展。通过重复这一过程，他们可以观察所有这些相互作用累加起来的结果。如果中子数量持续增长，链式反应就会爆发；但如果损失的中子多于产生的中子，反应就会逐渐平息。

因此，仅通过模拟所有可能路径中极小的一部分，乌拉姆就能估算整个核链式反应的表现模式。
<details>
<summary>Original English</summary>
So instead of trying to calculate
every possible path,
he could just start
with a hundred neutrons
and use random numbers to simulate
what would happen to each of them.
So say a neutron hits an atom.
If I roll a one, a two, or a three,
it bounces off the nucleus.
If I roll a four or a five,
it causes the nucleus to split.
And if I roll a six, it gets absorbed.
And then I just follow what
happens to that neutron
and any other neutrons that it produces
using more random numbers,
and that will decide their fate.
Now those are just example odds.
In the real simulations,
the scientists used probabilities
they had already measured to decide
which random numbers corresponded
to which outcomes.
And after each interaction,
the neutron's speed
or direction could also change.
So for the next step,
they'd used the probabilities
for its new situation.
So use another random number,
and then they kept
following what happened.
And by repeating this process,
they could see how all
those interactions added up.
If the number of neutrons keeps growing,
the chain reaction takes off.
But if more are lost than are produced,
it fizzles out.
So by simulating just a tiny
fraction of the possible paths,
Ulam could estimate how an
entire nuclear chain reaction
would behave.
</details>

### ENIAC 与平方取中法

但是靠人工完成所有这些计算似乎是不可能的。幸运的是，同为数学家兼洛斯阿拉莫斯顾问的约翰·冯·诺依曼（John von Neumann）一直在使用世界上最早的电子计算机之一——ENIAC。在 1947 年 3 月，他推导出了如何让计算机在短短 5 个小时内跟踪 100 个中子及其后代经历成千上万次碰撞的过程。

但 ENIAC 无法通过掷骰子来决定中子会遭遇什么。当时，研究人员需要随机数时，会使用像这样的随机数字表书籍。而且 ENIAC 也没有足够的内存来存储它所需要的全部随机数。因此，冯·诺依曼想出了一种惊人简单的方法，让 ENIAC 自己生成随机数。
<details>
<summary>Original English</summary>
But doing all of these
calculations by hand
seemed impossible.
Luckily, fellow mathematician
and Los Alamos advisor John von Neumann
had been working with one of the world's
first electronic computers, the ENIAC.
In March 1947,
he worked out how it
could follow 100 neutrons
and their descendants through thousands
of collisions in just five hours.
But the ENIAC couldn't roll a die
to decide what would happen to a neutron.
At the time,
when researchers needed random numbers,
they used books of random
digits like this one.
And the ENIAC didn't
have nearly enough memory
to store all the random
numbers it would need either.
So von Neumann came up with
a surprisingly simple way
for the ENIAC to generate
its own random numbers.
</details>

假设我想生成一组四位随机数。我们的做法是，先选择一个数字作为起点，这被称为“种子”（seed）。比如我们试试 2,137。接下来要做的是对它进行平方，2,137 的平方是 4,566,769。现在我要取这个数字中间的四位数，但在此之前，我必须在最前面加一个 0，因为起初我们得到的是一个七位数。

我不会使用边缘的数字，因为它们的可预测性更高。最后两位数仅取决于种子的末尾，因为 37 的平方以 1,369 结尾。因此，任何以 37 结尾的数，其平方都会以 69 结尾。这就是为什么我们要舍弃这里的这几个数字。同样，2,100 多范围内的每个种子平方后都在 440 万到 490 万之间，因此它们都以 0 和 4 开头，所以这部分也可以舍弃。

但是中间的数字会受到种子中每个数字的影响。因此，5,667 将成为序列中的下一个数。如果我们对其进行平方，得到 32,114,889。现在我忽略两端的各两位数，这样你就可以一直继续下去。
<details>
<summary>Original English</summary>
Let's say I want to generate
a bunch of random four digit numbers.
So the way we're going to do this
is I'm actually going to
start by choosing one,
which is called the seed.
So let's try with 2,137.
So what I'm going to do next is square it,
and 2,137 squared is 4,566,769.
Now I'm going to take the four
middle digits of this number,
but to do that first,
I have to add a zero to the front
because we initially had
a seven digit number.
I won't use the digits at the edges
because they're actually more predictable.
So the last two digits
only depend on the end of the seed
because 37 squared ends in 1,369.
So anything ending in 37,
squares to something ending in 69.
So that's why we get
rid of these guys here.
Also, every seed in the
2,100s is going to square
to somewhere between 4.4 and 4.9 million.
So they all start with a zero and a four,
so we can get rid of that too.
But the middle digits get a contribution
from every digit in the seed.
So 5,667 is going to be the
next number in the sequence.
So if we square that, we get 32,114,889.
Now I disregard the two
digits at either end,
and you can just keep going.
(upbeat music)
</details>

看着这些数字，并没有明显的规律，但注意看如果我继续算下去会发生什么。从 2,137 开始，经过 43 步后，我得到了 4,100，然后是 8,100，再然后是 6,100，接着是 2,100，然后又是 4,100。序列陷入了这个循环之中。

从这里开始，生成器将一遍又一遍、永久地生成这四个相同的数字，而几乎三分之二的四位种子最终都会落入完全相同的循环中。其他种子则会以 0 告终，而一旦落到 0，之后跟随的每个数字也都是 0。近五分之一的起始值最终都会走向这里。事实上，如果你尝试所有可能的四位起始值，每一个序列最终都会卡在仅有的八个陷阱之一中。
<details>
<summary>Original English</summary>
Looking at these numbers,
there's no obvious pattern,
but watch what happens if I keep going.
Starting from 2,137,
after 43 steps, I get 4,100,
then 8,100,
and then 6,100,
and then 2,100,
and then 4,100 again.
The sequence gets stuck in this loop.
From here on, the generator will produce
these same four numbers
over and over forever,
and nearly two-thirds
of all four digit seeds
end up in this exact loop.
(dramatic music)
Others end up at zero,
and once they do every number
that follows is also zero.
Almost one in five starting
values end up here.
In fact, if you try every possible
four digit starting value,
every single sequence
eventually gets stuck
in one of just eight traps.
</details>

冯·诺依曼深知这些陷阱是一个严重的问题。因此在 ENIAC 的第一次模拟中，团队实际上使用了八位数而不是四位数，以便在陷入循环前生成更长的序列。他们还手动对前 2,000 个数字进行了随机性的统计检验。接着，为了避免遭遇意外循环的风险，他们将 ENIAC 编程为在运行完这 2,000 个数字后，直接从原始种子重新开始。

1948 年春天，ENIAC 终于运行了人类历史上第一批由计算机执行的中子行为模拟。冯·诺依曼在给乌拉姆的信中写道：“结果非常喜人，该方法显然取得了 100% 的成功。”

这种方法后来被称为蒙特卡洛方法，得名于摩纳哥的蒙特卡洛，因为乌拉姆的一位叔叔喜欢在那里赌博。如今，它已成为统计学和科学计算中最重要的工具之一。
<details>
<summary>Original English</summary>
Now, von Neumann knew that these traps
were a serious problem.
So for the first ENIAC simulation,
the team actually used eight
digit numbers, not four,
so they produced much longer
sequences before they looped.
They also statistically
tested the first 2,000 numbers
for randomness by hand.
Then rather than risk running
into an unexpected loop,
they programmed the ENIAC to
restart from the original seed
after it had got through
these 2,000 numbers.
And in the spring of 1948,
the ENIAC finally ran the first
computerized simulations
of neutron behavior.
Von Neumann wrote to Ulam,
"The results are very promising,
"and the method is
clearly a 100% success."
The approach became known
as the Monte Carlo method,
named after Monte Carlo, Monaco,
where Ulam's uncle liked to gamble.
Today, it's one of the
most important tools
in statistics and scientific computing.
</details>

### 伪随机数的三大缺陷

不过，这串数字并不是真正的随机。如果你以相同的种子开始，每次都会得到完全相同的序列。因此它们被称为“伪随机数”（pseudorandom numbers），但这并没有妨碍它们的实用价值。随着蒙特卡洛方法传播到洛斯阿拉莫斯之外，对伪随机数的需求也随之扩散。

尽管如此，正如冯·诺依曼所开的玩笑：“任何考虑用算术方法生成随机数字的人，当然都处于一种有罪的状态。”因为伪随机数伴随着三大主要挑战：
第一，序列可能会陷入这种简短的循环；
第二，即便看起来随机的序列也可能潜藏模式；
第三，如果有人知道了种子，他们就能推导出随后的每一个数字——它们是可预测的。
<details>
<summary>Original English</summary>
Now, this sequence of
numbers isn't truly random.
If you start with the same seed,
you get exactly the same
sequence every time.
So they're called pseudorandom numbers,
but that didn't actually
stop them from being useful.
As Monte Carlo spread beyond Los Alamos,
so did this demand for
pseudorandom numbers.
Still, as von Neumann joked,
"Anyone who considers arithmetical methods
"of producing random digits is, of course,
"in a state of sin."
Because pseudorandom numbers
came with three major challenges.
One, sequences could get
stuck in these short loops.
Two, even sequences that looked
random could hide patterns.
And three, if someone knew the seed,
they could work out every
number that followed.
They were predictable.
</details>

### 《我的世界》与线性同余生成器

>> 所以，你得教我怎么找到这些钻石了。
>> 行。走吧。
>> 这位是马修·博兰（Matthew Bolan），《我的世界》专家兼多伦多大学数学系三年级博士生。
好，那我就跟着你走了，先生。如果你以前没玩过《我的世界》，钻石可是件大事。我不知道我有没有做过一整套钻石装备。
>> 我们今天就来改变这一点。
>> 每一个《我的世界》世界都是由区块（chunks）构成的。它们是在 X 方向上宽 16 个方块、Z 方向上宽 16 个方块的区域。在我们玩的这个版本中，每个区块在地下某处最多只会生成单单一矿脉的钻石矿石。
<details>
<summary>Original English</summary>
- So, you got to show me how
we get these diamonds then.
- Yeah. All right.
- This is Matthew Bolan,
Minecraft expert and
third-year PhD student
in Mathematics at the
University of Toronto.
Well, I shall follow you, sir.
If you haven't played Minecraft before,
diamonds are a big deal.
I don't know if I've ever
made a full diamond set.
- We're going to change that today.
- Every Minecraft world
is made up of chunks.
They're segments 16 blocks
wide in the X direction
and 16 blocks in the Z direction.
And in our version, each chunk originates
at most a single vein of diamond ore
that is hidden somewhere
below the surface.
(bright music)
</details>

>> 好的，那我们要找什么？
>> 我们要找粘土块或者沙砾堆。你要做的是打开 F3 调试屏幕，确定哪个方向是 Z 轴正方向。在这个例子中是这边。对于粘土，你要加 3。这是中心，我们朝 Z 轴正方向数一、二、三。现在如果我们在下面挖掘，除非被基岩之类的东西挡住，或者下面正好有个空洞导致无法生成，否则在这个方块的正下方一定会有钻石矿石。
>> 我们来试试看。
>> 好的。
>> 哇，不可能吧！
>> 你挖到了吗？
>> 挖到了。我拿到了 8 块。
>> 拿到 8 块了！漂亮！
>> 我拿到 8 块了。哇，我发财了。谢谢你，马修。
>> 好的，好的。
<details>
<summary>Original English</summary>
Okay, so what are we looking for?
- So we are looking for either
a clay patch or a gravel patch.
What you do is you pull up your F3 screen.
You locate which direction is positive Z.
So in this case, that's this way.
And what you do for clay, you add three.
So here, this was the center,
and we go one, two,
three in the positive Z.
And now, if we dig down here,
unless it got blocked
by bedrock or something,
or there's like a cave down there
where it couldn't spawn in,
there will be diamond
ore under this block.
- Let's give it a shot.
- All right.
- Oh, no way.
- Did you get anything?
- I did. I got eight.
- You got eight! Let's go!
- I got eight. Oh, I'm a rich man.
Thank you, Matthew.
- Okay, okay.
</details>

在我们玩的这个版本的《我的世界》中，游戏使用一种算法生成伪随机数，以此决定粘土和钻石等资源的出现位置。其原理大致如下：

假设拿一个有 7 个位置的轮盘，标有从 0 到 6 的数字。我们要做的，是从 1 开始，然后乘以某个数字。在这个例子中设为 3。1 乘以 3 得 3，所以我们将指针移到 3。现在我们再把 3 乘以 3，得到 9；但这个轮盘上只有 7 个位置，所以我们必须绕圈回绕。本质上，我们做的是将 9 除以 7，得出余数为 2。因此我们绕回圈内，移到 2。这种绕圈回绕的模式被称为模运算（modular arithmetic），或者简称为 mod。

现在我们继续：2 乘以 3 是 6，移动到 6；6 乘以 3 是 18，18 除以 7 得 2 余 4，所以走到 4；4 乘以 3 是 12，除以 7 的余数是 5；5 乘以 3 是 15，除以 7 的余数是 1。这样一来，我们在开始重复之前，遍历了除 0 以外的每一个数字。
<details>
<summary>Original English</summary>
- In this version of
Minecraft we're playing,
the game uses an algorithm to generate
the pseudorandom numbers that determine
where resources like
clay and diamonds appear.
It works something like this.
So I'm going to take a
wheel with seven positions.
It has numbers going
from zero through to six.
And what we're going to
do is we'll start at one
and then multiply by some number.
In this case, say three.
So one times three gives us three,
so we move the arrow to three.
Now, we multiply three by
three again and we get nine,
but there are only seven
positions on this wheel,
so we're going to have to wrap around.
Essentially, what we're doing
is dividing nine by seven,
and that gives us a remainder of two.
So we're going to wrap
around and go to two.
This kind of wrapping-around pattern
is called modular arithmetic, or just mod.
And now we keep going.
So two times three is six.
So we move to six.
And then 6 times 3 is 18.
If you divide 18 by 7,
you get two with the remainder of four.
So we get to four.
Four times 3 is 12.
The remainder after
dividing by seven is five.
Five times 3 is 15.
And the remainder after
dividing by seven is one.
So what we've done is we've
gone through every number
except for zero before
we started to repeat.
</details>

这种算法的公式看起来像这样。在当前数字与下一个数字之间存在简单的线性关系，但模运算步骤仅保留除以 M 后的余数。因此，数值并非沿一条直线向上延伸，而是回绕落下，分布在这些平行的对角线上。这是一种结合了模运算（也称为同余）的线性规则。

因此，这类伪随机数生成器得名为“线性同余生成器”，通常缩写为 LCG（Linear Congruential Generators）。

使用更大的数值时，LCG 可以在重复前生成极其漫长的数字序列。20 世纪 60 年代，IBM 开发了一个名为 RANDU 的生成器，它被内置在 IBM 的科学软件中，用于从放射性衰变到 NASA 天空实验室（Skylab）空间站机载仪器的各种模拟。RANDU 在重复前可以生成超过 5 亿个数字，因此至少解决了一个问题。
<details>
<summary>Original English</summary>
The formula for this kind of
algorithm looks like this.
There's a simple linear relationship
between the current number and the next,
but the mod step keeps only the remainder
after dividing by M.
So instead of continuing
up one straight line,
the values wrap around,
falling along these parallel diagonals.
So it is a linear rule
using modular arithmetic,
also called congruences.
So, these kinds of
pseudorandom number generators
got the name linear
congruential generators,
better known as LCGs.
With much larger numbers,
LCGs can produce enormously long
sequences of numbers before they repeat.
In the 1960s,
IBM developed one called RANDU.
It was included in IBM's
scientific software
and used in simulations of
everything from radioactive decay
to instruments aboard
NASA's Skylab space station.
And RANDU could generate over
half a billion numbers before repeating,
so at least that was
one problem dealt with.
</details>

但序列长并不一定代表质量好。看看如果我们将每三个连续数字作为三维空间中的坐标绘制出来会发生什么。如果这些数字表现得相互独立，我们会预期这些点像模糊的云团一样充满整个立方体。从这个角度看，它们确实似乎是这样分布的，从大多数角度看也是如此。

但如果你恰到好处地旋转这个立方体，就会发现它们实际上整齐地排列在穿过立方体的 15 个平面上。其中存在巨大的空隙，RANDU 永远不会在其中放置任何点。事实证明，由于那种线性关系的存在，这是所有 LCG 都无法避免的特征。第二个数字由第一个数字计算得出，第三个数字又按照完全相同的规则由第二个数字计算得出，因此这三个数字都被同一个线性方程联系在一起。在三维空间中，线性方程描述的是一个平面，而取模步骤则创建了一系列平行平面。

RANDU 对参数的具体选择让这种模式显得格外刺眼，但其他 LCG 在这方面的表现要好得多。在 20 世纪 90 年代，Java 采用了一种加入常数项的生成器，使用了更好的乘数和更大的模数。它的序列在重复前需要经历超过 281 万亿步。如果我们用同样的方式绘制其输出结果，就会得到这样一幅图。虽然这些平面实际上依然存在，但我们看不出来了，因为它们紧密地贴在一起，使得这些点大致呈现为一团随机的云。至此，第二个问题得到了解决。
<details>
<summary>Original English</summary>
But a long sequence doesn't
necessarily mean a good one.
Take a look at what happens if we take
every three consecutive numbers
and we plot them as coordinates
in three-dimensional space, right?
If the numbers behaved independently,
we'd expect the points to fill the cube
kind of in a fuzzy cloud.
And from this angle,
they certainly seem to,
and from most angles they do.
But if you rotate the cube
in just the right way,
you can see that they actually line up
in these 15 rows throughout the cube.
There are enormous gaps where
RANDU will never place a point,
and it turns out that that is just
an unavoidable feature of all LCGs
because of that linear relationship.
The second number is
calculated from the first
and the third from the second
using exactly the same rule.
So all three numbers are
linked by a linear equation.
And in three dimensions,
a linear equation describes a plane,
and the mod step creates a
series of parallel planes.
RANDU's particular choice of numbers
made that pattern especially obvious,
but other LCGs are much better at this.
In the 1990s, Java adopted
one that adds a constant
using a better multiplier
and a much larger modulus.
Its sequence takes over 281
trillion steps before repeating.
We can also plot its outputs the same way,
and what we get is this.
Now the planes are actually still there,
but we can't see them
because they're so closely packed together
that the points more or less
look like a random cloud.
So that is problem two dealt with.
</details>

>> （吸气）
>> 兄弟。
>> 职业风险。
>> 这个版本的《我的世界》是用 Java 编写的。因此在游戏历史的大部分时间里，它都使用 Java 的 LCG 来确定给定区块中资源的分布位置。但在生成不同资源时，《我的世界》并没有使用完全独立的起始数字。相反，它采用了相同的底层种子，并为每种资源加上不同的固定数值。对于钻石和河流粘土，这两个起始数字仅仅相差 3。

Java 随后在使用这些种子前对其进行了修改，因此差值不再总是 3，但在大多数世界中，它都会落入少数几个可预测的数值之一。由于它们经过了相同的 LCG 处理，用来选择它们位置的数字也是相互关联的。如果对比这些结果，其中共有的未知部分就会被抵消掉。因此，我根本不需要知道这个《我的世界》世界的原始种子，粘土块的位置就足以告诉我该去哪里找钻石。马修在他的频道上有一期非常精彩的视频，更详细地讲解了这一原理。我们已将其链接放在简介中，想看的话可以去看看。
<details>
<summary>Original English</summary>
(Gregor gasps)
- Dude.
- Occupational hazard.
- This edition of
Minecraft is coded in Java.
So for most of the game's history,
it used Java's LCG to
determine the placement
of resources in a given chunk.
But when Minecraft generated
different resources,
it didn't use completely
independent starting numbers.
Instead, it took the same underlying seed
and added a different fixed
number for each resource.
So for diamonds and river clay,
those starting numbers
differed by just three.
Java then modified those
seeds before using them,
so the difference wasn't
always three anymore,
but in most worlds,
it fell into one of a
few predictable values.
And because they went
through the same LCG,
the numbers used to choose
their position were related.
If you compare the results,
the shared unknown part cancels out.
So I didn't need to know the original seed
of the Minecraft world.
The location of the clay patch
was enough to tell me where to look.
Matthew has a great video on his channel
that works through how
this works in more detail.
We've linked it in the description
if you want to go check it out.
(explosion rumbles)
</details>

但还有一个更根本的问题：输出本身就能泄露足够的信息，从而预测出接下来的内容。

Java 的 LCG 会维护一个由 48 位二进制数字构成的内部状态值，Java 的 LCG 正是用它来生成序列中的下一个数字。但当它生成一个整数输出时，实际上会暴露其中的 32 位，只留下 16 位处于隐藏状态。由于是二进制，每一位只能是 0 或 1，因此总共只有 65,536 种可能的取值。

这听起来或许不少，但计算机可以对照生成器的紧接着的下一个输出对这些值进行验证，并且只有一个能够匹配。这样一来，你就能获知完整的 48 位内部数值；一旦知晓了它，你就能计算出随后的每一个数字。

对于所有的 LCG 而言其实都是如此。它们能生成极其漫长且没有明显规律的序列，但简单的数学结构仍然使其具有可预测性。
<details>
<summary>Original English</summary>
But there is a more fundamental problem.
The outputs themselves can reveal
enough information to
predict what comes next.
See, Java's LCG keeps
track of an internal number
that is made up of 48 binary digits,
and this is what Java's LCG uses
to generate the next
number in the sequence.
But when it generates an integer output,
it actually reveals 32 of those digits,
leaving just 16 hidden.
And since it's binary,
each can only be a zero or a one.
So that's just 65,536 possible values.
Now, maybe that sounds like a lot,
but a computer can test them against
the very next output of the generator,
and only one matches.
And then you know the full
48-bit internal number,
and once you know that,
you can calculate every
number that follows.
And this is actually
the same for all LCGs.
They can produce incredibly long sequences
with no obvious patterns,
but their simple mathematical structure
still makes them predictable.
</details>

>> 就像 LCG，它们并不好用，会引发各种各样的问题，非常容易被利用。它们只适合用在类似电子游戏这种场景下，你只需要一个快速而粗糙的方案，并且不怎么担心会遇到像我这样的人。
>> 但我需要指出，这个技巧在最新版的《我的世界》中已经不管用了。
>> 我一把这个技巧公开发布，它很快就在游戏中被修复了。
>> 哇，不可能吧。
>> 我记得在 1.18 版本中有人提交了漏洞报告。他们的做法是，直接把《我的世界》用来生成矿石的随机数生成器替换成了一个不同的生成器，新的生成器就不存在我们在此利用的特定缺陷。
>> 他们换掉了整个随机数生成器。
>> 没错，确实如此。你可以来完成最后这道工序了。
>> 好的，好的，好的。看看我能不能记起来。呃……
>> （笑）哎呀。
>> 好，看看这个。做好了。护腿、靴子、胸甲、头盔。
<details>
<summary>Original English</summary>
- Like LCGs, they're not good.
They cause all sorts of problems.
They're very exploitable.
They're for when you
have like a video game,
and you just need
something quick and dirty,
and you're not too worried
about people like me.
- But I should point out
that this trick doesn't
actually work on the most
recent versions of Minecraft.
- Once I published this trick,
it got patched out of
the game very quickly.
- Oh, no way.
- I think a bug report was
made in the version 1.18.
What they did is they actually switched
the random number generator
that Minecraft uses to generate ores
to a different random number generator
that would not have the particular flaw
we're exploiting here.
- They changed the whole number generator.
- Yeah, exactly.
You can do the honors.
- Okay, okay, okay.
Let's see if I can remember.
Uh...
- (laughs) Oh, boy.
- Okay, check this out.
Here you go.
Pants, boots,
chest piece, helmet.
(light upbeat music)
</details>

《我的世界》中的破绽之所以奏效，是因为开发者选择在游戏中使用了这种特定的随机数生成器；这也很好地提醒了我们：在构建软件时，所使用的工具是多么重要。

这便引出了今天的赞助商——Hostinger。Hostinger 是一个用于在线构建、运营和发展业务的一体化平台。无论你需要的是网站、网络应用还是网店，都可以在一个地方进行集中管理，甚至完全不需要懂得写代码。

举个例子，假设我想开创一项业务，出售刚才辛苦挖来的所有钻石。我只需用纯英文描述我想要的网站，Hostinger 的人工智能就会构建出一个初始版本。如果我想修改某些内容，只需用语言描述即可；但这仅仅是个起点，因为我还可以添加自己的自定义代码。与其从零开始构建一切，我不如把更多的时间花在挖钻石上。

目前 Hostinger 正在进行“黑色星期五”促销，如果你访问 hostinger.com/veritasium，还可以使用优惠码 Veritasium 享受额外 10% 的折扣。感谢 Hostinger 赞助本段视频内容。
<details>
<summary>Original English</summary>
The trick in Minecraft works
because the developers chose to put
this particular random number
generator into the game,
but it's a good reminder of
how much the tools you use
matter when you're building software.
And that brings me to
today's sponsor, Hostinger.
Hostinger is an all-in-one platform
for building, running, and
growing businesses online.
So whether you need a website
or a web app or an online store,
you can manage it all from one place,
and you don't even have
to know how to code.
So for example, let's say
I want to start a business
selling all those hard-earned
diamonds that I just mined.
So I can just describe the
website I want in plain English,
and Hostinger's AI is going
to build an initial version.
And if I want to change something,
I can just describe it,
but that is just a starting point
because I can also add my own custom code.
Instead of having to build
everything from scratch,
I can just spend more
time mining diamonds.
Right now, Hostinger is
doing Black Friday offers,
and if you go to hostinger.com/veritasium,
you can use code Veritasium
for an additional 10% off.
I want to thank Hostinger for sponsoring
this part of the video,
</details>

### 老虎机攻防与梅森旋转算法

现在回到赌场，赌客们当时正利用随机数生成器的漏洞赢取成千上万的美元。

2014 年 7 月 14 日，调查人员拘留了在全美各地老虎机上屡屡获胜的一名赌客。

>> 当他们在加州抓获这些家伙时，缴获了其中一部手机，并且发现视频其实正被传回俄罗斯的一台服务器。
>> 更具体地说，是传给圣彼得堡的一个由代号为“亚历克斯”（Alex）的黑客领导的团队。

五年前，俄罗斯实际上取缔了境内的大部分赌博活动，成千上万台老虎机被低价变卖。于是，亚历克斯搞到了其中的一些机器，并开始对其进行拆解。

>> 机器里有一块处理板，还有一块被称为 SMIB 的板子，也就是老虎机接口板。基本上，处理板是固化在游戏里的，随机器自带。一旦你拿到了物理设备，逆向工程就只是时间问题了。
<details>
<summary>Original English</summary>
and now back to the casino,
where gamblers were exploiting
random number generators
to win thousands of dollars.
(faint background chatter)
(light instrumental music)
(machine chiming)
On July 14, 2014,
investigators detained one of the gamblers
who had been repeatedly
winning on slot machines
across the U.S.
- So when they picked these
guys up in California,
they were able to get one of the phones,
and they were able to see that the video
was actually being transmitted
back to a server in Russia.
- More specifically, a
team in St. Petersburg,
led by a hacker only known as Alex.
Five years earlier,
Russia actually banned
most of its gambling,
and thousands of slot
machines were being sold off.
So Alex got hold of some of these machines
and started taking them apart.
- There's a processing board,
and then there's what
they refer to as a SMIB,
which was the slot
machine interface board.
Basically, the processing
board is locked into the game.
That comes with the machine.
Once you have access to the device,
it's just a matter of time
before it's reverse engineered.
</details>

不过问题在于，这些机器使用的并不是像 Java 那样的 LCG，而是复杂得多的随机数生成器。

>> 其中很多机器使用的是同一种梅森旋转算法（Mersenne Twister）。

该算法依然从一个种子开始，但它并不是用种子来生成单一数字，而是填满一个包含 624 个数字的表格。随后它执行一种称为“旋转”（twist）的计算，将表格不同部分的二进制位组合起来，生成 624 个全新的数字。接着它取出新表格中的第一个数字，经过另一系列运算处理，产生第一个伪随机输出。它对下一个及随后的每个数字重复同样的操作，直到产生 624 个输出。之后它对整个表格重新进行旋转运算，流程如此循环往复。它的序列周期十分巨大，重复所需的步数长度超过 6,000 位数。

尽管如此，每一步依然遵循着这些固定的数学规则，而亚历克斯通过研究自己拥有的机器内部的软件，成功破解了这些规则。因此，当他的团队收到来自美国赌场的旋转视频时，他们可以进行反向推导，与自己的机器进行比对，并预测何时最有可能出现赢局。
<details>
<summary>Original English</summary>
- The thing is though,
these machines weren't
using an LCG like Java.
They used a far more complicated
random number generator.
- A lot of them were using the same
Mersenne Twister algorithm.
- This algorithm still starts with a seed,
but instead of using this
to generate one number,
it fills a table of 624 numbers.
It then performs a
calculation called a twist,
combining the binary digits from different
parts of the table to
produce 624 new numbers.
Then it takes the first
number in this new table,
runs it through another
series of calculations,
and it produces its first
pseudorandom output.
It does the same with the
next number and the next
until it has produced 624 outputs.
Then it twists the whole table again
and the process continues,
and its sequence is huge.
The number of steps before it repeats
has more than 6,000 digits.
But despite all that,
every step still follow
these fixed mathematical rules,
and those were rules that Alex
was actually able to work out
by studying the software
inside of his own machines.
So when his team received videos
of spins from casinos in the U.S.,
they could work backwards,
and they could compare them
with their own machines,
and predict when a winning
spin was most likely.
</details>

但在老虎机内部，即使无人玩耍，随机数生成器也一直在不间断运行，最终结果取决于玩家按下旋转按钮的那一瞬间所选中的数字。因此，赌客必须在绝对精确的时刻按下按钮。然而人类大约需要四分之一秒的时间做出反应，于是亚历克斯将这种延迟写入了系统中。他开发了一款应用程序，在赌徒真正需要按键的前四分之一秒让其手机震动，然后……

这种手段并不能保证每一次旋转都中奖，但据报道，一个由四人组成的团队每周可以掠走超过 250,000 美元，因此手段相当奏效。最终，因参与该骗局而被捕的四人被指控犯有共谋欺诈罪。其中三人被判处两年监禁，而一人选择与联邦调查局（FBI）合作。

>> 那么，现在赌场里是否仍有可能有人在利用这种漏洞？
>> 确实，如果现在没人这么干，我反而会觉得非常奇怪。
>> 哦，真的吗？
>> 是的，外头仍有大量的那些老机器在运行。
<details>
<summary>Original English</summary>
But inside the slot machines,
the random number generator kept running
even when nobody was playing,
and the outcome depended
on the number selected
at the instant the player pressed spin.
So the gamblers had to press
at exactly the right time,
but it takes a human roughly a
quarter of a second to react.
So Alex built that delay into the system.
He created an app that made
the gambler's phone vibrate
a quarter of a second before
they actually needed to press, and...
(machine chiming)
(coins clattering)
Now, this trick didn't
guarantee a win on every spin,
but a four person team could reportedly
take more than $250,000 in a week,
so it was pretty effective.
In the end, the four men who were caught
as part of the scheme were charged
with conspiracy to commit fraud.
Three of them were sentenced
to two years in prison,
while one chose to cooperate with the FBI.
Oh, but is it possible
that people are still
running this exploit in casinos still?
- Yeah, I would be completely
surprised if they weren't.
- Oh, really?
- Yeah.
Yeah, there's a lot of those
boxes that are still out there.
</details>

### 加密安全与物理世界的熵源

所以归根结底，如果你对这类生成器的工作原理了解得足够充分，并且能够获取并分析足够多的输出，它们全都无法做到真正的不可预测。

但我们在数字安全领域却离不开随机数。它们被用于保护从个人信息到银行账户的各种数据；如果这些数字可以被预测，那么安全性就会荡然无存。

为此，我们前往位于科罗拉多州博尔德的美国国家标准与技术研究院（NIST）。NIST 负责制定安全随机数生成的标准，但那里的一个团队正在尝试一项更为宏大的目标。

>> 我们正在尝试探索的是：自然界所允许你制造的极限最佳随机数生成器究竟是什么样的？
>> 是的。
>> 这正是我们在这里开展的大量工作。
>> 这就是这个实验的意义所在。
>> 没错，所有这个实验都是为了制造出世界上最好的随机数生成器。我们真切地尝试利用物理和科学来发展出尽可能最佳的测量手段，然后再利用这些测量结果来制定标准。
<details>
<summary>Original English</summary>
- So ultimately, all of these
generators fail at being
unpredictable if you know
enough about how they work
and if you can study
enough of their outputs.
But we need random numbers
for digital security.
They're used to protect everything
from our messages to our bank accounts,
and if those numbers can be predicted,
then that security can be compromised.
So we went to the National Institute
of Standards and Technology
in Boulder, Colorado.
NIST sets the standards for
secure random number generation,
but one team there is trying
something even more ambitious.
- So what we're trying to do is say,
what's the best random number generator
that nature allows you to build?
- Yeah.
- And that's a lot of
what our work is here.
- [Gregor] And that's what this is about.
- Yep, this is what all
of this experiment is
to try to make the world's
best random number generator.
We really try to use physics and science
to try to develop the best
measurements possible,
and then we use those measurements
to develop standards.
</details>

这包括用于数字安全的随机数生成标准。因为在加密领域，你需要比我们目前见过的任何生成器都更难预测的机制。

密码学家因此研发出了另一种生成器。其背后的思路相当直观：首先准备一串数字，比如简单的 1、2、3、4 等等；接着，把这些数字逐一输入到加密算法中。算法会利用一个基于大型随机数的秘密密钥（secret key）将它们打乱。加密过程对输入进行了极其彻底的变换，以至于在没有密钥的情况下，输出看起来毫无关联。

从某种意义上说，那个密钥扮演了种子的角色。它是你启动时所需要的唯一随机数，并且决定了随后输出的每一个数字。在 Java 的情况下，其输出直接暴露了大部分内部隐藏状态；而对于梅森旋转算法，即便隐藏其输出的额外计算步骤也能被逆向破解。但在这里，即使你完全清楚加密的工作原理，并且掌握了所有的输入和输出，在实际操作中也没有可行的方法来复原秘密密钥。

想去猜测密钥同样是不切实际的。常见的密钥长度为 128 位，也就是 128 个 0 和 1，对应着超过 300 万亿亿亿（3×10^38）种可能的密钥。如果没有密钥，要想预测下一个输出几乎是不可能的。这是构建“密码学安全伪随机数生成器”（CSPRNG）的途径之一，它解决了我们的第三个难题——可预测性。
<details>
<summary>Original English</summary>
- And that includes the standards
for generating random numbers
for digital security,
because for encryption,
you need generators that are much harder
to predict than the
ones we've seen so far.
So cryptographers have developed
a different kind of generator.
The idea behind them is pretty simple.
Start with a string of numbers,
say just one, two, three, four, and so on,
and now you feed each of those numbers
into an encryption algorithm.
The algorithm scrambles
them using a secret key,
which is based on a large random number.
Encryption transforms the inputs
so thoroughly that without the key,
the outputs look completely unrelated.
In a way, that key plays
the role of a seed.
It's the one random
number you need to start,
and it decides every
number that comes out.
Where with Java, its outputs revealed
most of its hidden state,
and with the Mersenne Twister,
even the extra steps hiding
its outputs could be reversed.
Here, even if you know exactly
how the encryption works,
and you've seen all
its inputs and outputs,
there's no practical way
to recover the secret key.
And guessing it isn't realistic either.
A common key length is 128 bits,
so that's 128 ones and zeros and over
300 trillion, trillion,
trillion possible keys.
And without the key,
predicting the next output,
it's practically impossible.
This is one of the ways that you can build
a cryptographically secure
pseudorandom number generator,
and it solves our third
problem, predictability.
</details>

但那个秘密密钥最初又是从何而来的呢？因为算法本身无法凭空创造不可预测性，它在启动时切实需要某种随机的源头。

为此，计算机转向了物理世界。许多现代处理器都内置了硬件随机数生成器，通过测量电信号中的微小涨落来提供那些不可预测的种子。加利福尼亚州的一家名为 Cloudflare 的公司，甚至使用了一整面熔岩灯（lava lamps）墙来为其算法生成随机种子。

那么，这是否意味着问题已经解决了？并不完全是。

以抛硬币为例，我们通常认为正面或反面是一个随机事件。然而在严格控制的条件下，你其实可以让硬币每一次落下都是正面朝上，这是因为硬币遵循经典力学定律。因此，如果你能精确控制硬币的初始状态和翻转方式，就可以次次预测它的落地结果。

法国数学家皮埃尔-西蒙·拉普拉斯（Pierre-Simon Laplace）甚至将这一想法推向了极致。他设想存在某种智能实体，知晓宇宙中每一个粒子的位置与运动状态。根据经典力学，它便可以计算出未来发生的一切。
<details>
<summary>Original English</summary>
But where did that secret
key actually come from?
Because the algorithm can't
create unpredictability
from nothing on its own.
It actually needs something
random to start with.
And for that, computers
turn to the physical world.
Many modern processors
have built-in hardware
random number generators that
measure tiny fluctuations
in electrical signals to provide
those unpredictable seeds.
One company in California, Cloudflare,
even uses a whole wall of lava lamps
to generate random seeds
for its algorithms.
So does that mean the problem is solved?
Not exactly.
If you take a coin toss,
we normally think of this
as a random event, heads or tails.
Only under carefully
controlled conditions,
you can actually make the coin
land heads every single time,
and that's because a coin
follows the laws of classical mechanics.
So if you control exactly how it starts
and how it's flipped,
you can predict how it will
land every single time.
The French mathematician
Pierre-Simon Laplace
actually took this idea even further.
He imagined an intelligence
that knew the position
and motion of every
particle in the universe.
So according to classical mechanics,
it could calculate everything
that would ever happen.
</details>

### 量子纠缠与贝尔测试

>> 我曾耗费很长时间努力去探寻一个优秀的随机性定义到底是什么。我对随机性的定义，就是宇宙中没有任何事物能够提前预测的东西。不仅仅是没有人——我的意思不仅指人类，而是宇宙中的任何存在。
>> 这正是克里斯泰尔（Krister）的团队试图实现的：不仅要生成看起来随机的数字，还要证明它们在本质上是真正无法预测的。
>> 我们完全不想使用种子，也完全不想使用算法。
>> 于是，他们转向了量子力学，因为某些量子测量结果在根本上就是不可预测的。
<details>
<summary>Original English</summary>
- You know, I looked long
and hard to try to figure out
what is a good definition of randomness.
And my definition of randomness
is just something that nobody
could have predicted in advance.
And not just nobody,
I don't mean just humans,
but like anything in the universe.
- [Gregor] So that's what Krister's team
is trying to achieve,
not just to generate
numbers that seem random,
but to prove that they are
genuinely unpredictable.
- We don't want to do seeds at all,
and we don't want to do algorithms at all.
- So they've turned to quantum mechanics
because some quantum measurement outcomes
are fundamentally unpredictable.
</details>

>> 在眼前的这套装置中，我们首先使用一束非常明亮、强烈的激光。每秒能产生大约一亿个这样的脉冲，这束光脉冲射入并与这里的这块晶体发生相互作用。在光与晶体的相互作用下，有时我们的一个光子会发生反应，并裂变成我们所称的一对“子光子”（daughter photons）。

每个光子都具有一种被称为偏振的属性，对应于光电场振荡的方向。研究人员对实验进行了安排，使得这对子光子要么全部水平偏振，要么全部垂直偏振，但两者的状态无法区分。因此，光子最终处于这两种可能性的量子叠加态之中。

>> 这非常类似于薛定谔的猫的状态，但被扩展到了两个粒子上，现在就好像它们同时兼具这两种状态。
<details>
<summary>Original English</summary>
- So on this setup right here,
we start with a very bright
laser, a very intense laser.
You're generating about a hundred million
of these pulses per second,
and this pulse of light comes in
and interacts with this crystal here.
What can happen is the interaction
of this light with this crystal,
sometimes one of our photons
will interact with it
and fission into what we call
a pair of daughter photons.
(light dramatic music)
- [Gregor] Now, each photon
has a property called polarization,
which corresponds to the direction
in which light's electric
field oscillates.
And the researchers have
arranged the experiment
so that the pair can be
produced with both photons
polarized either horizontally
or both vertically,
but there's no way to distinguish which.
So the photons end up in
a quantum superposition
of both possibilities.
- This is very much like a
Schrödinger's cat-type state,
but it extended to two particles,
and now it's like they're kind of
both of those at the same time.
</details>

无论这两个光子身处宇宙何方，它们都共享同一个量子态。换句话说，它们纠缠在了一起。这意味着当我们对两者都进行测量时，其结果是相互关联的。

但首先，他们需要将光子分别送往两个独立的测量站，这意味着他们必须将每个光子导入一根光纤之中。

>> 最艰难的部分就在于眼前的这些光纤线缆。里面实际的光纤线缆是肉眼看不清的，它的直径只有大约 10 微米。打个比方，这大约只有人类头发直径或宽度的十分之一。所以这是一个极其微小的目标。我们必须做的事情，我称之为“量子射箭”。
这让我想起罗宾汉，他可以拉弓射箭并正中靶心；接着他能继续射箭，把上一支箭从中心劈开。我们所做的是这一场景的变体：罗宾汉现在面对两个靶子，手里只有一张弓，他必须同时射出两支箭，并且能够不断地持续命中并劈开这两个目标。
>> 射进这 10 微米的孔洞里。
>> 射进这 10 微米的孔洞里。
<details>
<summary>Original English</summary>
- [Gregor] The photons
share a quantum state
no matter where in the universe they are.
In other words, they are entangled.
And this means that when we measure both,
the results are correlated.
But first, they need to send the photons
to two separate measurement stations,
and that means they
have to get each photon
into an optical fiber.
- The really hard part is
these fiber cables right here.
The actual fiber optic cable
inside, you can't see it.
It's only about 10 microns in diameter.
And to put that in context,
that's about one-tenth the diameter
or width of a human hair.
So it's a very, very tiny target.
And what we have to do is
what I like to call quantum archery.
So, you know, I think about Robin Hood
and the fact that, you know,
he could kind of pull back
and shoot an arrow and hit a
target dead in the bullseye.
And then he can keep shooting arrows
and keep splitting the
center of the arrow.
We're doing a version of that
where now Robin Hood has two targets,
and he has a single bow.
And he has to shoot two arrows at a time,
and yet he's able to continually
keep splitting these two targets.
- [Gregor] Into these 10-micron holes.
- [Krister] Into these 10-micron holes.
</details>

光子随后到达相距 110 米的两个测量站。这意味着，即便是以光速传播的信号，也无法在测量完成前从一端赶到另一端从而对测量造成影响。

在每个测量站，研究人员都会测量光子的偏振，但他们可以在两个不同的角度之间选择其一来进行测量。每个测量站都会在光子抵达前的一瞬间随机选择其测量角度。

>> 你们在这两端获取的是什么样的结果，从而能得出最终的随机数呢？
>> 我要么探测到一个光子，要么探测不到。
>> 好的。探测到就计为 1，没探测到就计为 0。

但等等，他们在一项旨在生成随机数的实验中，居然使用随机数来选择测量方式。这似乎说不通。
<details>
<summary>Original English</summary>
- The photons then arrive
at two measurement stations
110 meters apart.
This means that even a signal
traveling at the speed of light
can't get from one to the other
in time to impact the measurement.
Now, at each station,
the researchers measure
the photon's polarization,
but they can choose between two
different angles to measure it at.
And each station chooses
its angle at random
just before the photon arrives.
What sort of result are
you getting here and there
that gives you that ultimate
final random number?
- I either detect a photon or I don't.
- Okay.
A detection gives us a one.
No detection gives us a zero.
But wait, they're using random numbers
to choose the measurements
in an experiment
that is designed to
generate random numbers.
It doesn't make sense.
</details>

>> 如果这部分本身不依靠整个装置来生成，那它们怎么能算随机的呢？
>> 制造随机性本身需要随机性作为起点。你只需要‘相当不错’的随机性。而整套装置的作用，是将这种‘相当不错’的随机性进行提纯，把它转化为经认证的、真正顶级的随机性。

前置的数字负责挑选执行哪一种测量，但 NIST 想要认证的，是探测器输出的那些 0 和 1。由于每个站都有两个可能的测量角度，因此总共有四种可能的测量组合。

如果光子只是携带针对每种可能测量的预先确定的答案，那么两个站的结果之间的关联强度就会存在一个数学上限。但当研究人员对比测量结果时，其关联度超越了这一极限。这被称为“违反贝尔不等式”（violation of Bell's inequality）。我们其实制作过一整期关于贝尔测试的视频，对这个话题进行了更深入的探讨；如果你想了解更多原理，我们已将链接放入了简介中。

由于测量的选择是独立的，且两站在测量期间无法相互通信，这就意味着光子的测量结果无法用任何局域的预先决定机制来解释。因此，该实验实际上是在检验这些数字是否蕴含真正的不可预测性。
<details>
<summary>Original English</summary>
- How are these guys random
if they don't use the whole setup?
- So you know, it takes
randomness to make randomness.
You just need pretty good randomness.
And this whole setup is a way to kind of
purify or take, you know,
what is pretty good randomness
and turn it into something that is like
certifiably like really good randomness.
- The first numbers choose
which measurements to perform,
but the numbers NIST wants to
certify are the zeros and ones
coming out of the detectors.
Because each station has two
possible measurement angles,
there are four possible
combinations of measurements.
Now, if the photons were
simply carrying predetermined
answers for every possible measurement,
there's a mathematical
limit to how strongly
the results from the two
stations could be correlated.
But when the researchers
compare the results,
the correlations exceed that limit.
This is called a violation
of Bell's inequality.
We actually made an entire
video about Bell tests,
and it goes much deeper into the topic.
So we've linked it in the description
if you want to find out
more about how this works.
Because the measurement
choices are independent
and that the stations can't communicate
during the measurements,
that means the photons'
results can't be explained
by any kind of locally
predetermined outcome.
So the experiment is actually testing
whether those numbers contain
genuine unpredictability.
</details>

### 漏洞规避与随机性提纯

但还存在其他潜在的漏洞。

>> 我们团队参与研究的一个漏洞被称为‘选择自由漏洞’（Freedom of Choice loophole）。也就是说，如果一个学生提前拿到了测验卷子，知道第二天会被问到什么题目，然后在考试中拿了满分，没有人会觉得意外。同样拟人化地来说，这些粒子在到达探测器之前，不应该被允许知道它们将面临什么问题。这又回到了随机性的核心本质：你是否真的能够确信，测量的选择在事前不存在任何关联？

有几种方法可以解决这个问题，而戴维·凯泽（David Kaiser）及其合作者想出了这个办法：

>> 我们要做的是把宇宙本身变成一对随机数生成器。
<details>
<summary>Original English</summary>
But there are other potential loopholes.
- The one that my own
group got involved with
was called the Freedom of Choice loophole.
Said no one should be surprised
if a student gets the quiz ahead of time,
knows what questions she'll be asked,
and then aces the quiz the next day.
These particles, again to speak
kind of anthropomorphically,
shouldn't be allowed to know
what questions they'll be posed
before they reach their detectors.
And that goes back to
randomness really at its core.
Can you really be confident that
the selection of measurements to perform
had no kind of correlations ahead of time?
- [Gregor] There are
a few ways to do this,
but David Kaiser and his
collaborators came up with this.
- What we wanted to do was
turn the universe itself
into a pair of random number generators.
</details>

他们将两台望远镜对准天空两端遥远的类星体，并利用来自各个类星体的单个光子的波长来决定执行哪一种测量。那些光线已经在太空中穿梭了数十亿年，发自自大爆炸以来几乎从未能够彼此通信的宇宙区域。假定中途没有人干扰过这些光线，那么测量选择与最终结果之间的任何隐秘协同，都必须早在数十亿年前就已经发生。虽然这并没有彻底消除漏洞，但它将那种可能性推回到了极其遥远的过去。

戴维的团队当时在研究是否存在某种隐藏的机制来解释这些结果，但 NIST 还必须考虑别的事情。

>> 如果我是个黑客，我会如何攻击这套系统？我会怎么做？
>> 原则上，两个人联手就可以把他们自己的光线射入那些望远镜，从而控制所选择的测量，进而操纵实验结果。

因此，NIST 必须对用来选择测量的随机数生成器提供物理保护，使其免受外部干扰。在这方面他们不能依赖类星体光。这使得外部人员攻击该系统的难度大为增加，但这依然无法证明他们的测量选择完全独立于受测设备。NIST 仍须做出这一假设，同时还必须假设超光速通信是不可能的、时间和距离的测量是精准的，以及对结果的记录是忠实且安全的。

如果这些假设成立，那么贝尔测试就可以对探测器输出中所包含的真正不可预测性的量给出认证。
<details>
<summary>Original English</summary>
- [Gregor] They pointed two telescopes
at distant quasars on
opposite sides of the sky
and used the wavelengths
from individual photons
arriving from each of the quasars
to choose which measurements to perform.
Now, that light had been
traveling for billions of years,
from regions of the universe that hadn't
been able to communicate with each other
since nearly the Big Bang.
And assuming no one had
interfered with the light,
any hidden coordination
between the measurement choices
and the results would have had to happen
billions of years ago.
Now, this didn't completely
eliminate the loophole,
but it pushed that possibility
much further back in time.
David's team were investigating
whether some hidden explanation
could account for the results,
but NIST has to consider something else.
- If I was a hacker, how
would I attack the system?
What would I do?
- [Gregor] In principle,
two people working together
could shine their own light
into those telescopes,
and control which
measurements are selected
and potentially rig the results.
So NIST has to keep the
random number generators
used to choose its measurements
physically protected from
outside interference.
They can't rely on quasar light for that.
That makes it much harder for
someone to hack the system,
but that doesn't prove their choices
are independent of the
devices being tested.
NIST still has to assume that,
along with the impossibility
of faster-than-light signaling,
accurate timing and distance measurements,
and faithful, secure
recording of the results.
If those assumptions hold,
then the Bell test can certify
how much genuine unpredictability
the detector outputs contain.
</details>

>> 如果我们利用纠缠态，你就可以执行这类测量，并证明没有任何事物能够预先知晓接下来的结果。

然而，原始测量结果并不必然是 0 和 1 的均匀混合，0 的数量可能会远远多于 1。贝尔测试告诉研究人员在数百万次测量中存在多少不可预测性，但它给出的并不是一串整齐平衡、相互独立的随机比特。因此，他们需要一种方法将那些不可预测性提取出来。

其基本思路与冯·诺依曼在他发表“有罪状态”笑话的那篇 1951 年论文中提出的方法类似：抛硬币两次，如果出现“正、反”，就记为 0；如果出现“反、正”，就记为 1；如果两次抛出的面相同，就直接舍弃。即使这枚硬币是有偏向的，只要每次抛掷相互独立且偏差保持恒定，“正-反”和“反-正”的概率也是完全相等的。因此剩下的序列就极为公正，只是序列长度会缩短。

NIST 所使用的技术要强大得多，但核心逻辑是相通的。贝尔测试认证了原始测量中至少含有 820 个比特的不可预测性；然后研究人员利用一种名为“随机性提取”（randomness extraction）的数学技术，将其浓缩为刚好 512 个比特。
<details>
<summary>Original English</summary>
- If we use entanglement,
you can do these types of measurements,
and you can show that there's nothing
that could have predicted
what's happening in advance.
- [Gregor] But the raw
measurements aren't necessarily
an even mixture of ones and zeros.
There might be far more zeros than ones.
The Bell test tells the researchers
how much unpredictability is present
across millions of measurements,
but it doesn't give them a neat sequence
of evenly balanced,
independent, random bits.
So they need a way to get
that unpredictability out.
The basic idea is similar to
the one von Neumann proposed
in the same 1951 paper as
his "state of sin" joke.
You flip a coin twice.
If you get heads, then
tails, you call that a zero.
And if you get tails, and then
heads, you call that a one.
And if both flips match, then
you just throw them away.
Even if the coin is biased,
as long as the flips are independent
and the bias doesn't change,
heads-tails and tails-heads
are equally likely.
So what's left is perfectly fair.
You just end up with a shorter sequence.
Now, NIST's technique
is far more powerful,
but the basic idea is similar.
The Bell test certifies
at least 820 bits worth
of unpredictability in
the raw measurements.
And then using a mathematical technique
called randomness extraction,
the researchers concentrate
that down to just 512 bits.
</details>

### 上帝的骰子

>> 我们进行的每一次测量，都对这每一个比特有所贡献。
>> 与我们在整个视频中所见到的那些随机数不同，这些数字不仅仅是难以预测，它们的不可预测性是可以被严格认证的。因此，这是你所能达到的最接近纯粹随机的状态。

>> 阿尔伯特·爱因斯坦曾有名言断言：‘上帝不与宇宙掷骰子。’爱因斯坦在这点上错了。事实上，我们在此所做的这些实验表明，经典物理学中爱因斯坦所支持的那种可预测本质、那种决定论的世界观，与量子力学是真正不兼容的。因此，如果上帝确实在与宇宙掷骰子，那么那些骰子长什么样？就是这个实验。这就是我们掷出的‘上帝的骰子’。这是你所能产生的最随机的熵源。
>> 所以上帝的骰子没有灌铅。
>> ‘上帝的骰子没有灌铅’，正是如此。这是宇宙中任何事物都无法提前预测的产物。
<details>
<summary>Original English</summary>
- Every one of the
measurements that we make
contributes to every bit.
- And unlike the random numbers
that we've seen throughout the video,
these aren't just difficult to predict.
Their unpredictability
can actually be certified.
So this is the closest
you can get to random.
- Albert Einstein, his argument was,
"God does not play dice
with the universe."
That's this famous Einstein quote.
And Einstein was wrong about that.
In fact, these experiments
that we do here show that really,
you know, this predictable nature,
this kind of deterministic worldview
that we have in classical
physics that Einstein espoused,
really is incompatible
with quantum mechanics.
So if God does play
dice with the universe,
then what do those dice look like?
And it's this experiment.
You know, this is like God's
dice that we're throwing.
This is the most random source
of entropy you can generate.
- So God's dice are not loaded.
- "God's dice are not loaded," exactly.
Yeah, so this is something that, you know,
nothing in the universe could
have predicted in advance.
</details>

NIST 与科罗拉多大学博尔德分校合作，实际上在 random.colorado.edu 上公开发布了这些数据，并附带了追踪和验证这些数字生成过程所需的信息。因此如果你愿意，完全可以使用它们。

这些数字已经被公开分享，我完全可以使用这里生成的比特，来决定我今天是穿一件绿色还是红色的毛衣，而且我是通过这些纠缠光子来做决定的。

>> 我是个色盲，所以不管你穿红毛衣还是绿毛衣对我来说看起来都一样。但制造这种随机性真的非常困难，需要大量的设备。你今天也看到了，我们摸索出了如何将这些不同的系统交织并联在一起、如何把这些不同的信标串联在一起的过程。这些随机性来源实际上可以构成一层额外的安全防线。所以，我想我们希望赋予随机性的，是整个互联网。
>> 太棒了。
>> 我的终极梦想就是：我们能不能让所有的事物都变得更加安全？
<details>
<summary>Original English</summary>
- Together with the University
of Colorado Boulder,
NIST actually publishes
this on random.colorado.edu,
along with the information
that you need to trace
and verify how the numbers were generated.
So you can go and use them if you want.
These numbers have been shared,
and I can really use the
bits that are generated here
to choose whether I'm wearing,
I don't know, a green or a red sweater,
and I'll be using these
entangled photons to do so.
- And I'm colorblind, so
it'll look the same to me
if you wear a red and green sweater,
but producing the
randomness was really hard.
It takes a lot of equipment.
You've seen that today.
We've figured out this process
of how we actually interconnect and weave
these different systems together,
and these different beacons together.
And sources of randomness
can kind of actually form a
layer of additional security.
So yeah, I guess the thing
that we hope to randomize
is the internet.
- That's awesome.
- That's my ultimate dream is, you know,
can we just make everything more secure?
(computer chirping)
</details>

好了，最后还有一件事。去年我们推出了官方 Veritasium 问答桌游，名字叫《Elements of Truth》。这是一款包含 200 道科技问题的游戏，但它不仅仅在于回答是否正确。游戏中有一套信心机制，你必须为自己的答案下注 1 到 10 分。因此，即使你答对了问题，如果你对自己产生怀疑，也可能会丢分。团队聚在一起时一直在测试这款游戏，过程超级有趣。如果你错过了 Kickstarter 众筹，我非常激动地宣布它现在已经正式发售了。如果你感兴趣，我们在简介中放了《Elements of Truth》网站的链接。

感谢大家对这个项目的支持，一如既往，感谢收看。

>> 它的原理是……
>> （男子呻吟）
>> （笑）
>> 不要啊。
>> 不要啊。
>> 出来，到这边来。（笑）不。
>> 我觉得我不该死掉。我觉得我不该死掉。我觉得我不该死掉。我会没事的。
<details>
<summary>Original English</summary>
- Okay, one last thing.
Last year we launched the
official Veritasium trivia game.
It's called Elements of Truth.
It's a game with 200 questions
about science and technology,
but it's not just about
getting the answer right.
See there's a confidence
mechanic in the game
where you have to put down a point
between 1 and 10 on your answer.
So even if you do get the question right,
you may lose out on points
if you're doubting yourself.
The team has been play testing
this when we get together,
and it has been super fun.
If you missed the Kickstarter,
I'm so excited to announce
that it's now available.
If you're interested, we put
a link in the description
to the Elements of Truth website.
So thank you for supporting this project,
and as always, thanks for watching.
- [Matthew] And the way
that it works is that...
(man groans)
(Matthew and Gregor laughing)
- No.
- No.
- [Gregor] Come out, come up here.
(laughs) No.
- [Matthew] I don't think I should die.
I don't think I should die.
I don't think I should die.
I'll be fine.
</details>