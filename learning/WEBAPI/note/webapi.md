# WEBAPI

## DOM的基本认识

```JS
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    /*
    *
    * JavaScript分三个部分:
    * ECMAScript标准:JS的基本的语法
    * DOM:Document Object Model --->文档对象模型----操作页面的元素
    * BOM:Browser Object Model----->浏览器对象模型---操作的是浏览器
    *
    * DOM: 文档对象模型
    *
    * 文档:把一个html文件看成是一个文档,由于万物皆对象,所以把这个文档看成是一个对象
    * XML文件也可以看成是一个文档
    *
    * HTML:展示信息,展示数据的
    * XML:侧重于存储数据
    * html文件看成是一个文档,那么这个文档看成是一个对象,文档中的所有的标签都可以看成是一个对象
    *
    * 页面中的每个标签,都是一个元素(element),每个元素都可以看成是一个对象
    * 标签可以嵌套,标签中有标签,元素中有元素
    *
    * html页面中都有一个根标签--html--也叫根元素
    *
    * 页面中的有一个根元素(标签--html),里面有很多的元素(有很多的标签,有很多的对象)
    *
    * 文档:一个页面就是一个文档
    *
    * 元素(element):页面中的所有的标签都是元素,元素可以看成是对象
    *
    * 节点(node):页面中所有的内容都是节点:标签,属性,文本
    * root:根
    *
    *
    * 页面就是文档--document,文档中有根元素:html
    * html--->head
    *------>body--->其他的标签
    *
    * 由文档及文档中的所有的元素(标签)组成的一个树形结构图,叫树状图(DOM树)
    *
    * */

  </script>
</head>
<body>


</body>
</html>
```

## DOM操作

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>认识Dom</title>
	<script>
		function f1() {
			alert('第二版本的JS代码结构...');
		}
	</script>
	<!-- 
		出现这种错误：
			 Uncaught TypeError: Cannot set property 'onclick' of null
			主要是因为JS代码的放置位置的不正确性！
			HTML文档是从上向下顺序执行的，执行到JS代码的时候，不理解'btn1'是什么意思
			解决方法：将JS代码放置在body的最后部分！！
	 -->
</head>
<body>
	<!-- 第一版本 -->
	<input type="button" value="第一版本" onclick="alert('第一版本的JS代码...')"/>
	<!-- 第二版本的JS代码结构：未实现完全的分离 -->
	<input type="button" value="第二版本" onclick="f1()" />
	<!-- 第三版本的JS代码结构：开始分离JS和HTML，容易函数重名 -->
	<!-- 使用在HTML文档中id值唯一的特性 -->
	<input type="button" value="第三版本" id="btn1" />
	<!-- 第四版本的JS代码结构：匿名函数的使用 -->
	<input type="button" value="第四版本" id="btn2" />
	
	<script>
		function f2() {
			alert('第三版本的JS代码结构：开始分离JS和HTML');
		}
		var btn1Obj = document.getElementById("btn1");
		btn1Obj.onclick = f2;
	</script>
	<script>
		var btn2Obj = document.getElementById('btn2');
		btn2Obj.onclick = function () {
			alert('第四版本的JS代码结构：匿名函数的使用');
		}
	</script>


</body>
</html>
```

### 操作img标签的2种方法

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>img标签的操作</title>
</head>
<body>
	<input type="button" value="操作img标签" id="btn">
	<img src="" alt="" id="im">
	<script>
		/**
		 * 注意：
		 * document.getElementById('btn');
		 * 返回对象元素
		 * document.getElementsByTagName
		 * 返回数组元素，数组里面是对象
		 *
		 * 注意链式对象 document是文档的根部
		 */
		var btnObj = document.getElementById('btn');
		btnObj.onclick = function () {
			/**
			 * 两种方法：
			 * 	方法1:使用id属性
			 * 	方法2：使用标签名称
			 * 
			 */
			// var imObj = document.getElementById('im');
			// imObj.src = "../images/1.jpg";
			// imObj.alt = "这是一个美女";
			// imObj.title = "图片：美女";
			// imObj.width = "128";
			// imObj.height = "80";
			// 
			var imObj = document.getElementsByTagName("img");
			imObj[0].src = "../images/1.jpg";
			imObj[0].alt = "这是一个美女";
			imObj[0].title = "图片：美女";
			imObj[0].width = "128";
			imObj[0].height = "80";
		}

	</script>
</body>
</html>
```

