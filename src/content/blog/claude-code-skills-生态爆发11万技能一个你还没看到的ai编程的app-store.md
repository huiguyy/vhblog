---
title: "Claude Code Skills 生态爆发：11万技能，一个你还没看到的「AI编程的App Store」"
id: claude-code-skills-生态爆发11万技能一个你还没看到的ai编程的app-store
date: 2026-07-13T00:16:26.453Z
categories: AI热点
tags:
  - AI
  - Claude
  - Anthropic
  - Gemini
  - Cursor
  - GitHub
cover: "https://raphael.18.do/images/1696c281-7554-462d-afd6-537dce68128c.jpg"
---

# Claude Code Skills 生态爆发：11万技能，一个你还没看到的「AI编程的App Store」
![cover_封面](/images/bef0b612-6863-44ab-bde7-672c5204f194.png)


* * *

## 一、SkillHub 上已经有 11.3 万个技能

2026年7月11日，SkillHub（skillhub.club）收录的技能数突破了 11.3 万。ClawHub 收录了 13,700+ 个，官方 Marketplace 658 个。GitHub 上社区贡献的 Claude Code Skills 超过 1400 个。

**Superpowers**（obra/superpowers，21.3 万星）是星数最高的项目。不是某个单独的 Skill，而是一整套 Agent 工程技能框架：自动规划、子代理调度、TDD 强制化、代码审查。安装一条命令，开发者不用再反复写「先跑测试再提交」「按照这个规范写代码」之类的指令。

**NousResearch/hermes-agent**（15.5 万星）稳坐第二。**mattpocock/skills** 一个月新增 7.25 万星。

三个数据放在一起看，结论很清晰：Claude Code Skills 生态，在 2026 年中，进入了爆发期。
![illust_01_11万技能爆发](/images/d10138b8-2ef7-4211-b170-295b27ae4ef5.png)


* * *

## 二、从「手写 Prompt」到「安装 Skill」

Claude Code 在 2026 年 1 月发布 2.1.0 版本，把 Skills 升级成了「一等公民」。核心的突破有三个。

**热重载**。修改 `~/.claude/skills/` 目录下的 Skill 文件，立即生效，不用重启会话。调试一个 Skill 从原来的 10 秒重启变成了 0.1 秒热加载。100 倍的迭代效率提升。

**生命周期钩子**。Agent、Skill、Slash Command 全覆盖。Skill 可以在分叉的子 Agent 上下文中运行（context fork），互不干扰。

**渐进式披露**。每个 Skill 启动时只占 30-50 个 token 的元数据（名字+描述），任务匹配到了才加载完整指令。装 30 个 Skill，实际占用的上下文不到 1500 token。不会因为装多了而撑爆窗口。

这三个特性，让 Skills 从「能用的工具」变成了「生态的底座」。
![illust_02_三个核心突破](/images/9cc144f9-e3a6-4ef3-b3b1-02b96eaf0d50.png)


* * *

## 三、Skill 生态的 App Store 时刻

2026 年 5 月到 7 月，Skill 生态从「萌芽」进入「爆发」。

SkillHub 的社区数据可以说明问题。\*\*安全审核通过率 87%**，说明不是垃圾堆——大多数技能是有质量的。**周活跃开发者 5000+**，说明有人在持续用、持续维护。**最高单项安装量 18 万+\*\*，说明有头部项目形成了品牌效应。

跨平台兼容也在加速。Claude Code Skills 的格式已经可以被 **13 款 AI 编程工具**原生使用——Cursor、Windsurf、OpenCode、Gemini CLI、Antigravity、Aider 都在兼容列表里。装一个 Skill，在 Claude Code 里写的前端设计规范，切到 Cursor 一样生效。

ClawHub 被开发者叫做「AI Agent 的 npm」，支持向量语义搜索（用自然语言找技能）、语义版本控制（Semver）、社区评分和举报机制。一条命令安装：`npx clawhub@latest install`。

回头看，这和 iOS 的 App Store 早期非常像。2010 年，App Store 上有 25 万个 App，开发者们刚刚学会「原来手机软件可以专门做一件事」。2026 年，Skill 生态站在同样的十字路口。11.3 万个技能，覆盖前端设计、数据科学、DevOps、安全审计、文档生成。每个 Skill 就是一套经过验证的最佳实践，装上去就能用。
![illust_03_App Store时刻](/images/dd0e8149-7f3a-4763-8910-49f7f2729ac7.png)


* * *

## 四、真正在用的，不超过 10 个

有一个 CSDN 文章讲得很实在。作者装了 31 个 Skill，一个月后只保留了 8 个。不是其他 23 个不好，而是不常用。

**每个 Skill 的描述会出现在每一轮的上下文里**。虽然渐进式披露只占 30-50 token，但装到 30 个的时候，光元数据就是 1500 token。Anthropic 官方手册的建议是 8 到 12 个 Skill，超过这个数，每一轮对话都在交「上下文税」。

这里有一个很重要的认知：**Skill 的价值不在于数量，在于筛选**。

作者留下的 8 个 Skill 里，6 个是官方的，2 个是社区构建的。筛选标准不是「这个 Skill 看起来有用」，而是「过去一周我有没有用过它」。如果没用过，就删掉。

这和 iOS 用户删 App 的逻辑一样。装的时候觉得「总有一天用得上」，实际上再也没打开过。Skill 也是。
![illust_04_从11万到8个](/images/3d6bf13b-06a1-4c47-835e-37849c63cbcc.png)


* * *

## 五、Skill 生态意味着什么

**第一，AI 编程的能力边际在从「模型」向「生态」转移。**

2025 年，开发者关心的是「哪个模型编程最强」。2026 年，开发者关心的是「哪个生态的技能最全」。模型会迭代，但 Skills 是经验的沉淀。Superpowers 的 21.3 万星，不是模型的能力，是社区共识。

**第二，Skill 正在成为 AI 编程的「标准化知识载体」。**

一个 Skill 就是一个 SKILL.md 文件。YAML 元数据做路由，Markdown 正文写指令。没有复杂的编译过程，没有二进制依赖。写一个 Skill，跨 13 个平台生效。这种低门槛 + 跨平台的设计，是生态爆发的关键。

**第三，筛选能力正在成为核心技能。**

当 11.3 万个技能摆在你面前的时候，装什么、留什么、删什么，比怎么用更重要。能管好 8 个 Skill 的开发者，比装 30 个的开发者更高效。这是 Skill 生态带来的新认知——**AI 编程的效率瓶颈，已经从「模型能力」变成了「工具管理能力」**。
![illust_05_能力重心转移](/images/e57e2254-8a43-42dd-95f8-9cb2d69a87db.png)


2026 年 7 月的 SkillHub 上，11.3 万个技能等着被安装。但真正能留下来的，永远是那 8 个。

#ClaudeCode #AI编程 #Skill生态 #Superpowers #AppStore时刻 #开发者工具 #AgentEngineering