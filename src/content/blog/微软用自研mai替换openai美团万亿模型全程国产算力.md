---
title: "微软用自研MAI替换OpenAI，美团万亿模型全程国产算力"
id: 微软用自研mai替换openai美团万亿模型全程国产算力
date: 2026-07-08T00:44:31.869Z
categories: AI热点
tags:
  - AI
  - GPT
  - Claude
  - OpenAI
  - Anthropic
  - Copilot
---

# 微软用自研MAI替换OpenAI，美团万亿模型全程国产算力
![cover_封面](/images/b8836e57-d259-4d26-b240-938a4b335569.png)


* * *

## 一、微软开始「去OpenAI化」

7月8日，The Information报道，微软已经在Excel和Outlook里用自研的MAI模型替换OpenAI和Anthropic的模型。每周通过MAI处理的AI提示词已达数万条量级。

这不是小测试。这是微软AI负责人Mustafa Suleyman主导的「断奶工程」。

6月Build大会微软一口气发布了7款自研MAI模型。MAI-Thinking-1做推理，35B激活参数MoE架构，256K上下文，数学竞赛94.5%。MAI-Code-1-Flash已经在GitHub Copilot和VS Code里上线。MAI-Image-2.5进了PowerPoint和OneDrive。MAI-Transcribe-1.5支持43种语言语音转写。

**8月Project Polaris将取代GPT-4 Turbo成为Copilot默认引擎。**

Suleyman在内部分明说，MAI一款模型的代码生成能力媲美Anthropic Opus 4.6，但成本远低。未来几个月MAI语音转写模型还会进Teams。

**微软投了OpenAI 130亿美元，投了Anthropic 50亿美元，到头来还是决定自己造发动机。**
![illust_01_微软七款MAI模型](/images/5d7ac866-c170-43c1-844f-38c8408e1e75.png)


* * *

## 二、为什么微软必须自研

答案只有一个，成本。

Copilot每次调用OpenAI模型，微软都要付钱。用户量越大，账单越吓人。当Anthropic Opus 4.8输出价25美元/百万token，每天数亿次调用，这是一笔天文数字。

**用自研MAI，成本直降30%。**

但成本不是唯一原因。

OpenAI拒绝透露o1模型详细技术文档，微软不满意。OpenAI和微软的技术合作出现矛盾。OpenAI自己做硬件跟博通合作发布Jalapeño芯片，OpenAI自己筹谋IPO，OpenAI跟Apple合作Frontier平台。微软意识到，把命脉交给一个越来越独立的合作伙伴，风险太高。

**自研是必然选择。微软不能再当OpenAI的经销商。**

7月还有个细节。执行副总裁Jacob Andreou发内部备忘录，整合消费者版和企业版Copilot的App，裁撤低效功能，目标是在客户眼中「赢得存在的权利」。

**微软开始向内要效率了。**
![illust_02_Copilot换发动机](/images/84bcdf62-6f11-4045-88fb-46b05bc9de17.png)


* * *

## 三、美团LongCat-2.0，另一个维度的突破

就在微软自研MAI消息传出的同一周，7月6日，美团正式开源LongCat-2.0。

**业界首个在五万卡国产算力集群上完成全流程训练与推理的万亿参数模型。英伟达含量为零。**

总参数1.6T，平均激活约48B，动态范围33B~56B。原生支持1M超长上下文。预训练数据超过30T tokens。SWE-bench Pro 59.5，超越GPT-5.5。

架构上引入LongCat稀疏注意力和N-gram Embedding，提升长上下文处理效率。专为Agentic Coding任务打造。

**美团还做了一件少见的事。同步开源BF16、FP8、INT8多精度版本，全面覆盖不同算力平台部署需求，针对国产算力极致优化的推理代码也同步开源。**

这意味着，即使手上没有最新算力，也能基于现有硬件把LongCat-2.0稳定跑起来。

LongCat-2.0预览版以Owl Alpha匿名接入OpenRouter平台后，调用量冲进全球前三，Hermes月调用量全球第一。
![illust_03_成本直降30%](/images/0d7f02ef-f9fc-46d3-bfc7-01eba33c28fb.png)


* * *

## 四、两条路，一个方向

微软和美团，一个是去外部依赖，一个是从零做国产算力。看上去是两件事，本质上指向同一个方向。

**核心技术必须握在自己手里。**

微软投了130亿美元给OpenAI，最后发现还是得自研。美团做过外卖做过本地生活，现在用五万卡国产芯片训出万亿参数模型。两个决策背后是同一种判断，依赖别人是有上限的。

对开发者来说，这意味着两件事。

**第一，模型选择会更多元。** 微软MAI进Copilot，美团LongCat开源进OpenRouter，加上GPT-5.6、Claude、DeepSeek、豆包、MiniMax M3、智谱GLM-5.2，2026年下半年的模型市场已经不是几家独大，而是百花齐放。
![illust_04_LongCat国产算力](/images/dd0766ef-8ae0-451e-a81c-b728bf1cfe9b.png)


**第二，国产算力跑通了。** LongCat-2.0证明了五万卡国产芯片能完成万亿参数全流程训练和推理。这意味着，即使英伟达断供，中国大模型也不会停。

**微软的自研是防守反击。美团的国产算力是战略储备。**

两条路都通向同一个终点，自主可控。下周LongCat-2.0的SWE-bench Pro 59.5%数据如果能在更多任务上复现，国产算力训练的模型就真正站稳了。

这场仗才刚开始。