### 修改p标签的内容

```js 
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>修改p标签的内容</title>
</head>
<body>
	<input type="button" value="修改第一个p标签" id="btn1" />
	<input type="button" value="群改p标签" id="btn2">

	<div id="div1">
		<p id="p1">我是谁？ 我是p标签啊，来修改我啊！！</p>
		<p>我是谁？ 我是p标签啊，来修改我啊！！</p>
		<p>我是谁？ 我是p标签啊，来修改我啊！！</p>
		<p>我是谁？ 我是p标签啊，来修改我啊！！</p>
		<p>我是谁？ 我是p标签啊，来修改我啊！！</p>

	</div>
	<script>
		var btn1Obj = document.getElementById('btn1');
		btn1Obj.onclick = function () {
			var p1Obj = document.getElementById('p1');
			p1Obj.innerText = "小样，改了你又怎么样！，你打我呀！！！";
		}

		var btn2Obj = document.getElementById('btn2');
		btn2Obj.onclick = function () {
			//这是一个链式寻找目标
			//好像前面的必须是通过id属性来链接
			var pObj = document.getElementById('div1').getElementsByTagName('p');
			console.log(pObj.length);
			for(var i = 1; i < pObj.length; i ++){
				pObj[i].innerText = "小样，改了你又怎么样！，你打我呀！！！";
			}
		}

	</script>

</body>
</html>
```

### 修改a标签的属性

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>修改a标签的属性</title>
</head>
<body>
	<input type="button" value="修改a标签" id="btn1">
	<a href="https://www.jiumodiary.com/" id="a1">鸠摩搜书</a>

	<script>
		var btn1Obj = document.getElementById('btn1');
		btn1Obj.onclick = function () {
			var a1Obj = document.getElementById('a1');
			a1Obj.href = "http://www.baidu.com";
			a1Obj.innerText = "百度";
		}
	</script>
</body>
</html>
```

### 修改文本框的值

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>修改文本框的值</title>
</head>
<body>
	<input type="button" value="修改文本框的值" id="btn1"> <br />
	<input type="text" value=" "><br />
	<input type="text" value=" "><br />
	<input type="text" value=" "><br />
	<input type="text" value=" "><br />
	<input type="text" value=" "><br />

	<script>
		var btn1Obj = document.getElementById('btn1');
		btn1Obj.onclick = function () {
			var textObj = document.getElementsByTagName('input');
			for(var i = 0; i < textObj.length; i ++){
				if(textObj[i].type == "text"){
					textObj[i].value = "我修改了文本框的值";
				}
				
			}
		}

	</script>
</body>
</html>
```

### 修改按键的自身属性

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>修改按钮的自身属性</title>
</head>
<body>
	<!-- 使用this从来访问本类对象 -->
	<input type="button" value="未点击" id="btn1">
	<script>
		var btn1Obj = document.getElementById('btn1');
		btn1Obj.onclick = function () {
			this.value = "以点击";
			this.type = "text";
			this.id = "btn2";
		}
	</script>
