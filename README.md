# HTML_Study

  HTML，Hypertext Makeup Language超文本标记语言。其实当初在学javascript权威指南第二部分的时候，就觉得应该补一下html和css权威指南方面的知识，才能更好地进行第二部分的学习^_ ^

## 一、	初探HTML
### 1.1	元素
#### 1) 元素格式
>>> 其实HTML其实HTML的职责应该被限定于说明文档内容的结构和含义，而并非内容呈现的形式，内容呈现形式的责任应该由CSS承担。
  
>>>>>>![图1-1 元素格式](https://github.com/hblvsjtu/HTML_Study/blob/5f7ba08d23b8f4de45599032c5b7445e4de8da87/picture/%E5%9B%BE1-1%20%E5%85%83%E7%B4%A0%E6%A0%BC%E5%BC%8F.png?raw=true)  

#### 2)	空元素
>>> 空元素的表示内容为空的标签，如`<code></code>`；  
>>> 或者你可以使用自闭合的标签，如`<code/>`,直接在第一个标签的最后加上“/”；  

#### 3)	虚元素
>>> 本身规定就不允许带有内容的元素，如`<hr>`,是一种段落组织元素，一条长横线，不过更倾向于类似空元素的写法，在末尾加上一个“/”，形如`<hr/>`  

			I like apples; <hr/> I like pears;
			
#### 4) 元素属性
- 属性只能用于开始标签或者单个标签；
- 属性又分为全局属性和局部属性；
>>>>>>![图1-2 元素属性](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/%E5%9B%BE1-2%20%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png?raw=true) 
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

### 1.2 创建HTML文档
#### 1) 用户代理user agent
>>> 用于处理HTML文档的软件有一个共同的软件——用户代理user agent，浏览器是最流行的用户代理，但不是唯一的一种；

#### 2) 外层结构
>>> 外层结构由两个元素决定: DOCTYPE和html;  

			<!DOCTYPE HTML>
				<html>
					<!-- type your text -->
				</html>

#### 3) 元数据
>>> 放在`<head>内容</head>`中间的内容；

#### 4) HTML实体
>>> 特殊字符的编码，避免该特殊字符被当作HTML元素处理，而当作普通显示字符处理；
>>>>>>![图1-3 常用HTML实体](https://github.com/hblvsjtu/HTML_Study/blob/master/picture/%E5%9B%BE1-2%20%E5%85%83%E7%B4%A0%E5%B1%9E%E6%80%A7.png?raw=true) 

#### 5) 全局属性
- accesskey 快捷键 在Windows系统上是“Alt” + accesskey的值；
- class 给元素归类用的；
- contenteditable 赋予用户可修改的文字的权限，它的值是一个布尔值，“true”或者“false”；
- contextmenu 用来为元素设置快捷菜单，即右键会弹出菜单，然而，暂时还没有支持该特性的浏览器；
- dir 文字向左靠边还是向右靠边，“ltr” | “rtl”；
- draggable 表示元素是否可被拖放；
- dropzone 与draggable搭配使用；
- hidden 是否隐藏该元素；



