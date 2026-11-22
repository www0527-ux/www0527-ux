<div align="center">

# 未明廖

**Go Backend & AI Agent Engineer**

用 Go 构建高可靠的分布式后端系统，用可观测性与工程化方法落地 AI Agent 应用。

<p>
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" />
  <img src="https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" />
  <img src="https://img.shields.io/badge/Jaeger-60D0E4?style=flat-square&logo=jaeger&logoColor=black" />
</p>

[wzm.star@gmail.com](mailto:wzm.star@gmail.com) · [Projects](#featured-projects) · [Open Source](#open-source) · [Tech Stack](#tech-stack)

</div>

---

## Quick Tour for Reviewers

如果你正在快速评估我的工程能力，建议直接按以下路径查看核心代码与实测证据（约 3 分钟）：

- **Go 后端高并发与一致性** → [`IM`](https://github.com/www0527-ux/IM)（事务级会话 `Seq` 有序、Kafka 异步推送、缓存一致性与 [36,000 消息压测报告](https://github.com/www0527-ux/IM/blob/main/docs/load-test-report.md)）
- **Go AI Agent 与可观测性排障** → [`Vigil`](https://github.com/www0527-ux/Vigil)（Eino ADK 多信号排障、混合检索、SSE 事件续接与 [故障恢复实测](https://github.com/www0527-ux/Vigil/blob/main/docs/product-demo.md)）
- **开源源码阅读与问题定位** → [`open-im-server#3799`](https://github.com/openimsdk/open-im-server/issues/3799)（分布式一致性 Bug 分析）· [`agilePool#128`](https://github.com/Yiming1997/agilePool/pull/128)（Prometheus 指标 PR）

---

## Featured Projects

### [Vigil](https://github.com/www0527-ux/Vigil) — Observability-Driven AI Troubleshooting Agent

> 基于 **Go + Eino ADK** 的智能排障工作台（原名 Pilot），将 Elasticsearch 日志、Prometheus 指标、Jaeger 调用链与 Markdown 技术指南整合为多轮证据驱动的排障链路，并支持人工审核沉淀排障经验。

<p align="center">
  <img src="https://raw.githubusercontent.com/www0527-ux/Vigil/main/docs/images/demo/04-agent-recovery.png" width="760" alt="Vigil 排障工作台演示" />
</p>

- **跨信号根因调查**：Agent 按需调用日志 / 指标 / Trace 工具，将调查过程与最终结论分离展示；在本地慢下游复现场景中完成 P95 延迟 **`49 ms → 1.74 s → 49 ms`** 全链路诊断与恢复验证。
- **混合检索与章节补全**：Markdown 结构切分 + Elasticsearch BM25 / 向量检索 + RRF 融合与父子章节窗口补全。
- **可控执行与工程规范**：支持 SSE 事件序号续接、请求幂等、原始问答与工作快照事务提交；GitHub Actions CI 持续全绿。

**Stack:** `Go` · `Eino ADK` · `Elasticsearch` · `Prometheus` · `Jaeger` · `MySQL` · `SSE` · [Repository →](https://github.com/www0527-ux/Vigil)

---

### [IM](https://github.com/www0527-ux/IM) — Distributed Real-Time Messaging Backend

> 基于 **Go + go-zero** 的分布式实时通信后端，聚焦高并发下的消息可靠投递、会话内严格有序、离线同步、热点缓存一致性与红包资金事务。

- **可靠投递与会话有序**：MySQL 事务内原子提交消息与独立递增会话 `Seq`，支持分片批量写入；客户端基于 `Seq` 游标实现离线补偿。
- **异步推送与缓存一致性**：Kafka 异步分发在线通知，WebSocket 单写循环串行化帧写入；群成员采用进程内有界缓存 + Redis Pub/Sub 主动失效 + 短 TTL 兜底。
- **资金一致性与压测验证**：红包业务以整数分存储，Redis 候选加速 + MySQL 事务最终裁决；本地单机压测完成 **`300 msg/s · 36,000 条消息 · 零丢消息 · 接收端 P95 102 ms / 238 ms`** 验证。

**Stack:** `Go` · `go-zero` · `MySQL` · `Redis` · `Kafka` · `WebSocket` · `gRPC` · `etcd` · [Repository →](https://github.com/www0527-ux/IM) · [Load Test Report →](https://github.com/www0527-ux/IM/blob/main/docs/load-test-report.md)

---

## Open Source

| Project | Contribution | Summary |
| --- | --- | --- |
| [`openimsdk/open-im-server`](https://github.com/openimsdk/open-im-server/issues/3799) | Bug Report (`#3799`) | 源码级定位 Kafka offset 标记与 MongoDB 写入失败的边界一致性隐患（后续 offset 标记可能跳过未落库消息） |
| [`Yiming1997/agilePool`](https://github.com/Yiming1997/agilePool/pull/128) | Feature PR (`#128`) | 为 Go 高性能协程池新增 Prometheus 文本格式运行指标暴露能力 |

---

## Tech Stack

| Domain | Technologies |
| --- | --- |
| **Backend & Distributed Systems** | Go, go-zero, Gin, gRPC, WebSocket, MySQL, Redis, Kafka, etcd |
| **AI Agent Engineering** | Eino ADK, Tool Calling, Hybrid RAG (BM25 + Vector + RRF), Context & Memory |
| **Observability & Infra** | Prometheus, Jaeger, OpenTelemetry, Elasticsearch, Docker Compose, GitHub Actions |

---

<div align="center">
  <sub>Build reliable systems. Make trade-offs explicit. Verify with real evidence.</sub>
</div>