</body>
</html>
```

### 按键排他功能

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>按键排他功能</title>
</head>
<body>
	<input type="button" value="没怀孕"> <br />
	<input type="button" value="没怀孕"> <br />
	<input type="button" value="没怀孕"> <br />
	<input type="button" value="没怀孕"> <br />
	<input type="button" value="没怀孕"> <br />
	<input type="button" value="没怀孕"> <br />

	<script>
		var btnObj = document.getElementsByTagName('input');
		//为每一个按钮分别注册事件
		for(var i = 0; i < btnObj.length; i++){

			btnObj[i].onclick = function () {
				//所有的按钮被重置
				for (var j = 0; j < btnObj.length; j++) {
        			btnObj[j].value = "没怀孕";
      			}
      			//被按下的按钮被打开了
      			this.value = "怀孕了";
			}
			
		}
	</script>
</body>
</html>
```

### 点击超链接按钮实现图片的修改，不能进行页面跳转

```java
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>点击超链接切换图片</title>
</head>
<body>
	<a href="../images/1.jpg" id="ak"><img src="../images/1-small.jpg" alt="" id="im"></a>
	<script>
		document.getElementById('im').onclick = function () {
			this.src = document.getElementById('ak').href;
			//必须加上，不加的话会进行页面的跳转
			return false;
		}
	</script>
</body>
</html>
```

### 设置单选多选等

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>点击按钮修改性别和兴趣</title>
</head>
<body>
	<input type="button" value="修改" id="btn1">
	<input type="radio" value="1" name="sex"> 男
	<input type="radio" value="2" name="sex" checked> 女
	<input type="radio" value="3" name="sex" id="ch1"> 中间
	<br>

	<input type="button" value="修改" id="btn2">
	<input type="checkbox" value="1" name="xq" id="c2">eat1
	<input type="checkbox" value="2" name="xq" id="c3">eat2
	<input type="checkbox" value="3" name="xq" id="c4">eat3
	<input type="checkbox" value="4" name="xq" checked>eat4
	<input type="checkbox" value="5" name="xq" checked>eat5
	<input type="checkbox" value="6" name="xq" checked>eat6
	<br>

	<input type="button" value="修改" id="btn3">
	<select name="" id="ss">
		<option value="1">1</option>
		<option value="2">2</option>
		<option value="3">3</option>
		<option value="4">4</option>
		<option value="5" id="s5">5</option>
		<option value="6">6</option>

	</select>
	
	<script>
		function my$(id){
			return document.getElementById(id);
		}
		my$("btn1").onclick = function () {
			my$("ch1").checked = true;
		}
	</script>
	<script>
		my$('btn2').onclick = function () {
			my$('c2').checked=true;
			my$('c3').checked=true;
			my$('c4').checked=true;
		}
	</script>
	<script>
		my$('btn3').onclick = function () {
			my$('s5').selected=true;
		}
	</script>
</body>
</html>
```

### 设置div的宽高背景

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>设置div的宽高背景</title>
</head>
<body>
	<input type="button" value="修改样式" id="btn1">
	<div id="div1" style="width: 300px;height: 300px;background-color: red;"></div>
	<script>
		function my$(id) {
			return document.getElementById(id);
		}
	</script>
	<script>
		//凡是css中这个属性是多个单词的写法,在js代码中DOM操作的时候.把-干掉,后面的单词的首字母大写即可
		my$('btn1').onclick = function () {
			my$('div1').style.width = "600px";
			my$('div1').style.height = "600px";
			my$('div1').style.backgroundColor = "pink";
		}
	</script>

</body>
</html>
```

### 设置div的隐藏和显示操作-单按钮

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>设置div的隐藏和显示操作-单按钮</title>
	<style>
	.div1 {
		width: 300px;
		height: 300px;
		background-color: red;
	}
		
	</style>
</head>
<body>
	<input type="button" value="隐藏" id="btn1">
	<div class="div1" id="d1"></div>
	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>
	
	<script>
		my$('btn1').onclick = function () {
			if(this.value == "隐藏"){
				my$('d1').style.display = "none";
				this.value = "显示";
			}
			else if(this.value == "显示"){
				my$('d1').style.display = "block";
				this.value = "隐藏";
			}
			
		}

	</script>

