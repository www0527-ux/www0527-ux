<div align="center">

# 未明廖

**Software Engineering Student · Go Backend · AI Agent Engineering**

用 Go 构建可靠的后端系统，用工程方法探索 AI Agent 应用。

<p>
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" />
  <img src="https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white" />
</p>

[中文](#关于我) · [English](#about-me) · [Projects](#selected-projects)

</div>

---

## 关于我

软件工程专业本科生，主要关注 **Go 后端开发** 与 **AI Agent 应用工程**。

目前的技术兴趣集中在两个方向：

- **Backend Engineering：** 实时通信、消息可靠投递、会话有序、缓存一致性、异步处理与事务设计。
- **AI Agent Engineering：** Agent 工作流、工具调用、RAG、上下文管理，以及面向开发者的智能排障应用。

我喜欢从具体问题出发，理解系统链路与设计取舍，再通过代码和测试验证方案。

## Selected Projects

### [Pilot — AI Troubleshooting Workspace](https://github.com/www0527-ux/pilot-v2)

基于 Go 与 Eino ADK 构建的智能排障工作台，整合日志、指标、调用链与技术知识库，辅助开发者进行多轮故障调查。

- 联合检索 Elasticsearch 日志、Prometheus 指标与 Jaeger 调用链。
- 通过 BM25、向量检索、RRF 融合与重排构建知识检索链路。
- 支持多轮排障、SSE 事件续接与上下文摘要。
- 将排障过程中的 Issue 和证据整理为可审核、可复用的知识。

**Stack:** Go · Eino ADK · Elasticsearch · Prometheus · Jaeger · MySQL

[Repository →](https://github.com/www0527-ux/pilot-v2)

### [IM — Real-time Messaging Backend](https://github.com/www0527-ux/IM)

基于 Go 与 go-zero 实现的实时通信后端，覆盖单聊、群聊、离线同步与红包业务。

- 使用 WebSocket 建立实时连接，以单写模型管理连接写入。
- 通过 MySQL 事务分配会话 Seq 并持久化消息。
- 使用 Kafka 异步分发消息通知，以 Seq 游标完成离线补偿。
- 使用 Redis 优化热点数据与群成员缓存。
- 通过 MySQL 事务与 Redis Lua 实现红包领取流程。

**Stack:** Go · go-zero · MySQL · Redis · Kafka · WebSocket · etcd

[Repository →](https://github.com/www0527-ux/IM)

## Open Source

正在关注 Go 后端与 AI 工程生态，希望从 Issue、测试、文档和 Bug Fix 等具体工作开始，持续参与开源协作。

## Tech Interests

| Area | Topics |
| --- | --- |
| Backend | Go, HTTP, gRPC, WebSocket, MySQL, Redis, Kafka |
| AI Engineering | Agent, Tool Calling, RAG, Eino, Elasticsearch |
| Observability | Prometheus, Jaeger, OpenTelemetry |
| Engineering | Docker, Git, Linux, automated testing |

---

## About Me

I'm an undergraduate software engineering student interested in **Go backend development** and **AI agent engineering**.

My current focus includes:

- **Backend systems:** real-time messaging, reliable delivery, per-conversation ordering, cache consistency, asynchronous processing, and transaction design.
- **AI applications:** agent workflows, tool use, RAG, context management, and AI-assisted troubleshooting.

I enjoy understanding how systems work end to end, making design trade-offs explicit, and validating ideas through implementation and tests.

## Open to Collaboration

I'm interested in contributing to open-source projects in the Go and AI engineering ecosystems, especially backend services, agent workflows, retrieval, testing, and developer tooling.

---

<div align="center">
  <sub>Build useful things. Understand the trade-offs. Keep improving.</sub>
</div>
