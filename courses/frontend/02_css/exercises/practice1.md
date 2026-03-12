# 练习题：CSS 基础

## 练习1：选择器

### 题目
写CSS选中以下元素：
1. 所有h1标签，文字颜色设为蓝色
2. class为"important"的元素，背景设为黄色
3. id为"logo"的元素，字号设为24px

### 答案

```css
h1 {
    color: blue;
}

.important {
    background: yellow;
}

#logo {
    font-size: 24px;
}
```

---

## 练习2：盒子模型

### 题目
给一个div设置：
- 宽度100px，高度50px
- 内边距10px
- 边框1像素实线黑色
- 外边距20px

### 答案

```css
.box {
    width: 100px;
    height: 50px;
    padding: 10px;
    border: 1px solid black;
    margin: 20px;
}
```

---

## 练习3：Flex水平垂直居中

### 题目
父容器宽高400px，里面有一个子元素宽高100px，让子元素在父容器正中间。

### 答案

```css
.parent {
    width: 400px;
    height: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.child {
    width: 100px;
    height: 100px;
}
```

---

## 练习4：导航栏

### 题目
用Flex布局实现一个导航栏：
- 左侧：Logo文字
- 右侧：两个链接"首页"、"关于"
- 链接颜色是白色，hover时变红色

### 答案

```html
<nav class="navbar">
    <div class="logo">Logo</div>
    <div class="links">
        <a href="#">首页</a>
        <a href="#">关于</a>
    </div>
</nav>
```

```css
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    background: #333;
}

.links a {
    color: white;
    text-decoration: none;
    margin-left: 20px;
}

.links a:hover {
    color: red;
}
```

---

## 练习5：卡片布局

### 题目
用Grid布局实现3列卡片，每列之间间距20px。

### 答案

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
```

---

## 练习6：响应式

### 题目
当屏幕宽度小于600px时，3列卡片变成1列。

### 答案

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

@media (max-width: 600px) {
    .container {
        grid-template-columns: 1fr;
    }
}
```

---

## 练习7：综合实战

### 题目
写一个登录表单样式：
- 输入框宽度100%，内边距10px
- 按钮宽度100%，背景蓝色，白色文字，hover时变深蓝
- 输入框和按钮都圆角4px，间距15px

### 答案

```css
input {
    width: 100%;
    padding: 10px;
    border-radius: 4px;
    border: 1px solid #ccc;
    margin-bottom: 15px;
}

button {
    width: 100%;
    padding: 10px;
    background: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

button:hover {
    background: #0056b3;
}
```

---

## 🎉 完成标准

- 练习1-4：正确使用选择器和Flex
- 练习5-6：掌握Grid和响应式
- 练习7：能独立完成表单样式

完成后找AI教练批改！
