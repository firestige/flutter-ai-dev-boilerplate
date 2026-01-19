# UI Layer

**职责**: 纯粹的界面展示。

**原则**:
- **Dumb Widgets**: 尽量只负责渲染，不包含复杂逻辑。
- **Passive View**: 数据来自 Feature 层，事件回调给 Feature 层。

**包含内容**:
- `pages/`: 页面级 Widget。
- `common/`: 跨特性通用的原子组件 (Design System)。
- `router/`: 路由配置。
