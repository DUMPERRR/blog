原图2.1

<img width="1080" height="689" alt="image" src="https://github.com/user-attachments/assets/f57b53a3-5189-4d14-b8da-d4aec87802d7" />

EA绘制

<img width="852" height="450" alt="image" src="https://github.com/user-attachments/assets/3878fd1e-e85e-40c1-885d-687fbc763e62" />

图2.1 通讯录的初始模型。

这个模型展示了人和组织的相似责任。

PlantUML

@startuml

left to right direction

skinparam ranksep 80

skinparam nodesep 80

class 人

class 公司

class 电话号码

class 地址

class 电子邮件地址

人          "0..1" -- "0..*" 电话号码

电话号码    "0..*" -- "0..1" 公司

人          "0..1" -- "0..*" 地址

地址        "0..*" -- "0..1" 公司

人          "0..1" -- "0..*" 电子邮件地址

电子邮件地址 "0..*" -- "0..1" 公司

@enduml

<img width="618" height="474" alt="image" src="https://github.com/user-attachments/assets/5399acf7-88ce-40dc-ba30-fa407c8020bb" />

原图2.2

<img width="1080" height="707" alt="image" src="https://github.com/user-attachments/assets/13152c59-adb5-4110-9e43-838c31b736c9" />

EA绘制

<img width="798" height="472" alt="image" src="https://github.com/user-attachments/assets/2bc28f6e-e534-4c03-9148-9287f27e63fa" />

图2.2 使用当事者来泛化之后的图2.1 。

很多用到人或组织的情形，应该使用当事者。

PlantUML

@startuml

class 当事者

class 人

class 组织

class 电话号码

class 地址

class 电子邮件地址



当事者 <|-- 人

当事者 <|-- 组织

当事者 "1" -- "0..*" 电话号码

当事者 "1" -- "0..*" 地址

当事者 "1" -- "0..*" 电子邮件地址

@enduml

<img width="811" height="280" alt="image" src="https://github.com/user-attachments/assets/870bf995-9b61-4184-8179-1e9c0c57a9d7" />

原图2.3

<img width="1080" height="240" alt="image" src="https://github.com/user-attachments/assets/5db19457-12c7-4c1f-be70-1f28ba41a27e" />

EA绘制

<img width="1080" height="132" alt="image" src="https://github.com/user-attachments/assets/41df6995-0202-4857-9b18-03b972379fb1" />

图2.3 用显式级别表示的组织结构。

这样一个结构不灵活又难以复用。

PlantUML

@startuml

left to right direction

class 经营单位

class 地区

class 分部

class 销售办事处



经营单位 "1" -- "0..*" 地区

地区     "1" -- "0..*" 分部

分部     "1" -- "0..*" 销售办事处

@enduml

<img width="950" height="119" alt="image" src="https://github.com/user-attachments/assets/5b2c2d13-238a-4698-8583-050f69e35fe9" />

原图2.4

<img width="1080" height="709" alt="image" src="https://github.com/user-attachments/assets/d248f88b-e307-4923-9247-37d9305e9412" />

EA绘制

<img width="1080" height="563" alt="image" src="https://github.com/user-attachments/assets/da8a7418-6c8d-40e6-be21-15058f4ea5ae" />

图2.4 带层级关系的组织超类型。

层级关联提供了最大的灵活性。级别导致的约束必须作为规则添加在子类型上。

PlantUML

@startuml

skinparam ranksep 20

skinparam nodesep 80

left to right direction



class 组织

class 经营单位

class 地区

class 分部

class 销售办事处



经营单位 --|> 组织

地区 --|> 组织

分部 --|> 组织

销售办事处 --|> 组织

组织 "-母 0..1" -- "-子女s 0..*" 组织

note left of 经营单位

  约束:

  母->isEmpty()

end note

note left of 地区

  约束:

  母.oclIsTypeOf(经营单位)

