Swift Learning


//This article introduce the outlets strong or weak are difference.
http://scottberrevoets.com/2016/03/21/outlets-strong-or-weak/

//This is iOS developer must knows 14 items
https://github.com/xitu/gold-miner/blob/master/TODO/14-must-knows-for-an-ios-developer.md

//This is a learning website.
http://fuckingswiftblocksyntax.com/


http://www.cocoachina.com/ios/20170301/18811.html


############################################Link ######################

26.GPUImage 系列教程：http://www.jianshu.com/nb/4268718
27.OPenGL 系列教程：http://www.jianshu.com/nb/2135411
28.OpenGL 基础教程：https://learnopengl-cn.github.io 配合着书本一起看有助于理解
29.着色器语言概述：https://www.cnbogs.com/oloroso/p/5159378.html
30.OpenGL 详解：http://www.jianshu.com/p/9d7dca6b70c7
31.着色器代码地址：https://github.com/XJALYN/OpenGLES_Learn.git
32.GLSL 语言关键字：http://blog.csdn.net/hgl868/article/details/7846269
34.自定义视频播放器：http://www.sohu.com/a/124410052_473801
35.一篇入门OpenGL的不错的文章：http://blog.csdn.net/Xoxo_x/article/details/72598275
36.滤镜链的玩法：http://blog.csdn.net/u1031/article/details/48712163
37.大神的实时美颜滤镜：http://www.jianshu.com/p/945fc806a9b4
38.直播中运用faceu效果：http://www.jianshu.com/p/ba1f79f8f6fa

################################################Note##############################################
open
* open 修饰的 class 在 Module 内部和外部都可以被访问和继承
* open 修饰的 func 在 Module 内部和外部都可以被访问和重载（override）

Public
* public 修饰的 class 在 Module 内部可以访问和继承，在外部只能访问
* public 修饰的 func 在 Module 内部可以被访问和重载（override）,在外部只能访问

Final
* final 修饰的 class 任何地方都不能不能被继承
* final 修饰的 func 任何地方都不能被 Override

现在的访问权限则依次为：open，public，internal，fileprivate，private
