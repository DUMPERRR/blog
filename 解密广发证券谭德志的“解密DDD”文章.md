2024年11月15日，“广发证券科技金融”公众号刊登了谭德志的《架构整洁之道|解密DDD的本质一降低共识与扩展成本》（https://mp.weixin.qq.com/s/ESi5vbNUkucNqVy4wmqwwA），接下来，我将写若干篇文章，逐个截屏来赏析此文的内容。
我在“DDD领域驱动设计批评”合集中已经写有67篇文章，对于DDD圈子的各种话术、“创新技巧”应该剖析得相当透彻了，其中一些内容归纳到了《软件方法》中。近一段时间还写了“《分析模式》漫谈”合集，部分内容也有涉及。
因此，在赏析此文时，我将尽量不写新内容，而是引用曾写过的内容，看看此文的内容有多少命中率，命中我曾剖析过的DDD圈子特征。
我对DDD（领域驱动设计）的总观点可以看《小甜甜和牛夫人》（https://mp.weixin.qq.com/s/briTMPxQgWWtONE0jJOntw）。
声明了总观点，接下来开始“解密”。

<img width="621" height="1073" alt="image" src="https://github.com/user-attachments/assets/c8d854db-4226-4090-81c4-9c0e15cf427c" />

①架构整洁之道、解密
⑥道
这里应该是引用了“Clean Architecture ”的中译本名称。原书名并没有“道”，国内的一些编辑喜欢加“之道”，也是为了迎合这些圈子的口味。“解密”也是如此，我这篇文章的标题也跟一下风。
我写过的以下文章，剖析了“之道”现象：
★《软件方法（第3版）》第1章（umlchina.com/url/softmeth2024.html）：

<img width="1080" height="968" alt="image" src="https://github.com/user-attachments/assets/14dcdf7d-1074-45e3-a907-e170b2d86472" />

★《软件方法》强化自测题-总纲（3）（https://mp.weixin.qq.com/s/6kct6Z9EQ6vzSNx7Qzry5Q），有题目考查： 

<img width="843" height="739" alt="image" src="https://github.com/user-attachments/assets/b4492e3c-542a-4ff1-bbba-02f43cff20c1" />

<img width="845" height="911" alt="image" src="https://github.com/user-attachments/assets/c472abfa-3169-43a4-a6bd-430e6805da6a" />

②降低共识与扩展成本
乍一看，是不是反了，应该是“扩展共识与降低成本”？不过看文中内容，作者好像就是想说标题里的意思。
③腾讯理财通、广发证券信息技术部
⑨这也是广发证券将复杂的金融业务落地成技术系统时积极尝试探索的路径。
意思是这篇文章是有官方背书的——这也是我专门为此写文章的原因。上一次评点的文章也是用京东来背书：“京东云开发者DDD妙文欣赏（1-4合集）”（https://mp.weixin.qq.com/s/lU-PSXHTyVORIcUuvelnRw）。
如果只是个人的心得感受，没有拉官方背书，也没有开宗布道，写得再离谱，我也不会写文章评点，像下面这些最近几天出来的DDD饭圈文，看起来是个人感受，我也不会专门写文章批评。 

<img width="1029" height="599" alt="image" src="https://github.com/user-attachments/assets/7eb45522-2f79-4b8f-b77d-87af44924ffc" />

<img width="833" height="847" alt="image" src="https://github.com/user-attachments/assets/2e0e2bbf-154e-4787-be7c-f82a4df6f418" />

甚至有更肉麻的吹捧DDD的内容，但明显看出来是培训公司卖课的（不同于有名有姓的“DDD专家”开宗布道），我也不会写文章批评。
④一个实例
文章开头说明，前面还有一篇《架构整洁之道|关于DDD的实战落地分享》（https://mp.weixin.qq.com/s/boorTsBB-LcbpWd6m1R3Ig）。
点击去看这篇“实战落地分享”，举的例子既不是腾讯理财通，也不是证券，而是网购。
好吧，网购就网购，但是在列了两个类UserInfo和UserExtInfo（每个类后面加一个Info，这属于我批评过多次的废话刷工作量，后面文章再详谈）之后，就开始大谈仓储、服务。
以下文章谈了这个问题：
★《软件方法（第3版）》第1章（umlchina.com/url/softmeth2024.html） 

