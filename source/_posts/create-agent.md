---
title: Create Agent
date: 2026-04-23 22:24:08
categories: 大模型
tags:
- LangChain
- Deep Agents
---

1. 代理基础架构：ReAct 循环
概念实现：实现了“推理（Reasoning）+ 行动（Acting）”的闭环，让 AI 能够发现工具、调用工具并根据结果给出回复。
预置接口：掌握了 create_agent（1.0 版本核心抽象）的使用，极大简化了手动构建图节点的复杂度。
2. 工具定义规范 (Tool Specification)
声明式编程：学习了 @tool 装饰器的用法。
语义传递：理解了 Docstring（文档字符串） 和 类型标注 (Type Hints) 的重要性——它们是模型理解如何调用工具的唯一途径。
3. 图的可视化与理解 (Graph Visualization)
节点与边：通过 get_graph().draw_mermaid_png() 观察到了 agent 节点与 tools 节点之间的循环指向，理解了代理运行的“骨架”。
4. 进阶状态管理 (State Management) —— 核心难点
自定义状态 (Custom State)：学会了通过继承 AgentState 定义自己的 CalcState，为代理增加了除对话以外的“业务记忆”（如 ops 日志）。
还原器 (Reducers)：掌握了 Annotated 的用法，通过指定 reduce_list 函数，控制状态字段如何合并新旧数据（追加而非覆盖）。
5. 依赖注入技术 (Injection)
参数屏蔽：学习了 InjectedState 和 InjectedToolCallId 的高级用法。
作用：这些技术能让工具在执行时“偷偷”获取系统内部数据，而不会把这些复杂的程序参数展示给 AI 模型，保持了 Prompt 的简洁。
6. 状态的动态写回 (Command)
多重更新：掌握了 Command 对象。这让一个工具在返回计算结果的同时，能够异步更新状态中的其他自定义字段。
闭环交互：理解了在 Command 中手动构造 ToolMessage 的必要性，以及它与 tool_call_id 的关联。


![](inject_state_diagram.png)