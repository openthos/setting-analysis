# 往整个项目中添加新的application总结
内容：

- 整体app实现
- 项目移植准备
- 实现方式
- 配置文件
- 运行编译

## １.整体app实现
- 实现你要完成的application功能，可以使用eclipse 或者 androidStudio开发工具,基本实习按正常app开发流程进行就好
- 要注意你开发的apk的sdk版本，要与androidx86所兼容支持的sdk版本一致，版本太低，太高目前可能都会有些许问题，现阶段默认使用
android sdk为5.1.1
- 保证本地编译运行正常

## ２.项目移植准备
- 针对你本地开发的应用，一些注意细节，首先，应用布局文件中不可以有直接android:text="xxx"之类语法，所有用到的必须使用R.String
引用，否则编译不通过。
- 其次，在编写本地代码过程中尽量少使用tab键（或你把tab默认改成４个空格）,否则代码移植上去后后格式混乱，后期整理耗时颇多
- 明确你要移植的app路径,一般app存放路径（根目录／package/app），如若需要，需要管理员给你建一个你的应用相关的空文件，你可以把自己的代码push到服务器上，一般编译者是
没有创建库的权限的。

## ３.实现方式
- 实现方式有两种，看个人爱好：第一种：一切都是新建的，同时需要放在已经存在的列子创建Android.mk、CleanSpec.mk
类似于这种结构：
![image](https://github.com/openthos/setting-analysis/edit/master/1.jpg)
第二种方式：直接将其他文件中的相关文件复制过来。只需后期更改其中内容即可（推荐使用第二种，减少出错概率）
- 你需要熟悉linux的复制粘贴命令，需要将你自己本地应用中的res,src以及AndroidManifest.xml移植到服务器上，保证不会遗漏

## ４.配置文件
- 接下来进行配置文件配置，首先是Android.mk文件，如图（只是随便举了个例子，具体情况具体分析）：
![image](https://github.com/openthos/setting-analysis/edit/master/Android配置文件.png)
修改其中的LOCAL_PACKAGE_NAME　为你自己的应用名称，如果引入新的jar包，需要LOCAL_PREBUILT_STATIC_JAVA_LIBRARIES := xutils:xUtils-2.6.14.jar
处理，将该包放到根目录下，参考相应例子实现即可
- 接下来配置CleanSpec.mk，内容如图:
![image](https://github.com/openthos/setting-analysis/edit/master/cleanSpec配置文件.png)
只需添加自己需要的项目即可
- 接下来，要让应用可以部署上去重要的配置：在build/target/product/core.mk文件，在PRODUCT_PACKAGES 中添加自己的项目名称即可

## ５.运行编译
- 运行过程中若报错，根据错误提示（Error）提示区修改错误内容，然后重新编译，直至可以顺利编译通过
- 可以运行跑起，点击观察自己的应用是否可用，若布局等有所不同，需要自己在后期处理
- 一切正常，就可以提交代码，将新应用仍上去了
