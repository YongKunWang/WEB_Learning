# 简介

## 课程介绍

```html
/*
    *
    * JavaScript :简称:js
    * js分三个部分:
    * 1. ECMAScript 标准----js的基本的语法
    * 2. DOM------Document Object Model  文档对象模型
    * 3. BOM------Browser Object Model  浏览器对象模型
    *
    *
    * JavaScript是什么？
    * 是一门脚本语言
    * 是一门解释性语言
    * 是一门动态类型的语言
    * 是一门基于对象的语言
    *
    * 编译语言:需要把代码翻译成计算机所认知的二进制语言,才能够执行
    * 脚本语言:不需要编译,直接执行
    * 常见的脚本语言:t-sql,cmd
    *
    * 电脑的硬件---->系统--->客户端的程序--->代码
    * 电脑的硬件---->系统--->浏览器--->js代码
    * js原名不是JavaScript,而是LiveScript
    * js的作用?解决用户和浏览器之间的交互的问题
    * js现在可以做什么?
    *
    * HTML:是标记语言,展示数据的
    * CSS:美化页面
    * JavaScript:用户和浏览器交互,
    * */
```

## js代码编写位置

```html
/*
    *
    * 页面中有什么代码?html--展示内容,css---美化页面的,js---控制页面
    *
    * js的代码可以分三个地方写:
    * 1.在html的文件中,script的标签中写js代码
    * 2.js代码可以在html的标签中写---
    * 3.在js文件中可以写js代码,但是需要在html的页面中引入 script的标签中的src="js的路径"
    *
    * */
```

## 注意问题

```html
//js代码的注意问题
    /*
    *
    *  1.在一对script的标签中有错误的js代码,那么该错误的代码后面的js代码不会执行
    *  2.如果第一对的script标签中有错误,不会影响后面的script标签中的js代码执行
    *  3.script的标签中可以写什么内容 type="text/javascript"是标准写法或者写language="JavaScript"都可以
    *  但是,目前在我们的html页面中,type和language都可以省略,原因:html是遵循h5的标准
    *
    *  4.有可能会出现这种情况:script标签中可能同时出现type和language的写法.
    *
    *
    *  5.script标签在页面中可以出现多对
    *  6.script标签一般是放在body的标签的最后的,有的时候会在head标签中,目前讲课的时候都在body标签的后面(body中的最后)
    *
    *  7.如果script标签是引入外部js文件的作用,那么这对标签中不要写任何的js代码,如果要写,重新写一对script标签,里面写代码
    *
    * */
```

## 变量

```html
    /*
     * 变量:========>
     * 操作的数据都是在内存中操作
     * js中存储数据使用变量的方式(名字,值--->数据)
     * js中声明变量都用var---->存储数据,数据应该有对应的数据类型
     * js中的字符串类型的值都用双引号或者单引号
     *
     * 存储一个数字10
     * 变量的声明及赋值
     * var num=10;
     * 存储一个名字
     * var name='小黑';
     *
     * */

    /*
     *
     * 变量---作用,存储数据的或者是操作数据
     *
     * 变量声明(有var 有变量名字,没有值)
     *
     * 变量初始化(有var 有变量名字,有值)
     *
     * 变量声明的方式:
     * var 变量名字;
     *
     * */

    //var number;//变量的声明,此时是没有赋值的,
    //一次性声明多个变量
    //var x,y,z,k,j;//都是声明,没有赋值

    //变量的初始化(变量声明的同时并且赋值了)
    //   = 的意义:赋值的含义
    //存储一个数字10
    var number = 10;
    //存储一个5
    var number2 = 5;
    //存储一个人的名字
    var name = "小黑";
    //存储真(true)
    var flag = true;
    //存储一个null--->相当于是空
    var nll = null;
    //存储一个对象
    var obj = new Object();
```

```html
    * 变量作用:用来操作数据的(可以存储,可以读取)
    * 变量的声明:没有赋值
    * var 变量名;
    * 变量的初始化:有赋值
    * var 变量名=值;
    *
    * 注意的基本的代码的规范
    * js中声明变量都用var
    * js中的每一行代码结束都应该有分号;(写代码有分号的习惯)
    * js中的大小写是区分的: var N=10; n
    * js中的字符串可以使用单引号,也可以使用双引号,目前我们暂时使用双引号
    *
    * 变量名的注意问题---变量名的命名规范,要遵循驼峰命名法
    * 1.变量的名字要有意义,
    * 2.变量名有一定的规范:一般以字母,$符号,下划线开头,中间或者后面可以有$符号,字母,数字
    * 3.变量名一般都是小写的
    * 4.变量名如果是多个单词,第一个单词的首字母是小写的,后面的所有的单词的首字母都是大写的,这种命名方式称为:驼峰命名法
    * 5.不能使用关键字(系统自带的一些单词,不能使用)
    * 6.不会单词用拼音,拼音也要遵循驼峰命名法
    *
    * var bigNumber=10;
    * */

    //声明变量并初始化---变量的初始化----声明变量赋值
    //声明了一个num的变量存储了一个数字100
    //var num=100;
    //输出这个变量的值
    //alert(num);//弹框
    //浏览器的控制台在浏览器中的开发人员工具中(快捷键:F12)的console的选项中
   // console.log(num);//把内容输出在浏览器的控制台中

    //声明多个变量然后一个一个的赋值
//    var num1,num2,num3;//声明
//    //依次的赋值
//    num1=10;
//    num2=20;
//    num3=30;
    //声明多个变量并且赋值
    //var num1=10,num2=20,num3=30;
//    var num=10;
//    var $break=10;
//    var shuZi=10;
```

### 交换两个数字的三种方式

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>交换数字的三种方式</title>
	<script>
		var a = 10;
		var b = 100;
		var temp = a;
		a = b; 
		b = temp;
		console.log(a,b);

		var a2 = 10;
		var b2 = 100;
		a2 = a2 + b2;
		b2 = a2 - b2;
		a2 = a2 - b2;
		console.log(a2,b2);

		var a3 = 10;
		var b3 = 100;
		// a = a^b;
		// a = a^b;
		// b = a^a;
		a3 = a3^b3;   
		b3 = a3^b3;
		a3 = a3^b3;
		console.log(a3,b3);
	</script>
</head>
<body>
	
</body>
</html>
```

## 数据类型

```html
number---数字类型（整数和小数）
string---字符串类型
boolean---布尔值
null---空类型（只有一个值）
undefined---未定义值
		变量声明了，为赋值
		函数没有明确的返回值，如果接收了
变量类型为undefined类型的值和一个数字进行计算，结果为Nan
object

获取变量类型：
typeof(变量名)
```

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数据类型</title>
	<script>
		var num = 10;
		var num2 = 10.2;
		var str = "10";
		var str2 = '10';
		var flag = true;
		var nul = null;
		var a;
		var b = a + 10;
		var obj = new Object();
		console.log(typeof num); //number
		console.log(typeof num2); //number
		console.log(typeof str);  //string
		console.log(typeof str2); //string
		console.log(typeof flag); //boolean
		console.log(String(nul)); //null 字符串为空
		console.log(typeof nul); //object类型
		console.log(typeof a);   //undefined
		console.log(b);          //NaN
		console.log(typeof obj); //object
	</script>
</head>
<body>
	
</body>
</html>
```

## 数字

数字类型：整数和小数

```js
  /*
    * js中可以表示哪些进制
    * var num=10;//十进制
    * var num2=012;//八进制
    * var num3=0x123;//十六进制
    * */
    //数字类型有范围: 最小值和最大值
//    console.log(Number.MAX_VALUE);//数字的最大值
//    console.log(Number.MIN_VALUE);//数字的最小值

//总结:
    /*
    *
    * 数字类型:number类型
    * 无论是整数还是小数都是数字类型
    * 不要用小数验证小数
    * 不要使用NaN判断是不是NaN，应该使用isNaN(值或者是变量)
    * 想要表示十进制:就是正常的数字
    * 想要表示八进制:以0开头
    * 想要表示十六进制:0x开头
    *
    *
    *
    * */
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数字类型</title>
	<script>
		var a = 10;
		var a1 = 010;
		var a2 = 0x10;
		console.log(a); // 10
		console.log(a1); // 8
		console.log(a2);  // 16

		var a3;
		var b = a3 + 10;
		console.log(b); //NaN
		console.log(isNaN(b));//true

		var d = 0.1;
		var c = 0.1;
		console.log(d == c); //true
		console.log(Number.MAX_VALUE);
		console.log(Number.MIN_VALUE);
	</script>

</head>
<body>
	
</body>
</html>
```

## 字符串类型

