# 🎓 毕业项目：个人主页美化

> 学完CSS阶段，你需要美化之前的个人主页

## 承接上一阶段

继续使用 HTML阶段的个人主页代码，在此基础上添加CSS样式。

## 项目目标

让个人主页**看起来漂亮、专业**。

## 必须实现的效果

| 效果 | 描述 | 难度 |
|------|------|------|
| 布局 | 使用Flexbox实现导航栏水平排列 | ⭐ |
| 间距 | 合理的margin/padding，让页面呼吸感 | ⭐ |
| 配色 | 选定一个配色方案（不超过3种主色） | ⭐⭐ |
| 字体 | 使用Google Fonts，设置合适的字号 | ⭐⭐ |
| 响应式 | 手机端正常显示，导航变垂直 | ⭐⭐ |
| 卡片 | 技能和作品用卡片样式展示 | ⭐⭐⭐ |

## 挑战题（可选）

- [ ] 添加渐变背景
- [ ] 添加按钮hover效果
- [ ] 作品用Grid布局展示
- [ ] 添加简单的CSS动画

## 示例样式

```css
/* 全局重置 */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Noto Sans SC', sans-serif;
    line-height: 1.6;
    color: #333;
}

/* 导航 */
nav {
    display: flex;
    justify-content: space-between;
    padding: 1rem 2rem;
    background: #fff;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

/* 卡片 */
.card {
    background: #fff;
    padding: 1.5rem;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

/* 响应式 */
@media (max-width: 768px) {
    nav {
        flex-direction: column;
    }
}
```

---

**完成后找AI教练验收！**
