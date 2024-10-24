# HTML

## meta标签简介

meta标签一般用于定义页面的特殊信息，比如页面关键字、页面描述等。

在HTML中meta中有2个重要的属性：name和http-equiv

```html
(1) name 属性取值:

keywords 网页关键字    description 网页的描述   author 网页的作者  copyright 版权信息

(2)http-equiv 属性作用
<meta charet="uft-8"/> 定义网页所使用的编码
<meta http-equiv="refresh" content="5":url="网址" 定义网页自动刷新跳转
```

## HTML注释语法

```html
语法: <!--注释内容-->
```

## 文本标签

```html
标题标签 h1~h6   水平线标签 hr       上标标签 sup       下划线标签 ins、u
段落标签 p       加粗标签 strong、b  下标标签 sub       大字号标签 big
换行标签 br      斜体标签 i、em      删除线标签 del、s  小子号标签 small
```

## 特殊符号

```html
&quot 双引号  &lsquo 左单引号  &rsquo 右单引号   &times 乘号   &divide 除号   &dt 大于号   &lt  小于号
&copy 版权    &reg 注册商标    &trade 商标      &deg 度
```

## 列表简介

在HTML中列表共分为3种：有序列表、无序列表、定义列表

```html
1.有序列表：ol li      ol的type属性取值：1 a A i l
2.无序列表：ul li      ul的type属性取值：disc cirde square
3.定义列表：dl dt dd   dl表示定义列表   dt表示标题   dd表示描述
```

## 表格table标签

```html
table   表格标签  tr 行标签     th 表头标签   caption 表格标题  td 单元格标签 
1.rowspan 表格合并行（所谓合并行指的是将纵向的N个单元格合并）
语法：<td rowspan="跨域的行数"></td>
2.colspan 表格合并列（所谓合并列指的是将横向的N个单元格合并）
语法：<td colspan="跨域的列数"></td>
```

## 图片 img

```html
<img src="图片路径" alt="图片描述" title="图片标题" >
```

## 超链接   a标签

```html
<a href="链接地址" target="打开方式">文本或图片</a>
target属性取值：
_self   在原来的窗口打开链接(默认值)
_blank  在新窗口打开链接
_parent 在父窗口打开链接
_top    在顶层窗口打开链接
```

## 表单 form标签

```html
form属性：
name 表单名称     method 提交方式          action 提交地址     target 打开方式
name的值：自定义   method的值：get/post    action的值：url地址
```

## 新增的语义化标签

```html
header  头部标签                                  aside   侧边栏标签
nav      导航标签                                   footer  底部标签
actide  内容标签                                    main    文档主要内容
progress  进度条                                    meter   度量器
fieldset  绘制表单边框                             legend定义fieldset的标题
```

## input表单新增的type属性

```html
<input type="text" />  单行文本框       <input type="password" /> 密码文本框 
<input type="radio" /> 单选框             <input type="checkbox" /> 多选框
<input type="button" /> 按钮              <input type="file" /> 上传文件
<input type="image" /> 图片按钮        <input type="reset" /> 重置按钮
<input type="submit" /> 提交按钮       <input type="textare" /> 多行文本框
<input type="email" /> 输入邮箱格式   <input type="url" /> url网址
<input type="time" /> 时间                 <input type="date" /> 日期
<input type="month" /> 月                 <input type="week" /> 周
<input type="number" /> 数字            <input type="tel" /> 手机号
<input type="search" /> 搜索框          <input type="color" /> 颜色菜单
```

## input表单新增的其他属性

```html
value      自定义文本内容          size 设置单行文本的长度
requlred  表单内容不能为空      placeholder 表单提示信息
autofocus  自动获得指定焦点    maxlength 设置最多输入字数
multiple  多选文件提交             pattern 行内正则表达式
autocomplete  值为off/on 保存用户输入过的值然后显示
```

## input表单新增的元素（datalist标签）

```html
<form action="" method="post">
            <input type="text" list="inputs"/>
            <datalist id="inputs">
                <option value ="" label=""></option>
                <option value ="" label=""></option>
            </datalist>
                    </form>

重点
1：option标签中创建选项值：value：具体的值，label：提示信息（辅助值）
2：input标签里的list属性的值为datalist标签里的id值
3：option可以是单标签也可以是双标签
4：如果input输入框的type类型是url，那么value的值必须添加http://

```

## audio音频标签

```html
属性：
src：播放的音频文件路径                 controls：音频播放器的控制面板
autoplay：自动播放                          loop：循环播放
语法：<audio src="播放的音频文件路径 " controls  autoplay  loop"></audio> 

```

## video 视频标签

```html
属性：
src：播放的音频文件路径                 controls：音频播放器的控制面板
autoplay：自动播放                          loop：循环播放
height：播放窗口高度                       width：播放窗口高度
poster：当视频还没有完全下载，或者用户还没有点击播放的默认显示的封面，默认显示当前视频的第一帧画面图。
typy：视频文件格式
代码示范：
<video controls >
<source  src="播放的音频文件路径 " poster =”视频默认显示的图片路径” typy=“video/mp4”>
对不起，您的浏览器不支持当前的视频播放
</video>
重点：
1：当设置宽高的时候，一般情况下只会设置宽度或者高度，让其自动的等比缩放，如果同时设置的宽度和高度，那么视频并不会真正的调整到设置的宽高，除非设置的值刚好是等比例。
2：source的使用，因为不同的浏览器支持的视频格式不一样，所以可以准备多个格式的视频文件，让浏览器自动选择。

```

# CSS

## CSS引入方式

css引入方式共有一下3种

```html
外部引入：<link rel="stylesheet" type="text/css" href="文件路径"/>
内部引入:<style type="text/css"></style>
行内引入：<div style="color:red"></div>
```

## 字体样式

```css
font-family 字体类型                             font-size 字体大小
语法：font-family:字体1，字体2，字体3              语法：font-size：取值
可选值：Arial "Times new Roman" "微软雅黑"        可选值的单位：px em rem %

font-weight 字体粗细                            font-style 字体风格
语法:font-weight：取值                          语法:font-style：取值
可选值：normal 正常   lighter 较细               可选值：normal 正常   italic 斜体
       bolder 很粗   bold 较粗                          oblique 斜体       
```

## CSS注释

```html
语法：/* 注释内容 */
```

## 文本样式

```css
text-decoration 文本修饰                   text-indent 首行缩进 
语法：text-decoration：取值                语法：text-indent：像素值 
可选值： none 去除所有效果                 
        overline  顶划线                   line-height 行高 
        underline 下划线                   语法:line-height：像素值
        line-through 中划线

text-align  水平对齐
语法：text-align：取值
可选值：left 左对齐   center 居中对齐 
       right 右对齐

```

## 间距

```css
letter-spacing 字间距 语法：letter-spacing：像素值
word-spacing 词间距   语法：word-spacing：像素值
```

## 边框样式

```css
border-width  边框的宽度   border-height 边框的高度   border-color 边框的颜色
border-style  边框的样式
可选值：none 无样式   dashed 虚线   solid 实线
border的简写样式 语法：border：宽度 颜色 样式 
```

## 边框的局部样式

```css
border-top 上边框   border-bottom 下边框   border-left 左边框   border-right 右边框
边框局部简写语法：border-top：1px solid red
```

## 列表样式

```css
list-style-type 列表项目符号     语法：list-style-type：取值
可选值：lower-roman 小罗马数字    upper-roman 大写罗马数字       
       lower-alpha 小写英语      upper-alpha 大写英语       
       decimal     阿拉伯数字    disc  实心圆       
       circle      空心圆        square 正方形   
```

## 表格样式