```js
   //var str="10";//字符串
    //var str2='20';//字符串

    //字符串可以使用单引号,也可以使用双引号

    //字符串的长度如何获取? 变量名.length

    //    var str="what are you no sha lei";
    //    //字符串的个数有多少个?这个字符串的长度是多少
    //    console.log(str.length);
    //
    //    var str1="fdshfjworwoijpfskj;akjfpojfiwnmoiwajdoiwajiwaewowj";
    //    console.log(str1.length);

    //html中的转义符: <  &lt; > &gt; 空格: &nbsp;
    //js中的字符串里也有转义符

    //tab键----水平制表符
    //    console.log("哈哈\\嘎嘎");
    //    console.log("哈哈\t嘎嘎");
    //    console.log("哈哈\"嘎嘎");
    //
    //
    //    console.log('哈哈\'嘎嘎');


    //字符串的拼接: 使用+可以把多个字符串放在一起形成一个字符串
    //只要有一个是字符串,其他的是数字,那么结果也是拼接,不是相加
    //如果有一个是字符串,另一个不是字符串,使用- 号,此时会发生计算
    //    var str1="您好";
    //    var str2="我好";
    //    console.log(str1+str2);

    //console.log("哈哈"+"嘎嘎"+"嘿嘿");
    //    var str1="10";
    //    var str2="20";
    //    console.log(str1+str2);

    //    var str1="10";
    //    var str2=20;
    //    console.log(str1+str2);


//    var str1 = "10";
//    var str2 = 5;
//    //浏览器帮助我们自动的把字符串类型转成了数字类型,这种方式叫:隐式转换
//    console.log(str1-str2);

//    var str1="10";
//    var str2=5;
//    console.log(str1*str2);

```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>字符串类型</title>
	<script>
		var str = '10';
		var str_length = str.length;
		console.log(str_length);
		console.log("&lt;");
		console.log("&gt;");
		var str1 = "Hello ";
		var str2 = "world!";
		console.log(str1 + str2);

		var str3 = '10';
		var str4 = '5';
		var str5 = str3 - str4;
		console.log(typeof str5); //number

	</script>
</head>
<body>
	
</body>
</html>
```

## 布尔类型

```js
    //布尔类型:的值有两个,一个是true(真),一个是false(假)

//    var flag=1;
//    console.log(flag);

//    var fdf=null;
//
//    var num=0;
```

## 类型转换

```js
    //类型转换


    //其他类型转数字类型:三种方式:
    //1.parseInt();//转整数

    //    console.log(parseInt("10"));//10
    //    console.log(parseInt("10afrswfdsf"));//10
    //    console.log(parseInt("g10"));//NaN
    //    console.log(parseInt("1fds0"));//1
    //    console.log(parseInt("10.98"));//10
    //    console.log(parseInt("10.98fdsfd"));//10

    //2.parseFloat()//转小数

    //    console.log(parseFloat("10"));//10
    //    console.log(parseFloat("10afrswfdsf"));//10
    //    console.log(parseFloat("g10"));//NaN
    //    console.log(parseFloat("1fds0"));//1
    //    console.log(parseFloat("10.98"));//10.98
    //    console.log(parseFloat("10.98fdsfd"));//10.98
    //3.Number();//转数字
//    console.log(Number("10"));//10
//    console.log(Number("10afrswfdsf"));//NaN
//    console.log(Number("g10"));//NaN
//    console.log(Number("1fds0"));//NaN
//    console.log(Number("10.98"));//10.98
//    console.log(Number("10.98fdsfd"));//NaN

    //总结:想要转整数用parseInt(),想要转小数用parseFloat()
    //想要转数字:Number();要比上面的两种方式严格

    //其他类型转字符串类型
    //1    .toString()

//    var num=10;
//    console.log(num.toString());//字符串类型
//    //2  String();
//
//    var num1=20;
//    console.log(String(num1));

    //如果变量有意义调用.toString()使用转换
    //如果变量没有意义使用String()转换

//    var num2;
//    console.log(num2.toString());
//    var num3=null;
//    console.log(num3.toString());

    //这个可以
//    var num2;
//    console.log(String(num2));
//    var num3=null;
//    console.log(String(num3));


    //其他类型转布尔类型

    //1  Boolean(值);
//
//    console.log(Boolean(1));//true
//    console.log(Boolean(0));//false
//    console.log(Boolean(11));//true
//    console.log(Boolean(-10));//true
//    console.log(Boolean("哈哈"));//true
//    console.log(Boolean(""));//false
//    console.log(Boolean(null));//false
//    console.log(Boolean(undefined));//false


//    var str=10;
//    console.log(+str);

```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>类型转换</title>
	<script>
		console.log(parseInt(10.98));
		console.log(parseInt("101ddd"));
		console.log(parseInt("ds11"));
		console.log(parseFloat(10.98));
		console.log(parseFloat("10.98"));
		console.log(parseFloat("a10.98"));
		console.log(Number(10.98));
		console.log(Number("a10.98"));

		var a = 10;
		console.log(a.toString());
		var b = 20;
		console.log(String(a));

		console.log(Boolean(1));//true
	   	console.log(Boolean(0));//false
	   	console.log(Boolean(11));//true
	   	console.log(Boolean(-10));//true
	   	console.log(Boolean("哈哈"));//true
	   	console.log(Boolean(""));//false
	   	console.log(Boolean(null));//false
	   	console.log(Boolean(undefined));//false
	</script>
</head>
<body>
	
</body>
</html>
```

## 操作符

```js
    /*
     *
     * 操作符:一些符号-----用来计算
     *
     * 算数运算符:  +  -  * /(真正的除法) %
     * 算数运算表达式:由算数运算符连接起来的表达式
     * 一元运算符: 这个操作符只需要一个操作数就可以运算的符号  ++  --
     * 二元运算符: 这个操作符需要两个操作数就可以运算,
     * 三元运算符: -----不讲,明天讲
     * 复合运算符: +=  -=  *= /= %=
     * 复合运算表达式:由复合运算符连接起来的表达式
     *
     * var num=10;
     * num+=10;------>就是:num=num+10;
     * console.log(num);20
     *
     *
     * 关系运算符: >  <  >=  <=  ==不严格的（只判断值） ===严格的（判断类型和值） !=不严格的不等 !==严格的不等
     * 关系运算表达式:由关系运算符连接起来的表达式
     * 关系运算表达式的结果是布尔类型
     * 逻辑运算符:
     * &&---逻辑与--并且
     * ||---逻辑或---或者
     * !---逻辑非---取反--取非
     * 逻辑运算表达式:由逻辑运算符连接起来的表达式
     * 表达式1&&表达式2
     * 如果有一个为false,整个的结果就是false
     * 表达式1||表达式2
     * 如果有一个为true,整个的结果为true
     * !表达式1
     * 表达式1的结果是true,整个结果为false
     * 表达式1的结果是false,整个结果为true
     *
     * 赋值运算符:  =
     *
     *
     *
     *
     * */
    //    var num1=10;
    //    var num2=20;
    //
    //    console.log(num1==num2&&5>6);

    //    var num=20;
    //    console.log(num>10||5<0);

    //    var flag=false;
    //    console.log(!flag);

    //    var num=10;
    //    var sum=(num+10)*5;
    //    console.log(sum);


    //    var result = (4 >= 6 || '人' != '狗' && !(12 * 2 == 144) && true);
    //    console.log(result);

//
//    var num = 10;
//
//    var result2 =( 5 == num / 2 && (2 + 2 * num).toString() === '22');
//    console.log(result2);


    //    var num=20;
    //    var result=num/3;//num变量与3取余--->10/3的余数
    //    console.log(parseInt(result));


    //    var num=20;
    //    var result=num%3;//num变量与3取余--->10/3的余数
    //    console.log(result);


    //    var num=10;
    //    var sum=(num+10)+10;

    //    var num = 20;
    //    num %= 5;
    //    //    num=num-5;
    //    console.log(num);

    //    var str="5";
    //    var num=5;
    //    console.log(str===num); //false
    //    var str="5";
    //    var num=5;
    //    console.log(str==num); //true

    //    console.log(5>10);//false
    //    console.log(5>=5);//true
    //    console.log(5>3);//true
    //    console.log(5==10);//false



    //字面量: 把一个值直接赋值给一个变量

    //声明变量并初始化
//    var num=10;
//
//    var flag=true;
//
//    var str="哈哈哈";
//
//    var y=10;
//    var n=y;
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>操作符</title>
	<script>
		var a = 10;
		var b = 3;
		console.log(parseInt(a/b)); //真正的除法
		console.log(a%b);

		var str = "10";
		var str2 = 10;
		console.log(str == str2); // true
		console.log(str === str2);//false
	</script>
</head>
<body>
	
</body>
</html>
```



## 常识

