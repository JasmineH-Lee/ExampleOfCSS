# CSS

## 盒子模型

1、width、height 设置的只是盒子内容的宽和高
2、padding值会扩大整个盒子的宽度和高度
3、border的设置也会增加盒子的整体宽高，solid的边框线默认是黑色的
4、外边距叠加：除行内框、浮动框和绝对定位框之外都会产生外边距叠加问题

box-sizing:content-box|border-box|inherit


## 定位（position、float）

CSS有3种基本的定位机制：基本流、浮动和绝对定位

position： static(默认值)、 absolute(绝对定位)、 relative(相对定位)、 fixed、 inherit、 sticky(css3新增position属性)

static: 会忽略top、 right、 bottom、 left和z-index的值

absolute： 相对最近的父级元素（非static）定位，与文档流无关

relative： 相对它本身应该在的位置

fixed: 总是相对body定位

sticky：

使用相对定位时，无论元素是否移动，元素在文档流中会占据原来的空间，只是表现会改变


## 浮动

### 清楚浮动

1、clear属性：left、 right、 both和none，元素的哪些边不挨着浮动框
   添加一个空元素，为其设置clear属性
   缺点：添加了多余的代码

2、为父元素设置浮动
   缺点：父元素的浮动会影响与该父元素同级的下一个元素

3、父元素设置overflow属性
   缺点：当内容溢出时会影响页面表现，IE6不支持

4：伪类 :after

## 布局

固定宽度、流式布局 和 弹性布局

### 流式布局

百分比设置尺寸，缺点当窗口非常小或者非常大的时候列的宽度受到影响会变得很难阅读，视觉效果差。需要设置以em为单位的min-width

### 弹性布局

宽高为百分比，间隔为em(字号)

### 居中

1、center 不建议使用

2、text-align:center

3、vertical-align:middle

4、line-height:

5、margin:0 auto

6、translate(-50%,-50%) + position

6、绝对定位居中 + position:relative(父元素)

7、视口居中 + 子元素position:fixed

8、响应式 宽高百分比、min-

9、偏移  margin：auto 设置position + 四个偏移量

10、溢出  overflow

11、调整尺寸 resize属性

12、图像  height:auto

13、可变高度 高度必须定义

14、负margin  确切指导宽高，负margin是宽高的一半

15、Table-cell

16、Flex-box

### Flex

块元素 {
	display:flex;
}
行内元素 {
	display:inline-flex;
}

容器：

flex-direction(主轴方向): row | row-reverse | column | column-reverse

flex-wrap(换行): nowrap | wrap | wrap-reverse 

flew-flow(简写): <flex-direction> || <flex-wrap>

justify-content(主轴上的对齐方式): flex-start | flex-end | center | space-between | space-around;

align-items(交叉轴上如何对齐): flex-start | flex-end | center | baseline | stretch

align-content(多根轴线对齐方式):flex-start | flex-end | center | space-between | space-around | stretch;

项目：
order(排列顺序):

flex-grow(放大比例):

flex-shrink(缩小比例):

flex-basis():

flex(grow shrink basis简写):

align-self(单个项目对齐方式不同):auto | flex-start | flex-end | center | base-line | stretch;


## CSS优先级

0 标签选择器+ 伪类选择器

1 类选择器

2 ID选择器

3 通用选择器 组合子 否定伪类

4 内联样式

!import 优先级虽高但是不要轻易使用

Always 优化考虑使用样式规则的优先级而不是!import
Only 在需要覆盖全站或者外部CSS的特定页面中使用
Never 在全站使用!import
Never 在插件中使用

取而代之：

1、更好的利用CSS级联属性

2、使用更具体的规则


## 文字溢出

text-overflow: ellipsis;
overflow: hidden;
white-space: nowrap;
