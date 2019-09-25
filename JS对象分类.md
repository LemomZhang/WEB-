## 构造函数

* new X() 自动做了四件事

	1. 自动创建空对象
	2. 自动为空对象关联原型，原型地址为X.prototype
	3. 自动将空对象作为this关键字运行构造函数
	4. 自动return this

* 构造函数X

	1. X函数本身负责给对象本身添加属性
	2. X.prototype对象负责保存对象的公用属性

	```
	funtion Square(width){
		this.width=width
	}
	Square.prototype.getArea=function(){
		return this.width*this.width
	}
	Square.prototype.getLength=function(){
		return this.width*4
	}
	let square = new Square(5)
	```

### 代码规范

* 大小写
	1. 所有构造函数（用于创建对象的函数）首字母大写
	2. 所有被构造出来的对象，首字母小写
* 词性
	1. new后面的函数使用名词形式
		* 如new Person()    new Object()
	2. 其他函数一般用动词开头
		* 如createSquare(5)   createElement('div')

### 原型公式

<span style='color:red'>对象. __ proto __ = 其构造函数.prototype</span>

### 类型与类

* 类型

	类型是JS数据的分类，有7种（4基2空1对象）

* 类

	类是针对于对象的分类，有无数种，如Array,Function,Date,RegExp等

