> 参考：
> 
> Those three papers
> 
> Building Software Systems at Google and Lessons Learned.ppt

    

## 背景

    一定要把握 BigTable 技术产生的背景与业务需求。

    Google 放出来三篇 BigData Paper：GFS + MR + BigTable，但在其内部只有 Google Search（GSearch） 这一个系统。

    GSearch 的核心业务逻辑就是，为大量互联网网页生成关键词索引。难点存在于以下几个方面：

- 如何运行在普通硬件上；

- 如何提升系统性能：可扩展、高可用；

- 如何增量地产生索引；

    针对以上三个问题就分别形成了 GFS、BigTable、MR 三个方案。它们也可以视为 GSearch 自下而上的三个基础设施层，分别是两个存储层和一个计算层。基础设施层之上就是业务层，具体到 GSearch 业务层就是 Reversed Index、Page Rank 这些算法。

    

## 主要工作

三个基础设施层之间是存在密切联系的：

- GFS 提供普通硬件上的可靠存储，在文件系统这一层保证可靠性与可扩展性；

- BigTable 在可靠的分布式文件系统上，更加关注数据的一致性与分区能力；

- MR 是运行在存储层上的、基于分区的计算层；

    除了这些主要的基础设施，Google 还创造了一些周边设施：

- Build System：Bazel 等；

- Encoding Protocol：Proto Buffer 等；

- Testing Framework：GTest、GLog 等；

    

**关于 BigTable 与数据库系统**

    首先 BigTable 是不是数据库系统？结论如下：BigTable 是无模式的数据库系统，是 NoSQL 数据库先驱。“无模式”是指不像关系型数据库那样预定义 Data Schema，这样的**数据模型**同样体现在之后的诸多 NoSQL 上，例如 Redis、HBase、Dynamo。

> No-schema 与 DBMS **存在交集**，也存在不相交元素。
> 
> Redis 数据库需要用户自定义 Schema，比如自定义 Key 的序列化规则。XML 也需要用户自定义 Schema，但却被称为“文件”。
> 
> 两者的不同之处在于，Redis 会提供简单的 ACID 特性，但 XML 不支持一丁点的 ACID 特性。

    BigTable 的数据模型为：稀疏的、多维度的、有序的映射（Map），即： (row:string, column:string,time:int64)->string。
