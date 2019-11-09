# FART
ART环境下基于主动调用的自动化脱壳方案，基于Android 6.0实现，理论上可以移植到任何ART系统上，现在已经移植到Android 8.0，很快就将移植到Android 10.0。具体原理和实现请移步看雪，系列文章共计3篇，对加固和对抗感兴趣的可以看看：


1、拨云见日：安卓APP脱壳的本质以及如何快速发现ART下的脱壳点 https://bbs.pediy.com/thread-254555.htm


2、FART正餐前甜点：ART下几个通用简单高效的dump内存中dex方法 https://bbs.pediy.com/thread-254028.htm


3、FART：ART环境下基于主动调用的自动化脱壳方案 https://bbs.pediy.com/thread-252630.htm


安装完待脱壳的应用后，点击应用，等待开始进入脱壳，点击应用后请不要再进行其他操作，此时查看logcat，过滤ActivityThread此时可以看到脱壳日志，脱壳后的文件位于应用的私有目录下，如应用的报名为com.example.code,则脱壳下来的dex位于/data/data/com.example.code目录下。由于脱壳时间可能较长，与应用的大小有关，建议等待一段时间，先喝杯热咖啡。（如果发现脱壳后的dex依然不够，可以多尝试脱几次，甚至待应用脱壳结束后手动点击app，完成一些交互）。


 更新1.1版，修复上一个版本由于没有对脱壳的应用彻底过滤的原因导致的配置文件失效，对所有app进行脱壳的问题。


 更新1.2版，修复上一个版本中存在的一些异常；重新寻找dump整体dex的点，从而解决某数字壳以及某加密壳等无法dump整体dex的问题。
 
 qq群共享有上传1.2.1betal版，功能更强大，让内存中的dex无处藏身，但可能还存在一些小问题，所以不在这里上传，需要的可以去群内自取。同时，鉴于有些安全爱好者手中没有nexus5真机，而在用模拟器过程中又遇到各种问题，导致不能启动，这里再在qq群公告中上传了可以启动的sdk，需要的可以自取。（依然建议使用真机，模拟器只适合体验）
 
 此次更新修复函数体文件乱序问题，同时，提升fart运行效率问题。同时，提供的压缩包中包含了一个可供测试的apk。
 
 脱壳流程：
 
 1、安装待脱壳apk，并到设置中授予sd卡读写权限
 
 
 2、将fart配置文件fart复制到/data/fart（注意文件权限问题，和换行的问题），其中，fart配置文件中为要脱壳的app包名
 
 
 3、点击app图标，开始进入fart脱壳过程
 
 
 接下来可以对logcat中的tag为ActivityThread的log进行过滤，等待出现"fart run over"，此时fart主动调用过程结束。脱壳下来的
 
 dex文件和函数体bin文件均在/sdcard/fart/app包名的目录下
 
 
 下面截图为fart的运行流程和脱壳结果
 
 <p align="center">
  <img width="200" height="200" src="https://github.com/hanbinglengyue/img/blob/master/logcat.JPG">
</p>
 
 
<p align="center">
  <img width="200" height="200" src="https://github.com/hanbinglengyue/img/blob/master/fartresult.JPG">
</p>

这里将arm模拟器、nexus5镜像合并为一个包，以供下载。


链接：https://pan.baidu.com/s/18QIdXKwp5VCYAL_jxXcwEA 
提取码：wyxm 


联系邮箱：edunwu@gmail.com 另外建立了个qq群方便交流,群内提供学术交流并上传最新相关资料，感兴趣的可以扫描二维码加群。

qq群二维码
<p align="center">
  <img width="200" height="200" src="https://github.com/hanbinglengyue/img/blob/master/qq.JPG">
</p>


