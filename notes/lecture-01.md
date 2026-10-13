# 第 1 讲：What Are Agents? And How Do They Work?

状态：学习中。完整录播、讲义、指定阅读与理解检查均保留在完成要求中。

## 官方材料

- [讲义](https://www.cmu-agents.com/slides/lecture-01-agents.pdf)
- [录播](https://www.youtube.com/watch?v=UwfjzyLnvMg)
- [Toolformer](https://arxiv.org/abs/2302.04761)
- [ReAct](https://arxiv.org/abs/2210.03629)
- [Mini-SWE-Agent](https://github.com/swe-agent/mini-swe-agent)

## 开场讨论：能力与行动边界

讲义开场展示复杂任务的执行能力，并讨论不同任务应允许怎样的自主行动。评价智能体需要考虑任务完成能力、结果的可靠性、授权范围和行动后果。

理解练习：用户要求修复网站结账失败，智能体修改代码后本地测试全部通过。部署前还需要确认什么？

我的初始回答：“检查失败原因，修复方法。”

补充反馈：这两项有助于判断修复是否针对根因；上线还需要确认部署授权，以及线上环境、测试覆盖和回滚条件。本地测试通过并不能单独决定是否可部署。

## 待继续

按讲义顺序推进智能体定义、语言模型与工具、行动循环、能力与训练、工程组成，以及课程学习要求。观察、环境状态、动作和奖励的理解检查尚待进行。