</body>
</html>
```

### 设置div的class

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>设置div的隐藏和显示操作-单按钮</title>
	<style>
	.div1 {
		width: 300px;
		height: 300px;
		background-color: red;
	}

	.div2 {
		width: 500px;
		height: 500px;
		background-color: pink;
	}
		
	</style>
</head>
<body>
	<input type="button" value="隐藏" id="btn1">
	<div class="div1" id="d1"></div>
	<!-- 行内块元素 -->
	<input type="button" value="修改div属性" id="btn2">
	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>
	
	<script>
		my$('btn1').onclick = function () {
			if(this.value == "隐藏"){
				my$('d1').style.display = "none";
				this.value = "显示";
			}
			else if(this.value == "显示"){
				my$('d1').style.display = "block";
				this.value = "隐藏";
			}
			
		}

	</script>

	<script>
		//在js代码中DOM操作的时候,设置元素的类样式,不用class关键字,应该使用,className
		my$('btn2').onclick = function () {
			my$('d1').className = "div2";
		}
	</script>
</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>设置div的隐藏和显示操作-使用类样式</title>
	<style>
	.div1 {
		width: 300px;
		height: 300px;
		background-color: red;
	}

	.div2 {
		width: 500px;
		height: 500px;
		background-color: pink;
	}

	.div1dis {
		display: none;
	}
		
	</style>
</head>
<body>
	<input type="button" value="隐藏" id="btn1">
	<div class="div1" id="d1"></div>
	<!-- 行内块元素 -->
	<input type="button" value="修改div属性" id="btn2">
	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>
	
	<script>
		my$('btn1').onclick = function () {
			if(this.value == "隐藏"){
				my$('d1').className = "div1dis";
				this.value = "显示";
			}
			else if(this.value == "显示"){
				my$('d1').className = "div1";
				this.value = "隐藏";
			}
			
		}

	</script>

	<script>
		//在js代码中DOM操作的时候,设置元素的类样式,不用class关键字,应该使用,className
		my$('btn2').onclick = function () {
			my$('d1').className = "div2";
		}
	</script>
</body>
</html>
```

### 获取body标签

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>网页开关灯</title>
	<style>
		.cls {
			background-color: #000;
		}
	</style>
</head>
<body>
	<input type="button" value="开/关灯" id="btn1">
	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>

	<script>
		my$('btn1').onclick = function () {
			//获取body标签
			document.body.className = document.body.className != "cls" ? "cls":"";
		}
	</script>
</body>
</html>
```

## 上述内容的总结部分

```js

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>

    /*
    *
    * JavaScript分三个部分:
    * 1. ECMAScript标准----JS基本的语法
    * 2. DOM:Document Object Model 文档对象模型
    * 3. BOM:浏览器对象模型
    *
    * DOM的作用:操作页面的元素
    * DOM树:把html页面或者是xml文件看成是一个文档,文档就是一个对象,这个文档中所有的标签都是元素,元素也可以看成是对象,标签(元素,对象)有很多,还有嵌套的关系,组成的这种层次结构,可以模拟成树形结构图,简称:树状图 ,就是DOM树
    *
    * 获取元素:
    * 2种方式:
    * 根据id从整个的文档中获取元素---返回的是一个元素对象
    * document.getElementById("id属性的值")
    * 根据标签的名字获取元素-----返回的是元素对象组成的伪数组
    * document.getElementsByTagName("标签的名字");
    * 操作基本标签的属性
    * src,title,alt,href,id属性
    * 操作表单标签的属性
    * name,value,type,checked,selected,disabled,readonly
    * 元素的样式操作
    * 对象.style.属性=值;
    * 对象.className=值;
    *
    * 为元素添加事件的操作
    * 事件:就是一件事,有事件源,触发和响应
    *
    * this关键字----如果是在当前的元素的事件中使用this,那么this就是当前的对象
    *
    *
    * 内置对象:系统自带的对象
    * 自定义对象:自己写的对象
    * 浏览器对象:
    * DOM
    * DOM对象:------->通过DOM方式获取的元素得到的对象
    *
    * 元素:element:页面中的标签
    * 节点:Node:页面中所有的内容,标签,属性,文本
    * 根元素:html标签
    * 页面中的顶级对象---:document
    *
    *
    *
    *
    *
    * */

  </script>
