# 弹性盒子布局

> 弹性盒子布局灵活且自适应，属于H5新特性，值得好好学习

- 弹性盒布局中的条目有两个尺寸：主轴尺寸和交叉轴尺寸，分别对应其 DOM 元素在主轴和交叉轴上的大小。如果主轴是水平方向，则主轴尺寸和交叉轴尺寸分别对应于 DOM 元素的宽度和高度；如果主轴是垂直方向，则两个尺寸要反过来。与主轴和交叉轴尺寸对应的是主轴尺寸属性和交叉轴尺寸属性，指的是 CSS 中的属性 width 或 height。比如，当主轴是水平方向时，主轴尺寸属性是 width，而 width 的值是主轴尺寸的大小。
- 弹性盒布局模型中的 CSS 样式声明分别适用于容器或条目。在下面的内容中会详细的介绍相关的 CSS 属性。首先介绍如何使用弹性盒布局模型进行基本的页面布局。在本文的所有代码示例中，容器的 CSS 类名统一为 flex-container，而条目的 CSS 类名则为 flex-item。所有的示例都可以在CodePen上进行预览。

---
## 浏览器支持
由于弹性盒模型规范本身有过多个不同的版本，因此浏览器对于该规范的支持也存在一些不一致。浏览器一共支持 3 个不同版本规范的语法：
- 新规范：最新版本规范的语法，即"display: flex"。
- 中间版本：2011 年的非官方规范的语法，即"display: flexbox"。
- 老规范：2009 年的规范的语法，即"display: box"。

##  弹性盒布局模型的浏览器前缀形式
```
.flex-container {
 display: -webkit-box;
 display: -moz-box;
 display: -ms-flexbox;
 display: -webkit-flex;
 display: flex;
}
 
.flex-item {
 -webkit-box-flex: auto;
 
-moz-box-flex: auto;
-webkit-flex: auto;
-ms-flex: auto;
 flex: auto;
}
 
.flex-item {
 -webkit-box-ordinal-group: 1;
 -moz-box-ordinal-group: 1;
 -ms-flex-order: 1;
 -webkit-order: 1;
 order: 1;
}
```
