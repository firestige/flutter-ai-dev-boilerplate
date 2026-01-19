# Adapter Layer (Ports)

**职责**: 定义 Core 层所需的外部能力接口 (Interface/Abstract Class)。

**原则**:
- 纯 Dart 抽象类。
- 不包含实现逻辑。
- 让 Core 层依赖此层，实现依赖倒置。

**示例**:
- `LogPort`
- `StoragePort`
- `NavigationPort`
