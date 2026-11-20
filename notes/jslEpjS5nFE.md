---
author: TechButMakeItReal
date: '2026-11-18'
guest: ''
layout: post.njk
source: https://www.youtube.com/watch?v=jslEpjS5nFE
speaker: TechButMakeItReal
tags:
  - export-control
  - semiconductor
  - artificial-intelligence
  - sanctions-evasion
title: 制裁漏洞与算力暗道：中国获取AI芯片的途径与博弈
summary: 视频剖析了中国在美国芯片禁令下获取AI算力与核心技术的多种途径，包括降规芯片的博弈与关税改道、提前囤积三星HBM内存、经由马来西亚数据中心租赁或转运算力、改装消费级游戏显卡、借助算能科技等中介获取台积电代工，以及利用DUV多重曝光替代EUV光刻机。
insight: ''
draft: true
series: ''
category: geopolitics
area: geopolitics
project: []
people:
  - Jensen Huang
companies_orgs:
  - Nvidia
  - Huawei
  - TSMC
  - Samsung
  - ASML
products_models:
  - Ascend 910B
  - H20
  - H800
  - H200
media_books: []
status: evergreen
---
### 禁令之下的疑云与现实

我来给大家出个速算题：到底需要多少位情妇，才能在中国造出自己的 AI 芯片之前帮它搞到芯片？天哪，我们怎么到现在都还没聊过这个？

中国被禁止使用美国芯片，但在 Kimik 3 中却出现了使用 Blackwell 的痕迹。黄仁勋（Jensen Hang）承认与一名涉嫌为中国间谍的女性有染，尽管目前没有任何证据表明她就是间谍。好几个中国 AI 项目的文件中都赫然列着被禁用的芯片。

但你知道真正有意思的是什么吗？大众的目光全被这场桃色风波吸引了，而现实中，中国至少找到了七种绕过美国制裁的方法。这整出所谓的情妇风波，顶多只占整件事的七分之一。

如今，在中国找到七种绕开禁令的途径的同时，完全没有受到任何禁令限制的欧洲、韩国和日本，在前沿前线 AI 领域却依然被远远甩在后面。那么，被禁用的芯片究竟是如何流入中国的？马来西亚、新加坡和中国台湾在其中扮演了什么角色？为什么那些完全不受禁令约束的国家反而赶不上来？让我们深入探究。

<details>
<summary>Original English</summary>
I have a quick math problem for you. How many mistresses does it take to get China AI chips until it can make its own? My oh my, how have we not talked about this yet? China, which is banned from using American chips, shows traces of using Blackwell in Kimik 3. Jensen Hang admitted to an affair with the suspected Chinese spy, although there is no evidence that she is a spy. Several Chinese AI projects have banned chips listed in their paperwork. You know what's interesting though? There is so much attention drawn to the whole affair situation when in reality China found at least seven ways to bypass US sanctions. The whole mistress situation [music] is at most 17th of the entire story. Now, while China found seven ways around the ban, Europe, Korea, and Japan, which don't have any bans at all, are still far behind on Frontier AI. So, how do banned chips reach China? What do Malaysia, Singapore, and Taiwan have to do with it? And why can't the countries with no ban at all catch up? Let's dive in.
</details>

### “打地鼠”式制裁与政策反复

我们将沿着制裁出台的脉络，逐一剖析每道禁令是如何被绕开的。

2022 年，美国首次对中国限制销售 AI 芯片。次年，英伟达研发出 A800 和 H800，以在遵守制裁规定的同时继续向中国客户供货。据报道，阿里巴巴、BYU 和腾讯都使用了这些芯片。这些芯片的算力品质大致相当，但计算速度相对更慢。到目前为止一切清晰：美国不卖旗舰芯片，但为中国定制了一款不同规格的产品，相安无事。

随后到了 2023 年，美国再次施加制裁，这一次直接封杀了他们此前生产的 800 和 H800。英伟达迅速应对，又专门针对中国市场打造了另一款产品——H20。

到了 2025 年，H20 也遭到了制裁。然而就在 H20 被封杀后短短几个月，特朗普政府表示：“稍等一下。”随后他们逆转了这一决定，允许英伟达重新向中国销售 H20，但附带了一个条件：英伟达必须向美国政府上缴 15% 的抽成。同样的规则也适用于之前被禁的 H200——也可以放行，但必须给美国政府交 25% 的抽成。