```HTML
   /*
    * 编程思想:
    * 面向过程:凡事亲力亲为,所有的事情的过程都要清楚,注重的是过程
    * 面向对象:提出需求,找到对象,对象解决这个问题,我们要结果,注重的是结果
    *
    * 面向对象的特性:封装,继承,多态,(抽象性)
    *
    * JS是一门什么样的语言?
    * 是一门解释性的语言
    * 是一门脚本语言
    * 是一门弱类型的语言
    * 是一门基于对象的语言
    * 是一门动态类型的语言
    *
    * 对象:有属性和方法,具体特指的某个事物
    * 对象:js中就是一组无序的属性的集合
    * 属性----特征
    * 方法----行为
    * 创建的对象的方式:
    * 1.通过调用系统的构造函数创建对象 new Object()
    * var obj1=new Object();
    * 2.自定义构造函数创建对象
    * var obj2=new 自定义构造函数();
    * 3.字面量的方式创建对象
    * var obj3={};
    * 变量 instanceof 对象------->布尔类型,判断这个变量是不是这个类型的
    *
    * JSON格式的数据,都是键值对,成对的数据
    * var obj={
    *   name:"小明"
    * };
    * var json={
    *   "name":"小明"
    * };
    *
    * json的数据实际上就是格式化后的一组字符串的数据
    *
    * 对象设置属性的值的写法
    * 对象.属性名字=值;----点语法
    * 对象["属性的名字"]=值;-----
    *
    * 对象获取属性的值的写法
    * 对象.属性
    * 对象["属性"]
    *
    * 遍历对象
    * for(var key in 对象){   key---是一个变量,这个变量中存储的是遍历的对象的属性的名字
    *
    * }
    *
    * 原始数据类型:number,string,boolean,null,undefined,object
    * 基本类型(简单类型,值类型):number,string,boolean
    * 复杂类型(引用类型):object
    * 空类型:undefined,null
    *
    * 基本类型的值在栈上
    * 复杂类型的对象在堆上,地址(引用)在栈上
    *
    * 值类型之间传递的是值
    * 引用类型之间传递的是引用(地址)
    *
    *
    * 对象分三种:内置对象,自定义对象,浏览器对象
    * 内置对象:系统提供的
    * 自定义对象：自己写的
    * 浏览器对象:浏览器的
    *
    * Math 是一个对象,但是不是一个函数
    * Math对象下的属性和方法都是静态
    *
    * 方法:
    * Math.ceil()---向上取整
    * Math.floor()---向下取整
    * Math.Pi----圆周率的值
    * Math.Max()---一组数字中的最大值
    * Math.Min()---一组数字中的最小值
    * Math.abs()----绝对值
    * Math.random---随机数字
    * Math.sqrt()----开平方
    * Math.pow()----一个数字的多少次幂
    *
    *  new 的执行过程:----->new的时候，系统做了什么事?
    *  1. 开辟空间,存储创建的新的对象
    *  2. 把this设置为当前的对象
    *  3. 设置属性和方法的值
    *  4. 返回当前的新的对象
    */
```

# 流程控制

## ++ -- 的前后区分

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>自加自减运算符</title>
	<script>
		var a = 10;
		var b = a ++ + 1;
		console.log(a); //11
		console.log(b); //11

		var c = 10;
		var d = ++ c + 1;
		console.log(c); //11
		console.log(d); //12
	</script>
</head>
<body>
	
</body>
</html>
```

## if循环

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    /*
    *
    * if语句:主要是判断
    * 语法:
    * if(表达式){
    *   代码块
    * }
    *
    * 执行过程:
    * 先判断表达式的结果是true还是false,如果是true则执行代码块,如果是false,大括号中的代码是不执行的
    *
    * 例子:
    * 1.如果8大于6,请输出8,如果一个数字大于另一个数字则输出大的数字
    * 2.问:小苏的年龄是否大于18岁,如果是成年的,则提示,可以看电影了
    *
    *
    * */
//    if(8>6){
//      console.log(8);
//    }
    //例子1:
//    var num1=10;
//    var num2=100;
//    if(num1>num2){
//      console.log(num1);
//    }
//    console.log("我执行了");

    //例子2
    var age=19;
    if(age>=18){
      console.log("可以看电影了,嘿嘿...");
    }
    //例子3:
    //问小杨帅不帅,则输出真的好帅
    var str="帅";
    if(str=="帅"){
      console.log("真的好帅");
    }


  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    /*
     *
     * if-else 语句
     * 两个分支,只能执行一个分支
     *
     * if-else语句的语法:
     *
     * if(表达式){
     *   代码1
     * }else{
     *   代码2
     * }
     * 执行过程:
     * 如果表达式的结果是true则执行代码1,如果表达式的结果是false,则执行代码2
     *
     *
     * */

    //例子:问；小苏的年龄是否是成年人,如果是成年人则提示,可以看电影,否则；回家写作业区

    //定义变量,并初始化
//    var age = 100;
//    //判断
//    if (age >= 18) {
//      console.log("可以看电影了,嘎嘎...");
//    } else {
//      console.log("看什么看,回家写作业去");
//    }


    //提示用户请输入年龄----
//    var age=prompt("请您输入您的年龄");//弹框---并且有输入,输入的内容在age变量中
//    console.log(age);//最终的结果是字符串的类型



    //案例1:
//    var age = parseInt(prompt("请您输入年龄"));
//    //判断
//    if (age >= 18) {
//      console.log("可以看电影了,嘎嘎...");
//    } else {
//      console.log("看什么看,回家写作业去");
//    }

    //练习1:找到两个数字中的最大值
    var num1=10;
    var num2=20;
    if(num1>num2){
      console.log(num1);
    }else{
      console.log(num2);
    }

    //练习2:判断这个数字是奇数还是偶数

    var number=parseInt(prompt("请输入一个数字"));
    if(number%2==0){
      console.log("偶数");
    }else{
      console.log("奇数");
    }



  </script>
</head>
<body>


</body>
</html>
```

输入数字：`prompt();`字符串形式！

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>if循环</title>
	<script>
		var a = 10;
		var b = 21;
		if(a > b)
			console.log(a);
		else
			console.log(b);

		var age = prompt("请输入您的年龄：");
		console.log(age);
		if(age > 18)
			console.log("可以看电影了，咯咯。。。");
		else
			console.log("看什么看，快去写作业吧。。。");
		var num = parseInt(prompt("请输入一个数字："));
		console.log(num);
		console.log(a%2);
		if(num % 2)
			console.log("您输入的数为奇数");
		else
			console.log("您输入的数为偶数");

	</script>
</head>
<body>
	
</body>
</html>
```

## 三元表达式

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    //获取两个数字中的最大值
    //if-else语句
    //    var num1 = 10;
    //    var num2 = 100;
    //    if (num1 > num2) {
    //      console.log(num1);
    //    } else {
    //      console.log(num2);
    //    }

    //两个分支,最终的结果是两个分支中的一个,像这种情况可以使用三元表达式

    /*
     * 三元表达式
     * 运算符号:  ?  :
     *
     * 语法:
     *  var 变量=表达式1?表达式2:表达式3;
     *  执行过程:
     *  表达式1的结果是true还是false,如果是true则执行表达式2,然后把结果给变量
     *  如果表达式1的结果是false,则执行表达式3,把结果给变量
     *
     *
     *
     * */

    //两个数字中的最大值
    var x = 10;
    var y = 20;
    var result1 = x > y ? x : y;
    console.log(result1);

    //显示成年还是未成年
    var age = 10;
    var result2 = age >= 18 ? "成年了" : "未成年";
    console.log(result2);

    //总结:大多数情况,使用if-else的语句都可以用三元表达式的方式来表示


  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		var score = Number(prompt("请输入你的成绩："));
		if(!isNaN(score)){
			if(score > 90 && score <= 100)
				console.log("A Class...");
			else if(score > 80 && score <= 90)
				console.log("B Class...");
			else if(score > 70 && score <= 80)
				console.log("C Class...");
			else if(score > 60 && score <= 70)
				console.log("D Class...");
			else
				console.log("E Class...");
		}
		else
			console.log("你输入的成绩有错误...");
	</script>
</head>
<body>
	
</body>
</html>
```

## switch case

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    /*
     * switch-case语句---分支语句---多分支语句
     * 语法:
     * switch(表达式){
     *  case 值1:代码1;break;
     *  case 值2:代码2;break;
     *  case 值3:代码3;break;
     *  case 值4:代码4;break;
     *  ...多个case
     *  default:代码5;
     *
     * }
     *
     * 注意问题:
     * default后面的break是可以省略的
     * default也可以省略
     *
     * switch-case 语句中和case后面的值比较的时候使用的是严格的模式
     * break是可以省略
     *
     *
     * 执行过程:
     * 获取表达式的值,和值1比较,如果一样,则执行代码1,遇到break则跳出整个的语句,后面代码不执行
     * 如果表达式的值和值1不一样,则和值2比较,如果相同则执行代码2,遇到break则跳出
     * 否则和值3比较,相同则执行代码3,遇到break,跳出,否则和值4比较,相同则执行代码4,遇到break则跳出,否则直接执行代码5
     *
     *
     *
     *
     *
     *
     * */

    //例子:获取一个人的成绩的级别,如果是A级则显示90到100直接的分数
    /*
     * 如果是B级则显示80到90分
     * 如果是C级则显示70到80之间分数
     //     * 如果是D级则显示60到70分之间
     //     * 否则显示0到59之间
     //     * */
    //    var jiBie = "E";
    //    switch (jiBie) {
    //      case "A":
    //        console.log("90到100之间");
    //        break;
    //      case "B":
    //        console.log("80到90之间");
    //        break;
    //      case "C":
    //        console.log("70到80之间");
    //        break;
    //      case "D":
    //        console.log("60到70之间");
    //        break;
    //      default :
    //        console.log("0到59之间");
    //    }


    //注意问题

//    var num = "10";//字符串
//   // console.log("10"===10);//true还是false
//    switch (num) {
//      case 10:
//        console.log("数字的10");
//        break;
//      case "10":
//        console.log("字符串的10");
//        break;
//    }


    //根据月份显示对应的天数
    //1,3,5,7,8,10,12 ---31天
    //2----28天
    //4,6,9,11----30
