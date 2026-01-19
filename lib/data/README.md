# Data Layer

**职责**: 数据的定义与存储实现。

**包含内容**:
- **Models**: 数据传输对象 (DTOs) 或数据库实体。
- **Sources**: 数据源接口实现 (RestApiClient, LocalDatabase)。
- **Repositories**: 仓库的具体实现 (注：仓库接口定义在 Core 层，或者简化场景下直接在此层实现并由 Core 调用)。

**依赖**: 可依赖 Core 层定义的实体。