</head>
<body>
<p id="p1"></p>


</body>
</html>
```

## 重点案例二

```js

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <script>


    /*
    *
    * 案例----重点
    *
    * 元素的样式的操作的案例
    *
    * 阻止超链接跳转---------
    * 小图和大图切换
    * 美女相册
    * 获取元素的其他的方式
    * 元素样式操作的相关的案例:查缺补漏:操作基本标签和表单标签的小案例
    *
    * innerText和textContent
    * innerText和innerHTML的区别
    * 兼容代码==========================重点
    * 自定义属性---------重点
    * 节点操作-----------理解为主
    *
    *
    * */
  </script>
</head>
<body>


</body>
</html>
```

### 禁用文本框

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>禁用文本框</title>
</head>
<body>
	<input type="button" value="禁用文本框" id="btn1">
	<input type="text" name="" id="t1">
	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>
	<script>
		my$('btn1').onclick = function () {
			my$('t1').disabled=true;
		}
	</script>
</body>
</html>
```

### 背景变色

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>背景变色</title>
</head>
<body>
	<input type="button" value="背景变色" id="btn1">
	<ul id="ul1">
		<li>文字文字文字文字文字文字</li>
		<li>文字文字文字文字文字文字</li>
		<li>文字文字文字文字文字文字</li>
		<li>文字文字文字文字文字文字</li>
		<li>文字文字文字文字文字文字</li>
	</ul>
	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>
	<script>
		my$('btn1').onclick = function () {
			my$('ul1').style.backgroundColor = "yellow";
		}
	</script>
</body>
</html>
```

### 阻止超链接进行跳转

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>阻止超链接进行跳转</title>
</head>
<body>
	<a href="http://www.baidu.com" onclick="alert('阻止跳转1'); return false;">百度</a>
	<br>
     <!--注意一下！！！！ return f1()-->
	<a href="http://www.baidu.com" onclick="return f1()">百度</a>
	<br>
	<a href="http://www.baidu.com" id="a1">百度</a>

	<script>
		function f1() {
			alert('阻止跳转2'); 
			return false;
		}
	</script>
	
	
	<script>
		document.getElementById('a1').onclick = function () {
			alert('阻止跳转3'); 
			return false;
		};
	</script>

</body>
</html>
```

### 小图切换大图

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>小图切换大图</title>
</head>
<body>
	<a href="../images/1.jpg" id="ak"><img src="../images/1-small.jpg" alt=""></a>
	<img src="" alt="" id="big">

	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>
	<script>
		my$('ak').onclick = function () {
			// 注意：直接使用了自身的属性
			my$('big').src= this.href;
			return false;
		}
	</script>