<img width="877" height="967" alt="image" src="https://github.com/user-attachments/assets/835268e8-4595-4cb9-a9ca-3b6071178ac2" />

★《软件方法》强化自测题-总纲（3）（https://mp.weixin.qq.com/s/6kct6Z9EQ6vzSNx7Qzry5Q）：

<img width="513" height="1003" alt="image" src="https://github.com/user-attachments/assets/a1990460-5983-45b7-8ffd-89ed78197b2a" />

★是不是互联网更适合用DDD（https://mp.weixin.qq.com/s/aLMBioFyukS-KA_ZTl9lJQ）： 

<img width="611" height="955" alt="image" src="https://github.com/user-attachments/assets/5fd02e16-e424-42a6-a6eb-f647e696858a" />

<img width="723" height="861" alt="image" src="https://github.com/user-attachments/assets/00f39d2c-2589-40aa-945b-196553b194ec" />

<img width="833" height="851" alt="image" src="https://github.com/user-attachments/assets/e5eff171-b1b0-4064-8d11-11cc4bf81704" />

⑤DDD本质上是一种业务建模的方法论
虽然这些年我经常评点张逸老师的文章，但张逸老师也没敢这么说啊！张老师在他的书中，开篇就承认DDD缺乏这个、DDD缺乏那个，所以他自己创新了一个过程。这回倒好，“DDD本质上是一种业务建模的方法论”，确实是“革命性创造++”了。
首先，可以看出来，作者应该不知道“业务建模（business modeling）”到底是做什么的。
关于“业务建模”、“业务”、“技术”这些用语上犯的错误，我也写过不少文章：
★“CTO也糊涂的常用术语”（https://mp.weixin.qq.com/s/F0xKgcrSmbMXlAsJey2ncg）： 

<img width="581" height="1029" alt="image" src="https://github.com/user-attachments/assets/c8f38a5c-132a-46e4-a77c-06a72402c3fa" />

<img width="741" height="975" alt="image" src="https://github.com/user-attachments/assets/a606c7c3-461f-4834-8867-f3b880ad4261" />

<img width="837" height="977" alt="image" src="https://github.com/user-attachments/assets/14ea6278-6311-471f-8441-369f02056a50" />

★评张逸的“业务服务”（一）（https://mp.weixin.qq.com/s/rDAnW1JQMwQbnFVLVwdNJQ）： 

<img width="721" height="877" alt="image" src="https://github.com/user-attachments/assets/0c4114f1-29b0-4011-92c8-862e50572fd5" />

★《软件方法》强化自测题-总纲（4）（https://mp.weixin.qq.com/s/Xwigz0CsmPlTSARGMe6GQQ）： 

<img width="745" height="881" alt="image" src="https://github.com/user-attachments/assets/8d00b1fd-7dc7-4bf7-b8a3-576c9b268ffd" />

其次，DDD谈不上什么“方法论”。
DDD属于自己的东西，只是一些零散的心得，如果用原理、原则、模式来套的话，勉强算是模式。
“DDD是分析和设计的一些模式”这个表述勉强可以。其中很多内容既不新、也不深，甚至是错误和倒退的。
以下文章有谈到：
★DDD浮夸，Eric Evans开了个坏头（https://mp.weixin.qq.com/s/fzRG27uyDSWtNN9thi6Lrw）： 

<img width="555" height="975" alt="image" src="https://github.com/user-attachments/assets/a172cd87-0942-4eec-a9c5-396f8095f2c6" />

★领域驱动设计割裂历史，哪里有详细一些的真实历史？（https://mp.weixin.qq.com/s/NmfCoeFp-Qv67JEcMu12CA）： 

<img width="559" height="971" alt="image" src="https://github.com/user-attachments/assets/f511f6be-8717-4933-9b79-a894be58cf73" />

<img width="433" height="1015" alt="image" src="https://github.com/user-attachments/assets/5e76eb93-690b-4143-90bc-d039363d8893" />

