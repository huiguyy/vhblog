---
title: "AI编程三国杀，今天杀到明面上来了"
id: ai编程三国杀-今天杀到明面上来了
date: 2026-05-20
categories: AI热点
tags:
  - 随笔
cover: "/images/162b9e3145c27d54.png"
---

# AI编程三国杀，今天杀到明面上来了
![图片](/images/5d3a28d0945858af.png)

过去半年，AI编程工具赛道一直暗流涌动。Anthropic的Claude Code拿了半数市场份额，OpenAI的Codex在后面追，Cursor占了编辑器生态。

今天（5月20日），谷歌I/O大会把暗流变成了明战。

Antigravity 2.0发布，定位从"智能体式IDE"升级为"通用智能体优先工作平台"。两天前，Anthropic花了3亿美元收购Stainless，把AI行业最关键的SDK基建收入囊中。再加上Claude Code 54%的编程市场份额，AI编程的三国杀，牌面彻底摊开了。

## 谷歌出牌，Antigravity 2.0正面硬刚

谷歌这次I/O发布了一组开发者工具，核心是Antigravity 2.0桌面应用。

几个关键变化值得细看。

第一，定位升级。从"面向开发者的智能体式IDE"变成"通用智能体优先工作平台"。这不是换了个slogan，是产品逻辑的重构。以前的Antigravity绑定代码仓库，按workspace组织会话。现在改为按project管理，一个项目可以对应多个文件夹，拥有独立的智能体设置和权限边界。

坦率的讲，Antigravity不再把自己局限在"写代码的工具"里，它在做一个管理多个数字智能体的统一中枢。

第二，多智能体并行。开发者可以同时部署多个子智能体，分别处理不同编程任务，还能安排后台自动化例程。这个能力Claude Code目前没有，Claude Code是单Agent模式，虽然强但在多任务并行上天然受限。

第三，定时任务。新增"/schedule"命令，支持一次性任务和周期性调度，智能体按预设时间自动执行。这个功能看似不起眼，实际是把Agent从"被动响应"推向"主动运行"。你睡着的时候，你的Agent还在干活。

第四，Agent Skills生态。Google Cloud AI总监Addy Osmani开源了生产级工程技能库，覆盖定义、规划、构建、验证、审查、发布六个阶段，20个核心skill。Antigravity支持加载这些skill，还能自定义。

第五，云端托管。Managed Agents通过Gemini API，一次请求就能启动一个运行在隔离Linux环境中的软件智能体，关闭后再返回，已编译文件、记忆日志和项目状态都保留。

还有一个细节，谷歌同步推出Antigravity CLI，建议旧版Gemini CLI用户迁移。Google AI Studio移动应用开放预注册，用户可以在手机上整理想法，回到桌面端查看可运行原型，还能通过提示词生成完整Android应用，直接导出到Google Play Console测试轨道。
![图片](/images/9637bef958f62100.png)

坦率的讲，谷歌这波是补课+超车同时进行。补的是之前Antigravity和Claude Code的差距，超的是多智能体编排和移动端链路，这两条线Anthropic和OpenAI都没走到。

## Anthropic的3亿美元暗棋

就在I/O开幕前两天，Anthropic悄悄完成了一笔收购。

5月18日，Anthropic宣布收购Stainless，交易估值超过3亿美元。

Stainless做的事情听起来很枯燥，把API规范文档一键转化为TypeScript、Python、Go、Java、Kotlin等语言的SDK，API变更时自动同步更新代码。

但它的客户名单几乎覆盖了AI行业所有头部玩家，OpenAI、Google、Cloudflare、Replicate、Runway都在用。

也就是说，Anthropic花3亿美元买下了竞争对手共享的核心基础设施。

而且Anthropic明确表示，收购完成后将逐步关闭所有Stainless托管产品，未来工具链只为Anthropic独家所用。现有客户可以保留已生成的SDK，但无法再获得官方更新和支持。

这一手直接切断了竞争对手的捷径。据行业估算，手动维护一套支持5种以上语言的SDK，每年至少需要3名全职工程师，每次API更新需要数周才能完成全语言同步。OpenAI曾长期依赖Stainless生成官方SDK，内部自研尝试因维护成本过高而放弃。现在不得不回归手动维护模式。

