---
title: "OpenAI掏出30天免费迁移，AI编程工具战从比模型变成抢人"
id: openai掏出30天免费迁移-ai编程工具战从比模型变成抢人
date: 2026-06-28
categories: 随笔
tags:
  - 随笔
cover: "/images/9195b82bdc44db81.jpeg"
---

# OpenAI掏出30天免费迁移，AI编程工具战从比模型变成抢人
![图片](/images/ea1691cc69c1dcd2.jpeg)

* * *

## 一、Codex ultrafast模式，速度再翻倍

今天OpenAI放了大招。

Codex正式上线**ultrafast模式**，速度提升2到3倍，专为延迟敏感型任务设计。你敲一行代码，它比你眨眼还快给你补完。

但ultrafast只是前菜。

真正的杀手锏是GPT-5.6已经进了Codex内部测试。知名爆料人Leo从OpenAI内部Codex日志的rollout\_mapping.json里扒出了调用记录，两个内部代号ember-alpha和beacon-alpha，当前分别有0.03%和0.01%的流量在跑canary测试。

GPT-5.5上线才三周，下一代就已经在跑测试了。这个迭代速度在大模型行业前所未有。

更狠的是定价。GPT-5.6旗舰版Sol，输入5美元/百万token，输出30美元。同期Claude Fable 5是输入10美元，输出50美元。

**Codex比Claude Code便宜了一半，速度还更快。**

* * *

## 二、30天免费迁移，赤裸裸抢人

OpenAI宣布了一个政策，未来30天内，企业用户如果迁移到Codex，**2个月免费用量**。

这不是重点。重点是桌面端内置了迁移工具。

Claude Code的system prompts、custom skills、chat history、MCP server配置，**一键全搬过来**。

你不需要重新配环境，不需要重新写prompt，不需要重新训练skill。你原来在Claude Code里积累的一切，30秒搬到Codex。

这才是真正的抢人。

开发者为什么一直不换工具，不是因为Claude Code最好，是因为迁移成本太高。你的skill库、你的prompt模板、你的聊天历史、你的MCP配置，全在Claude Code里。换工具等于从头开始。

OpenAI把这个成本打到零了。

2个月免费加一键迁移。这不是促销，这是宣战。
![图片](/images/879dc076fabd74eb.jpeg)


* * *

## 三、Claude Tag，AI虚拟同事来了

Anthropic没闲着。

6月23日，Anthropic发布**Claude Tag**，一个以"AI虚拟团队成员"身份直接加入Slack的协作工具。

用法简单到离谱，在Slack里@Claude，它就来了。它会主动从频道历史里提取相关信息建立上下文，不是那种你问一句它答一句的呆板机器人，是真的能读懂当下、随时加入讨论、推动工作向前走。

\> Anthropic表示，其产品团队目前已有65%的代码由内部版本的Claude Tag生成。

**65%。**

这不是demo数据，这是Anthropic自己生产环境的数据。

Claude Tag目前已在Slack上推出，向Claude Enterprise和Team版客户开放Beta，未来30天内将逐步替换原有的"Claude in Slack"。

可以理解为，Claude Code是给开发者个人用的编程工具，Claude Tag是给整个团队用的AI同事。一个to开发者，一个to团队。
![图片](/images/93a9d107702b36e7.jpeg)
* * *


## 四、从模型比拼到工具生态战

把这三件事放一起看，你会发现AI编程赛道的竞争维度变了。

**上一轮是比模型。** SWE-Bench Pro跑分，Claude Fable 5是80.3%，GPT-5.5是58.6%，谁强谁弱一目了然。

**这一轮是比生态。**

OpenAI的打法，用ultrafast拉速度，用GPT-5.6拉能力，用30天免费迁移拉用户，用一键迁移工具消除切换成本。四板斧组合拳，不跟你跑分玩，直接抢你的装机量。

Anthropic的打法，用Claude Tag从开发者工具升级成团队协作平台。不跟你拼CLI性能，直接把AI嵌入Slack，嵌入团队的日常沟通流。你OpenAI抢的是开发者的终端，我Anthropic抢的是整个团队的工作入口。

两条路。

OpenAI的逻辑是，工具更好更便宜更易迁移，开发者自然会来。

Anthropic的逻辑是，AI不应该只是开发者的工具，应该是团队的成员，融入协作流程本身就是护城河。
![图片](/images/bfcdbf71ba68fbd8.jpeg)
* * *

## 五、开发者该选谁

说点实在的。

**如果你是个人开发者，重度代码库，复杂重构，预算不是第一考量**，Claude Code+Fable 5仍然是能力天花板。SWE-Bench Pro 80.3%是实打实的。但账单可能到三四百美金一个月。

**如果你追求性价比，做CI/CD集成，做日常CRUD**，Codex+GPT-5.5是更务实的选择。便宜一半，速度更快，现在还能一键迁移。2个月免费等于白嫖。

**如果你是团队负责人，想让AI融入团队协作流**，Claude Tag值得关注。65%代码由AI生成这件事，已经不是实验阶段了。

但说实话，这场仗的赢家不是OpenAI也不是Anthropic。

**是开发者。**

两家拼命降价、提速、做迁移工具、做团队协作。谁赢谁输不重要，重要的是你用上了更好的工具，花了更少的钱。
![图片](/images/ae7b444224e8d2d2.jpeg)

* * *

**AI编程工具的战争，才刚刚开始。**