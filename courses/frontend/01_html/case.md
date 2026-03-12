# HTML 案例篇

> 光说不练假把式，来看看真实的HTML长啥样

## 案例：一个最简单的网页

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>我的第一个网页</title>
</head>
<body>
    <header>
        <h1>我的个人主页</h1>
        <nav>
            <a href="#about">关于</a>
            <a href="#works">作品</a>
            <a href="#contact">联系</a>
        </nav>
    </header>

    <main>
        <section id="about">
            <h2>关于我</h2>
            <p>你好！我叫小明，热爱编程和设计。</p>
        </section>

        <section id="works">
            <h2>我的作品</h2>
            <ul>
                <li>个人博客</li>
                <li>天气应用</li>
                <li>待办清单</li>
            </ul>
        </section>

        <section id="contact">
            <h2>联系我</h2>
            <p>邮箱：xiaoming@email.com</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 小明</p>
    </footer>
</body>
</html>
```

## 逐行解读

### 头部声明

```html
<!DOCTYPE html>
<html lang="zh-CN">
```
- `<!DOCTYPE html>`：告诉浏览器"这是HTML5"
- `<html lang="zh-CN">`：这是中文网页

### HEAD部分

```html
<head>
    <meta charset="UTF-8">
    <title>我的第一个网页</title>
</head>
```
- `meta charset="UTF-8"`：字符编码，避免乱码
- `title`：浏览器标签上的文字

### BODY部分

```html
<body>
    <header>...</header>
    <main>...</main>
    <footer>...</footer>
```
三大件：头部、主体、底部

## 案例二：带表单的页面

```html
<form action="/submit" method="POST">
    <label for="name">姓名：</label>
    <input type="text" id="name" name="name" required>

    <label for="email">邮箱：</label>
    <input type="email" id="email" name="email" required>

    <label for="message">留言：</label>
    <textarea id="message" name="message" rows="4"></textarea>

    <button type="submit">提交</button>
</form>
```

### 表单要点

| 标签 | 作用 |
|------|------|
| `<form>` | 表单容器，action是提交地址 |
| `<label>` | 关联文字和输入框 |
| `<input>` | 输入框，type决定类型 |
| `<textarea>` | 多行文本 |
| `<button>` | 按钮 |

### input的type

| type | 用途 |
|------|------|
| `text` | 单行文本 |
| `email` | 邮箱（有验证） |
| `password` | 密码（隐藏） |
| `number` | 数字 |
| `checkbox` | 多选框 |
| `radio` | 单选框 |

## 怎么运行？

### 方法1：直接打开
把代码保存为 `index.html`，双击用浏览器打开

### 方法2：VSCode Live Server
1. 安装VSCode插件"Live Server"
2. 右键 → "Open with Live Server"

---

**下一步**：来做练习检验一下！→ exercises/
