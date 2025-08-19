二、创建项目的包图

项目的包图，即书上的图16.1，如下： 

<img width="641" height="667" alt="image" src="https://github.com/user-attachments/assets/16a9d3f6-f399-44c2-9cf0-7c62298839ea" />

一共有8个包，当然，包名“Distiller ***”中的“Distiller”属于批量刷废话，可以删掉。但为了尊重原来的教程，我们建模时就不删了。

ISO-80000是外部的一个模型库，是ISO量和单位的标准。

EA16版本里面自带了添加ISO-80000库的菜单，因此可以直接在EA里面操作。如果是更早的EA版本，需要从OMG的网站下载XML文件，然后导入该文件。

步骤2.1 导入ISO 80000（EA16）

右击Browser中的“蒸馏器项目”，从快捷菜单选择Add a Model using Wizard。 

<img width="473" height="647" alt="image" src="https://github.com/user-attachments/assets/58d51f60-5328-435d-b1d8-cbdc531ee0af" />

在列表中找到SysML 1.5 Libraries下面的ISO 80000 Library，右击，从快捷菜单选择Create in Project。 

<img width="589" height="743" alt="image" src="https://github.com/user-attachments/assets/199267cb-2e49-4921-afcb-b4413bae66f8" />

导入的过程耗费一些时间： 

<img width="369" height="217" alt="image" src="https://github.com/user-attachments/assets/edf0212b-e2e1-49e0-9448-aff7f1145f5f" />

导入完成后，可以看到，Browser中的“蒸馏器项目”下面多了一个包“ISO-80000” 

<img width="331" height="363" alt="image" src="https://github.com/user-attachments/assets/db61438b-c7c9-49d0-9b3e-e2414a1f79b3" />

步骤2.1 导入ISO 80000（EA15或之前版本）（可选）

访问OMG的网站，下载xmi文件，地址为：

https://www.omg.org/spec/SysML/1.5/About-SysML/ 

<img width="1080" height="308" alt="image" src="https://github.com/user-attachments/assets/46cb1bff-6ac4-4a51-b111-5b3f98d0b440" />

下载完毕后，在工具栏选择Import-XML | Import Package from XMI： 

<img width="360" height="255" alt="image" src="https://github.com/user-attachments/assets/bc40f9b3-4480-49a8-a4b9-c36eda113bee" />

在对话框的Filename栏选中刚下载的xmi文件，点击Import按钮，弹出窗口点击“是”。 

<img width="572" height="522" alt="image" src="https://github.com/user-attachments/assets/7338d771-28dc-445d-b7d4-0441ea462da9" />

在这个过程中，如果出现错误提示，不用管它，点击“确定”跳过去。 

<img width="652" height="536" alt="image" src="https://github.com/user-attachments/assets/88a7011a-7bec-4210-ad96-5ce26569a919" />

导入完成后，可以看到Browser中多了一个包“ISO-80000”：

<img width="369" height="516" alt="image" src="https://github.com/user-attachments/assets/25836444-07b8-4021-867e-91a84b5cd10a" />
