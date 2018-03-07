# 设计数据密集型应用 - 中文翻译 

- 作者： [Martin Kleppmann](https://martin.kleppmann.com)
- 原书名称：[《Designing Data-Intensive Application》](http://shop.oreilly.com/product/0636920032175.do)
- 译者：[冯若航]( http://vonng.com/about) （fengruohang@outlook.com ）
- 建议本地使用[Typora](https://www.typora.io)以获取最佳阅读体验。

-------------

## 法律声明

译者纯粹出于学习目的与个人兴趣翻译，本译文只供学习研究参考之用，不得公开传播发行或用于商业用途。有能力阅读英文书籍者请购买正版支持。

译者保留对译文的署名权，其他权利以原作者和出版社的主张为准，侵删。



## 译序

> 不懂数据库的全栈工程师不是好架构师
>
> —— Vonng

现今，尤其是在互联网领域，大多数应用都属于数据密集型应用。本书从底层数据结构到顶层架构设计，将数据系统设计中的精髓娓娓道来。其中的宝贵经验无论是对架构师，DBA、还是后端工程师、甚至产品经理都会有帮助。

这是一本理论结合实践的书，书中很多问题，译者在实际场景中都曾遇到过，读来让人击节扼腕。如果能早点读到这本书，该少走多少弯路啊！

这也是一本深入浅出的书，讲述概念的来龙去脉而不是卖弄定义，介绍事物发展演化历程而不是事实堆砌，将复杂的概念讲述的浅显易懂，但又直击本质不失深度。每章最后的引用质量非常好，是深入学习各个主题的绝佳索引。

本书为数据系统的设计、实现、与评价提供了很好的概念框架。读完并理解本书内容后，读者可以轻松看破大多数的技术忽悠，与技术砖家撕起来虎虎生风🤣。

这是2017年译者读过最好的一本技术类书籍，这么好的书没有中文翻译，实在是遗憾。某不才，愿为先进技术文化的传播贡献一分力量。既可以深入学习有趣的技术主题，又可以锻炼中英文语言文字功底，何乐而不为？

不过翻译，尤其是精翻，确实是一件极其耗费心血的工作。没有什么经济收益，只有纯粹的兴趣，欢迎有兴趣的朋友一起[加入](https://github.com/Vonng/db)。



## 前言

> 在我们的社会中，技术是一种强大的力量。数据、软件、通信可以用于坏的方面：不公平的阶级固化，损害公民权利，保护既得利益集团。但也可以用于好的方面：让底层人民发出自己的声音，让每个人都拥有机会，避免灾难。本书献给所有将技术用于善途的人们。

---------

> ​计算是一种流行文化，流行文化鄙视历史。 流行文化关乎个体身份和参与感，但与合作无关。流行文化活在当下，也与过去和未来无关。 我认为大部分（为了钱）编写代码的人就是这样的， 他们不知道自己的文化来自哪里。                         
>
>  ——阿兰·凯接受Dobb博士的杂志采访时（2012年）



## [目录](ddia/README.md)

####  [I. 数据系统基础](ddia/part-i.md)

1. [可靠性、可扩展性、可维护性](ddia/ch1.md)  
2. [数据模型与查询语言](ddia/ch2.md) 
3. [存储与检索](ddia/ch3.md) 
4. [编码与演化](ddia/ch4.md) 

####  [II. 分布式数据](ddia/part-ii.md)

5. [复制](ddia/ch5.md) 
6. [分片](ddia/ch6.md) 
7. [事务](ddia/ch7.md)
8. [分布式系统的麻烦](ddia/ch8.md)
9. [一致性与共识](ddia/ch9.md) 

#### [III. 派生数据](ddia/part-iii.md)

10. [批处理](ddia/ch10.md) 
11. [流处理](ddia/ch11.md) 
12. [数据系统的未来](ddia/ch12.md)


#### [术语表](ddia/glossary.md)

#### [后记](ddia/colophon.md)



## 翻译计划

* 机翻：只在乎结构：梳理文章结构、图片、引用、备注。
* 初翻：保证经完全理解本章内容，人工修复显著的错误，重新组织语言。
* 精翻：阅读相关领域文献书籍，确定术语的最终译法，修复格式瑕疵，着力信达雅。

通常机翻一章1个小时左右，初翻一章6小时，精翻一章三到五天。

精翻可以看，机翻基本没法看，初翻对于业内人士能凑合看。

|                章节                |     进度     | Credit                                                    |
| :--------------------------------: | :----------: | --------------------------------------------------------- |
|                序言                |     机翻     | 序言初翻 by [seagullbird](https://github.com/seagullbird) |
|   第一部分：数据系统基础 ——概览    |     初翻     |                                                           |
| 第一章：可靠性、可扩展性、可维护性 |   **精翻**   |                                                           |
|     第二章：数据模型与查询语言     |     初翻     |                                                           |
|         第三章：存储与检索         |     初翻     |                                                           |
|         第四章：编码与演化         |     初翻     |                                                           |
|     第二部分：分布式数据——概览     |     初翻     |                                                           |
|            第五章：复制            |     初翻     |                                                           |
|            第六章：分片            |     初翻     |                                                           |
|            第七章：事务            | **精翻 80%** |                                                           |
|      第八章：分布式系统的麻烦      |   **初翻**   |                                                           |
|        第九章：一致性与共识        |     机翻     | 进行中                                                    |
|           第三部分：前言           |     机翻     |                                                           |
|           第十章：批处理           |     机翻     |                                                           |
|          第十一章：流处理          |     机翻     |                                                           |
|      第十二章：数据系统的未来      |     机翻     |                                                           |
|               术语表               |      -       |                                                           |
|                后记                |     机翻     |                                                           |

最近比较忙，精翻计划可能会延后，但初翻会尽量先过一遍。早期的几章初翻质量很一般，后续会重新过一遍。



## CONTRIBUTION

欢迎贡献，初翻后的章节，接受ISSUE指正。

贡献者需要同意[法律声明](#法律声明)所叙内容，翻译请提前联系以免冲突。

有人建议拉个群，也许发布更新通知？

![](ddia-wexin.JPG)



## LICENSE

CC-BY 4.0