```CSS
caption-side 表格标题位置   语法：caption-side：取值
可选值：top 标题在顶部   bottom 标题在底部

border-collapse 表格边框合并 语法： border-collapse：取值
可选值：separate 边框分开，有空隙
       collapse 边框合并，无空隙

border-spacing 表格边框间距  语法：border-spacing：像素值
```

## 图片样式

```css
text-align 图片对齐   语法：text-align：取值
可选值：left 左对齐   right 右对齐   center 居中对齐

vertical-align 垂直对齐   语法：vertical-align：取值
可选值：top 顶部对齐   middle 中部对齐
       baseline 基线对齐   bottom 底部对齐

图片大小：width 宽度   height 高度
图片边框：border：1px solid red
```

## 文字环绕

```css
float 文字环绕   语法：float：取值 可选值:left 元素向左浮动   right：元素向右浮动
```

## 背景样式

```css
background-color 背景颜色   语法：background-color：颜色值
background-image 背景图片   语法：background-image：url（图片路径）

background-repeat 图片背景重复 语法：background-repeat：取值
可选值：repeat 在水平和垂直方向上同时平铺   repeat-x 只在水平方向（x轴）上平铺
       repeat-y 只在垂直方向（y轴）上平铺  no-repeat 不平铺

background-position 图片背景位置   语法：background-position：像素值/关键字
background-attachment 背景图片固定 语法：background-attachment：取值
可选值：sroll 随元素一起滚动   fixed 固定不动
```

## 超链接伪类

```
a:link 定义a元素位访问的样式            a:visited 定义a元素访问后的样式
a：hover 定义a元素鼠标经过时的样式       a:active 定义鼠标单击激活时的样式
```

## 鼠标样式

```css
cursor 鼠标样式   语法：cursor：取值 可选值：default pointer text wait 
自定义鼠标样式 语法：cursor：url（图片地址），属性值
鼠标图片后缀一般都是“.cur”，属性值一般都是default pointer text
```

## 浮动布局

```css
float 浮动   语法：float：取值   可选值:left 元素向左浮动   right 元素向右浮动
```

## 清除浮动

```css
clear 清除浮动   语法：clear：取值   可选值：left 清除左浮动  right 清除右浮动 both 同时清除左右浮动
```

## 定位布局

```css
position 开启定位 语法：position：取值 
可选值:fixed 固定定位 relative 相对定位 absolute 绝对定位  static 静态定位
4中定位可选值：top：像素值 bottom：像素值 left：像素值 right：像素值
```

## 显示模式元素转换

```css
display：block 转换为块级元素     display：inline 转换为行内元素   display：inline-block 转换为行内块元素
```

## ：focus 伪类选择器

```css
：focus 伪类块级元素 语法：input：focus{background-color：red} 用于选取活动焦点的表单元素，一般都在input类
```

## 元素的显示与隐藏

```css
display：none 隐藏元素  display：block 显示元素  visibility：visible元素可视   visibility：hidden 元素隐藏
display不保留位置，visibility保留位置
```

## 新增的属性选择器

```css
input[value] 必须是input同时具有value这个属性，选择这个属性
input[type=text]选择input里的type的值为text
div[class^=icon]选择首先是div具有class属性而且必须是icon开头的
```

## 伪类选择器

```css
:first-child 选择第一个子元素      :last-child 选择最后一个子元素    :nth-child(n)选择第n个子元素
:first-of-type 指定类型的第一个    :last-of-type 指定类型的最后一个  :nth-of-type(n)指定类型的第n个

:nth-child()可以是数字也可以是公式也可以是关键字
关键字：even 偶数   odd 奇数
公式：2n 偶数  2n+1 奇数 5n:5 10 15...  n+5 从第5个开始包含第5个到最后
区别：
1.nth-child 对父元素里面所有的孩子排序选择(序号固定)先找到第n个孩子，后面再看看是否匹配。
2.nth-of-type 对父元素里面指定的子元素进行排序，先去匹配然后再根据找到第n个孩子。
```

## 伪元素选择器

```css
::before 在元素内部前面插入内容                                           ::after 在元素内部后面插入内容
before和after创建一个元素，单是属于行内元素，在文档树中找不到所以称为伪元素。
语法:element::before{content:""}before和after必须要有content属性    
```

## 计算盒子宽度

```less
width:cala(100%-80px)可使用 + - * /
```

## snipaste小工具

```css
按F1可截图，测量大小，设置箭头，书写文字等。
按F3可在桌面置顶显示
按Esc可取消图片显示
点击图片alt可取色(按shift可切换取色模式)
```

## CSS常用代码

```css
text-align:center 文本居中对齐                            text-decoration:none 去除所有划线效果
text-indent:20px  所有段落首行缩进20像素                      background:rgba(0,0,0,0.5)背景颜色半透明
outline:none 去除input输入框的轮廓线                          resize:none 防止textarea拖拽
*{padding:0 margin:0} 去除所有默认样式                       border-radius：数值(px或%) 圆角
list-style-type:none 去除项目符号                            opacity：0.5 半透明
border:none 去除input边框
```

### CSS斜切边

```css
        .xiaolong{
            margin-top: 50px;
            width: 305px;
            height: 75px;
            background: linear-gradient(-125deg,transparent 42px,#fff000 0)top right;
            background-size:100% 100% ;
            background-repeat: no-repeat;
        }

```

# JavaScript

## JavaScript的引入方式

```html
行内引入：<input type="button" onclick="alert()">
内部引入：<script>//执行语句</script>
外部引入：<script src="文件路径"></script>
```

## javaScript注释

```javascript
//单行注释    /*多行注释*/
```

## javaScript输出语句

```html
alert()弹出警示框     console.log()控制台打印输出信息
promet()弹出输入框，用户可以输入
```

## 变量

```html
var a=1 声明变量名为a并赋值为1
```

## 数据类型

```html
Number 数字型     String 字符串   Boolean 布尔值
underfinded 未定义  Null 空值    Object 对象
数据类型共有以上六种数据类型,基本数据类型除object,其余全是基本数据类型变量的数据类型是只有程序在运行过程中根据等号右边的值来确定的。
```

## 判断数据类型

```html
isNaN()用来判断一个变量是否为非数字类型返回true表示不是数字型。
```

## 获取数据类型

```html
typeof 语法:console.log(typeof 变量名)
```

## 数据类型转换

```html
使用表单prompt获取过来的数据默认是字符串类型的此时就不能直接简单地进行加法运算需要转换变量的数据类型，通俗来说就是把一种数据类型的变量转换成另一种数据类型。
数字型转换为字符串类型
语法(1):变量.toString()
例:var num=10      var str=num.toString()
语法(2):String(变量)
例:var num=10      var str=string(num)
语法(3):和字符串拼接的结果都是字符串(隐式转换)
```

## 转换为数字型

```html
语法(1):parseInt(变量) 转换为数字型得到的是整数
语法(2):parseFloat(变量) 转化为数字型得到的是小数浮点数
语法(3):Number(变量) 强制转换为数字型
```

## 转换为布尔型

```html
语法:Boolean 其他类型转化为布尔型代表空值，否定的值会被转换为false。
如:0 NaN Null nudefind,其余的值都会转化为true。11
```

## 运算符

```html
(1)算数运算符:+ - * / %
(2)前置自增自减运算符:++num --num (前置先加1后返回值)
(3)后置自增自减运算符num++ num-- (后置返回原值后加1)
(4)比较运算符:< > >= <= = != === !==
(5)逻辑运算符:&&与 ||或 !非
重点:= 赋值,把右边的值给左边
    == 比较,段段两边的指示不相等
    ===全等,判断两边的值和数据类型是否完全相等
```

