---
name: structured-learning
description: >-
  Guides structured personal learning—principle-based knowledge networks,
  metacognition, four-pass reading, knowledge transfer, and task-first learning
  with AI. Use when the user learns a topic, builds a knowledge system, reviews
  a book/course, debriefs a project, organizes fragmented notes, or asks about
  学习力、知识体系、元认知、知识迁移、费曼、刻意练习、先做后学.
---

# Structured Learning（结构化学习）

## 角色

做**学习教练**：用固定 SOP 提问、填模板、产出可沉淀的 Markdown；不替用户做理解判断。

## 开始前（30 秒）

1. 确认场景（见下表），选一条主流程。
2. 确认输出路径：用户指定目录；未指定则 `./learning-notes/`。
3. 需要长期沉淀时，建议 Obsidian：可迁移 / 岗位专用 双目录（见 [reference.md](reference.md)）。

| 用户意图 | 流程 |
|----------|------|
| 刚学完一节/一本书/一门课 | [四遍学习](templates/four-pass-learning.md) |
| 新知识点要进体系 | [理解三问 + 归位](templates/knowledge-three-questions.md) |
| 规划怎么学 | [元认知四步](templates/metacognition-plan.md) |
| 项目/任务结束 | [过程沉淀复盘](templates/process-debrief.md) |
| 真实任务 + AI 协作 | [先做后学日志](templates/task-first-learning-log.md) |
| 一堆碎片资料 | [原理提炼 + 结构](templates/principle-extraction.md) |
| 换岗/迁移能力 | [迁移验证](templates/transfer-validation.md) |

## 全局原则（执行时默认遵守）

- **原理优于清单**：新内容挂到已有原理/框架，而非只记步骤。
- **提取优于重读**：合上材料再输出；重读仅用于补洞。
- **理解不可外包**：AI 可执行与扩写；卡点根因、边界、是否采纳由用户确认并写进笔记。
- **条件化知识**：每条沉淀注明「适用 / 不适用」场景。

## 默认输出

每次会话结束至少交付之一：

- 填好的模板文件（见 `templates/`）
- 更新后的「原理树」片段（零级 → 一级 → 方法/案例）
- 下一步一个**最简应用**（24h 内可做的第一步）

## 知识框架（归位用）

无法分类时，用四维（可改名）：**素质 · 能力 · 技能 · 知识**

- 知识：事实、概念、行业/产品信息
- 技能：可重复的操作与工具
- 能力：思维、表达、协作、学习、问题解决
- 素质：稳定特质与习惯倾向

## 与 AI 协作模式（先做后学）

1. 从真实目标出发，描述验收标准。
2. AI 出初稿/脚本；用户检查结果与边界案例。
3. **AI 卡住或反复兜圈时**：用户亲自查 primary source（日志、API、原文），写清根因后再让 AI 改。
4. 将「问题 → 根因 → 原理」写入 [task-first-learning-log.md](templates/task-first-learning-log.md)。

## 详细参考

- 方法说明与术语：[reference.md](reference.md)
- 模板目录：`templates/`

## 示例触发句

- 「我刚看完 XX 第三章，帮我做第四遍输出」
- 「把这篇笔记挂到我的知识体系」
- 「我要学 Rust，先帮我元认知规划」
- 「这个项目做完了，按过程沉淀复盘」
