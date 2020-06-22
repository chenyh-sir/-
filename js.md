# js

数据类型

Number(整数、小数...)、String (单引号或双引号)、boolean、null、undefined

alert（）在网页弹出消息

var a = 3; 相当于 window.a = 3;

函数调用 function

compile.log()运行打印

定义对象  var person = {

​	name : 'cyh',

...

}

数组声明：var arr = [1,2,3]或者var arr = new Array()

判断数组：Array.isArray(arg)

数组分割：

```
var arr = ['red', 'yellow', 'green'];
arr.join('|')
arr.join(',')
...

```

运行结果：red|yellow|green

数组添加和删除元素：

arr.push(arg)|arr.pop() (对添加/删除数组最后一个元素)

arr.unshift(arg)|arr.shift()  (FIFO)

返回数组长度



数组排序：

arr.sort(arg)   (注意：是根据字符串的ascii比较，故在进行数字排序时需要注意)

如果要实现数字排序需要传递一个函数参数，例如arr.sort(compare1)

```
//升序
function compare1(a,b){
	/*
	if (a<b){
	return -1;
	}else if(a>b){
	return 1;
	}else{
	return 0;
	}
	*/
	return a-b;    //等效于上面代码
}
//降序
function compare1(a,b){
	/*
	if (a<b){
	return 1;
	}else if(a>b){
	return -1;
	}else{
	return 0;
	}
	*/
	return b-a;
}
```

数组操作方法1.concat()   2. slice()    3.splice()

1.数组合并 concat()

返回一个新的数组

arr.concat(arg)

2.数组切割 slice()

返回一个新的数组

arr.slice(1)    返回从第一个数组元素开始到最后一个元素

arr.slice(arg, arg) arg可以是负数，与python类似

3.数组删除、添加、替换

splice(arg1, arg2, arg3)

arg1 表示开始位置

arg2表示删除个数

arg3表示添加的元素

直接对原来数组进行操作

添加：arg2 = 0

替换：即删除再添加

例如：

1.arr.splice(0,1)

2.arr.splice(1,0,'jack')

3.arr.splice(1,1,'mike')