## 流程控制-if语句

```html
(1)if语句 语法:if(条件表达式){执行语句}
(2)if else语句 语法:if else(条件表达式){条件执行成立的代码}else{条件不成立时执行的代码}
(3)if else if语句 语法:if(){}else if(){}else if(){}else{}
```

## 三元表达式

```html
语法:条件表达式?表达式1:表达式2
例:num>5?"大于":"不大于";
执行思路:如果条件表达式为真，则返回表达式1的值，如果条件表达式的结果为假，则返回表达式2的值。
```

## 流程控制-switch语句

```html
语法:switch(表达式value值){case value值:
                         执行语句1;
                         break;
                         default:执行最后的语句}
执行思路:利用表达式的值和case后面的选项值相匹配，如果匹配上就执行该case里面的语句，如果都没有匹配上，那么执行default里面的语句。
switch注意事项:
1.在开发时表达是我们经常写成变量
2.num的值和case里面的值相匹配的时候是全等，必须是和值的数据类型一致
3.break如果当前case里面没有break不会退出switch,是继续执行下一个case
```

## switch和if else if语句区别

```html
1.一般情况下，他们两个语句可以相互替换
2.switch...case语句通常处理case为比较确定值的情况,而if...else语句更加灵活,常用于范围判断(大于等于某个范围)
3.switch语句进行条件判断后直接执行程序的条件语句效率更高。而if...else语句有几种条件就得判断多少次。
4.当分支比较少时,if...else语句执行效率比switch语句高。
5.当分支比较多时,switch语句的执行效率比较高，而且结构更清晰。
```

## 循环-for循环

```html
在程序中，一组被重复执行的语句被称为循环体，能否继续重复执行取决于循环的终止条件。由循环体及循环的终止条件组成的语句称之为循环语句。
语法结构:for(初始化变量;条件表达式;操作表达式){循环体}
1.初始化变量就是用var声明的一个普通变量，常用于作为计数器使用。
2.条件表达式就是用来决定每一次循环是否继续执行就是终止的条件。
3.操作表达式是每次循环最后执行的代码，通常我们用于计数器变量进行更新。
```

## 循环-while循环

```html
语法结构:while(条件表达式){循环体}
```

## continue关键字

```html
continue关键字用于立即跳出本次循环，继续下一次循环(本次循环中continue之后的代码就会少执行一次)
```

## break关键字

```html
break关键字用于即跳出整个循环(循环结束)
```

## 数组

```html
创建数组（1):var 数组名=new Array（）利用new创建数组
创建数组(2):var 数组名=[] 利用字面量创建数组
```

## 数据的索引

```html
用来访问数组元素的序号(数组下标从0开始)
```

## 获取数组元素

```html
数组名[索引号]
```

## 新增数组元素

```html
修改数组的长度:数组名.length=要修改的数量
追加数组的元素:数组名[索引号]=[数组元素]
```

## 函数的概念

```html
在JS里面可能会定义非常多的相同代码或者功能相似的代码，这些代码可能需要大量重复使用，虽然for循环语句也能实现一些简单的重复操作，但是比较具有局限性，此时我们可以使用JS中的函数。
函数就是封装了一段，可被重复调用执行的代码块，通过此代码块可以实现大量代码的重复使用。
```

## 声明函数

```html
语法:function 函数名(){函数体}
注意事项:
1.function声明函数的关键字全部小写。
2.函数是做某件事，函数名一般是动词。
3.函数不调用自己不执行。
```

## 调用函数

```html
语法:函数名()
```

## 函数的封装

```html
函数的封装是把一个或多个功能通过函数的方式封装起来，对外只提供一个简单的接口。
```

## 函数的参数

```html
形参 function 函数名(形参1,形参2){}形式上的参数接收实参
实参 函数名(实参1,实参2)  实际的参数
函数在声明时,可以在函数名称后面的小括号添加一些参数，这些参数被称为形参，而在调用该函数时，同样也需要传递相应的参数，这些参数被称为实参。
参数的作用:在函数内部某些值不能固定，我们可以通过参数在调用函数时传递不同的值进去
```

## 函数形参和实参个数不匹配的问题

```html
实参个数等于形参个数:输出正确结果。
实参个数多于形参个数:只取道形参的个数。
实参个数小于形参个数:多的形参定义为undefined结果为NaN。
```

## 函数的返回值return

```html
return语句:有的时候我们会希望函数将值返回给调用者，此时通过使用return语句就能实现。
语法:return 需要返回的结果(形参)
```

## return注意事项

```html
1.return语句之后的代码不会被执行(终止函数)
2.return只能返回一个值，如果用逗号隔开或者多个值,以最后一个为准。
3.函数没有return返回undefined
4.函数有return则返回undefined
```

## break continue return的区别

```html
break:结束当前的循环体(如for和while)。
continue:跳出本次循环继续执行下次循环(如for和while)。
retrun:不仅可以跳出循环，还能够返回return语句中的值，同时还可以结束当前的函数体内的代码。
```

## arguments的使用

```html
当我们不确定有多少个参数传递的时候，可以使用arguments来获取在js中Arg ments，实际上它是当前函数的一个内置对象。所有函数都内置了一个arguments对象，argument对象中储存了传递所有实参。
arguments显示是一个为数组，因此可以进行遍历为数组具有以下特点:
1.所以索引存方式储数据。
2.不具有数组push pop等方法。
3.只有函数才有argument对象。
```

## 声明函数(2)

```html
语法:var 变量名 =function(){}
```

## 创建对象的三种方式

```html
(1)利用字面量创建对象   var obj={属性1:值,属性2:值}
1.里面的属性或方法，我们采取键值对的形式,键 属性名:值 属性值
2.多个属性或方法，中间用逗号隔开
3.方法冒号后面跟的是一个匿名函数
```

## 使用对象

```html
1.调用对象的属性我们采用 对象名.属性名
例:alert(ojb.uname)
2.调用属性还有一种方法  对象名["属性名"]
例:alert(obj["age"])
3.调用对象函数的方法  对象名.函数名()
例:obj.getkey()
```

## 构造函数

```html
构造函数是一种特殊的函数，主要用来初始化对象，即为对象成员变量赋初始值，它总与new运算符一起使用。我们可以把对象中一些公共属性和方法抽取出来，然后封装到这个函数里面。
语法格式:
function 构造函数名(){
         this.属性=值
         this.方法=function(){}
}
使用构造函数:new 构造函数名()
注意事项:构造函数名首字母要大写,构造函数不需要return,调用构造函数必须使用new属性和方法，必须添加this。
代码验证:
function Star(uname,agr,sex){
this.name=uname
this.age=age
this.sex=sex
}
var ldh=new Star("刘德华","18","男")
```

## new关键字执行过程

```html
1.new构造函数可以在内存中创建一个空的对象
2.this就会指向刚才创建的空对象
3.执行构造函数里面的代码给这个空对象添加属性和方法
4.返回这个对象(所以构造函数里面不需要return)
```

## 遍历对象

```html
for...in语句用于数组或者对象的属性进行循环操作。
语法:for(变量 in 对象){console.log([变量])}
使用for in里面的变量命名一般为key或者key(不强制命名)
```

## 内置对象

```html
内置对象就是指js语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或是最基本的必要的功能(属性和方法)
javaScript供了多个内置对象:Math Date Array String
```

## 查文档

```html
MDN官方网址:https://developer.mozilla.org/zh-CN
```

## Math取随机整数方法(公式)

```html
function getRandom(min,max){
return Math.floor(Math.random()*(max-min+1))+min
}
```

## Date日期对象