//    var month=parseInt(prompt("请输入月份"));
//    switch (month){
//      case 1:console.log("31天");break;
//      case 2:console.log("28天");break;
//      case 3:console.log("31天");break;
//      case 4:console.log("30天");break;
//      case 5:console.log("31天");break;
//      case 6:console.log("30天");break;
//      case 7:console.log("31天");break;
//      case 8:console.log("31天");break;
//      case 9:console.log("30天");break;
//      case 10:console.log("31天");break;
//      case 11:console.log("30天");break;
//      case 12:console.log("31天");break;
//
//    }



//
//    var month=parseInt(prompt("请输入月份"));
//    switch (month){
//      case 1:
//      case 3:
//      case 5:
//      case 7:
//      case 8:
//      case 10:
//      case 12:console.log("31天");break;
//      case 4:
//      case 6:
//      case 9:
//      case 11:console.log("30天");break;
//      case 2:console.log("28天");break;
//    }


    //练习:根据数字显示对应的星期
//    var num=parseInt(prompt("请输入一个星期的数字"));
//    switch (num){
//      case 1:console.log("星期一");break;
//      case 2:console.log("星期二");break;
//      case 3:console.log("星期三");break;
//      case 4:console.log("星期四");break;
//      case 5:console.log("星期五");break;
//      case 6:console.log("星期六");break;
//      case 7:console.log("星期日");break;
//      default:console.log("输入错误");
//    }


  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>switchcase练习</title>
	<script>
		var score = Number(prompt("请输入你的成绩："));
		if(!isNaN(score))
			switch(score){
				case score > 90 && score <= 100 :
					console.log("A Class...");
					break;
				case score > 80 && score <= 90 :
					console.log("A Class...");
					break;
				case score > 70 && score <= 80 :
					console.log("A Class...");
					break;
				case score > 60 && score <= 70 :
					console.log("A Class...");
					break;	
				default:
					console.log("D Class...");
					break;
			}
		else
			console.log("输入成绩有错误，请再次输入...");
	</script>
</head>
<body>
	
</body>
</html>
```

## 循环

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    //循环:一件事不停的或者是重复的做
    //循环要有结束的条件,循环还应该有计数器(记录循环的次数的)

    //while循环
    /*
    * while循环语法:
    *
    * 计数器
    * var 变量=0;
    * while(循环的条件){
    *   循环体;
    *   计数器++;
    *
    * }
    *
    * 执行过程:
    * 先判断条件是否成立,(条件的结果是true还是false),如果是false,那么循环的代码(while的大括号中的代码都不执行),如果是true,那么先执行循环体,然后执行计数器,然后,直接去--->循环的条件,再次判断是否成立,成立则继续执行循环体,否则跳出循环,执行完循环体之后,计数器加1,然后再去循环的条件,判断,成立则循环,否则跳出循环
    *
    * var i=0;
    * while(i<20){
    * 循环体
    * i++;
    * }
    *
    *
    *
    * */

    //请输出10次:哈哈,我又变帅了
//    var i=0;//计数器
//    while(i<10){
//      console.log("哈哈,我又变帅了"+(i+1));
//      i++;//记录次数
//    }


//    var i=0;//计数器
//    while(i<100){
//      console.log("哈哈,我又变帅了"+(i+1));
//      i++;//记录次数
//    }


    //练习:计算1-100之间所有数字的和

    var sum=0;//存储最终的和
    var i=1;//计数器
    while(i<=100){
      //sum=sum+i;//不停的计算数字的和
      sum+=i;
      i++;
    }
    console.log("和为:"+sum);


//    var sum=0;//存储最终的和
//    var i=0;//计数器
//    while(i<=5){
//      //sum=sum+i;//不停的计算数字的和
//      sum+=i;
//      i++;
//    }
//    console.log("和为:"+sum);

  </script>
</head>
<body>
</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>while练习</title>
	<script>
		//求6的阶乘
		var num = 6;
		var sum = 1;
		while(num > 0){
			sum *= num --;
		}
		console.log(sum);

		//求100以内所有偶数的和
		var num1 = 0;
		var sum1 = 0;
		while(num1 <= 100){
			if(num1 % 2 == 0)
				sum1 += num1;
			num1 ++;
		}
		console.log(sum1);
	</script>
</head>
<body>
	
</body>
</html>
```

## do while 循环

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    /*
     *
     * do-while循环
     *
     * 语法:
     *
     * do{
     *     循环体
     * }while(条件);
     *
     * 执行过程:
     * 先执行一次循环体,然后判断条件是否成立,不成立,则跳出循环,成立则执行循环体,然后再判断条件是否成立,成立则继续循环,否则跳出.....
     *
     * */


    //例子:
    //输出:哈哈,我又变帅了..10次

    //    var i=0;//计数器
    //    do{
    //      console.log("哈哈,我又变帅了");
    //      i++;
    //    }while(i<10);

    //例子:问用户:您觉得我帅吗?提示用户请输入y/n ,如果n就一直问,我帅不帅,如果用户输入的y,则结束,并提示用户,您真有眼光


    //    do {
    //      //把用户输入的结果存储到result变量中
    //      var result = prompt("您觉得我帅吗?y/n");
    //    } while (result != "y");
    //    console.log("您真有眼光");


    //练习:求100以内所有3的倍数的和

    //    var i = 1;
    //    var sum = 0;
    //    while (i <= 100) {
    //      if (i % 3 == 0) {
    //        sum += i;
    //      }
    //      i++;
    //    }
    //    console.log(sum);//1683

    var i = 1;
    var sum = 0;
    do {
      if (i % 3 == 0) {
        sum += i;
      }
      i++;
    } while (i <= 100);
    console.log(sum);


  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>dowhile循环</title>
	<script>
		do {
			var result = prompt("您觉得我帅吗？");
		} while(result != "y");
		console.log("您真有眼光！！！");

		var num = 1;
		var sum = 0;
		do {
			if(num %3 == 0)
				sum += num;
			num ++;
		} while(num <= 100);
		console.log(sum);
	</script>
</head>
<body>

</body>
</html>
```

## 复习

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    /*
     *
     * 一元运算符:  ++  --
     *
     * 如果不参与运算, ++在前面还是在后面结果都是一样的  +1
     * 如果不参与运算, --在前面还是在后面结果都是一样的  -1
     *
     * var num=10;
     * num++;   后+
     * ++num;   前+
     * 无论是前+还是后+只要参与运算,结果可能就不太一样
     * 如:
     *  var num=10;
     *  var sum= num++ +10;
     *  ++在后面的时候,先参与运算,然后自身加1
     *  var num=10;
     *  var sum=++num +10;
     *  ++在前面的时候,先自身加1,然后再参与运算
     *
     *  流程控制: 代码的执行过程
     *  1. 顺序结构:代码的执行的顺序,从上到下,从左到右(不严谨)
     *  2. 分支结构: if,if-else ,if-esle if,switch-case ,三元表达式
     *  3. 循环结构:while 循环,do-while,for循环  for-in循环
     *
     *  总结分支:如果只有一个分支,就用if
     *  如果有两个分支,就用if-else
     *  如果多个分支,一般是范围的,推荐使用if-else if
     *  如果多个分支,一般是具体的值,推荐使用switch-case
     *
     *
     *
     *
     *  总结循环:
     *  while:先判断后循环,有可能一次循环都不执行
     *  do-while:至少执行一次循环体,再判断
     *  for循环:知道了循环的次数,推荐使用for循环
     *
     *
     *  调试:是为了找代码的错误和问题所在,
     *  断点,不加断点,就不方便调试
     *
     *
     *
     *
     *
     *
     *
     *
     *
     *
     *
     *
     *
     *
     * */



    //本金10000元存入银行，年利率是千分之三，每过1年，将本金和利息相加作为新的本金。计算5年后，获得的本金是多少？

//    var money = 10000;//本金
//    var rate=0.003;
//    for(var i=0;i<5;i++){
//      //money=money+money*rate;
//      money+=money*rate;
//    }
//    console.log(money);








    //有个人想知道，一年之内一对兔子能繁殖多少对？于是就筑了一道围墙把一对兔子关在里面。已知一对兔子每个月可以生一对小兔子，而一对兔子从出生后第3个月起每月生一对小兔子。假如一年内没有发生死亡现象，那么，一对兔子一年内（12个月）能繁殖成多少对？（兔子的规律为数列，1，1，2，3，5，8，13，21）

    //每个月的值 就是前两个月的和

//    var num1=1;//第一个月
//    var num2=1;//第二个月
//    var sum=num1+num2;//第三个月
//
//
//    var num1=num2;//第二个月
//    var num2=sum;//第三个月
//    sum=num1+num2;//第四个月
//
//
//    var num1=num2;//第三个月
//    var num2=sum;//第四个月
//    var sum=num1+num2;

    var num1=1;//第一个月
    var num2=1;//第二个月
    var sum=0;
    //i=3是从第三个月开始
    for(var i=3;i<=12;i++){
      sum=num1+num2;
      num1=num2;
      num2=sum;
    }
    console.log(sum);
    //求斐波那契数列数列第12个月的值









    //卡卡西  佐助  大蛇丸 鸣人  雏田

    //练习: ++ 和 --

    //    var a = 1;
    //
    //    var b = ++a + ++a;
    //
    //    console.log(b);


    //    var a = 1;
    //
    //    var b = a++ + ++a;
    //    console.log(b);


    //    var a = 1;
    //
    //    var b = a++ + a++;
    //    console.log(b);


    //    var a = 1;
    //
    //    var b = ++a + a++;
    //    console.log(b);


    //    var a=1;
    //    var b=++a + ++a+a++ + ++a;

    //  var sum=0;
    //  for(var i=1;i<=100&&i%2==0;i++){
    //    sum+=i;
    //  }
    //  console.log(sum);


    //    var num = 10;
    //    switch (num) {
    //      case 1:
    //      case 2:console.log("嘎嘎");break;}


    //    var i=1;
    //    j=i++ + i++;
    //    j=1+ 2++;
    //    console.log(j);

  </script>
</head>
<body>


</body>
</html>
```

