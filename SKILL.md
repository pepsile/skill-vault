---
name: go-mode
description: Use when the user wants a go-mode entrypoint for a coding task, gives a goal to execute, or needs one place to turn a target into phased implementation work.
---

# Go Mode

把这个 skill 当成“总入口”。它负责接收目标、拆分阶段，并把后续工作路由到合适的 Superpowers 流程里。顶层始终只盯一个目标。

## Operating Rules

- 先用一句话把目标锁死，再开始别的动作。
- 目标不清楚，或者有隐藏约束，就只问最少的问题，把阻塞点问开。
- 只有当每个 phase 都有明确验收点时，才拆 phase。
- 优先拆成小而能收尾的阶段，不要把一个大计划硬推到底。
- 一次运行里不要混进无关目标。

## Route To Superpowers

- 还没有计划，或者需求还不清楚：用 `superpowers:brainstorming`
- 需要一份多步骤书面计划：用 `superpowers:writing-plans`
- 已经有计划，希望在当前会话里执行：用 `superpowers:subagent-driven-development`
- 已经有计划，希望在独立会话里执行：用 `superpowers:executing-plans`
- 每个实现任务内部：用 `superpowers:test-driven-development`
- 某个任务已经变绿以后：先 simplify / refactor，再进入下一个任务
- 工作结束时：用 `superpowers:finishing-a-development-branch`

## Default Loop

目标 -> phase -> 测试 -> 实现 -> review -> simplify -> 验证 -> commit -> 下一个 phase

## Guardrails

- 除非用户明确改目标，否则保持目标稳定。
- 变绿以后不能跳过 simplify / refactor。
- 当前 phase 没验证完，不要进下一个 phase。
- 如果某个 phase 变得太大，就先拆开，再实现，不要硬推。
