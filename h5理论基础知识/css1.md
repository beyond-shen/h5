# CSS样式1
## 语义化
### 定义

语义化是指用合理HTML标记以及其特有的属性去格式化文档内容。通俗地讲,语义化就是对数据和信息进行处理,使得机器可以理解。

    　　HTML是一种对文本内容进行结构和意义（或者说“语义”）进行补充的方法。在做前端开
    发的时候要记住：HTML告诉我们一块内容是什么（或其意义），而不是它长的什么样子。当我们提到“语义标记”的时候，
    我们所说的HTML应该是完全脱离表现信息的，其中的标签应该都是语义化地定义了文档的结构。要掌握html中各个标签的语义。
### 好处
1. 去掉或样式丢失的时候能让页面呈现清晰的结构
2. 便于访客的易用性，方便其他设备解析以意义的方式渲染页面。
3. 有助于搜索引擎的友好，便于索引
4. 你的页面是否对爬虫容易理解非常重要,因为爬虫很大程度上会忽略用于表现的标记,而只注重语义标记.

   因此,如果页面文件的标题被标记,而不是,那么这个页面在搜索结果的位置可能会比较靠后.除了提升易用性外,语义标记有利于正确使用CSS和JavaScript,因为
其本身提供了许多“钩钩”来应用页面的样式与行为.SEO主要还是靠你网站的内容和外部链接的。
5. 便于团队开发和维护

注：事实上SEO最有效的一种办法，就是对网页的HTML结构进行重构，实质上就是语义化。

### 原则
1. 重语义的地方多用有语义的标签，比如 h 和 p 等等，少用没有语义的标签比如 div span 等等。
2. 如果有地方可以用p 又可以用div， 优先选用 p标签（结构更清晰，特别是文字段落）。
3. 少用纯样式标签 比如 b u font，可以运用css样式。 如果有强调的地方，可以考虑 strong em 等 有强调语义的标签。
## CSS基本了解
CSS通常称为CSS样式表或层叠样式表（级联样式表），主要用于设置HTML页面中的文本内容（字体、大小、对齐方式等）、
图片的外形（宽高、边框样式、边距等）以及版面的布局等外观显示样式。
### 作用
1. CSS 主要目的： 控制网页中元素的样式
2. 优势：让ＨＴＭＬ结构和样式分离出来。
3. 可以让我们专注结构。代码更少，语义更好，搜索更容易。
### 规则
使用HTML时，需要遵从一定的规范。CSS亦如此，要想熟练地使用CSS对网页进行修饰，首先需要了解CSS样式规则，具体格式如下:

选择器{属性1:属性值1; 属性2:属性值2; 属性3:属性值3;}

在上面的样式规则中，选择器用于指定CSS样式作用的HTML对象，花括号内是对该对象设置的具体样式。其中，属性和属性值以“键值对”的形式出现，属性是对
指定的对象设置的样式属性，例如字体大小、文本颜色等。属性和属性值之间用英文“:”连接，多个“键值对”之间用英文“;”进行区分。
### 块元素(block)和行内元素区别
1. 块内元素：包括h1-h6,p,div,hr,br,ul,ol,dl等，独占一行或多整行。行内元素：包括b,strong,span,i,u,s,em,ins,del,a等，有独立的区域，仅仅靠
自身的字体大小和图像尺寸来支撑结构。
2. 块元素可以包含行内元素和块元素，但是行内元素不可以。
3. 块元素可以设置高度，宽度和对齐灯元素。但是行内元素一般不可以。
注：img,input,td特殊，虽然不独占一行，但是可以设置属性。
### 几种选择器(使用英文字符，写在style标签里面的，style在head里面的)
1. 标签选择器:用html标记名称作为选择器

   1. 格式：标签名{属性1:属性值1;属性2:属性值2;}----键值对之间用:,多个属性之间用；。
   2. 标记选择器最大的优点是能快速为页面中同类型的标记统一样式，同时这也是他的缺点，不能设计差异化样式
2. 类选择器：用“.”进行标识，后紧跟类名，可多个使用

   1. 格式:.classname{属性1:属性值1;属性2:属性值2;}
   2. 类选择器最大的优势是可以为元素对象定义单独或相同的样式。
   3. 使用:
```html
   <p class="classname">这是一个被优化的段落</p>
```
3. id选择器：使用“#”进行标识，后紧跟id名

   1. #idName{属性1:属性值1;属性2:属性值2;}
   2. 在一个html中id属性唯一
   3. 使用:
```html
   <h1 id="idName">这识一个被优化的标题</h1>
```
4. 通配选择器：用“*”号来表示，是所有选择其中作用范围最广的，能匹配页面的所有元素

   1. 格式: * {属性1:属性值1;属性2:属性值2;}
   2. 使用：清除当前文档中所有元素的外边距和内边距
```html
   * {
   margin:0;
   padding:0;
   }
```
5. 后代选择器：后一个元素必须属于前一个元素的后代元素，用空格分开祖辈和后辈

   1. 使用：
```html
    div p {
    width: 100px;
    height: 100px;
}
div span {
    color:red;
}

<div>
    <p>
       <span></span>
    </p>
</div>
```
   * 注意：后代选择器是从右向左的
   
6. 交集选择器：多个选择器共用
```html
div p.boss {
    color:red;
}
<div>
    <p class="boss">刘备</p>
    <p>关羽</p>
    <p>张飞</p>
</div>
```
7. 并集选择器：将共同的样式抽出来，用“,”隔开
```html
p, span {
    color: red;
}
<div>
    <p>张三</p>
    <p>李四</p>
    <span>我是span</span>
</div>
```
8. 伪类选择器：
   * 格式：　类名/标签名:样式{属性:属性值;}
```   
顺序如下:
1. .one:link{}------标签原本样式
2. .one:visited{}-----访问后的样式
3. .one:hocer{}------鼠标放在标签上的样式
4. .one:active{}-----当点击标签时的样式
```
**注**：不只有a标签可以使用，都可以
