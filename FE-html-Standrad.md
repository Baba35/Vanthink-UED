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
 
 + 不乱用标签，强调 [HTML的语义化](http://www.cnblogs.com/freeyiyi1993/p/3615179.html)。
 
 
 
 
 
 
 代码有效性验证: 
 > http://validator.w3.org/#validate_by_input 
 
 > http://jigsaw.w3.org/css-validator/#validate_by_input
 