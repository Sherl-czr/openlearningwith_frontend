# 🤖 AI Learning Coach

> 让AI成为你的私人编程教练，像打怪升级一样学习前端

## 🎯 项目介绍

这是一个**AI驱动的编程学习系统**，让你在VSCode里通过Claude Code，随时拥有一个1对1的编程私教。

- **学什么**：HTML → CSS → JavaScript（最小化路径）
- **怎么学**：概念 → 案例 → 练习 → 反馈
- **AI怎么帮你**：出题、批改、答疑、记录进度、情感陪伴

## 📁 项目结构

```
ai-learning-coach/
├── prompts/
│   └── coach.md              # 🤖 AI教练核心Prompt
├── courses/
│   └── frontend/             # 前端学习路径
│       ├── 01_html/          # 第一阶段：HTML
│       │   ├── concept.md    # 概念
│       │   ├── case.md       # 案例
│       │   └── exercises/    # 练习题
│       ├── 02_css/           # 第二阶段：CSS
│       └── 03_js/            # 第三阶段：JS
├── user_data/                # 用户数据（你的学习记录）
│   ├── progress.json         # 进度
│   ├── logs/                 # 学习日志
│   └── emotions/             # 情感记录
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

基于第一性原理，只学最核心的：

| 阶段 | 内容 | 优先级 |
|------|------|--------|
| 01 | HTML：标签、语义化、表单 | ⭐⭐⭐⭐⭐ |
| 02 | CSS：布局(Flex/Grid)、盒子模型、响应式 | ⭐⭐⭐⭐⭐ |
| 03 | JS：DOM操作、事件、异步基础 | ⭐⭐⭐⭐⭐ |

**不学的**：复杂的CSS动画、偏门的JS API、遗留语法

## 💡 如何让AI帮你学习

### 核心Prompt逻辑

1. **读取教练Prompt**：`prompts/coach.md`
2. **理解学习内容**：读取对应阶段的 `concept.md`、`case.md`
3. **出题**：从 `exercises/` 读取练习，或自动生成
4. **记录**：写入 `user_data/progress.json` 和 `logs/`
5. **情感陪伴**：记录用户在 `emotions/` 中的问题

### 示例对话

```
你：我想学前端
AI：好的！让我先了解一下你的基础...
（读取coach.md，开始指导）

你：HTML学完了
AI：来做道题检验一下？
（出题，你作答，AI批改，反馈）

我遇到了一个问题：...
AI：别急，这是个常见问题...
（记录到emotions/，给出解决方案）
```

## 🎮 打怪升级

每完成一个练习：
- ✅ 经验值 +10
- 🏆 解锁新成就
- 📈 进度可视化

## 🤝 贡献

欢迎贡献练习题！

1. 在 `courses/frontend/XX_xxx/exercises/` 添加 `.md` 文件
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
