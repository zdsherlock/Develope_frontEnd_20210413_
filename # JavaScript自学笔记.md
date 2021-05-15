# JavaScript自学笔记

## 数据类型
* 基本类型
```javascript
x = 1; //数值
x = 0.01; //数值包括整数或者实数
实数是有理数和无理数的总称（实数和虚数共同构成复数）
整数 数的集合 包括 正整数 、负整数、零
x = "Hello World"; //文本字符串包含在引号中
x = 'JavaScript'; //单引号也用于界定字符串
x = true; //布尔值
x = false; //另一个布尔值
x = null; //特殊值，意思是没有值
x = undefined; //另一个特殊值
```
* 对象和数组
```javascript
//对象是JavaScript最重要的数据类型
//对象是一个名/值对的集合，或者一个字符串到值得映射
let book = {			  //对象包含在一对大括号内
	topic: "JavaScript", //属性"topic"的值是"JavaScript"
	edition: 7			 //属性"edition"的值是7
};						//对象末尾还有一个大括号
```
* 访问对象的属性
```javascript
//使用.或者[]方位对象的属性
book.topic   //=> "JavaScript"
book["edition"] //=> 7:另一种访问属性值的方式
那么这两种方式间有区别么
book.author = "Flanagan"; //通过赋值创建新属性
book.contents = {};      //是一个没有属性的空对象

//使用?.(ES2020)条件式访问属性
book.contents?.ch01?.sect1 //undefined: book.contets没有ch01这个属性
```
* JavaScript也支持的数组（数值索引的列表）
```javascript
let primes = [2,3,5,7]; //包含4个值得数组，]和[ 是定界符
primes[0];				//=>2: 数组得第一个（索引为0）元素
primes.length			//=>4: 数组包含多少个元素
primes[primes.length-1] //->7: 数组得最后一个元素
primes[4] = 9;			//通过赋值添加新元素
primes[4] = 11;			//或者通过赋值修改已有元素
let empty = [];			//[]是一个没有元素得空数组
emypt.length			//=>0
```
* 数组和对象可以保存数组和对象
```javascript
let points = [			//包含2个属性得对象
	{x:0, y:0},			//每个元素都是一个对象
	{x:1, y:1}
];
let data = {			//包含2个属性的对象
	trial1:[[1,2], [3,4]],//每个属性的值都是一个数组
	trial2:[[2,3], [4,5]]//数组的元素也是数组
}