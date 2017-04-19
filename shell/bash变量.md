#bash变量	
*2017-4-17*
####bash变量的功能
						
>1. 不管是PHP ，还是JAVA ，它是用来编写应用程序的，或是网站； JAVA主要是实现服务端程序。
而shel编程，它是一个脚本语言（所见即所得）。它不需要执行编译过程之后再执行；它是编译过程放在执行过程中，所以，执行起来要慢得多，
2. SHELL，主要是帮助管理员，简化管理操作。
比如，批量增加用户，定时备份脚本，批量记录什么LOG.....
####什么是变量与变量分类
>变量命名规则：
	>>在任何系统中，目录名、文件名、变量名都要有含义
	注意：Linux中默认变量类型都是字符串类型，不含有其他类型，所以对数字计算时，要用特殊方法将字符串转变为数字才能计算。
	
>Shell中变量的分类
  >
	·用户自定义变量
	·环境变量
	·位置参数变量
	·预定义变量
>*注*
>>在shell中，所有变量的默认类型都是字符串型，（即系统把所有值都当作字符串放到变量中，不论这个“字符串”实际上是整数、浮点数等等）

###1.用户自定义变量

>·定义格式：变量名=变量值(=两边不含空格)
·调用格式：**echo $变量名**（调用的是变量名等效的值）
·变量叠加：$x=123,y="$x"123则y=123123  或者 y=${x}123
·查看变量：set（列出所有变量）
		*Set –u（设定当调用不存在时会提示错误）*
	·删除变量：unset 变量名
	
###2.bash环境变量

>1.环境变量是全局变量，用户自定义变量是局部变量。用户自定义变量只在当前shell中生效，环境变量在当前shell和这个shell的所有子shell中生效。
对系统生效的环境变量名和变量作用是固定的。
建议都设置为大写。
	
>2.设置环境变量
	export 变量名=变量值
	或
	变量名=变量值
	export 变量名

>3.查看环境变量
	set #查看所有变量
	env #只查看环境变量

>4.删除环境变量
unset 变量名
注意：在子shell中删除环境变量，只删除了当前shell的环境变量， 父shell的环境变量不会发生改变。

>5.PATH环境变量：
	![这里写图片描述](http://img.blog.csdn.net/20170417224220873?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2luYXRfMzQzMjIyODU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)
>>系统搜索命令的路径，路径之间用：分割。
Linux中执行可执行文件常用的方法是输入绝对路径，但是如果不输入路径时，系统会在PATH中的路径中寻找该可执行文件，直到找到该指定文件，就执行，但是找不到时就报错。
当我们想要直接输入文件名就能执行自定义脚本，①将该脚本文件复制到PATH中的任意路径中；②在PATH中添加该脚本文件的路径
**echo $PATH #查看PATH环境变量**
PATH="$PATH":文件路径名 #利用变量的叠加，将要定义为环境变量的路径加到PATH中，只是临时生效，要永久生效要写入文件中
tab补全命令也是按照PATH中的来补全

>6.pstree #查看进程树，查看shell进程

附加：
![PS1环境变量](http://img.blog.csdn.net/20170417225402827?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2luYXRfMzQzMjIyODU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

----------



######[Markdown](http://www.jianshu.com/p/1e402922ee32/)的入门指南
![这里写图片描述](http://ww1.sinaimg.cn/large/6aee7dbbgw1effeaclhiyj20eh09cwez.jpg)
![这里写图片描述](http://ww4.sinaimg.cn/large/6aee7dbbgw1effew5aftij20d80bz3yw.jpg)
![这里写图片描述](http://ww3.sinaimg.cn/large/6aee7dbbgw1effezhonxlj20e009c3yu.jpg)
![这里写图片描述](http://ww2.sinaimg.cn/large/6aee7dbbgw1efffa67voyj20ix0ctq3n.jpg)
![插入代码](http://ww3.sinaimg.cn/large/6aee7dbbgw1effg1lsa97j20lt0a8dgs.jpg)
![分割线](http://ww3.sinaimg.cn/large/6aee7dbbgw1effgmnpgqlj210j0us44j.jpg)




