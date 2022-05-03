# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

**这是加粗的文字**
*这是倾斜的文字*
~~这是加删除线的文字~~
***这是斜体加粗的文字***


---
----
***
****


> 这是引用的内容
> > 这是引用的内容
> > > 这是引用的内容
> > >
> > > >>> 这是引用的内容

[百度](http://www.baidu.com '百度')  
[Markdown之语法入门篇](https://www.cnblogs.com/yuxiuyan/p/6044682.html)  
[Markdown基本语法](https://www.jianshu.com/p/191d1e21f7ed)  
[Markdown添加图片的三种方式](https://www.jianshu.com/p/280c6a6f2594)  
[Markdown语法之换行与段落](https://www.jianshu.com/p/1dc33c39da9e)  
[Markdown段首空格/段首缩进问题](https://blog.csdn.net/bat67/article/details/72858409)  
[Markdown文字居中](https://blog.csdn.net/chengyq116/article/details/82260934)  
[PHP图片转base64](https://www.runoob.com/w3cnote/php-image2base64.html)  


![blockchain](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=702257389,1274025419&fm=27&gp=0.jpg "区块链")  
![Alt text][pic1str]


- 无序列表-列表内容
+ 无序列表-列表内容
* 无序列表-列表内容


1. 有序列表-列表内容
2. 有序列表-列表内容
3. 有序列表-列表内容


- 一级无序列表
   + 二级无序列表
      * 三级无序列表
   
   
+ 一级无序列表
   1. 二级有序列表
   2. 二级有序列表
   
   
1. 一级有序列表
   1. 二级有序列表
      + 三级无序列表


| 姓名 | 技能 | 排行 |
| ---- | ---- | ---- |
| 刘备 | 哭   | 大哥 |
| 关羽 | 打   | 二哥 |
| 张飞 | 骂   | 三弟 |


| 姓名 | 技能 | 排行 |
| ---- | :--: | ---: |
| 刘备 |  哭  | 大哥 |
| 关羽 |  打  | 二哥 |
| 张飞 |  骂  | 三弟 |


#### **特殊字符需转义**
\\
\`
\*
\_
\{
\}
\[
\]
\(
\)
\#
\+
\-
\.
\!


`create database hero;`


```
<?php
//PHP图片转base64
$file = "u469.png";
if($fp = fopen($file,"rb", 0))
{
$gambar = fread($fp,filesize($file));
fclose($fp);
$base64 = chunk_split(base64_encode($gambar));
//输出
$encode = '<img src="data:image/jpg/png/gif;base64,' . $base64 .'" >';
echo $encode;
}
```


```mermaid
graph TD
A[模块A] -->|A1| B(模块B)
B --> C{判断条件C}
C -->|条件C1| D[模块D]
C -->|条件C2| E[模块E]
C -->|条件C3| F[模块F]
```

[pic1str]: 
data:image/png;base64,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