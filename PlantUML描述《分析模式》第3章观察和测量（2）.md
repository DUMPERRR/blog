原图3.8

<img width="1080" height="329" alt="image" src="https://github.com/user-attachments/assets/b0ec09a7-894d-4ad6-8e67-1a62fda8bef8" />

EA绘制

<img width="415" height="230" alt="image" src="https://github.com/user-attachments/assets/0db7743b-29e1-47c1-9fbf-08e8796be147" />

图3.8 递归关系用于记录证据和评估。

PlantUML

@startuml

class 观察



观察 -- "-证据s 0..*" 观察

观察 -- "-评估s 0..*" 观察

@enduml

<img width="305" height="140" alt="image" src="https://github.com/user-attachments/assets/962d1502-e266-44f0-8383-68f334af682c" />

原图3.9

<img width="1080" height="525" alt="image" src="https://github.com/user-attachments/assets/96743e29-67d2-4f58-8115-7a7c1feb21b6" />

EA绘制

<img width="740" height="589" alt="image" src="https://github.com/user-attachments/assets/091d15dd-95a4-49b7-969a-0ad3e4d7ee33" />

图3.9 知识级中的现象(之前叫类别)。

将定性陈述(如血型A)放在知识级，就可以在规则中使用它们。

PlantUML

@startuml

skinparam ranksep 60

skinparam nodesep 120



class 人

class 观察

class 数量

class 测量

class 类别观察

class 现象类型

class 现象



观察 <|-- 测量

观察 <|-- 类别观察



人 "1" -- "0..*" 观察

数量 "1" -right- "0..*" 测量

测量 "0..*" -- "1" 现象类型

类别观察 "0..*" -- "1" 现象

现象类型 "1" -- "0..*" 现象

@enduml

<img width="903" height="928" alt="image" src="https://github.com/user-attachments/assets/0a76835f-cdd9-457f-a0af-d22e0cef8fa6" />

原图3.10

<img width="1080" height="743" alt="image" src="https://github.com/user-attachments/assets/c75fb7ec-b8bf-430e-bc23-b88eecbc2576" />

EA绘制

<img width="1080" height="659" alt="image" src="https://github.com/user-attachments/assets/0abe134a-36dc-426a-89c4-085979c3c717" />

图3.10 观察概念的不存在和存在。

现象的不存在和发现现象的存在一样有价值。

PlantUML

@startuml

skinparam ranksep 50

skinparam nodesep 100



class 现象类型

class 协议

class 现象

abstract class 观察概念 {

  .. constraints ..

  {not 超类型s.closure(超类型s)->includes(self)}

}



class 人

abstract class 观察

class 测量

class 类别观察

class 数量

class 不存在

class 存在



协议 -[hidden]- 观察概念

观察概念 -[hidden]down- 观察



现象类型 "1" -- "0..*" 测量

现象类型 "1" -right- "0..*" 现象

观察概念 "-超类型s\n0..*" -- "0..*" 观察概念

观察概念 "1" -- "0..*" 类别观察

人 "1" -right- "0..*" 观察

测量 "0..*" -- "1" 数量

协议 "0..1" -- "0..*" 观察



观察概念 <|-up- 现象

类别观察 <|-- 不存在

类别观察 <|-- 存在

观察 <|-- 测量

观察 <|-- 类别观察

@enduml

<img width="969" height="496" alt="image" src="https://github.com/user-attachments/assets/1fc7e190-52fe-4bed-9bb4-b74f59b64c9e" />

原图3.11

<img width="1080" height="693" alt="image" src="https://github.com/user-attachments/assets/20760a8e-968c-4c67-a455-24dd690796f1" />

EA绘制

<img width="800" height="551" alt="image" src="https://github.com/user-attachments/assets/02ef4d20-7464-4e8a-abaa-d1cd26a17328" />

图3.11 观察的双重时间记录。

时间记录既允许记录时间段，也允许记录单个时间点。大多数事件的发生时间和记录时间是分开的。

PlantUML

@startuml

skinparam ranksep 60

skinparam nodesep 120



class 观察

class 时间记录

class 时间点

class 时间段



时间记录 <|-- 时间点

时间记录 <|-- 时间段



观察 "0..*" -- "-适用1" 时间记录

观察 "0..*" -- "-记录时间1" 时间记录

时间点 "-开始1" -- "0..*" 时间段

时间点 "-结束1" -- "0..*" 时间段

@enduml

<img width="413" height="613" alt="image" src="https://github.com/user-attachments/assets/2319821e-4b21-4f98-bc7d-09db743ca6d9" />

原图3.12

<img width="949" height="381" alt="image" src="https://github.com/user-attachments/assets/4f422229-21cd-4e66-99ba-8dc275490099" />

EA绘制

<img width="315" height="355" alt="image" src="https://github.com/user-attachments/assets/f5fd56f5-0f53-4946-a1c1-3ec0d2d63594" />

图3.12 被否决的观察。

如果需要完整的审计跟踪，观察不能被删除。

PlantUML

@startuml

class 观察

class 被否决观察



被否决观察 --|> 观察

观察 "1" -- "0..*" 被否决观察

@enduml

<img width="171" height="264" alt="image" src="https://github.com/user-attachments/assets/b4392c14-0984-4b56-b623-6312e03e5b1c" />

原图3.13

<img width="1080" height="229" alt="image" src="https://github.com/user-attachments/assets/38be2325-3784-49b0-ad52-0daa76a458d3" />

EA绘制

<img width="584" height="333" alt="image" src="https://github.com/user-attachments/assets/2cd7a645-971d-4738-875a-3c71a447216b" />

图3.13 有效观察、假设和预测。

PlantUML

@startuml

class 观察

class 假设

class 预测

class 有效观察



观察 <|-- 假设

观察 <|-- 预测

观察 <|-- 有效观察

@enduml

<img width="449" height="271" alt="image" src="https://github.com/user-attachments/assets/94a5d197-dd38-49e0-8277-9875d91e0a5a" />

原图3.14

<img width="1080" height="742" alt="image" src="https://github.com/user-attachments/assets/10d82f4c-9e77-4b05-9478-f1dcfcf26c53" />

EA绘制

<img width="585" height="461" alt="image" src="https://github.com/user-attachments/assets/e8271ed6-91dc-4fd1-881a-1da2691e9df5" />

图3.14 观察之间的链接。

患者的实际证据链记录在操作级。知识级描述了什么链是可能的。

PlantUML

@startuml

skinparam ranksep 60

skinparam nodesep 140



class 关联函数

class 观察概念

class 观察

class 关联观察



观察 <|-- 关联观察



关联函数 "0..*" -right- "-参数s\n1..*" 观察概念

关联函数 "0..*" -- "-产出1" 观察概念

观察概念 "1" -- "0..*" 观察

关联函数 "1" -- "0..*" 关联观察

观察 "1..*" -- "-证据s\n0..*" 关联观察

@enduml

<img width="1080" height="922" alt="image" src="https://github.com/user-attachments/assets/4d116e92-ad00-4e5f-8111-d1ca8ae3f8ea" />
