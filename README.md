# structured-learning — Cursor Agent Skill

面向 **结构化个人学习** 的 Cursor Skill：原理化知识体系、元认知规划、四遍学习、过程沉淀、先做后学与知识迁移。Agent 按 SOP 引导并生成 Markdown 笔记。

## 安装

### 方式 A：个人 Skill（推荐）

克隆本仓库后，将 `structured-learning` 目录复制到 Cursor 个人技能目录：

**Windows**

```bash
git clone https://github.com/<你的用户名>/<仓库名>.git
xcopy /E /I structured-learning "%USERPROFILE%\.cursor\skills\structured-learning"
```

**macOS / Linux**

```bash
git clone https://github.com/<你的用户名>/<仓库名>.git
cp -R structured-learning ~/.cursor/skills/structured-learning
```

在 Cursor 对话中 @ 引用 **structured-learning**，或描述学习/知识体系相关需求，Agent 会按 `SKILL.md` 执行。

> 不要放到 `~/.cursor/skills-cursor/`，该目录为 Cursor 内置技能保留。

### 方式 B：项目 Skill

在本仓库根目录已有完整 skill 时，也可复制到项目的 `.cursor/skills/structured-learning`（需自行创建 `.cursor/skills`）。

## 仓库结构

```
structured-learning/
├── SKILL.md              # Agent 主指令
├── reference.md          # 方法参考（按需阅读）
└── templates/            # 可复制的输出模板
assets/                   # 本地参考素材（可选，未纳入 skill 逻辑）
```

默认学习笔记输出目录：`./learning-notes/`（可在对话中指定其他路径）。

## 发布到 GitHub

在项目根目录（本 README 所在目录）：

```bash
git init -b main
git add .
git commit -m "Initial commit: structured-learning Cursor skill"
gh repo create structured-learning-skill --public --source=. --remote=origin --push
```

未安装 [GitHub CLI](https://cli.github.com/) 时，在 GitHub 网页新建空仓库后：

```bash
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

## 使用示例

- 「用 structured-learning 帮我规划接下来两周学 Docker」
- 「刚读完某书第 5 章，做第四遍输出，写到 learning-notes」
- 「项目结束了，按过程沉淀模板复盘」

## 许可

Skill 文本与模板以 MIT 发布（见 [LICENSE](LICENSE)）。`assets/` 内若为第三方课程转录，请自行确认版权后再公开仓库；不需要公开时可把 `assets/` 加入 `.gitignore`。

## 开发

- 改流程：编辑 `structured-learning/SKILL.md`
- 改方法细节：`structured-learning/reference.md`
- 新增场景：在 `templates/` 增加 Markdown，并在 `SKILL.md` 路由表登记