你大概看出其中的规律了：整套制裁与芯片的对抗就像一场打地鼠游戏。政府封杀 100，英伟达就造 800；政府封杀 800，英伟达就造 20。

<details>
<summary>Original English</summary>
We're going to follow the sequence of bans and see how each one got bypassed. 2022, the US restrict sales of AI chips to China for the first time. The following year, Nvidia develops A800 and H800 to comply with sanctions, but still keep selling to Chinese customers. Alibaba, BYU, and Tencent reportedly used those chips. The chips were roughly the same quality, but they did the calculations slowly. So far, all clear. US is not selling flagship chips, but they built a different product for China. No problem there. Then 2023, US applies sanctions again, and now they're blocking the same 800 and H800 that they produced. Nvidia responds and creates another product specifically for China, H20. 2025, H20 gets sanctioned. And right after H20 gets sanctioned, just a few months later, the Trump administration says, "Hold on a sec." [music] And then they reverse the decision and let Nvidia sell the H20s in China again, but with a condition. Nvidia has to give a 15% cut to the US government. The same rule applies for the previously banned H200. We'll let it slide too, but you pay us a 25% cut. So, you probably see the pattern here. The whole thing with sanctions and chips works like a whack-a-ole. The state whacks 100, Nvidia builds 800. The government whacks 800, Nvidia builds 20s.
</details>

### 华为的崛起与漫长的供应链改道

那么，美国为何要退让？答案是华为。

想想看：当你对中国这样一个庞大的市场切断所有好用的芯片时，会发生什么？你在该市场制造了真空。但这个真空不会永远存在，在本土企业取而代之之前，它的存在往往屈指可数。在中国，这家本土企业就是华为。美国制裁的芯片越多，就越是将中国推向替代方案。

即便在美国国内，这种反复摇摆的举动也引发了巨大反弹。民主党人斥责这是拿国家安全换取贸易利益的极其严重的错误；共和党人虽然推进了政策逆转，但也表示英伟达不应抱有任何幻想，中国必定会仿制其技术并进行大规模量产，力图彻底终结英伟达这个竞争对手。

你知道这项逆转导致了什么结果吗？它催生了一条涉及台湾的新供应链。

<details>
<summary>Original English</summary>
So, why did the US back down? The answer is Huawei. Think about it. What happens when you withhold all useful chips from a massive market such as China? You create a vacuum in that market, but that vacuum won't be there forever, and its days are usually numbered until a domestic business takes its place. In China's case, it's Huawei. The more chips the US sanctions, the more it pushes China toward the alternative. Even within the US, this back and forth dance caused a lot of backlash. The Democrats called it a terrible mistake to trade off national security for advantage in trade. The Republicans still went with a reversal, but said that Nvidia should be under no illusions and China will definitely rip off its technology, mass-produce it, and seek to end Nvidia as a competitor. And you know what happened as a result of this reversal? It created a new supply chain where Taiwan comes in.
</details>

2025 年 12 月，白宫宣布，未来在台湾制造的芯片必须经由美国转运至中国。进入美国时，需缴纳 25% 的进口关税，并在出口至中国前接受安全审查。

于是，供应链变成了：台湾 -> 美国 -> 获批的中国企业。

等等，这和以前有什么不同？看一眼地图：这里是台湾，这里是中国大陆，这里是美国。2026 年之前，台湾制造的芯片哪怕是由英伟达售出，也是直运中国。现在却要绕这么一大圈。运输成本在此处反倒不是最关键的，真正要命的是整条路线耗费的时间。

在经历了这一连串打地鼠闹剧后，北京表态：受够了，我们不需要你们的芯片。好吧，或许我们确实需要一点点，但绝不是全盘照收。

2026 年 1 月 14 日，北京通知本国海关在边境扣留 H200，禁止其入境。你能想象当时的画面吧？成堆的芯片囤在自家国门边境，但就是不让进。

1 月 28 日，中国稍有松口，批准了少量芯片供应给字节跳动（Bance）、阿里巴巴和腾讯，但并非全部。到了 5 月，华盛顿方面踩下刹车，故意放慢了安全审批速度。他们放行了向大约 10 家中国客户的货运审批，但就是迟迟不发货。

