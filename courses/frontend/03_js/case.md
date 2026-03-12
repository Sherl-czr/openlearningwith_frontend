# JavaScript 案例篇

> 光说不练假把式，来看看真实的JS长啥样

## 案例一：点击切换颜色

```html
<button id="btn">点我变色</button>
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

## 案例二：输入验证

```html
<input type="text" id="username" placeholder="请输入用户名">
<p id="msg"></p>

<script>
    const input = document.querySelector('#username');
    const msg = document.querySelector('#msg');

    input.addEventListener('blur', () => {
        const value = input.value.trim();
        
        if (value.length < 3) {
            msg.textContent = '用户名至少3个字符';
            msg.style.color = 'red';
        } else {
            msg.textContent = '✓ 用户名可用';
            msg.style.color = 'green';
        }
    });
</script>
```

## 案例三：Tab切换

```html
<div class="tabs">
    <button class="tab active" data-tab="1">Tab1</button>
    <button class="tab" data-tab="2">Tab2</button>
    <button class="tab" data-tab="3">Tab3</button>
</div>
<div class="content">
    <div class="panel active" id="panel1">内容1</div>
    <div class="panel" id="panel2">内容2</div>
    <div class="panel" id="panel3">内容3</div>
</div>

<script>
    const tabs = document.querySelectorAll('.tab');
    
    tabs.forEach(tab => {
        tab.addEventListener('click', () => {
            // 移除所有active
            tabs.forEach(t => t.classList.remove('active'));
            document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
            
            // 添加当前active
            tab.classList.add('active');
            const tabId = 'panel' + tab.dataset.tab;
            document.querySelector('#' + tabId).classList.add('active');
        });
    });
</script>
```

## 案例四：待办事项

```html
<input type="text" id="todoInput" placeholder="添加待办...">
<button id="addBtn">添加</button>
<ul id="todoList"></ul>

<script>
    const input = document.querySelector('#todoInput');
    const btn = document.querySelector('#addBtn');
    const list = document.querySelector('#todoList');

    // 添加
    btn.addEventListener('click', addTodo);
    input.addEventListener('keypress', (e) => {
        if (e.key === 'Enter') addTodo();
    });

    function addTodo() {
        const text = input.value.trim();
        if (!text) return;
        
        const li = document.createElement('li');
        li.innerHTML = `
            ${text}
            <button class="delete">删除</button>
        `;
        
        // 删除功能
        li.querySelector('.delete').addEventListener('click', () => {
            li.remove();
        });
        
        list.appendChild(li);
        input.value = '';
    }
</script>
```

## 案例五：异步获取数据

```html
<button id="loadBtn">加载数据</button>
<div id="data"></div>

<script>
    const btn = document.querySelector('#loadBtn');
    const container = document.querySelector('#data');

    btn.addEventListener('click', async () => {
        btn.disabled = true;
        btn.textContent = '加载中...';
        
        try {
            // 模拟API调用
            const res = await fetch('https://jsonplaceholder.typicode.com/posts/1');
            const data = await res.json();
            
            container.innerHTML = `
                <h3>${data.title}</h3>
                <p>${data.body}</p>
            `;
        } catch (err) {
            container.textContent = '加载失败：' + err.message;
        } finally {
            btn.disabled = false;
            btn.textContent = '加载数据';
        }
    });
</script>
```

---

## 常用DOM操作汇总

| 操作 | 代码 |
|------|------|
| 获取元素 | document.querySelector('.class') |
| 创建元素 | document.createElement('div') |
| 添加到页面 | parent.appendChild(child) |
| 删除元素 | element.remove() |
| 修改内容 | element.textContent = '新内容' |
| 修改样式 | element.style.color = 'red' |
| 添加class | element.classList.add('active') |

---

**下一步**：来做练习检验一下！→ [exercises](./exercises/)