## break和continue

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>break和cuntinue练习</title>
	<script>
		//跳出当前循环
		for (var i = 0; i < 10; i++) {
			while(true){
				console.log(i);
				break;
			}
		}

		//找见100·200之间第一个被7整除的数字
		for(var i = 100; i <= 200; i++){
			if( i % 7 == 0){
				console.log(i);
				break;
			}
		}

		//直接开始下一次循环
		//案例:求100-200之间所有的奇数的和（用continue）
		console.log('---');
		var sum = 0;
		for(var i = 100; i <= 200; i ++){
			if(i % 2 == 0){
				continue;
			}
			sum += i;
		}
		console.log(sum);

		//求整数100~300之间额累加值，但要求跳过所有各位为3的数字
		sum = 0;
		for(var i = 100; i <= 200; i ++){
			if(i % 10 == 3){
				continue;
			}
			sum += i;
		}
		console.log(sum);
	</script>
</head>
<body>
	
</body>
</html>
```

## 数组

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    //数组:一组有序的数据
    //数组的作用:可以一次性存储多个数据
    //数组的定义:
    /*
    *
    * 1. 通过构造函数创建数组
    * 语法:
    * var 数组名=new Array();
    * var array=new Array();//定义了一个数组
    * 数组的名字如果直接输出,那么直接就可以把数组中的数据显示出来,如果没有数据,就看不到数据
    *
    * var 数组名=new Array(长度);
    * 如果数组中没有数据,但是有长度---,数组中的每个值就是undefined
    * 构造函数的方式创建数组的时候,如果在Array(一个数字)--->数组的长度(数组元素的个数)
    * 如果在Array(多个值);这个数组中就有数据了,数组的长度就是这些数据的个数
    *
    *
    * 2. 通过字面量的方式创建数组
    *
    * var 数组名=[];//空数组
    * var array=[];
    *
    *
    * 无论是构造函数的方式还是字面量的方式,定义的数组,如果有长度,那么默认是undefined
    *
    * 数组:一组有序的数据
    * 数组元素:数组中存储的每个数据,都可以叫数组的元素,比如:存储了3个数据,数组中3个元素
    * 数组长度:就是数组的元素的个数,比如有3个元素,就说,这个数组的长度是3
    * 数组索引(下标):用来存储或者访问数组中的数据的,索引从0开始,到长度减1结束
    * 数组的索引和数组的长度的关系:长度减1就是最大的索引值
    *
    * 如何设置数组中某个位置的值
    * 数组名[下标]=值;
    * arr[3]=100;
    * 如何获取数组中某个位置的值
    * var result=数组名[下标];
    * console.log(result);
    *
    *
    *
    *
    * */

    //通过构造函数的方式定义一个数组
//    var array=new Array(5);//没有数据,空数组
//    console.log(array);
    //alert(array);

    //就是一个数组---->字面量的方式
//    var arr=[];
//    console.log(arr);


//    var arr1=new Array();//构造函数的方式---空数组
//    var arr2=new Array(5);//构造函数的方式定义了一个数组,数组中有5个元素,数组长度是5,每个数据是undefined
//
//    var arr3=new Array(10,20,1000,40,50,60);
//    console.log(arr3);


//    var arr=new Array(10,20,30,40,100);
//    //console.log(arr[4]);//获取
//    //设置
//    arr[3]=1000;
//    console.log(arr);


    //字面量的方式更简单

//    var arr=[10,20,30,40,50,60,70,80,10,20,3043,5];//空数组
//    console.log(arr.length);


    /*
    *
    * 请输入班级人数,根据班级人数,输入每个学生的数学成绩,求总成绩,求平均成绩,求最高分,求最低分
    *
    *
    *
    * */
  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    //var arr=[10,2,3,4,1];
    //长度:5
    //索引:0-4
    //console.log(arr);
    //alert(arr);

    //数组中存储的数据类型一定是一样的吗? 类型可以不一样
//    var arr=[10,"哈哈",true,null,undefined,new Object()];
//    console.log(arr);
    //数组的长度是不是可以改变呢?
    var arr=[];
    //通过索引来设置数组中的元素的值
    arr[0]=10;
    arr[1]=20;
    console.log(arr.length);
    //获取元素的值,通过索引的方式
    console.log(arr[2]);
  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    /*
    *
    * 数组:存储一组有序的数据
    * 数组的作用:一次性存储多个数据
    * 数组的定义方式:
    * 1.构造函数定义数组: var 数组名=new Array();
    * 2.字面量方式定义数组: var 数组名=[];
    *
    * var 数组名=new Array();空数组
    * var 数组名=new Array(值);数组定义了,有长度
    * var 数组名=new Array(值1,值2,值3....);定义数组并且有多个数据
    * var 数组名=[];空数组
    * var 数组名=[值1,值2,值3];有三个数据
    * 数组元素:就是数组中存储的数据
    * 数组长度:就是数组中元素的个数
    * 数组索引(下标):从0开始,到数组的长度减1结束
    * 通过下标设置数组的元素值: 数组名[索引]=值
    * 通过下标访问数组的元素值: 数组名[索引]
    *
    *
    *
    *
    * */

    var arr1=new Array();//空数组
    var arr2=new Array(5);//长度为5的数组,每个数据的值是undefined
    var arr3=new Array(1,2,3,4,5);//长度为5分数组,
    var arr4=[];//空数组
    var arr5=[1,2,3];//长度为3的数组
    var arr6=["red","blue","green",1,true];//数组中元素的值的类型可以不一样

    var arr7=[];
    //设置数组的元素的值
    arr7[0]=10;
    arr7[1]=20;

  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>数组练习</title>
	<script>
		//1. 数组初始化
		var arr1 = new Array(); // 空数组
		var arr2 = new Array(5); //长度为5的数组，每一个值为undefined
		var arr3 = new Array(1,2,3,4,5);
		var arr4 = [1,2,3,4,5,6,7,,8,9,0];
		//数组中元素的值可以不一样
		var arr5 = [1,"1","red",true,false];
		
		console.log(arr1);
		console.log(arr2);
		console.log(arr3);
		console.log(arr4);
		console.log(arr5);

		for (var i = 0; i < arr5.length; i++) {
			console.log(arr5[i]);
		}

		//eg1. 求数组中所有元素的和
		var eg = [1,2,3,4,5,9,7,8,6,0];
		var sum1 = 0;
		for(var i = 0; i < eg.length; i ++)
			sum1 += eg[i];
		console.log(sum1);
		//eg2.求取元素最大值
		var j = 0;
		for(var i = 0; i < eg.length; i ++){
			if(eg[i] > eg[j]){
				j = i;
			}
		}
		console.log(eg[j]);

		//eg3.数组元素进行拼接
		var names=["卡卡西","佐助","鸣人","大蛇丸","雏田","小苏","凤姐","黑崎一护"];
		var str;
		for(var i = 0; i < names.length - 1; i ++){
			str += names[i] + '|';
		}
		console.log(str + names[names.length - 1]);
		
		//去除重复元素0
		var arr = [10, 0, 20, 0, 30, 0, 50];
		var newarr = [];
		for(var i = 0; i < arr.length; i ++){
			if(arr[i] != 0){
				newarr[newarr.length] = arr[i];
			}
		}
		console.log(newarr);
		
		// 反转数组
		var array = [10, 20, 30, 40, 50];
		for(var i = 0; i < (parseInt)(array.length / 2); i ++){
			var temp = array[i];
			array[i] = array[array.length - 1-i];
			array[array.length - 1-i] = temp;
		}
		console.log(array);
		</script>	
</body>
</html>
```

## 函数的定义

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>


    //单身生活:

    //早上饿了
    //自己做饭-----番茄炒西红柿盖饭-----
    //切菜
    //洗菜
    //放油
    //炒菜
    //放盐
    //装盘
    //---目的---吃


    //中午饿了
    //自己做饭---番茄炒西红柿盖饭
    //切菜
    //洗菜
    //放油
    //炒菜
    //放盐
    //装盘
    //---目的---吃

    //晚上饿了
    //自己做饭---番茄炒西红柿盖饭
    //切菜
    //洗菜
    //放油
    //炒菜
    //放盐
    //装盘
    //---目的---吃

    //半夜饿了
    //自己做饭---番茄炒西红柿盖饭
    //切菜
    //洗菜
    //放油
    //炒菜
    //放盐
    //装盘
    //---目的---吃




    //非单身---
    //早上饿了
    //找一个会做饭的人---做饭的所有的步骤,都是这个人
    //吃

    //中午饿了
    //一个人
    //吃

    //晚上饿了
    //这个人
    //吃




  </script>

  <script>

    //函数:把一坨重复的代码封装,在需要的时候直接调用即可
    //函数的作用:代码的重用
    /*
    *
    * 函数的定义
    * 语法:
    *
    * function 函数名字(){
    *   函数体-----一坨重复的代码
    * }
    *
    * 函数的调用:
    *
    * 函数名();
    *
    *
    *
    * */

