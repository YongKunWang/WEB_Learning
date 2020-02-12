# MDN_CSS_01

## CSS简介

CSS：层叠样式表

语法构成：

```css
h1 {
    color:red;
    font-size:5em;
}
/*
selector {
property: value;
}
*/
```

## CSS选择器基础

1. 类选择器
2. id选择器
3. 多类选择器 （这个是说在定义的时候空格隔开）
4. 通配符选择器
5. 交集选择器 
6. 并集选择器 (逗号)
7. 后代选择器 （包含选择器 使用空格隔开）
8. 子元素选择器 （父元素 > 子元素）

```css
/*选择器实例*/
h1 {
	color: red;
}

/*使用逗号分隔符可使用多个选择器*/
p, li {
	color: green;
}
/*改变元素的默认行为*/
li {
	/*list-style-type: none;*/
	list-style-type:square;
}
/*类选择器使用点来选择*/
.special {
	color: orange;
	font-weight: blod;
}
/*选中special类的li元素*/
li.special {
	color: red;
	font-weight: bold;
}

/*根据元素在文档中的位置来确定*/
em {
	color: rebeccapurple;
}
/*只有li嵌套的em元素变色*/
li em {
	color: red;
}
/*相邻兄弟组合器：只装饰h1后面的p标签，且两者具有相同的父标签*/
h1 + p {
	font-size: 200%;
}

/*
	注意： 在CSS定义中，a:hover 必须被置于 a:link 和 a:visited 之后，才是有效的。
	注意： 在 CSS 定义中，a:active 必须被置于 a:hover 之后，才是有效的。
	注意：伪类的名称不区分大小写。

 */

/*未访问*/
a:link {
	color:pink;
}
/*已访问过*/
a:visited {
	color: purple;
}

/*鼠标悬停*/
a:hover {
	text-decoration: none;
}
/*点击时*/
a:active {
	color: red;
}




```

## CSS结构

- 外部样式表

  - 通过创建并且引入CSS外部文件

- 内部样式表

  - 在`<head></head>`中引入`<style></style>`

  ```css
  <!DOCTYPE html>
  <html lang="en">
  <head>
  	<meta charset="UTF-8">
  	<title>CSS结构练习</title>
  	<style>
  		h1 {
  			color: blue;
  			background-color: yellow;
  			border: 1px solid black;
  		}
  		p {
  			color: red;
  		}
  	</style>
  </head>
  <body>
  	<h1>Hello World!</h1>
      <p>This is my first CSS example</p>
  </body>
  </html>
  ```

- 内联样式表

  ```css
  <!DOCTYPE html>
  <html lang="en">
  <head>
  	<meta charset="UTF-8">
  	<title>内联样式表</title>
  </head>
  <body>
  	<h1 style="color:blue; background-color: yellow border:1px solid black">Hello World!!!</h1>
  	<p style="color: red">This is my first CSS example</p>
  </body>
  </html>
  ```

内联样式表难以维护；使得代码难以阅读

## 常见属性和值

1. `font-size`:字体大小，从1~7  默认为3

2. `width`:`content`的宽度

   - `px`绝对长度单位

   - `em`

     - 浏览器默认`16px` 所以`1em = 16px`

     - 简化计算：`1em = 10px`

       ```css
       body {
           font-size:62.5%; /*16px x 62.5% = 10px*/
       }
       ```

     - 缺点:

       - `em`不是固定的
       - `em`会继承父级元素的字体的大小`参考物是父级元素的font-size`
       - 如果：一个设置了`font-size:1.2em`；另一个设置了`font-size:1.2em`；在设置一个`font-size:1.2em`。其结果为`1.2x1.2x1.2 = 1.728em`

   ```css
   <!DOCTYPE html>
   <html lang="en">
   <head>
   	<meta charset="UTF-8">
   	<title>CSS作用规则</title>
   	<style>
   		.special {
   			color: blue;
   		}
   		p {
   			color: red;
   		}
   		.pxclass {
   			width: 160px;
   			border: 1px solid black;
   		}
   		.emclass {
   			width: 10em;
   			border: 1px solid black;
   		}
   	</style>
   </head>
   <body>
   
   	<h1>CSS作用规则</h1>
   	<!-- 显示红色，后面的样式覆盖前面的样式 -->
   	<p class="blue">What Color is I</p>
   
   	<p class="pxclass">px，em演示</p>
   	<p class="emclass">px，em演示</p>
   </body>
   
   </html>
   ```

   ![](../media/02_盒子模型pxem.png)

   ```css
   <!DOCTYPE html>
   <html lang="en">
   <head>
   	<meta charset="UTF-8">
   	<title>CSS作用规则</title>
   	<style>
   		body {
   			font-size: 62.5%;
   		}
   		.special {
   			color: blue;
   		}
   		p {
   			color: red;
   		}
   		.pxclass {
   			width: 100px;
   			border: 1px solid black;
   		}
   		.emclass {
   			width: 10em;
   			border: 1px solid black;
   		}
   	</style>
   </head>
   <body>
   
   	<h1>CSS作用规则</h1>
   	<!-- 显示红色，后面的样式覆盖前面的样式 -->
   	<p class="blue">What Color is I</p>
   
   	<p class="pxclass">px，em演示</p>
   	<p class="emclass">px，em演示</p>
   </body>
   
   </html>
   ```

   ![](../media/03_盒子模型pxem1.png)

   

   ![](../media/01_盒子模型.png)

3. `background-color`:背景颜色

4. `color`:字体颜色

5. `border`: `border-width border-style border-color`

## 盒子的稳定性布局

优先使用：	`width` 没有出现问题

其次使用： `padding` 会影响盒子的大小，`padding` 会撑开盒子，需要进行加减计算

最后使用：`margin`  会出现内外边距合并的问题

## 盒子圆角

```CSS
border-radius : 50%;
```

## 盒子阴影

```css
box-shadow: 水平阴影（rquired） 垂直阴影(rquired) 模糊距离（虚实）  阴影尺寸（影子大小）  阴影颜色  内/外阴影；
```

## 浮动

标准流会撑开盒子！！！！

`float`

我们引入浮动后，再进行有关浮动布局时，我们会定义一个父元素，且父元素给定宽度和高度，然后里面的子元素进行浮动布局。

例子可见常规布局中的部分！！

`float`

### 清除浮动

准确的说不是清除浮动，而死清除浮动后造成的影响

而现在我们又要清除浮动？

在引入浮动概念进行布局的时候，使用父元素且给定宽和高是不适用的！！

比如动态网页的显示的数据长短不一，这是使用父元素+浮动布局会很不好看的！！

例子：

```html
<!-- 案例5：父元素不给宽高且浮动 -->
	<!-- 
		当未给父元素宽度和高度的时候，在标准流中，子元素会撑开父元素
		但当子元素浮动之后，会脱标，此时会形成一条线！！
	 -->
	<div class="ex5">
		<div class="father">
			<div class="son1"></div>
			<div class="son2"></div>
		</div>
	</div>
```

```css
.ex5 .father{
	border: 4px solid red;
}

.ex5 .father .son1 {
	width: 300px;
	height: 300px;
	background-color: purple;
	border: 1px solid green;
	float: left;
}

.ex5 .father .son2 {
	width: 300px;
	height: 300px;
	background-color: purple;
	border: 1px solid green;
	float: left;

}
```



## 高度剩余法

文字默认上对齐

可以不通过调整`padding`和`margin`的值，而直接设置宽度来获得间距

