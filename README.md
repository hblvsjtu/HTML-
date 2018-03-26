# HTML_Study

  HTML，Hypertext Makeup Language超文本标记语言。其实当初在学javascript权威指南第二部分的时候，就觉得应该补一下html和css权威指南方面的知识，才能更好地进行第二部分的学习^_ ^

## 一、	初探HTML
### 1.1	元素格式
#### 1)	其实HTML其实HTML的职责应该被限定于说明文档内容的结构和含义，而并非内容呈现的形式，内容呈现形式的责任应该由CSS承担。
  
>>>>>>![图1-1 元素格式](https://github.com/hblvsjtu/HTML_Study/blob/5f7ba08d23b8f4de45599032c5b7445e4de8da87/picture/%E5%9B%BE1-1%20%E5%85%83%E7%B4%A0%E6%A0%BC%E5%BC%8F.png?raw=true)  
>>>>>> 图1-1 元素格式

#### 2)	空元素
>>> 空元素的表示内容为空的标签，如`<code></code>`；  
>>> 或者你可以使用自闭合的标签，如`<code/>`,直接在第一个标签的最后加上“/”；  

#### 3)	虚元素
>>> 本身规定就不允许带有内容的元素，如`<hr>`,是一种段落组织元素，一条长横线，不过更倾向于类似空元素的写法，在末尾加上一个“/”，形如`<hr/>`  

			I like apples; <hr/> I like pears;


