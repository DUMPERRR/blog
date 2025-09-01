Extreme 2024-4-11 11:36
我从工具栏把一个包拖在另一个包里面，可是项目树上两个包的位置并列，拖了几次结果都一样。我的目的是做一个多层级的包图，是不是（EA）不能在图上做？

<img width="392" height="267" alt="image" src="https://github.com/user-attachments/assets/48de8132-97dc-4ca8-8d57-4e991643ba34" />

<img width="158" height="98" alt="image" src="https://github.com/user-attachments/assets/087db446-5beb-4fab-b9e7-16ced8cbcdff" />

UMLChina潘加宇
确实是这样，但这里不是EA错了。
像下图，在一个已有的包“操作性”的内部加一个新的包“1-需求”，用EA在包图上操作的话，加的时候有个提示，提示中默认这个包的上一级（可以改）是拥有这张包图的那个包，即“安全域to-be”：

<img width="492" height="357" alt="image" src="https://github.com/user-attachments/assets/29844bde-2a3e-43fb-ba9e-10144837ddc6" />

因此在Project Browser文件夹中，两个包在同一层级。

<img width="1080" height="407" alt="image" src="https://github.com/user-attachments/assets/400f0fc2-a897-4e55-bb0a-7edb3b9a69c6" />

但这两个包的容纳（Containment）关系是已经建立了的。
如果把“1-需求”拖到“操作性”外面，可以看到这两个包之间有一个带圈的十字，嵌套和十字的含义是相同的。

<img width="1080" height="343" alt="image" src="https://github.com/user-attachments/assets/f2bdfaa5-455c-440d-931b-5164ab31c56e" />

如果在Project Browser中把“1-需求”挪到“操作性”下面，此时图上“1-需求”下面会出现“from 操作性”的说明。在图上把“1-需求”挪回“操作性”内部，同样有“from 操作性”。这是因为“1-需求”此时已经不是直接被包图的所有者“安全域to-be”包含，如下图：

<img width="1080" height="338" alt="image" src="https://github.com/user-attachments/assets/a8d92d56-ab63-4f59-a0a3-259e1bbd0688" />

我用当前电脑上的其他工具尝试了类似操作。
（1）Astah（日本出产的工具，有英文界面，但这个刚好是日文的）
加上去之后，图上的包含关系和左侧的树是一致的，如下图：

<img width="822" height="506" alt="image" src="https://github.com/user-attachments/assets/142a7a39-385e-4e96-abf0-756a2a45522d" />

把里面的“パッケージ2（package2）”拖到“パッケージ1（package1）”外面，可以看到，确实有带圈十字的包含关系：

<img width="1070" height="473" alt="image" src="https://github.com/user-attachments/assets/01361bff-db08-47f5-bf61-d2315d54b9ae" />

（2）StarUML
刚加上去的时候，在文件夹上，新加的包Package3和外层的包Package2是并列的。稍微拖动一下Package3，它就很神奇地跳到了Package2下面，如下图：

<img width="797" height="368" alt="image" src="https://github.com/user-attachments/assets/76b8349e-c53a-4ba4-b713-584b985ca126" />

把Package3拖到Package2外面，如下图，文件夹上的位置也跟着改变为同一层级，两个包之间没有带圈十字关系。也就是说，之前两个包有没有包含关系不知道，但现在肯定是没有的。

<img width="948" height="331" alt="image" src="https://github.com/user-attachments/assets/ad91dffe-ed3d-4215-bde1-8ab515970f6a" />

这时，从工具栏中选中Containment关系，从Package3画向Package2，随着包含关系的建立，文件夹上Package3的位置挪到了Package2的下面，如下图：

<img width="1050" height="339" alt="image" src="https://github.com/user-attachments/assets/29075b82-54e3-4785-8f54-cf5734e6e853" />

在有包含关系的情况下，在图上把Package3挪回Package2，观察文件夹的变化，再把Package3挪出来，再观察变化，所发生的变化和预期的不一样，这个地方StarUML的逻辑应该乱掉了。
**********
对比此处的操作，Astah默认让文件夹的包含和图上的包含一致（可以不一致），应该更符合心理预期。EA的操作比较特别，StarUML存在逻辑错误。
