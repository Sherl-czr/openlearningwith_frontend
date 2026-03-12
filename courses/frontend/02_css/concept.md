# CSS 概念篇

> HTML是骨架，CSS是衣服

## 什么是CSS？

**CSS = 层叠样式表**

用人话说：它是一种用来**美化网页**的语言。

- HTML决定**结构**
- CSS决定**样式**（颜色、布局、大小）

## 核心概念

### 1. 选择器（Selector）

你想要样式化哪个元素，就要先**选中它**：

```css
/* 选中所有p标签 */
p {
    color: red;
}

/* 选中class="title"的元素 */
.title {
    font-size: 24px;
}

/* 选中id="header"的元素 */
#header {
    background: blue;
}
```

### 2. 三大引入方式

```html
<!-- 1. 内联样式（不推荐） -->
<p style="color: red;">红色文字</p>

<!-- 2. 内部样式表（学习时用） -->
<head>
    <style>
        p { color: red; }
    </style>
</head>

<!-- 3. 外部样式表（正式项目） -->
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

### 3. 盒子模型（Box Model）

每个元素都是一个"盒子"：

```
┌─────────────────────┐  ← margin（外边距）
│  ┌───────────────┐  │  ← border（边框）
│  │ ┌───────────┐ │  │  ← padding（内边距）
│  │ │  内容区域  │ │  │
│  │ └───────────┘ │  │
│  └───────────────┘  │
└─────────────────────┘
```

```css
.box {
    margin: 20px;      /* 外边距 */
    padding: 10px;    /* 内边距 */
    border: 1px solid red; /* 边框 */
    width: 100px;     /* 内容宽度 */
    height: 50px;     /* 内容高度 */
}
```

### 4. Flex布局（最重要！）

```css
/* 父容器 */
.container {
    display: flex;
    justify-content: center;    /* 水平居中 */
    align-items: center;       /* 垂直居中 */
    gap: 10px;                /* 元素间距 */
}

/* 子元素 */
.item {
    flex: 1;  /* 等分剩余空间 */
}
```

### 5. Grid布局（进阶）

```css
.container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr; /* 三列等宽 */
    gap: 20px;
}
```

### 6. 常见属性

| 属性 | 用途 | 例子 |
|------|------|------|
| color | 文字颜色 | color: red; |
| background | 背景 | background: #f5f5f5; |
| font-size | 字号 | font-size: 16px; |
| width/height | 宽高 | width: 100px; |
| margin/padding | 间距 | margin: 10px; |
| border | 边框 | border: 1px solid #ccc; |
| display | 显示模式 | display: flex; |
| position | 定位 | position: relative; |

### 7. 响应式设计

```css
/* 屏幕宽度小于768px时生效 */
@media (max-width: 768px) {
    .container {
        flex-direction: column;
    }
}
```

## 最小化必须掌握

| 优先级 | 属性 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | display: flex | 布局 |
| ⭐⭐⭐⭐⭐ | margin/padding | 间距 |
| ⭐⭐⭐⭐ | color/font-size | 文字 |
| ⭐⭐⭐ | background | 背景 |
| ⭐⭐ | 媒体查询 | 响应式 |
| ⭐ | position | 特殊定位 |

## 常见误区

1. **❌ 不理解盒子模型**
   - ✅ width是内容区，不包含padding和border

2. **❌ 滥用div**
   - ✅ 用语义化标签配合class

3. **❌ 忘记重置样式**
   - ✅ 加 `* { margin: 0; padding: 0; box-sizing: border-box; }`

4. **❌ flex布局居中失效**
   - ✅ 父容器要设置height

---

**下一节**：看看真实案例 → [case.md](./case.md)
