30 天 AI Agent 系统化学习计划（面向软件工程师）
学习目标
理解 AI Agent 的核心概念与全貌，包括生态、关键技术与系统架构。

掌握主流 AI Agent 框架（LangChain、LlamaIndex、AutoGen 等）的使用与对比。

能够将 AI Agent 融合到 Java 或多语言的工程体系中（API、微服务、插件架构）。

熟悉部署、监控、性能优化、安全等工程落地问题。

有一个可运行的 AI Agent 项目 Demo。

---

## **30 天 AI Agent 系统化学习计划（面向软件工程师）**

### **学习目标**

1. 理解 AI Agent 的核心概念与全貌，包括生态、关键技术与系统架构。
2. 掌握主流 AI Agent 框架（LangChain、LlamaIndex、AutoGen 等）的使用与对比。
3. 能够将 AI Agent 融合到 Java 或多语言的工程体系中（API、微服务、插件架构）。
4. 熟悉部署、监控、性能优化、安全等工程落地问题。
5. 有一个可运行的 AI Agent 项目 Demo。

---

## **阶段 1：AI Agent 全貌与基础（第 1-5 天）**

目标：建立全景地图，理解关键组件与生态。

| 天数    | 学习内容                                                                                                                                                                                   | 产出                                       |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| Day 1 | **AI Agent 基础概念**<br> - 什么是 AI Agent（与普通 LLM 应用的区别）<br> - Agent 的关键组成：LLM、工具调用（Tool）、记忆（Memory）、规划（Planning）、执行（Execution）<br> - Agent 架构模式（Reactive / Plan-and-Execute / Multi-Agent） | 绘制一张 **AI Agent 架构全景图**                  |
| Day 2 | **AI Agent 技术生态**<br> - LangChain、LlamaIndex、AutoGen、Haystack、Semantic Kernel<br> - 各框架的适用场景、优缺点<br> - Agent 与 RAG（检索增强生成）的关系                                                          | 制作 **框架对比表**                             |
| Day 3 | **软件工程视角的 Agent 系统设计**<br> - 输入/输出契约设计（API Schema）<br> - 状态管理（短期记忆 vs 长期记忆）<br> - 错误恢复与重试机制                                                                                            | 画出一个 **Java 微服务 + AI Agent** 集成示意图       |
| Day 4 | **Prompt Engineering 基础**（面向工程师）<br> - 系统提示词（System Prompt）结构化设计<br> - 模块化 Prompt 模板化<br> - Prompt 调试方法                                                                                | 用 Java 调用 OpenAI API 实现一个可配置 Prompt 的小例子 |
| Day 5 | **Hands-on**：最小化 AI Agent Demo<br> - 使用 LangChain（Python）实现一个简单的工具调用 Agent<br> - 用 Java 通过 HTTP 调用该 Agent                                                                              | 第一个可运行 Agent Demo                        |

---

## **阶段 2：核心能力与单体 Agent 架构（第 6-15 天）**

目标：深入掌握 Agent 的“工具调用、记忆、规划”三大能力。

| 天数        | 学习内容                                                                                                             | 产出                                    |
| --------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| Day 6     | **工具调用（Tool Invocation）原理**<br> - Function Calling（OpenAI/Anthropic）<br> - JSON Schema 输出约束<br> - Java 中的工具注册与调用 | 在 Java 中实现一个 **本地工具注册与调用的 Agent**     |
| Day 7     | **记忆（Memory）机制**<br> - 短期记忆（上下文窗口）<br> - 长期记忆（向量数据库、RAG）<br> - 常见向量数据库（Pinecone、Weaviate、Milvus）                 | 用 Java 集成一个向量数据库，并存储会话历史              |
| Day 8     | **规划（Planning）与任务分解**<br> - 反应式 Agent vs 计划执行型 Agent<br> - 任务分解算法（ReAct、Tree of Thoughts）<br> - 执行链管理            | 实现一个 Java 侧的“多步任务分解 + API 调用”示例       |
| Day 9     | **知识检索增强（RAG）**<br> - RAG 架构（Retriever + Reader）<br> - 文档切分与索引策略<br> - Java 与 LlamaIndex API 集成                  | 搭建一个简单的 RAG 系统                        |
| Day 10    | **Hands-on**：构建一个“文档问答 Agent”                                                                                    | Java + LlamaIndex 实现一个可查询 PDF 的 Agent |
| Day 11-12 | **Agent 调度与控制**<br> - Agent Executor<br> - 工具调用限流与熔断<br> - 调用链追踪                                                 | 在 Java 中实现调用链追踪日志系统                   |
| Day 13-14 | **安全与合规**<br> - Prompt Injection 攻击与防御<br> - 数据脱敏与审计<br> - API 调用安全策略                                            | 对你的 Agent Demo 增加安全过滤                 |
| Day 15    | **阶段小结**：整理“单体 AI Agent”架构文档                                                                                     | 技术文档 + 架构图                            |