而到了 2026 年 11 月，也就是眼下，这些芯片终于运往香港，但此时中国却并不急于审批放行了。

整套互动模式从最初的“打地鼠”，演变成了一出彻头彻尾的《呼啸山庄》式爱恨拉扯。华盛顿问：“你要我的芯片吗？”北京回：“不用了，谢谢，我很好。”接着北京又说：“其实，我还是需要一点的。”华盛顿说：“行啊，但我得先去安全部门过审。”随后中国选择了安全稳妥的华为，暗地里却依然惦记着英伟达。

所以，如果你身处中国的位置，意识到获得完整芯片充满了重重障碍，自然而然就会开始盘算：退而求其次，我能争取的最好替代是什么？究竟是什么让那颗芯片如此关键？是内存，也就是 HBM。

面对这种拉扯博弈，中国祭出了几乎称得上最强的策略之举：开始大量囤积高带宽内存。

<details>
<summary>Original English</summary>
December 2025, the White House announces that going forward, the chips manufactured in Taiwan will be shipped to China through the United States. And upon entering the United States, they will have to pay a 25% fee as an import tax. and go through a security review before being exported to China. So, the supply chain becomes Taiwan, United States, approved Chinese company. Wait a sec. But how is this different from before? Well, look at the map. This is Taiwan. This is China. And this is the US. Before 2026, the chips manufactured in Taiwan, even if they were sold by Nvidia, went straight to China. Now they do this. The whole shipping cost situation is not as important here as the time spent on this entire route. So Beijing looks at this after the whole whack-a-ole situation and says enough. We don't need your chips. Okay, maybe we do a little bit, but like not all of them. January 14th, 2026, Beijing tells its own customs to hold H200's at the border and not let them in the country. You can picture the situation, right? You've got piles of chips sitting in your country at the border, but you don't let them in. January 28, China bags down a little bit. They approve some chips for Bance, Alibaba, and Tencent, but not all of them. In May, Washington hits the brakes [music] and makes the security clearance very slow. They clear shipping to around 10 Chinese customers, but they don't ship the chips. November 2026, right now, the chips are finally being shipped to Hong Kong, but now China isn't rushing to approve them. So, this whole pattern went from whack-a-ole to this like fullblown withering heights. Washington says, "Would you like my chips?" Beijing says, "No, thank you. I'm fine." Then Beijing says, "Actually, I need a few." Washington says, "Sure, but let me talk to security first." And then China picks the safe choice, Huawei, but secretly thinks about Nvidia. So, if you're China and you understand that getting the entire chip is a problem, naturally, you're going to start thinking, "What is the next best thing I can win? What makes that chip so critical? The memory or HBM. And what China did is probably the best power move you can think of when it comes to playing the Withering Heights situation. They started stockpiling the memory.
</details>

### 赞助商插播：NA 自主 AI 助手

当本频道开始发展壮大后，我们开始与许多出色的科技品牌合作，而我也遇到了以往从未面对过的难题：做账。

过去十年里，我一直是一名普通雇员。但经营一家企业，哪怕是一家小企业，也完全是另一码事。每个月我都会整整搭上一天的时间处理文书工作，我对那一天深恶痛绝。我有一大堆纸质收据，我讨厌记账。软件订阅分散在两个不同的邮箱，买来作为拍摄背景的新灯具，要通过三个不同软件给团队发放的款项，还有机票、酒店凭证等等。有些收据是截图，有些是纸质凭证，有些在收件箱里。

为了减轻这些行政琐事、帮我赢回一整天的工作时间，我们与 NA 达成了合作。NA 是一款运行在 Mac 和 iPhone 上的自主 AI 助手，能够跨所有应用工作。我只需要说一句：找出我邮件和相册里 10 月份的所有收据，然后按日期和供应商重命名，导出为 PDF 保存到电脑，并上传到我的财务表格和 Notion 页面。它就能一气呵成、端到端全自动搞定。它只会触碰我授权它处理的内容，因此在任何内容提交发送之前，我仍然可以过目把关。NA 简单、流畅且体验极佳。在配备 M 系列芯片的 Mac 和 iPhone 上提供 14 天免费试用及 10,000 个 AI 积分点数。不妨一试，链接就在视频简介中。