</body>
</html>
```

### 美女相册效果

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<!-- 
		1. 多个并列的东西使用无序列表进行实现
		2. 列表左浮动可以实现并列，此时处于脱标状态，在父级元素添加
	 -->
	<meta charset="UTF-8">
	<title>美女相册</title>
	<style>
		* {
			padding: 0;
			margin: 0;
		}
		body {
			background-color: #ccc;
		}
		ul {
			overflow: hidden;
		}
		li {
			display: inline;
			margin: 20px 10px 20px 10px;
			list-style: none;
			float: left;
		}
		.dis {
			/*border: 1px solid yellow;*/
			margin-left: 20px;
		}

		.dis img {
			/*border: 1px solid red;*/
			display: block;
			margin: 20px 0px 20px 0px;
		}
	</style>
</head>

<body>
	<h2>美女相册</h2>

	<ul id="imageallery">
		<li>
			<a href="../images/1.jpg" title="美女A">
				<img src="../images/1-small.jpg" width="100" alt="" title="美女A">
			</a>
		</li>

		<li>
			<a href="../images/2.jpg" title="美女B">
				<img src="../images/2-small.jpg" width="100" alt="" title="美女B">
			</a>
		</li>

		<li>
			<a href="../images/3.jpg" title="美女C">
				<img src="../images/3-small.jpg" width="100" alt="" title="美女C">
			</a>
		</li>

		<li>
			<a href="../images/4.jpg" title="美女D">
				<img src="../images/4-small.jpg" width="100" alt="" title="美女D">
			</a>
		</li>
			
	</ul>

	<div class="dis">
		<img src="../images/placeholder.png" width="450" alt="" id="images">
		<p id="des">
			请选择一幅图片
		</p>
	</div>

	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>
	<script>
		var aObjs = my$('imageallery').getElementsByTagName('a');
		for(var i = 0; i < aObjs.length; i ++){
			aObjs[i].onclick = function () {

				my$('images').src = this.href;
				my$('des').innerText=this.title;
				return false;
			}
		}
	</script>
</body>

</html>
```

### 隔行变色

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>隔行变色</title>
</head>
<body>
	<input type="button" value="隔行变色" id="btn1">
	<ul id="ul1">
		<li>红旗</li>
	  	<li>五菱宏光</li>
	  	<li>奔驰</li>
	  	<li>兰博基尼</li>
	  	<li>哈弗</li>
	  	<li>奥拓</li>
	  	<li>奥迪</li>
	  	<li>悍马</li>
	</ul>

	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>

	<script>	
		my$('btn1').onclick = function () {
			var liObjs = my$('ul1').getElementsByTagName('li');
			for(var i = 0; i < liObjs.length; i ++){
				// 这个写法值得借鉴
				liObjs[i].style.backgroundColor = (i%2 == 0 ? "red":"yellow");
			}
		}

	</script>
</body>
</html>
```

### 鼠标移动注册事件

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>注册鼠标事件</title>
</head>
<body>
	<ul id="ul1">
		<li>红旗</li>
	  	<li>五菱宏光</li>
	  	<li>奔驰</li>
	  	<li>兰博基尼</li>
	  	<li>哈弗</li>
	  	<li>奥拓</li>
	  	<li>奥迪</li>
	  	<li>悍马</li>
	</ul>

	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>

	<script>	
		var liObjs = my$('ul1').getElementsByTagName('li');
		for(var i = 0; i < liObjs.length; i ++){
			liObjs[i].onmouseover = function () {
				this.style.backgroundColor = "yellow";
			}
			liObjs[i].onmouseout = function () {
				this.style.backgroundColor = "white";
			}
		}

	</script>
</body>
</html>
```

### innerText和textContent的区别

