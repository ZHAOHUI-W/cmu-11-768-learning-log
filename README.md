# CMU 11-768 · AI Agents 学习记录

我正在用三周高强度学习 [CMU 11-768: AI Agents](https://www.cmu-agents.com/)。这里记录我实际学过的内容、动手实验、遇到的错误和仍未解决的问题。课程材料和作业归原作者所有；本仓库只收录我的学习记录与原创实现。

## 当前进度

更新日期：2026-10-10

| 主题 | 状态 | 记录 |
| --- | --- | --- |
| 智能体的行动—观察循环 | 概念讨论完成 | [笔记](notes/01-agent-loop-and-context.md) |
| 工具调用与框架职责 | 概念讨论完成 | [笔记](notes/01-agent-loop-and-context.md) |
| 长上下文与渐进式披露 | 概念讨论完成 | [笔记](notes/01-agent-loop-and-context.md) |
| 作业 1：构建智能体框架 | 尚未提交实现 | [官方作业](https://github.com/cmu-agents/assignment-1) |
| 作业 2：设计智能体评估 | 尚未提交实现 | [官方作业](https://github.com/cmu-agents/assignment-2) |
| 作业 3：强化学习训练 | 尚未提交实现 | [官方作业](https://github.com/cmu-agents/assignment-3) |

## 学习路线

详见 [三周计划](PLAN.md)。目前重点是把工具接口、错误处理和上下文管理从概念落实到可运行的智能体，再用评估结果驱动改进。

## 学习日志

- [2026-10-10：建立记录与阶段复盘](journal/2026-10-10.md)

## 更新方式

每次学习结束后新增或更新一篇 `journal/YYYY-MM-DD.md`，并同步：

1. 本次实际学习和实现的内容；
2. 可验证的结果，例如测试、运行轨迹或实验数据；
3. 修正过的认识和仍未解决的问题；
4. `README.md` 中的进度状态。

日志可从[模板](templates/session.md)开始。涉及 API 密钥、个人数据或课程受限材料时，先清理再公开提交。