end note

note left of 分部

  约束:

  母.oclIsTypeOf(地区)

end note

note left of 销售办事处

  约束:

  母.oclIsTypeOf(分部)

end note

note bottom of 组织

  约束:

  not 母.closure(母)->includes(self)

end note

@enduml

<img width="702" height="565" alt="image" src="https://github.com/user-attachments/assets/c9dcd7bc-42b2-4062-a45a-5f37b0e9d8fc" />

原图2.5

<img width="1080" height="483" alt="image" src="https://github.com/user-attachments/assets/f1c83ce8-6f52-49ee-b4d0-06fd33a038b0" />

EA绘制

<img width="1078" height="421" alt="image" src="https://github.com/user-attachments/assets/6ca795cd-f313-4de5-914d-02309b3c6791" />

图2.5 两个组织层级结构。

组织的子类型未展示。如果有很多层级结构，这个模型将很快失控。

PlantUML

@startuml

skinparam linetype ortho

class 组织



组织 "-销售母 0..1" -up-  "销售子s 0..*" 组织

组织 "-产品母 0..1" -left- "-产品子s 0..*" 组织



note right of 组织

  约束：

  (not 销售母.closure(销售母)->includes(self)) and

  (not 产品母.closure(产品母)->includes(self))

end note

@enduml

<img width="997" height="237" alt="image" src="https://github.com/user-attachments/assets/fb6c50d6-3473-4878-9a8a-91b6827939e5" />

原图2.6

<img width="1080" height="711" alt="image" src="https://github.com/user-attachments/assets/239b2468-23a6-47b8-84d1-a5a9fa31909d" />

EA绘制

<img width="921" height="675" alt="image" src="https://github.com/user-attachments/assets/fd9528c4-2f55-4e40-9b02-627fd4600213" />

图2.6 使用类型化关系。

组织之间的每一个关系都由一个组织结构类型定义。如果有很多个关系，这样做比显式关联更好。

PlantUML

@startuml

left to right direction

skinparam ranksep 40

skinparam nodesep 80



class 组织结构类型

class 组织结构

class 时间段

class 组织

class 经营单位

class 地区

class 分部

class 销售办事处



组织结构类型 "1" -- "0..*" 组织结构

时间段 "1" -- "0..*"组织结构

组织结构 "0..*" -- "-母1" 组织

组织结构 "0..*" -- "-子1" 组织

组织 <|-- 经营单位

组织 <|-- 地区

组织 <|-- 分部

组织 <|-- 销售办事处

@enduml

<img width="789" height="710" alt="image" src="https://github.com/user-attachments/assets/7acd45db-c60a-4c4f-a049-803044bd7744" />

原图2.7

<img width="1080" height="693" alt="image" src="https://github.com/user-attachments/assets/22464688-07d4-421e-a815-08df2c39c31d" />

EA绘制

<img width="913" height="678" alt="image" src="https://github.com/user-attachments/assets/9413e264-61bf-469b-b7d7-295b0aebec6b" />

图2.7 给图2.6添加规则。

该规则强制执行约束，例如销售办事处向分部汇报。

PlantUML

@startuml

skinparam ranksep 100

skinparam nodesep 140

class 组织结构类型

class 组织结构

class 时间段

class 规则

class 组织 

class 经营单位

class 地区

class 分部

class 销售办事处



组织结构类型 "1" -- "0..*" 组织结构

组织结构 "0..*" -- "1" 时间段

组织结构类型 "0..*" -- "1" 规则

组织结构 "0..*" -- "-母1" 组织

组织结构 "0..*" -- "-子1" 组织



经营单位 -left-|> 组织

地区 --|> 组织

分部 --|> 组织

销售办事处 -up-|> 组织

@enduml

<img width="1080" height="789" alt="image" src="https://github.com/user-attachments/assets/526bfd0f-6724-428b-8cf5-ec20de877815" />
