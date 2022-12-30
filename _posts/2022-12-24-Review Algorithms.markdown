# Review Algorithms（复习算法）

    忽然对这个 topic 很感兴趣，因为它确实很实用，能科学地帮助人记忆更多信息。

## 从 Anki 这款产品聊起

    [Anki](https://apps.ankiweb.net) 是比较著名的单词记忆软件，当然不止是单词，还包括各种碎片知识。



## 主流算法及其特性

    目前的复习算法主要可以[分为两大类别][ref1]：以 SuperMemo 为代表的状态转移法，以 Duolingo 为代表的机器学习方法。

    有关状态空间和状态转移的背景知识参考[此处][ref2]，其核心在于维护状态转移表



## 应用到 OneTab 产品上

    [Onetab](https://www.one-tab.com) 是一款实用的Todo类软件，能记录下一些待办的 URL。相似的产品还包括 Edge Collections，但我没怎么用过。因为按照我的需求，这些 URL 都是**将亡的**，所以不需要花这么多心思去打标签。我只想要 URL 和 Abstract 两部分即可，这些 Onetab 都能提供。

    我们可以将 Onetab 建模为一个一维的 Queue，理论上应当做到**先进先出**，即先 Pin 的 URL 应当先 review，且应当符合**记忆规律**。

    新需求是，Onetab 的行为是完全静态的，我希望它能**动态地**提醒我哪些 URL 是时候 review 了，不然当初将其 collect 下来是没有意义的，因为 forget 之后再看其内容就和 first meet 这个页面没什么区别了。真实的情况是，我的 Queue Length 始终维持在 200 上下水平，且有增长趋势，并且很多队头的项根本没有在合适的时机 Unpin。

    所以，我需要引入一款 Review Algorithm。我采用的是





---

[ref1]: https://zhuanlan.zhihu.com/p/343419228

[ref2]: https://zhuanlan.zhihu.com/p/344716900 搜索记忆的状态空间


























