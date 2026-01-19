# Task-XXX: {任务标题}

<!-- 
Task 文档用于记录具体开发任务的详细执行过程。
并非所有 Todo 都需要 Task 文档，通常用于：
1. 涉及多个模块修改的复杂功能 (建议关联 Design Doc)
2. 需要记录详细验证过程的任务
3. 跨度较大的重构 (建议关联 ADR)
-->

## 元数据
- **ID**: Task-XXX (建议与 Issue ID 或 Todo 编号一致)
- **类型**: [Feature | Refactor | Fix | Chore]
- **关联**: [Todo 链接](../todo.md) | [PR 链接](...)
- **设计**: [ADR-XXX](../design/adr/...) | [Design Doc](../design/...) (若涉及架构/特性变更则必填)
- **负责人**: {Name}
- **日期**: YYYY-MM-DD
- **状态**: [Done]

## 1. 任务目标 (Objective)
> 简述本次任务的具体目标和交付物。

## 2. 实现细节 (Implementation)
> 记录关键的修改点。
- **模块 A**: 修改了...
- **模块 B**: 新增了...

## 3. 验证结果 (Verification)
> 记录自测结果和截图。
- [x] 单元测试通过
- [x] UI 还原度检查 (附截图)

## 4. 后续跟进 (Follow-up)
- [ ] 遗留问题...
