<img width="782" height="653" alt="image" src="https://github.com/user-attachments/assets/5dacb6f1-7cc1-4f11-8bae-894caa0f299e" />原图2.8

<img width="1080" height="714" alt="image" src="https://github.com/user-attachments/assets/954f2441-2615-4ce6-9d12-35290d39b52f" />

EA绘制

<img width="825" height="576" alt="image" src="https://github.com/user-attachments/assets/2f48a1e5-46e9-419c-af49-ebe3b80c93ad" />

图2.8 当责。

使用当事者，当责可以涵盖广泛的当事者间责任，包括管理、雇佣和合约。

PlantUML

@startuml

skinparam linetype ortho

skinparam ranksep 60

skinparam nodesep 120



class 当责类型

class 当责

class 时间段

class 当事者

class 人

class 组织



当责类型 "1" -- "0..*" 当责

时间段 "1" -- "0..*" 当责

当责 "0..*" -- "-委托方1" 当事者

当责 "0..*" -- "-责任方1" 当事者



当事者 <|-- 人

当事者 <|-- 组织



当责类型 -[hidden]down- 当责

当责 -[hidden]down- 时间段

当责 -[hidden]right- 当事者

当事者 -[hidden]right- 组织

@enduml

<img width="733" height="449" alt="image" src="https://github.com/user-attachments/assets/115047a4-2a06-4d0c-bd60-7acbd340c4c2" />

原图2.9

<img width="1080" height="957" alt="image" src="https://github.com/user-attachments/assets/c7e92452-6700-43a7-8d82-1aedafbce38f" />

EA绘制

<img width="1080" height="665" alt="image" src="https://github.com/user-attachments/assets/ac50e5fe-b7cd-49c9-8112-fcd7c4bf4dce" />

图2.9 当责的知识级和操作级。

知识级对象定义操作级对象的合法配置。只能根据相应的当责类型和当事者类型在当事者之间创建当责。

PlantUML

@startuml

skinparam ranksep 160

skinparam nodesep 140



class 动作

class 当责

class 当责类型

class 当事者

class 当事者类型

class 时间段



当责类型 "0..*" -- "-委托方s\n1..*" 当事者类型

当责类型 "0..*" -- "-责任方s\n1..*" 当事者类型

当责 "0..*" -- "-委托方1" 当事者

当责 "0..*" -- "-责任方1" 当事者

当责类型 "-类型1" -- "0..*" 当责

当事者类型 "-类型1" -- "0..*" 当事者

当责 "0..*" -- "1" 时间段

当责 "0..*" -- "0..*" 动作



note right of 当责

  <b>约束:</b>

  类型.委托方s->includes(委托方.类型)

  and

  类型.责任方s->includes(责任方.类型)

end note

当责类型 -[hidden]right- 当责

当事者类型 -[hidden]right- 当事者

@enduml

<img width="1080" height="432" alt="image" src="https://github.com/user-attachments/assets/59a8137f-d6a7-4749-8fc1-ec811c651565" />

原图2.10

<img width="1080" height="609" alt="image" src="https://github.com/user-attachments/assets/a2487503-84f3-49dd-8f6a-7bafde77843d" />

EA绘制

<img width="1080" height="736" alt="image" src="https://github.com/user-attachments/assets/0eece0f7-e696-41be-88d4-30d5d69ce40d" />

图2.10 允许当事者类型具有子类型和超类型。

给当事者类型添加泛化使定义知识级变得更容易

PlantUML

@startuml

skinparam ranksep 120

skinparam nodesep 180



class 当责

class 当责类型

class 当事者

class 当事者类型



当责类型 "0..*" -- "-委托方s\n1..*" 当事者类型

当责类型 "0..*" -- "-责任方s\n1..*" 当事者类型

当责 "0..*" -- "-委托方1" 当事者

当责 "0..*" -- "-责任方1" 当事者

当责类型 "-类型1" -- "0..*" 当责

当事者类型 "-类型1" -- "0..*" 当事者

当事者类型 "-子类型s\n0..*" -- "-超类型\n0..1" 当事者类型



note top of 当责

  <b>约束:</b>

  (委托方.类型->closure(超类型))->intersection(类型.委托方s)->notEmpty()

  and

  (责任方.类型->closure(超类型))->intersection(类型.责任方s)->notEmpty()

end note



当责类型 -[hidden]left- 当责

当事者类型 -[hidden]left- 当事者

@enduml

<img width="1080" height="632" alt="image" src="https://github.com/user-attachments/assets/428214db-e6cd-42d0-8e14-6a878a63010c" />

原图2.11

