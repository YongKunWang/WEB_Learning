# MDN_HTML_03

## HTML中的图片

将一幅图片加载到网页上：

```html
<img src="" alt="" width="" heigth="" title="">
```

- `src`的作用：图片资源的位置所在，推荐本地文件
- `alt`的作用：
  - 给图片一个备选的描述文本
  - 文件路径出错
  - 浏览器不支持图片显示
- 图片的宽度`width`和高度`height`问题：
  - 不推荐使用html来改变图片的尺寸，而是应该使用`CSS`
- 图片的标题`title`：
  - 鼠标的悬停提示

## 图片添加描述信息

```html
<div class="figure">
	<img src="" alt="">
    <p>图片描述</p>
</div>
```

这种方法是可以实现的；但是从语义上来讲两者没有什么关系

语义化元素：

```html
<figure>
    <img src="" alt="">
    <figcaption>图片内容描述</figcaption>
</figure>
```

## WEB网页中的音频嵌入

```html
<video src="" controls></video>
```