```html
1.Date()日期对象是一个构造函数必须使用new来调用来创建日期对象。
2.参数常用写法数字型2021，5，29或是字符串型“2021－5－29 8:8:8”。
3.Date实例用来处理日期和时间，获取当前时间必须实例化
var now =new Date()
```

## 日期格式化

```html
var date=new Date() 声明日期对象函数
getFullYear()  获取当年
getMonth()     获取当月(0-11)
getDate()      获取当天日期
getDay()       获取星期几(0－6)
getHours()     获取当前小时
getMinutes()   获取当前分钟
getSeconds()   获取当前秒钟
```

## 四种获得总的毫秒数

```html
valueOf（）      get Time()
+new Date()     Date.now()
例:console.log(date.getFullYear())
   console.log(date.valueOf)
```

## 总毫秒数转换为天、时、分秒公式

```html
d=parseInt(总秒数/60/60/24) 计算天数
h=parseInt(总秒数/60/60%24) 计算小时
m=parseInt(总秒数/60%60)    计算分钟
s=parseInt(总秒数%60)       计算当前秒数
```

## 检测是否为数组

```html
1.instance of 运算符  语法:数组名.instance of Array
2.Array.isArray()    语法:Array.is Array(数组名)
提示:第二种是H5新增的 IE9以上才可以用
```

## 添加数组元素

```html
1.push() 在数组中的尾末添加一个或多个数组元素
(1)push是可以给数组追加新的元素
(2)push()参数直接写数组元素
(3)push完毕之后返回的结果写新的长度
(4)原数组也会发生变化
2.unshift()在数组开头添加一个或多个数组元素
例:数组名.push(5,"1")
```

## 删除数组元素

```html
1.pop()删除数组最后一个元素
(1)pop()是可以删除数组的最后一个元素，一次只能删除一个元素
(2)pop()没有参数
(3)pop()完毕后返回的结果是删除的那个元素
(4)原数组也会发生变化
2.shift()删除数组第一个元素
例:数组名.pop()
```

## 数组排序

```html
1.reverse() 翻转数组   语法:数组名.reverse()
2.sort() 冒泡排序      语法:数组名.sort()
```

## sort解决方案

```html
var arr1=[13,4,76,1,2]
arr1.sort(function(a,b){
return a-b  
})
a-b升序的顺序排序       b-a降序的顺序排序
```

## 数组索引方法

```html
indexOf() 作用就是返回该数组元素的索引号(从前面开始查找)
(1)他只满足第一个满足条件的索引号
(2)他如果在该数组里面找不到元素，则返回-1
2.lastIndexOf()作用就是返回该数组元素的索引号（从后往前）
```

## 数组转换为字符串

```html
1.tostring()   语法:数组名.tostring()
2.join()       语法:数组名.join("-")
```

## 字符串操作方法

```javascript
1.concat() 用于连接两个或多个字符串，拼接字符串等。
2.substr(start,length)从start位置开始(索引号)，length取的个数。
例:var start1="你好，世界"
alert(start1.substr(3,2))
replace() 替换字符串  例：replace('被替换的字符','替换为的字符')
split() 字符串转换为数组
```

## 字符串对象

```javascript
toUpperCase() 转换为大小           toLowerCase() 转换为小写
```

## 获取元素的方式

```javascript
1.根据ID获取元素               2.根据标签名获取
3.通过HTML5新增的方法获取       4.特殊元素获取
console.dir 打印返回元素对象更好的查看里面的属性和方法
获取元素ID：document.getElementById()
获取标签名:document.getElementsByTagName()
获取元素class:document.getElementsByClassName()
获取选择器:document.querySelector()
获取所有选择器:document.querySelectorAll()
获取body元素:document.body
获取html元素:document.doucumentElement
```

## 事件三要素

```html
(1)事件源,事件被触发的对象,谁,按钮。
(2)事件类型 如何触发 什么事件 比如鼠标点击(onclick)。
(3)事件处理程序,通过一个函数赋值的方式完成。
```

## 执行事件的步骤

```html
(1)获取事件
(2)注册事件
(3)添加事件处理程序(采用函数赋值方式)
```

## 常见鼠标事件

```javascript
onclick    鼠标点击左键触发  onmouseover 鼠标经过触发
onmouseout 鼠标离开触发     onfocus  获得鼠标焦点触发
onblur     失去焦点触发     onmousemove 鼠标移动触发
onmouseup  鼠标弹起触发     onmousedown 鼠标按下触发
```

## 操作元素

```html
JavaScript的DOM操作可以改变页面内容结构和样式，我们可以利用DOM操作元素来改变元素里的内容，属性等。
element.innerText  改变元素内容
element.innerHTML  改变元素内容
```

## 常见的元素属性操作

```html
src href id alt title 等  例:img.src='./img/img.png'
```

## 获取属性值

```html
element.属性  //获取内置属性值（元素本身自带的属性）
element.getAttribute("属性") //主要获取自定义的属性
```

## 设置属性值

```html
element.属性=“值” //设置内置属性值
element.setAttribute(“属性”，“值”)//设置自定义属性值
```

## 移除属性

```html
element.removeAttribute(“属性”)
自定义属性目的是为了保存并使用数据，有些数据可以保存到页面中，而不用保存到数据库中。
H5自定义属性书写规范:data-开头，做为属性名并且赋值。
例:data-index1=“1”
```

## 节点操作

```html
document.createElement(“li”) 创建元素节点
document.appendChild(child) 添加元素节点
node.inserBefore(child,指定元素) 添加元素节点到最前面
node.removeChild(child) 删除节点
例：var li=document.createElement(“li”)
   ul.appendChild(li)
   li.innerHTML=text.value
   或ul.insertBefore(li,ul.children[0])
```

## 阻止链接默认跳转

```html
JavaScript:void(0);或者javascript:;
```

## 复制节点(克隆节点)

```html
node.cloneNode() 方法返回调用该方法节点的副本
例:var lili=ul.children[0].cloneNode(true)
   ul.appendChild(lili)
   注意:括号为空或者false是浅拷贝，只复制标签，不复制里面的内容。
```

## 注册监听事件

```html
eventTarget.addEventListener(type,listent,[useCapture])
eventTarget.addEventListener()方法将指定的监听到eventTarget(目标对象上)该对象方法接收三个参数：
type:事件类型字符串，比如click mouseover注意这里不能带on
listener:事件处理函数事件发生时会调用该监听函数。
useCapture：可选参数是一个布尔值默认是false。
```

## 删除事件

```html
传统解除事件:eventTarget.onclick=null
监听解除事件:eventTarget.removeEventListener(type,listener[useCapture])
```

## 事件对象 event

```html
1.event就是一个事件对象写到侦听函数的小括号里当形参来看。
2.事件对象只有有了事件才会存在，它是系统给我们自动创建的，不需要我们传递参数。
3.事件对象是事件一系列相关数据的集合，跟事件相关的。
4.这个事件对象我们可以自己命名e event evt等。
官方解释:event对象代表事件的状态，比如键盘的状态，鼠标的位置，鼠标按钮的状态。
简单理解:事件发生后，跟事件相关的一系列信息数据的集合者放到这个对象里面，这个对象就是事件对象event它有很多属性和方法。
```

## this和e.target的区别

```html
this哪个元素绑定了这个事件那么就返回谁。
e.target点击了哪个元素就返回哪个元素？
```

## 事件对象的常见属性和方法

```html
e.returnValue 该属性阻止默认行为
e.preventDefault()该方法阻止默认行为(标准)
e.stopPropagation()阻止冒泡
e.canceBubble 该属性阻止冒泡
e.type 返回事件的类型 比如:click mouseover
e.srcElement 返回触发事件对象
e.target 返回触发事件的对象(标准)
```

