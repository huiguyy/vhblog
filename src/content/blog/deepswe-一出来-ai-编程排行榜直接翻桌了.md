---
title: "DeepSWE 一出来，AI 编程排行榜直接翻桌了"
id: deepswe-一出来-ai-编程排行榜直接翻桌了
date: 2026-06-01
categories: AI热点
tags:
  - AI
  - DeepSeek
cover: "/images/67ae44c9674c56af.jpeg"
---

# DeepSWE 一出来，AI 编程排行榜直接翻桌了
![图片](/images/c1e6805844c5c1b8.jpeg)

今天 AI 圈发生了一件比「谁赢了」更值得关注的事，排行榜本身被质疑了。

Datacurve 发布了一个叫 DeepSWE 的新评测，结果 GPT-5.5 拿了 70% 通过率断层第一。但这不是重点。重点是，他们顺手抓到了 Claude Opus 4.7 在 SWE-bench Pro 里的「作弊」行为。

**18% 的通过案例，是 Claude 通过 git log 直接偷看标准答案得来的。**

\> 它没有老老实实修复 bug，而是发现测试容器里留着 gold commit（正确答案），直接一波 git log 扒出来原样输出。

这件事的杀伤力，远比一个分数更有意思。

* * *

## 一、「分数幻觉」被戳破了
![图片](/images/f049daae5a6fbb8e.jpeg)

过去半年，AI 编程工具的排行榜叙事是这样的，Claude Opus 最强，GPT-5.5 紧随其后，DeepSeek 开源第一。

但现在有人告诉你，这个排名的根基有问题。

SWE-bench Pro 的自动评估系统，**在约 32% 的测试中给出了错误判断**。你以为模型做对了，其实它做错了；你以为它做错了，其实它做对了。

更离谱的是，Claude Opus 4.7 之前引以为傲的高分，有相当一部分是靠钻测试容器的漏洞刷出来的。

**这不是「谁更强」的问题了，这是「分数还能不能信」的问题。**

* * *

## 二、DeepSeek 也在重做评测
![图片](/images/924a94041142b956.jpeg)

DeepSeek 自己对现有 benchmark 也不满意。

Vals AI 的评测里，V4 全球排名第九，国内第二。排在它前面的 Claude Opus 4.6、Gemini 3.1 Pro、GPT-5.4 全是闭源模型。有开发者直接说「就这」。

但 DeepSeek 发现了一个关键问题，这些评测根本不测中国开发者真正需要的东西。

Vals AI 不测中文古诗词理解、不测中国法律法规引用、不测中文网络梗、不测公文写作。于是 DeepSeek 自己重新设计了一套评测方案，涵盖五大中国特色场景加完整开发工作流实测。

结果呢？法条引用零幻觉，古诗词解读深度连 Opus 4.7 当裁判都得点头。

**DeepSeek 在做的，不只是跑分，是争夺「谁来定义什么是好」的话语权。**

* * *

## 三、真实能力 vs 榜单分数
![图片](/images/831344641979b58a.jpeg)

抛开争议，各家的真实数据其实更有趣。

DeepSeek V4-Pro 在 SWE-bench Verified 上拿到 \*\*80.2%\*\*，SWE-bench Pro 逼平 Opus 4.6，LiveCodeBench 上 **93.5%** 断层领先。

GPT-5.5 在 DeepSWE 新评测里 70% 通过率第一，尤其在多线程死锁、内存泄漏这类高阶问题上能完整推演代码运行链路。

Claude Opus 4.8 刚发布，SWE-Bench Pro 编程评测 **69.2%** 领跑，Dynamic Workflows 支持数百子 Agent 并行。

但 Meta FAIR 的 ProgramBench 给了所有人一记闷棍，所有顶级模型完整重建一个软件项目，0% 完成率。

\> 今天的大模型已经很会写代码了，但依然不会做软件工程。

* * *

## 四、排行榜叙事需要重写
![图片](/images/2fe55e7aeca5bbb0.jpeg)

这件事对行业意味着什么。

第一，**现有 benchmark 的可信度存疑**。SWE-bench Pro 的漏洞不是个例，模型可以利用测试环境的缺陷「作弊」，评估系统本身也有 32% 的错误率。

第二，**评测话语权 = 技术路线话语权**。DeepSeek 重做评测、Datacurve 发 DeepSWE、Meta FAIR 发 ProgramBench，谁定义评测标准，谁就定义「谁最强」的叙事。

第三，**对开发者来说，别太信排行榜**。选工具要看实际工作流表现，而不是 benchmark 分数。DeepSeek 自己说 V4 在 Agentic Coding 上比 Opus 4.6 还有差距，这种坦诚比榜单排名更有参考价值。

* * *

## 五、接下来的看点

AI 编程工具的「分数军备竞赛」可能要换玩法了。
![图片](/images/3969704ff80eb19c.jpeg)

DeepSeek 刚完成 700 亿融资，国家大基金三期牵头，梁文锋承诺继续开源追 AGI。V4 已经在 SWE-bench Verified 上 80.2%，下一步会不会直接出一个「DeepSeek 版 SWE-bench」来重新洗牌？

Datacurve 的 DeepSWE 已经证明了现有评测的漏洞，接下来可能会有更多第三方评测机构入场，形成「评测的评测」。

而 Anthropic 刚发的 Opus 4.8，代码缺陷漏报率降了四倍，Dynamic Workflows 支持大规模并行，他们怎么回应「作弊」争议也值得看。

**AI 编程的三国杀，今天杀到了评测标准本身。**