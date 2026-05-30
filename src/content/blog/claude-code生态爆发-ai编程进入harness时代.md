---
title: "Claude Code生态爆发，AI编程进入Harness时代"
id: claude-code生态爆发-ai编程进入harness时代
date: 2026-05-30
categories: AI热点
tags:
  - AI
  - Claude Code
cover: "/images/8304275f23f12c5c.jpeg"
---

# Claude Code生态爆发，AI编程进入Harness时代

![图片](/images/claude-code生态爆发-ai编程进入harness时代-1.jpg)

3月底，Anthropic的Claude Code因为一个意外事件被推到了聚光灯下。

npm发布包中的source map文件意外暴露了存储在官方R2存储桶内的未混淆源码。超过51万行TypeScript代码的工程样本，让外界第一次看清了工业级AI Agent系统的真实架构。

这件事本来应该是一个安全事件。但它反而成了AI编程领域最值钱的开源教材。

过去两个月，CSDN上涌现了十几篇深度解读Claude Code源码的文章。从Harness Engineering、记忆系统、编排循环、工具系统、权限模型到上下文工程，每个模块都有人拆解。

这不是巧合。这是生态爆发的信号。 ![图片](/images/claude-code生态爆发-ai编程进入harness时代-2.jpg)

* * *

## Harness Engineering，AI编程的新范式

Claude Code源码泄露后，一个词开始频繁出现——Harness。

Harness Engineering，直译是驾驭工程。在Claude Code的语境里，它指的是模型之外的所有工作，包括编排循环、工具系统、权限管控、记忆架构、上下文管理、事件驱动的自动化钩子

Anthropic把模型本身和Harness分得很清楚。模型负责思考和生成，Harness负责让模型在正确的边界内工作。

这个区分非常重要。它意味着AI编程的下半场，竞争焦点从模型能力转移到了Harness能力。

Claude Code定义了当前AI编程工具的上限。但它不对中国开发者开放。这个缺口，就是DeepSeek的机会。

DeepSeek最新组建了一个团队，专门做Harness。他们对这个团队的定义很清楚，正在把DeepSeek的前沿模型能力转化为领先的Agent产品，而除模型本身以外的所有工作，都属于Harness的范畴

模型之外，皆属Harness

* * *

## 记忆系统，AI编程的长期记忆

Claude Code的记忆系统是它最复杂也最有价值的模块之一。

它不是简单地把对话历史存下来。而是一套分层、可覆盖、可共享的记忆架构。

每次启动新会话时，Claude Code按七层顺序自底向上加载记忆文件

-   Git提交：企业全局强制策略
-   `~/.claude/CLAUDE.md：`个人全局偏好
-   `~/.claude/rules/*.md：`个人模块化规则
-   `./CLAUDE.md：`团队共享项目规范
-   `./.claude/rules/*.md：`路径级项目规则
-   `./CLAUDE.local.md：`个人项目覆盖（不入库，自动gitignore）
-   `./src/CLAUDE.md`等子目录文件：单仓库多包独立配置

越是上层的文件优先级越高，可以覆盖下层设置。

记忆类型分为短期记忆（当前会话的对话历史）、项目记忆（跨会话保留的结构化信息）、本地记忆、自动记忆。支持`@include`指令、条件记忆规则、自动记忆提取、记忆压缩和摘要、团队记忆同步。

最近还有消息说，Anthropic正在为Claude测试一套全新的「双模记忆系统」。相比现在「压缩成一段总结」的记忆方式，这次升级最大的变化在于，Claude或将开始像维护个人知识库一样，把用户长期对话拆分成多个可编辑、可检索、按主题分类的记忆文件

这意味着，AI编程的记忆能力，正在从「压缩总结」走向「结构化知识库」。 ![图片](/images/claude-code生态爆发-ai编程进入harness时代-3.jpg)

* * *

## Gemini CLI，Google的开源反击

就在Claude Code生态爆发的同时，Google也出手了。

Google DeepMind推出了Gemini CLI——一个完全开源的命令行AI编程工具，专门对抗昂贵的终端AI工具。

