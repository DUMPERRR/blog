第五元素 2024-4-23 19:46
潘老师，请教一个问题 结合片段是否需要事先有一个判断？比如

<img width="884" height="574" alt="image" src="https://github.com/user-attachments/assets/6bab8328-b67c-42f6-8867-7dbb057d7be7" />

UMLChina潘加宇
不需要，这样的判断是包含在循环内部的，不需要另外画出来。
这个和编码一样的
编码我们只会写
while(未搞定)
{
搞();
}
这个循环在运行中可能会多次判断“未搞定”这个布尔表达式，但代码中并不需要在某个地方再加一个if（未搞定）
第五元素 2024-4-28 20:56
潘老师，你说的情况是do...while循环，是“先执行，后判断”。“先判断，后执行”（while循环）的情况如何表达呢？
UMLChina潘加宇
缺省的应该是while，如果是do...while，给loop加下限，看规范或《UML参考手册》

<img width="1080" height="1379" alt="image" src="https://github.com/user-attachments/assets/fa6f1a56-f691-4b05-a758-61d3871507f6" />
