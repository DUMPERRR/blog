例如，用EA在BDD（块定义图）上画了一个关联：

<img width="638" height="281" alt="image" src="https://github.com/user-attachments/assets/2d33e941-34c1-42fd-8ca1-83caa475b4d0" />

此时，“手机”和“SIM卡”中都没有出现references栏。

右击“手机”，选“Compartment Visibility”，也没有看到可以勾选的references选项。

<img width="591" height="290" alt="image" src="https://github.com/user-attachments/assets/44e51953-cd78-41bc-9d22-03ecb109a1d0" />

<img width="793" height="561" alt="image" src="https://github.com/user-attachments/assets/19b0868d-7556-43a5-9620-52d14bc9adad" />

此时由于图上可以看到关联关系，信息倒也没有缺失，但是，把“SIM卡”从图上删除，也没有出现references栏。

此处，需要通过IBD（内部块图）同步一下：

右击“手机”，选择“Internal Block Diagram”，创建“手机”的IBD：

<img width="811" height="581" alt="image" src="https://github.com/user-attachments/assets/d133fc62-f2f5-4fe7-b99b-af31ce58f1d9" />

然后，右击IBD的空白处，选择“Synchronize Structural Elements”

<img width="628" height="329" alt="image" src="https://github.com/user-attachments/assets/e68a8250-cac0-4cca-922f-988e4642e8e6" />

此时，IBD中出现了“SIM卡”，切回到BDD，references分栏也出现了：

<img width="373" height="273" alt="image" src="https://github.com/user-attachments/assets/cf3a2dd4-b89c-4cd5-a254-1123dd53ffd4" />

<img width="669" height="337" alt="image" src="https://github.com/user-attachments/assets/e72d3205-bdb0-46e1-a30e-c1efb6aed8f4" />

从IBD图也可以添加references。把“SIM卡”从Project Browser拖到IBD上，“Drop as”选择“Property”：

<img width="867" height="390" alt="image" src="https://github.com/user-attachments/assets/1ea02c74-6f4c-4981-af2b-92eb49bcaab8" />

然后，在属性框把属性名“Property1”改为“辅卡”：

<img width="566" height="317" alt="image" src="https://github.com/user-attachments/assets/ee417292-17cc-4fba-a995-ccc864618049" />

此时，切回BDD，“辅卡”出现在Properties分栏，而且EA没有在“手机”和“SIM卡”之间创建新的关联线。

<img width="676" height="421" alt="image" src="https://github.com/user-attachments/assets/887d6657-e328-47d7-b967-8812ab2df5d3" />

切回IBD，选中“辅卡”，在属性框的Property栏勾选“Reference”：

<img width="337" height="420" alt="image" src="https://github.com/user-attachments/assets/93b77d0b-ac84-4881-9572-b3401aee20ed" />

切回BDD，“辅卡”出现在References分栏，但 “手机”和“SIM卡”之间仍然没有新的关联线。

<img width="669" height="420" alt="image" src="https://github.com/user-attachments/assets/174013b0-5698-4e8d-974a-e73ccbb28767" />

因此，EA中按照第一种操作，应该是更妥当的做法。

**********

理想的使用场景可能应该是下面这样，不过目前EA没有做到：

在图上创建关联，此时图上已有关联线，references不应该显示该关联。如果从图上删掉引用关联的类，references中出现从图上删掉的引用关联。

IBD上添加了新的引用，也应该同步回BDD，建立新的关联线。