基于Gemini 2.5 Pro模型，支持多模态输入和本地文件操作。核心架构基于ReAct循环，支持自动化任务处理、代码库分析与多模态交互。

最狠的是免费层，每分钟60个模型请求，每天1000个请求，完全免费

虽然我喜爱Claude Code的质量，但Google刚刚让终端AI对大多数开发者来说基本上变成了免费。而且它完全开源。

Gemini CLI的安装非常简单，`npx https://github.com/google-gemini/gemini-cli。`它还提供了Python SDK，便于集成开发

Google的这个动作，把终端AI的门槛降到了地板。免费、开源、多模态。这对Claude Code和Cursor都是直接冲击。

* * *

## Dify，工作流平台的崛起

终端AI在爆发，工作流平台也在崛起。

Dify是一款开源的大语言模型应用开发平台。它融合了后端即服务（BaaS）的理念，使开发者可以快速搭建生产级的生成式AI应用。

Dify的核心能力包括AI Workflow工作流、RAG知识库、Prompt编排、多模型支持、Agent架构、数据存储设计

过去几年，AI应用开发存在一个很大的问题，大模型很强，但业务很难落地企业在接入AI时通常会遇到Prompt工程复杂、知识库构建困难、工作流编排混乱等问题。

Dify解决的就是这个问题。它让开发者可以通过可视化界面搭建AI工作流，不需要写代码就能实现复杂的AI应用。

Forrester定义了一个趋势，从任务级自动化向企业规模的流程编排的明确转变Dify正是这个趋势的受益者。

Dify工作流如何赋能企业智能化转型？有3大战略路径与5倍效率提升方案。支持Docker一键部署，可导入Dify、Coze等第三方工作流与智能体。 ![图片](/images/claude-code生态爆发-ai编程进入harness时代-4.jpg)

* * *

## 从单点工具到系统工程

把这三件事放在一起看，你会看到一个清晰的趋势。

Claude Code定义了AI编程的上限，它的源码被逆向工程，Harness Engineering成为一门新学科

Google推出Gemini CLI，开源免费，把终端AI的门槛降到地板

Dify等工作流平台崛起，从任务级自动化走向企业级流程编排

**AI编程正在从单点工具走向系统工程。**

过去我们关注的是模型有多强。现在我们关注的是Harness有多完善、记忆系统有多可靠、工作流有多灵活。

这个转变意味着什么？

第一，**AI编程的护城河从模型转移到了工程。**模型能力差距在缩小，Harness能力的差距在扩大。

第二，**开源正在重塑终端AI市场。**Gemini CLI免费开源，Claude Code源码被逆向，DeepSeek组建Harness团队。开源不再是选项，而是必选项。

第三，**工作流平台正在成为AI应用的基础设施。**Dify、Coze等平台让AI应用开发从代码走向配置。 ![图片](/images/claude-code生态爆发-ai编程进入harness时代-5.jpg)

* * *

## 开发者站在哪里

对于开发者来说，这个格局意味着什么？

第一，**学会Harness Engineering。**这不是一个技能，而是一个思维范式。模型之外的所有工作，都属于Harness。

第二，**拥抱开源工具。**Gemini CLI、Claude Code的逆向工程、DeepSeek的Harness团队，都在降低AI编程的门槛。

第三，**关注工作流平台。**Dify、Coze等平台让AI应用开发从代码走向配置。这不是取代开发者，而是让开发者专注于更高价值的工作。

* * *

## 还没结束

Claude Code的源码泄露，本来是一个安全事件。但它反而成了AI编程领域最值钱的开源教材。

这本身就说明了一个道理，AI编程的生态正在从封闭走向开放，从单点走向系统，从模型走向Harness ![图片](/images/claude-code生态爆发-ai编程进入harness时代-6.jpg)

这个转变才刚刚开始。

说实话，我自己觉得，我们现在正处于一个非常关键的转折点。AI编程不再是「用哪个模型」的问题，而是「如何构建完整的AI编程系统」的问题

这个系统的核心，不是模型，而是Harness。