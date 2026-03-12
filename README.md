# 🤖 AI Learning Coach

> 让AI成为你的私人编程教练，像打怪升级一样学习前端

## 🎯 项目介绍

这是一个**AI驱动的编程学习系统**，让你在VSCode里通过Claude Code，随时拥有一个1对1的编程私教。

### 学习三阶段模式

```
第一阶段：手敲基础（必须）
    ↓ 基础练习全部完成
第二阶段：认知测试（解锁）
    ↓ 测试通过（≥80%）
第三阶段：AI生成进阶（手写）
```

- **学什么**：HTML → CSS → JavaScript（最小化路径）
- **怎么学**：概念 → 案例 → 练习 → 认知测试 → 毕业项目 → AI进阶
- **AI怎么帮你**：出题、批改、答疑、记录进度、情感陪伴

## 📁 项目结构

```
ai-learning-coach/
├── prompts/
│   ├── coach.md              # 🤖 AI教练核心Prompt
│   └── ai_generator/         # 🤖 AI练习生成器
│       └── generator.md
├── courses/
│   └── frontend/
│       ├── 01_html/
│       │   ├── concept.md    # 概念
│       │   ├── case.md       # 案例
│       │   ├── exercises/    # 练习题
│       │   ├── test/         # 认知测试
│       │   │   └── cognition_test.md
│       │   └── project/      # 毕业项目
│       ├── 02_css/
│       └── 03_js/
├── user_data/                # 用户数据（你的学习记录）
│   ├── progress.json         # 进度
│   ├── logs/                 # 学习日志
│   ├── emotions/             # 情感记录
│   ├── errors/               # 错误记录
│   └── ai_generated/         # AI生成练习记录
├── .claude/
│   └── settings.json         # Claude Code配置
└── plugins.md                # 推荐插件
```

## 🚀 快速开始

### 1. 安装Claude Code

```bash
# Mac
brew install claude-code

# 或其他方式安装
npm install -g @anthropic/claude-code
```

### 2. 在VSCode中打开此项目

```bash
cd ai-learning-coach
code .
```

### 3. 启动AI教练

在VSCode终端输入：
```bash
claude
```

然后告诉AI：
> "我想开始学习前端，请读取 `prompts/coach.md` 并按照指示指导我学习。"

## 📚 学习路径（最小化）

| 阶段 | 内容 | 子阶段 |
|------|------|--------|
| 01 | HTML：标签、语义化、表单 | 基础 → 认知测试 → 毕业项目 |
| 02 | CSS：布局(Flex/Grid)、盒子模型、响应式 | 基础 → 认知测试 → 毕业项目 |
| 03 | JS：DOM操作、事件、异步基础 | 基础 → 认知测试 → 毕业项目 |

**不学的**：复杂的CSS动画、偏门的JS API、遗留语法

## 🎮 打怪升级

- 完成练习：+10 XP
- 认知测试通过：+50 XP
- 阶段通关：+100 XP
- 毕业项目：+200 XP
- AI进阶练习：+15 XP

### 成就徽章
- 🌱 新手：完成第一道题
- 🧠 学者：通过认知测试
- 📄 页面师：完成HTML毕业项目
- 🎨 美化师：完成CSS毕业项目
- ⚡ 交互师：完成JS毕业项目
- 🤖 AI捕手：完成AI生成进阶练习
- 🏆 全通：完成所有阶段

## 🔑 核心创新点

### 1. 先手敲再认知测试
- 确保肌肉记忆
- 验证真理解，不假会

### 2. 边学边记录
- 实时进度
- 错误类型统计
- 问题记录

### 3. AI生成进阶（需通过认知测试）
- 个性化无限练习
- 必须手写，拒绝vibecoding

### 4. 毕业项目制
- HTML阶段：个人网页骨架
- CSS阶段：美化网页
- JS阶段：添加交互

## 💡 如何让AI帮你学习

### 对话示例

```
你：我想学前端
AI：好的！让我先了解一下你的基础...
（读取coach.md，开始指导）

你：做练习
AI：来做道题检验一下？
（出题，你作答，AI批改）

你：参加认知测试
AI：好的，请完成这份测试...
（测试，批改，记录分数）

你：生成AI练习
AI：（确认已通过认知测试）请描述你想要什么练习...
```

## 🤝 贡献

欢迎贡献练习题！

1. 在对应阶段的 `exercises/` 添加 `.md` 文件
2. 格式：
```markdown
# 练习题：XXX

## 题目
...

## 答案
...
```

## 📝 许可证

MIT
