# Flutter AI Dev Boilerplate

一个为 AI 辅助开发量身定制的 Flutter 项目脚手架。包含严格的分层架构、文档驱动开发（DDD - Documentation Driven Development）流程以及 AI 友好的上下文管理。

## 核心特性

-   **架构基本法**: 已内置清晰的六层架构设计 (UI, Feature, Core, Data, Adapter, Implement)，无需从零思考代码存放位置。
-   **文档驱动**: 预置了 `docs/` 体系，包含设计文档、架构决策记录 (ADR)、任务日志 (Task Journal) 等标准模版，极大增强 AI 的上下文理解能力。
-   **AI 友好**: 所有文档结构经过优化，便于 AI (Copilot, Windsurf, Cursor) 快速索引和理解项目背景。
-   **开发规范**: 内置 `analysis_options.yaml` 和开发指南，确保代码质量和团队协作一致性。

## 目录结构

```text
lib/
├── app/          # 全局配置 (DI, EventBus, Theme)
├── core/         # 核心业务域 (纯 Dart, 无 Flutter UI 依赖)
├── data/         # 数据层 (Models, Repositories)
├── adapter/      # 接口适配层 (Ports)
├── implement/    # 基础设施实现层 (Infrastructure)
├── features/     # 业务特性层 (Feature-First)
└── ui/           # 纯 UI 层 (Pages, Common Widgets)
```

## 快速开始

1.  Clone 此仓库。
2.  运行 `flutter pub get`。
3.  参考 `docs/guideline.md` 了解开发流程。
4.  开始你的 AI 辅助开发之旅。

## 文档索引

-   [开发指南 (Guideline)](docs/guideline.md)
-   [架构设计 (Architecture)](docs/design/architecture.md)
-   [任务规划 (Todo)](docs/todo.md)
