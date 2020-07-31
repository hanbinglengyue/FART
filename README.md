# FART
ART环境下基于主动调用的自动化脱壳方案，基于Android 6.0实现，理论上可以移植到任何ART系统上。具体原理和实现请移步看雪，系列文章共计3篇，对加固和对抗感兴趣的可以看看：


1、拨云见日：安卓APP脱壳的本质以及如何快速发现ART下的脱壳点 https://bbs.pediy.com/thread-254555.htm


2、FART正餐前甜点：ART下几个通用简单高效的dump内存中dex方法 https://bbs.pediy.com/thread-254028.htm


3、FART：ART环境下基于主动调用的自动化脱壳方案 https://bbs.pediy.com/thread-252630.htm

 
 脱壳流程：
 
 1、安装待脱壳apk，并到设置中授予sd卡读写权限(否则dump下的文件无法写入到sdcard)
 
 
 2、点击app图标，开始进入fart脱壳过程

 
 接下来可以对logcat中的tag为ActivityThread的log进行过滤，等待待脱壳app进程出现"fart run over"，此时fart主动调用过程结束。脱壳下来的
 
 dex文件和函数体bin文件均在/sdcard/fart/app包名的目录下
 
 
 下面截图为fart的运行流程和脱壳结果
 
 <p align="center">
  <img width="600" height="80" src="https://shop.io.mi-img.com/app/shop/img?id=shop_1af85f3aa99152c0c1e639b68c5eb072.jpeg">
</p>
 
 
<p align="center">
  <img width="600" height="400" src="https://shop.io.mi-img.com/app/shop/img?id=shop_fc3910a8d77359bafc66c7aa19ae3eca.jpeg">
</p>

FART 6.0 8.0镜像地址:


链接：https://pan.baidu.com/s/1c3AyDZ92vVPxt06xwjFO9w 
提取码：1yzb

联系邮箱：edunwu@gmail.com 另外建立了个qq群方便交流,群内提供学术交流并上传最新相关资料，感兴趣的可以扫描二维码加群。

qq群二维码
<p align="center">
  <img width="200" height="200" src="https://shop.io.mi-img.com/app/shop/img?id=shop_120792e8e3796da77247e610eb8e39cf.jpeg">
</p>

--------------------------------------------------------------------------------------------------
添加frida版的fart的两种不同实现，各有特色。可以实现具体到对某一个类下的所有函数甚至是对某一个函数的CodeItem的dump。需要的可以去体验下其强大的脱壳能力。(注意，测试环境为pixel Android8.0,frida-server 12.8.0)
<p align="center">
  <img width="600" height="400" src="https://shop.io.mi-img.com/app/shop/img?id=shop_257a3a5d40964ec8e941865e817e5224.png">
</p>
