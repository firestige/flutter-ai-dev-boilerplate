# 开发规范 (Guidelines)

## 1. AI 协作流程
- **读取入口**：每次会话开始时，请优先参考 `docs/index.md`。
- **更新文档**：代码变更必须同步更新相关文档（如 `design/` 或 `todo.md`）。不要只改代码不改文档。
- **任务确认**：在执行复杂任务前，先简述你的计划。

## 2. 设计规范 (Design)
- **体验优先**：移动端优先，交互遵循 iOS Human Interface Guidelines 和 Material Design 3。
- **Design Tokens**：严禁硬编码颜色值或字号。必须建立统一的 Theme/Token 系统管理颜色和排版，避免散乱取值。
- **组件化**：优先复用通用组件与样式，保持 UI 一致性。

## 3. 代码规范 (Flutter/Dart)
- **静态分析**：全局启用 `analysis_options.yaml`，确保空安全 (NNBD)。
- **命名约定**：
    - 变量/方法/参数：`lowerCamelCase`
    - 类/Extension/Enum：`UpperCamelCase`
    - 常量：`SCREAMING_SNAKE_CASE`
- **目录结构**：采用 Feature-First 分层。
    - 各个功能模块独立分包。
    - 公共基础能力放入 `core/` 目录。
- **资源管理**：图片、字体等资源统一存放在 `assets/`，并通过生成的常量类（如 `AppAssets`）集中引用，严禁手写字符串路径。
- **路由管理**：使用集中式路由表定义，必须支持 Deep Link。
- **最佳实践**：
    - 保持 Widget 拆分，避免单个文件过大 (>300行)。
    - 遵循官方 Linting 规则。

## 4. 提交与评审 (Commit & Review)
- **提交信息**：遵循 `type(scope): summary` 格式。详见 [commit_message.md](template/commit_message.md)。
- **Pull Request (PR)**：
    - 必须包含自测说明。
    - 涉及 UI 变更必须附带截图。
    - 尽量附带测试或测试计划。

## 5. 分支管理与合并 (Branching & Merge)
### 分支命名
- **特性开发**：`feat/<feature-name>` (例如 `feat/search_module`)
- **重构**：`refactor/<scope>`
- **修复**：`fix/<issue-id>` 或 `fix/<description>` (例如 `fix/login_crash`)

### 开发流程
1. 从 `main` 创建特性分支。
2. 在分支上进行开发，遵循小步提交。
3. 完成后更新相关文档（`todo.md`, `changelog/history.md`）。
4. 执行合并前检查。

### 合并前检查清单 (Checklist)
- [ ] **AI Code Review**: 提交前必须要求 AI (Codex) 进行代码审查。
    - **架构违约**: 零容忍。检查是否存在跨层/反向依赖违反 `docs/design/architecture.md`。必须整改。
    - **代码风险**: 检查潜在 Bug 或性能风险。由作者决定是否修复。
- [ ] `flutter analyze` 无 error。
- [ ] 所有验收标准已满足。
- [ ] `docs/changelog/history.md` 已记录变更。
- [ ] `docs/todo.md` 任务状态已更新。
- [ ] `docs/features.md` 特性列表已更新（如涉及新特性）。
- [ ] 无未提交的变更。

### 合并步骤 (Merge)
```bash
# 1. 切换到 main 并拉取最新
git checkout main
git pull origin main

# 2. 合并特性分支（使用 --no-ff 保留分支历史）
git merge <branch-name> --no-ff -m "Merge branch '<branch-name>'"

# 3. 推送
git push origin main

# 4. 清理本地分支（可选）
git branch -d <branch-name>
```

## 6. 文档维护 (Documentation)
所有文档应遵循标准模板：
- **设计文档**：[template/design_doc.md](template/design_doc.md)（用于系统设计）
- **任务清单**：[template/todo.md](template/todo.md)（用于规划）
- **任务记录**：[template/task.md](template/task.md)（用于记录复杂任务的执行细节，存于 `docs/task/`）
- **变更日志**：[template/changelog.md](template/changelog.md)（用于版本发布）
- **架构决策**：[template/adr.md](template/adr.md)（用于重大决策）

## 7. 测试 (Testing)
- **单元/组件测试**：运行 `flutter test`。
- **覆盖范围**：尽量为核心逻辑与适配层编写测试。

## 8. 性能与质量 (Performance & Quality)
- **渲染性能**：避免无界重绘与重复构建，尽可能使用 `const Widget`。
- **包体积**：关注资源文件大小，删除未使用的资源。
- **安全**：日志分级，release 模式下禁止输出敏感信息。