现在让我们回到正题。

<details>
<summary>Original English</summary>
When this channel started growing, we started working with many amazing tech brands. And I faced something I never had to face before. Accounting. For the past 10 years, I've been an employee. But running a business, even a small one, is a very different beast. Every month, there is a full day I lose to paperwork. And I dread that day with passion. I have a ton of paper receipts. I hate logging. Software subscriptions tied to two different emails, new lights we bought for the background, payments for the team that I have to make through three different apps, plane tickets, hotel receipts, you name it. Some receipts are screenshots, some are physical receipts, some are in my inbox. And to make this admin work easier and give me back a full day of work, we partnered with NA. NA is an autonomous AI assistant that lives on Macs and iPhones [music] and it works across all of your apps. All I got to say is find every receipt from October across my email and photos. Then I rename the receipts by date and vendor, save it as a PDF to my computer, and upload it to my finance spreadsheet and notion. and it just does it end to end all in one go. It only touches what I give it permission to touch, so I can still check before anything goes out. NA is simple, smooth, and delightful to use. It's free for 14 days with 10,000 AI credits on M series Max and iPhone. Give it a try. The link is in the description. And now back to the video.
</details>

### 途径二：囤积三星 HBM 内存

路透社与 SemiAnalysis 均估计，有 1,150 万组 HBM 堆栈通过韩国三星流入中国。1,100 万到 1,200 万组 HBM 堆栈，足以组装大约 160 万颗华为 AI 芯片。

这是个庞大的数字吗？我们来对比一下：DeepSeek 训练其 V3 模型大约用了 2,000 颗英伟达 H800 芯片，Kimik 3 使用了大约 20,000 颗。而中国的库存储备足够产出 160 万颗华为芯片。虽然这些芯片无法与 H800 完全对标，但差距也没有夸张到遥不可及。

他们为何押注 HBM？因为掌握了 HBM，他们就能制造自己的芯片。这个漏洞确实推动他们迈向了 AI 主权。他们早在 2024 年就开始布局此事，主要供华为和 BYU 使用。到 2024 年年中，在新一轮制裁落地之前，他们就已经开始大量囤积 HBM 堆栈。

随后华盛顿反应了过来。2024 年 12 月 2 日，美国宣布将对韩国出口 HBM 实施管制。这跟韩国有什么关系？为什么是由美国发号施令？因为三星是中国最大的 HBM 供应商，而三星在制造内存时使用了美国的半导体制造设备。华盛顿对 HBM 施加限制，直接牵连所有使用美国技术的外国制造产品，这其中就包括韩国。

这些管制措施定于 12 月 31 日正式生效。但在 12 月 2 日至 12 月 31 日之间，大约有四周的时间窗口。正是这四周内，三星向中国突击供应了 700 万组 HBM 堆栈。

囤积 HBM 是一帖极佳的缓兵之计，因为它争取到了宝贵的时间。它能帮助中国在芯片制造上进行更多试验，但在战术层面却无法解燃眉之急。当下的战术目标是：他们必须紧跟前沿模型而不掉队。因此，HBM 漏洞虽然成效显著，中国仍在寻找更多途径，并且他们确实找到了。

这就引出了下一个漏洞——一个在近期新闻中你或许有所耳闻的地方，一个芯片与情感交汇的枢纽：马来西亚。

<details>
<summary>Original English</summary>
Both Reuters and semi analysis estimate 11 and a half million HBM stacks enter China through Korean Samsung. 11 12 million HBM stacks is enough for approximately 1.6 million Huawei AI chips. Now, is this a lot? Let's put it in perspective. Deepseek trained its V3 model on about 2,000 Nvidia H800 chips. [music] Kim 3 used around 20,000. China's stockpile is enough to pump out 1.6 million Huawei chips. Now, they're not the same as H800s, but they're not crazy far. Why did they make a bet on HBM? Because having HBM allows them to build their own chips. This loophole actually does move them towards AI sovereignty. They started doing this back in 2024, primarily for Huawei and BYU. By mid 2024, they already started piling up HBM stacks before new waves of sanctions. Then Washington catches up. December 2nd, 2024, the US says we will apply controls on export of HBM from Korea. What does this have to do with Korea? And why is the US calling the shots? Because [music] Samsung is the biggest supplier of HBM to China. and Samsung manufactures its memory using American semiconductor making equipment. If Washington puts a restriction on HBM, it does affect all foreignmade production that uses American technology. This includes Korea. [music] On December 31st, these controls actually kick in. But between December 2nd [music] and December 31st, there are roughly four weeks. And in those four weeks, Samsung supplied 7 million HBM stacks to China. Now, the HBM stockpile is a good band-aid because it buys time. It helps China experiment with more chip manufacturing, but it does nothing in tactical terms. And the tactics is they need to stay afloat with Frontier models. So the HBM loophole is great, but China looks for more and it finds them. Which brings us to the next loophole, which is a place you have probably heard of in the light of recent news. A place where chips and hearts meet. Malaysia.
</details>

