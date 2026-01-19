# Implement Layer (Infrastructure)

**职责**: 实现 Adapter 层定义的接口，封装具体的第三方库或平台能力。

**包含内容**:
- 第三方 SDK 的 Wrapper。
- Flutter Plugin 的具体调用。

**示例**:
- `CrashlyticsLogImpl` (implements LogPort)
- `HiveStorageImpl` (implements StoragePort)
