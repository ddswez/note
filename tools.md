
#### 工具 

##### 抓包工具 whistle Android开发抓包利器,唯一推荐

​       [GitHub 地址](https://github.com/avwo/whistle/blob/master/README-zh_CN.md)

​       [文档地址](http://wproxy.org/whistle/)

- 匹配response中某一字符替换  用于同一个url请求多个接口, 根据请求头中字段不同返回不同数据

  1. rules: https://www.xxx.com/v1/abce resReplace://{ticker.json}
  2. values: 正则匹配请求的resposne包含字符串 "test"

  /.\*?test.\*/:  {"result":[{"result":{"a":7.15,"b":7.17,"c":1,"d":100,"e":10000,"f":5,"g":0,"test":0}}]}

  3. 根据想获取的数据修改在values中的字符串

- 直接替换请求response 用于一个url请求一个接口

  1. relues中新建 https://www.io.com/v1/info  resBody://{appinfo.json}
  2. values中直接新建appinfo文件, 把response的json直接复制进去修改即可

##### 本地服务器文件列表H5AI

- docker 安装 H5AI

  1. 安装docker

  2. $ docker pull clue/h5ai

  3. $ docker run -d -p 80:80 -v PWD :/var/www clue/h5ai

     > 例如: docker run -d -p 80:80 -v /Users/just/h5ai:/var/www clue/h5ai

  4. 浏览器 输入 localhost查看

     > PWD:  /Users/用户名/h5ai   /h5ai: 新建文件夹用于存放需要共享的文件
  
     > 重启电脑后如果需要重新启动   
     >
     > - docker ps -a
     > - docker start xxxxxx(容器id)

参考: [<https://hub.docker.com/r/clue/h5ai/>](<https://hub.docker.com/r/clue/h5ai/>)

##### websocket在线调试

<http://coolaf.com/tool/chattest>

---

#### 布局相关

* ConstraintLayout

​       [android 约束布局容器ConstraintLayout的初探](https://www.jianshu.com/p/5423989756e8)

​       [ConstraintLayout终极秘籍](<http://blog.chengyunfeng.com/?p=1030>)

​	[ConstraintLayout 完全解析 快来优化你的布局吧](<https://blog.csdn.net/lmj623565791/article/details/78011599>)

* CoordinatorLayout 

  CoordinatorLayout 完全解析](https://www.jianshu.com/p/4a77ae4cd82f) 

  Android 详细分析AppBarLayout的五种ScrollFlags](https://www.jianshu.com/p/7caa5f4f49bd) 

* CollapsingToolbarLayout 

  

* others 

   

---

#### 技术文章  

[Android 内存泄漏全解](<https://juejin.im/entry/57c966b05bbb500074e1d4a4>)

[关于硬件加速的那么点儿东西](<https://www.jianshu.com/p/9cd7097a4fcf>)

[Android：你要的WebView与 JS 交互方式 都在这里了](<https://blog.csdn.net/carson_ho/article/details/64904691>)

[Android：这是一份全面 & 详细的Webview使用攻略](<https://www.jianshu.com/p/3c94ae673e2a>)

##### Router

[Android Router 从 0 到 1](<https://juejin.im/entry/5897a1c8128fe10058e76368>)

#####  Gradle

[gradel 属性详解官方文档](<https://google.github.io/android-gradle-dsl/current/com.android.build.gradle.BaseExtension.html>)

[Gradle 4.1更新内容及注意事项](<https://my.oschina.net/u/3389024/blog/1605822>)

[Gradle User Guide 中文版](<https://dongchuan.gitbooks.io/gradle-user-guide-/>)

[如何发布jar/aar到本地仓库](<https://www.jianshu.com/p/0629548ab5a4>)

[Android依赖导入全攻略](<https://juejin.im/post/5acd6daaf265da238a30ca73>)

[如何理解 Transform API](<https://juejin.im/entry/59776f2bf265da6c4741db2b>)

[Android动态编译技术:Plugin Transform Javassist操作Class文件](<https://blog.csdn.net/yulong0809/article/details/77752098>)

[Transform 官方文档](<http://google.github.io/android-gradle-dsl/javadoc/> )

##### View

[深入理解View知识系列一- setContentView和LayoutInflater源码原理分析](http://blog.csdn.net/yulong0809/article/details/79277574)

[深入理解View知识系列二- View底层工作原理以及View的绘制流程](http://blog.csdn.net/yulong0809/article/details/79277594)

[深入理解View知识系列三-Window机制、Canvas的由来、Android事件的由来](http://blog.csdn.net/yulong0809/article/details/79277633)

[深入理解View知识系列四-View的测量规则以及三大方法流程](http://blog.csdn.net/yulong0809/article/details/79277667)



##### 正则

[正则表达式30分钟入门教程](<http://deerchao.net/tutorials/regex/regex.htm>)



##### 疑难杂症  

[Android Release 切换到后台再点桌面图标进入后, App 重启](<https://blog.csdn.net/stupid56862/article/details/82219554>)

[解决Android应用第一次安装成功后Home键切到后台再点击桌面图标应用重启](<https://www.jianshu.com/p/9757ce0c69a5>)

