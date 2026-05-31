---
title: "DeepSeek终于能看图了，AI编程工具也疯了"
id: deepseek终于能看图了-ai编程工具也疯了
date: 2026-05-31
categories: AI热点
tags:
  - DeepSeek
  - IDE
cover: "/images/6a01ba3985d9f964.jpeg"
---

# DeepSeek终于能看图了，AI编程工具也疯了
![图片](/images/5945da72656126ee.jpeg)

昨天，DeepSeek灰度上线了识图模式。今天，多模态技术报告正式发布。

这份报告的名字很有意思，《用视觉原语思考》(Thinking with Visual Primitives)。核心创新是，把点、边界框这些空间标记提升为「思维的基本单元」，让模型在推理时能够「指代」，把认知轨迹锚定在图像的物理坐标中。

简单讲，以前AI看图是用语言来「描述」图片。现在AI看图是用视觉来「思考」图片。

这不是一个小升级。这是一个范式转变。

* * *

## DeepSeek的视觉原语，到底在做什么
![图片](/images/aeb922cec477dde7.jpeg)

主流的思维链(CoT)范式，一直主要局限在语言学领域。AI的思考过程说到底就是一串文字推理，即使看图，也是先把图片转成文字描述，再进行推理。

DeepSeek多模态模型提出的是另一条路。基于视觉原语的思考，将点、边界框等空间标记直接融入思考过程，让模型在推理时能「指代」图像中的具体位置。

这个模型参数量284B，激活13B，基座是DeepSeek-V4-Flash。虽然模型规模紧凑且图像标记预算显著较低，但在计数和空间推理基准测试上，能够与GPT-5.4、Claude-Sonnet-4.6和Gemini-3-Flash等前沿模型匹配。

DeepSeek称，权重将整合进基础模型，未来发布。

坦率的讲，这件事的意义在于，它为开发更高效、更具可扩展性的System-2类多模态智能指明了方向。不是用更大的模型来硬扛，而是用更聪明的思考方式来突破。

* * *

## Understand Anything，3万星的代码理解神器
![图片](/images/29e3a97c3615b579.jpeg)

就在DeepSeek发布多模态模型的同时，GitHub上另一个项目也在爆发式增长。

Understand Anything，上线数月，狂揽近3万颗Star，持续霸榜GitHub Trending。仅5月29日一天就涨了3776星，7天累计31336。

它做的事听起来很简单，把任何代码库变成一张可以点击、搜索、提问的「知识地图」。

不是帮你「找代码」，而是帮你「懂代码」。这两件事之间，差了一个数量级。

Understand Anything基于Claude Code，通过多智能体(Multi-Agent)管道分析代码库。7个专业Agent流水线并行分析，Tree-sitter确定性解析加上LLM语义理解双引擎。

它支持三种视图，结构图、业务域图、知识库图。15个AI编程平台一键安装，包括Claude Code、Cursor、Copilot、Codex、Gemini CLI、OpenCode、OpenClaw等。

增量更新只分析改动文件，知识图谱JSON可提交Git与团队共享。

我自己觉得，这个项目之所以能爆，是因为它补齐了AI编程最大的短板。AI编程助手最大的问题不是写不出代码，而是看不到全局。Understand Anything给了AI一双能看懂全局的眼睛。

* * *

## Grok Build vs Trae，AI编程工具战升级
![图片](/images/a60422812cace904.jpeg)

5月25日，xAI正式发布Grok Build，一款终端CLI的AI编程智能体。

Grok Build的核心亮点包括Plan Mode（规划模式），针对复杂开发任务自动生成详细执行计划。开发者可以在任务执行前查看、评论、修改甚至完全重写该计划。

它还集成了Imagine工具，在开发过程中直接调用AI生成图片与视频资源。对于超大规模任务，Grok Build能自动拆解并指派多个子智能体(Sub-agents)并行处理。

实战数据出来了。Kilo Code测试Grok Build 0.1，要求其使用TypeScript、Bun和SQLite构建webhook交付服务，整个成本约1.65美元。零工具调用失败，且成本低于GPT-5.5和Claude Opus 4.7。

不过Grok Build的门槛不低。SuperGrok Heavy每月300美元订阅层级才能用。马斯克在X上回复称「物超所值」。

另一边，字节跳动的Trae走的是完全不同的路线。AI原生IDE，免费开放核心功能，全链路团队协作与规范管控。搭载长上下文理解机制，可完整索引整个代码仓库内容。

Trae对国内开发者更友好。语言和易用性上更符合国人习惯，而且现阶段完全免费。

**Grok Build是高端付费路线，Trae是大众免费路线。**两条路线都在咬AI编程这个市场。

* * *

## 三个信号
![图片](/images/82a61dfc5c6b35ca.jpeg)

把这三件事放在一起看，三个信号很清晰。

第一，**多模态正在从附加能力变成核心能力**。DeepSeek的视觉原语不是在看图说话，而是在用视觉思考。这是质的区别。

第二，**代码理解正在成为AI编程的新战场**。Understand Anything 3万星不是偶然。AI编程的下一个瓶颈不是写代码，而是懂代码。

第三，**AI编程工具的分层在加速**。Grok Build月费300美元走高端，Trae免费走大众，Gemini CLI免费开源走生态。三层价格带已经形成。

* * *

## 开发者该怎么看
![图片](/images/ec9ab8bd55232692.jpeg)

说真的，我觉得现在是一个非常好的时机。多模态能力在突破，代码理解工具在成熟，编程工具在分层。

如果你是独立开发者，Trae和Gemini CLI的组合基本够用，而且免费。如果你是专业开发者，Grok Build和Claude Code的高阶功能值得投入。

Understand Anything呢，无论你用哪个编程工具，都建议装一个。看懂代码比写代码更重要，这件事我越来越确信。