# [评析]评XXX布道师关于DDD和敏捷的观点

---

刚发了这篇“评Thoughtworks 首席咨询师林宁的《OOP 和 DDD 其实就是对现实的比喻》（https://mp.weixin.qq.com/s/IRPiaDD-C2ZnolWO0op0jQ）”，又在b站看到一个更敢说的DDD布道师。

我们来看第一段视频（字幕是我配的）：

<img width="570" height="570" alt="image" src="https://github.com/user-attachments/assets/4aebe573-08b4-4945-b773-ce391c019516" />

这位DDD布道师说：
> 先去对问题进行分析设计，得到模型之后，再用软件把模型给实现，你就可以宣称我就是用了 DDD了，我就是用了DDD的方法论了，你就是属于Domain-Driven Design了。
> 叫原来的词“分析设计”或“建模”不行吗，为什么要造一个词“领域驱动设计”呢？

★该DDD布道师把建模等同于分析设计，这是另外一个问题了。

这是伪创新的一个常用手段。我之前文章中说过的“武德驱动设计”：
**如何让“武德驱动设计”包揽每一年的诺贝尔物理、化学、生理学奖？**
1.  提出“武德驱动设计”的口号，把它定义为“一种强力推动人类文明发展的科学”；
2.  全球组圈子，散布“武德驱动设计是一种强力推动人类文明发展的科学”的说法；
3.  称赞历年的诺贝尔物理、化学、生理学奖符合“武德驱动设计”的精神；
4.  建立“凡是强力推动人类文明发展的科学就叫武德驱动设计”的思想钢印。

这样的现象在1895年（清光绪21年）勒庞的《乌合之众》中有描述：

<img width="1080" height="990" alt="image" src="https://github.com/user-attachments/assets/6a60aa3b-c15e-4f73-b0c5-daef7aa3a770" />

勒庞所说的现象，在软件开发领域的一个例子就是“敏捷”，关于“敏捷”的话术，我在《软件方法》（ http://umlchina.com/url/softmeth2025.html）有详细描述。
前些年，伪创新以“敏捷”为名。“敏捷”的真相逐渐暴露，名声变差之后，伪创新转而以“DDD（领域驱动设计）”为名。细心观察可以发现，两者背后的主要推手是同一批人。

我们来看第二段视频：

<img width="570" height="570" alt="image" src="https://github.com/user-attachments/assets/267a7c20-d8a2-4ca2-ab69-3174c822276a" />

这位DDD布道师说：
> 除了面向对象的领域模型，其他的领域模型理论上也是可以有的，但实际上大家做的比较少，也没有什么相关这方面资料。

分析设计在1950年代就开始了，面向对象分析设计直到1980年代末才开始。

以下摘自《软件方法》（ http://umlchina.com/url/softmeth2025.html）第8章：

<img width="1080" height="319" alt="image" src="https://github.com/user-attachments/assets/09b8792d-1901-48e3-9456-dee7151d8316" />

但凡认真看过一本面向对象分析设计方法学家的书，也不至于说出这样的暴论，因为作者在讲述自己的面向对象分析设计方法学之前，会讲述这个方法学之前的历史。
之前的方法学家还是讲究的，不会像Eric Evans那样，一张嘴就是“至少20年以来几乎没人写点什么”，参见：

* DDD浮夸，Eric Evans开了个坏头，https://mp.weixin.qq.com/s/fzRG27uyDSWtNN9thi6Lrw
* 我为什么写《DDD浮夸，Eric Evans开了个坏头》，https://mp.weixin.qq.com/s/wOhbtZ73svvCd5IHJJlNtA

看起来，这位DDD布道师只不过是传承了Eric Evans的风格。
* Eric Evans：领域驱动设计之前的面向对象分析设计是空白；
* 这位DDD布道师：除了面向对象分析设计之外的分析设计是空白。

我们来看第三段视频：

这位DDD布道师说：
> 事件风暴也不是唯一的建模过程，还有别的建模方法论，我这里只是列出了一个目前最成熟最常用的一个建模方法论，叫事件风暴。

是吗？那说说，其他面向对象建模方法有哪些缺点，事件风暴“成熟”在哪里？
我在《潘老师，你的气度有点小了！》（https://mp.weixin.qq.com/s/1ne1HLBuf-O8oUkmiZLPaA）里说过：

<img width="557" height="900" alt="image" src="https://github.com/user-attachments/assets/a37b8fc2-fd9d-43ba-9e9f-6bb636b98839" />

关于事件风暴，我写过以下文章：

* 《软件方法2022版》第8章，https://mp.weixin.qq.com/s/8rHVc6KA6D5BN7AV6lN-HQ，其中的“伪创新例二”
* 拯救中国足球，要不尝试一下DDD事件风暴？，https://mp.weixin.qq.com/s/LgKyFvo9IAA7Hd2nsPm0Ug

读者也可以看看始作俑者Alberto Brandolini的书，全书299页，大部分篇幅谈仪式感，建模的理论基础呢？
“邓宁-克鲁格效应”归纳的就是这样的“饭圈”现象。感兴趣的读者可以自行搜索。
我只质疑了“最成熟”的说法，并未敢质疑“最常用”的说法，没准投票哪个“最受欢迎”，“事件风暴”遥遥领先都有可能。

对此，我写过以下内容：

* 《软件方法》（ http://umlchina.com/url/softmeth2025.html）第1章，1.2.4.3 伪创新泛滥，谈到了伪创新为什么受欢迎
* 可以跨专业做软件，怎么就不能跨专业做医生？，https://mp.weixin.qq.com/s/EATm8U7TBByFt6kYxDJ6Zw，谈到了软件业伪创新盛行的原因。

**********

还是昨天我在“评Thoughtworks 首席咨询师林宁的《OOP 和 DDD 其实就是对现实的比喻》（https://mp.weixin.qq.com/s/IRPiaDD-C2ZnolWO0op0jQ）”中说的：
如果只是随便写写个人见解，我不会专门写文章批评，既然要布道，那就有必要说一说了。
邻居大爷坚持认为“张三和李四一前一后走，张三突然转身撞到李四，张三倒地受伤，这个情况李四该赔，谁让李四没保持安全距离！”，这是邻居大爷的自由。
如果法律人用这样的例子给大众普法，那就有必要说一说了。

**********

从林宁到这位DDD布道师，没有认真研究过面向对象建模的人，说出各种奇谈怪论，说自己在推广面向对象建模。
可能会有人有这样的看法：别管人家怎么乱说，至少人家推崇面向对象建模，是好事啊！
如果是这样，也就应该感谢韩法官，毕竟人家也是在推动法治建设嘛，还要感谢“武德驱动设计”，推广了诺贝尔奖和科学。

《软件方法》（ http://umlchina.com/url/softmeth2025.html）第1章：

<img width="1080" height="293" alt="image" src="https://github.com/user-attachments/assets/b988ae18-aa71-49b3-b9b5-55fa79f297c0" />
