# Settings功能需求与设计实现文档
内容：

- 项目简介
- 功能需求
- 存在问题
- 项目进展
- 设计实现

# 项目简介

本项目属于openthos项目的一部分，提供 [Openthos](https://github.com/openthos/openthos/wiki) 对原Settings的功能扩展与样式改变。

##　当前开发人员 (20170316-20170415)
刘晓旭 曾非非 周怡洁

##　当前开发人员 (20161001-20161130)
李冰 曾非非 周怡洁 

##　当前开发人员 (20160801-20160930)
李冰 王利峰 曹永韧

## 功能需求

|完成|描述|模块|完成度|
|---|---|---|---|
|√| 系统用户管理界面实现|界面|100%|
|√| 以太网界面实现|界面|100%|
|√| 代理模块界面实现|界面|100%|
|√| 防火墙模块界面实现|界面|100%|
|√| 云服务界面实现|界面|100%|
|√| 自启管理模块界面实现|界面|100%|
|√| 运行模式模块界面实现|界面|100%|
|√| 节能模式模块界面实现|界面|100%|
|√| 睡眠时间设置模块界面实现|界面|100%|
|√| 锁屏时间设置模块界面实现|界面|100%|
|√| 重置模块界面添加|界面|100%|
|√| About相关界面改动|界面|100%|
|√| 系统用户管理界面实现|功能|100%|
|√| 以太网界面功能实现　|功能|100%|
|x| 代理模块功能实现|功能|0%|
|x| 防火墙模块功能实现|功能|0%|
|x| 云服务模块功能实现|功能|70%|
|√| 自启管理模块功能实现|功能|100%|
|x| 运行模式模块功能实现　|功能|0%|
|x| 节能模式模块功能实现|功能|20%|
|√| 睡眠时间设置模块功能实现|功能|100%|
|√| 重置模块功能实现|功能|100%|
|x| About相关功能完善|功能|80%|

## ８月任务计划

|时间节点|任务|
|---|---|
|2016.8.1-2016.8.7|1.运行模式界面（run mode），按openthos UI 实现，添加自动选择条目<br />2.将系统重置的功能模块移到Ａｂｏｕｔ中，已ｂｕｔｔｏｎ方式触发<br />3.设置默认睡眠时间３０分钟<br />4.设置默认字体为最小字体<br />5.系统中英文对应<br />6.用户名/主机名写入build.prop,无法立即生效（使用命令set prop 解决）待实现 |
|2016.8.8-2016.8.14|1.运行模式功能实现<br />2.代理模式功能实现<br />3.About相关界面功能实现（包括硬盘容量／ｃｐｕ信息等）<br />4.节能模式功能（实现方式有误，需通过ｌｉｎｕｘ命令，调用相关命令　　cpufrequtils) |
|2016.8.15-2016.8.21|1.锁屏时间设置　<br />2.云服务功能<br />|
|2016.8.22-2016.8.31|1.锁屏密码功能<br /> 2.防火墙功能<br />|

## ８月任务计划(20160820-20160902)

