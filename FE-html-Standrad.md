##html 开发规范
主要出于统一代码风格，提升开发效率，方便团队进行交流。

 + 推荐使用tab（四个空格）。
 
 + 文档申明，统一为 &lt;!doctype html&gt; 
 
 + 编码统一为 &lt;meta charset=”utf-8″ /&gt; ,在CSS中使用  @charset utf-8; 来指定编码；
 
 + 推荐将css 文件放置在 &lt;head&gt; 标签内，将 JS文件放置底部 &lt;/body&gt; 前。
 
 + css 或者 js 文件用外链引入时去掉 type 属性
 ```html
 <link rel=”stylesheet” href=”…” />
 
 <script src=”…”></script>
 ```
 + 遵循xhtml标准，标签闭合(  &lt;br&gt; 推荐 &lt;br/&gt; )。
 + 用双引号进行属性赋值，所有标签属性均用双引号进行赋值，避免出现不统一的情况
 <pre>错误：
 &lt;input type="button" class=btn value='button' /&gt;
 </pre>
 + 给图片尽量加上 alt 属性，给 a 元素尽量加上 title 属性。
 
 + 所有元素必须正确嵌套，不允许交叉，不允许inline元素包含block元素，不允许类似在ul下出现除了li外的其它子元素等等
 
 + 不乱用标签，强调 [HTML的语义化](http://www.cnblogs.com/freeyiyi1993/p/3615179.html)。
 
 + 为模块加上注释.
 ```html
 <!-- list -->
 ....
 ...
 <!-- end lis-->
 ```
 
 ### html 模板
 
```html
<!doctype html>
<html lang="zh-cn">
<head>
    <meta charset="utf-8" />
    <title>网站项目名称-网站名称</title>
    <link href="*.css" rel="stylesheet" />
</head>
<body>
<div id="doc">
    <div id="hd">
        头部诸模块
    </div>
    <div id="bd">
        主体部分诸模块
    </div>
    <div id="ft">
        底部诸模块
    </div>
</div>
<script src="*.js"></script>
</body>
</html>

```
 
### 兼容性 html hack

```html
<!--[if lt IE 7 ]><html class="ie6" lang="zh-cn"><![endif]-->
<!--[if IE 7 ]><html class="ie7" lang="zh-cn"><![endif]-->
<!--[if IE 8 ]><html class="ie8" lang="zh-cn"><![endif]-->
<!--[if IE 9 ]><html class="ie9" lang="zh-cn"><![endif]-->
<!--[if (gt IE 9)|!(IE)]><!--><html class="" lang="zh-cn"><!--<![endif]-->

```
 

 
### 代码有效性验证: 
 > http://validator.w3.org/#validate_by_input 
 
 > http://jigsaw.w3.org/css-validator/#validate_by_input
 