# JVM规范导读系列 - 第3章：为Java虚拟机编译

> Oracle 的 JDK 包括两部分内容：一部分是将 Java 源代码编译成 Java 虚拟机的指令集的编译器，另一部分是用于Java 虚拟机的运行时环境。

第一部分应该说的是 Javac 这个前置编译器，用于将Java源代码编译成字节码。第二部分是说 JIT 即时编译器，用于在JVM运行时进行进一步优化，将字节码编译成本地机器码。

> 即时代码生成器（Just-In-Time/JIT Code Generator）就是一种在
Class 文件中的代码被 Java 虚拟机代码加载后，生成与平台相关的特定指令的编译器。

上面这句验证了我的理解，JIT编译器把字节码转成与平台相关的特定指令。

> Java 虚拟机代码将使用 Oracle 的 javap 工具所生成的非正式的“虚拟机汇编语言（Virtual Machine Assembly Language）”格式来描述。

原来javap生成的那份东西叫做：虚拟机汇编语言！涨知识了！

下面是一个Java代码的字节码指令，通过这个例子了解下字节码指令，非常不错。

```
void spin() {
	int i;
	for (i = 0; i < 100; i++) {
		; // Loop body is empty
	}
}
```

对应的字节码指令：

```
Method void spin()
0 iconst_0 // Push int constant 0
1 istore_1 // Store into local variable 1 (i=0)
2 goto 8 // First time through don’t increment
5 iinc 1 1 // Increment local variable 1 by 1 (i++)
8 iload_1 // Push local variable 1 (i)
9 bipush 100 // Push int constant 100
11 if_icmplt 5 // Compare and loop if less than (i < 100)
14 return // Return void when done
```

下面的各种都是对于字节码指令的解读，有点枯燥，耐心看下去就好了。




