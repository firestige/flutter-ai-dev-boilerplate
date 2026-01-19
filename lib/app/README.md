# App Layer

**职责**: 全局应用配置与组装。

**包含内容**:
- `di.dart`: 依赖注入组装 (Dependency Injection)。
- `theme/`: 全局主题定义 (Design Tokens)。
- `events/`: 全局事件定义 (Event Bus)。
- `config/`: 环境变量、全局配置。
- `routes.dart`: 如果不使用特性内路由，可在此定义集中路由。

**注意**: 此层是将所有积木搭建成完整应用的胶水层。
