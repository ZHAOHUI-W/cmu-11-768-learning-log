# 笔记 01：智能体循环、工具职责与上下文

## 1. 为什么权重不变，能力仍可能提高？

工具使模型在任务进行中获取新的环境信息。读文件可以看到真实代码；运行测试可以观察修改后的结果。智能体可以根据观察改变下一步行动，因此一次任务可包含多轮“决策 → 执行 → 观察 → 再决策”。重复测试本身不会修复问题；关键是根据失败信息定位和修改。

## 2. 模型与框架各负责什么？

| 事项 | 主要责任 |
| --- | --- |
| 选择下一步工具及参数 | 模型；框架限制允许使用的工具与参数范围 |
| 真正执行工具、记录结果 | 框架 |
| 工具报错后的下一步策略 | 框架先捕获并呈现错误，模型再决定如何继续 |
| 最多运行多少步 | 框架强制执行 |

一个最小循环需要在**每轮**重新调用模型，并把工具结果加入历史。早期写出的伪代码只调用了一次模型，且循环条件把“已完成”和“继续运行”写反；这会让智能体无法根据新观察调整行动。

```text
history = [task]
for step in range(step_limit):
    answer = model(history, allowed_tools)
    history.add(answer)
    if answer.is_final():
        return answer.final_result
    for call in answer.tool_calls:
        try:
            observation = execute(call)
        except Exception as error:
            observation = safe_error_message(error)
        history.add_tool_result(call.id, observation)
raise StepLimitError
```

实现时还要检查无效工具调用、缺少工具结果、空回复和资源清理；上面的代码只是概念结构。

## 3. 长输出为什么需要渐进式披露？

一次读取整个大文件可能超出上下文窗口，增加调用成本，也可能使相关线索难以定位。更好的工具设计是先显示文件路径、结构和搜索命中，再按需读取带行号的片段，并保留继续展开的能力。

片段阅读的风险是漏掉远处的定义、调用关系或例外条件。因此截取结果必须明确标注，并允许智能体继续搜索或扩大读取范围。

## 下一步

为“保存设置后超时时间没有生效”的代码仓库问题设计三个工具，写明名称、参数和返回值，然后用它们实现一个最小智能体循环。

## 参考

- [课程官网](https://www.cmu-agents.com/)
- [作业 1：Build an Agent Harness](https://github.com/cmu-agents/assignment-1/blob/main/ASSIGNMENT.md)
