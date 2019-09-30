# 如何撰写 Code Review 评论

## 总结

-   善待。
 - 解释你的推理。
 - 在给出明确的指示与只指出问题并让开发人员自己决定间做好平衡。
 -   鼓励开发人员简化代码或添加代码注释，而不仅仅是向你解释复杂性。

## 礼貌

一般而言，重要的是要礼貌和尊重，同时对正在审查其代码的开发人员非常清楚和有帮助。 一种方法是确保您始终对代码发表评论，而不是对开发人员发表评论。 你并不总是必须遵循这种做法，但在说出可能令人不安或有争议的事情时你绝对应该使用它。 例如：

糟糕：“为什么这里**你**使用了线程，显然并发并没有带来什么好处？”

好的：“这里的并发模型增加了系统的复杂性，但没有任何实际的性能优势，因为没有性能优势，最好是将这些代码作为单线程处理而不是使用多线程。”

## 解释为什么{#why}

关于上面的“好”示例，您会注意到的一件事是，它可以帮助开发人员理解您发表评论的原因。 并不总是需要您在审查评论中包含此信息，但有时为了表明您的意图，追加您在遵循的最佳实践，或为您建议如何提高代码健康状况提供更多解释是恰当的。

## 给予指导 {#guidance}

**一般来说，修复 CL 是开发人员的责任，而不是审查者。您无需为开发人员详细设计解决方案或编写代码。**

但这并不意味着审查者应该没有帮助。一般来说，您应该在指出问题和提供直接指导之间取得适当的平衡。指出问题并让开发人员做出决定通常有助于开发人员学习，并使代码审查变得更容易。它还可以产生更好的解决方案，因为开发人员比审查者更接近代码。

但是，有时直接说明，建议甚至代码会更有帮助。代码审查的主要目标是获得最佳 CL。第二个目标是提高开发人员的技能，以便他们随着时间的推移需要的审查越来越少。

## 接受解释 {#explanations}

如果您要求开发人员解释一段您不理解的代码，那通常会导致他们**更清楚地重写代码**。偶尔，在代码中添加注释也是一种恰当的响应，只要它不仅仅是解释过于复杂的代码。

**仅在代码审查工具中编写的解释对未来的代码阅读者没有帮助。**这仅在少数情况下是可接受的，例如当您查看一个您不熟悉的领域时，开发人员会向您解释代码的普通读者已经知道的内容。

下一篇：[处理 Code Review 中的抵触](pushback.md)
