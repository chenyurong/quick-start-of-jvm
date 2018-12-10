# JVM规范导读系列 - 总结

我们花了几天的时间来阅读《Java虚拟机规范》，了解要实现一个虚拟机应该包括什么内容。通过这么一次阅读，我们大致了解了虚拟机规范的内容。

* 第1章。对Java虚拟机进行了一些简单的介绍。
* 第2章。介绍了虚拟机的结构，以及一些异常体系以及字节码指令集。可以说是规范的重点内容。
* 第3章。介绍了编译器是如何将Java源代码编译成JVM所需要的字节码的，如何去阅读这些字节码指令。
* 第4章。这一章针对字节码文件的格式做了详细的讲解，让我们了解字节码里的每一个字节的作用。
* 第5章。这一章对JVM是如何启动、加载以及初始化字节码做了详细的描述。
* 第6章。这一章节介绍了虚拟机指令集的相关知识，对虚拟机指令集的每个指令做了详细的介绍，可以当成工具书来查询使用。

通过这么一个介绍，我们可以知道第2、3、4、5章节是重点。这些章节中的Java虚拟机结构、字节码文件格式、JVM加载过程是重点，读完之后至少要弄懂这些过程。

读完这份规范，也有许多不懂的地方，例如：

* 第3章中，将Java代码编译成字节码指令集，几乎每一章节都有对应的Java代码和字节码的对照。这需要我们耐心地一个个指令去查询和理解，这部分我在阅读的时候也是简单略过。这是后期的学习重点。
* 本文其他部分也有不少关乎数学的严谨描述，这部分我也只是粗略扫过。这也是后期进一步学习需要加强的。

简单地说，通过阅读《Java虚拟机规范》，我从官方渠道验证了之前的一些猜想。例如：

* JVM 就是一个虚拟机的机器，与正常的PC一样，其有内存也有指令集。
* 准备阶段，虚拟机不执行任何字节码指令，而知识为类或接口的静态字段分配空间，并用默认值初始化这些字段。
* boolean类型在JVM中的实现，是通过int类型来实现的。在JVM中，是没有boolean类型这一数据类型的。
* 等等

很多时候我们会被网络上许多知识点的解释迷惑，不知道哪个说的是正确的。这个时候就需要我们去找到官方的消息渠道。而对于虚拟机来说，《Java虚拟机规范》就是这样一个官方的消息，在规范中所说的就是绝对正确的消息来源。所以说阅读《Java虚拟机规范》才显得尤为重要。

通过这一次阅读，我验证了不少之前留存下来的疑惑，也新增了不少新的疑惑。但我相信这一次阅读将会给我带来很大的积极影响，下次当我遇到虚拟机模棱两可的问题时，我会优先查找规范中的解释，之后再去参考其他的。这可以说是一种更为有效的学习方式。

如果你还没有阅读过，那么你可以跟着这个系列，与我一起阅读。也与我一样，在阅读中写下自己的想法。随着更多人能读完这本规范，我相信也有更多不同的想法蹦出，通过彼此交流，我们定能够理解得更加深刻。