//
//    //单身生活
//    //早上
//    console.log("切菜");
//    console.log("炒菜");
//    console.log("放油");
//    console.log("炒菜");
//    console.log("装盘");
//
//    //中午
//    console.log("切菜");
//    console.log("炒菜");
//    console.log("放油");
//    console.log("炒菜");
//    console.log("装盘");
//
//    //晚上
//
//    console.log("切菜");
//    console.log("炒菜");
//    console.log("放油");
//    console.log("炒菜");
//    console.log("装盘");
//
//    //半夜
//    console.log("切菜");
//    console.log("炒菜");
//    console.log("放油");
//    console.log("炒菜");
//    console.log("装盘");


    //有函数了,把这些重复使用的代码放在函数中写,在需要的时候直接调用函数就可以



    //函数定义
    function cook() {
      console.log("切菜");
      console.log("放油");
      console.log("炒菜");
      console.log("放盐");
      console.log("装盘");
    }

    //函数调用
    console.log("早上======");
    cook();
    console.log("中午======");
    cook();
    console.log("晚上======");
    cook();
    console.log("半夜======");
    cook();
    console.log("后半夜");
    cook();
  </script>
</head>
<body>


</body>
</html>
```

### 函数的参数

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    /*
     * 函数参数:
     * 在函数定义的时候,函数名字后面的小括号里的变量就是参数,目的是函数在调用的时候,用户传进来的值操作
     * 此时函数定义的时候后面的小括号里的变量叫参数;写了两个变量,就有两个参数,
     * 在函数调用的时候,按照提示的方式,给变量赋值--->就叫传值,把这个值就传到了变量(参数)中
     *
     * 形参:函数在定义的时候小括号里的变量叫形参
     * 实参:函数在调用的时候小括号里传入的值叫实参,实参可以是变量也可以是值
     *
     *
     * */
    //函数定义
    function consoleSum(x, y) {
      var sum = x + y;//计算和----功能
      console.log(sum);//输出和---第二个功能
    }
//    //函数调用
//    var num1=parseInt(prompt("输入第一个数字"));
//    var num2=parseInt(prompt("输入第二个数字"));
//    consoleSum(num1, num2);


    //    function f1(x) {
    //      console.log(x);
    //    }
    //    function f2(x,y) {
    //
    //    }
    //    function f3(x,y,z) {
    //
    //    }
    //    function f4(x,y,z,k) {
    //
    //    }
  </script>
</head>
<body>

</body>
</html>
```

### 函数的返回值

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    //set:设置
    //get:获取
    //函数的返回值:在函数内部有return关键字,并且在关键字后面有内容,这个内容被返回了
    //当函数调用之后,需要这个返回值,那么就定义变量接收,即可

    /*
    *
    * 如果一个函数中有return ,那么这个函数就有返回值
    * 如果一个函数中没有return,那么这个函数就没有返回值
    * 如果一个函数中没有明确的返回值,那么调用的时候接收了,结果就是undefined
    * (没有明确返回值:函数中没有return,函数中有return,但是return后面没有任何内容)
    * 函数没有返回值,但是在调用的时候接收了,那么结果就是undefined
    * 变量声明了,没有赋值,结果也是undefined
    * 如果一个函数有参数,有参数的函数
    * 如果一个函数没有参数,没有参数的函数
    * 形参的个数和实参的个数可以不一致
    * return 下面的代码是不会执行的
    *
    *
    *
    * */


    function f1(x,y) {
      var sum= x+y;
      return sum;
      console.log("助教才是最帅的");
      return 100;
    }
    var result=f1(10,20);
    console.log(result);




//    function getSum(x, y) {
//      var sum = x + y;
//      return sum;//把和返回
//
//    }
//    //函数调用
//    var result=getSum(10, 20);
//    console.log(result+10);



    //函数定义: 有参数有返回值的函数
//    function getSum(x, y) {
//      return  x + y;//把和返回
//    }
//    //函数调用
//    var result=getSum(10, 20);
//    console.log(result+10);



    //有参数,有返回值的函数
//    function f1(x,y) {
//      return x+y;
//    }
//    //有参数,无返回值的函数
//    function f2(x) {
//      console.log(x);
//    }
//    //无参数,有返回值的函数
//    function f3() {
//      return 100;
//    }
//    //无参数无返回值的函数
//    function f4() {
//      console.log("萨瓦迪卡");
//    }
//
//
//    var sum=f1(10);
//    console.log(sum);//

  </script>
</head>
<body>

</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>函数练习2</title>
	<script>
		//1. 求两个数字的和
		function getSum(x,y) {
			return x + y;
		}
		console.log(getSum(1,4)); //5

		//2. 求两个数字的和,无返回值
		function getSum1(x,y) {
			var sum = x + y;
			console.log(sum); //5
		}

		console.log(getSum1(1,4)); //undefined
	</script>
</head>
<body>
	
</body>
</html>
```

### arguments对象

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    //计算两个数字的和
//    function f1(x, y) {
//      return x + y;
//    }
//    //计算三个数字的和
//    function f2(x, y, z) {
//      return x + y + z;
//    }
//    //计算四个数字的和
//    function f3(x, y, z, k) {
//      return x + y + z + k;
//    }
//    //计算五个数字的和
//    function f4(a, b, c, d, e) {
//      return a + b + c + d + e;
//    }
//    //计算六个数字的和
//    function f5(a, b, c, d, e, f) {
//      return a + b + c + d + e + f;
//    }
    //计算n个数字的和
    //定义一个函数,如果不确定用户是否传入了参数,或者说不知道用户传了几个参数,没办法计算,但是如果在函数中知道了参数的个数,也知道了，每个参数的值.可以

    //定义
//    function f1() {
//      //获取的是函数在调用的时候,传入了几个参数
//      //console.log(arguments.length);
//      //使用arguments对象可以获取传入的每个参数的值
//      console.log(arguments);
//    }
//
//    f1(10,20,30,40,100,200);//调用



    function f1() {
      //arguments----->数组使用------伪数组---
      var sum=0;
      for(var i=0;i<arguments.length;i++){
        sum+=arguments[i];
      }
      return sum;
    }

    console.log(f1(10,20,30));
  </script>
</head>
<body>
</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>arguments</title>
	<script>
		function fun() {
			//必须要初始化，未定义的变量为undefined
			var sum = 0;
			for(var i = 0; i < arguments.length; i++ ){
				sum += arguments[i];
			}
			return sum;
		}
		console.log(fun(1,2,3,4,5));
	</script>
</head>
<body>
	
</body>
</html>
```

### 函数的其他定义方式

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    /*
     * 命名函数:函数如果有名字,就是命名函数
     *
     * 匿名函数:函数如果没有名字,就是匿名函数
     *
     * 函数的另一种定义方式
     * 函数表达式:
     * 把一个函数给一个变量,此时形成了函数表达式
     * var 变量=匿名函数;
     * 例子:
     * var f1=function (){
     *
     * };
     * 如果是函数表达式,那么此时前面的变量中存储的就是一个函数,而这个变量就相当于是一个函数,就可以直接加小括号调用了
     * f1();
     *
     * 注意:
     * 函数表达式后面,赋值结束后,要加分号
     *
     *
     *
     * 函数定义:
     * 1. 函数声明--函数定义
     * function 函数名(){
     *     函数体
     * }
     *
     * */



    //    var f1=function(){console.log("阿涅哈斯诶呦");};
    //    f1();

    //函数的自调用,没有名字,调用---声明的同时,直接调用
    //一次性的--------
    //    (function(){console.log("阿涅哈斯诶呦");})();
    //    (function(){console.log("嘎嘎")})();


    //
    //    function f1() {
    //      console.log("哈哈,我又变帅了");
    //    }
    //    f1();//函数调用
    //    //如果一个函数能够调用:  函数的代码();
    //
    //    //函数表达式
    //    var f2 = function () {
    //      console.log("哈哈,真的好帅哦");
    //    };
    //    //匿名函数不能直接调用
    //    f2();
    //
    //
    //    var f4 = function () {
    //      console.log("我是一个函数");
    //    };
    //    f4();
    //
    //
    //
    //    var num=10;


    //函数声明
    function f1() {
      console.log("助教好帅哦");
    }
    f1();
    function f1() {
      console.log("小苏好猥琐哦");
    }
    f1();

    //函数表达式
    var f2 = function () {
      console.log("助教没有小杨帅");
    };
    f2();
    f2 = function () {
      console.log("小杨真的很帅");
    };
    f2();
    //函数自调用
    (function () {
      console.log("阿涅哈斯诶呦");
    })();
    (function () {
      console.log("嘎嘎")
    })();


    //    var num=10;
    //    console.log(num);
    //    num=100;
    //    console.log(num);
  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>函数的其他定义方法</title>
	<script>
		//1. 函数声明
		function f1(){
			console.log("哈哈");
		}
		f1();
		function f1(){
			console.log("在这里f1表示的是函数体,()表示函数调用！");
		}
		f1();
		//上述语句覆盖操作！！

		//2、 函数表达式
		//命名函数无需函数表达式
		function f2(){
			console.log("哈哈f2");
		}
		f2();
		//匿名函数无法直接调用，需要使用函数表达式
		var f3 = function (){
			console.log("哈哈f3");
		};
		f3();
		//类似于：
		//var num1 = 10；
		//console.log(num1); 10
		//var num1 = 20；
		//console.log(num1); 20
		//使用同一个变量调用不同的函数
		
		//3. 函数自调用：即在定义的时候直接调用
		(function (){console.log("函数自调用！！")})();

		// 4. 函数也有类型
		console.log(typeof f1); //function

		//5. 函数可以作为参数进行使用
		function ff1(fn){
			fn();
		}
		function fn(){
			console.log("函数作为参数使用例子...");
		}

		ff1(fn);

		//6. 函数可以作为返回值使用
		function fff1() {
			console.log("fff1的函数调用...");
			return function (){
				console.log("这是一个函数...");
			}
		}
		var ff = fff1();
		ff();
	</script>