### 途径三：马来西亚数据中心算力通道与转运

在 2020 年代初，马来西亚（尤其是柔佛州）成为了数据中心建设的重镇。原因何在？由于新加坡。新加坡本国土地有限，数据中心建设达到饱和无法继续容纳，于是新加坡开始在马来西亚设立子公司。依托这些数据中心子公司，马来西亚迅速崛起为核心算力枢纽，这也顺理成章地使其成为英伟达芯片的汇集地。

这些芯片任何一方都可以使用，包括中国。考虑到马来西亚的地理区位，对中国而言极为便利，他们根本无需在美国繁琐的规则前周旋，直奔马来西亚即可。

中国获取马来西亚境内的美国芯片主要有两种途径：
1. **远程租赁算力**：搭载英伟达芯片的服务器部署在马来西亚数据中心内，中国从远程租赁算力。这样一来，没有任何芯片实体流入中国境内；
2. **暗道走私**：搭载英伟达芯片的服务器存放在马来西亚数据中心，对外申报部署在马来西亚，随后暗中将芯片偷运至中国。从美国监管立场来看，这属于彻头彻尾的走私行为。

据报道，Moonshot 的 Kimik 3 就是通过阿里巴巴租用的 20,000 颗芯片集群进行训练的，而阿里则是从马来西亚租赁的算力；字节跳动则从马来西亚的 Iolani 云租赁服务器。

这里还有一个漏洞：美国有一份禁止购买美国芯片的中国企业黑名单。但如果一家被拉黑的企业在海外设立子公司，该子公司并不在黑名单上，依然可以从马来西亚购买或租赁美国芯片。

去年（2025 年 9 月），华盛顿出台了一项规定以堵塞这一漏洞，将大股东为被制裁实体的任何公司自动列入黑名单。然而该规定随后被暂停执行。此次暂停是中美贸易休战的一部分，有效期持续至 2027 年 1 月 10 日。

你可以想象，在这一规定被搁置的过去一年里，发生了怎样的活动。

现在我们来聊聊那个不可回避的焦点：那位嫌疑间谍（之所以称“涉嫌”，是因为查无实据）——黄仁勋承认与之有染的 Alice Hang。这正是她的角色所在：她曾是 MegaSpeed 的高管。MegaSpeed 是一家在新加坡注册、账单地址也在新加坡的云服务公司，但它通过一家名为 Speed Matrix 的子公司与马来西亚连接。在 2024 年 6 月至 2026 年 2 月期间，Speed Matrix 采购了价值至少 48 亿美元的芯片。

由此可见，无论是从马来西亚“远程租算力”还是“实体转运”，两条通路规模都相当庞大，且都在运作之中，很难断定哪一条体量更大。两者都依赖数据中心和美国芯片。

