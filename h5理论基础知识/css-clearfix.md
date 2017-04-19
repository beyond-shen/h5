# clearfix

目的：

## 写法
```html
.clearfix::after,
.cleardix::before{
  content:"";
  height:0;
  clear:both;

  line-height:0;
  display:block;
  visibility:hidden;
}
.clearfix{
zoom:1---兼容ie
}
```
### 伪元素：是一个行内元素
```html
.f::before{
        content: "前边的内容内容";
      }
.f::after{
        content:"后面的内容";
      }
```
***
必须有**content**，否则其他的属性无效
***
### display

目的： 可以让块元素和行内元素进行转换
***
inline-block－－－行内块元素，两者属性都兼具。修改为行内块元素，同浮动后的效果差不多(区别:浮动后２个盒子无间隙而行内块元素有)。　
***

### visibility
1. 属性值：hidden visiable
2. 对比２种隐藏的区别：
    * display:none;----隐藏但是不占据页面空间有时候用于－>不用时隐藏用时显示(比如密码错误)
    * visibility:hidden；－－－隐藏但是还占据一定的页面空间