</head>
<body>
	
</body>
</html>
```

## 作用域

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    //作用域:使用范围
    /*
    *
    * 全局变量:声明的变量是使用var声明的,那么这个变量就是全局变量,全局变量可以在页面的任何位置使用
    * 除了函数以外,其他的任何位置定义的变量都是全局变量
    * 局部变量:在函数内部定义的变量,是局部变量,外面不能使用
    * 全局变量,如果页面不关闭,那么就不会释放,就会占空间,消耗内存
    *
    * 全局作用域:全局变量的使用范围
    * 局部作用域:局部变量的使用范围
    *
    * 块级作用域:一对大括号就可以看成是一块,在这块区域中定义的变量,只能在这个区域中使用,但是在js中在这个块级作用域中定义的变量,外面也能使用;
    * 说明:js没有块级作用域,只有函数除外
    *
    * 隐式全局变量:声明的变量没有var,就叫隐式全局变量
    * 全局变量是不能被删除的,隐式全局变量是可以被删除的
    * 定义变量使用var是不会被删除的,没有var是可以删除的
    *
    *
    * */

//    function f1() {
//      number=1000;//是隐式全局变量
//    }
//    f1();
//    console.log(number);

//    var num1=10;
//    num2=20;
//    delete num1;//把num1删除了
//    delete num2;//把num2删除了
//    console.log(typeof num1);
//    console.log(num1+10);
//    console.log(typeof num2);




//    num=100;
//    console.log(num);

    //扩展:隐式


//    function f1() {
//      var num=100;
//      num+=10;
//    }
//    f1();//这个函数结束之后


//    {
//      var num=10;
//      console.log(num);//10
//    }
//    console.log(num);

//    if(true){
//      var num=10;
//    }
//    console.log(num);
//    for(var i=0;i<5;i++){
//      var number=20;
//    }
//    console.log(number);

//    var i=0;
//    while (i<5){
//      var num=100;
//      i++;
//    }
//    console.log(num);


//    function f1() {
//      var num=10;
//    }
//    f1();
//    console.log(num);

//    var num=10;
//    console.log(num);//10
  </script>
  <script>
    //console.log(num);
  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>变量的作用域问题</title>
	<script>
		//1. JS无块级作用域
		{
			var num = 10;
		}
		console.log(num);
	</script>
	<script>
		console.log(num);
	</script>
	
	<script>
		//2. 使用var声明的变量为全局变量
		//3. 局部变量：在函数内部定义的变量是局部变量
		//4. 全局变量：使用var声明的变量
		//5. 隐式全局变量：声明的变量没有var
		//6. 全局变量是不能被删除的
		//7. 隐式的全局变量可以被删除
		var num1 = 20;
		num2 = 20;
		delete num1;
		delete num2;
		console.log(num1);
		console.log(num2);//提示未定义
	</script>
</head>
<body>
	
</body>
</html>
```

## 作用域链

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>


    var num=10;
    function f1() {
      var num=20;
      function f2() {
        var num=30;
        function f3() {
          var num=50;
          console.log(num);
        }
        f3();
      }
      f2();
    }
    f1();
  </script>
</head>
<body>
</body>
</html>
```

## 预解析

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    //预解析:提前解析代码
    /*
    *
    * 预解析:就是在解析代码之前
    * 预解析做什么事?
    * 把变量的声明提前了----提前到当前所在的作用域的最上面
    * 函数的声明也会被提前---提前到当前所在的作用域的最上面
    *
    *
    * */

    //函数调用的时候,把会函数的声明提升到作用域的上面
//    f1();//调用
//    var num=20;//这个变量的声明会提升到变量使用之前
//    function f1() {
//      console.log(num);
//      //var num=10;
//    }

//    function f1() {
//      console.log("小苏好猥琐");
//    }
//
//
//    f1();
//    function f1() {
//      console.log("小苏没有助教猥琐");
//    }
//    f1();



    //把变量的声明提前了
//    var num;
//    console.log(num);
//    num=10;
//    function f1() {
//      console.log("哈哈,助教好猥琐哦");
//    }
    //f1();//报错




  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>预先解析</title>
	<script>
		/*
			预先解析：提前解析代码
			预解析做什么事情：
				1. 把变量的声明提前了
						提前在所在变量作用域的最上面
				2. 函数的声明也会提前
						提前到当前所在的作用域的最上面

		 */
		
		console.log(num1); //undefined
		var num1 = 10;
		/*
			等价于：
			var num1;
			console.log(num1); 只声明为定义
			num1 = 10;

		 */
		f1();
		var num2 = 10;
		function f1(){
			console.log(num2);
		}

		/**
		 * 等价于：
		 * var num2;
		 * function f1(){
		 * 	console.log(num2);
		 * }
		 * f1();
		 * num2 = 10;
		 */

	</script>

	<script>
		function f1() {
	    	console.log(num);//undefined
	    	var num=10;
	    }
	    f1();
	    //console.log(num); error
	    /**
	     *等价于：
	     *	function f1() {
         *      var num;
	     *		console.log(num);//undefined
	     *		var num=10;
	     *	}
	     *	f1();
	     * 
	     */
	</script>

	<script>
		var a = 25;
		function abc() {
			console.log(a); //undefined
			var a = 10;
		}
		abc();
		console.log(25); //25

		/*
			var a = 25;
			function abc() {
				//函数名的变量只会提升到函数的作用域的最前面
				var a;
				console.log(a);
				a = 10;
			}
			abc();
			console.log(25);

		 */
	</script>
</head>
<body>
	
</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    //预解析中,变量的提升,只会在当前的作用域中提升,提前到当前的作用域的最上面
    //函数中的变量只会提前到函数的作用域中的最前面,不会出去
    //预解析会分段(多对的script标签中函数重名,预解析的时候不会冲突)

//    function f1() {
//
//      console.log(num);//undefined
//      var num=10;
//    }
//    f1();
//    console.log(num);//




    function f1() {
      console.log("哈哈");
    }

  </script>
  <script>
    f1();
    function f1() {
      console.log("嘎嘎");
    }
  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>

  <script>

    //    var a = 25;
    //    function abc (){
    //      alert(a);//undefined
    //      var a = 10;
    //    }
    //    abc();
    //    console.log(a);//25


    //  var a;
    //function a() {
    //  console.log('aaaaa');
    //}
    //    console.log(a);
    //
    //   a = 1;
    //    console.log(a);//1

//    var a;
//    a = 18;
//    function f1() {
//      var b;
//      var a;
//      b = 9;
//      console.log(a);//undefined
//      console.log(b);//9
//     a = '123';
//    }
//    f1();


//    function f1() {
//      var a;//局部变量
//      a=9;
//      //隐式全局变量
//      b=9;
//      c=9;
//      console.log(a);//9
//      console.log(b);//9
//      console.log(c);//9
//    }
//    f1();
//    console.log(c);//  9
//    console.log(b);// 9
//    console.log(a);//报错

    //console.log(parseInt(Math.random()*57+1));
  </script>


  <script>

    f1();//-----报错
   var f1=function () {
      console.log(a);
      var a=10;
    };

    function f2() {

    }
    f2();

  </script>
</head>
<body>
</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>预解析案例</title>
	<script>
//函数中的变量只会提前到函数的作用域中的最前面,不会出去
//预解析会分段(多对的script标签中函数重名,预解析的时候不会冲突)

		function f1() {
		 console.log(num);//undefined
		 var num=10;
		}
		f1();
		//console.log(num);
		/*
			function f1() {
				var num;
				console.log(num);//undefined
				num=10;
			}
			f1();
			console.log(num); //未定义

		 */
		f1();
		function f1() {
      		console.log("哈哈");
    	}

    	/*
    	function f1() {
			console.log(num);//undefined
			var num=10;
		}
		function f1() {
      		console.log("哈哈");
    	}
    	f1();
    	f1();
    	 */

	</script>
	<!-- 预解析会分段(多对的script标签中函数重名,预解析的时候不会冲突) -->
	<script>
		f1();
    	function f1() {
      		console.log("嘎嘎");
    	}
	</script>
</head>
<body>
	
</body>
</html>
```

