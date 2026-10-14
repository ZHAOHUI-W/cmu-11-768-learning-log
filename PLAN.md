# 按课程顺序学习 CMU 11-768

更新日期：2026-10-14

按课程公布的讲次顺序学习，每讲都完成课程材料、理解检查和对应练习。已学习过 CS336 的内容仍按本课程的讲法学习，用已有基础帮助理解。前三周是集中学习阶段，后续讲次与课程项目继续保留在计划中。

此前的智能体循环与上下文问答记为预习。目前第 1 讲学习中，已推进至第 16 页的运行轨迹，完整讲次、录播和指定阅读的完成验收仍待记录。

## 每讲的完成标准

1. 看本讲录播并阅读完整讲义；材料尚未发布时，记录缺项并在发布后补齐。
2. 完成本讲官方指定阅读，整理核心方法、假设和局限；补充参考按课程说明处理。
3. 用自己的话解释本讲概念，完成理解检查；涉及算法时给出推导或伪代码。
4. 完成对应练习，并记录实际结果、错误和下一步。

只有这些内容均有记录后才标为完成。作业按官方说明逐部分推进；需要计算资源的实验标为“待运行”，继续保留。

## 完整讲次清单

以下顺序依据[课程日程](https://www.cmu-agents.com/#schedule)，后续官网调整时同步更新。

| 讲次 | 主题 | 状态 |
| --- | --- | --- |
| 1 | Course Overview: What Is an Agent? · 课程概览与智能体定义 | 学习中：第 16 页运行轨迹，整讲待验收 |
| 2 | Tool Use · 工具调用 | 待完成整讲 |
| 3 | Context Management for Long-Context Agents · 上下文管理 | 待完成整讲 |
| 4 | Skills and Memory · 技能与记忆 | 待学习 |
| 5 | Planning, Task Decomposition, and Multi-Agent Coordination · 规划、任务分解与协调 | 待学习 |
| 6 | Coding Agents · 编程智能体 | 待学习 |
| 7 | GUI / Computer Use Agents · 界面与计算机操作智能体 | 待学习 |
| 8 | Supervised Fine-Tuning · 监督微调 | 待学习 |
| 9 | Reinforcement Learning Basics · 强化学习基础 | 待学习 |
| 10 | Deep Research Agents · 深度研究智能体 | 待学习 |
| 11 | Advanced RL Algorithms · 进阶强化学习算法 | 待学习 |
| 12 | RL Systems · 强化学习系统 | 待学习 |
| 13 | Sandboxing and Credential Management · 沙箱与凭证管理 | 待学习 |
| 14 | OpenHands | 待学习 |
| 15 | LangGraph | 待学习 |
| 16 | Observability and Monitoring · 运行观测与监测 | 待学习 |
| 17 | Agents and the Future of Work · 智能体与工作的未来 | 待学习 |
| 18 | Multi-Agent Interaction · 多智能体交互 | 待学习 |
| 19 | Human-Agent Interaction · 人与智能体交互 | 待学习 |
| 20 | Reranking and Critic Models · 重排序与评价模型 | 待学习 |
| 21 | Tree Search · 树搜索 | 待学习 |
| 22 | Guest Lecture · Karthik Narasimhan | 待学习 |
| 23 | Guest Lecture · Sasha Rush | 待学习 |

课程研究项目、项目讨论和最终展示在上述学习过程中持续推进，保留选题、实验、报告与展示的完整记录。

## 三周集中学习阶段（10/13–11/02）

预计每周投入 30–36 小时。下表是目标进度，依据每讲完成情况调整日期；未完成内容顺延。

| 时间 | 按顺序推进的内容 | 阶段检查 |
| --- | --- | --- |
| 10/13–10/19 | 第 1–6 讲；学习作业 1 的说明与全部部分，开始实现 | 第 1–6 讲均有材料、阅读和理解记录；作业 1 有逐部分进度 |
| 10/20–10/26 | 继续完成作业 1；第 7–10 讲；推进作业 2 | 记录编程、界面、SFT、RL 基础与研究智能体的学习结果；作业 2 有基线与错误分析 |
| 10/27–11/02 | 继续完成作业 2；第 11–16 讲；推进作业 3 | 完成 RL 算法与系统的理解检查；记录训练实现及实际运行进度 |

第 17–23 讲随后按顺序继续，结合材料发布时间推进。三周阶段结束时复盘真实进度并更新后续日期。

## 作业完整清单

### 作业 1：Build an Agent Harness

- [ ] 环境配置、作业规则与公开测试。
- [ ] Part 1：构建提示、ReAct 循环、执行工具、加载技能，修复并验证棋类应用。
- [ ] Part 2：实现上下文压缩并运行对应任务。
- [ ] Part 3：构建 ChessAgent；完成 play_move、观察 A/B 实验、simulate_move、run_python 与棋类技能。
- [ ] 整理运行轨迹、结果和作业要求的报告材料。

### 作业 2：Evaluating a Data-Visualization Agent

- [ ] 环境配置、评估格式和四类错误标准。
- [ ] Part 1：检查初始智能体运行，分析基线评估器。
- [ ] Part 2：改进评估器并比较结果。
- [ ] Part 3：设计新任务、运行与人工标注，按说明打包任务。
- [ ] Part 4：迭代设计，整理报告和结果。

### 作业 3：Training Agents with Reinforcement Learning

- [ ] Part 0：Warmup。
- [ ] Part 1：轨迹数据处理、loss mask 与优势值计算。
- [ ] Part 2：同步 REINFORCE 与 GRPO。
- [ ] Part 3：异步 GRPO。
- [ ] Part 4：Number Search 对照实验，包括组大小、同步/异步与重要性加权。
- [ ] Part 5：TextCraft-Synth 训练与评估。
- [ ] 整理诊断图、实验报告和复现材料。

以上清单来自各作业当前公开说明，具体要求以官方文件为准。

## 课程入口

- [课程官网与课表](https://www.cmu-agents.com/)
- [官方录播列表](https://www.youtube.com/playlist?list=PLSN0qpDfUvTM)
- [作业 1](https://github.com/cmu-agents/assignment-1)
- [作业 2](https://github.com/cmu-agents/assignment-2)
- [作业 3](https://github.com/cmu-agents/assignment-3)
