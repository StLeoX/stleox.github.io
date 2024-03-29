## 群体与个体

    软件工程的群体远远优先于个体。

    据说在 Google 的单仓里面，代码只有 "experimental" 和 "deprecated" 这两种状态。**所以不要从个人的角度去审视代码的稳定性**。在实际生产过程中，个人开发的代码很难进入主分支，就算进入主分支也可能在后续的迭代过程中很快被修改掉。如果你是抱着这样的心态去开发软件，那么你可能会收获很多失望：我写下的每一行代码，都是最完美、最稳定的版本。

    

## 人与技术

    软件工程的关键在于人（主要是程序员），核心在于软件制品。

    正是这种“关键”与“核心”不匹配的性质，导致软件开发过程中会侵害具体某个人的权益。

    软件工程中最大的**不确定性因素恰恰也在于人**，在于程序员之间异步的协作关系。所以我们才需要文档、各种协作工具来管理、约束人，不然团队就会像一组随机的向量，综合的结果是缺少战斗力。

    

## 程序的正确性

    **程序“正确性”的哲学。**
“正确性”不单单是属于软件的，比如一把尺子也有正确性。
那么如何判断一把尺子准不准，思路其实有两种：**相对比较和绝对比较**。

    相对比较就是用两把尺子测量同一个物体，尺子正确的必要条件是两个结果一致。当然也可能两个结果相同但两个结果都是错误的。所以将两把尺子推广到无数把尺子，通过数量来逼近精度。

    绝对比较就是造一把绝对正确的尺子（一把理想的尺子！）。一个尺子正确的充分必要条件是它与理想尺子的测量结果一致。显然，相对比较比绝对比较更加容易进行。

    BTW，**纠正人的认知偏差也是这个原理**。比较自己的观点与主流的观点，以此来纠正认知偏差。并非说主流的观点都是正确的，但也不可能预测谁的认知是绝对正确的。

    

## 软件开发模型

    从瀑布开发到敏捷开发是符合历史规律的。

    敏捷开发的一个核心的改进点是，增加了**开发过程的并行程度**。敏捷开发采用“**迭代**”作为开发进度单元，而迭代之间存在依赖关系、可以并行进行。而瀑布开发中，“设计-编码-测试”的串行方式，仍然是传统制造业的生产流程，这不符合“软件是对特性的综合”的特点。

    

## 软件需求工程

    需求工程划分为两个部分：需求开发和需求管理。

    需求开发的递进工作包含：需求获取（Elicitation）、需求分析（Analysis）、编写规约（Specification）和需求验证 （Validation）。

    需求管理的并列工作包含：基线管理、变更管理、需求跟踪。

    

**用户故事是需求的占位符**

    具体而言，故事和需求之间的关系是故事包含了用户的需求，而需求是故事的具体实现和要求。

    理解“占位符”。随着迭代，我们再次修改用户故事，并加需求。

    

**需求优先级**

    需求的优先级是影响开发规划的一个主要因素。

    较常见的用户故事会引起较优先的需求。例如登录之于商城、readline 之于 CLI，都是最为常见的用户故事，相应的需求都是要首先开发的。

    另一方面，需求规模与需求优先级之间的关系。

    

## 软件架构工程

    **软件开发中的上游和下游**

    一个软件生产流程和一条河流很相似，所以我们很容易理解：随着流程一步步往下进行，我们在往下游移动。我们可以推出以下两个原则：

- 依赖原则：从自身的角度看，每个环节都依赖其上游的环节；

- 价值原则：往下游移动，每一环节都在产品上增加了价值。

    如果一个事物在另一个事物上增加了价值，或者以任何方式依赖另一个事物，那么它一定是下游。

    

# 参考

[需求入门： 需求工程＝需求开发＋需求管理 | 人人都是产品经理](https://www.woshipm.com/pd/30370.html)
