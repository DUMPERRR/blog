接下来，按照下图添加上其他的包： 

<img width="641" height="667" alt="image" src="https://github.com/user-attachments/assets/b2566b57-6b79-4e27-b0d3-27fa25d4923a" />

步骤 2.2 

选中Browser中的“蒸馏器项目”，点击New Package（Browser工具栏左起第二个图标），在New Package对话框的Name栏输入“蒸馏器需求”，点击OK。 

<img width="1074" height="464" alt="image" src="https://github.com/user-attachments/assets/cf7550d2-40c8-4679-8030-383a24fa15a3" />

<img width="354" height="263" alt="image" src="https://github.com/user-attachments/assets/711df39e-9f11-4332-b2a6-8b8a1de493c7" />

步骤 2.3

同上步骤，继续添加以下包：

蒸馏器用例

蒸馏器行为

蒸馏器结构

项类型

值类型

工程分析

步骤2.4 创建包图

在Browser中右击“蒸馏器项目”，从快捷菜单选择“Add Diagram”。 

<img width="423" height="591" alt="image" src="https://github.com/user-attachments/assets/d732bd5f-9507-4db0-9c33-0949b262f36f" />

在New Diagram对话框的Select From列表框选择SysML 1.5，然后在右侧的Diagram Type列表框选择Package，在Diagram栏输入“模型组织”。 

<img width="892" height="641" alt="image" src="https://github.com/user-attachments/assets/ea340b74-81ab-45d6-8b10-523186890cb2" />

此时，得到空白的包图： 

<img width="575" height="253" alt="image" src="https://github.com/user-attachments/assets/78049103-5b81-4ccb-b1e5-b4f3d26b68a8" />

步骤2.5 将各个包拖入包图

按住Browser中的“蒸馏器需求”包，拖到图上松开，从弹出菜单选择“Package element”。 

<img width="1080" height="250" alt="image" src="https://github.com/user-attachments/assets/9f108d6d-bcf4-4d18-9df2-e5ee5a95a5e0" />

<img width="587" height="350" alt="image" src="https://github.com/user-attachments/assets/60e8b4ec-2946-4b66-9e1a-c3d552e30af9" />

同上，拖入其他包。 

<img width="537" height="672" alt="image" src="https://github.com/user-attachments/assets/eb8d8b2f-3c1f-4427-b139-21ad74b58169" />

可以把包对齐一下： 

<img width="623" height="975" alt="image" src="https://github.com/user-attachments/assets/385d8aec-69fe-47f1-b7b3-8fa0028e946c" />

步骤2.6 添加import关系

Import的意思是一个包可以引用另一个包的内容，和Java编码中的import类似。

在工具箱的SysML Model Relationship中找到Import，选中，然后，在包图上，将鼠标从“值类型”拖到“ISO-80000”。 

<img width="680" height="642" alt="image" src="https://github.com/user-attachments/assets/d57281c1-e937-4610-b0af-b18ca92238d4" />

步骤2.7 为ISO-80000包添加构造型

双击“ISO-80000”包，然后点击Stereotype栏右侧的按钮。 

<img width="1080" height="577" alt="image" src="https://github.com/user-attachments/assets/8b88e72d-cbe6-4606-9977-b50b10ac2415" />

在弹出对话框的Stereotypes中选择ModelLibrary。

<img width="793" height="674" alt="image" src="https://github.com/user-attachments/assets/24815eab-3b3c-4419-be9b-ce3baa3a99b5" />

<img width="498" height="632" alt="image" src="https://github.com/user-attachments/assets/733184e3-4265-427b-a43b-17f3113a0bf0" />

但此处要注意，ModelLibrary上方的Profile栏说明它是UML的Profile。如果在Profile栏选择SysML 1.5，则没有ModelLibrary选项，所以，我们就先用UML Profile的ModelLibrary代替了。 

<img width="497" height="500" alt="image" src="https://github.com/user-attachments/assets/3909c87e-de03-45fc-a419-fbc9d6eaa65b" />