```js

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <style>
    div {
      width: 200px;
      height: 150px;
      border: 2px solid red;
    }
  </style>
</head>
<body>

<input type="button" value="设置值" id="btn"/>
<div id="dv">哦,太神奇了</div>

<script src="common.js"></script>
<script>
  //设置标签中的文本内容,应该使用textContent属性,谷歌,火狐支持,IE8不支持
  //设置标签中的文本内容,应该使用innerText属性,谷歌,火狐,IE8都支持

  //如果这个属性在浏览器中不支持,那么这个属性的类型是undefined
  //判断这个属性的类型 是不是undefined,就知道浏览器是否支持

  //兼容代码

  //设置任意的标签中间的任意文本内容
  function setInnerText(element,text) {
    //判断浏览器是否支持这个属性
    if(typeof element.textContent =="undefined"){//不支持
      element.innerText=text;
    }else{//支持这个属性
      element.textContent=text;
    }
  }

  //获取任意标签中间的文本内容
  function getInnerText(element) {
    if(typeof element.textContent=="undefined"){
     return element.innerText;
    }else{
      return element.textContent;
    }
  }

  //测试

  my$("btn").onclick=function () {
    //console.log(getInnerText(my$("dv")));
    setInnerText(my$("dv"),"哈哈,我又变帅了");
  };





  //点击按钮设置div中的文本内容
  //my$("btn").onclick = function () {
    //设置标签中间的文本内容,应该使用textContent属性
    //my$("dv").textContent="this is div标签";
    //my$("dv").innerText = "啊,这是div";

    //获取标签中间的文本内容
    //console.log(my$("dv").innerText);
    //console.log(my$("dv").textContent);
//  };

</script>
</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>innerText和textContent的区分</title>
	<style>
		div {
			width: 200px;
			height: 200px;
			border: 2px dashed red;
		}
	
	</style>
</head>
<body>
	<input type="button" value="设置值" id="btn1">
	<input type="button" value="获取值" id="btn2">
	<div id="dv">你好，请设置我吧！！</div>
	
	<script>
		function my$(id){
			return document.getElementById(id);
		}
	</script>
	<script>
		function setInnerText(element, text){
			if(typeof element.textContent == "undefined"){
				element.innerText = text;
			}
			else {
				element.textContent = text;
			}
		}

		function getInnerText(element){
			if(typeof element.textContent == "undefined"){
				return element.textContent;
			}else {
				return element.innerText;
			}
		}

	</script>

	<script>

		my$('btn1').onclick = function () {
			setInnerText(my$('dv'),"This is a div标签");
		};

		my$('btn2').onclick = function () {
			alert(getInnerText(my$('dv')));
		};
	</script>
</body>
</html>
```

```js

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <style>
    div{
      width: 300px;
      height: 200px;
      border: 2px dotted red;
    }
  </style>
</head>
<body>
<input type="button" value="显示效果" id="btn"/>
<input type="button" value="显示效果获取" id="btn2"/>
<div id="dv">
  这是div
<p>这是一个p</p>
</div>
<script src="common.js"></script>
<script>

  //总结:如果使用innerText主要是设置文本的,设置标签内容,是没有标签的效果的
  //总结:innerHTML是可以设置文本内容
  //总结:innerHTML主要的作用是在标签中设置新的html标签内容,是有标签效果的

  //总结:想要设置标签内容,使用innerHTML,想要设置文本内容,innerText或者textContent,或者innerHTML,推荐用innerHTML


  //获取的时候:
  //innerText可以获取标签中间的文本内容,但是标签中如果还有标签,那么最里面的标签的文本内容也能获取.---获取不到标签的,文本可以获取
  //innerHTML才是真正的获取标签中间的所有内容


  my$("btn").onclick=function () {
    //my$("dv").innerText="哈哈";//设置文本
    //my$("dv").innerText="<p>这是一个p</p>";//设置html标签的代码

    //my$("dv").innerHTML="哈哈";
    //my$("dv").innerHTML="<p>这是一个p</p>";//设置Html标签的
  };

  //获取
  my$("btn2").onclick=function () {
    //可以获取标签中的文本内容
    //console.log(my$("dv").innerText);
    console.log(my$("dv").innerHTML);
  };
  //结论:
  //如果想要(获取)标签及内容,使用innerHTML
  //如果想要设置标签,使用innerHTML
  //想要设置文本,用innerText,或者innerHTML,或者textContent



</script>
</body>
</html>
```

### 自定义属性的引入(获取 设置 移除)