## 禁止选中文件和禁止右键菜单

```html
(1)contextmenu 禁止右键菜单
例:document.addEventListener("contextmenu",function(e){e.preventDefault()})
(2)selectstart禁止选中文字
例:document.addEventListener("selectstant",function(e){e.preventDefault()})
```

## 鼠标事件对象

```html
e.clientX 返回鼠标相对于浏览器可视窗口的X坐标
e.clientY 返回鼠标相对于浏览器可视窗口的Y坐标
e.pageX 返回鼠标相对于文档页面的X坐标
e.pageY 返回鼠标相对于文档页面的Y坐标
e.screenX 返回鼠标相对于电脑屏幕的X坐标
e.screenY 返回鼠标相对于电脑屏幕的Y坐标
```

## 常用键盘事件

```html
onkeyup 某个键盘按键被松开时触发
onkeydown 某个键盘按键被按下时触发
onkeypress 某个键盘按键被按下时触发(不识别功能键，如Ctrl shift等)
三个事件的执行顺序:keydown-keypress-keyup
```

## 键盘事件对象

```html
keyCode  返回该键的ASCLL值
```

## 封装原生ajax

```javascript
（function (){
            var ajax = {
            getxhr: function() {
                return new XMLHttpRequest()

            },
            postxhr: function() {
                return new XMLHttpRequest()

            },
            get: function(url, sync = true, fun) {
                var xhr = this.getxhr()
                xhr.onreadystatechange = function() {
                    if (xhr.readyState == 4) {
                        fun(xhr.responseText)
                    }
                }
                xhr.open('get', url, sync)
                xhr.send()

            },
            post: function(url, post_data, sync = true, fun) {
                var xhr = this.postxhr()
                xhr.onreadystatechange = function() {
                    if (xhr.readyState == 4) {
                        fun(xhr.responseText)
                    }
                }
                xhr.open('post', url, sync)
                xhr.send(post_data)
            }
        }
        window.=ajax
}）()
```

## CORS解决跨域

使用CORS:

```javascript
res.setHeader('Access-Control-Allow-Origin','*')
Access-Control-Allow-Origin：请求头的名字
*:请求头的值，如果只允许某一个域名访问，则替换成指定的域名，如果值为*则允许所有外域发送请求
例：res.setHeader('Access-Control-Allow-Origin','http://idc.shutianyun.com')

```

## 调用原生封装的ajax

```javascript
username.onblur = function() {
            window.myajax.get('http://127.0.0.1:8080/gets?username=' + username.value, true, function(data) {
                if (data == 1) {
                    txt.innerHTML = "账号已被注册"
                    txt.style.color = "red"
                } else {
                    txt.innerHTML = "账号可注册"
                    txt.style.color = "green"
                }
            })
        }
        tel.onblur = function() {
            window.myajax.get('http://127.0.0.1:8080/gettel', true, function(data) {
                alert(data)
            })
        }
```

# BOM

```html
window.onload 是窗口加载事件，当文档内容完全加载完成会触发该事件，就会调用处理。
window.onload传统注册事件方式只能写一次，如果有多个会以最后一个为准。
如果使用addEventListener则没有限制。
(1)window.addEventListener("load",function(){})
(2)document.addEventListener("DOMContentLoaded",function(){})
(3)window.onload=function(){}
1.load等页面内容全部加载完成,包含页面DOM元素图片flash css等。
2.DOMContentLoaded是DOM加载完毕，不包含图片 flash css等就可以执行。
```

## 调整窗口大小事件

```html
window.addEventListener("resize",function(){})
1.只要窗口大小发生像素变化，就会触发这个事件。
2.我们经常利用这个事件完成响应式布局window.innerWidth 当前屏幕的宽度。
```

## 定时器

```html
(1)setTimeout() 定时器
window.setTimeout(调用函数,[延迟的毫秒数])
setTimeout()方法用于设置一个定时器,该定时器到期后执行调用函数。
1.window在调用的时候可以省略。
2.这个延时事件单位是毫秒也可以省略，默认是0
3.页面中可能有很多定时器，可以给定时器声明一个变量。
(2)clearTimeout 清除定时器
window.clearTimeout(timeoutID)
(3).setInterval() 定时器
window.setInterval(回调函数,[延时的毫秒数])
(4).clearInterval 清除定时器
重点：setTimeout和setInterval区别
1.setTimeout延时事件到了,就去调用这个函数，只调用一次，就结束了这个函数。
2.setInterval每隔这个延迟时间就去调用一次回调函数，会调用很多次。
```

## location对象

```html
window对象给我们提供了location属性用于获取或设置窗口的URL，并且可以用于解析URL。因为这个属性返回的是一个对象，所以我们将这个属性称为location对象。
```

## URL

```html
protocol:通信协议常用的http，ftp，maito等
host:主机(域名)
port:端口号(可选)默认端口为80
path:路径由零个或多个“/”符合隔开的字符串，一般用来表示主机上的一个目录或文件地址。
query:参数以键值对的形式通过&符分隔开来。
fragment:片段#后面内容常见于链接锚点
```

## location对象属性

```html
locarion.href 获取或设置整个URL
location.host 返回主机(域名)
location.port 返回端口号
location.pathname 返回路径
location.search 返回参数
location.hash 返回片段#后面的内容
```

## location对象方法

```html
location.assign() 跟href一样，可以跳转页面（也称为重定向页面）
location.replace()替换当前页面，因为不记录历史，所以不能退页面
location.reload() 重新加载页面,相当于刷新按钮或这f5，为true强制刷新
```

## 中文转换为字符串

```html
var res=encodeURLComponent("张三")
```

## navigator对象

```html
navigator对象包含有关浏览器的信息，他有很多属性，我们最常用的就是userAgent该属性，可以返回由客户机发送服务器的user－agent头部的值。
下面的代码可以判断用户哪个终端打开页面就跳转到哪个：
if((navigator.userAgent.match(/(phone|pad|pod|iPhone|iPod|ios|iPad|Android|  
Mobile|BlackBerry|IEMobile|MQQBrowser|JUC|Fennec|wOSBrowser|BrowserNG|  
      WebOS|Symbian|Windows Phone)/i))) {
            window.location.href = ""; //手机端
          }  
 else{  
      window.location.href=""; //电脑端
  }
```

## history对象

```html
window对象给我们提供了一个history对象，与浏览器历史进行交互，该对象包含用户在浏览器窗口中访问过的URL。
back() 可以后退功能
forward() 忘了啥功能，自己百度
go() 也忘了
```

## 本地存储特性

```html
1.数据存储在用户浏览器中
2.设置、读取方便、甚至页面刷新不丢失数据
3.容量较大，session storage 约5M local storage约20M
4.只能存储字符串，可以将对象json.stringify()编码后存储。
(1)存储数据:sessionStorage.setItem("key",value)
(2)获取数据:sessionStorage.getItem("key")
(3)删除数据:sessionStorage.removeItem("key")
(4)删除所有数据:sessionStorage.clear("key")
———————————————————————————————————————————————
(1)存储数据:localStorage.setItem("key",value)
(2)获取数据:localStorage.getItem("key")
(3)删除数据:localStorage.removeItem("key")
(4)删除所有数据:localStorage.clear("key")
注:所有的key自定义,value是变量
```

# 箭头函数

ES6可以使用箭头（=>）定义函数，注意是普通函数，不要使用这种方式定义类（构造器）

具有一个参数并直接返回一个函数

```html

```

# Vue

## Vue的基本使用

