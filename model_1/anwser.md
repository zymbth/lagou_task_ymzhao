> 姓名：赵跃旻
> 
> 电话：13148787915



# 一、简答题

## 1.

- 10
- for循环体内var声明的变量作用域为全局，执行函数打印i时，i已经累加到了10。

## 2.

- 报错
- let块级作用域使之无法打印全局变量tmp；
- 而let声明的变量不可以先使用再声明。

## 3.

```javascript
console.log(arr.sort((a,b) => a - b)[0]);
```

## 4.

- var与let都是用来声明变量，而const声明常量。
- var只有函数作用域和全局作用域；
- let有块级作用域；
- 当const声明的是引用类型时，其引用不可变，但内容可变。

## 5.

- 20
- 箭头函数内未定义的this；
- obj.fn()，this指向调用它的对象obj。

## 6.

- 可生成匿名的唯一的值；
- 可用于创建对象属性，该属性不可枚举，无法通过for...in遍历，也无法通过Object.getOwnPropertyNames()获取，
- 可用于创建类的私有属性；

## 7.

- 对于引用类型数据，对它的浅拷贝是拷贝它的引用，和被拷贝的目标指向同一个数据；
- 深拷贝是将该引用类型数据拷贝，和被拷贝的目标指向不同的数据。
- 这种区别是由于引用类型数据的存储位置决定的。

## 8.

- JS主线程是单线程，异步是通过将无法立即执行的任务先放一边，先执行能立即执行的任务。
- 异步是通过运行环境的api的异步操作延后部分任务，并按指定的顺序或指定的时间添加到消息队列中等待主线程执行。
- “延后”的任务分为两种，宏任务和微任务。

- Event Loop用于判断消息队列中是否有任务，有则添加到主线程中。

- 宏任务一般是：包括整体代码script，setTimeout，setInterval、I/O、UI render。
- 微任务主要是：Promise、Object.observe、MutationObserver。
- 主线程执行完整体代码script之后，先执行微任务，完毕后执行一个宏任务，之后再执行微任务，再执行一个宏任务，如此循环。

## 9.

```javascript
Promise.resolve('hello')
    .then((res) => res + 'lagou')
    .then((res) => {
        console.log(res += 'I love U');
    })
```
## 10.

- TypeScript是JavaScript的超集，
- 在JavaScript基础上增添了ES6+的各种特性，
- 添加了类型系统用以弥补JavaScript弱语言的缺陷。

## 11.

- 优点：
兼容性强，可以最低兼容到ES3；
类型系统可以弥补JavaScript弱语言的缺陷；
作为一门完整的语言，功能强大，生态健全，应用广，前景好。

- 缺点：
相对于JavaScript，多了很多概念，提高了学习成本；
对于周期小的项目，起类型系统及配置会增加成本。

