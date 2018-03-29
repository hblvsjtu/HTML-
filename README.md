# HTML_Study  
  
  
### 作者：冰红茶  
### 参考书籍：《HTML5权威指南》
------  

  HTML，Hypertext Makeup Language超文本标记语言。其实当初在学javascript权威指南第二部分的时候，就觉得应该补一下html和css权威指南方面的知识，才能更好地进行第二部分的学习^_ ^
  
## 目录

## [一、初探HTML](#1)
### [1.1 元素](#1.1)
### [1.2 创建HTML文档](#1.2) 
### [1.3 HTML5元素背景知识](#1.3)
## [二、构建HTML元素](#2)
### [2.1 元数据——文档结构元素](#2.1)
### [2.2 短语元素——标记文字](#2.2) 
### [2.3 流元素——组织内容](#2.3)
### [2.4 流元素——文档分节](#2.4)
## [三、表格元素](#3)
### [3.1 表格元素](#3.1)
### [3.2 制作不规则表格](#3.2)
## [四、表单元素](#4)
### [4.1 表格元素](#4.1)
### [4.2 配置表单](#4.2)
### [4.3 input元素和fieldset元素和button元素](#4.3)
------  

    
<h2 id='1'> 一、初探HTML </h2>
<h3 id='1.1'> 1.1元素</h3>  

