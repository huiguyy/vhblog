---
title: "国产模型重写了AI编程的工具链"
id: 国产模型重写了ai编程的工具链
date: 2026-06-13
categories: AI热点
tags:
  - AI
  - DeepSeek
  - MiniMax
  - OpenCode
  - Claude
cover: "/images/159af1e93f9a7a59.jpeg"
---

# 国产模型重写了AI编程的工具链
![图片](/images/8926e9189f309fcd.jpeg)

## 三张成绩单，同一句潜台词

过去两周，三组数字几乎同时甩到了桌上。

**MiniMax M3**，SWE-Bench Pro 59.0%，超过GPT-5.5（58.6%）和Gemini 3.1 Pro。华为云昇腾算力适配同步完成，6月12日官宣。

**Qwen3.6-Plus**，Terminal-Bench 2.0拿了61.6分，第一个在这个基准上超过Claude Opus的国产模型。200K上下文，参数量不到Kimi K2.5的一半。

**DeepSeek V4-Pro**，SWE-Bench 80.6%，只比Claude Opus 4.6低0.2个百分点。输出价格3.48美元/百万token，Opus是25美元。差7.2倍。

三个模型，三个团队，三个方向。但潜台词是一样的，编程能力的天花板，不再只属于闭源巨头。

而且这次不一样的地方是，不是「追上了」，而是「用1/7的价格追上了」。
![图片](/images/51fad5c97d58484c.jpeg)

* * *

## Claude Code的壳，DeepSeek的芯

这才是本周最荒诞也最有意思的事。

Claude Code是现在程序员圈子里最火的终端编程工具。界面好，交互好，能自动读项目、改文件、跑命令、交diff。但有个问题，贵。

然后有人发现了一件事，DeepSeek V4提供了一个Anthropic兼容的API端点，地址是`/anthropic`。

你只需要两步。第一，把环境变量里的API地址指向`api.deepseek.com/anthropic`。第二，把鉴权信息换成你的DeepSeek API Key。

Claude Code的客户端以为自己还在跟Anthropic聊，后台实际跑的是DeepSeek V4。交互体验一样，成本降了差不多十分之一。

「deepseek claude code」这个搜索词在2026年5月暴涨了170%。

GitHub上有个项目叫`claudian-deepseek-tutorial`，教你把Claude Code嵌入Obsidian用DeepSeek V4驱动，标注使用成本$1/小时。还有个`ccSwitch`工具，图形界面一键切模型，DeepSeek、Qwen3.6、Kimi全适配。

说真的这不算什么高深操作，但效果太好了。你用着Anthropic精心设计的交互界面，跑着国产模型的推理能力，付着1/7的钱。Claude Code变成了一个壳。
![图片](/images/7ea4aafcede53624.jpeg)

* * *

## OpenCode 17万星，小米也下场了

Claude Code还有一个问题，不开源。你能用，但不能改。

OpenCode跳了出来。GitHub 17万+ Stars，对标Claude Code，完全开源MIT协议，模型随便换。博客园上有篇6月6日更新的实战帖，标题就叫「AI Coding工具一站配齐，适合国内网络环境」，作者的搭配已经定型，OpenCode做Agent，DeepSeek/Qwen3.6/MiniMax做模型。

然后小米也来了。

6月11日，小米发布MiMo Code V0.1.0，基于OpenCode二次开发，MIT开源。内置MiMo-V2.5多模态模型，限时免费，同时支持接入DeepSeek、Kimi、GLM这些主流大模型。

小米做这件事的逻辑很清楚，手机厂商做AI编程工具，模型是自己的，但Agent框架需要快速建起来。OpenCode省了从零造轮子的时间。

这也意味着AI编程工具的竞争，不再只是「谁的模型更强」，而是谁的Agent框架+模型组合更灵活、更便宜、更适合国内开发者。
![图片](/images/ca2450c54e3085e2.jpeg)

* * *

## Copilot涨价60倍，国产模型递刀子

6月1日，GitHub Copilot正式从固定额度订阅制切换到AI Credits按量计费。代码补全还免费，但Chat、Agent模式、PR摘要这些功能，每次调用按Token消耗扣积分。

对轻度用户没影响。但对重度Agent用户来说，月账单可能从10美元飙到几百美元。

同一周，Copilot Pro版涨到39美元/月。

这边涨着，那边国产模型在降价。DeepSeek V4-Pro输出3.48美元/百万token，MiniMax M3输入2.1元/百万token。按汇率算，M3的价格大约是Claude Opus的1/20。

这组数字放在一起就很扎心了。你用着最贵的工具，跑着最贵的模型，做着和1/10成本的人一样的事。而那个人用的是开源框架，跑的是国产模型，还不用翻墙。
![图片](/images/47de2753fcef88a9.jpeg)

* * *

## 工具链变了，从「买谁家」变成「拼谁家」

2026年上半年的AI编程工具链，正在经历一个结构性的变化。

之前的逻辑是买谁家的服务，Copilot捆绑GPT，Claude Code捆绑Opus，Cursor捆绑自己的模型层。整个链条从上到下都是一家的。

现在的逻辑是拼谁家的。Agent层用OpenCode或Claude Code，模型层插DeepSeek V4或Qwen3.6-Plus，上下文和微调自己做，成本自己控。

博客园那篇实战帖说得精准，选OpenCode不选Claude Code的原因就三个，MIT开源、模型可换、国内网络直连。再加上小米MiMoCode、CrabCode这些二次封装版本，Agent层的选择比半年前多了一倍。

模型的这边更夸张。MiniMax M3开了1M上下文+MSA稀疏注意力，Qwen3.6-Plus的Agentic Coding能自主规划+调用工具+执行验证，DeepSeek V4直接在API层面做了Anthropic兼容。三家的策略不同，但都指向同一件事，让开发者用最低的迁移成本，获得最好的编程体验。
![图片](/images/1f4cad0ca9f99fe8.jpeg)

工具链的竞争规则变了。不是谁家的模型分数最高谁赢，是谁的组合拳最灵活、成本最低谁赢。

这也解释了为什么Claude Code的用户疯狂给DeepSeek送钱。他们不是背叛Anthropic，他们做的事很简单，用最好的壳，配最划算的芯。工具链本来就是用来组合的，不是用来锁定的。