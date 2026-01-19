# Commit Message 模板

## 格式结构
```text
<type>(<scope>): <subject>

<body>

<footer>
```

## 字段说明

### 1. Header (第一行)
- **type**:
  - `Feat`: 新功能 (Future)
  - `Fix`: 修补 Bug
  - `Docs`: 文档修改
  - `Style`: 代码格式修改 (不影响代码运行的变动)
  - `Refactor`: 重构 (即不是新增功能，也不是修改 bug 的代码变动)
  - `Perf`: 性能优化
  - `Test`: 增加测试
  - `Chore`: 构建过程或辅助工具的变动
- **scope**: (可选) 说明 commit 影响的范围，例如 `auth`, `home`, `core`。
- **subject**: 简短描述，不超过 50 个字符，使用祈使句，结尾不加句号。

### 2. Body (可选)
详细描述更改的原因和内容。每行不超过 72 个字符。

### 3. Footer (可选)
- **Breaking Changes**: 如果有破坏性更新，必须在此说明。
- **Closes Issues**: 关闭的 Issue 编号，如 `Closes #123`。

## 示例
```text
Feat(auth): add google sign-in support

Implement Google Sign-In using firebase_auth package.
Added necessary iOS and Android configurations.

Closes #42
```
