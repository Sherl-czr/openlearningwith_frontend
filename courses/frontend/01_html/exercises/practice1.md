# 练习题：HTML 基础

## 练习1：基础标签认知

### 题目
写出以下内容的HTML标签：

1. 一级标题"欢迎来到我的网站"
2. 一个段落"这是一个关于编程的博客"
3. 一个跳转到"https://github.com"的链接，文字是"GitHub"
4. 一张图片，地址是"https://example.com/logo.png"

### 答案

```html
<h1>欢迎来到我的网站</h1>
<p>这是一个关于编程的博客</p>
<a href="https://github.com">GitHub</a>
<img src="https://example.com/logo.png">
```

---

## 练习2：列表和嵌套

### 题目
用HTML写一个无序列表，包含3个你最喜欢的编程语言，每个前面有一个emoji。

### 答案

```html
<ul>
    <li>🚀 JavaScript</li>
    <li>🐍 Python</li>
    <li>☕ Java</li>
</ul>
```

---

## 练习3：语义化标签

### 题目
用语义化标签（header, nav, main, footer）组织以下内容：

- 顶部：标题"我的博客"
- 导航：两个链接"首页"、"关于"
- 主体：一篇文章"学习HTML"
- 底部：版权文字

### 答案

```html
<header>
    <h1>我的博客</h1>
    <nav>
        <a href="/">首页</a>
        <a href="/about">关于</a>
    </nav>
</header>

<main>
    <article>
        <h2>学习HTML</h2>
        <p>HTML是网页的基础...</p>
    </article>
</main>

<footer>
    <p>&copy; 2026 我的博客</p>
</footer>
```

---

## 练习4：表单

### 题目
写一个注册表单，包含：
- 用户名（文本输入）
- 邮箱（邮箱输入）
- 密码（密码输入）
- 提交按钮

### 答案

```html
<form action="/register" method="POST">
    <label for="username">用户名：</label>
    <input type="text" id="username" name="username" required>

    <label for="email">邮箱：</label>
    <input type="email" id="email" name="email" required>

    <label for="password">密码：</label>
    <input type="password" id="password" name="password" required>

    <button type="submit">注册</button>
</form>
```

---

## 练习5：综合实战

### 题目
用HTML写一个个人介绍页面，包含：

1. 头部：你的名字作为标题
2. 导航：2个链接（GitHub、个人博客）
3. 关于我：一个介绍段落
4. 技能列表：3个技能
5. 联系方式：邮箱

### 答案（参考）

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>我的个人主页</title>
</head>
<body>
    <header>
        <h1>小明的个人主页</h1>
        <nav>
            <a href="https://github.com">GitHub</a>
            <a href="https://blog.example.com">个人博客</a>
        </nav>
    </header>

    <main>
        <section>
            <h2>关于我</h2>
            <p>大家好！我是一名热爱编程的开发者，喜欢学习新技术。</p>
        </section>

        <section>
            <h2>技能</h2>
            <ul>
                <li>JavaScript</li>
                <li>HTML/CSS</li>
                <li>Python</li>
            </ul>
        </section>

        <section>
            <h2>联系方式</h2>
            <p>邮箱：xiaoming@email.com</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 小明</p>
    </footer>
</body>
</html>
```

---

## 🎉 完成标准

- 练习1-4：能正确写出标签即可
- 练习5：结构完整、语义化、有实际内容

完成后找AI教练批改！