```html
(1)导入vue.js文件的script脚本
(2)在页面中声明一个将要被vue所控制的DOM区域
(3)创建一个vm实例对象
<body>
<div id="app">{{username}}</div>
<script>
//创建vue实例对象
const vm=new Vue({
el:“#app”,
data:{},
methods:{
函数名(){}
},
})
</script>
</body>
1:el属性是固定的写法,表示vm实例要控制页面上的哪个区域，接收的值是一个选择器。
2:data对象就是要渲染到页面上的数据。
3:methods的作用就是定义事件的处理函数。
```

## Vue调试工具以及组件库

```html
安装vue－devtools 调试工具
day.js时间库 :https://dayjs.fenxianglu.cn/category/
Element-ui :https://element.eleme.cn/#/zh-CN
vant :https://vant-contrib.gitee.io/vant/v2/
axios:https://www.axios-http.cn/docs/intro
```

## Vue指令

```html
Vue的指令按照不同的用途分为如下6大类
①内容渲染指令    ②属性绑定指令    ③事件绑定指令
④双向绑定指令    ⑤条件绑定指令    ⑥列表渲染指令
```

## Vue指令说明

```html
v-model 双向数据绑定       v-on 监听事件
v-bind 单向数据绑定        v-text 插入文本内容
v-html 插入包含HTML的内容  v-for 列表循环
v-if 条件渲染             v-show 显示隐藏
```

## 内容渲染指令

```html
内容渲染指令用来辅助开发者渲染DOM元素的文本内容。常用的内容渲染指令如:v-text  {{}}  v-html
语法:
<p v-text=""></p>
{{}}
<p v-html=""></p>
注意：
(1)v-text指令的缺点会覆盖元素内部原有的内容
(2){{}}指令是插值表达式，专门用来解决v-text会覆盖默认文本内容的问题。
(3)v-text和插值表达式只能渲染纯文本内容,如果要把包含HTML和字符串的渲染页面的HTML元素，则需要用到v-html。
```

## 属性绑定指令

```html
<input type="text” v-bind:placeholder="">
注意:
(1)如果需要为元素的属性动态绑定属性值，则需要用到v-bind属性绑定指令。
(2)也可以简写成“:”。
(3)在使用v-bind使用期间需要进行动态拼接则需要用双引号包裹单元号。
```

## 事件绑定指令

```html
<button v-on:click="事件函数名"></button>
注意:
(1)Vue提供了v-on事件绑定指令,用来DOM元素绑定事件监听。
(2)在methods方法内如果要修改data里面的数据源可以通过this修改值。
(3)在绑定事件处理函数的时候，可以使用()传递参数。
(4)v-on的简写指令为“@”。
(5)vue提供了内置的变量叫做$event，它就是原生DOM的事件对象e。
```

## 事件修饰符

```html
在事件处理函数中调用event.preventDefault()或event.stopPropagation()是非常常见的需求,因此vue提供了修饰符的概念，常用的五种修饰符如下:
.prevent 阻止默认行为(例如:阻止a链接跳转，表单的提交等)
.stop 阻止事件冒泡
.capture 以捕获模式触发当前的事件处理函数
.once 绑定的事件只触发一次
.self 只有在event.garget是当前元素自身触发事件处理函数。
注意:
.prevent和.stop.是最常用的修饰符。
```

## 按键修饰符

```html
在监听键盘事件时，我们经常需要判断详细的按键，此时可以为键盘相关的事件添加按键修饰符。
例:<input @keyup.enter="submit()">
```

## 双向数据绑定指令

```html
vue提供了v-model 双向数据绑定指令,用来辅助在不操作DOM前提下，快速获取表单的数据。
```

## v-model指令的专用修饰符

```html
.number 将用户输入的值转为数值型
.trim  自动过滤用户输入的首尾空白字符
.lazy 在“change”时而非“input”时更新
语法:<input type="text" v-model.number="">
```

## 条件渲染指令

```html
条件渲染指令用于辅助按需控制DOM的显示与隐藏分别是:v-if和v-show。
注意:
1:v-if每一次都会动态的移除元素或动态的创建元素。
2:v-show添加或移除display;none样式。
3:如果要频繁切换样式使用v-show更好。
4:如果刚进入页面的时候某些元素不需要被展示的时候，后期这个元素有可能不需要展出出来，此时用v-if的时候性能更好。
v-if 可以单独使用,或配合v-else指令一起使用。
v-else指令必须配合v-if指令一起使用，否则它将不会被识别。
v-else-if指令出现率很低一般用不到，除非判断条件很多。
```

## 列表渲染指令

```html
vue提供了v-for列表渲染指令，基于用来一个数组来循环渲染一个列表结构，v-for指令需要用item in items形式的特殊语法。
item:是待循环的数组变量名
items:是被循环的每一项
v-for指令还支持一个可选的第2个参数，当前项的索引，
语法:v-for”(item,index)in items”:key=""
官方建议:只要用到v-for指令，那么就一定要绑定一个:key 属性
而且尽量把id作为key的值。
key的注意事项：
①:key的值只能是字符串或者数字型
②:key的值必须是具有唯一性的(即:key的值不能重复)
③:建议把数据项id属性的值作为key的值(因为id属性的值具有唯一性)
④:使用index的值当做key的值没有任何意义(因为
index的值不具有唯一性)
⑤:建议使用v-for 指令时一定要指定key的值。
```

## 私有过滤器(Vue3已淘汰)

```html
过滤器应该添加在JavaScript表达式的尾部，由管道符“|”进行调用，常用于文本的格式化，可以用在插值表达式和v-bind属性绑定,过滤器函数必须定义到filters节点之下，与data平级。
语法:{{message|过滤器名(自定义)}}
    filters:{
    过滤器名(形参名){return结果}
    }
    charAt()方法，这个方法接收索引值,表示从字符串中把索引对应字符获取出来。
    toUpperCase()转换为大写
    slice()方法可以截取字符串，从指定索引往后截取。

```

## 全局过滤器

```html
声明全局过滤器语法:Vue.filter("全局过滤器的名字","全局过滤器的处理函数")
 注意点:
    1.要定义到filters节点下，本质是一个函数。
    2.在过滤器函数中,一定要有return值。
    3.在过滤器的形参中,就可以获取到管道符前面的待处理的值。
    4.如果全局过滤器和私有过滤器名字一致，此时就按“就近原则”，调用的是私有过滤器。
```

## watch 侦听器

```javascript
语法:watch:{
  uservalue(oldval,newval)
}
注意:
1.侦听器本质上是一个函数,要监视哪个数据的变化，就把数据名作为方法即可。
2.新值在前，旧值在后。
3.应用场景用于用户名是否被占用
4:immediate选项的默认值是false
5.immediate的作用是控制侦听器是否自动触发一次。
6.可以通过deep选项让助听器深度侦听对象中每个属性的变化。
```

## computed 计算属性

```html
1.所有的计算属性,都要定义到computed节点之下。
2.计算属性在定义的时候,要定义成方法格式。
```

## axios

```javascript
axios中文官网:http://www.axios-js.com
axios的基本语法:
document.querySelector("#id名").addEventListener("click",async function(){
const {data:res}=await axios({
method:"请求的类型",
url:"请求的URL地址",
params:{}
data:{}
})
con
})
注意:
1.发起GET请求用params:{}
2.发起POST请求用data:{}
3.await只能用在被async修饰的方法中
4.把解构出来的data属性使用冒号进行重新命名,一般都重命名为:data:res。
```

### axios.get和axios.post

```javascript
axios.get语法:
const{data:res}=await axios.get("url"{params:{}})
axios.post语法:
const{data:res}=await axios.post("url",{}
```

### axios挂载到vue原型上并配置请求根路径

