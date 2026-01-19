# Core Layer (Domain)

**职责**: 核心业务逻辑域，纯 Dart 代码。

**原则**:
- 严禁依赖 Flutter UI 库 (dart:ui 除外，但尽量避免)。
- 严禁直接依赖第三方 IO/UI/Platform 库。
- 必须通过 `adapter/` 接口与外部交互。

**包含内容**:
- **Services**: 业务逻辑服务 (e.g., `AuthService`).
- **Entities**: 纯业务实体。
- **UseCases**: (可选) 单一职责的业务操作。