## 复习

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
//    var str = prompt("请输入一个数字");
//    //用户没有输入内容
//    if (str == "") {
//      console.log("您输入有误");
//    } else {
//      //用户输入内容了
//      if (!isNaN(parseInt(str))) {
//        console.log("用户输入的是一个数字");
//        //调用一个函数,把这个数字传入到函数中,判断该数字是不是质数
//      } else {
//        console.log("用户输入的不是一个数字");
//      }
//    }
  </script>

  <script>
    //如何判断一个数字是质数
//    var num=7;
//    function isPrimeNumber(num) {
//      for(var i=2;i<=num/2;i++){
//        if(num%i==0){
//          return false;
//        }
//      }
//      return true;
//    }
//    console.log(isPrimeNumber(num));
  </script>

  <script>
    /*
    *
    *
    *
    *
    *
    *
    *
    * */
  </script>

  <script>

    /*
    * 复习:
    * 函数:把一些重复的代码封装在一个地方,在需要的时候直接调用这个地方的代码就可以了
    *
    * 函数作用:代码重用
    *
    * 函数的参数:
    * 1.形参:函数定义的时候,函数名字后面的小括号里的变量
    * 2.实参:函数调用的时候,函数名字后面的小括号里的变量或者值
    *
    * 返回值:
    * 函数中有return，函数有返回值
    * 函数中没有return,函数没有返回值
    * 没有明确返回值:函数中没有return或者return后面没有任何内容
    * 如果一个函数没有明确的返回值,接收这个函数,结果是undefined
    *
    * 无参数无返回值的函数
    * 无参数有返回值的函数
    * 有参数无返回值的函数
    * 有参数有返回值的函数
    *
    * arguments----->可以获取函数调用的时候,传入的实参的个数
    * arguments是一个对象,是一个伪数组
    * arguments.length--->是实参的个数
    * arguments[索引]---->实参的值
    *
    * 作用域:变量的使用范围
    * 全局作用域:全局变量在任何位置都可以使用的范围
    * 局部作用域:局部变量只能在某个地方使用---函数内
    * 作用域链:在一个函数中使用一个变量,先在该函数中搜索这个变量,找到了则使用,找不到则继续向外面找这个变量,找到则使用,一直找到全局作用域,找不到则是undefined
    * 全局变量:只要是在函数外面声明的变量都可以看成或者是理解成是全局变量
    * 局部变量:在函数中定义的变量
    *
    * 预解析:在执行代码之前做的事情
    * 变量的声明和函数的声明被提前了,变量和函数的声明会提升到当前所在的作用域的最上面
    * 函数中的变量声明,会提升到该函数的作用域的最上面(里面)
    * 如果有多对的script标签都有相同名字的函数,预解析的时候是分段的,互不影响
    *
    *
    *
    *
    *
    *
    * */
  </script>
</head>
<body>


</body>
</html>
```

# 面向对象编程

```javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>面向对象</title>
	<script>
		/**
		 * 创建对象有三种方式：
		 * 	1. 调用系统的构造函数进行创建
		 * 	var 变量 = new Object();
		 *
		 *  2. 自定义构造函数创建对象
		 *
		 *	3. 通过字面量来创建对象 
		 */
	</script>
	<script>
		//方法1.创建对象
		var obj = new Object();
		//添加属性
		obj.name = "xx";
		obj.age = 33;
		obj.sex = "女";
		//添加方法
		obj.eat = function (){
			console.log("eat ...");
		}
		obj.play = function (){
			console.log("play ...");
		}
		console.log(obj.name);
		console.log(obj.age);
		console.log(obj.sex);
		obj.eat();
		console.log(obj instanceof Object)
	</script>

	<script>
		// 方法2 工厂模式创建对象 一次性创建对个对象
		function createObject(name,age,sex) {
			var obj = new Object();
			obj.name = name;
			obj.age = age;
			obj.sex = "女";
			obj.sayHi = function () {
				console.log("Hi ... My name is " + this.name + " and My age is " + this.age + " , My sex is " + this.sex);
			}

			return obj;
		}

		var person1 = createObject("x1",22,"男");
		person1.sayHi();
	</script>
	<script>
		//方法2:自定义构造函数创建对象
		//实现过程：
		//	1. 在内存中开辟一块空间，存储创建新的对象
		//	2. 把this设置为当前的对象
		//	3. 设置对象的属性和方法的值
		//	4. 把this对象返回
		function Person(name,age){
			this.name = name;
			this.age = age;
			this.sayHi = function () {
				console.log("My Name is " + this.name + " My age is " + this.age);
			}
		}
		var person = new Person("xxx",22);
		console.log(person.name);
		console.log(person.age);
		person.sayHi();
		console.log(person instanceof Person);
	</script>
	<script>
		// 方法3： 字面量创建对象
		var obj = {}; //空对象
		obj.name = "222";
		obj.age = 30;
		obj.sayHi = function () { 
			console.log("My Name is " + this.name + " My age is " + this.age);
		};
		obj.sayHi();

		var obj1 = {
			name :"dsds",
			age : 40,
			sayHi:function () { 
			console.log("My Name is " + this.name + " My age is " + this.age);
			},
		};
		obj1.sayHi();
		obj1.name = "xxx";
		obj1.sayHi();
		//设置和获取属性的另一种写法
		obj1["name"]="sss";
		obj1.sayHi();
	</script>
</head>
<body>
	
</body>
</html>
```

## JSON数据格式

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    //对象:有属性和方法,特指的某个事物
    //对象:一组无序属性的集合的键值对,属性的值可以是任意的类型
    //    function Dog(name) {
    //      this.name=name;
    //    }
    //    function Person(name,age) {
    //      this.age=age;
    //      this.name=name;
    //      this.sex=true;
    //      this.dog={};
    //      this.play=function () {
    //        console.log("喜欢玩游戏");
    //      };
    //    }
    //
    //    var sex=false;//男
    //    console.log(sex?"男":"女");


    //JSON格式的数据:一般都是成对的,是键值对,

    //json也是一个对象,数据都是成对的,一般json格式的数据无论是键还是值都是用双引号括起来的

    //    var obj={
    //      name:"小明"
    //    };


    var json = {
      "name": "小明",
      "age": "10",
      "sex": "男"
    };
    //遍历对象,是不能通过for循环遍历,无序

    //key是一个变量,这个变量中存储的是该对象的所有的属性的名字
    for (var key in json) {
      console.log(key + "===========" + json[key]);
    }


    //    var key="name";
    //    console.log(json[key]);
    //可以通过for-in循环
    //
    //    for(var key in json){
    //      //console.log(key);//json对象中的属性的名字
    //      console.log(json[key]);
    //    }
    //对象中确实有这个属性对象.属性名字  或者对象[属性名字]


    //一个一个的遍历出来

    //    var arr=[10,20,30];
    //    for(var i=0;i<arr.length;i++){
    //      console.log(arr[i]);
    //    }
  </script>
</head>
<body>


</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>JSON数据格式</title>
	<script>
		//JSON也是一个对象
		var json = {
			"name": "xxx",
			"age" : "10",
			"sex" : "女",
		};
		//遍历对象不能使用for循环，因为对象是一组无序数据的集合
		//什么时候使用点，什么时候使用[]：
			// 1. 当对象中确实有这个属性时，使用.，还可以使用[]
			// 2.当访问使用JSON的键值对时，使用[]
		for(var key in json){
			console.log(key +" : "+ json[key]);
		}
	</script>
</head>
<body>
	
</body>
</html>
```

## 简单类型和复杂类型

```js
/*
原始类型：number string boolean  undefined null object
复杂类型：object
基本类型：number string boolean
空类型：  undefined null
*/

/*
值类型的值在栈上存储
引用型类型的值在堆上存储，地址在栈上存储
值类型之间的传递，传递的是值
引用类型之间的传递，传递的是地址
*/
```

## 值传递和地址传递实战

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>


    //    var num1 = 10;
    //    var num2 = num1;
    //    num1 = 20;
    //    console.log(num1);//20
    //    console.log(num2);//10
	//值传递

    //    var num = 50;
    //    function f1(num) {
    //      num = 60;
    //      console.log(num);//60
    //    }
    //    f1(num);
    //    console.log(num);//50
      
//
//    var num1 = 55;
//    var num2 = 66;
//    function f1(num, num1) {
//      num = 100;
//      num1 = 100;
//      num2 = 100;
//      console.log(num);//100
//      console.log(num1);//100
//      console.log(num2);//100
//    }
//
//    f1(num1, num2);
//
//
//
//    console.log(num1);//55
//    console.log(num2);//100
//    console.log(num);// 报错




    function Person(name,age,salary) {
      this.name = name;
      this.age = age;
      this.salary = salary;
    }
    function f1(person) {
      person.name = "ls";
      person = new Person("aa",18,10);
    }

    var p = new Person("zs",18,1000);
    console.log(p.name);
    f1(p);
    console.log(p.name);
  </script>
</head>
<body>


</body>
</html>
```

# 内置对象

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>
    /*
    * js学习中三种对象:
    * 1.内置对象----js系统自带的对象
    * 2.自定义对象---自己定义的构造函数创建的对象
    * 3.浏览器对象---BOM的时候讲
    *
    * 内置对象:
    * Math
    * Date
    * String
    * Array
    * Object
    * */

    //如何验证变量是不是对象
//    console.log(Array instanceof Object);
//    var obj={};
//    console.log(obj instanceof Object);

  </script>
</head>
<body>


</body>
</html>
```