<details>
<summary>Original English</summary>
Malaysia and specifically Johor became a major place for data centers in early 2020s. Why? because of Singapore. Singapore was building data centers on their own land, but they reached a point where they couldn't build anymore. They couldn't accommodate them. So, Singapore started building subsidiaries in Malaysia. And because of those data center subsidiaries, Malaysia became a major destination for computing power, which automatically makes it a hub for Nvidia chips. Those chips can be used by anyone including China. Now given where Malaysia is situated on the map, its geography is quite useful to China because they don't need to do this entire US curtsy and can go straight to Malaysia. Now there are two ways through which China gets access to American chips in Malaysia. One, when a server with Nvidia chips sits inside a Malaysian data center and China rents compute remotely. This way, no chips actually make it into China. Or two, a server with Nvidia chips sits in a Malaysian data center. Malaysia declares deployment in Malaysia, but then ships the chips over to China behind the curtains, which if you're the US, from your standpoint, this is straight up smuggling. Moonshot Kim K3 was reportedly trained on a 20,000 chip cluster rented through Alibaba who rents compute from Malaysia. Bidance rents servers from Iolani cloud in Malaysia. There's another gap. The US keeps a blacklist of Chinese companies that cannot buy American chips. But if a blacklisted company opens a subsidiary abroad, that subsidiary isn't on the list. So, we can still buy or rent American ships from Malaysia. In September 2025, last year, Washington made a rule to eliminate this problem because, well, they had to. And they started automatically blacklisting any company if the majority ownership of that company comes from a blacklisted company. Then they reversed the rule. The reversal happened as part of the trade truce with China and it's active until January 10, 2027. So you can probably imagine what's been happening over the past year when this rule was put on pause. Now let's address the elephant in the room. The suspected spy suspected because there is no evidence. [music] Alice Hang that Jensen Hang admitted to have had an affair with. This is where she comes in. She is a former executive of Megaspe. Mega Speed is a cloud company incorporated in Singapore with a billing address in Singapore, but it connects to Malaysia through a subsidiary. The subsidiary is called Speed Matrix. Speed Matrix buys at least $4.8 billion worth of chips between June 2024 and February 2026. So both routes, renting from Malaysia and shipping from Malaysia are quite large. Both of them are used, [music] but it's hard to say which one is bigger. And both of them need data centers and American chips.
</details>

### 途径四：消费级游戏显卡改装

现在，我向大家展示一个既不牵扯任何情妇、间谍，也不涉及芯片走私或数据中心的漏洞。

有人在关注《GTA 6》的发布吗？有的，我也在关注。接下来我们就聊聊传统纯粹的游戏硬件。

有证据表明，中国的工作室会将游戏显卡拆解，并重新组装用于 AI 计算。他们之所以对其进行改装，是因为英伟达 GeForce 等游戏芯片本身就集成了 CUDA 和 Tensor Core。只要拥有这些核心，技术上就能执行 AI 运算。

中国的显卡改装产业相当成熟完备。有关改装 RTX 4090（同样是游戏芯片）的官方文档已经流出，其中还附有工厂内部的实拍照片，详细展示了如何将处理器和显存从游戏卡移植到定制的 AI 板卡上。

如果仔细推敲时间线，这些文档早在 2023 年华盛顿对游戏显卡出口实施禁令之前就已经存在了。因此，你甚至不能指控他们走私，因为他们早在制裁生效之前就已经付诸实践。此外，一家香港媒体在 2023 年 10 月还报道了一些实拍画面，展示了对新一代游戏芯片 RTX 5090 采用的完全相同的改装工艺。

这些改装游戏卡足以维持少数几家实验室的运转，但要建立自主的本土芯片工业，你必须拥有一座晶圆制造厂。而中国通过一家中介公司，打通了通往全球半导体制造巨头的通道。

<details>
<summary>Original English</summary>
Now, let me show you a loophole that doesn't involve having any mistresses or spies or chips or data centers. Is anyone following the release of GTA 6? Yes. So am I. Now, let's talk the good old gaming. There has been evidence of Chinese workshops dismantling gaming graphic cards and rebuilding them for AI usage. The reason they tweak them is because gaming chips like Nvidia's GeForce already contain CUDA and Tensor Core. And as long as they have that, they can technically perform AI calculations. The conversion industry in China is quite robust and there is official documentation for the conversion of RTX 4090s also gaming chips with actual photographs from the facility of how the processors and memory can be transferred from gaming cards to custom AI boards. And if you dig into the dates, the documentation was created before Washington put a ban on gaming card expert in 2023. So, you can't even blame them for smuggling anything. They did it before the sanctions kicked in. There's also some footage from October 2023 reported by a Hong Kong outlet showing the same process with RTX 5090s, which is a newer generation of gaming chips. So, those gaming cards can keep a few labs going, but to build a domestic chip industry, you need a factory. and China found a way into the titan of semiconductor manufacturing through an intermediary.
</details>

### 途径五：借道中介获取台积电制造

