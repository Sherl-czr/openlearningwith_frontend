# VSCode 前端开发推荐插件

> 工欲善其事，必先利其器

## 🚀 必装插件

### 1. Live Server
- **作用**：本地启动一个实时更新的网页服务器
- **场景**：写HTML/CSS/JS时，保存自动刷新浏览器
- **快捷**：右键 → "Open with Live Server"

### 2. Prettier - Code formatter
- **作用**：自动格式化代码（缩进、对齐、引号等）
- **快捷**：`Shift + Option + F`（Mac）/ `Shift + Alt + F`（Windows）

### 3. ESLint
- **作用**：检测JavaScript语法错误和代码风格问题
- **配合**：保存时自动修复

### 4. HTML CSS Support
- **作用**：HTML和CSS的智能提示
- **场景**：写class名时自动补全

### 5. Auto Rename Tag
- **作用**：修改开始标签时，自动修改结束标签
- **场景**：改`<div>`时，帮你改`</div>`

---

## 💡 推荐插件

### 6. vscode-icons
- **作用**：美化文件图标
- **效果**：一眼认出文件类型

### 7. GitLens
- **作用**：增强Git功能
- **场景**：查看代码历史、谁改的

### 8. Error Lens
- **作用**：把错误直接显示在代码行上
- **效果**：更明显地看到问题

### 9. Path Intellisense
- **作用**：路径自动补全
- **场景**：写`src=""`、`href=""`时

### 10. Auto Close Tag
- **作用**：自动闭合HTML标签

---

## 🔧 插件安装方法

1. 打开VSCode
2. 按 `Cmd + Shift + X`（Mac）或 `Ctrl + Shift + X`（Windows）
3. 搜索插件名
4. 点击"安装"

---

## ⚙️ 推荐设置

在 `settings.json` 中添加：

```json
{
  // 保存时自动格式化
  "editor.formatOnSave": true,
  
  // 自动闭合标签
  "html.autoClosingTags": true,
  "javascript.autoClosingTags": true,
  
  // Tab大小
  "editor.tabSize": 2,
  
  // 空格代替Tab
  "editor.insertSpaces": true
}
```

---

## 📦 快速安装命令

```bash
# 打开VSCode并安装插件（需要code命令）
code --install-extension ritwickdey.LiveServer
code --install-extension esbenp.prettier-vscode
code --install-extension dbaeumer.vscode-eslint
code --install-extension ecmel.vscode-html-css-support
code --install-extension formulahendry.auto-rename-tag
```
