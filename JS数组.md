## 创建一个数组

* 新建

	```javascript
	let arr = [1,2,3]
	let arr = new Array(1,2,3)
	let arr = new Array(3)
	```

* 通过转化变为数组

	```javascript
	let arr = '1,2,3'.split(',')
	let arr = '123'.split('')
	Array.from('1,2,3') //传的值必须有1,2,3和length等属性名,结果为伪数组,因为返回结果__proto__!==Array.prototype
	```

* 伪数组

	let divList = document.querySelectorAll('div')

	<p style="color:red">伪数组的原型链中并没有数组的原型</p>

* 合并两个数组，得到新的数组

	arr1 . concat(arr2)

* 截取一个数组的一部分

	```javascript
	arr1.slice(1) //从第二个元素开始
	arr1.slice(0) //全部截取
	```

![1569256562469](C:\Users\z8974\AppData\Roaming\Typora\typora-user-images\1569256562469.png)

<p style="color:red">JS只提供浅拷贝</p>

* 删除元素

	arr.shift() //arr被修改，并返回被删元素

* 删除尾部元素

	arr.pop() //arr 被修改，并返回被删元素

* 删除中间的元素

	```javascript
	arr.splice(index,1) //删除index的一个元素
	arr.splice(index,1,'x') //并在删除位置添加'x'
	arr.splice(index,1,'x','y') //并在删除位置添加'x','y'
	```

	![1569347826887](C:\Users\z8974\AppData\Roaming\Typora\typora-user-images\1569347826887.png)

