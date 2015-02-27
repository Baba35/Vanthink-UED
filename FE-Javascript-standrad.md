##html 开发规范
主要出于统一代码风格，提升开发效率，方便团队进行交流。

 + 推荐使用tab（四个空格）,文件统一编码为utf-8。
 
 + 每行代码结束加上分号。
 
 + 变量命名
 
```html
// 变量：必须采用骆驼峰的命名且首字母小写
var memberNum = 15;
var userName = 'jack';

// 常量：推荐采用全大写的命名，且单词以_分割，常量通常用于ajax请求url，和一些不会改变的数据
var MAX_NUM = 1000;
var FILE_SIZE = 120000;

// 类或组件：必须采用骆驼峰的命名且首字母大写

var BookStore = function(){
    ...
};
 
 
```
 
 + 代码空格的使用

```html
 
 
 
```
+ 避免产生歧义的布尔变量名称，例如： isNotError, isNotFound 为非法
 
 + 避免定义行数过多的函数，超过120行，不妨进行重构，定义为两个或者三个函数。
 


#### 一些常用的变量命名或缩写

```html 

	* e : event
	* el : element
	* pEl : parentElement,父节点对象
	* ex : exception
	* arr : array
	* o : object,对象
	* fun : function
	* hdl : handle,通常是事件函数
	* json : json对象
	* opts : options:由参数组成的json
	* coll : collection,集合或数组
	* ctx : context,上下文
	* ctn : container,容器
	* src : source/src,源头/src
	* w : width
	* h : height

```
 

 
### 参考
+ [google Javascript 编程规范指南](http://www.blogjava.net/brock/archive/2013/03/11/396284.html)
+ [Dojo Javascript 编码规范](http://blog.bingo929.com/dojo-javascript-style-guide.html) 
+ [前端编码规范之JavaScript](http://www.w3cfuns.com/article-5598404-1-1.html)


 