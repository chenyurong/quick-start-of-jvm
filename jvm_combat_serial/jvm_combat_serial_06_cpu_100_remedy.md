# JVM实战系列第6讲：CPU100%的分析方法

CPU100%的异常，一般我们都需要通过linux的top命令来查看具体是哪个进程发生了问题，之后确定到具体的JVM进程。之后通过jstack命令dump出具体的线程信息，通过分析线程信息确定具体的代码位置，最终确定问题。 

## 实战案例

* [【JAVA 工具】jstack简单使用，定位死循环、线程阻塞、死锁等问题 - 可口可乐的博客 - CSDN博客](http://blog.csdn.net/wanglha/article/details/51133819)
* [不止JDK7的HashMap，JDK8的ConcurrentHashMap也会造成CPU 100%](http://mp.weixin.qq.com/s?__biz=MzU0MzQ5MDA0Mw==&mid=2247484571&idx=1&sn=6d5d71a34e15a1857782d3ea440e32a3&chksm=fb0bee0fcc7c67191e2e07d11f3ff23f3f6ca8a3a15523be8d868fec5d7e61f0b61f97b71609&mpshare=1&scene=1&srcid=1206h1M8iMQWEn726VEo0ape#rd)