更关键的是MCP。Stainless开发了MCP服务器生成工具，能从OpenAPI规范自动生成符合标准的MCP服务器，让AI智能体无需额外开发就能直接调用外部API。MCP是Anthropic在2024年推出的开放标准，被视为大模型与外部工具通信的"USB-C接口"。Stainless加入后，Anthropic在MCP生态上的主导权进一步巩固。

这不是孤立的一步棋。2025年12月，Anthropic收购了JavaScript运行时Bun，解决"AI生成的代码如何高效运行"的问题。现在收购Stainless，锁定SDK生成和MCP工具链，回答"开发者如何快速接入AI能力"的问题。
![图片](/images/ad5abcbaa3e335f6.png)

两笔收购合在一起，Anthropic正在搭建从模型到应用的全链条闭环。

## OpenAI怎么接招

OpenAI目前在AI编程赛道的位置比较微妙。

Menlo Ventures数据显示，Claude Code占编程市场54%的模型份额，Copilot占24%，Codex约占16%。2025年9月Codex使用量约为Claude Code的5%，到2026年1月升至近40%，追赶速度不慢，但差距仍然明显。

OpenAI采取了双线策略。一边组建"冲刺团队"加速产品迭代，另一边奥特曼看中了Windsurf，报价30亿美元想收购，但交易被微软搁置数月，据说7月告吹。

产品层面，Codex有几个动作。CLI用Rust重写，部署在Cerebras WSE-3上跑到1000+token/秒。Codex被集成到ChatGPT手机端，5月15日上线。macOS专属App可以管理多个Agent任务。

但Codex的核心问题是，它的定位和Claude Code越来越不一样。Claude Code是终端里的深度编程伙伴，面向专业开发者，Agent-first设计。Codex更像ChatGPT内置的异步编码Agent，面向所有人，上手门槛低但深度不够。

现在又多了一个Antigravity，定位在多智能体编排和移动端链路上，恰好是Claude Code和Codex都没覆盖的地带。

另外，Stainless被Anthropic拿走之后，OpenAI失去了统一的SDK生成工具，不得不分散精力维护自己的工具链。对于迭代速度越来越快的大模型行业来说，几周的SDK同步延迟可能直接影响市场份额。
![图片](/images/e24c2b55298d28a6.png)

微软封杀Claude Code强推Copilot的策略也值得玩味。The Verge报道，微软E&D团队数千开发者6月30日前须转Copilot CLI。但61%的双用者认为Claude Code更准。强推能不能锁住开发者，目前还是问号。

## 三国杀的牌面

把三家的牌摊开看。

Anthropic，最强模型份额（54%）+最强SDK/MCP基建（Stainless+Bun）+终端深度协作（Claude Code），弱点是多智能体并行和移动端。

谷歌，最强多智能体编排（Antigravity 2.0）+最强移动端链路（Android/Google Play）+最强端侧AI（Gemini Nano几十亿设备），弱点是起步晚，开发者心智份额不够。

OpenAI，最强品牌心智+最强手机端分发（ChatGPT 4亿周活）+最强推理速度（Cerebras 1000+token/s），弱点是SDK基建被切断，深度编程能力不够，Windsurf收购失败。

三家打的是三种不同的仗。Anthropic打的是"深度+基建"之战，让开发者离不开。谷歌打的是"广度+平台"之战，让开发者到处都能用。OpenAI打的是"普及+速度"之战，让所有人都能上手。

我自己的感受是，这场三国杀的胜负手不在"谁的模型更强"，而在"谁能让开发者更快地把东西做出来"。模型能力的差距已经缩小到几个百分点，真正拉开差距的是工具链的完整度和使用体验的流畅度。
![图片](/images/9108db0745836f3f.png)

Anthropic收Stainless这步棋，短期看是3亿美元买了一支工程团队，长期看是切断了对手的基础设施捷径。谷歌Antigravity 2.0的多智能体和移动端能力，短期看是补课，长期看是差异化竞争的切入点。

至于OpenAI，它能接的牌还有不少。ChatGPT的分发能力、微软的企业渠道、Cerebras的推理速度，这些都是硬牌。但Stainless的丢失和Windsurf收购的失败，让它在工具链上出现了明显的缺口。

下一张牌，看OpenAI怎么打。
