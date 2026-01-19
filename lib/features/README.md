# Feature Layer

**职责**: 具体的业务功能模块，连接 Core/Data 与 UI。

**结构 (Feature-First)**:
每个特性的文件夹通常包含：
- `providers/`: 状态管理 (Bloc/Riverpod/Provider)。
- `view_models/`: 视图模型。
- `widgets/`: 该特性特有的 UI 组件。

**原则**:
- 处理用户交互。
- 调用 Core 层逻辑。
- 暴露状态供 UI 渲染。
