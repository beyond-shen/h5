# 字体的css相关属性
## font
### font-size
  **font-size**属性用于设置字号，该属性的值可以使用相对长度单位，也可以使用绝对长度单位。其中，相对长度单位比较常用，
推荐使用像素单位px，绝对长度单位使用较少。
1. em:相当于当前对象内文本的字体尺寸
### font-family

**font-family**属性用于设置字体。网页中常用的字体有宋体、微软雅黑、黑体等，例如将网页中所有段落文本的字体设置为微软雅黑，可以使用如下CSS样式代码：
```html
p {font-family: “宋体”,“微软雅黑”;}
```
可以同时指定多个字体，**中间以逗号隔开**，表示如果浏览器不支持第一个字体，则会尝试下一个，直到找到合适的字体。

注意如下:
* 用英文状态下的逗号隔开
* 中文字体需要加英文状态下""，英文字体名位于中文字体名前。
* 如果字体名中包含空格、#、$等符号，则该字体必须加英文状态下的单引号或双引号，例如font-family: “Times New Roman”;
* 尽量使用默认字体
* 多使用unicode对中文进行编码：在 CSS 中设置字体名称，直接写中文是可以的。但是在文件编码（GB2312、UTF-8 等）不匹配时会产生乱码的错误。为此，在 CSS 直接使用 Unicode 编码来写字体名称可以避免这些错误。使用 Unicode 写中文字体名称，浏览器是可以正确的解析的(使用工具转换)。

### font-weight

**font-weight**属性用于定义字体的粗细，其可用属性值：**normal**、bold、**bolder**、lighter、**100~900（100的整数倍）**。

### font-style
**font-style**属性用于定义字体风格，如设置斜体(italic)、倾斜(oblique)或正常字体(normal)。
### font综合设置
1. 至少要有字号，字体２项
2. 要有顺序　中间用“空格”隔开:
```html
选择器 {
  font: font-style font-weight font-size/line-height font-family;
}
```

## Color:定义文本颜色
1. 纯色：red,pink,purple等
2. #+6个16进制：＃ff00ff－－－注意：红绿蓝３种组合，每一种不超过255(2位２进制为１种)
3. rgb(红,绿,蓝)：rgb(233,23,142)---其中的数值可与16进制转换
4. rgb(10%,20%,50%)---需要注意的是，如果使用RGB代码的百分比颜色值，取值为0时也不能省略百分号，必须写为0%。

## 字间距：letter-spacing

**letter-spacing**属性用于定义字间距，所谓字间距就是**字符与字符之间**的空白。其属性值可为不同单位的数值，允许使用**负值**，默认为normal。

## 单词间距 word-spacing

**word-spacing**属性用于定义**英文单词之间**的间距，对**中文字符**无效。和letter-spacing一样，其属性值可为不同单位的数值，允许使用负值，默认为normal。

注意：**word-spacing**和**letter-spacing**均可对英文进行设置。不同的是**letter-spacing**定义的为字母之间的间距，而**word-spacing**定义的为英文单词之间的间距。

## 行间距　line-height(基线之间的间距)

**line-height**属性用于设置行间距，就是行与行之间的距离，即**字符的垂直间距**，一般称为行高。line-height常用的属性值单位有三种，分别为像素px，相对值em和百分比%，实际工作中使用最多的是像素px。
![](http://i1.piimg.com/1949/304c3161956886fe.png)

从上到下四条线分别是顶线、中线、基线、底线，很像才学英语字母时的四线三格，我们知道vertical-align属性中有top、middle、baseline、bottom，就是和这四条线相关。尤其记得基线不是最下面的线，最下面的是底线。
注意：
* 行高是指上下文本行的基线间的垂直距离，即图中两条红线间垂直距离。
* 行距是指一行底线到下一行顶线的垂直距离，即第一行粉线和第二行绿线间的垂直距离。

## 文本修饰　text-decoration

**text-decoration**属性用于设置文本的默认(none),下划线(underline)，上划线(overline)，删除线(line-through)等装饰效果。
**注意**：可多个赋值,中间用空格隔开
```html
text-decoration: underline overline line-through;
```
## 文本对齐
### 水平对齐　text-aligen

text-align属性用于设置文本内容的水平对齐，相当于html中的align对齐属性。
1. left：左对齐（默认值）
2. right：右对齐
3. center：居中对齐

### 垂直对齐　vertial-align(使用于行内元素)

vertical-align 常用属性值：
* baseline： 将支持valign特性的对象的内容与基线对齐
* sub： 垂直对齐文本的下标
* super： 垂直对齐文本的上标
* top： 将支持valign特性的对象的内容与对象顶端对齐
* text-top： 将支持valign特性的对象的文本与对象顶端对齐
* middle： 将支持valign特性的对象的内容与对象中部对齐
* bottom： 将支持valign特性的对象的文本与对象底端对齐
* text-bottom： 将支持valign特性的对象的文本与对象顶端对齐
注意：要想垂直居中就要用到line-height=容器height

### 首行缩进　text-indent

**text-indent**属性用于设置首行文本的缩进，其属性值可为不同单位的数值、em字符宽度的倍数、或相对于浏览器窗口宽度的百分比%，允许使用**负值**, 建议使用**em作为设置单位**。

## 其他
### 空白字符处理　white-space

* normal：常规（默认值），文本中的空格、空行无效，满行（到达区域边界）后自动换行。
* pre：预格式化，按文档的书写格式保留空格、空行原样显示。
* nowrap：空格空行无效，强制文本不能换行，除非遇到换行标记。内容超出元素的边界也不换行，若超出浏览器页面则会自动增加滚动条。
### 自动换行　word-break

* normal 使用浏览器默认的换行规则。
* break-all 允许在单词内换行。
* keep-all 只能在半角空格或连字符处换行。

### word-wrap
属性允许长单词或 URL 地址换行到下一行normal
* normal 只在允许的断字点换行（浏览器保持默认处理）。
* break-word 在长单词或 URL 地址内部进行换行,几乎得到了浏览器的支持。



