# 练习题：JavaScript 基础

## 练习1：变量和输出

### 题目
1. 声明一个变量name，值为你的名字
2. 声明一个常量age，值为你的年龄
3. 用console.log输出"我叫xxx，今年xx岁"

### 答案

```javascript
let name = '小明';
const age = 18;

console.log('我叫' + name + '，今年' + age + '岁');
// 或模板字符串
console.log(`我叫${name}，今年${age}岁`);
```

---

## 练习2：函数

### 题目
写一个函数，接收两个数字参数，返回它们的和。

### 答案

```javascript
function add(a, b) {
    return a + b;
}

// 或箭头函数
const add = (a, b) => a + b;

console.log(add(1, 2)); // 3
```

---

## 练习3：DOM操作

### 题目
获取class为"title"的元素，把它的文字改成"Hello World"。

### 答案

```javascript
const title = document.querySelector('.title');
title.textContent = 'Hello World';
```

---

## 练习4：点击事件

### 题目
给一个按钮绑定点击事件，点击时弹出"你点击了我"。

### 答案

```javascript
const btn = document.querySelector('#btn');

btn.addEventListener('click', () => {
    alert('你点击了我');
});
```

---

## 练习5：修改样式

### 题目
点击按钮时，让div的背景色在红色和蓝色之间切换。

### 答案

```html
<button id="btn">变色</button>
<div id="box" style="width:100px;height:100px;background:red;"></div>

<script>
    const btn = document.querySelector('#btn');
    const box = document.querySelector('#box');
    let isRed = true;

    btn.addEventListener('click', () => {
        if (isRed) {
            box.style.background = 'blue';
        } else {
            box.style.background = 'red';
        }
        isRed = !isRed;
    });
</script>
```

---

## 练习6：数组操作

### 题目
有一个数组 `[1, 2, 3, 4, 5]`：
1. 用map返回每个元素*2的新数组
2. 用filter返回大于3的元素
3. 用reduce返回所有元素之和

### 答案

```javascript
const arr = [1, 2, 3, 4, 5];

// map
const doubled = arr.map(item => item * 2);
console.log(doubled); // [2, 4, 6, 8, 10]

// filter
const filtered = arr.filter(item => item > 3);
console.log(filtered); // [4, 5]

// reduce
const sum = arr.reduce((total, item) => total + item, 0);
console.log(sum); // 15
```

---

## 练习7：综合实战

### 题目
实现一个简单的计数器：
- 页面上有一个数字显示"0"
- 一个"+"按钮，点击数字+1
- 一个"-"按钮，点击数字-1

### 答案

```html
<p id="count">0</p>
<button id="add">+</button>
<button id="sub">-</button>

<script>
    const countEl = document.querySelector('#count');
    const addBtn = document.querySelector('#add');
    const subBtn = document.querySelector('#sub');
    let count = 0;

    addBtn.addEventListener('click', () => {
        count++;
        countEl.textContent = count;
    });

    subBtn.addEventListener('click', () => {
        count--;
        countEl.textContent = count;
    });
</script>
```

---

## 练习8：表单处理

### 题目
给输入框绑定input事件，实时把输入的内容显示在下面的p标签中。

### 答案

```html
<input type="text" id="input">
<p id="output"></p>

<script>
    const input = document.querySelector('#input');
    const output = document.querySelector('#output');

    input.addEventListener('input', (e) => {
        output.textContent = e.target.value;
    });
</script>
```

---

## 🎉 完成标准

- 练习1-4：掌握基础语法
- 练习5-6：掌握DOM和数组
- 练习7-8：能完成简单交互

完成后找AI教练批改！
