# CSS 案例篇

> 光说不练假把式，来看看真实的CSS长啥样

## 案例一：居中布局

```html
<div class="container">
    <div class="box">我在正中间</div>
</div>
```

```css
.container {
    width: 400px;
    height: 400px;
    background: #f0f0f0;
    /* 核心代码 */
    display: flex;
    justify-content: center;
    align-items: center;
}

.box {
    width: 100px;
    height: 100px;
    background: #ff6b6b;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
}
```

**效果**：一个灰色大方块，中间有一个红色小方块。

## 案例二：导航栏

```html
<nav class="navbar">
    <div class="logo">MyLogo</div>
    <ul class="nav-links">
        <li><a href="#">首页</a></li>
        <li><a href="#">关于</a></li>
        <li><a href="#">作品</a></li>
    </ul>
</nav>
```

```css
/* 重置 */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background: #333;
    color: white;
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-links a {
    color: white;
    text-decoration: none;
}

.nav-links a:hover {
    color: #ff6b6b;
}
```

## 案例三：卡片网格

```html
<div class="grid">
    <div class="card">卡片1</div>
    <div class="card">卡片2</div>
    <div class="card">卡片3</div>
</div>
```

```css
.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    padding: 20px;
}

.card {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

/* 响应式：小屏幕变1列 */
@media (max-width: 768px) {
    .grid {
        grid-template-columns: 1fr;
    }
}
```

## 案例四：按钮样式

```html
<button class="btn">点我</button>
<button class="btn btn-primary">主要</button>
<button class="btn btn-outline">描边</button>
```

```css
.btn {
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 1rem;
    transition: all 0.3s;
}

.btn-primary {
    background: #007bff;
    color: white;
}

.btn-primary:hover {
    background: #0056b3;
    transform: translateY(-2px);
}

.btn-outline {
    background: transparent;
    border: 2px solid #007bff;
    color: #007bff;
}

.btn-outline:hover {
    background: #007bff;
    color: white;
}
```

## 常用技巧

### 1. 文字省略

```css
.text-ellipsis {
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}
```

### 2. 清除浮动

```css
.clearfix::after {
    content: '';
    display: block;
    clear: both;
}
```

### 3. 渐变背景

```css
.gradient {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

---

**下一步**：来做练习检验一下！→ [exercises](./exercises/)
