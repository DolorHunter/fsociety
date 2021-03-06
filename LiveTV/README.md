# 网络电视直播源整理

- 声明:

节目源均来源于网络. 其中使用[罗宾(节目源已停更)](https://www.youtube.com/channel/UClHivjMLEM-ZqrI3skBPMHw), [Zzlab](https://www.youtube.com/channel/UCSRmL8I81f0PSbdJ8ktQOAw), [xuehaijun88](https://github.com/xuehaijun88)等不具名的用户提供的源, 在此表示感谢!!

**节目源导入电视直播软件节目单即可使用. 请优先使用时间靠后的节目单. 部分节目单内的源不稳定.**

## 快速导航

__[节目单文件名说明](#节目单文件名说明)__

__[导入我的节目单到直播软件](#导入我的节目单到直播软件)__

__[制作我的节目单](#制作我的节目单)__

## 节目单文件名说明

`[测试日期][是否需要翻墙][电视台地区].txt`

1. 文件名上的日期标号为电视源测试日期. 请选择最新日期的文件下载.

2. 免翻源比较**不稳定**, 且存在来源被GFW阻断情况. 多数存在线路*不稳定(看一会儿就断线要刷新)/(有些时段无讯号)*. 需要经常维护更新.
翻墙源均从Youtube爬取, **高清且稳定**, 但是**需要翻墙**才能使用.

3. 地区按照文件名分类可见.

4. **欢迎大家自制节目单上传到本仓库.**

## 导入我的节目单到直播软件

`不同版本, 不同软件可能有些微差异. 此处使用`**HDP直播**`举例.`

1. 打开电视HDP直播, 点击退出按键. 此时出现退出二级界面. (注意不要退出到主界面). 此时屏幕上有本机IP类似[192.168.***.***]的信息. 

2. 此时使用手机或电脑打开浏览器(手机/电脑和电视要在同一个网段下(连接同一个路由)), 输入以上网址回车进入HDP远程管理.

3. 选择上传视频源文件/节目单文件, 将自制的节目单文件上传到HDP直播. 此时提示上传成功.

4. 打开电视HDP直播, 按确认键打开节目单. 按左右键切换节目单至上传的自定义节目单即可找到上传的节目.

## 制作我的节目单

### 免翻版(不稳定版)

0. 下载vlc 对源进行测试.

1. 进入谷歌Chrome浏览器, 下载插件**猫抓**.

2. 打开一些直播网站[好趣网](http://www.haoqu.net/), [chalea直播](http://www.chalea.com/TV)等网站, 找到你想看的节目.

3. 点击右上角**猫抓**插件, 抓取页面信息. 复制[*****.m3u8]的信息, 粘贴至vlc软件对节目源进行测试.

4. 如果vlc能够正常播放, 可以以[电视台,节目源]格式记录到记事本中, 即[xx卫视,*****.m3u8].

### 翻墙版(稳定版)

*突然发现Youtube会一直更新源的信息, 看来要用youtube-dl实时获取新的m3u8..*

*有知道怎么弄的朋友麻烦告诉我. 多谢!!*

~~`刚刚用了试了you-get方法和网页原始码的方法都不太成功. 我讲讲我刚刚研究出来的可行的办法好了.`~~

~~**[注意]: 需要全程挂全局代理!!** (全局登天系统使用SSTap的Sock5连接127.0.0.1:1080创造全局环境)~~

~~0. 下载youtube-dl / vlc 等. 如果不是从pip下载可能要添加一下环境变量.~~

~~1. cmd/pwsh: 输入命令youtube-dl --list-formats https://www.youtube.com/watch\?v\=_Gtc-GtLlTk(改成想要的网站)~~

~~2. 然后出来一些直播源的信息, 然后选一个执行命令: youtube-dl -f 95 -g https://www.youtube.com/watch\?v\=_Gtc-GtLlTk(相同的网站)~~

~~3. 之后就会获得.m3u8的直播源信息. 然后去vlc测试一下能不能看. 我这边测了几个都ok.~~

~~*写的不是很清楚, 参考这个做的, 你们如果看不懂我写的可以参考一下StackOverflow上的[原始方法](https://stackoverflow.com/questions/35608686/how-can-i-get-the-actual-video-url-of-a-youtube-live-stream).*~~
