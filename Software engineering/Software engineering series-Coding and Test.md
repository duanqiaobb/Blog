
**目录**


- [概述](#概述)
- [软件测试准则](#软件测试准则)
- [软件测试方法](#软件测试方法)
    - [单元测试](#单元测试)
    - [集成测试](#集成测试)


<a name="概述"></a>
# <font color="#338DD" size="3" style="font-style:bold">概述</font>

     软件工程中的编码和测试实际上就是软件设计中的实现的阶段。

> 编码
   

     软件工程的编码阶段，就是针对软件设计，选择合适的程序语言进行实现。

> 测试
    
     软件测试阶段就是为了发现程序中的错误而执行程序的过程。


<a name="软件测试准则"></a>
# <font color="#338DD" size="3" style="font-style:bold">软件测试准则</font>

     1. 所有的测试应该追溯到用户需求
     2. 应该在测试开始之前就制定测试计划
     3. 应该从“小规模”测试开始，并逐步进行“大规模“ 测试。



# <font color="#338DD" size="3" style="font-style:bold">软件测试方法</font>
    
     按照测试的方式来分：
        1. 白盒测试
        2. 黑盒测试

     按照测试的步骤来分:
        1. 单元测试
        2. 集成测试
        3. 验收测试

     一般软件的测试过程分为: 模块测试->子系统测试->系统测试->验收测试->平行运行

<a name="单元测试"></a>
 > 单元测试

   单元测试(Unit Testing), 又称为模块测试，主要是针对程序模块（软件设计的最小单位）进行正确性检验的测试工作。在过程化编程中，一个单元就是单
   个程序、函数、过程等；对于面向对象编程，最小单元就是方法，包括基类（超类）、抽象类、或者派生类（子类）中的方法。

   **单元测试的重点 :**

       1. 模块接口：对模块接口的数据流进行测试，确保模块接口数据能够正确的进出。
       2. 局部数据结构：检查局部数据说明、初始化、默认值等方面的错误。
       3. 重要的执行通道：用来以发现由于错误的计算、不正确的比较或者不适当的控制流而造成的错误。
       4. 出错处理通道：确保程序对可能出现的错误的正确处理。
       5. 边界条件: 保证程序在常常出错的边界有效。


  **单元测试的方法：**

      单元测试常常使用的是白盒测试，但是有时也会使用黑盒测试。单元测试运用的管理方法有：
       
      单独单元测试： 由程序员自己编码的同时进行单元测试。比较常用。
      
      代码审查：由程序组长，程序的设计者，程序的编写者，程序的测试者一起组成的审查小组总统进行单元测试。

      计算机测试:  为单元测试开发驱动软件和存根软件，让计算机运行测试驱动进行单元测试。其中存根软件是当软件模块过多，用来做"虚拟子
      程序",替换被测试模块所调用的模块。驱动软件是测式模块的入口。


<a name="集成测试"></a>
  > 集成测试