# ReAct · 集中阅读问题

第 1 讲指定阅读的第二项；接在 Toolformer 之后。

原文：[ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)。按整篇集中作答、统一反馈；无需背具体实验分数。完整论文与附录继续保留在阅读范围。

## 阅读主线

Thought 整理上下文并选择行动；Action 与环境交互；Observation 提供新证据，支持后续推理与计划调整。语言推理本身不产生新的环境观察。论文中知识任务采用较密集的推理，交互任务允许稀疏的思考，不能把 ReAct 简化为所有任务都必须严格三步循环。

## 五道综合题

1. **信息流与方法**：Thought、Action、Observation 分别由谁产生，改变什么？ReAct 与 CoT、Act-only 的信息流有何区别？为何密集和稀疏的 Thought 都可以属于 ReAct？（第 2–4 页）
2. **工具接口与恢复**：Search、Lookup、Finish 各负责什么？举一段两跳问答的调用轨迹，说明搜索失败后怎样利用返回信息调整下一步。（第 4、6 页）
3. **实验任务与指标**：HotpotQA、FEVER、ALFWorld、WebShop 分别要求完成什么任务、与什么环境交互、使用什么评价指标？这些任务怎样检验“行动帮助推理”和“推理帮助行动”？（第 4–8 页）
4. **对照与失败分析**：ReAct 是否在所有任务上都优于 CoT？结合对照与失败案例，说明 CoT、Act-only 和 ReAct 的优势与局限，以及论文为什么把 ReAct 与 CoT-SC 结合。（第 5–8 页）
5. **提示与训练的区别**：主体 few-shot prompting 实验是否更新参数，演示来自哪里？初步 finetuning 用的轨迹又来自哪里？再列出两项尚未解决的问题。（第 3–9、15 页）

## 状态

题组与阅读主线已准备，尚未收到本篇作答或完整阅读确认。实验中某些比较包含特定提示选择与设置，分析结论时需保留条件，不概括为全面优于其他方法。
