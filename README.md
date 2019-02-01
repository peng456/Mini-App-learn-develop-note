# Mini-App-learn-develop-note
Mini-App  Mini Program ,小程序 开发 记录


最近要开发一个篮球的小项目。本来想和几个小伙伴一起做。其中一个小伙伴，也有相同的想法。
但是你知道的，人总是说着OK，但是却啥都不做。人性就是是这样。想法时时有，但是那只是在头脑中一闪而过。其实没有P用。

于是我就开始自己做。我本身做后端的。

不管了，startUp。

我用 go 写了 后台，接口不多几个。只是CURD。 框架 gin +  gorm 。
（我本身是PHP，也许用PHP实现会更快。但是为了学习go，语言。会遇到一些坑，特别基础的问题。以为go 写起来很会很顺利呢， 看来 go 确实是 很早期呀。（不如PHP 顺手））

前端打算用小程序实现。


如何选择  小程序框架，要考虑那几方面
https://segmentfault.com/a/1190000015032596
https://www.cnblogs.com/Smiled/p/9806781.html


框架呢 , 在两个之间选择:  微信官方、 wepy  和  mpvue (都是GitHuB 上开源的框架)

我觉得还是在  wepy  和  mpvue  之间选择吧。

wepy   :   源码   ==编译 or 实时编译  ==》 官方框架代码

        这个有微信群，也有好多组件，微信官方支持维护
        
 mpvue ：  源码   ==编译 ==》 官方框架代码   (跟wepy 比一个就是没有 实时编译)
 
          支持VUE、很多组件（包括VUE组件）、美团开源的框架
          
暂时 决定 用 wepy  吧。 毕竟 它这个 实时  编译功能 真喜欢。Yeah !!!(昨天看了VUE语法白看了，也许哪天 会用 mpvue 吧 。二者过程应该都差不多。)

开发模式

生成项目
1、npm install wepy-cli -g   // 安装工具  （需要环境，node 、npm）
2、wepy init standard myproject
3、cd myproject
4、npm install
5、wepy build --watch   // 这关就是实时编译功能

6、项目中 dist  就是生成的 ====》 官方框架代码

7、用 Atom  打开 项目 myproject  ===》 修改代码   src 目录中  ===》 实时编译功能 会把 修改编译后 输入 到 dist 目录中

8、《微信开发者工具》   ===》 引入  项目  ，项目位置 为  dist目录

9、正常开发流程
   修改  src 目录中  ==》《微信开发者工具》  点击  “编译”   ===》 就能看到修改  在 小程序 上的显示成果了 Yeah!!!
   
10、这个流程不错，接下来就是  考验  JS编程、组件等使用能力了。

目录如下

<img src="https://github.com/peng456/Mini-App-learn-develop-note/blob/master/Pasted.png" />


有捣鼓起 MPVUE 来了
1、我电脑是mac 按照官网教程 （http://mpvue.com/mpvue/quickstart/）
npm install --global vue-cli@2.9  ====》 这步命令 过不去，一直失败

然后 单独安装 VUE  &&  参加下面  安装了VUE 命令行 ===》 OK了。
http://www.cnblogs.com/pengjunhao/p/6798496.html

2、vue init mpvue/mpvue-quickstart mpvue-project

3、cd mpvue-project

4、npm install

5、npm run dev
端口 8082  是干啥的？？？

src  源文件

dist 目标项目  dist/wx 这个目录下 是生成的 微信目标框架（应该还可以生成其他的 比如 web 、Native 等）


6、项目中 dist  就是生成的 ====》 官方框架代码

7、用 Atom  打开 项目 myproject  ===》 修改代码   src 目录中  ===》 实时编译功能 会把 修改编译后 输入 到 dist 目录中

8、《微信开发者工具》   ===》 引入  项目  ，项目位置 为  dist目录

9、正常开发流程
   修改  src 目录中  ==》《微信开发者工具》  点击  “编译”   ===》 就能看到修改  在 小程序 上的显示成果了 Yeah!!!
   
10、这个流程不错，接下来就是  考验  JS编程、组件等使用能力了。




      
