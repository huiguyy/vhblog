---
title: "DeepSeek 把 Agent 做成白菜价"
id: deepseek-把-agent-做成白菜价
date: 2026-08-02T07:24:44.320Z
categories: AI每日热点解析
tags:
  - AI
  - GPT
  - Claude
  - OpenAI
  - Anthropic
  - Cursor
cover: "https://raphael.18.do/images/7333ea53-3dbd-4bd8-8fbb-698fb2397025.jpg"
---

# DeepSeek 把 Agent 做成白菜价
![封面_DeepSeek掀性价比革命](/images/2455375f-1067-4c7a-962b-c6f457e88774.png)


7 月 31 日下午，DeepSeek 在 API 文档里悄悄挂出一行更新日志。

V4-Flash 正式版，公测开放。

没有发布会，没有热搜预告。但看完那串基准分数，我后背有点发凉。

**底座一个字没动，Agent 能力直接翻了 6 倍。**

* * *

## 一次后训练，把 Agent 唤醒了

先说清楚一件事，这次的 0731 正式版，模型结构跟预览版一模一样。

还是那个 MoE，总参 2840 亿，每次只激活 130 亿，上下文还是 100 万 token。底座没换，变的是「后天教育」，一轮新的后训练加对齐优化。

效果有多猛，看这个数就够了。

DeepSWE，专门测 AI 编程 Agent 解题能力的榜，预览版只有 **7.3 分**，正式版直接干到 **54.4 分**。

**超过 6 倍。**

这不是挤牙膏，是把盖子掀了。同一副脑子，换种教法，突然就会自己干活了。

> 模型不再满足于陪你聊天、帮你补全代码，它想自己上手。

DeepSeek 自己写的更新说明里，竞争重点已经从对话和代码补全，转向 Coding Agent、工具调用和自动化执行。

这句话翻译过来就是，它不想当助手了，它想当工人。

* * *
![插图_01_同一副脑子换教法](/images/9d0066cb-a930-477d-aaeb-73304b878f4e.png)


## 智能指数 50 分，只比 Luna 低 1 分

Artificial Analysis 的智能指数榜上，V4-Flash 0731 拿了 **50 分**。

隔壁的 GPT-5.6 Luna，最高 **51 分**。

就差 1 分。

但你要看价格。OpenAI 刚把 Luna 砍了 80% 的价，DeepSeek 在自己 API 上跑同一个任务，成本还是比 Luna 低约 **60%**。

换算成大白话，DeepSeek 这次的单价，差不多是 Luna 的 **四成**。

输出端定价每百万 token 只要 **0.28 美元**，缓存命中时更低到 **0.02 元** 每百万 token。它给的缓存命中折扣约 98%，业内普遍才 90%。

一个 Agent 任务动辄几十轮对话、长上下文反复刷，这差价到月底结账时能差出几十倍。

前端代码竞技场更离谱，V4-Flash-High 在 [Arena.ai](http://Arena.ai) 拿了 **1586 分**，比预览版涨了 154 分。

**免费榜首的压力，现在在 DeepSeek 这边。**
![插图_02_指数持平价砍六成](/images/93be8dfa-7cd1-4c8b-9ef1-73719970a8fb.png)


* * *

## 它能不能塞进 Claude Code

这是开发者最关心的问题。

答案是，能，而且几乎零成本。

DeepSeek 这次原生支持了 OpenAI 的 Responses API 格式，还专门针对 Codex 做了适配。更关键的是，它有一层兼容 Anthropic 协议的 API 端点。

也就是说，理论上改一行环境变量，就能把 Claude Code 的「大脑」换成 DeepSeek。

```
ANTHROPIC_BASE_URL=https://api.deepseek.com/anthropic
ANTHROPIC_AUTH_TOKEN=你的DeepSeekKey
ANTHROPIC_MODEL=deepseek-v4-flash
```

就这三行，Claude Code 还是那个 Claude Code，底下跑的已经不是 Opus 了。

社区里还有个 DeepSeek TUI，已经 23K Star，跑的就是跟 Claude Code 一样的 Agent Loop，读代码、改文件、跑测试、汇报结果，循环往复。

它甚至做了个路由，简单问题用 Flash 低推理，复杂调试自动切 Pro 高推理。

**比 Claude Code 固定模型那套，灵活不少。**
![插图_03_一行配置换大脑](/images/956d218f-605c-4567-842c-75623a076c27.png)


* * *

## 真相是分流，不是替代

先把话说死一边都不负责任。

能力上，V4-Flash 确实摸到了第一梯队的门槛。Terminal Bench 2.1 拿 **82.7**，逼近 Opus 4.8 的 **85.0**，把 GLM-5.2 的 81.0 和自家 Pro 预览版的 72.1 甩在身后。Agent Last Exam 拿 **25.2**，跟 Opus 4.8 的 25.7 几乎贴脸。

但三个现实你得认。

第一，这次只是 Flash 线进公测，V4-Pro 的 App 和网页端还没动，复杂长链路任务 Opus 仍是天花板。

第二，Claude Code 那套 Skills、MCP、生态沉淀，不是换个模型端点就能搬走的。

第三，超长上下文和极致工程化质量上，闭源旗舰还有余量。

所以不是「DeepSeek 干掉 Claude Code」。

是**同一把锤子，多了一个便宜四成的头**。

日常 Agent 任务、成本敏感的批量跑、个人开发者练手，V4-Flash 已经够用，甚至更香。真到了要架构级决策、要替你背锅的硬活，Opus 暂时还不可替代。

* * *
![插图_04_分流不是替代](/images/cbc27b32-5fa8-4285-9699-8338081b3cc2.png)


## 这波性价比革命，砸向的是谁

我有时候觉得，DeepSeek 这步棋最狠的不是技术。

是它把「Agent 能力」从奢侈品货架，搬到了批发档口。

过去你想跑一个能自己改代码、自己调工具的 Agent，账单是 Opus 那档的几十美元每百万 token。现在同样的事，DeepSeek 告诉你，四折，还附赠 100 万上下文。

这对 AI 编程工具的格局意味着什么，不用我多说。

Cursor、Claude Code 卖的是「聪明的大脑加好用的壳」。当大脑可以四折换、壳又能一行配置接上，护城河就剩那层壳和生态了。

**便宜不会赢，但便宜加够用，会松动一切。**
![插图_05_白菜价搬货架](/images/7e234fcb-f288-4c7c-952f-6cd90fd3d2ab.png)


梁文锋把 Agent 做成白菜价这步，2026 年下半年的 AI 编程战争，已经从「谁更聪明」转向「谁更敢便宜」。

这局，DeepSeek 先落子了。