# 🎓 毕业项目：个人主页交互

> 学完JS阶段，你需要为个人主页添加交互功能

## 承接上一阶段

继续使用 CSS阶段的美化后的代码，在此基础上添加JavaScript交互。

## 项目目标

让个人主页**能动起来**，有用户交互。

## 必须实现的功能

| 功能 | 描述 | 难度 |
|------|------|------|
| 标签切换 | 点击标签切换不同内容区域 | ⭐⭐ |
| 表单验证 | 提交联系表单时验证输入 | ⭐⭐ |
| 回到顶部 | 点击按钮平滑回到页面顶部 | ⭐ |
| 移动端菜单 | 手机端点击hamburger菜单展开导航 | ⭐⭐⭐ |

## 挑战题（可选）

- [ ] 技能标签点击展开详情
- [ ] 作品图片点击放大
- [ ] 暗黑模式切换
- [ ] 滚动显示动画

## 示例代码

```javascript
// 标签切换
const tabs = document.querySelectorAll('.tab');
const panels = document.querySelectorAll('.panel');

tabs.forEach(tab => {
    tab.addEventListener('click', () => {
        // 移除active
        tabs.forEach(t => t.classList.remove('active'));
        panels.forEach(p => p.classList.remove('active'));
        
        // 添加active
        tab.classList.add('active');
        const target = tab.dataset.target;
        document.querySelector(target).classList.add('active');
    });
});

// 回到顶部
const backToTop = document.querySelector('#backToTop');
backToTop.addEventListener('click', () => {
    window.scrollTo({ top: 0, behavior: 'smooth' });
});

// 表单验证
const form = document.querySelector('#contactForm');
form.addEventListener('submit', (e) => {
    e.preventDefault();
    const email = form.querySelector('[name="email"]').value;
    if (!email.includes('@')) {
        alert('请输入正确的邮箱');
        return;
    }
    alert('提交成功！');
});
```

---

**完成后找AI教练验收！**
