# 🧠 认知测试：JavaScript基础

> 解锁AI辅助模式前，必须通过认知测试

## 测试规则

- 概念选择：5道题，至少对4道
- 改错题：3道题，至少对2道
- 思路题：2道题，表达清晰即可
- 总分：≥80%通过

---

## 第一部分：概念选择（5x4=20分）

### Q1: 下面哪个是声明变量的正确方式？

A. var name = '小明'
B. let const name = '小明'
C. int name = '小明'
D. name := '小明'

**答案**：A（ES6+推荐用let/const）

---

### Q2: 如何获取页面中class为"box"的第一个元素？

A. document.getElementByClass('box')
B. document.querySelector('.box')
C. document.getElementById('box')
D. document.querySelectorAll('.box')

**答案**：B

---

### Q3: 下面哪个是箭头函数的正确写法？

A. function = (a, b) => { return a + b }
B. const add = (a, b) => a + b
C. const add = (a, b) => { a + b }
D. const add = function(a, b) => a + b

**答案**：B

---

### Q4: 给按钮绑定点击事件，正确的方式是？

A. button.onclick = 'alert(1)'
B. button.addEventListener('click', alert(1))
C. button.addEventListener('click', () => { alert('1') })
D. button.click = alert(1)

**答案**：C

---

### Q5: 数组的map方法返回的是什么？

A. 数组
B. 对象
C. 字符串
D. 数字

**答案**：A

---

## 第二部分：改错题（3x20=60分）

### Q1: 找出下面JS代码的错误

```javascript
const box = document.querySelector('.box');
box.addEventListener('click', function() {
    console.log('clicked');
});
```

**答案**：
- ❌ 如果box不存在会报错
- ✅ 应该先判断：`if (box) { ... }`

---

### Q2: 找出下面JS代码的错误

```javascript
const arr = [1, 2, 3];
const result = arr.map(item => {
    item * 2
});
```

**答案**：
- ❌ map的回调函数没有return
- ✅ 应该 `return item * 2`

---

### Q3: 找出下面JS代码的错误

```javascript
const btn = document.querySelector('#btn');
btn.addEventListener('click', () => {
    console.log('hi);
});
```

**答案**：
- ❌ 字符串引号没有配对 'hi"
- ✅ 应该是 `'hi'`

---

## 第三部分：思路题（2x10=20分）

### Q1: 如果要实现"点击按钮切换元素的显示/隐藏"，请说出你的思路。

**参考答案**：
- 获取按钮和目标元素
- 给按钮绑定click事件
- 在事件中判断元素是否隐藏
- 使用 display: none/block 或 classList.toggle 来切换
- 或者使用 visibility: hidden/visible

**评分标准**：
- 提到获取元素：2分
- 提到事件绑定：3分
- 提到切换逻辑：3分
- 提到具体方法：2分

---

### Q2: 解释一下 const 和 let 的区别。

**参考答案**：
- const：声明常量，不能重新赋值
- let：声明变量，可以重新赋值
- 两者都是块级作用域，不像var有变量提升问题

**评分标准**：
- 解释const：4分
- 解释let：4分
- 提到作用域：2分

---

## 🎯 评分标准

| 分数 | 结果 |
|------|------|
| ≥80% | ✅ 通过，解锁AI辅助模式 |
| <80% | ❌ 需要重新学习，建议重新阅读concept.md |

---

**完成后找AI教练批改！**