#### 1) 元素格式  
>> 其实HTML其实HTML的职责应该被限定于说明文档内容的结构和含义，而并非内容呈现的形式，内容呈现形式的责任应该由CSS承担。  
>>>>>> ![图1-1 元素格式](https://github.com/hblvsjtu/HTML_Study/blob/5f7ba08d23b8f4de45599032c5b7445e4de8da87/picture/%E5%9B%BE1-1%20%E5%85%83%E7%B4%A0%E6%A0%BC%E5%BC%8F.png?raw=true)   

#### 2)	空元素
>> 空元素的表示内容为空的标签，如`<code></code>`；  
>> 或者你可以使用自闭合的标签，如`<code/>`,直接在第一个标签的最后加上“/”；  

#### 3)	虚元素
>> 本身规定就不允许带有内容的元素，如`<hr>`,是一种段落组织元素，一条长横线，不过更倾向于类似空元素的写法，在末尾加上一个“/”，形如`<hr/>`  

			I like apples; <hr/> I like pears;
			
#### 4) 元素属性
- 属性只能用于开始标签或者单个标签；
- 属性又分为全局属性和局部属性；
>>>>>> ![图1-2 元素属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/%E5%9B%BE1-2%20%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png?raw=true) 
- 布尔属性
>> 其属性值为空字符串==属性名字符串；或者直接赋予“true”或者“false”；
- 自定义属性
>> 用户自己定义的，以`data-`打头的,添加这样的前缀是为了避免与未来版本可能增加的属性名称冲突；可以跟CSS和JS结合起来；

#### 5) 元素的分类
- 父元素
- 子元素 关系最近的后代元素
- 后代元素
- 兄弟元素

#### 6) 元素的类型
- 元数据类型 构建html文档的基本结构，以及就如何处理文档向浏览器提供信息和指示；
- 流元素 流元素是短语元素的超集 ？不明所以
- 短语元素 ？不明所以
- 其他元素，如`<li>` ？不明所以


<h3 id='1.2'>1.2 创建HTML文档</h3>  

#### 1) 用户代理user agent
>> 用于处理HTML文档的软件有一个共同的软件——用户代理user agent，浏览器是最流行的用户代理，但不是唯一的一种；

#### 2) 外层结构
>> 外层结构由两个元素决定: DOCTYPE和html;  

			<!DOCTYPE HTML>
				<html>
					<!-- type your text -->
				</html>

#### 3) 元数据
>> 放在`<head>内容</head>`中间的内容；

#### 4) HTML实体
>> 特殊字符的编码，避免该特殊字符被当作HTML元素处理，而当作普通显示字符处理；
>>>>>> ![图1-3 常用HTML实体](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/%E5%9B%BE1-2%20%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png?raw=true) 

#### 5) 全局属性
- accesskey 快捷键 在Windows系统上是“Alt” + accesskey的值；
- class 给元素归类用的；
- contenteditable 赋予用户可修改的文字的权限，它的值是一个布尔值，“true”或者“false”；
- contextmenu 用来为元素设置快捷菜单，即右键会弹出菜单，然而，暂时还没有支持该特性的浏览器；
- dir 文字向左靠边还是向右靠边，“ltr” | “rtl”；
- draggable 表示元素是否可被拖放；
- dropzone 与draggable搭配使用；
- hidden 是否隐藏该元素，可以直接使用，后面不加值，或者说他本身就是键值同体；
- id 元素的唯一标识符，在CSS中是用“#”+id作为分类器。还可以利用id值导肮到文档中的特定位置，如URL=文档名+“#”+id，“#”+id称为URL的片段标识符；
- lang 语言选项，“en”“fr”“es”;
- spellcheck 拼写检查，只有在哪些用户可编辑的元素上才有意义，如：`<textarea>`它的值是一个布尔值，“true”或者“false”。不过有一个问题是，该属性会忽略之前的lang属性，原因是spellcheck属性基于用户操作系统或浏览器的语言设置;
- style 直接定义CSS样式用的；
- tabindex 键盘焦点的切换，一般用“tab”键，键值为1的会被首先选中，-1的不会被选中；
- title 提供元素的额外信息，一般是一些提示，即你用光标移过去之后会出现提示；  


<h3 id='1.3'> 1.3 HTML5元素背景知识 </h3> 

#### 1) 语义与呈现分离  
#### 2) 元素选用原则  
>> 这里说的很含糊，其实并没有什么具体的可操作选用原则；  
------  

<h2 id='2'> 二、构建HTML文档 </h2>  
<h3 id='2.1'> 2.1 元数据——文档结构元素</h3>   

>>>>>> ![图2-1 文档和元数据元素](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.1%20%E6%9E%84%E7%AD%91%E5%9F%BA%E6%9C%AC%E7%9A%84%E6%96%87%E6%A1%A3%E7%BB%93%E6%9E%84.png?raw=true)  

>> 元素|元素类型|内容|元素结束方式|是否HTML5新增
>> -|-|-|-|-
>> DOCTYPE|无|无|单个开始标签|否
>> html|无|head元素和body元素|开始标签和结束标签|否
>> head|无|必须有title元素|开始标签和结束标签|否
>> body|无|所有流元素和短语元素|开始标签和结束标签|否
>> title|元数据|普通说明文字|开始标签和结束标签|否
>> base|元数据|无|虚元素|否
>> style|无|CSS样式|开始标签和结束标签|否
>> link|元数据|无|虚元素|否
>> script|元数据/短语|脚本语言|必须使用开始标签和结束标签|否
>> noscript|元数据/短语/流|短语元素/流元素|必须使用开始标签和结束标签|否
>> title|元数据|普通说明文字|开始标签和结束标签|否
>> title|元数据|普通说明文字|开始标签和结束标签|否

#### 1) DOCTYPE元素  
>> 他告诉浏览器两件事：它处理的是HTML文档；用来标记文档内容HTML所属的版本；  
#### 2) html元素 开始标签和结束标签    
>> 有一个更加恰当的名字*根元素*；  
#### 3) head元素 开始标签和结束标签    
>> 包含着文档的元数据和文档信息，元数据向浏览器提供有关文档内容和标记的信息，还包括CSS和JS的文档的引用；
- title 标签页名字
- base 虚元素的形式，有两个属性
> - href 基准地址，如  	
> - target 告诉浏览器如何打开URL
- meta 虚元素的形式  
> - name 使用“name”和“content”作为键值对；  
> - content；  
> - charset 声明字符编码
> - http-equiv 模拟HTTP标头字段，字段值由content表示  

>>>>>> ![2.2 meta元素http-equiv属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.2%20meta%E5%85%83%E7%B4%A0http-equiv%E5%B1%9E%E6%80%A7.png?raw=true)  

- style 开始标签和结束标签  
> - text 定义CSS样式
> - scoped html5新增的，可以设置属性scoped已规定作用域，如果不设置的话就作用于整个文档
> - media 规定设备值,可以  采用“AND”“NOT”和表示“OR”的逗号表示  
>>>>>> ![2.3 style元素media属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.3%20style%E5%85%83%E7%B4%A0media%E5%B1%9E%E6%80%A7.png?raw=true)  

>>>>>> ![2.4 style元素media属性规定的设备值](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.4%20style%E5%85%83%E7%B4%A0media%E5%B1%9E%E6%80%A7%E8%A7%84%E5%AE%9A%E7%9A%84%E8%AE%BE%E5%A4%87%E5%80%BC.png?raw=true)  

- link 开始标签和结束标签   
> - 虚元素的形式，指定外部资源，在HTML5中新增“size”的属性，去掉“charset”“rev”“target”的属性；
> - rel的值除了我们常见的“stylesheet”载入CSS文档，还有“icon”，表示为网站载入图标,还有预获取功能“prefetch”； 
> - type的值可以是“text/css”，还可以是“image/x-icon”
> - 预获取功能“prefetch”,在用户点击某链接进入某个页面的前就已经进行预先加载。  
>>>>>> ![2.5 link元素属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.5%20link%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png?raw=true)  

		<!DOCTYPE html>
		<html>
			<head>
				<title>欢迎页面</title>
				<base href="http://"/>
				<meta name="author" content="LvHongbin"/>
				<meta name="description" content="A simple example"/>
				<meta charset="utf-8"/>
				<meta http-equiv="refresh" content="5"/>
				<style type="text/css" scoped="">>
					a{
						background-color: grey;
						color: white;
						padding: 0.5em;
					}
				</style>
			</head>
			<body>
				<a href="www.baidu.com">登陆页面</a> 
			</body>
		</html>  

- script  开始标签和结束标签，用于定义脚本并控制其执行方式，具有的属性包括；
> - type 不使用该属性的时候，默认是js类型
> - src 载入外部文件，设置了该属性的script元素只能是空白元素，不能既有src属性，又有内嵌内容。*另外，如果是引用外部的文件，则必须使用结束标签，不能采用自闭合标签，否则浏览器会忽略该外部文件的加载*；
> - defer 一般来讲，浏览器是按顺序解析html文本和JS文档，但是有时候需要将JS文档放在最后执行，此时除了将该JS脚本放在html文档的末尾之外，还有一种方法，就是使用defer，该属性没有值，直接放进去就可以了。需要注意的是，该属性只能用于外部JS文档的引用，如果使用内嵌式的JS脚本则不起作用；
> - async 异步执行脚本，该属性没有值，直接放进去就可以了
> - charset 
- noscript 
>> 假如用户的浏览器不支持JS或者用户选择禁用JS的功能是，使用noscript给用户显示一些简短信息；  


<h3 id='2.2'> 2.2 短语元素——标记文字</h3>  

>> >> 一个主要特点是元素内容是短语元素，组织形式是行内；
>>>>>> ![2.6 文本元素1](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.6%20%E6%96%87%E6%9C%AC%E5%85%83%E7%B4%A01.png?raw=true)  
>>>>>> ![2.6 文本元素2](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.6%20%E6%96%87%E6%9C%AC%E5%85%83%E7%B4%A02.png?raw=true)  

>> 元素|元素类型|内容|元素结束方式|是否HTML5新增
>> -|-|-|-|-
>> a|短语/流|短语内容/流内容|开始标签和结束标签|否
>> b|短语|短语内容|开始标签和结束标签|否
>> em|短语|短语内容|开始标签和结束标签|否
>> i|短语|短语内容|开始标签和结束标签|否
>> s|短语|短语内容|开始标签和结束标签|否
>> strong|短语|短语内容|开始标签和结束标签|否
>> small|短语|短语内容|开始标签和结束标签|否
>> sup|短语|短语内容|开始标签和结束标签|否
>> sub|短语|短语内容|开始标签和结束标签|否
>> br|短语|无|虚元素|否
>> wbr|短语|无|虚元素|是
>> code|短语|短语内容|开始标签和结束标签|否
>> var|短语|短语内容|开始标签和结束标签|否
>> samp|短语|短语内容|开始标签和结束标签|否
>> kbd|短语|短语内容|开始标签和结束标签|否
>> abbr|短语|短语内容|开始标签和结束标签|否
>> dfn|短语|短语内容|开始标签和结束标签|否
>> q|短语|短语内容|开始标签和结束标签|否
>> ruby|短语|短语内容/rt/rp|开始标签和结束标签|是
>> bdo|短语|短语内容|开始标签和结束标签|否
>> bdi|短语|短语内容|开始标签和结束标签|是
>> span|短语|短语内容|开始标签和结束标签|否
>> mark|短语|短语内容|开始标签和结束标签|是
>> ins|短语/流|短语内容/流内容|开始标签和结束标签|否
>> del|短语/流|短语内容/流内容|开始标签和结束标签|否
>> time|短语|短语内容|开始标签和结束标签|是

#### 1) 超链接a 开始标签和结束标签    
>> href 指向外部的超链接；  
>> href 指向内部的超链接，herf="# + id名称"，如果找不到这样的id，那么浏览器会尝试寻找name值等于该id值的元素；  
>> target 设定浏览环境，其实就是决定新窗口在哪里打开的问题  
>>>>>> ![2.7 a元素的target属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.7%20a%E5%85%83%E7%B4%A0%E7%9A%84target%E5%B1%9E%E6%80%A7.png?raw=true)  

#### 2) 用于设置文字格式的元素
> - b元素 开始标签和结束标签，用于内容加粗；    
> - em元素 开始标签和结束标签，用于内容强调，感觉就是做一个斜体；    
> - i元素 开始标签和结束标签，用于外文词语或者科技术语；  
> - s元素 开始标签和结束标签，用于不正确或者纠正，其实就是加一个删除线；  
> - strong元素 开始标签和结束标签，用于一段重要的文字，其实就是把字体放大一号；  
> - u元素 开始标签和结束标签，用于加下划线；  
> - small元素 开始标签和结束标签，用于小一号字；  
> - sup元素和sub 开始标签和结束标签，用于上标和下标；
#### 3) 换行
> - br元素 虚元素，用于强制换行；  
> - wbr元素 虚元素，当一行装不下那么多的文字的时候自动换行；  
#### 4) 输入和输出
>> 包括code,car,samp,kbd，不过基本上用不到；  
#### 5) 标题引用，引文，定义和缩写
>> 基本上用不到； 
#### 6) 使用语言元素
> - ruby,rt和rp，HTML5新增的，开始标签和结束标签，这个还有些用，主要用来注音的，即在文字的上方加拼音；
> - bdo 开始标签和结束标签，文字阅读的方向，跟dir属性一起使用；  
> - bdi HTML5新增的，开始标签和结束标签，保证文字方向
#### 7) 其他文本元素
> - span元素 开始标签和结束标签，内容是短语元素，本身并没有什么特别的含义，它可以把一些全局属性用到一段内容上；
> - mark元素 HTML5新增的，开始标签和结束标签，把文字变成黄底黑字；
> - del/ins元素 开始标签和结束标签，删除或者添加；
> - time元素 HTML5新增的，开始标签和结束标签，其实并不是很懂这个元素的用法；  


<h3 id='2.3'> 2.3 流元素——组织内容</h3>

>> 一个主要特点是内容元素是流，组织形式是块；
>>>>>> ![2.8 内容分组元素](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.8%20%E5%86%85%E5%AE%B9%E5%88%86%E7%BB%84%E5%85%83%E7%B4%A0.png?raw=true)  

>> 元素|元素类型|内容|元素结束方式|是否HTML5新增
>> -|-|-|-|-
>> p|流|短语内容|开始标签和结束标签|否
>> div|流|流内容|开始标签和结束标签|否
>> pre|流|短语内容|开始标签和结束标签|否
>> blockquote|流|流内容|开始标签和结束标签|否
>> hr|流|无|虚元素|否
>> ol|流|li元素|开始标签和结束标签|否
>> ul|流|li元素|开始标签和结束标签|否
>> li|无|流内容|开始标签和结束标签|否
>> dl dt dd|||开始标签和结束标签|否
>> figure|流|流内容,figcaption元素|开始标签和结束标签|是
>> figcaption|无|流内容|开始标签和结束标签|是

#### 1) 建立段落p
> - p元素 开始标签和结束标签
#### 2) 万能div
> - div元素 开始标签和结束标签，相当于文本元素的span元素，知识div元素应用于块形式；
> - 万不得已的时候不要使用div元素，因为它是万金油，如果有其他更加具体的元素应首先使用他们，这也会是选用元素的原则；
#### 3) 预先编排好的pre
> - pre元素 开始标签和结束标签，阻止浏览器合并连续空格，保留文本的源格式；
> - 尤其是与code元素搭配起来使用时特别有用；
#### 4) figure和figcaption
> - HTML5是这样定义figure：一个独立的内容单元，可带标题。通常作为一个整体被文档的主体引用，把它从文档主体中删除也不会影响文档的意思；
> - figcaption定义插图figure的标题；  


<h3 id='2.4'> 2.4 流元素——文档分节</h3>

>> 主要用于为不同的主题分节，是html5的一大特色
>>>>>> ![2.8 文档分节元素](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/2.9%20%E6%96%87%E6%A1%A3%E5%88%86%E8%8A%82%E5%85%83%E7%B4%A0.png?raw=true)  

>> 元素|元素类型|内容|元素结束方式|是否HTML5新增
>> -|-|-|-|-
>> h1~h6|流|流内容|开始标签和结束标签|否
>> hgroup|流|h1~h6|开始标签和结束标签|是
>> section|流|style元素/流内容|开始标签和结束标签|是
>> header|流|流内容|开始标签和结束标签|是
>> footer|流|流内容|开始标签和结束标签|是
>> nav|流|流内容|开始标签和结束标签|是
>> article|流|流内容|开始标签和结束标签|是
>> aside|流|流内容|开始标签和结束标签|是
>> address|流|流内容|开始标签和结束标签|是
>> header|流|流内容|开始标签和结束标签|是
>> details|流|流内容/可有可无的summary元素|开始标签和结束标签|是
>> summary|无|短语内容|开始标签和结束标签|是


#### 1) 隐藏子标题 hgroup
> - hgroup元素 开始标签和结束标签，子元素只有h1~h6，用于把不同的标题组成一个整体，以免影响html文档的大纲；
#### 2) 生成节 section
> - section元素 开始标签和结束标签，不能是address元素的后代元素；
> - 通常包含多个段落和一个标题，但是标题并不是必需的；
> - 包括Chrome和Firefox在内的一些浏览器对于section，article，aside和nav元素中的h1应用的样式有所不同；
> - 作为对比，Opera和Safari对于内嵌在section中的同种标题元素应用相同的样式；
#### 3) 提供联系信息 address
> - address元素 开始标签和结束标签，如果作为article的后代元素，则视为为article提供联系信息；
> - 如果是作为body元素的后代，则视为为整个文档提供联系信息；
> - 只能作为body元素或者article元素的后代；  
  
------   
  
    
<h2 id='3'> 三、 表格元素</h2>
<h3 id='3.1'> 3.1 表格元素</h3>  

>> 在HTML早期的版本中，用表格控制页面内容布局的现象很常见，但HTML5不再允许这样做，取而代之的是CSS的新特性；
>>>>>> ![3.1 表格元素](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/3.1%20%E8%A1%A8%E6%A0%BC%E5%85%83%E7%B4%A0.png?raw=true)  

>> 元素|元素类型|内容|元素结束方式|是否HTML5新增
>> -|-|-|-|-
>> table|流|caption colgroup thead tbody tfoot tr th td|开始标签和结束标签|否
>> tr|无|td th|开始标签和结束标签|否
>> td|无|流内容|开始标签和结束标签|否
>> thead|无|tr|开始标签和结束标签|否
>> tfoot|无|tr|开始标签和结束标签|否
>> tbody|无|tr|开始标签和结束标签|否
>> caption|无|流内容|开始标签和结束标签|否
>> colgroup|无|col *只有没有设定span属性的时候才能使用*|开始标签和结束标签|否
>> col|无|流内容|虚元素|否

#### 1) th元素 
> - th元素 其父元素为tr，用于表示第一行的内容（表头）；
#### 2) 表格的格式化
> - 那问题来了，为什么需要表格格式化？我们知道，一般来讲第一行的单元格全都是表头th，下面的每一行的第一个单元格为th，那么使用CSS的时候要区分第一行中的全th和其余行的一个th比较麻烦，而且有时候其余行不仅只有一个th，这时候每次都需要更改CSS就比较麻烦。这时候表格的结构化应运而生；
> - thead元素，其父元素是table元素，子元素是tr元素，表示表格的第一行；
> - tfoot元素，其父元素是table元素，子元素是tr元素，表示表格的最后一行；
> - tbody元素，其父元素是table元素，子元素是tr元素，表示表格除了第一行和最后一行的其余行；  

<h3 id='3.2'> 3.2 制作不规则的表格</h3>   

#### 1) 制作不规则的表格
> - colspan属性 合并多列，合并后的那些单元格被删除，只剩第一个；
> - rowspan属性 合并多行，合并后的那些单元格被删除，只剩第一个；
#### 2) colgroup元素
> - 主要用来方便对列进行分组处理；
> - 属性span表示要处理那几列，比如span="2"，表示处理前面两列，如果再来一个colgroup元素，它的属性是span="3"，则表示处理第3~5列；
> - 可以用col元素的span属性让一个col元素代表几列，不用span属性的col属性只代表一列；
#### 3) 设置表格边框
> - border属性，大多数浏览器止呕见到border属性之后才会在表格和每个单元格周围绘出边框；
> - border属性的值必须设置为1或者空字符串；  

------   
  
    
<h2 id='4'> 四、 表单元素</h2>
<h3 id='4.1'> 4.1 表单元素</h3>  

>> 在HTML早期的版本中，用表格控制页面内容布局的现象很常见，但HTML5不再允许这样做，取而代之的是CSS的新特性；
>>>>>> ![4.1 表单元素a](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/4.1%20%E8%A1%A8%E5%8D%95%E5%85%83%E7%B4%A0a.png?raw=true)  
>>>>>> ![4.1 表单元素b](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/4.1%20%E8%A1%A8%E5%8D%95%E5%85%83%E7%B4%A0b.png?raw=true)

>> 元素|元素类型|内容|元素结束方式|是否HTML5新增
>> -|-|-|-|-
>> form|流|主要是label元素和input元素|开始标签和结束标签|否
>> input|短语|无|虚元素|否
>> button|无|流内容|开始标签和结束标签|否
>> label|短语|短语内容|开始标签和结束标签|否
>> fieldset|流|流内容|开始标签和结束标签|否
  
  
<h3 id='4.2'> 4.2 配置表单</h3>  

#### 1) 配置表单
> - action属性 把用户的数据发送到什么地方，一般是一个网页地址；
> - method属性 允许的值只有get和post两个。get：用于安全交互safe interaction，同一个请求发起任意多次不会产生额外作用，一般用于请求只读信息，而post请求则用于不安全的请求，提交数据的行为会导致一些状态的改变，对于Web应用程序多半采用这种方式。
> - enctype属性 指定了浏览器对发送给服务器的数据采用的编码方式，第一种方式是默认的，其中的特殊字符已经替换成相应的HTML实体，数据项的名称和值以等号分开，各组数据间以符号&分开；第三种方式每家浏览器都有自己的处理方案，结果难以预料，所以最好不要采用。
>>>>>> ![4.2 配置数据编码](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/4.2%20%E9%85%8D%E7%BD%AE%E6%95%B0%E6%8D%AE%E7%BC%96%E7%A0%81.png?raw=true)  

> - autocomplete属性，帮助用户记住输入表单的数据，并在再次遇到类似的表单的时候可以自动填写，它有两个值，on和off；
> - target属性
> - name属性，form的name属性只用于DOM中，并不会发送给服务器，而input的name属性如果不设置的话，数据在提交表单的时候不会被发送给服务器，所以input元素的name属性和id属性最好是同一个值。
> - 以前的HTML4中input和button元素必须放在form元素里面，但是在HTML5中input和button元素可以放在外面，使用form属性将与特定的表单关联在一起。

#### 2) 在表单中添加说明标签
> - for属性，将for属性的值跟其后input的id值相等，这样可以帮助把该标签跟input元素关联起来，有利于屏幕阅读器和其他残障辅助技术对表单的处理。这里有两种方式，可以如  独立分开，也可以把input元素写在label元素里面  

	<label for="input1">input1</label><input id="input1" name="input1" type="text"/>  
	或者   
	<label for="input1">input1 <input id="input1"  name="input1" type="text"/></label>  
    
<h3 id='4.3'> 4.3 input元素和fieldset元素和button元素</h3>  

#### 1) input元素
> - autofocus属性，鼠标光标的聚焦，只有键没有值，一旦出现说明已经开启该功能；
> - disable属性，禁用，只有键没有值，一旦出现说明已经开启该功能；
#### 2) fieldset元素
> - 其实就是给表单分组；
> - 他也有对应的标签————legend元素；
>>>>>> ![4.2 配置数据编码](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/4.3%20fieldset%E5%92%8Clegend%E5%85%83%E7%B4%A0.png?raw=true)    

#### 3) button元素
> - type属性，有三个值：submit，reset（将所有的input元素重置）和button（把button当一般元素使用，按下它不会做任何事情，但可以执行JS脚本）；
> - 如果type属性为submit，那么该按钮会多出几个值，该值其实就是将原先属性form的属性搬到button来，不过他们都是在HTML5中新增的属性；
>>>>>> ![4.3 button元素新增的属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/4.4%20button%E5%85%83%E7%B4%A0%E7%9A%84%E5%B1%9E%E6%80%A7.png?raw=true)  






