```javascript
在main.js文件中导入
import axios from ‘axios’
//全局配置axios的请求根路径
axios.defaults.baseURL='请求根路径'
//把axios挂载到Vue.prototype上，每个.vue组件的实例直接使用。
Vue.prototype.axios=axios
今后在每个vue组件中要发起请求，直接调用this.axios.xxx
例:const {data:res} =await this.axios.get('')
```

## 单页面应用程序

```html
单页面应用程序(英文名: Single Page Application)简称SPA，顾名思义，指的是一个Web网站中只有唯一一个HTML页面，所有的功能与交互都在唯一一个页面内完成。
```

## Vue项目构成

```html
assets文件夹:存放项目中用到的静态资源文件,例:css样式表、图片资源。
components文件夹:封装的可复用的组件都要放到components目录下。
main.js:是项目的入口文件，整个项目的执行要先执行main.js。
app.vue:项目的根组件
```

### Vue项目的运行流程

```html
在工程化的项目中,vue要做的事很单纯,通过main.js把App.vue渲染到index.HTML的指定区域中。

import Vue from "vue" //导入vue这个包,得到Vue构造函数。
import App from "./App.vue"//导入App.vue根组件，将要把App.vue中的模板结构渲染到HTML页面中。
$mount(“#app”)作用跟el:"#app"没啥区别。
render:h=>(App) //把render函数指定的组件渲染到HTML页面中。
其中:
①:App.vue用来编写待渲染的模板结构。
②:index.html中需要预留一个el区域。
③:main.js把App渲染到了index.html所预留的区域中。
```

### #vue组件的三个组成部分

```html
每个.vue组件都由3部分构成,分别是:
template->组件的模板结构
script->组件的JavaScript行为
style->组件的样式
export default{}默认导出script的固定写法
<script>
export default{
data(){
return{}
}
}
</script>
注意:
①vue组件中的data必须是一个函数。
②这个return出去的{}中，可以定义数据。
```

### 使用组件的三个步骤

```html
 1.使用import语法导入需要的组件
 import Left from "@/components/Life.vue"
 2.使用components节点注册组件
 export default{
       components:{Left}}
 3.以标签形式使用刚才注册的组件
 <div class="box">
 <Left></Left>
 </div>
```

### 注册全局组件

```javascript
在Vue项目的main.js入口文件中，通过Vue.component()方法可以注册全局组件。
语法:
//导入需要全局注册的组件
import Count from "@/components/Count.vue"
Vue.component("MyCount",Count)
参数1:字符串格式，表示组件的“注册名称”
参数2:需要被全局注册的那个组件
```

### 组件样式冲突的问题

```html
默认情况下，写在.vue组件中的样式会全局生效,因此很容易造成多个组件之间的样式冲突。
导致组件之间样式冲突的根本原因是:
①单页面应用程序中,所有组件的DOM结构都是基于唯一的index
.html页面进行呈现的。
②每个组件中的样式都会影响整个index.html页面中的DOM。
写法:<style lang="less" scoped>/deep/ 类名{}</style>
socped属性:自动为每一个标签生成date-v-数字。
在父组件中直接修改子组件的样式时需要用到/deep/，当使用第三方组件库的时候，如果有修改第三方组件库默认样式的需求，需要用到/deep/。
```

## 组件的props

```html
props是组件的自定义属性,在封装通用组件的时候合理地使用props可以极大的提高组件的复用性。
语法:props:[“自定义属性名A”,"自定义属性名B"]
<自定义标签 自定义属性名=“”></自定义标签>
{{自定义属性名}}
注意点:
①自定义属性名的值如果是数字那么要在自定义属性名前面加上“:”，否则为字符串。“:”的意思就是v-bind。
②封装的自定义属性是只读的，不能直接修改props值，否则会报错，要修改props值可以把props的值转存到data中，因为data中的数据是可读可写的。
```

### props的default默认值

```html
语法:props:｛自定义属性:{default:0}｝
注:如果外界使用自定义组件的时候没有传递值则默认值生效，如果传了值则覆盖默认值。
```

### props的type值属性

```html
在声明自定义属性时，可以通过type来定义属性值的类型。
type:Number并在自定义属性名前面加上“:"
```

### props的required必填项

```javascript
语法:props:{自定义属性:{required:true}}
```

## 生命周期

```html
生命周期(life cycle)是指一个组件从创建->运行->销毁的整个阶段，强调的是一个时间段。
生命周期函数:是由vue框架提供的内置函数，会伴随着组件的生命周期，自动按次序执行。
```

### 组件生命周期函数分类

```html
       组件创建阶段
beforeCreate 创建实例对象之前执行
created 创建实例对象之后执行
beforeMount 页面挂载成功之前执行
mounted 页面挂载成功之后执行

       组件运行阶段
beforeUpdate 组件更新之前执行
updated 组件更新之后执行

       组件销毁阶段
beforeDestory 实例销毁之前执行
destroyed 实例销毁之后执行

①beforeCreate:组件的props、data、methods 尚未被创建，都处于不可用状态。－初始化事件和生命周期函数

②created:组件的props、data、methods①创建好,都处于可用状态。但是组件的模板结构尚未生成。－初始化props、data、methods，非常常用，一般用于发送ajax，数据转存到data中。

③beforeMount:将要把内存中编译好的HTML结构渲染到浏览器中,此时浏览器中还没有当前组件的DOM结构。

④mounted:已经把内存中的HTML结构,成功渲染到当前浏览器中，此时浏览器中已经包含了当前组件的DOM结构。

⑤beforeUpdate:将要根据变化过后，最新的数据，重新渲染组件的模板结构。

⑥updated:已经根据最数据，完成了组件DOM结构的重新渲染。

⑦beforeDestroy:将要销毁此组件,此时尚未销毁,组件还处于正常工作状态。－执行后销毁当前组件，数据侦听器、子组件、事件监听。

⑧destroyed:组件已经被销毁，此组件在浏览器中对应的DOM结构已经完全被移除。
```

## 自定义事件—子向父传值

```html
  $emit(“自定义事件名称”,传给父组件的新值)        
  子组件:this.$emit('numchange',this.count)
父组件:<Son @numchange="getNewCount"></SonSon>
      data(){
         retrun{
              countFromSon:0
}
}
      getNewCount(val){
         this.countFromSon=val
}
```

## 父向子传值

```html
例：
父组件：<son :msg="message" :user="userinfo"><son/>
data(){
    return{message:"数据1",userinfo:"数据2"}
    }
    子组件:<p>父组件传过来的值是{{msg}}</p>
          <p>父组件传过来的值是{{user}}</p>
    props:["msg","user"]
```

## EventBus数据共享

```javascript
①创建eventBus.js模块,并向外共享一个Vue的实例对象
②在数据发送方，调用bus.$emit(“事件名称”，要发送的数据)方法触发自定义事件
③在数据接收方，调用bus.$on(“事件名称”，事件处理函数) 方法注册一个自定义事件
eventBus文件内容:
import Vue from "vue"
export default new Vue() //向外共享vue的实例对象
例：
兄弟组件A(数据发送方)                               兄弟组件B(数据接收方)
import bus from './eventBus.js'                import bus from './eventBus.js’
export default {                                export default{
    data(){                                     data(){
        ruturn{                                 return{
            msg:'值'                            msgFromLeft:''
        }，                                                   }
        methods:{                                              },
            sendMsg(){                                        created(){
                bus.$emit('share',this.msg)                   bus.$on('share',val=>{
            }                                                 this.msgFromLeft=val
        }                                                     })
    }                                                              }
}                                                                       }
```

## ref引用

