<img width="1080" height="789" alt="image" src="https://github.com/user-attachments/assets/01728f37-a87f-42e2-a249-2375459703a2" />Eric Evans在《领域驱动设计》的前言中说：
Leading software designers have recognized domain modeling and design as critical topics for at least 20 years, yet surprisingly little has been written about what needs to be done or how to do it. Although it has never been formulated clearly, a philosophy has emerged as an undercurrent in the object community, a philosophy I call domain-driven design.
领先的软件设计人员认识到领域建模和设计的关键性已经有【至少20年】，然而令人惊讶的是，关于需要做到什么或者如何做，【一直以来几乎没人写点什么】。不过，一种哲学像一股暗流已经在对象社群出现，虽然还从来没有被清晰确切地表述出来。我把这种哲学叫作“领域驱动设计”。
Eric Evans说的20年，指《领域驱动设计》出版时间2003年前面的20年，大约是1983-2002年。
事实和Eric Evans所说的在这个期间“几乎没人写点什么”恰好相反，那个年代的“领域驱动”味道比今天还要浓。
先以Eric Evans的这段文字提到的对象社群来说。如果没有各种面向对象分析和设计方法学，怎么会有UML的出现？
感兴趣的同学可以用object modeling analysis design method 等关键字灵活组合在amazon.com搜2000年之前的书籍，应该可以得到很多结果。
列出一些我认为有价值的面向对象分析设计的早期书籍，这些书籍的内容焦点都放在如何用对象思想去剖析一个领域的复杂性。
1988，Sally Shlaer和Stephen J. Mellor的“Object Oriented Systems Analysis”
1990，Peter Coad和Ed Yourdon的“Object Oriented Analysis (2nd Edition)”
1991，Ian Graham，“Object Oriented Methods”（Ian Graham的书很值得一读）
1991，James Rumbaugh等，“Object-Oriented Modeling and Design”
1992，Stephen J Mellor和Sally Shlaer，“Object Life Cycles: Modeling the World in States”
……
1995，Peter Coad等，“Object Models: Strategies, Patterns, and Applications”（一本案例集）
1996，Edward Yourdon和Carl A. Argila，“Case Studies in Object-Oriented Analysis and Design” （一本案例集）
1996，Martin Fowler，“Analysis Patterns：Reusable Object Models”（分析模式）
1999，Peter Coad等，Java Modeling in Color with UML（彩色UML建模）
……
没提到Grady Booch、Ivar Jacobson、Bertrand Meyer早期的书，也没提到GoF，要么是因为书中“领域”例子太简单，要么这个书就不是说“领域”的。
……
我们从以上列出的书中摘一些图，看看其中的“领域模型”是不是碾压今天大多数把DDD挂在嘴边的“发明家”？
1990年的“Object Oriented Analysis, 2nd Edition”书中的类图：

<img width="1080" height="1303" alt="image" src="https://github.com/user-attachments/assets/43f2cdaf-f9f8-441b-af55-1959990d8a9a" />

可以看到，Peter Coad等把类图划分成若干个主题。
1991年James Rumbaugh的“Object-Oriented Modeling and Design”书中的图更加精细：


<img width="1080" height="1734" alt="image" src="https://github.com/user-attachments/assets/7a164211-f005-415c-82e4-7b81edc2099d" />

<img width="1080" height="1734" alt="image" src="https://github.com/user-attachments/assets/3533fb07-7aec-4e1a-a978-54b6a07b70ea" />

1992年的“Object Life Cycles: Modeling the World in States”中的状态图:

<img width="1080" height="515" alt="image" src="https://github.com/user-attachments/assets/3ffd5761-8f66-4d96-b5f5-6272af2cd03f" />

1995年的“Object Models: Strategies, Patterns, and Applications”是一本案例集，仅能找到第二版中译本，以下是截图：

<img width="1025" height="967" alt="image" src="https://github.com/user-attachments/assets/1ce415f5-fa6b-4c89-a5f9-79abe3d68f38" />

<img width="1080" height="1034" alt="image" src="https://github.com/user-attachments/assets/d6d5409f-be7e-47ae-a3de-92ffbee179a7" />

如果不限于面向对象建模，那方法就更多也更早了，诞生于1976年的实体-关系法、诞生于1981年的IDEF1……。
例如，以下是1990年的“Database Modeling and Design: The Entity-Relationship Approach”中的E-R图：


很多人都知道Martin Fowler写了一本“Analysis Patterns：Reusable Object Models”（分析模式：可复用对象模型），其实，David C. Hay的“Data Model Patterns：Conventions of Thought”出版时间更早，可惜不在那个网红圈子中，国内连中译本都没有。
《设计模式》作者之一Ralph Johnson在《分析模式》书的推荐序中也提到David C. Hay的书：

<img width="763" height="945" alt="image" src="https://github.com/user-attachments/assets/cb28a9b1-e8ef-4144-bb5f-23d578ee9528" />

以下是“Data Model Patterns”中关于“开支”的截图，我认为该书的内容比《分析模式》还要丰富一些。
书中用的表示法是Oracle的“鸦脚”（学名Case*Method）。《分析模式》虽然全名叫《分析模式：可复用的对象模型》，名字里有个“对象”，其实里面用的表示法也是“鸦脚”。


再看一个Tom DeMarco1979年的“Structured analysis and system specification”书中的数据流图：


如果不局限于为了开发某个软件系统而建模，感兴趣的同学还可以用领域工程、领域分析、Domain Engineering、Domain Analysis，甚至软件重用、软件复用、Software Reuse等关键词搜上个世纪的书籍和文章。
用网上搜的一个幻灯片借花献佛吧，幻灯片地址：https://www.doc88.com/p-78061787560101.html?r=1

<img width="794" height="562" alt="image" src="https://github.com/user-attachments/assets/af4018f6-e219-4a45-8b36-0dd32a71911c" />

……
<img width="1013" height="677" alt="image" src="https://github.com/user-attachments/assets/547ccefb-9e4c-42e9-bdfd-6e4da95c6685" />

……
<img width="1053" height="795" alt="image" src="https://github.com/user-attachments/assets/df62af3e-ceeb-4129-8369-f7a6d55fbc85" />

……
<img width="1041" height="731" alt="image" src="https://github.com/user-attachments/assets/5b33bacc-20da-40cf-9dc9-52ac6fbf64d8" />

综上所述，Eric Evans所说的“几乎没人写点什么”是错误的。把前面20年描述成荒漠，为“领域驱动设计”营造横空出世的感觉，这是一种夸大。
上面列出的资料，Eric Evans只在书中提到了Fowler的“Analysis Patterns”，是一无所知，还是刻意忽略，就不得而知了。
《领域驱动设计》阐述了Eric Evans对分析和设计工作流的一些观点，谈不上是方法学。
在不少开发人员误以为会背诵设计模式，再喊几句“针对接口编程”、“分离变化”、“SRP”、“OCP”就算掌握了面向对象建模技能的时候，Eric Evans的书能重新提醒大家还是要聚焦于系统的核心领域，以它来驱动开发。这是值得肯定的。
书中很多地方用了“新式话语”，但内容其实不新，也不深，甚至有的是错误的。
这本来也是可以理解的，但如果有人把这些“新式话语”拿出来刻意夸大，那就要好好说说了。
