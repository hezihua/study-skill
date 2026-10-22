# study-skill

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

面向 Cursor 的 **结构化学习 Agent Skill**（`structured-learning`）。把「原理化知识体系、元认知、四遍学习、过程沉淀、先做后学、知识迁移」收成可执行的 SOP；Agent 按场景选模板，引导提问并生成 Markdown 笔记。

**仓库地址**：<https://github.com/hezihua/study-skill>

---

## 能做什么

| 场景 | 对应模板 / 流程 |
|------|-----------------|
| 规划一门新技能/课程怎么学 | 元认知四步 |
| 读完一节书、一门课 | 四遍学习（认路 → 理解 → 关联 → 提取） |
| 把一条新知识挂进体系 | 理解三问 + 四维归位 |
| 项目或任务结束 | 过程沉淀复盘 |
| 真实任务里用 AI 协作 | 先做后学日志（卡点自己查清根因） |
| 一堆碎片文章/笔记 | 原理提炼 + 知识树 |
| 经验换岗、换领域能不能用 | 迁移验证 |

核心原则：**原理优于清单 · 提取优于重读 · 理解不可外包 · 知识要写清适用边界**。

---

## 安装

Skill 目录名为 **`structured-learning`**，安装后 Cursor Agent 通过 `@structured-learning` 或描述学习相关需求来调用。

### 1. 克隆仓库

```bash
git clone https://github.com/hezihua/study-skill.git
cd study-skill
```

### 2. 复制到 Cursor 技能目录

**Windows（PowerShell / CMD）**

```bash
xcopy /E /I structured-learning "%USERPROFILE%\.cursor\skills\structured-learning"
```

**macOS / Linux**

```bash
cp -R structured-learning ~/.cursor/skills/structured-learning
```

> **注意**：请勿放入 `~/.cursor/skills-cursor/`，该路径为 Cursor 内置技能保留。

### 3.（可选）仅当前项目可用

```bash
mkdir -p .cursor/skills
cp -R structured-learning .cursor/skills/structured-learning
```

---

## 怎么用

在 Cursor 对话中：

1. 输入 `@structured-learning`，或  
2. 直接说明意图（Agent 会根据 `SKILL.md` 的 description 匹配）。

**示例提示词**

- `用 structured-learning 帮我做接下来两周学 Docker 的元认知计划`
- `刚读完《XXX》第 5 章，按四遍学习输出，笔记写到 ./learning-notes/`
- `这个项目结束了，按过程沉淀模板复盘`
- `这些链接/笔记太散了，帮我提炼 3～5 条原理并建树`
- `竞品分析是 AI 写的，我卡在 B 站 API 字段上——帮我记先做后学日志`

默认笔记目录：`./learning-notes/`（可在对话里改路径）。若用 Obsidian，可参考 `structured-learning/reference.md` 中的「可迁移 / 岗位专用」目录建议。

---

## 仓库结构

```
study-skill/
├── README.md
├── LICENSE
├── structured-learning/
│   ├── SKILL.md                 # Agent 主指令与场景路由
│   ├── reference.md             # 方法参考（Agent 按需阅读）
│   └── templates/
│       ├── knowledge-three-questions.md   # 理解三问 · 归位
│       ├── metacognition-plan.md        # 元认知学习计划
│       ├── four-pass-learning.md          # 四遍学习
│       ├── process-debrief.md             # 过程沉淀复盘
│       ├── task-first-learning-log.md     # 先做后学
│       ├── principle-extraction.md        # 原理与知识树
│       └── transfer-validation.md         # 迁移验证
```

---

## 自定义与贡献

| 想改的内容 | 编辑文件 |
|------------|----------|
| 触发场景、主流程 | `structured-learning/SKILL.md` |
| 方法论说明 | `structured-learning/reference.md` |
| 新增一种学习场景 | 在 `templates/` 加 Markdown，并在 `SKILL.md` 路由表登记 |

欢迎 Issue / PR。

---

## 许可

本项目 Skill 文本与模板采用 [MIT License](LICENSE) 发布。

本地若另有 `assets/` 等第三方课程转录，默认不纳入本仓库；自行公开前请确认版权。