<img width="1080" height="540" alt="image" src="https://github.com/user-attachments/assets/ae257f2b-fdef-48ee-8eed-1780e82ca78e" />

EA绘制

<img width="740" height="424" alt="image" src="https://github.com/user-attachments/assets/a0d98573-e008-47b9-bc2e-fbaa27d24e44" />

图2.11 层级当责类型。

所添加的约束意味着通过此类型的当责来链接的当事者必须形成一个层级结构。

PlantUML

@startuml

class 当责类型

class 层级当责类型



当责类型 <|-- 层级当责类型



note right of 层级当责类型

  约束:

  对于此类型的“当责”，

  “当事者”只对其中一个负责。

end note

@enduml

<img width="670" height="343" alt="image" src="https://github.com/user-attachments/assets/ab960baf-7e48-4089-897f-7a1b19e983df" />

原图2.12

<img width="1080" height="738" alt="image" src="https://github.com/user-attachments/assets/04c32253-1bfc-478c-990a-1d27eb873645" />

EA绘制

<img width="1080" height="627" alt="image" src="https://github.com/user-attachments/assets/1e8a48a7-272d-45ad-b913-038619d0fd60" />

图2.12 分级当责类型。

分级当责支持固定级别，如销售办事处、分部、地区。

PlantUML

@startuml

skinparam ranksep 80

skinparam nodesep 180



class 当责类型

class 分级当责类型

class 层级当责类型

class 当事者类型



当责类型 <|-- 分级当责类型

当责类型 <|-- 层级当责类型

当事者类型 "-级别s* {sequence}" -right- " * " 分级当责类型



note bottom of 分级当责类型

约束：

“当事者”只对唯一的“当事者类型”

为级别列表中的下一个级别的“当事者”负责。

end note

note bottom of 层级当责类型

约束：

对于此类型的“当责”，“当

事者”只对其中一个负责。

end note

@enduml

<img width="1080" height="438" alt="image" src="https://github.com/user-attachments/assets/076ba6d2-02cb-4564-b946-61987df8b550" />

原图2.13

<img width="1080" height="466" alt="image" src="https://github.com/user-attachments/assets/26201df8-2259-47ab-a42a-7412f4a2b94f" />

EA绘制

<img width="782" height="653" alt="image" src="https://github.com/user-attachments/assets/3a345853-7c75-4652-a697-7d06e6cb2ece" />

图2.13 重新平衡当责类型的子类型。

一个更好地组织当责类型层级结构的方式。

PlantUML

@startuml

skinparam ranksep 80

skinparam nodesep 120



class 当责类型

class 层级当责类型

class 分级当责类型

class 定向当责类型

class 当事者类型



分级当责类型 -up-|> 当责类型

定向当责类型 -up-|> 当责类型

层级当责类型 -left-|> 当责类型

分级当责类型 "*" -- "-级别s*\n{sequence}" 当事者类型

定向当责类型 " *" -right- "-委托方s*" 当事者类型 

定向当责类型 " *" -- "-负责方s*" 当事者类型

@enduml

<img width="874" height="588" alt="image" src="https://github.com/user-attachments/assets/ebbd3f1d-5620-447f-a705-b49aefe90617" />

原图2.14

<img width="1065" height="1019" alt="image" src="https://github.com/user-attachments/assets/5d404975-0481-41b6-a8a9-5dc5ca48b3f0" />

EA绘制

<img width="1055" height="739" alt="image" src="https://github.com/user-attachments/assets/1f432ed4-f68a-4714-856b-12dc4519511e" />

图2.14 操作范围

操作范围定义当责在创建时所承担的责任。它们可以用于职务描述。

PlantUML

@startuml

class 当责

abstract class 操作范围

class 地点

class 临床护理范围

class 协议范围

class 资源供给

class 销售区域

class 观察概念

class 数值

class 协议

class 数量

class 资源类型

class 产品类型



操作范围 <|-- 临床护理范围

操作范围 <|-- 协议范围

操作范围 <|-- 资源供给

操作范围 <|-- 销售区域



当责 "1" -- "0..*" 操作范围

地点 "0..1" -- "*" 操作范围

临床护理范围 "0..*" -- "1" 观察概念

协议范围 "0..*" -- "-数额1" 数值

协议范围 "0..*" -- "1" 协议

资源供给 "0..*" -- "1" 数量

资源供给 "0..*" -- "1" 资源类型

销售区域 "0..*" -- "1" 产品类型

@enduml

<img width="1080" height="668" alt="image" src="https://github.com/user-attachments/assets/06e5de79-4c41-4bca-8fd3-99569da5d37d" />
