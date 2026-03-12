# 🎓 毕业项目：个人主页

> 学完HTML阶段，你需要创建一个属于自己的个人主页

## 项目目标

创建一个**个人主页**，包含你的基本信息展示。

## 必须包含的内容

| 模块 | 内容 | 难度 |
|------|------|------|
| 头部 | 你的名字作为大标题 | ⭐ |
| 导航 | 3个锚点链接（关于、技能、联系） | ⭐ |
| 关于 | 一段自我介绍 | ⭐ |
| 技能 | 你会的东西列表 | ⭐⭐ |
| 作品 | 展示3个作品（可以用占位图） | ⭐⭐ |
| 联系 | 你的联系方式（邮箱/社交媒体） | ⭐ |
| 底部 | 版权信息 | ⭐ |

## 验收标准

1. ✅ 使用语义化标签（header/nav/main/footer）
2. ✅ 所有链接能正常跳转（锚点）
3. ✅ 表单元素可用（email输入）
4. ✅ 代码规范（缩进、命名）
5. ✅ 内容真实（不要用"Lorem Ipsum"）

## 示例代码

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
            <a href="#about">关于</a>
            <a href="#skills">技能</a>
            <a href="#contact">联系</a>
        </nav>
    </header>

    <main>
        <section id="about">
            <h2>关于我</h2>
            <p>我是xxx，热爱编程...</p>
        </section>

        <section id="skills">
            <h2>我的技能</h2>
            <ul>
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
            </ul>
        </section>

        <section id="contact">
            <h2>联系我</h2>
            <p>邮箱：xxx@email.com</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 我的个人主页</p>
    </footer>
</body>
</html>
```

## 挑战题（可选）

- [ ] 添加一张个人照片
- [ ] 添加一个留言表单
- [ ] 做一个作品集网格

---

**完成后找AI教练验收！**
