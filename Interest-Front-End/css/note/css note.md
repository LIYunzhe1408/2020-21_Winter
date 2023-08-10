1.基础选择器：不能差异化设计同类型标签

2.类选择器：.red{

​	color: red;

}

<div class = "red">XXX</div>



3.多类名选择器：

一个标签内部只能有一个class

class = “xxx xxx”；



4.id选择器：

#pink{color:blue;}

<p id = "pink">xxx</p>

 *元素的id是唯一的；类选择器好比是人类的名字，可以重复使用；

id选择器相当于身份证号码，不能重复使用；

区别：使用次数



5. 通配符选择器

   *选择所有标签；

   *{xxx}

   不要随便使用

6. 基础选择器总结：

    

   | 选择器       | 作用                          | 缺点                   | 使用情况 | 用法             |
   | ------------ | ----------------------------- | ---------------------- | -------- | ---------------- |
   | 标签选择器   | 可以选出所有相同的标签，比如p | 不能差异化选择         | 较多     | p{color:red;}    |
   | 类选择器     | 可以选出1个或多个标签         | 可以根据需求差异化选择 | 非常多   | .nav{color:red;} |
   | id选择器     | 一次只能选择1个标签           | 只能使用一次           | 不推荐   | #nav{color:red;} |
   | 通配符选择器 | 选择所有标签                  | 选择的太多部分不需要   | 不推荐   | *{color:red;}    |

   尽量少用id，通用选择器；

   不使用无具体语义的选择器div，span

   

   #### 

   

   

   # 字体样式

   

   ## 1.font字体

   #### 	1.1 font-size大小

   | 相对单位长度     | 说明                           |
   | ---------------- | ------------------------------ |
   | em               | 相对于当前对象内文本的字体尺寸 |
   | px               | 像素、最常用、推荐使用         |
   | **绝对单位长度** | **说明**                       |
   | in               | 英寸                           |
   | cm               | 厘米                           |
   | mm               | 毫米                           |
   | pt               | 点                             |

   -以后基本就用px了。

   -谷歌浏览器默认文字大小为16px。

   -要有明确值。一般给body中的默认字体大小为16px

   #### 	1.2 font-family 字体

   作用：设置字体

   p{font-family:"微软雅黑";}

   宋体；黑体 etc

   Arial,"Microsoft YaHei"

   可以同时指定多个字体，中间以逗号隔开，如果浏览器不支持第一个字体会依次往下

   中文字体一定要引号；多个单词组成也要引号
   
   -unicode：取代中文
   
   ​	![](C:\Users\Jonas Li\Desktop\css\note\png\css字体unicode.png)
   
   #### 	1.3 font-weight: 字体粗细
   
   语法：font-weight：normal|bold; 700 = bold 不要加单位 数值支持100-900 400 = normal
   
   #### 	1.4 font-style：字体风格 倾斜问题
   
   -可用i，em标签实现
   
   -font-style: normal|italic;
   
   #### 	1.5 font：综合设置字体样式
   
   .选择器{ font: font-style 	 font-weight	 font-size/line-height 	 font-family;}
   
   必须严格按照顺序来 size和family 一定不能省略
   
   #### 	1.6 总结
   
   ##### 外观属性：
   
   1.预定义颜色：red, green, blue......
   
   2.#000000 黑色 #FFFFFF 白色；rrggbb 可以用吸管吸取
   
   3.RGB：rgb(xxx,xxx,xxx)
   
   ##### 文本水平方式：
   
   text-align:center;
   
   ##### 行间距：
   
   一般情况下，行距比字号大7-8像素左右
   
   line-height:24px;
   
   真正的行间距应用于p中。
   
   ##### 首行缩进：
   
   text-indent: xx em;
   
   这里的em是宽度单位
   
   ##### 文本装饰：
   
   text-decoration: none;
   
   none: 取消下划线
   
   underline:加下划线
   
   blink:几乎不用
   
   overline: 几乎不用
   
   line-through:几乎不用
   
   

# 导航栏

css复合选择器-标签的显示模式-行高

### 1.复合选择器

两个或多个基础选择器通过不同组成而成

#### 1.1后代选择器（重点）

· 概念：
	后代选择器又称为包含选择器

· 作用：

​	用来选择元素或元素组的子孙后代

· 写法：父级 子级{属性：属性值； 属性：属性值；}

​	.class h3{color: red;  font-size:16px;} 

#### 1.2 子元素选择器	>

只能选择作为某元素子元素的元素

.class **>** h3{color: red; font-size: 14px;}

#### 1.3 交集选择器	.

既是又是 p和class的交集

p**.**class{xxxxx;}

用的相对比较少

#### 1.4 并集选择器	,

p和class的并集,用于集体声明，逗号隔开  

p,

.class{xxxxx}

#### 1.5 链接伪类选择器

·类选择器：      .demo{}

·伪类选择器： 	 :link{}

作用：向某些元素添加特殊效果

- a:link     未访问的链接
- a:visited 已访问的链接
- **a:hover  鼠标移动到链接上**
- a:active  选定的链接

lvha 顺序不要颠倒

实际工作中要给nav单独指定样式

一般写法如下：

![](C:\Users\Jonas Li\Desktop\css\note\png\屏幕截图 2021-01-07 152812.png)

 ![](C:\Users\Jonas Li\Desktop\css\note\png\选择器小结.png)

### 2.标签显示模式

- 标签的三种显示模式
- 特点与区别
- 转化方式

#### 2.1 什么是标签显示模式

- div span这种独有的显示模式
- 标签类型： 块元素 & 行内元素

#### 2.2 块元素 block-level

- h1~h6 \ p \ div \ ul \ ol \ li

- 特点：1.自己独占一行

2. 高度、宽度、外边距以及内外边距都可以控制
3. 宽度默认是父级宽度的100%
4. 是一个容器，里面可以放行内或者块级元素

- 注意：

  只有 文字 才能组成段落，因此 p 里面不能放块级元素，特别是p 不能放div

  同理h1 h2 h3 h4 h5 h6 dt哦都是文字类块级标签，不能放其他块级元素



#### 2.3 行内元素 inline-level

a  strong  b  em  i  del  s  ins  u  span

- 特点：

  1. 相邻行内元素在一行上，一行可以显示多个
  2. 高、宽直接设置是无效的
  3. 默认宽度就是它本身内容的宽度
  4. **行内元素只能容纳文本或其他行内元素**

  - 链接里面不能再放链接
  - 特殊情况a里面可以放块级元素，但是给a转换一下块级模式最安全

####  2.4行内块元素 inline-block

- img input td
- 特点：1. 和相邻行内元素在一行上，但是之间会有空白缝隙，一行可以显示多个
  2. 默认宽度就是它本身的宽度
  3. 高度、行高、内外边距都可以控制

####  2.5三种模式区别

![](C:\Users\Jonas Li\Desktop\css\note\png\三种模式总结区别.png)

####  2.6标签显示模式转换

- 块转行内：display:inline;
- 行内转块：display:block;
- 块、行内元素转换为行内块：display:inline-block;