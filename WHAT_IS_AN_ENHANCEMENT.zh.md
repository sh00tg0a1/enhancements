# 什么是 Enhancement？

本文提炼自 Kubernetes 上游指南 [kubernetes/enhancements/README.md](https://github.com/kubernetes/enhancements/blob/master/README.md)，概括 Enhancement 的定义与判定要点。

## 何时应视为 Enhancement

- 值得在发布时写博客介绍，用户可见且会依赖。
- 需要多个 SIG/负责人协作，具备跨领域影响。
- 会经历阶段演进（Alpha → Beta → Stable）。
- 范围较大（如组件重构、API 变更、多周工程量）。
- 对用户体验/运维有明显影响，可能需要用户学习。

## 通常不属于 Enhancement

- 仅通过 CRD 就能实现。
- 解决单个 flaky 测试、重构、或纯性能小优化。
- 小幅错误信息或事件补充。

## 流程提示（源自 Kubernetes）

- 想法获得共识后创建 Enhancement Issue，通常跨多个版本推进。
- 使用标签明确归属与阶段（如 `sig/*`、`kind/feature`、`stage/{alpha,beta,stable}`）。
- 通过看板/表格追踪状态；设计细节放在关联的 Issue/PR 中讨论。

更多细节参见上游文档：[kubernetes/enhancements/README.md](https://github.com/kubernetes/enhancements/blob/master/README.md)。