```js

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>$永远的24k纯帅$</title>
  <style>
    ul{
      list-style-type: none;
      cursor: pointer;
    }
  </style>
</head>
<body>
<ul id="uu">
  <li score="10">助教的数学成绩</li>
  <li score="20">班主任的成绩</li>
  <li score="30">小苏的成绩</li>
  <li score="40">小杰老师成绩</li>
  <li score="50">乔峰成绩</li>
</ul>
<script src="common.js"></script>
<script>

  //html标签中有没有什么自带的属性可以存储成绩的----没有
  //本身html标签没有这个属性,自己(程序员)添加的,----自定义属性---为了存储一些数据

  //在html标签中添加的自定义属性,如果想要获取这个属性的值,需要使用getAttribute("自定义属性的名字")才能获取这个属性的值

  //获取所有的li标签
  var list=document.getElementsByTagName("li");
  for(var i=0;i<list.length;i++){
    list[i].onclick=function () {
        //alert(this.score);//不能
      //可以
      alert(this.getAttribute("score"));
    };
  }
</script>
</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>引入自定义属性</title>
	<style>
		li {
			list-style:  none;
			cursor: pointer;
		}
		
	</style>
</head>
<body>
	<ul>
		<li score="10">111111</li>
		<li score="20">222222</li>
		<li score="30">333333</li>
		<li score="40">444444</li>
		<li score="50">555555</li>
		<li>666666</li>
	</ul>

	<script>
		
		var listObjs = document.getElementsByTagName('li');
		for(var i=0; i< listObjs.length; i++){
			// listObjs[i].score = (i+2)*10;
			listObjs[i].setAttribute('score',(i+2)*10);


			listObjs[i].onclick = function() {
				//必须使用这种方法
				//必须加上this关键字
				alert(this.getAttribute('score'));
			};
		}

	</script>
</body>
</html>
```

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>移除自定义属性</title>
	<style>
		div {
			width: 200px;
			height: 100px;
			background-color: yellow;
		}
		.cls {
			background-color: green;
		}
	</style>
</head>
<body>
	<input type="button" value="移除样式", id="btn1">
	<div id="dv" score="10" class="cls"></div>

	<script>
		document.getElementById('btn1').onclick = function () {
			//不仅可以移除自定义样式
			//还可以移除元素样式
			document.getElementById('dv').removeAttribute('score');
			document.getElementById('dv').removeAttribute('class');
		};
	</script>
</body>
</html>
```

### 案例使用：tab键切换元素

```js
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>复习</title>
	<style>
		* {
			margin: 0;
			padding: 0;
		}
		ul {
			list-style: none;
		}
		.box {
			width: 300px;
			height: 300px;
			border: 1px solid #ccc;
			overflow: hidden;
		}
		.box .hd li {
			display: inline-block;
			width: 70px;
			height: 50px;
			background-color: pink;
			text-align: center;
			line-height: 50px;
			cursor: pointer;
		}
		.box .hd .current {
			background-color: purple;
		}
		
		.box .bd li {
			height: 250px;
			background-color: pink;
			display: none;
		}
		.box .bd .current {
			background-color: purple;
			display: block;
		}
	</style>
</head>
<body>
	<div class="box" id="box">
		<div class="hd">
			<ul>
				<li class="current">体育</li>
				<li>娱乐</li>
				<li>新闻</li>
				<li>综合</li>
			</ul>

		</div>
		<div class="bd">
			<ul>
				<li class="current">体育模块</li>
				<li>娱乐模块</li>
				<li>新闻模块</li>
				<li>综合模块</li>
			</ul>

		</div>
	</div>
	<script>
		//使用索引将两个部分连接在一起
		var box = document.getElementById('box');

		var hd = box.getElementsByTagName('div')[0];
		var listHdObjs = hd.getElementsByTagName('li');

		var bd = box.getElementsByTagName('div')[1];
		var listBdObjs = bd.getElementsByTagName('li');

		for(var i=0; i < listHdObjs.length; i ++){
			
			listHdObjs[i].setAttribute('index',i);

			listHdObjs[i].onclick = function () {
				for(var j=0; j < listHdObjs.length; j++){
					listHdObjs[j].removeAttribute('class');
				}
				this.className = 'current';

				var num = this.getAttribute('index');
				console.log(num);

				for(var k=0; k < listBdObjs.length; k++){

					listBdObjs[k].removeAttribute('class');
				}
				listBdObjs[num].className = 'current';
			}

			
		}
	</script>
</body>
</html>
```