⑦各类对象及行为
不知道作者有没有想清楚他说的“对象”指的是像上面图9的“餐馆系统”（业务建模的业务实体对象）还是图9下面的类图上的“菜品”、“订单”（分析中的实体类对象）？
⑧技术建模
即使欣赏过许多DDD妙文和造词，但“技术建模”这个新词，我还是第一次看到。
可能作者觉得，既然有“业务建模”的说法，那也应该有“技术建模”吧？
根据上面关于“业务”的讲解，读者应该可以看出来，和“业务建模”的“业务”对立的并不是“技术”，而是“系统”，和“业务规则”的“业务”对立的才是“技术”。
无独有偶，前面评点过的⑨“广发证券将复杂的金融业务落地成技术系统”，这个“技术系统”也是非常新颖。
对这种乱用词的现象，我写过以下文章：
★为什么要对术语"吹毛求疵"（https://mp.weixin.qq.com/s/a1_UCtZZmCGigyYTivOqdA）： 

<img width="587" height="953" alt="image" src="https://github.com/user-attachments/assets/6d2033a1-6b55-4db3-9930-275306b7f370" />

<img width="583" height="927" alt="image" src="https://github.com/user-attachments/assets/6c1dded7-bf93-4aa5-9b9a-9fbb9b50275b" />

<img width="693" height="907" alt="image" src="https://github.com/user-attachments/assets/919a8ff4-7cc5-4a92-ad8a-f0daccfbafae" />

关于造词的手段，在《软件方法》中有剖析：
★《软件方法（第3版）》第1章（umlchina.com/url/softmeth2024.html） 

<img width="809" height="961" alt="image" src="https://github.com/user-attachments/assets/0dbbc412-f1f1-4588-b241-decccb31902d" />

<img width="685" height="945" alt="image" src="https://github.com/user-attachments/assets/a202322b-43f1-45c1-bae7-b134f628082e" />

<img width="711" height="927" alt="image" src="https://github.com/user-attachments/assets/2634e5aa-0763-4d0e-a0ec-1c4abe0a4767" />

“业务建模→技术建模”，属于上文的mX→nX。
我们可以把以上列举的造词手段都用上，看如何能造一个更精彩的词。
先换词。
“技术”这个词老旧了，改成“手艺”，一股浓浓的敏捷和DDD的味道就出来了。
“建模”这个词老旧了，改成“麻豆塑形”，够时尚。
现在得到：手艺麻豆塑形。
接下来，加前缀。
敏捷数智化AI赋能业务用户领域功能手艺麻豆塑形
然后，加后缀。
敏捷数智化AI赋能业务用户领域功能手艺麻豆塑形逻辑技术架构设计风暴
大功告成。
另外，“技术”一词也是模糊用语。见以下文章：
★《软件方法（第3版）》第8章（umlchina.com/url/softmeth2024.html）： 

<img width="945" height="919" alt="image" src="https://github.com/user-attachments/assets/31287d46-3348-44d2-ac5f-e768b4f23fa9" />

<img width="721" height="957" alt="image" src="https://github.com/user-attachments/assets/b504b761-7edd-4302-a1b9-9e231d3b4f83" />

<img width="695" height="963" alt="image" src="https://github.com/user-attachments/assets/537fced6-278a-4f3b-a58f-741ba4c1a31d" />

我的这第一篇“解密”文章的最后，请大家做一道题：
1 [单选] 
如果穿越回30年前，叮！系统（金手指）发布任务：通过【公关策划】手段，10年内让“武德驱动设计”包揽每一年的诺贝尔物理、化学、生理学奖！
任务成功，则延寿九千岁，任务失败，则形神俱灭。 
假设有以下候选步骤：
1. 介绍本世纪以来每一年的诺贝尔物理、化学、生理学奖，称赞这些成果符合“武德驱动设计”的精神
2. 全球组圈子，散布“武德驱动设计是一种强力推动人类文明发展的科学”的说法
3. 逐渐建立“凡是强力推动人类文明发展的科学就叫武德驱动设计”的思想钢印
4. 提出“武德驱动设计”的口号，把它定义为“一种强力推动人类文明发展的科学”
5. 认真研究怎样做到强力推动人类文明发展，包括认真研究如何联系三体人
6. 认真研究当前科学各学科的最大发展障碍
请问，这些步骤的最合理顺序是：
 A) 6→4→1→2→3→5
 B) 3→2→1→4
 C) 1→4→2→3
 D) 4→1→2→3
 E) 4→2→1→3
 F) 6→3→2→1→4
后面的解密待续……