---

## **阶段 3：多 Agent 协作与系统落地（第 16-25 天）**

目标：构建多 Agent 协作体系，接近生产级应用。

| 天数        | 学习内容                                                                             | 产出                                  |
| --------- | -------------------------------------------------------------------------------- | ----------------------------------- |
| Day 16    | **多 Agent 协作模式**<br> - 任务分工模式（Manager-Worker、Peer-to-Peer）<br> - 通信协议（消息队列、事件总线） | 绘制多 Agent 协作架构图                     |
| Day 17    | **AutoGen 框架实践**（或 LangGraph）<br> - 定义多个 Agent<br> - 对话协调与中间状态存储                 | 实现一个双 Agent 协作 Demo                 |
| Day 18    | **任务路由与动态分配**<br> - 基于规则/Embedding 的路由<br> - 优先级调度                               | 在 Java 中实现简单任务路由器                   |
| Day 19-20 | **跨系统集成**<br> - AI Agent 与企业系统（ERP/CRM/数据库）集成<br> - REST/gRPC/WebSocket 通信       | 将 Agent 接入一个真实业务 API                |
| Day 21    | **长生命周期 Agent**<br> - 持久化上下文<br> - 定时任务与事件驱动                                     | 实现一个“每日汇报生成 Agent”                  |
| Day 22-23 | **可观测性与运维**<br> - 日志、指标（Prometheus/Grafana）<br> - 健康检查与恢复                        | 给 Agent 系统加上监控面板                    |
| Day 24-25 | **阶段项目**：多 Agent 协作系统                                                            | Java 后端 + Python Agent 编排，完成一个端到端应用 |

---

## **阶段 4：生产化与优化（第 26-30 天）**

目标：掌握性能优化、部署、版本迭代策略。

| 天数     | 学习内容                                                                             | 产出                              |
| ------ | -------------------------------------------------------------------------------- | ------------------------------- |
| Day 26 | **性能优化**<br> - 并行化工具调用<br> - 缓存策略（Prompt Cache、Embedding Cache）<br> - Token 成本优化 | 给项目加缓存                          |
| Day 27 | **部署与环境**<br> - 本地容器化（Docker）<br> - 云部署（K8s、Serverless）                          | 部署到云环境                          |
| Day 28 | **A/B 测试与版本控制**<br> - Prompt 版本化<br> - 功能开关（Feature Flag）                        | 给 Agent 增加版本管理                  |
| Day 29 | **团队协作与代码规范**<br> - 多语言项目管理（Java + Python）<br> - 接口契约与文档自动化                      | 整理 API 文档                       |
| Day 30 | **最终总结与展示**                                                                      | 完成 **AI Agent 项目 Demo + 技术白皮书** |

---

## **学习资料推荐**

* **框架**：

  * LangChain 官方文档 + LangChain4j（Java SDK）
  * LlamaIndex 官方文档
  * AutoGen GitHub
* **书籍**：

  * 《LangChain 实战》
  * 《Designing Bots》
* **视频**：

  * Andrej Karpathy — "State of GPT"
  * LangChain YouTube 官方教程
* **工具**：

  * Postman / Bruno（调 API）
  * DBeaver（调试数据库）
  * Grafana（监控）

