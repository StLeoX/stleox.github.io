> **CMU-15-445/645 Database Systems Series:**
> 
> Textbook: *Database System Concepts*
> 
> Project: BusTub

## 理论

### 核心概念

#### 系统分层

#### 缓冲池

    缓冲池用来优化页的换入换出

#### 数据倾斜

    并行处理器（Parallel Processor/Executor）能处理大量数据，但是惧怕“数据倾斜”的情况。

### 关键思想

    在数据库领域内存在很多关键的思想/原则/设计模式，这些思想指导着系统设计、算法设计。

#### 哈希

    建立哈希桶是非常常用的技巧，因为哈希桶的查找操作有非常好的时间复杂度。需要注意的是，哈希桶中的内容是可以泛化的，可以是页、是索引、是。

#### 归并

## 实践

### BusTub整体架构

    遵从DBMS的典型架构，

### 逻辑计划

    针对子句生成逻辑计划的一般顺序为：

    From → Join → Where → GroupBy → Having → Select → Select Function → Distinct → OrderBy → Limit

### 物理计划
