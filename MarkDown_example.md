##MaHua是什么?
一个在线编辑markdown文档的编辑器

向Mac下优秀的markdown编辑器mou致敬

##MaHua有哪些功能？

* 方便的`导入导出`功能
    *  直接把一个markdown的文本文件拖放到当前这个页面就可以了
    *  导出为一个html格式的文件，样式一点也不会丢失
* 编辑和预览`同步滚动`，所见即所得（右上角设置）
* `VIM快捷键`支持，方便vim党们快速的操作 （右上角设置）
* 强大的`自定义CSS`功能，方便定制自己的展示
* 有数量也有质量的`主题`,编辑器和预览区域
* 完美兼容`Github`的markdown语法
* 预览区域`代码高亮`
* 所有选项自动记忆

##有问题反馈
在使用中有任何问题，欢迎反馈给我，可以用以下联系方式跟我交流

* 邮件(dev.hubo#gmail.com, 把#换成@)
* QQ: 287759234
* weibo: [@草依山](http://weibo.com/ihubo)
* twitter: [@ihubo](http://twitter.com/ihubo)

##捐助开发者
在兴趣的驱动下,写一个`免费`的东西，有欣喜，也还有汗水，希望你喜欢我的作品，同时也能支持一下。
当然，有钱捧个钱场（右上角的爱心标志，支持支付宝和PayPal捐助），没钱捧个人场，谢谢各位。

##感激
感谢以下的项目,排名不分先后

* [mou](http://mouapp.com/) 
* [ace](http://ace.ajax.org/)
* [jquery](http://jquery.com)

##关于作者

```javascript
  var ihubo = {
    nickName  : "草依山",
    site : "http://jser.me"
  }
```


## Welcome to MarkdownPad 2 ##

**MarkdownPad** is a full-featured Markdown editor for Windows.

### Built exclusively for Markdown ###

Enjoy first-class Markdown support with easy access to  Markdown syntax and convenient keyboard shortcuts.

Give them a try:

- **Bold** (`Ctrl+B`) and *Italic* (`Ctrl+I`)
- Quotes (`Ctrl+Q`)
- Code blocks (`Ctrl+K`)
- Headings 1, 2, 3 (`Ctrl+1`, `Ctrl+2`, `Ctrl+3`)
- Lists (`Ctrl+U` and `Ctrl+Shift+O`)

### See your changes instantly with LivePreview ###

Don't guess if your [hyperlink syntax](http://markdownpad.com) is correct; LivePreview will show you exactly what your document looks like every time you press a key.

### Make it your own ###

Fonts, color schemes, layouts and stylesheets are all 100% customizable so you can turn MarkdownPad into your perfect editor.

### A robust editor for advanced Markdown users ###

MarkdownPad supports multiple Markdown processing engines, including standard Markdown, Markdown Extra (with Table support) and GitHub Flavored Markdown.

With a tabbed document interface, PDF export, a built-in image uploader, session management, spell check, auto-save, syntax highlighting and a built-in CSS management interface, there's no limit to what you can do with MarkdownPad.

###常见语法###
输出后的效果	Markdown 快捷键
Bold	**text**	Ctrl/⌘ + B
Emphasize	*text*	Ctrl/⌘ + I
Strike-through	~~text~~	Ctrl + Alt + U
Link	[title](http://)	Ctrl/⌘ + K
Inline Code	`code`	Ctrl/⌘ + Shift + K
Image	![alt](http://)	Ctrl/⌘ + Shift + I
List	* item	Ctrl + L
Blockquote	> quote	Ctrl + Q
H1	# Heading	
H2	## Heading	Ctrl/⌘ + H
H3	### Heading	Ctrl/⌘ + H (x2)  


##1.标题设置##
通过在文字下方添加=可以变成一个一级标题
=
通过在文字下方添加-可以变成一个一级标题
-
这是什么都不加的结果
二级标题下面有一横线
-
##使用##下方也有一横线##  
- **Headings 1, 2, 3 (`Ctrl+1`, `Ctrl+2`, `Ctrl+3`)**  


##2.块注释（blockquote）##
>通过在文字开头添加“>”表示块注释。（当>和文字之间添加五个blank时，块注释的文字会有变化。
>>块注释（blockquote）
通过在文字开头添加“>”表示块注释。（当>和文字之间添加五个blank时，块注释的文字会有变化。
>>>2.块注释（blockquote）
通过在文字开头添加“>”表示块注释。（当>和文字之间添加五个blank时，块注释的文字会有变化。  

快捷键为**ctrl+Q**，多敲一行可以结束块注释  
- **Code blocks (`Ctrl+K`)**

##3. 斜体##
将需要设置为斜体的文字两端使用1个“*”或者“_”夹起来  
将需要设置为*斜体*的文字两端使用1个“*”或者“_”夹起来  
将需要设置为斜体的文字两端使用1个“\*”或者“\_”夹起来将需要设置为*斜体*的文字两端使用1个“\*”或者“\_”夹起来,这里被转义了，出现了**混乱**  
- **Italic (`Ctrl+I`)**

###问题###
- - - 
**Q1.** 混乱问题怎么解决，有没有跟java语言中相同的转义符号"\"
> 转义符号仍为"\"
  
**Q2.** MarkDown怎么强制换行  

> 如果你确实想要依赖 Markdown 来插入 标签的话，**在插入处先按入两个以上的空格然后回车**。 的确，需要多费点事（多加空格）来产生 ，但是简单地「每个换行都转换为 」的方法在 Markdown 中并不适合， Markdown 中 email 式的 区块引用 和多段落的 列表 在使用换行来排版的时候，不但更好用，还更方便阅读

##4. 粗体##
将需要设置为斜体的文字两端使用“\*\*”或者“\_\_”夹起来  
快捷键为**Ctrl+B**

##5. 无序列表##
在文字开头添加(\*, \+, and \-)实现无序列表。但是要注意在(\*, \+, and \-)和文字之间需要添加空格。（建议：一个文档中只是用一种无序列表的表示方式)  

* 在文字开头添加(\*, \+, and \-)实现无序列表。但是要注意在(\*, \+, and \-)和文字之间需要添加空格。（建议：一个文档中只是用一种无序列表的表示方式)  
* 在文字开头添加(\*, \+, and \-)实现无序列表。但是要注意在(\*, \+, and \-)和文字之间需要
添加空格。（建议：一个文档中只是用一种无序列表的表示方式)  

<hr/>

    没想到html标签还可以用


* 测试子列表
	* 测试子列表
	* 只要插入一个tab键就可以了
* 测试子列表



- **Code blocks (`Ctrl+K`)**
- Headings 1, 2, 3 (`Ctrl+1`, `Ctrl+2`, `Ctrl+3`)
- Lists (`Ctrl+U` and `Ctrl+Shift+O`)


### 问题 ###
- - - 
**Q1.** 无序列表测试失败
> 前面空一行  

**Q2.** code blocks中怎么使用无序列表
> **？？**


##6. 有序列表##
使用数字后面跟上句号。（还要有空格）  
1. 使用数字后面跟上句号。（还要有空格）  
2. 使用数字后面跟上句号。（还要有空格）  
3. 使用数字后面跟上句号。（还要有空格）  
4. 使用数字后面跟上句号。（还要有空格）  
5.      

##7. 链接（Links）##
Markdown中有两种方式，实现链接，分别为内联方式和引用方式。  

- 内联方式：This is [baidu](http://www.baidu.com/ "访问baidu").  
- 引用方式：
I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3] or [baidu][4].
[1]: http://google.com/        "Google" 
[2]: http://search.yahoo.com/  "Yahoo Search" 
[3]: http://search.msn.com/    "MSN Search"
[4]: http://www.baidu.com/		"Baidu Search"
- - - 
[**Emmet语法速查表**](http://www.powerxing.com/emmet-syntax-cheatsheet/ "Emmet语法速查表") 

## 8. 图片（Images） ##
图片的处理方式和链接的处理方式，非常的类似。

- 内联方式：  
![alt text](http://f.hiphotos.baidu.com/baike/g%3D0%3Bw%3D268/sign=3c4e049cc1cec3fd9b3ea27ea1b5e609/6159252dd42a2834b1c7cf5b59b5c9ea15cebf79.jpg "网络图片插入")
- 引用方式：  
![alt text][1] 

[1]: /logo.jpg "本地图片使用的是相对引用"


## 9. 代码（HTML中所谓的Code） ##
实现方式有两种：

- 第一种：简单文字出现一个代码框。使用`<blockquote>`。  
（`不是单引号而是左上角的ESC下面~中的`）  
- 第二种：大片文字需要实现代码框。使用Tab或四个空格。  

		public static void main(String arg){  
		    System.out.print("MarkDown好好玩");  
			System.out.print("MarkDown好好玩");  
			System.out.print("MarkDown好好玩");  
			System.out.print("MarkDown好好玩");   
		}
### 问题 ###
- - - 
**Q1.** MakeDown实现缩进 

> 不断行的空白格& nbsp;或& #160;  
> 半方大的空白& ensp;或& #8194;  
> 全方大的空白& emsp;或& #8195;  
注：去掉&后的空格

**Q2.** MakeDown插入整段代码效果不明显
> **第一行记得空一行**

## 10. 脚注（footnote） ##
实现方式如下：
hello[^1]


[^1]: 这个是其那面的脚注，在前面哦，不管标在哪里都出现在最后面的，不信你点一下
### 问题 ###
- - - 
**Q1.** MakeDown 实现脚注

> **？？**好像没效果 


## 11. 分割线 ##
— 或 – – – 或者 * * *
我是用来测试分割线的  
- - -  
横杠 空格 横杠 空格 横杠 空格 就可以了
其实也可以用html标记
<hr/>

## 12. 表格 ##



	具体使用方式请看示例。   
	* ------:为右对齐。   
	* :------为左对齐。   
	* :------:为居中对齐。   
	* -------为使用默认居中对齐。  
	
	1.9.2 示例
	
|标题|

|         序号    |    交易名    |    交易说明    |    备注    |
|    ------: |    :-------:    |    :---------   |    ------    |
|    1    |    prfcfg    |    菜单配置    |    可以通过此交易查询到所有交易码和菜单的对应关系    |
|    2    |    gentmo    |    编译所有交易    |    |
|    100000    |    sysdba    |    数据库表模型汇总    |    |  
	
		  
	
	**注意**：每个Markdown解析器都不一样，可能左右居中对齐方式的表示方式不一样。
	```


更多可以参考[www.zybuluo.com](https://www.zybuluo.com/AntLog/note/63228 "zybuluo的博客，还可以在线编辑")  
**这个人很厉害的样子，模仿一下？**
- - - 
然并卵，上面的好像**不能用**，还是看下面的吧  

**``` 升级就可以用了```**

注册email:  
 
	www.zixue.it
	
注册码:
	
	4vuvQFtGkF0oH7by922v75FtaUGq7niFveCKDxqC2KSqYTfaSGzxzxKQXNhc2BG51N9URrF71PZcBGdVxEm41c/FasBJQybIEYkahzRnjGwhaEocTe2eye6RZpzjaEvoz9fm04e2oyveK5wjXAXVmTRTDnTJvbNG7pEH1y6SC5mgxbhrNQ5/2GyQD7Ml/X2ipVZ7MdQkFdkEiM+H+99/ar0azcwrdQ8s0Zg31kjdcbVsL3DjW2GMlvxsvGpCVjn7savohzdhHq7QjFrl5/C4e6TVsEjaaBSVkAA18ag2Dvx7c2vOf9OlndNZxE8GARRSV2lQdahNKlrKIYK3E3UpgQ==
- - - 
目前编辑器不支持表格，以往是通过截图，呈现的效果并不好，Markdown支持html，所以我们可以用html来写表格。但是......用html写表格，实在太麻烦了，这里有个简单的转换方法，供大家参考：

举例，假设有这样一个表格，内容如下：

	时间 地点 人物  
	3月5日 北京 姚明  
	3月7日 上海 韩寒  

处理方法如下：

1. 从word或excel中复制表格

2. 打开此[链接](http://pressbin.com/tools/excel_to_html_table/index.html "表格转html")

3. 贴上复制的文字，然后按convert，就会得到这个表格的代码。


简要说明表格设定如下：

1. 将第一个`<table\>`变成`<table class="table table-bordered table-striped table-condensed"\>`。

		为什么要加它们呢？这三个是什么意思呢？  

		解释如下：
		它们都会给表格带上某种样式，如果没有的话，比较不好看：
		 table-bordered：带圆角边框和竖线  
		 table-striped：奇偶行颜色不同  
		 table-condensed：压缩行距  
		以上三个可以进行不同的组合，如果是很长的表格，建议只用后两个。


2. 另外，如果需要表头跟内容不一样，可以将<td\>表头内容</td\>换成<th\>表头内容</th\>。

3. 如果表格内文需要换行，可以在要换行的内容后加入<br\>，后面的内容就会跑到下一行。

4. 如果内文中有代码，需要特别显示，可使用：<code\>代码</code\>。

5. 如果表格中有需要设为斜体的内容，可使用：<I\>要设为斜体的内容</I\>。

6. 如果有跨行或者跨列的单元格，可用<th colspan="跨列数"\>内容</th\>。
跨行则是用rowspan="跨行数"。

7. 如果要调整某一列的宽度，可使用：<th width="宽度值或百分比"\>表头内容</th\>。

8. 如果要调整整个表格的宽度，可以参考berlinix的这篇[文章](http://www.ituring.com.cn/article/details/8367 "berlinix")


##13. 空格##
Markdown语法会**忽略首行开头的空格**，如果要体现出首行开头空两个的效果，可以使用**全角**符号下的空格，windows下使用**shift+空格**切换  
  我空个了哦  
　　我换行了全角下面真的可以空格
　　新技能get

##13. 很少用到的##
1. 标签  
标签: 数学 英语  
Tags: 数学 英语
2. 删除线  
  
~~这是一条删除线~~ 	 

### 问题 ###
- - - 
**Q1.** MakeDown Tag标记

> **？？**好像没效果 
**Q2.** MakeDown 删除线

> **？？**好像没效果，编辑器里面没有效果，但是挂到github上就可以显示了

图灵社区的一个学习链接：[MarkDown](http://www.ituring.com.cn/article/504 "MarkDown")






  
  

#使用pandoc转换格式#

## windows 下安装pandoc ##

## 切换到工作路径 ##
1. `cd..`向上一级目录
2. 根目录下直接输入盘符可以直接切换盘符，如在`C:\`下可以直接输入`H:\`
3. 检查pandoc是否正确安装可使用`pandoc --version`、`pandoc -v`、`pandoc --help`以及`pandoc -h`

## 常用指令介绍 ##





## 查看盘中已有的字体文件 ##

在控制台中输入命令：`fc-list >> C:\fonts.txt`。这样，扫到的字体信息就全部被导入到C盘根目录下的fonts.txt文件中了。

使用`fc-list :lang=zh-cn > C:\font_zh-cn.txt`查看系统中的所有字体  
详情可参加：[http://liam0205.me/2014/09/08/latex-introduction/](http://liam0205.me/2014/09/08/latex-introduction/)

文件格式为：<字体文件路径>: <字体标示名 1>, <字体表示名 2>:Style=<字体类型>
如：

	C:/WINDOWS/fonts/simsun.ttc: 宋体,SimSun:style=Regular

出现了之前文档里调用的字体SimSun，此处表明该字体有两个表示名：宋体和SimSun，我们在\setCJKmainfont{·}中填入任意一个都有同样的效果。


## 安装转pdf支持文件 ##
使用pandoc将其他文件格式的文件转为pdf需要使用[LaTeX](http://www.pandoc.org/installing.html)  
> For PDF output, you’ll also need to install LaTeX. We recommend MiKTeX.  

[MiKTeX 下载](http://miktex.org/)

## 指定转存pdf时所用编译方式 ##
pandoc 默认选择的是 pdflatex 方式编译，pdflatex 不支持中文，因此，可以通过在转换时指定 xelatex 编译方式来解决，具体命令如下：

	pandoc filename.md -o filename.pdf --latex-engine=xelatex

## 中文下转pdf下中文不显示问题 ##

打开pdf文件一看，内容都是空白，这是由于中文字体的原因，这个问题，我们可以通过以下两个方法解决。  

1. 在转换时显示指定使用字体，命令如下：`-V mainfont="SimSun"`
2. 修改编译方式 `--latex-engine=xelatex`

## 中文下转pdf越界问题 ##
使用模板可以解决 具体步骤为：下载模板，放到同一个文件夹下，然后加入语句`--template=pm-template.latex` “=”号后面为模板名称

## 测试 ##

- 英文转pdf

		pandoc eng.md -o eng.pdf 
- 中文转pdf  

		pandoc chinese.md  -o chinese.pdf --latex-engine=xelatex  -V mainfont="SimSun"
		
- 中文转pdf使用模板  
	- github上的一个模板

		pandoc alibaba.md  -o alibaba.pdf --latex-engine=xelatex  -V mainfont="SimSun" --template=pm-template.latex  
	- 大神专治懒癌·l 提供的模板

		pandoc alibaba.md  -o alibaba_chinese.pdf --latex-engine=xelatex  --template=chinese.latex

	NB.专治懒癌·l的模板不需要使用`-V mainfont="SimSun"`参数

- 关于提示 `! Undefined control sequence. l.80 \tightlist`

新版本中增加了tightlist提示，运行时可以在模板中加入声明tightlist相关申明即可。

	\newcommand{\tightlist}{%
	 \setlength{\itemsep}{0pt}\setlength{\parskip}{0pt}}

详情请参见gym的github [LaTeX writer: Use a declaration for tight lists #1571](https://github.com/jgm/pandoc/pull/1571)

大神github [LiamHuang0205](https://github.com/LiamHuang0205)

		

## 转换pdf常用参数 ##

- `–latex-engine=pdflatex|lualatex|xelatex`


	–latex-engine用来指定转换PDF格式时LaTeX引擎，默认情况下是pdflatex，但是由于pdflatex不支持中文，因此需要将引擎设置为xelatex

- `–template=FILE`

    使用FILE指定的文件作为输出文档的自定义模板。可将模板文件放置任意处，只是指定FILE时需要该FILE的路径。

- `–toc, –table-of-contents`

    使用该参数后，会在输出文档开头自动产生文件目录，对于输出格式是man, docbook, slidy, slideous, s5, docx 或者odt的文档，该参数不起任何作用。

- `–toc-depth=NUMBER`

    指定文件目录中包含的章节级别，默认NUMBER=3，表示一级标题、二级标题、三级标题都会被在目录中展示。

- `-V KEY[=VAL], –variable=KEY[:VAL]`

    当渲染standalone模式下文档时，设置模板变量KEY的值为VAL。pandoc会自动设置默认模板中的这些变量，因此该选项这通常在使用–template选项指定自定义模板时有用，如果没有指定VAL值，那么该KEY会被赋予值true。

- `-s, –standalone`

    转换输出文档时会自动加上合适的header和footer(例如standalone HTML, LaTeX, RTF).该选择在转换输出pdf，epub，epub3，fb2，docx，odt格式文件时会被自动设置，因此如果转换输出上述格式文件，则不用显示指定该选项。

-  `-N, –number-sections`

    对于转换输出LaTeX, ConTeXt, HTML, EPUB格式文档时，对文中章节进行编号。默认情况下，文章的章节是不会被编号的。对于使用了class unnumbered 的章节肯定不会被标号，即使使用了–number-sections选项。

## 查看Page layout in latex 文档 ##

在命令行中使用`texdoc fancyhdr`或打开`
G:\ANEWWIN7\MiKTeX\doc\latex\fancyhdr\fancyhdr.dvi`,前面为安装路径。




