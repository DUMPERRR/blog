接下来是图16.5： 

<img width="1080" height="653" alt="image" src="https://github.com/user-attachments/assets/7c928312-e79d-4798-b8a2-ce3260321308" />

这是一个蒸馏器系统上下文图，相当于结构化分析中的0层数据流图，聚焦于目标系统，观察目标系统跟它周围的其他系统之间有什么数据流动。

例如，从上图可知，蒸馏器的输入是污水和热，输出是净水。

当然，这个图并不严谨。用水人员和蒸馏器没有交互，不应该在此图中出现。

我们也不能直接先画这个图，因为这里面的Block（水源、水分配系统）、Actor（操作人员）、Item Flow（脏水：水）目前还没有，需要先画其他图添加这些元素，然后才能画图16.5。

我们先画图16.6的蒸馏器用例图： 

<img width="955" height="759" alt="image" src="https://github.com/user-attachments/assets/89e25261-d732-4c46-a63b-04b3f9e316bf" />

这个用例图也存在问题。例如，用例叫“操作蒸馏器”，这个相当于废话。

用例的意思是，你用我来干啥。这样一写，意思是：

我用你的目的就是用你，我和蒸馏器打交道的目的就是操作蒸馏器。

听君一席话，如听一席话？更好的是：

我和蒸馏器打交道的目的是为了“蒸馏净水”或“生产净水”。

另外，“照料热源”、“照料水源”不是通过蒸馏器做到的，不应该出现在这张用例图中。虽然作者很聪明地用了一个边界框，只框住了“操作蒸馏器”，但依然是不合适的。

为什么作者要这样画，原因也是现在很多MBSE方法学普遍存在的问题，缺少业务建模工作流的推导过程，一上来就是这个系统怎么样怎么样，作者想表达“照料热源”、“照料水源”都没有地方放，只好硬凑到系统用例图中。

步骤6.1 创建蒸馏器用例图

在Browser右击“蒸馏器用例”，从快捷菜单选择“Add Diagram”。在New Diagram对话框的Select From列表框选择SysML 1.5，然后在右侧的Diagram Type列表框选择UseCase，点击OK。 

<img width="831" height="641" alt="image" src="https://github.com/user-attachments/assets/6e7e10c4-d5cc-4009-b314-53c9c2e50372" />

<img width="756" height="544" alt="image" src="https://github.com/user-attachments/assets/749f017a-007f-4f2f-bec9-25486344f33e" />

<img width="590" height="228" alt="image" src="https://github.com/user-attachments/assets/2b6db31f-bafb-44d4-8d19-b42e5b316892" />
