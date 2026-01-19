# Flutter AI Dev Boilerplate

[中文](./README.md) | **English**

A Flutter project boilerplate tailored for AI-assisted development. It features a strict layered architecture, Documentation Driven Development (DDD) workflow, and AI-friendly context management.

## Core Features

-   **Architectural Constitution**: Built-in clear 6-layer architecture (UI, Feature, Core, Data, Adapter, Implement), eliminating the need to think about where to put code from scratch.
-   **Documentation Driven**: Pre-configured `docs/` system containing design docs, Architecture Decision Records (ADR), Task Journals, and other standard templates, greatly enhancing AI's understanding of context.
-   **AI Friendly**: All document structures are optimized for AI (Copilot, Windsurf, Cursor) to quickly index and understand the project background.
-   **Development Standards**: Built-in `analysis_options.yaml` and development guidelines to ensure code quality and team collaboration consistency.

## Directory Structure

```text
lib/
├── app/          # Global Configuration (DI, EventBus, Theme)
├── core/         # Core Domain Layer (Pure Dart, No Flutter UI dependency)
├── data/         # Data Layer (Models, Repositories)
├── adapter/      # Adapter Interface Layer (Ports)
├── implement/    # Infrastructure Implementation Layer (Infrastructure)
├── features/     # Feature Layer (Feature-First)
└── ui/           # Pure UI Layer (Pages, Common Widgets)
```

## Quick Start

1.  Clone this repository.
2.  Run `flutter pub get`.
3.  Refer to `docs/guideline.md` to understand the development workflow.
4.  Start your AI-assisted development journey.

## Documentation Index

-   [Development Guideline](docs/guideline.md)
-   [Architecture Design](docs/design/architecture.md)
-   [Task Planning (Todo)](docs/todo.md)
