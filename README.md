# FART
ART环境下自动化脱壳方案，基于Android 6.0方案实现，理论上可以移植到任何ART系统上。具体原理和实现请移步看雪: https://bbs.pediy.com/thread-252630.htm


联系邮箱：edunwu@gmail.com 另外建立了个qq群方便交流：852777822


为了能够更有动力维护和更新该项目，有钱的大佬可以给点茶水费哈，下面附上微信和支付宝打赏码

微信打赏码
<p align="center">
  <img width="300" height="300" src="https://github.com/hanbinglengyue/img/blob/master/1.JPG">
</p>

支付宝打赏码
<p align="center">
  <img width="300" height="300" src="https://github.com/hanbinglengyue/img/blob/master/2.JPG">
</p>



安装完待脱壳的应用后，点击应用，等待开始进入脱壳，点击应用后请不要再进行其他操作，此时查看logcat，过滤dumpDexFile，此时可以查看脱壳日志，脱壳后的文件位于应用的私有目录下，如应用的报名为com.example.code,则脱壳下来的dex位于/data/data/com.example.code目录下


 更新1.1版，修复上一个版本由于没有对脱壳的应用彻底过滤的原因导致的配置文件失效，对所有app进行脱壳的问题。


 更新1.2版，修复上一个版本中存在的一些异常；重新寻找dump整体dex的点，从而解决某数字壳以及某加密壳等无法dump整体dex的问题。
 
 
 这里将arm模拟器、x86模拟机、nexus5镜像合并为一个包，以供下载。


链接：https://pan.baidu.com/s/1M9RE_883wAcTbsEnIGilKw 
提取码：q5bo 
