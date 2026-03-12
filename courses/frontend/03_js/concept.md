# JavaScript 概念篇

> HTML是骨架，CSS是衣服，JS是灵魂

## 什么是JavaScript？

**JS = 网页的编程语言**

- HTML：决定网页有什么
- CSS：决定网页长什么样
- **JS：决定网页能做什么**

## 核心概念

### 1. 变量

```javascript
// 声明变量
let name = '小明';      // 可以修改
const age = 18;         // 不能修改

// var（旧语法，不推荐）
var old = '旧写法';
```

### 2. 数据类型

```javascript
// 字符串
let str = '你好';

// 数字
let num = 123;

// 布尔值
let isTrue = true;
let isFalse = false;

// 数组
let arr = [1, 2, 3, '四', true];

// 对象
let person = {
    name: '小明',
    age: 18,
    city: '北京'
};
```

### 3. 函数

```javascript
// 声明函数
function sayHello(name) {
    return '你好，' + name;
}

// 调用
sayHello('小明');

// 箭头函数（现代写法）
const sayHi = (name) => {
    return '你好，' + name;
};

// 简写
const add = (a, b) => a + b;
```

### 4. 条件判断

```javascript
if (age >= 18) {
    console.log('成年人');
} else if (age >= 6) {
    console.log('未成年人');
} else {
    console.log('小孩');
}
```

### 5. 循环

```javascript
// for循环
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// for...of（数组）
const arr = [1, 2, 3];
for (let item of arr) {
    console.log(item);
}

// for...in（对象）
const obj = { a: 1, b: 2 };
for (let key in obj) {
    console.log(key, obj[key]);
}
```

### 6. DOM操作（最核心！）

```javascript
// 获取元素
const box = document.querySelector('.box');
const boxes = document.querySelectorAll('.box');

// 修改内容
box.innerHTML = '新内容';
box.textContent = '纯文本';

// 修改样式
box.style.color = 'red';
box.style.background = 'blue';

// 修改class
box.classList.add('active');
box.classList.remove('hidden');
box.classList.toggle('show');
```

### 7. 事件

```javascript
// 点击事件
button.addEventListener('click', () => {
    alert('你点击了按钮');
});

// 鼠标悬停
box.addEventListener('mouseenter', () => {
    box.style.background = 'red';
});

// 输入事件
input.addEventListener('input', (e) => {
    console.log(e.target.value);
});
```

### 8. 异步基础

```javascript
// setTimeout
setTimeout(() => {
    console.log('1秒后执行');
}, 1000);

// fetch（网络请求）
fetch('https://api.example.com/data')
    .then(res => res.json())
    .then(data => console.log(data))
    .catch(err => console.error(err));

// async/await（现代写法）
async function getData() {
        const res = await fetch(' {
    tryhttps://api.example.com/data');
        const data = await res.json();
        console.log(data);
    } catch (err) {
        console.error(err);
    }
}
```

## 最小化必须掌握

| 优先级 | 内容 | 用途 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | 变量 + 函数 | 基础 |
| ⭐⭐⭐⭐⭐ | DOM操作 | 让页面动起来 |
| ⭐⭐⭐⭐ | 事件监听 | 交互 |
| ⭐⭐⭐ | 数组方法 | 数据处理 |
| ⭐⭐ | 异步基础 | 网络请求 |

## 常见误区

1. **❌ 用var**
   - ✅ 用let/const

2. **❌ 直接操作DOM**
   - ✅ 用querySelector

3. **❌ 忘记事件解绑**
   - ✅ 合理使用事件委托

4. **❌ 回调地狱**
   - ✅ 用async/await

---

**下一节**：看看真实案例 → [case.md](./case.md)
