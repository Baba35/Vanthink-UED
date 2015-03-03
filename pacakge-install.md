##部分软件包安装教程

### php+apache

推荐安装继承包：
+ wamp,Windows下的Apache+Mysql/MariaDB+Perl/PHP/Python，一组常用来搭建动态网站或者服务器的开源软件


云盘地址 http://yunpan.cn/cJGFjVVNpfask （提取码：f47e）


###yaf安装

* Yaf只支持PHP5.2及以上的版本. 并支持最新的PHP5.3.3 

* Yaf需要SPL的支持. SPL在PHP5中是默认启用的扩展模块 

* Yaf需要PCRE的支持. PCRE在PHP5中是默认启用的扩展模块 

#### Linux下安装
下载Yaf的最新版本, 解压缩以后, 进入Yaf的源码目录, 依次执行(其中PHP_BIN是PHP的bin目录):

```html
$PHP_BIN/phpize
./configure --with-php-config=$PHP_BIN/php-config
make
make install
```

然后在php.ini中载入yaf.so, 重启PHP.


#### windows下安装
1.首先去下载windows下面的编译好的dll [yaf.dll] 版本选择： http://code.google.com/p/yafphp/downloads/list

如何选择那个版本的dll尼? 嘿嘿,这个时候,就要用到我们的 phpinfo()看一下你的php版本是多少[默认首页里面有个phpinfo的链接]。如果你的php版本的是php 5.3.13 所以我选择是php_yaf-2.1.9-x86-5.3.13-zts-nodebug.dll ，那么有两个5.3.13版本的dll我们又该选择那个，还是得看phpinfo() 如果 Thread Safety enabled 项为 enabled 的话就选择 zts 版本，反之应该就是 nts 了.还有就是记住你的cpu是x86还是x64

2.然后就是找到wamp安装目录比如F:/wamp/bin/php/php5.3.13/ext/ (根据你自己系统路径)目录下把刚才下载的 php_yaf-2.1.9-x86-5.3.13-zts-nodebug.dll复制重命名为 yaf.dll。然后打开php.ini 加上 extension=yaf.dll 重启一下服务.就可以了

3.需要注意: 不管是在linux还是在win下,有时候步骤都对了,但是phpinfo还是没有出现的时候,你要检查一下你是用的是那个 php.ini 文件,你可以在页面搜索一下.然后顺便看看 extension_dir 指向的目录是那个.Loaded Configuration File 看看他指向的是那个php.ini 就修改那个php.ini

如何开启 Yaf 的命名空间功能，文档里默认是关闭的
yaf.use_namespace 0  PHP_INI_SYSTEM 开启的情况下, Yaf将会使用命名空间方式注册自己的类, 比如Yaf_Application将会变成Yaf\Application
所以如果我们要用命名空间，那么就修改一下php.ini就可以
添加
```1html
[yaf]
yaf.use_namespace = 1
```
重启一下php 服务就可以了。
ok,至此,yaf安装完成,是不是很简单.

yaf-for-wamp2.5 云盘地址 http://yunpan.cn/cJGxAM7TVBYqf （提取码：ff43）



### redis安装与开启


####windows下安装

下载地址https://github.com/dmajkic/redis/downloads。下载到的Redis支持32bit和64bit。根据自己实际情况选择，我选择32bit。把32bit文件内容拷贝到需要安装的目录下,比如：D:\dev\redis-2.4.5。

打开一个cmd窗口，使用cd命令切换到指定目录（D:\dev\redis-2.4.5）运行 redis-server.exe redis.conf 。运行以后出现如下界面。
<img src="http://images.cnitblog.com/blog/270324/201305/27152838-1d64c3178a504a1dab2c48e270703104.png"/>

这就说明Redis服务端已经安装成功。

重新打开一个cmd窗口，使用cd命令切换到指定目录（D:\dev\redis-2.4.5）运行 redis-cli.exe -h 127.0.0.1 -p 6379，其中 127.0.0.1是本地ip，6379是redis服务端的默认端口。运行成功如下图所示。

<img src="http://images.cnitblog.com/blog/270324/201305/27152846-f394a6eb01ad41ba92989d571f34d211.png"/>

这样，Redis windows环境下搭建已经完成，是不是很简单。
更多参考 http://www.cnblogs.com/linjiqin/archive/2013/05/27/3101694.html

云盘地址：http://yunpan.cn/cJGuIBpfwMKQu （提取码：6601） 

##### php开启扩展

1. 下载windows 版本php对应的php扩展。php_redis.dll 。注意版本号的选择 。Thread Safety enabled 项为 enabled 的话就选择 zts 版  下载地址： https://github.com/phpredis/phpredis/downloads 

2.将下载的php_redis.dll 复制到php的扩展目录下比如wamp的安装路径比如 F:/wamp/bin/php/php5.3.13/ext/

3.修改php的配置文件，加载php_redis.dll ：extension=php_redis.dll

4.重启Apache 。打开phpinfo页面。就可以看到已经加载php_redis了。这时候就可以使用redis  了。

#### 开启igpbinary扩展
1. 和上面一样需要下载dll ,选择对应的版本就ok啦，http://pecl.php.net/package/igbinary
2. 将下载的dll文件复制到 复制到php的扩展目录下比如wamp的安装路径比如 F:/wamp/bin/php/php5.3.13/ext/ 重命名 php_igpinary.dll
3.在php配置文件 php.ini写入 ：extension=php_ipgbinary.dll
4.重启ok,

集合包云盘地址(redis+ipgbinay) http://yunpan.cn/cJGracRFGbEfE （提取码：6b8f）



### laraval安装

参考 http://www.golaravel.com/laravel/docs/4.2/