```javascript
ref可以在不依赖于jQuery的情况下,获取DOM元素或组件的引用。
每个vue的组件实例上,都包含了一个$refs对象,里面存储着对应的DOM元素或组件的引用,默认情况下组件的$refs指向一个空对象。
语法:
            加给标签 
<h1 ref="myh1">APP</h1>
this.$refs.myh1.style.color="red" 
            加给组件
<Left ref='myLeft'> </Left>
this.$refs.myLeft.count=0
```

## this.$nextTick(cb)方法

```javascript
组件的$nextTick(cb)方法,会把cb回调推迟下一个DOM更新周期之后执行，通俗理解是:等组件的DOM更新完成之后，在执行cb回调函数。从而能保证cb回调函数可以操作最新的DOM
```

## 数组中的some循环方法

```html
some循环在找到对应的项之后可以通过return:true固定语法可以终止some循环。
语法：
const arr=['小孩','大人','男人']
arr.some((item,index)=>{
if(item==='小孩'){
return true
}
})
```

## 数组中的every 循环方法

```html
every循环只要有任何一项不满足条件就返回false，满足则返回true。
语法：
const arr=[
{id:1,name='西瓜',state:true}
{id:2,name='苹果',state:true}
{id:3,name='梨子',state:true}
]
const result= arr.every(item=>item.state)
```

## 数组中的reduce方法

```javascript
const arr=[
{id:1,name='西瓜',state:true,price:10,count:1}
{id:2,name='苹果',state:true,price:20,count:2}
{id:3,name='梨子',state:true,price:30,count:3}
]
arr.filter(item=>item.state).reduce((amt,item)=>{
    return amt+=item.price*item.count
},0)

reduce((累加的结果，当前的循环项)=>{
return 算法
},初始值)
```

## 动态组件component标签

```html
语法:<component :is=''></component>
is:指定哪个组件就渲染哪个组件
```

## keep-alive保持状态

```html
用法:
<keep-alive>
<component :is='' include=‘’></component>
</keep-alive>
```

### keep-alive的include属性

```html
include属性用来指定:只有名称匹配的组件会被缓存，多个组件用逗号隔开。
```

### keep-alive的exclude属性

```html
exclude属性指定哪些组件不需要被缓存，但是不能同时使用exclude和include属性。
```

## v-slot指令

```html
①vue官方规定每一个slot标签都要有一个name属性。
②如果省略了name属性则有一个默认名称叫default。
③v－slot后面要跟上插槽的名字
④v－slot指令不能直接用在元素身上，必须用在template标签上
⑤v－slot指令的简写形式是 #
写法:
父组件<template v-slot:插槽的name></template>
子组件<slot name='插槽名称'></slot>
```

## 私有自定义指令

```javascript
可以在directives节点下声明私有自定义组件
写法:
directives:{
          color:{
         bind(el，binding){
      el.style.color=binding.value
                }
}
①定义为color的指令，指向一个配置对象。
②当指令第一次被绑定到元素上的时候，会立即触发bind函数。
③形参中的el表示当前指令绑定到的那个DOM对象。
④binding.value是固定写法
```

## update函数

```javascript
bind函数只调用一次:当指令第一次绑定到元素时调用，当DOM更新时bind函数不会被触发。update函数会在每次DOM更新时被调用。
updata函数在directives节点内。不是钩子函数不与data平级。
写法:
update(el,binding){
el.style.color=binding.value
｝
```

## 全局自定义指令

```javascript
写法:
Vue.directive('color',function(el,binding){
el.style.color=binding.value
})
参数1:字符串，表示全局自定义指令的名字
参数2:对象，用来接收指令的参数值
```

## 路由

### 路由的工作方式

```html
①用户点击了页面上的路由链接。
②导致URL地址栏中的Hash值变化。
③前端路由监听了Hash地址的变化。
④前端路由把当前的Hash地址对应的组件渲染在浏览器中。
```

### vue-router安装和配置路由

```javascript
①安装vue-router包
npm i vue-router@3.5.2 -S
②创建路由模块
在src源代码目录下，新建router/index.js路由模块，并初始化代码：
import Vue from 'vue'
import VueRouter from 'vue-router'
Vue.use(VueRouter)
const router=new VueRouter({routes:[
{path:'/home',component:Home}
]})
export default router
③在main.js文件导入并挂载路由模块
import router from '@/router/index.js'
并在new Vue({})里输入router
④声明路由链接和占位符
只要在项目中安装了vue-router就可以使用
<router-view></router-view>这个标签。
1.routes:是一个数组，作用定义hash地址与组件之间的对应关系。
2.Vue.use()函数的作用就是来安装插件。
3.VueRouter安装为Vue项目的插件。
```

### router-link

```html
写法:
<router-link to=''></router-link>
1.当安装和配置了vue-router后就可以使用router-link来代替普通的a标签了。
2.to就代替了href属性，并在to里面可以不用写#
```

### redirect重定向

```javascript
路由重定向指的是用户在访问地址A的时候，强制用户跳转到地址C，从而展示特定的组件页面，通过路由规则的redirect属性，指定鱼缸新的路由地址，可以很方便地设置路由的重定向。
例:{path:'/',redirect:'Home'}
当用户访问/的时候，跳转到/home对应的路由规则。
```

### children属性声明子路由和默认子路由规则

```javascript
在src/router/index.js路由模块中，导入需要的组件，并使用children属性声明子路由规则:
写法:
routers:[{
path:'/father',component:Father,
           //默认子路由
redirect:'./father/tab1',
,children:[{
path:'tab1',component:Tab1
}]
}]
```

### 默认子路由(拓展)

```javascript
默认子路由如果children数组中，某个路由规则的path值为空字符串，则这条子路由规则叫做默认子路由。
写法:{path:'',component:Tab1}
```

### 动态路由匹配

```html
动态路由指的是:把Hash地址中可变的部分定义为参数项,从而提高路由规则的复用性。
在vue-router中使用英文的冒号(:)来定义路由的参数项。
例:{path:'./movie/:id',component:Movie}
this.$route是路由的参数对象
this.$touter是路由的导航对象
```

### 路由props传参

```html
写法:{path:'/movie/id',component:Movie,props:true}
可以为路由规则开启props
```

### 拓展query和fullPath

```html
①在hash地址中/后面的参数项，叫做‘路径参数’。
②在路由参数对象中需要使用this.$route.params来访问路径参数。
③在hash地址中,?后面的参数项，叫做‘查询参数’。
④在路由参数对象中需要使用this.$route.query来访问查询参数。
⑤在this.route中path只是只是路径部分,fullPath是完整地址
```

### vue-router 中的编程式导航API

```javascript
①this.$router.push('hash地址') 
跳转到指定的hash地址，并增加一条历史记录
②this.$router.replace('hash地址')
跳转到指定的hash地址,并替换掉当前的历史记录
③this.$router.go(数值 n)
调用this.$router.go()方法,可以在浏览历史中前进和后退
$router.go的简化用法
$router.back() 在历史记录中，后退到上一个页面
$router.forward() 在历史记录中,前进到下一个页面
```

## 导航守卫

### 全局前置导航

```javascript
1.创建路由实例对象
const router =new VueRouter({})
router.beforeEach((to,from,next)=>{})
①调用路由实例对象的beforeEach方法，即可声明‘全局前置守卫’
②每次发生路由导航跳转到时候,都会自动触发fn这个回调函数
```

### 守卫方法3个形参

```html
to:是将要访问的路由的信息对象
from:是将要离开的路由的信息对象
next:是一个函数,调用next()表示放行,允许这次路由导航
```

### next函数的3中调用方式

```html
①当前用户拥有后台主页的访问权限，直接放行：next()
②当前用户满意后台主页的访问权限,强制其跳转到登录页面:next('/login')
③当前用户没有后台主页访问权限,不允许跳转到后台主页:next(flase)
```
