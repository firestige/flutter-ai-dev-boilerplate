# 架构/设计文档模板

## 元数据
- **作者**: [Name]
- **状态**: [Draft/Proposed/Accepted/Deprecated]
- **创建日期**: YYYY-MM-DD
- **最后更新**: YYYY-MM-DD

## 1. 背景与问题 (Context & Problem)
> 描述当前面临的问题、背景信息以及为什么要进行这次设计变更。

## 2. 目标 (Goals)
> 列出本次设计的核心目标和非目标（Non-goals）。
- [ ] 目标 1
- [ ] 目标 2

## 3. 方案概述 (Solution Overview)
> 简要描述解决方案的核心思路。

### 3.1 核心组件/模块
- **组件 A**: 职责描述...
- **组件 B**: 职责描述...

### 3.2 交互流程 (Interaction/Flow)
> 可以用时序图或文字描述模块间的交互。

## 4. 详细设计 (Detailed Design)
> 深入技术细节，如 API 定义、数据结构、算法等。

### 4.1 数据模型 (Data Model)
```dart
class ExampleModel {
  // ...
}
```

### 4.2 接口设计 (API Design)
- `Method A()`: ...

## 5. 决策记录 (Decision Records / Alternatives)
> 记录主要的技术决策点，以及被否决的替代方案 (Alternatives)。

- **决策点 1**: 选择了方案 A。
    - *原因*: ...
    - *替代方案 B*: 因为...被否决。

## 6. 其它考虑 (Concerns)
- **性能**: ...
- **安全**: ...
- **兼容性**: ...
