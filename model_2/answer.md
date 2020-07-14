> 姓名：赵跃旻
> 手机：13148787915
> 邮箱：ymzhaobth@aliyun.com




# 模块二：ES新特性与TypeScript、JS性能优化

## 简答题

### 一、请说出下列最终的执行结果，并解释为什么。
```javascript
var a = [];
for(var i = 0; i < 10; i++) {
	a[i] = function() {
		console.log(i)
	}
}
a[6]()
```
___

**Answer**:
10
var定义的i为全局变量，for循环后，i已经累加到了10。


### 二、请说出下列最终的执行结果，并解释为什么。
```javascript
var tmp = 123;

if(true) {
	console.log(tmp)
	let tmp
}
```
___

**Answer**:
报错，let创建的tmp存在块级作用域内，且不同于var的定义变量提升，let创建的变量tmp必须先定义后引用，否则报错。

### 三、结合ES6新语法，用最简单的方式找出数组中的最小值。
`var arr = [12, 34, 32, 89, 4]`

___

**Answer**:

```javascript
console.log(arr.sort((a,b) => a - b)[0]);
```

### 四、请详细说明var，let，const三种声明变量的方式之间的差别。

**Answer**:

* var与let都是用来声明变量，而const声明常量。
* var只有函数作用域和全局作用域；
* let有块级作用域；
* 当const声明的是引用类型时，其引用不可变，但内容可变。

### 五、请说出下列代码最终输出的结果，并解释为什么。
```javascript
var a = 10;
var obj = {
	a: 20,
	fn () {
		setTimeout(() => {
			console.log(this.a)
		})
	}
}
obj.fn()
```

___

**Answer**:

20
箭头函数内未定义this；obj.fn()，this指向调用它的对象obj。

### 六、简述symbol类型的用途。

**Answer**:

* 可生成匿名的唯一的值；
* 可用于创建对象属性，该属性不可枚举，无法通过for...in遍历，也无法通过Object.getOwnPropertyNames()获取，
* 可用于创建类的私有属性；

### 七、说说什么是浅拷贝，什么是深拷贝？

**Answer**:

* 对于引用类型数据，对它的浅拷贝是拷贝它的引用，和被拷贝的目标指向同一个数据；
* 深拷贝是将该引用类型数据拷贝，和被拷贝的目标指向不同的数据。
* 这种区别是由于引用类型数据的存储位置决定的。

### 八、请简述TypeScript与JavaScript之间的关系。

**Answer**:

* TypeScript是JavaScript的超集，
* 在JavaScript基础上增添了ES6+的各种特性，
* 添加了类型系统用以弥补JavaScript弱语言的缺陷。

### 九、请谈谈你所认为的TypeScript优缺点

**Answer**:

* 优点：
* 兼容性强，可以最低兼容到ES3；
* 类型系统可以弥补JavaScript弱语言的缺陷；
* 作为一门完整的语言，功能强大，生态健全，应用广，前景好。

* 缺点：
* 相对于JavaScript，多了很多概念，提高了学习成本；
* 对于周期小的项目，起类型系统及配置会增加成本。

### 十、描述引用计数的工作原理和优缺点。

### 十一、描述标记整理算法的工作流程。

### 十二、描述V8中新生代存储区垃圾回收的流程。

### 十三、描述增量标记算法在何时使用及工作原理。