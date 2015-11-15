#JavaScript101

##0x00什么是Javascript
一种具有c语言语法的Lisp（函数式编程语言的典范）

##0x01应用场景

+ 客户端
+ 服务器端
+ 动态网页

属于一款全栈型的语言

##0x02语言入门

交互式的编程学习网站codecademy

<https://www.codecademy.com/learn/javascript>

廖学峰的js教程
<http://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000>

fenby上的js教程（有邱大师的那本书哦）

<http://www.fenby.com/>

##0x03函数式编程
###函数式编程的特性
函数传入的参数可以是一个方法或者函数，返回值也可以是一个方法或者函数。
###什么时候需要函数式编程？
当重复的代码太多时可以考虑函数式编程的使用。（其实我觉得能用函数式编程的地方都去用。这是一个趋势，代码也简洁，好看。）
###三个高阶函数
**以下内容大多来自廖学峰的网站**
####map
下图来自廖雪峰的网站 很清楚的介绍了map到底是个啥玩意儿

![下图来自廖雪峰的网站](http://www.liaoxuefeng.com/files/attachments/0013879622109990efbf9d781704b02994ba96765595f56000/0)

以下是上图的实现代码：

	function pow(x) {
    	return x * x;
	}

	var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];
	arr.map(pow); // [1, 4, 9, 16, 25, 36, 49, 64, 81]

####reduce

reduce和map类似，遍历传入集合中的每个对象 不同的是reduce把所有的操作值都存起来进行迭代，最后
的返回值只有一个（map是传入多少就传出多少）

就像这样`[x1, x2, x3, x4].reduce(f) = f(f(f(x1, x2), x3), x4)`

比方说对一个Array求和，就可以用reduce实现：

	var arr = [1, 3, 5, 7, 9];
	arr.reduce(function (x, y) {
    	return x + y;
	}); // 25
	
####filter
filter是一个常用的操作，它用于把集合的某些元素过滤掉，然后返回剩下的元素。

和map()类似，集合的filter()也接收一个函数。和map()不同的是，filter()把传入的函数依次作用于每个元素，然后根据返回值是true还是false决定保留还是丢弃该元素。

例如，在一个集合中，删掉偶数，只保留奇数，可以这么写：

	var arr = [1, 2, 4, 5, 6, 9, 10, 15];
	var r = arr.filter(function (x) {
    	return x % 2 !== 0;
	});
	r; // [1, 5, 9, 15]

##0x04常用的js库

这次作业里面需要用到两个库

jQuery [这是中文文档](http://www.css88.com/jqapi-1.9/)   [这是英文文档](http://api.jquery.com/)

underscore.js [这是中文文档](http://www.css88.com/doc/underscore/) [这是英文文档](http://underscorejs.org/)

或者lodash  [这是英文文档](https://lodash.com/docs) 暂时没找到中文文档。

