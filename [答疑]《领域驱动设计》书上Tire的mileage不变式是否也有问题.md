Seven 2024-5-31 21:23
潘老师，我记得您写过要注意不变式写成等式的情况，领域驱动书上面的这个图，圈出的不变式是一个等式，是不是也有问题？

<img width="996" height="652" alt="image" src="https://github.com/user-attachments/assets/49bcb3fd-1a72-4b65-baf8-d7e8a5fc672e" />

UMLChina潘加宇

应该是有问题的。

Tire的mileage属性是一个冗余，花括号里的“不变式”其实是这个冗余属性的算式，说Tire的mileage是怎样算出来的。

我在文章《续1-续3：你的医书是假的！》里批评的“不变式”，有可能就是模仿这个图。

★在之前的答疑《领域驱动设计》里的这个不变式是不是也是错的，也列出了圈子对书中另一张错误图的模仿。

如果这样可以，领域驱动设计投资少、见效快、产量高、门槛低、仪式感十足的特点真的要充分发挥了。

我们可以随意添加可计算的冗余：

例如，在Car类中也加一个mileage属性，然后，再加一个“不变式”{mileage=sum（Tile. mileage）}。

例如，在Car类中再加一个positionstimeperiod集合属性，记录该Car的所有Tire的所有Position的time period，然后再配上一个“不变式”（此处作者删除若干字。删除？我看你是写不出来吧？）

*****以下是扩展*****

什么情况下不变式可以是等式？

涉及到的属性（关联）不是冗余的就行。知识点看《软件方法》第8章（umlchina.com/url/softmeth2024.html），可重点看“8.2.5 审查类和属性”和“8.3.4.1 关联是不得不记住的关系”。

我还是用《续1-续3：你的医书是假的！》里的订单例子举例，像下面这个不行：

<img width="1080" height="249" alt="image" src="https://github.com/user-attachments/assets/3f3c466d-1e91-48d0-9ed5-061f067745d2" />

这个图和问题中的图是类似的，总价是可计算的冗余属性，本来就不应该存在。

下面这个可以：

<img width="1080" height="451" alt="image" src="https://github.com/user-attachments/assets/4831421d-c7ee-431e-aa9e-e8f28a8a728a" />

订单的配送项信息不是（也不能）从订单的订单项信息计算出来。订单的配送项存在多种可能，但不管是哪一种，上图最左侧关于“订单”的约束必须要遵守。

上图最左侧的约束是以自然语言表达的，严格来说只能算是约束的名称或描述，如果用OCL等形式化语言来表达约束内容，这个表达式就比较复杂了。以下是在AI帮助下得到的，看起来像是对的（OCL语法我也不熟）：先定义两个统计集合，然后比较两个统计集合。

<img width="957" height="795" alt="image" src="https://github.com/user-attachments/assets/4dee8028-56c7-487e-97c8-7b7545198550" />

（严格来说，应该是已完成的订单，此处就不花精力完善了。）
