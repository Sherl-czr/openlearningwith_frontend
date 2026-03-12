# 🧠 认知测试：CSS基础

> 解锁AI辅助模式前，必须通过认知测试

## 测试规则

- 概念选择：5道题，至少对4道
- 改错题：3道题，至少对2道
- 思路题：2道题，表达清晰即可
- 总分：≥80%通过

---

## 第一部分：概念选择（5x4=20分）

### Q1: 下面哪个CSS属性用于设置文字颜色？

A. background-color
B. text-color
C. color
D. font-color

**答案**：C

---

### Q2: Flex布局中，如何让元素水平居中？

A. align-items: center
B. justify-content: center
C. text-align: center
D. margin: 0 auto

**答案**：B

---

### Q3: 盒子模型的组成从内到外是？

A. margin → padding → content → border
B. content → padding → border → margin
C. padding → content → margin → border
D. content → margin → padding → border

**答案**：B

---

### Q4: 下面哪个选择器优先级最高？

A. .box
B. #box
C. div.box
D. *

**答案**：B

---

### Q5: 响应式设计中，下面哪个媒体查询表示"屏幕宽度小于768px"？

A. @media (min-width: 768px)
B. @media (max-width: 768px)
C. @media (width: 768px)
D. @media (screen: 768px)

**答案**：B

---

## 第二部分：改错题（3x20=60分）

### Q1: 找出下面CSS的错误

```css
.box {
    width: 100px,
    height: 100px,
    background: red;
}
```

**答案**：
- ❌ 属性之间不能用逗号，应该用分号
- ✅ 正确：`width: 100px; height: 100px;`

---

### Q2: 找出下面CSS的错误

```css
.container {
    display: flex;
    justify-content: center;
}
```

**答案**：
- ❌ 垂直方向没有居中
- ✅ 应该加 `align-items: center;`

---

### Q3: 找出下面CSS的错误

```css
@media (max-width: 768px) 
    .grid {
        grid-template-columns: 1fr;
    }
}
```

**答案**：
- ❌ 媒体查询条件后要加 `{`
- ✅ 正确：`@media (max-width: 768px) { ... }`

---

## 第三部分：思路题（2x10=20分）

### Q1: 如果要让一个元素在其父容器中水平和垂直都居中，请说出你的思路。

**参考答案**：
- 父容器设置 `display: flex;`
- `justify-content: center;` 水平居中
- `align-items: center;` 垂直居中
- 需要给父容器明确的高度

**评分标准**：
- 提到flex：3分
- 提到justify-content：3分
- 提到align-items：3分
- 提到高度：1分

---

### Q2: 解释一下CSS中 margin 和 padding 的区别。

**参考答案**：
- margin：元素外部的间距，影响元素与其他元素的距离
- padding：元素内部的间距，影响内容与元素边框的距离

**评分标准**：
- 解释margin：5分
- 解释padding：5分

---

## 🎯 评分标准

| 分数 | 结果 |
|------|------|
| ≥80% | ✅ 通过，解锁AI辅助模式 |
| <80% | ❌ 需要重新学习，建议重新阅读concept.md |

---

**完成后找AI教练批改！**
