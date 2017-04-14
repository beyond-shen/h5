# html的基本标签
## 例子
```html
<!DOCTYPE>
<html>  -->html是一个双标签 开始标签
<head>
<meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
<title></title> -->可能是标题
</head>
<body>-->用来存放页面中的内容
 你的第一个HTML页面
</body>
</html> -->结束标签
```
## <!--注释--->

**用法**：一些解释却不希望被网页显示，或者使用注释标签来隐藏浏览器不支持的脚本也是一个好习惯。

## 最基础的tag

### <!DOCTYPE> 

* 文档类型声明
* 必须使用在html标签前面
* 文档以h5标准解析

### html标签

```html
<html></html>
```
* 此元素可告知浏览器其自身是一个 HTML 文档。

### meta标签

```html
<meta/>
```
1. 设置页面编码格式，关键字，以及页面的描述
2. 在 HTML 中，<meta> 标签没有结束标签。在 XHTML 中，<meta> 标签必须被正确地关闭。

[meta](http://www.w3school.com.cn/tags/tag_meta.asp)

### <title></title> 

  1. 可定义文档的标题。
  2. 浏览器会以特殊的方式来使用标题，并且通常把它放置在浏览器窗口的标题栏或状态栏上。同样，当把文档加入用户的链
接列表或者收藏夹或书签列表时，标题将成为该文档链接的默认名称。
  3. 属性:lang:规定元素中内容的语言代码。

### head标签
```html
<head></head>
```
[head](http://www.w3school.com.cn/tags/tag_head.asp)

### body标签

页面的主体部分


## 一些常用标签
```html
1. <p>这是一个段落</p>
2. <h1>这是一个h１标题</h1>　　　h1-h6
3. <hr/>－－水平线　　　<br/>－－换行
4. <strong>加粗</strong>
5. <em>倾斜</em>
6. <ins>下划线</ins>
7. <del>删除线</del>
8. <img src="路径/x.jpg" title="标题"　alt="图片不正常时显示的文字内容">
9. <a href="url"　target="_self(默认本窗口打开)/_blank(新窗口打开)">链接提示</a>
10. 锚点链接：快速定位到目标内容
   1. 用标签a创建超文本链接--------- <a href="">第一段</a>
   2. 用id给要跳转的位置进行标记----- <p id="p1">第一段</p>
   3. 标签a中的href="#id"--------- <a href="#p1">第一段<a>
11. 特殊字符
   * &nbsp;-----空格符--
   * &lt;-------“<”
   * &gt;-------“>"
12. list
   1. 无序列表：<ul><li>第一</li><li>第二</li></ul>
   注：<li></li>之间相当于一个容器，可以容纳所有元素。但是<ul></ul>中只能嵌套<li></li>，直接在<ul></ul>标记中输入文字的做法是不被允许。
   2. 有序列表：<ol><li>一</li><li>二</li></ol>
   注:同１
   3. 自定义列表
 　 　<dl>
         <dt>名词1</dt>
         <dd>名词1解释1</dd>
         <dd>名词1解释2</dd>

         <dt>名词2</dt>
         <dd>名词2解释1</dd>
         <dd>名词2解释2</dd>
     </dl>
13. 表格:
    <table>
         <tr>
          <td>单元格内的文字</td>
                ...
         </tr>
          ...
    </table>
    属性：
       1. border:设置表格的边框(默认为０无边框)
       2. cellspacing:设置单元格和单元格之间的空白间距(默认为２px)
       3. cellpadding:设置单元格内容和单元格边框之间的空白间距(默认为１px)
       4. width:设置表格宽度。
       5. height:设置表格高度。
       6. align:设置对齐格式－－center(居中)---left(左对齐)---right(右对齐)
       7. colspan(列合并)　＋　rowspan(行合并)  注：用于td标签的属性，属性值即为要合并的行数/列数。
14. <caption>这是个表格标题</caption>： caption 标签必须紧随 table 标签之后。您只能对每个表格定义一个标题。通常这个标题会被居中于表格之上。
15. <th>强调的单元格</th>
    　　
```