|时间节点|任务|
|---|---|
|2016.8.20-2016.8.26|界面优先<br />1.系统用户管理 -有BUG,未对齐<br />2.开机自启动—后面的按钮图标太大（王立峰负责）<br />3.系统升级-界面差（陈老师安排人去解决）<br />4.防火墙-- 界面少一列(新需求如此，不用改动）<br />功能实现<br />5.节能模式功能实现<br />6.休眠，切换电源状态，导致睡眠时间不稳定(有BUG,已提交)<br />7.锁屏密码实现以及锁屏时间设置(实现功能按时完成有风险，暂定时间充足去研究解决，否则移到八月之后) |
|2016.8.30-以后|1.设置-有线网---静态IP功能未实现（需验证）<br />2.代理模式功能实现<br />3.DHCP 地址也显示在界面上<br />4.锁屏时间设置<br /> 5.锁屏密码功能<br />6.云服务功能<br />7.防火墙功能<br />8.显示-壁纸-图库一点就死(BUG,遗留BUG )<br />|

## 9月任务计划(20160919-20160930)

|时间节点|任务|
|---|---|
|2016.9.19-2016.9.23|周怡洁:https://github.com/openthos/setting-analysis/blob/master/%E5%85%B3%E4%BA%8ESettings%E4%B8%AD%E5%A4%9A%E4%BD%99%E6%A8%A1%E5%9D%97%E9%A1%B9%E7%9B%AE%E7%9A%84%E9%9A%90%E8%97%8F%E6%96%B9%E6%A1%88%E6%80%BB%E7%BB%93%EF%BC%8820160917%E5%91%A8%E6%80%A1%E6%B4%81%EF%BC%89<br />1.根据以前跟刘总的讨论结果整理一份关于settings需隐藏功能条目的文档，依次文档由简及繁的进行界面或功能的隐藏移植等<br />曾非非<br />1.进行升级界面（OtoOta）的修正完善，根据任务进度会做出调整，后期会支援周一洁的Settings隐藏任务<br />李兵<br />1.完善powerpoint 相关全屏的问题<br />2.实现header的自动隐藏<br />3.根据进度情况，根据陈工分配bug进行fix <br />|
|2016.9.26-2016.9.30|周怡洁／曾非非：<br />根据上周完成情况在具体安排，主要完善settings功能隐藏里边剩余较繁琐的项目,曾菲菲负责完善otoota的后期对接工作<br />李兵：<br />１.实现tagic　video 全屏显示<br />２.实现部分应用header的自动隐藏<br />3.继续进行相关multiwindow的bug修复<br />|

## 10月任务计划(20161008-20161030)

|时间节点|任务|
|---|---|
|2016.10.08-2016.10.20|周怡洁:<br />1.热键设置，功能支持，在settings中增加新的模块实现（参考linux有哪些）<br />曾非非:<br />1.调研实现锁屏相关功能feature（包括锁屏密码及锁屏时间设置）<br />李兵:<br />1.改善terminal界面及使用体验<br />2.完善应用打开方式及部分应用标题栏header的的隐藏显示<br />3.根据进度情况，根据陈工分配bug进行fix <br />|
|2016.10.24-2016.10.30|周怡洁:<br />1.修改泰捷视频的bug<br />2.热键国际化<br />3.Setting中，充电时休眠功能移动到电源管理<br />曾非非:<br />1.解决锁屏功能以及按键盘所有键进入锁屏密码界面。<br />2.完善OtoOta相关问题。<br />李兵:<br />1.移植terminal源码到开发环境中<br />2.完善界面展示以及功能在openthos中<br />3.熟悉配置流程、完成工作机的配置 <br />4.进行触摸copy事件的调研、完成自己组内工作分配与帮助 <br />|

## 11月任务计划(20161101-20161130)

|时间节点|任务|
|---|---|
|2016.11.01-2016.11.30|周怡洁:<br />1.热键具体功能后期完善<br />2.云服务<br />3.锁屏密码设置相关（第一次启动会用到，与曾非非合作完成）<br />曾非非:<br />1.openthos版本设置相关问题。<br />２.锁屏密码设置。<br />３.锁屏时间设置。<br />４.防火墙功能。<br />|

## 3-4月任务计划(20170316-20170415)

|时间节点|任务|
|---|---|
|2016.11.01-2016.11.30|1.[feature]应用的运行模式<br />2.[feature]谷歌输入法的稳定性改善<br />3.[bug]重启后wifi检测<br />4.隐藏云服务和防火墙的条目<br />5.解决ota升级存在的bug<br />6.根据测试提供的优先级高的bug进行fix|

# 存在问题

| 简述 | 类别 | 备注
|---|---|---|
|谷歌输入法的焦点依托|feature|手机输入法默认没有此feature，需调研|
|云服务应用商店与应用数据同步|feature|需要应用商店支持相应功能，此feature才能实现|
|应用运行模式|feature|目前通过白名单控制，需完善为通过Setting数据保存控制，需要与systemui组合作实现此feature|
|防火墙涉及底层实现或命令的功能|feature|需要与底层对接人员协作实现|
# 项目进展

- 2016/05/01-2016/05/15
  * 李兵
    * 在本地实现仿ｑｑ样式的自定义OtoSettings　的view 样式
  * 朱思敏
    * 实现OtoSetting 界面原型
�
- 2016/05/16-2016/05/31
  * 李兵
    * 实现本地OtoSettings 往multiwindow上的移植，并逐步开始实现简单功能
  * 朱思敏
    * 实现本机信息的获取功能

- 2016/06/01-2016/06/15
  * 李兵
    * 逐步往OtoSettings中融入功能，由于设计思路问题，开始决定以功能到页面的方式实施
  * 朱思敏
    * 打印机的界面实现
�
- 2016/06/16-2016/06/30
  * 李兵
    * 实现系统用户管理模块
  * 朱思敏
    * 调研对安卓底层系统文件的读写修改，并成功找到对底层文件修改的方法。对系统用户名的修改。

- 2016/07/01-2016/07/15
  * 李兵
    * 现以太网模块的追加，以及节能模式模块追加
  * 王利峰　　　　
    * Settings中增加程序自启模块（AutoStart）,参考Settings中其他模块实现了界面的展示，功能未实现。
�
- 2016/07/16-2016-/07/28
  * 李兵
    * 实现代理模块追加，锁屏时间模块追加，About相关条目改动
  * 王利峰
    * Settings中增加防火墙模块（FireWall）,实现了界面展示；ettings中代理模块界面（proxy）进行优化；
  * 王之旭
    * 实现CloudService界面；完善FireWall界面；实现SystemReset模块；完善RunMode功能／FireWall界面；

- 2016/07/29-2017/03/16
  * Settings功能需完善模块：
    * 无线和网络：蓝牙、VPN
    * 设备：
      * 显示：字体大小
      * 电源管理：锁屏
    * 个人：账户、系统账户管理
    * 系统：关于设备、云服务、热键
  * Settings功能缺失模块： 
    * 无线和网络：代理
    * 设备：
      * 运行模式
      * 显示：屏幕分辨率
      * 电源管理：节能设置 
    * 个人: 防火墙  
   
# 设计实现

我将涉及到的整体流程及技术点分别叙述。

## 如何在系统上添加一个新的应用以及注意点（类似与追加打印机、文件管理器及桌面应用等）

请查看：[InstallApp.md](https://github.com/openthos/setting-analysis/edit/master/InstallApp.md)

## Settings整体代码结构以及语法格式特点

请查看：[specialIntroduce.md](https://github.com/openthos/setting-analysis/edit/master/specialIntroduce.md)

## Settings各个模块的代码结构

请查看：[setting_modules.md](https://github.com/openthos/setting-analysis/blob/master/setting_modules.md)   

## 如何往settings中追加新的一个项目（类似于运行模式）

请查看：[文档](https://github.com/openthos/setting-analysis/edit/master/如何在Settings实现一个运行模式功能的布局V0.3.docx)


## 如何在settings中隐藏已经存在的某些项目

请查看：[setting_hide_menu.md](https://github.com/openthos/setting-analysis/blob/master/setting_hide_menu.md)

## 如何在在Settings中顺利定位要操作的代码位置，以及代码分析经验

请查看：[experience.md](https://github.com/openthos/setting-analysis/edit/master/experience.md)