正如我之前所言，中国摆脱对美制芯片依赖、实现完全 AI 主权的最大指望是华为。但在许多方面，华为依然依赖台积电（TSMC）——也就是为英伟达代工芯片的同一家台湾半导体制造巨头。因为放眼全球，没有任何一个地方能像台湾那样制造这些芯片。

即使华为拿出自己的芯片设计方案，也无法成为台积电的直接客户，因为未经美国许可，台积电不得为华为制造或供应芯片。其原因在于台积电制造的芯片受制于美国的出口管制条例。

因此，华为需要一个中介：算能科技（Sophgo）。

算能科技是一家为加密货币挖矿巨头比特大陆（Bitmain）设计芯片的中国企业。比特大陆本身就是台积电的现有客户。等一下，比特大陆不也是中国公司吗？为什么没有被制裁？

因为中国企业并没有被台积电全员拉黑。美国封禁的是特定企业，比特大陆并不在名单中，算能科技最初也未被列入实体清单。因此，台积电合法承接了算能科技的订单。2023 年，算能科技下单定制了芯片，随后该芯片内部的裸晶（die）被发现出现在华为昇腾 910B（Ascend 910B）芯片之中。

这枚裸晶引发了一场调查。事实证明，华为通过算能科技获得了超过 300 万片台积电制造的硅片。这意味着，华为的昇腾 910B 在技术层面正是由台湾制造的。

<details>
<summary>Original English</summary>
Like I said before, China's strongest bet to break dependency on American chips and create full AI sovereignty is Huawei. But Huawei in many ways depends on the same Taiwanese semiconductor manufacturing company, TSMC, that builds Nvidia's chips. Because no other country on earth assembles those chips the way Taiwan does. Huawei cannot be a direct customer of TSMC, even if it brings its own chip design because TSMC cannot manufacture or supply chips to Huawei without US authorization. The reason they can't do it is because TSMC chips are under US export controls. Therefore, Huawei needs an intermediary. Sofgo. Sofgo is a Chinese chip designer for a crypto mining giant, Bitmain. Bitmain is an existing TSMC customer. But wait, why isn't Bitmain a Chinese company? Why isn't it banned? Because Chinese companies are not banned as a whole, as a group from using TSMC. The US bans specific companies, and Bitmain isn't one of them. SOFGO wasn't on the list either, so TSMC could legally accept orders from SOFGO. In 2023, SOFGO ordered chips, and the dye in those chips was also found inside Huawei's Ascend 910bs. This die triggered an investigation and as it turned out later Huawei got more than three million TSMC made pieces of silicon through SAVGO. So Huawei's Ascend 910bs are technically built by Taiwan.
</details>

### 途径六：ASML 光刻机禁令下的 DUV 多重曝光替代

现在我们来看最后一个漏洞，也是一切开端时中国就摸索出的应对方案。在针对芯片与内存的一连串禁令、在马来西亚和新加坡的斡旋、在涉嫌间谍风波出现之前，中国面临的第一场重大封禁来自荷兰。

谈到荷兰，自然是指 ASML。ASML 成为了中国的关键一课，让他们明白当正门被关上时，你就必须去寻找窗户。

荷兰著名的 ASML 是半导体制造光刻环节不可或缺的核心存在。在美国外交施压下，ASML 于 2019 年实施了出口限制。自那时起，中国便无法购入极紫外光刻机（EUV）。

但缺乏 ASML 的极紫外光刻机（即 EUV），并不意味着找不出变通方案。他们转向了较为老旧的深紫外光刻机（DUV）——本质上是 EUV 之前一代的早期版本。

简而言之，究竟是什么让 EUV 机器如此珍贵与特殊？EUV 能将图案投射在硅晶圆上，基本上能单次曝光生成一层紧密排布的平行线条，从而刻画出极其微小精细的图案。较老的 DUV 机器无法直接取代 EUV，技术精度不够先进。但它的变通之处在于：可以将 EUV 一次成型的图层拆解为多个密度较低的图层分别曝光，这种技术称为多重曝光（multi-patterning），通过多道工序循序打印。

有直接证据表明这种变通方案是奏效的：华为 Mate 60 Pro 采用的 7 纳米芯片，正是由 DUV 光刻机生产的。

