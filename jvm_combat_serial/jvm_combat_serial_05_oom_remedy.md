# JVM实战系列第5讲：内存溢出的分析方法

一般来说内存溢出，我们首先肯定是查看日志以及dump文件。通过分析dump文件来分析到底是哪一部分内存发生了泄露，通过分析可以确定哪一部分代码逻辑出现了问题。在定位问题的时候，更多时候还是要依靠实际经验。

## 实战案例

* [从JVM模型谈十种内存溢出的解决方法](https://news.html5.qq.com/share/4088289516556353660?ch=060000&qbredirect=&sc_id=ThhrDDC&sh_sid=5__14aaa1c103835950__05fd90cd86c2e501d5ce57a513b788cb&share=true&share_count=1&url=http%3A%2F%2Fkuaibao.qq.com%2Fs%2F20181202A12H2300)
* [一次JVM GC长暂停的排查过程](https://www.jianshu.com/p/8a4366a7f32d)
* [一次 Redis 内存诡异增长的排查过程](http://mp.weixin.qq.com/s?__biz=MzIwMzY1OTU1NQ==&mid=2247484311&idx=1&sn=33a1fae7d3a431f062449e30cbedf9be&chksm=96cd43dba1bacacd8a24ded8f54dcfac499176a44563a3d7bdaa743e96b304a7f9c2642347c1&mpshare=1&scene=1&srcid=0719NKXnYBIz7DXad4x40z9E#rd)