---
title: "DeepSeek 一条内测帖，引来 120 万星排队「投简历」"
id: deepseek-一条内测帖引来-120-万星排队投简历
date: 2026-08-05T06:43:21.364Z
categories: AI每日热点解析
tags:
  - AI
  - GPT
  - Claude
  - Cursor
  - DeepSeek
  - Llama
cover: "https://raphael.18.do/images/e26384dd-f103-41db-b485-c91157827dec.jpg"
---

# DeepSeek 一条内测帖，引来 120 万星排队「投简历」
![封面_120万星排队投简历](/images/4871890b-aa29-4b14-ad1e-98a18891e719.png)
8月1日，DeepSeek 的 Agent Harness 团队负责人崔添翼发了条内测招募帖。

要求很简单：参与过开源 Agent 项目的建立和维护，提交 GitHub 仓库作为代表作。

三天后，**769 位开发者报名，712 个开源仓库，合计 120 万 Stars**。

评论区秒变「开源 Agent 路演」。

* * *

## 一条帖子，炸出 Agent 开源生态全图

报名项目跨越 18 个赛道，几乎覆盖了当前 Agent 基础设施探索的所有方向。

**智能体框架和编程智能体** 是最大的两个方向，合计 242 个项目，占全部项目约三分之一。Top 10 高星项目里，deer-flow（79k 星）探索长周期 SuperAgent 框架，CodeWhale（40k 星）是 DeepSeek 原生项目发展成的编程智能体框架，orca（36k 星）关注多 Agent 编排。

**记忆与上下文** 相关项目 56 个，累计 194k 星。开发者正在尝试 Git、数据库、知识图谱等不同路线，但 Agent 记忆目前仍没有统一答案。

**研究与评测、安全治理** 各有 24 个项目。有开发者尝试建立跨 Harness 评测体系，有人关注工具调用权限、文件系统隔离和代码执行沙箱。

这条帖子，提前暴露了 Agent 工程化的能力版图。

![插图_01_三条路径长任务记忆安全](/images/bf2e0748-0f3b-471a-b0e2-e5240eb2e6c9.png)


* * *

## Model + Harness = Agent

业内一直有这样一个公式：**Model + Harness = Agent**。

模型负责理解需求、推理和生成方案。Harness 负责把这些能力落到真实环境：调用工具、操作终端、读写文件、管理上下文、处理执行过程中的错误，最终完成一个完整任务闭环。

DeepSeek 已经在内部用 Harness 完成 DeepSeek-V4-Flash 正式版的基准测试。五组基准——Terminal Bench（终端操作）、Cybergym（安全攻防）、Toolathlon（多工具调用）、DSBench-FullStack 和 DSBench-Hard（全栈开发）——本质上都在测试 Agent 是否具备持续执行复杂任务的能力。

社区猜测，DeepSeek 可能会基于 Harness 打造一款对标 Claude Code、Codex 的 AI Coding Agent，具备自主规划、工具调用、代码执行能力，并围绕长周期 Agent 工作流加入 Memory、项目仓库感知等机制。

这些信息尚未得到官方确认，但方向已经清晰：**未来 Coding Agent 的竞争，不只取决于模型能力，也取决于模型之外的工程基础设施。**

* * *
![插图_02_Model加Harness等于Agent](/images/157d5419-dde8-4dc2-8ac8-0bb5ddc4fa41.png)


## 同一天，LlamaFactory 作者开源 PenguinHarness

8月4日，LlamaFactory 作者郑耀威开源了一个新项目——**PenguinHarness**。

这个「企鹅驾驭师」能帮你自动完成 Agent 的构建、评测和持续改进，真正从「手动调优 Agent」迈入「Agent 自我迭代」。

核心数据：

-   **0.2 元从零构建新的 Agent**，耗时仅为 Codex 的一半，成本低至 Codex 的 1/200
    
-   **不到一元钱让 Agent 自己变强**，无需手动微调，准确率从 50% 提高到 90%
    
-   支持 1000 多种模型，无论是 GPT-5.6 还是 DeepSeek V4 都能驾驭
    

PenguinHarness 是全球首个支持多 Agent 自进化的 Harness。原生支持自我进化，主打轻量、开源、易用。

* * *
![插图_03_评论区变开源路演](/images/3848ee20-82d7-465d-bd4b-e2df891d2547.png)


## 三天，两条信号，一个方向

8月1日，DeepSeek 内测招募帖发出。

8月4日，PenguinHarness 开源。

三天，两条信号，指向同一个方向：

**当模型能力越来越强后，竞争焦点转向 Harness（执行层）。**

769 份报名记录里，开发者关注的是三个底层问题：

1.  **长任务执行**：Agent 能不能稳定跑完一个复杂任务，而不是跑到一半失控
    
2.  **上下文和记忆**：Agent 能不能理解一个持续演进的项目，而不是每次从零开始
    
3.  **评测和安全**：Agent 能不能被放心部署到生产环境，而不是变成风险源
    

这三个方向，对应了 Agent 从「能用」走向「好用」的关键迭代路径。
![插图_04_企鹅0.2元造Agent](/images/9cc96248-2f3c-4703-b188-a5aff9578f22.png)


* * *

## 内测名单的意义：找到能提供有效反馈的开发者

DeepSeek 官方尚未公布最终的筛选标准和名单。

但从这份报名统计表来看，真正有价值的，不是寻找「最热门」的项目，而是找到能在产品迭代过程中提供有效反馈的开发者。

**第一类**：能验证模型能力如何转化为执行能力。比如 akashic-agent 的作者以 V4 Flash 高思考强度模式运行 TerminalBench2.1，拿到 70.8% 的成绩，是基于 DeepSeek 模型调优 Agent 运行时并给出实测结果的开发者。

**第二类**：能验证 Harness 能否进入真实应用场景。open-design（83k 星）、lobehub（81k 星）、career-ops（63k 星）等高星项目，都已经拥有一定用户基础，长期面对真实用户和实际工作流。

**第三类**：能提前发现安全风险。有开发者曾挖掘 Codex、Claude Code、Cursor 等产品漏洞，关注权限控制、文件隔离、安全边界问题。

这些来自一线应用的反馈，可能比单纯的测试数据更有价值。

* * *

## 一份提前出现的 Agent 工程路线图

DeepSeek Harness 最终会是什么样，目前还没有答案。

但这场由内测招募引发的开源项目「大摸底」，提前勾勒出了一张 Agent 工程演进的路线图。

有人在解决长任务执行，让 Agent 不会跑到一半失控。有人在探索记忆和上下文管理，让 Agent 能理解一个持续演进的项目。有人在测试安全边界，确保工具调用和代码执行不会成为风险源。

这些项目未必都会进入 DeepSeek 的内测名单，但它们共同回答了一个底层问题：
![插图_05_工程化大战刚开局](/images/b9ce93b2-c383-4bd8-a675-7fb12dde03e6.png)


**当模型具备越来越强的推理能力后，如何让它稳定、长期、可靠地完成真实任务？**

答案不在模型层，在 Harness 层。

Agent 工程化大战，才刚开局。