但该方案的弊端在于成本高昂且扩产困难。因为使用 DUV 意味着单片晶圆所需的制造步骤成倍增加，要达到相同的晶圆产出量，需要耗费数量多得多的设备支持。

总而言之，中国在技术上可以通过老旧设备绕开 ASML 生产出先进制程芯片，但制造过程缓慢且造价昂贵。如果北京能如期达标，中国将在 2028 年拥有自主研发的 EUV 光刻机；而按照业内人士的看法，时间点可能更接近 2030 年。无论如何，针对 ASML 设备的制裁并没有阻断中国自主研发的脚步，它唯一的作用，只是为美国争取了一点喘息的时间。

<details>
<summary>Original English</summary>
And now we're moving to the last loophole. The one that China came up with back when it all started. Before a series of bans on chips and memory bans and Malaysia and Singapore situation, before the suspected spies, the first big ban that China got came from the Netherlands. And of course, when we say Netherlands, we mean ASML. ASML became the first big lesson for China when it learned that when the front door closes, you start looking for windows. The famous Dutch ASML, without which there is no lithography in semiconductor manufacturing, enforced restrictions under American diplomatic pressure in 2019, and since then, China has not been able to buy extreme ultraviolet machines. But not having ASML's extreme ultraviolet machines, also known as EUVs, does not mean that you can't find a workaround. And they did. They reached for older deep lithography machines, otherwise known as DUVs, basically the earlier version of EUVs. Now, quickly, what does make EUV machine so incredibly valuable and special? EUV projects a pattern on a silicon wafer and it basically builds one solid layer of packed parallel lines and it can produce incredibly intricate minuscule patterns. Older DUV machines cannot replace EUV. They're simply not advanced enough. But what it can do is it can separate the layer that EUV does in one go into multiple less dense parts. This is called multi-pattering and it can print them in a sequence and there is direct evidence that this workaround works because Huawei's 60 Pro uses a 7 nanometer chip which is produced by a DUV. The problem with this workaround is that it's very expensive and not very scalable because using a DUV implies more manufacturing steps per one wafer. you need a lot more equipment to produce the same output. So to sum it up, China can technically bypass ASML and make advanced chips with older machines, but the process is slow and expensive. If Beijing hits the target, China is going to have its own EUV machine by 2028. If you believe what insiders are saying, it's more like 2030. Either way, sanctions over ASML equipment did not stop China from building their own. The only thing it did is bought America a little bit of time.
</details>

### 结语与行业反思

美国对中国实施的一系列制裁和禁令确实拖慢了其步伐。但有志者事竟成，准确地说，至少有七种门路。

如果要问我对黄仁勋被免职的个人看法——顺便提一句，我们在 11 月 14 日录制本期视频，截至今天他已经辞职，但我依然抱有希望他会重返岗位——失去这位英伟达的 CEO 将会是整个 AI 行业的重大损失。

再次声明，就我个人浅见而言，我既不能也不会去评价他在婚姻层面的忠诚与否。首先，这根本不是我该过问的事；其次，我也不清楚其中有多少是媒体捕风捉影编造的。但纯粹从他作为英伟达 CEO 的身份来评价，曝光他的绯闻对美国的 AI 主权起不到半点帮助。

这整套局面让我想起了某种障眼法：不要只盯着正中间的焦点，注意看两旁正在运作的手。

希望本期内容对大家有所启发，我们下期视频再见。拜拜！

<details>
<summary>Original English</summary>
Sanctions and bans that the US has been enforcing against China definitely slowed it down. But when there is a will, there is a way or at least seven ways to be [music] exact. If you ask my personal opinion on the ousting of Jensen Huang, and by the way, we're filming this video on November 14th, and as of today, he has resigned, but I still have hopes that he will come back. Losing him as a CEO of Nvidia is going to be a huge loss for the AI industry. Again, [music] in my humble opinion, I can't and I won't judge him on his matrimonial faithfulness. [music] It's first of all, simply not my business. Secondly, I don't know how much of it was made up by media, but judging purely on who he is as the CEO of Nvidia. Exposing his affairs does absolutely nothing to the American AI sovereignty. And this whole situation reminds me of something that looks like [music] this. So, don't look just in the middle and watch the hands around. [music] We hope this was helpful and we'll see you in the next video. Bye.
</details>