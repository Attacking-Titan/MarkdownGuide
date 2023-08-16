# Markdown教程

**注：本教程的Markdown代码示例的效果预览都在其对应代码下。**

<span id="#base"></span> 
**[Markdown基础语法](#base "Markdown基础语法")**  
[标题](#heading "标题")  
[段落](#paragraph "段落")  
[换行](#wrap "换行")    
[粗体](#bold "粗体")  
[斜体](#italic "斜体")  
[粗体与斜体](#bold&italic "粗体与斜体")  
[引用](#quote "引用")  
[列表](#list "列表")  
[代码](#code "代码")  
[分隔线](#line "分隔线")  
[链接](#link "链接")  
[图片](#image "图片")  
[转义字符](#escape "转义字符")  
[内嵌HTML标签](#mark "内嵌HTML标签")  
**[Markdown拓展语法](#expand "Markdown拓展语法")**    
[表格](#table "表格")  
[围栏代码块](#fence "围栏代码块")  
[脚注](#footnote "脚注")  
[标题编号](#titleNumber "标题编号")  
[定义列表](#definitionList "定义列表")  
[删除线](#deleteLine "删除线")  
[任务列表](#taskList "任务列表")  
[Emoji表情](#emoji "Emoji表情")  
[自动网址链接](#autoLink "自动网址链接")  
[获取代码](#getCode "获取代码")

<span id="heading"></span>
## 标题
在标题内容前添加#表示标题，#的数量表示标题的级别  

```
# heading       
## heading      
### heading     
#### heading        
##### heading       
###### heading      
```

效果：
# heading       
## heading      
### heading     
#### heading        
##### heading       
###### heading  

为了考虑兼容性，请在#与标题内容之间添加一个空格  
![标题的使用](https://i.hd-r.cn/c0f17f4dc03f7ef4a2dcc01f7da65d54.png)

可选语法：  
1.在标题内容的下一行添加任意`==`可以标识为一级标题  

```
This is heding1
==
``` 
2.在标题内容的下一行添加`--`可以标识为二级标题  
```
This is heading2    
--
```  

注：经测试发现以上可选语法在Subline Text的实时预览中生效，在浏览器中预览时没有效果。


<span id="paragraph"></span>
## 段落
要创建段落，用空白行将不同段落内容分隔

```
This is paragraph1

This is paragraph2
```

This is paragraph1

This is paragraph2

不要用空格(space)或制表符(tab)来缩进段落  
![段落的使用](https://i.hd-r.cn/ebfd281fae3f64566224f764de5e7e78.png)

<span id="wrap"></span>
## 换行
1.在一行的末尾添加两个空格可以表示换行  
2.使用`<br>`或`<br/>`表示从该位置进行换行

```
when a sentence gets too long,we need to wrap it.<br/>like this
```

when a sentence gets too long,we need to wrap it.<br/>like this

<span id="bold"></span>
## 粗体
用两个星号(`**`)或两个下划线(`__`)包围一段文字可以标识该段文字为粗体。

```
**This is a piece of bold text**
__This is a piece of bold text__
```

**This is a piece of bold text**  
__This is a piece of bold text__  
注意：`**`或`__`与文本之间不能存在空格，用`**`或`__`只能将一行标识为粗体，不能将多行标识为粗体

为了考虑兼容性，一般用`**`包围文本来标识为粗体：  
![粗体的使用](https://i.hd-r.cn/a9f344daa116f0c7095e7d1316d8e76c.png)

<span id="italic"></span>
## 斜体
用一个星号(`*`)或一个下划线(`_`)包围一段文字可以标识该段文字为粗体 

```
*This is a piece of text in italics*  
_This is a piece of text in italics_
```

*This is a piece of text in italics*    
_This is a piece of text in italics_  
注意：`*`或`_`与文本之间不能存在空格，用`*`或`_`只能将一行标识为斜体，不能将多行标识为斜体

为了考虑兼容性，一般用`*`包围文本来标识为斜体：  
![斜体的使用](https://i.hd-r.cn/d27fc4935ec43bd4e9941d1dc7311c27.png)  

<span id="bold&italic"></span>
## 粗体与斜体
用三个星号(`***`)或三个下划线(`___`)包围一段文字可以标识该段文字为粗体和斜体

```
***This is a piece of text in bold and italic***
___This is a piece of text in bold and italic___
```

***This is a piece of text in bold and italic***  
___This is a piece of text in bold and italic___  
注意：`***`或`___`与文本之间不能存在空格，用`***`或`___`只能将一行标识为粗体和斜体，不能将多行标识为粗体和斜体

为了兼容性，一般用`***`标识为粗体+斜体：  
![粗体和斜体的使用](https://i.hd-r.cn/8e66d27e0a713b4bfc8078ee53e079ae.png)

<span id="quote"></span>
## 引用
1.单句引用  
在引用内容前添加一个`>`可以标识为引用,一般需要用空白行将引用与其他内容分隔开  
``> This is a quote``    

>This is a quote   

2.多段落的块引用  
块引用可以包含多个段落，请在段落之间的空白行添加一个`>`  

```
下面是块引用：
> This is quote1
> 
> This is quote2  
```

下面是块引用：
> This is quote1
> 
> This is quote2 

3.嵌套引用
在嵌套引用的语句前添加一个`>>`

```
> This is a quote  
>> This is a nested quote
```

> This is a quote  
>> This is a nested quote

<span id="list"></span>
## 列表
**有序列表**  
要创建有序列表，请在每个列表项前面添加数字并紧跟一个英文句号。

```
1.First item
2.Second item
3.Third item
```

1.First item  
2.Second item  
3.Third item  

有时候在句号与列表内容之间添加空格会导致被识别为无序列表，例如:

```
1. First item
2. Second item
3. Third item
```

可以在句号和空格之间加上反斜杠（\）来转义来避免这个问题：

```
1.\ First item
2.\ Second item
3.\ Third item
```

**无序列表**  
要创建无序列表，请在每个列表内容前面添加一个星号(*)或减号(-)或加号(+),并再添加一个空格

```
* First item
* Second item
* Third item
```

或

```
- First item
- Second item
- Third item
```

或

```
+ First item
+ Second item
+ Third item
```
以上三种效果相同：  
+ First item  
+ Second item  
+ Third item  

注意：不要将`*`、`-`、`+`混合使用，因为在浏览器中不起作用。

**列表的嵌套使用**
缩进一个或多个列表项可以创建嵌套列表,注意下面嵌套元素使用的符号：

```
+ Tea
    * red tea
    * white tea
+ wine  
    * beer  
        - stout
        - witbier
    * white spirit
```

+ Tea
    * red tea
    * white tea
+ wine  
    * beer  
        - stout
        - witbier
    * white spirit

**在列表中嵌套其他元素**
要保留列表连续性的同时在列表中添加其他元素，请将该元素缩进四个空格(space)或一个制表符(tab),如果列表项存在嵌套元素，那么请用空行将其与下一个列表项分隔开。

```
* First item  
    > This is a quote

* Second item  
    1.\ item1
    2.\ item2

* Third item
```

* First item  
    > This is a quote  

* Second item  
    1.\ tem1  
    2.\ item2  

* Third item

```
+ First item
    ![列表中嵌套图片](https://i.hd-r.cn/55622d6146e0db19020f614dabde97dd.png)

+ Second item
    ![列表中嵌套图片](https://i.hd-r.cn/f79464aa8ee05fdced1731483f9b1d6f.png)
```

+ First item  
    ![列表中嵌套图片](https://i.hd-r.cn/55622d6146e0db19020f614dabde97dd.png)

+ Second item  
    ![列表中嵌套图片](https://i.hd-r.cn/f79464aa8ee05fdced1731483f9b1d6f.png)

**列表中嵌套代码块**  
代码块通常采用四个空格(space)或一个制表符(tab)进行缩进。当它们嵌入列表中时，请将代码块缩进八个空格(space)或两个制表符(tab)。  
代码块通常前后预留一个空白行。

```
* C language code
        <stdio.h>  
        int main(){  
            printf("hello,world");  
            return 0;  
        }  

* Java language code  

        public static void main(String []args){
            System.out.println("hello,world");
        }

* JS language code

        alert("hello,world");
```

* C language code  

        <stdio.h>    
        int main(){
            printf("hello,world");
            return 0;
        }  
 
* Java language code    

        public static void main(String []args){
            System.out.println("hello,world");
        }

* JS language code

        alert("hello,world");

<span id="code"></span>
## 代码
**单句代码**  
如果要将一段单词或短语表示为代码，请将其包裹在反引号(\`)中  
```
`align: center;`实现文本居中
```  
`align: center;`实现文本居中  

**转义反引号**  
如果要在代码中使用反引号(\`),请使用两个反引号(\`\`)包裹代码

```
这段代码中需要用到反引号:``var value = `transform: translateX(${value})`;``
```

这段代码中需要用到反引号:``var value = `transform: translateX(${value});``

**代码块**  
要创建代码块，请将代码块的每一行至少缩进四个空格(space)或一个制表符(tab)。由于代码块也是段落，因此代码块的前后需要有一个空白行。

```
代码块需要缩进四个空格(space)或一个制表符(tab)  

    <HTML>
        <p>This is a paragraph</p>
    </HTML>

代码块的前后需要预留两个空白行
```

代码块需要缩进四个空格(space)或一个制表符(tab)  

    <HTML>
        <p>This is a paragraph</p>
    </HTML>

代码块的前后需要预留两个空白行

<span id="line"></span>
## 分隔线
要创建分隔线，在单独一行使用三个或更多的星号(`***`)或减号(- - -)或下划线(`___`)，并且不能包含其他内容。  
注意：在单行中使用三个减号(`- - -`)创建分隔线必须用空格将`-`隔开。

```
三个`***`创建分隔线
***
三个`- - -`创建分隔线  
- - -
三个`___`创建分隔线
___
```

三个`***`创建分隔线
***
三个`- - -`创建分隔线  
- - -
三个`___`创建分隔线
___

<span id="link"></span>
## 链接
超链接语法：`[超链接显示名][超链接地址 "超链接title"]`  
对应的HTML代码：`<a href=”超链接地址” title=”超链接title”>超链接显示名</a>`  
超链接title是当鼠标悬停在链接上时会出现的文字，这个title是可选的，它放在圆括号中链接地址后面，跟链接地址之间以空格分隔。  

```
B站：[www.bilibili.com/](https://www.bilibili.com/ "Bilibili")  
E站：[www.edddh.com](www.edddh.com/ "E站")
```

B站：[www.bilibili.com/](https://www.bilibili.com/ "Bilibili")  
E站：[www.edddh.com](www.edddh.com/ "E站")

**网址和邮箱**  
使用尖括号将网址或邮箱括起来也可以将网址或邮箱变成可以点击的链接  
```
<https://markdown.com.cn>
<fake@example.com>  
```
<https://markdown.com.cn>  
<fake@example.com>

**带格式化的链接**  
强调链接，用两个星号(`**`)包围链接代码 
将链接展示为斜体，用一个星号(`*`)包围链接代码
要将链接显示为代码，在链接代码的方括号中用反引号(\`)包裹链接地址  
```
点击**[https://markdown.com.cn](https://markdown.com.cn)**访问Markdow中文官网
点击*[https://markdown.com.cn](https://markdown.com.cn)*访问Markdow中文官网
点击[`https://markdown.com.cn`](https://markdown.com.cn)访问Markdown中文官网
```
点击**[https://markdown.com.cn](https://markdown.com.cn)**访问Markdow中文官网  
点击*[https://markdown.com.cn](https://markdown.com.cn)*访问Markdow中文官网  
点击[`https://markdown.com.cn`](https://markdown.com.cn)访问Markdown中文官网  

**引用类型链接**  
引用格式：`[链接的文本][标签]`  
注：`[链接的文本]`与`[标签]`之间可以存在一个空格  
标签不区分大小写，标签可以由字母、数字、空格及标点符号组成。

引用主体：``[标签]:<链接地址>(可选标题)``  
链接地址的尖括号`<>`可以省略  
可选标题是当鼠标移动到链接上方时显示的提示文字。  
链接的可选标题，可以将其括在双引号、单引号或括号中。

引用类型链接是为了方便管理链接，用一个标签引用链接，可以统一将引用主体放在某个位置方便管理链接，引用主体仅在代码中可以看到。

```
中国最大的动漫社区[Bilibili][1]  
点击[这里][2]访问Markdown中文官网  
[1]: https://www.bilibili.com/ "Bilibili"
[2]: http://www.markdown.com.cn/ "Markdown"  
```

中国最大的动漫社区[Bilibili][1]  
点击[这里][2]访问Markdown中文官网  
[1]: https://www.bilibili.com/ "Bilibili"
[2]: http://www.markdown.com.cn/ "Markdown"  

注意：如果链接中存在空格，用%20代替

<span id="image"></span>
## 图片
图片语法：`![图片alt](图片链接 "图片title")`    
对应的HTML代码：`<img src="图片链接" alt="图片alt" title="图片title"/>`

```
![linux][https://i.hd-r.cn/f79464aa8ee05fdced1731483f9b1d6f.png "linux"]
```

![linux](https://i.hd-r.cn/f79464aa8ee05fdced1731483f9b1d6f.png "linux")  

Markdown中的图片通常会放在图床上，图片的链接由图床提供。  

<span id="escape"></span>
## 转义字符
| 符号 | 名称 |  
|:---:|:---:|  
|\\|斜杆|  
|\`|反引号|  
|\*|星号|  
|\_|下划线|  
|\[\]|中括号|  
|\{\}|花括号|  
|\(\)|括号|  
|\+|加号|  
|\-|减号|  
|\.|英文句号|  
|\!|英文感叹号|  
|\||管道符|

```
用\\可以转义一些特殊字符:  
**\\**  
**\`**  
__\*__  
**\_**  
**\{ \}**  
**\[ \]**  
**\( \)**  
**\+**  
**\-**  
**\.**  
**\!** 
**\|**
```

用\\可以转义一些特殊字符:  
\\   
**\`**  
__\*__  
**\_**  
**\{ \}**  
**\[ \]**  
**\( \)**  
**\+**  
**\-**  
**\.**  
**\!**  
**\|**

**特殊字符自动转义**  
HTML文件中，有两个字符需要特殊处理：< 和 &  
<符号用于起始标签，&符号用于标记HTML实体，如果你需要使用这些符号那么必须使用实体的形式：`&lt`;和`&amp`;  
Markdown 允许你直接使用这些符号，它帮你自动转义字符。  
如果你要在文件中插入一个著作权的符号：&copy，Markdown不会对这段文字进行修改。  
如果你这样写：`AT&T`，Markdown就会将其转为`AT&amp;T`  
类似的状况也会发生在`<`符号上，因为 Markdown 支持 行内 HTML ，如果你使用`<`符号作为 HTML 标签的分隔符，那 Markdown 也不会对它做任何转换

<span id="mark"></span>
## 内嵌HTML标签
HTML的行内标签如`<span>`\、`<cite>`、`<del>`不受限制，可以在 Markdown的段落、列表或是标题里任意使用。  
依照个人习惯，甚至可以不用 Markdown 格式，而采用 HTML 标签来格式化。

```
<h1>This is a heading</h1>
<h3>This is a heading</h3>
<p>This is a paragraph</p>
<cite>This is a quote</cite>  
<a href="www.bilibili.com" title="www.bilibili.com">Bilibili</a>

```

<h1>This is a heading</h1>
<h3>This is a heading</h3>
<p>This is a paragraph</p>
<cite>This is a quote</cite>  
<a href="www.bilibili.com" title="www.bilibili.com">Bilibili</a>

区块元素──比如`<div>`、`<table>`、`<pre>`、`<p>` 等标签，必须在前后加上空行，以便于内容区分。  
而且这些元素的开始与结尾标签，不可以用 tab 或是空白来缩进。  
Markdown 会自动识别这区块元素，避免在区块标签前后加上没有必要的 <p> 标签。  
不过需要注意，这些标签在一些Markdown的编辑器中不一定支持。

```
HTML中的区块元素在Markdown使用时，必须在前后加上空行：

<pre>
int main(){
    printf("hello,world");
    return 0;
}
</pre>

就像上例一样。
```

- - -

<span id="expand"></span>
# Markdown拓展语法
**注：一些Markdown编辑器实时预览时并不支持Markdown拓展语法，而在浏览器预览以及导出的HTML支持Markdown拓展语法。 
<span id="table"></span> 
## 表格
**创建表格**
要添加表格，请使用三个或多个连字符（---）创建每列的标题，并使用管道符(|)分隔每列。您可以选择在表的任一端添加管道。

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

```

| Syntax      | Description |  
| ----------- | ----------- |  
| Header      | Title       |  
| Paragraph   | Text        |  

单元格宽度可以变化，效果不变：

```
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
```

| Syntax | Description |  
| --- | ----------- |  
| Header | Title |  
| Paragraph | Text |  

**对齐**  
左对齐: 在连字符`-`的左侧添加`:`  
右对齐: 在连字符`-`的右侧添加`:`  
居中： 在连字符`-`的两端添加`:`  
表格默认是左对齐。

右对齐：
```
| Syntax      | Description |
| ----------: | ----------: |
| Header      | Title       |
| Paragraph   | Text        |
```

| Syntax      | Description |  
| ----------: | ----------: |  
| Header      | Title       |  
| Paragraph   | Text        |  

居中：

```
| Syntax      | Description |
| :---------: | :---------: |
| Header      | Title       |
| Paragraph   | Text        |
```

| Syntax      | Description |  
| :---------: | :---------: |  
| Header      | Title       |  
| Paragraph   | Text        |  

**格式化表格的文字**  
您可以在表格中设置文本格式。例如，您可以添加链接，代码（仅反引号（\`）中的单词或短语，而不是代码块）和强调。  
您不能添加标题，块引用，列表，水平规则，图像或HTML标签  
注：在表中转义管道符:用`&#124`;表示管道符(|)

<span id="fence"></span>
## 围栏代码块
Markdown基本语法允许您通过将行缩进四个空格或一个制表符来创建代码块。如果发现不方便，请尝试使用受保护的代码块。  
在代码块之前和之后的行上使用三个反引号（\`\`\`）或三个波浪号（`~~~`）。  
注：有些Markdown编辑器的实时预览可能不支持使用`~~~·来标识代码块。  
![围栏代码块示例](https://i.hd-r.cn/2439846100d307ecd534e4b69f052698.png "围栏代码块示例")  
~~~
<stdio.h>
int main(){
    printf("hello,world");
    return 0;
}
~~~

```
public static void main(String[] args){
    System.out.println("hello,world");
}
```

**语法高亮**  
要添加语法突出显示，请在代码块之前的反引号(\`\`\`)旁边指定一种语言。  
![语法高亮](https://i.hd-r.cn/ccb32ffe6a0b1e66214aee34a2406c60.png)

```c                               
<stdio.h>                                 
int main(){                               
    printf("hello,world");                        
    return 0;                             
}                                 
```                                 

```java                                 
public static void main(String[] args){                 
    System.out.println("hello,world");              
}                                   
```                                 
                                    
```python                               
print("Hello, world!")                          
```                             
                                    
```json                                 
{                                   
  "firstName": "John",                          
  "lastName": "Smith",                          
  "age": 25                             
}                                   
```

<span id="footnote"></span>
## 脚注
要创建脚注参考，请在方括号（`[^1]`）内添加插入符号`^`和标识符。  
标识符可以是数字或单词，但不能包含空格或制表符。  
标识符仅将脚注参考与脚注本身相关联-在输出中，脚注按顺序从1编号。  
在括号内使用另一个插入符号和数字添加脚注，并用冒号和文本（`[^1]:footnote.`）。  
您不必在文档末尾添加脚注。您可以将它们放在除列表，块引号和表之类的其他元素之外的任何位置。  
每个脚注需要占用一行位置。

```
Here's a simple footnote,[^1] and here's a longer one.[^foonote]

[^1]: This is the first footnote.
[^footnote]: This is the second footnote.

```

Here's a simple footnote,[^1] and here's a longer one.[^longnote]  
注：此处引用的脚注见页面底部

<span id="titleNumber"></span>
## 标题编号
要添加自定义标题ID，请在标题内容的右边用花括号括起它的ID  
``### Heading{id-name}``  
相当于HTML:  
``<h3 id="id-name">Heading</h3>``

**链接到标题ID**  
语法：``[链接标题][#标题ID]``  
相当于HTML：   
``<a href="#标题ID">链接标题</a>``  
  
Markdown中的标题ID只是为了给标题添加一个唯一的标识符，以便于在文档中进行链接和引用。  
然而，Markdown本身并不支持直接通过标题ID来实现跳转功能。  
要实现标题跳转，需要使用特定的工具或编辑器来解析Markdown文档，并将标题ID与相应的跳转链接关联起来  

跳转效果像[这样](#base "回到顶部")

<span id="definitionList"></span>
## 定义列表
要创建定义列表，请在第一行输入术语。在下一行输入`:`,后面跟一个空格和定义

```
First Term
: This is the definition of the first term.
Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```

相当于HTML：

```
<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>
```

效果：  
First Term  
: This is the definition of the first term. 

Second Term  
: This is one definition of the second term.  
: This is another definition of the second term.  

<span id="deleteLine"></span>
## 删除线
您可以通过在文本中心放置一条水平线来标识删除。  
~~结果看起来像这样~~。  
此功能使您可以指示某些文本是一个错误，要从文档中删除。  
若要删除文本，请在文本前后使用两个波浪号~~  
``~~这是一段错误的文本~~``  
~~这是一段错误的文本~~  

<span id="taskList"></span>
## 任务列表
任务列表使您可以创建带复选框的项目列表，在支持任务列表的Markdown应用程序中，复选框将显示在内容旁边。  
要创建任务列表，在任务项之前添加减号`-`和方括号`[]`，并在`[]`前面加上空格，要选择一个复选框，请在方括号之间添加小写字母x  
未勾选的复选框: `- [] task`  
勾选的复选框: `- [x] task`  
注意：任务列表与其他语句之间需要用空行隔开

```
- [x] Write the press release
- [x] Update the website
- [ ] Contact the media
```

- [x] Write the press release  
- [x] Update the website  
- [ ] Contact the media  

<span id="emoji"></span>
## Emoji表情
一些Markdown应用程序允许您通过键入表情符号短代码来插入表情符号。  
这些以冒号开头和结尾，并包含表情符号的名称。  

可以在此获取表情符号简码列表：[Complete list of github markdown emoji markup](https://gist.github.com/rxaviers/7360908)

```
:smiley:
:heart_eyes:
:birthday:
:fire:
```

:smiley:  
:heart_eyes:  
:birthday:  
:fire:

<span id="autoLink"></span>
## 自动网址链接
许多Markdown处理器会自动将URL转换为链接。  
这意味着如果您输入`http://www.example.com`，即使您未使用方括号，您的Markdown处理器也会自动将其转换为链接。  
警用自动URL链接：如果您不希望自动链接URL，则可以通过将URL表示为带反引号的代码来删除该链接。  
![自动网址链接](https://i.hd-r.cn/762fbd370bc5cf1e7b4c6c51291cb488.png)  
`http://www.markdown.com.cn`

[^1]: This is the first footnote.
[^longnote]: This is the long footnote.

<span id="getCode"></span>
## 获取代码
本文使用Markdown编写，代码获取:
[Markdown教程.md](https://github.com/Attacking-Titan/Repo-note/blob/master/Markdown%E6%95%99%E7%A8%8B/Markdown%E6%95%99%E7%A8%8B.md)  
![Markdown教程](https://i.hd-r.cn/5278794687635c2af392a2ddd9252301.png)

