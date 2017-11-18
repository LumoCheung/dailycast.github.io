---
title: Markdown-常用语法
date: 2017-11-15 19:49:19
tags: markdown
---
本篇文章简要介绍常用的Markdown语法，方便快速查阅。

标题
=======

# 一级标题
	# 一级标题
## 二级标题
	## 二级标题
### 三级标题
	### 三级标题
#### 四级标题
	#### 四级标题
##### 五级标题
	##### 五级标题
###### 六级标题
	###### 六级标题

分隔线
----------
***
	`***实现分隔线`
---
	`---实现分隔线`
___
	`___实现分隔线`

表格
------------
| Title|Content|
|---|---
|项目1|实现项目1方案

	 | Title|Content|
	 |---|---
	 |项目1|实现项目1方案
文本
--------
#### 最普通的文本
普通文本，直接书写，没有任何特殊符号
#### 单行文本
	这是一行单行文本
实现方案:  
 在单行文本前面加一个Tab

#### 多行文本  
##### 实现方案1:
在每行文本前都加一个Tab 相当于多个单行文本

		这是多行文本的第一行
		这是多行文本的第二行
		这是多行文本的第三行
##### 实现方案2:  
使用三个反引号，这也是代码的使用方式

```java
反引号是 带有 ~ 符合的按键
String VIDEO = "video";
String TEXT = "text";
String PHOTO = "photo";
String HOME = "home";
```

换行
-------
按照惯例，使用回车来换行，但是在Markdown上行不通。换行实现有以下方式:

	1.两行直接空出一行。  
	2.前一行后面保留两个空格，第二行自动换行


斜体,粗体,删除线,下划线
-------
|语法|效果|
|---|---|
|`*斜体*`|*文字*|
|`_斜体_`|_文字_|
|`<u>下滑线</u>`|<u>文字</u>|
|`**加粗**`|**文字**|
|`__加粗__`|__文字__|
|`~~删除线~~`|~~文字~~|
|`***斜粗体***`|***文字***|
|`__斜粗体__`|__文字__|
|`***~~斜粗体删除线~~***`|***~~斜粗体删除线~~***|
|`~~**斜粗体删除线***~~`|***~~斜粗体删除线~~***|

高亮
-------
使用一对反引号即可  
	`高亮文字`,`高亮文字`
	
[高亮文字]()
	
	实现方案:
	[高亮文字]()
	
#### 超链接
[百度](https://www.baidu.com)

	实现方案:
	[百度](https://www.baidu.com)

引用图片
---------
![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")   
	
	实现方案:
	![alt](URL "title")
	alt 和 title 都可以省略
	
	![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")
	
![](https://www.google.co.jp/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)

emoji 表情
-----------
默认情况下Github 的Markdown 语法支持emoji表情
[emoji大全](https://www.webpagefx.com/tools/emoji-cheat-sheet/)
or
[emoji大全](https://github.com/gerenvip/README/blob/master/emoji.md)

简单举例:

比如`:blush:`，可以显示:blush:
