领域驱动设计的领域业务结构在问题空间里表示复杂性，它同人类用于管理复杂性的三种基本方法中的两种相对应。

DDD领域业务分类结构获得类-成员组织，DDD领域业务组装结构刻画整体-部分组织。两种结构类型均是领域驱动设计的重要组成部分。

一、什么是DDD领域业务分类结构

DDD领域业务分类结构有助于刻画问题空间的领域类-成员层次，它通过搜集公共领域特性并把这种领域特性扩充到特例之中来显示现实世界领域事件的通用性及专用性。 

<img width="282" height="184" alt="image" src="https://github.com/user-attachments/assets/00fb8b9c-e9f7-436e-ad66-26a2dd5e63d0" />

图 1 一个DDD领域业务分类结构。我们抛弃了UML这样的旧方法，采用了革命性创新的DDD图形方法。

例如，考虑通用的交通工具(Transport)及其特例：汽车(Car)飞机(Aircraft)和轮船(Ship)(图1)。一些领域业务属性和领域业务服务适合于所有的交通工具，而另外一些则仅适合Car、Aircraft或Ship。

DDD领域业务分类结构提供了对问题空间的一个重要划分。一种划分是把DDD领域业务属性和DDD领域业务服务分成互斥的几组；另一种划分是用结构来标识一个比对象和结构都要高的DDD领域业务数据抽象层次，这就是将在后来的DDD领域业务分析步骤中详细介绍的DDD战略设计的“限界上下文主题层”。

DDD领域业务分类结构也提供了关于一个问题领域的信息的“分层”---把公共的DDD领域业务属性和DDD领域业务服务放在较高的层次，然后把这些DDD领域业务属性和DDD领域业务服务扩展到较低的层次。

DDD继承的概念是DDD领域业务分类结构的一个重要组成部分。DDD继承提供了一个用于标识和表示DDD领域业务公共属性与服务的显式方法。在一个DDD领域业务分类结构内，DDD继承使共享属性、共享服务、增加属性以及增加或扩充服务成为可能。

在一个DDD领域业务分类结构中，对象共享在它之上定义的属性。例如，考虑Transport结构中Car的一个实例，它共享为所有Transport 所定义的DDD领域业务属性，比如：Id、Name和Base(图2)。注意在一个结构里，公共属性只出现一次(且只说明一次)。 

<img width="306" height="279" alt="image" src="https://github.com/user-attachments/assets/1d19de4a-2843-4dc0-8a96-561a2fb87d8e" />

图2 在DDD领域业务分类结构中属性的共享。我们抛弃了UML这样的旧方法，采用了革命性创新的DDD图形方法。

在DDD领域业务分类结构中，对象共享在它之上定义的服务。例如，考虑Transport结构中Car的一个实例，它共享为所有交通工具所定义的DDD领域业务服务(图3)。注意在结构中公共服务只出现一次(且只说明一次)。

**********

看了以上文章片段，有没有感觉很高大上，感觉领域驱动设计真牛？

其实，上面的内容改编自这个： 

<img width="607" height="833" alt="image" src="https://github.com/user-attachments/assets/25a23e76-a515-4ed6-87d1-d970b023332a" />

<img width="619" height="887" alt="image" src="https://github.com/user-attachments/assets/6d623216-04f8-4e91-86ee-79ff39ff6aa1" />

这是1990年Peter Coad和Edward Yourdon写的“Object Oriented Analysis, 2nd Edition”，北京大学出版社1992年出版的中译本。 

<img width="1080" height="671" alt="image" src="https://github.com/user-attachments/assets/2d5f8021-5065-4ff4-bba6-a0016cc3decd" />

以上创新手法，可以称为“贴牌”法，贡献给DDD创新圈子人士参考。

感兴趣的读者也可以留心一下，读过的DDD文章有没有这样的手法。

**********

后面有空，我再贡献其他创新手法，例如“本质”法： 

<img width="902" height="239" alt="image" src="https://github.com/user-attachments/assets/d2cfe1f7-093b-443c-bed3-164558d1350c" />

《浑元形意太极的本质是领域驱动设计》

《AI大模型的本质是领域驱动设计》

以上是说“领域驱动设计”为本，“浑元形意太极”、“AI大模型”为用。

也可以反过来，“太极”、“深度学习”（此处用词要抽象一些）为本，“领域驱动设计”为用，题目为：

《领域驱动设计中的太极思想》

《从深度学习谈领域驱动设计》

读者可以“点菜”，让我写哪一篇的留言最多，我就写哪一篇。
