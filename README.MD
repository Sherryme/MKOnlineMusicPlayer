SherryMusic web
========
SherryMusic 是一款开源的基于 `Meting` 的在线音乐播放器。具有音乐搜索、播放、下载、歌词同步显示、个人网易云音乐播放列表同步等功能。

前端界面参照 QQ 音乐网页版进行布局，同时采用了流行的响应式设计，无论是在PC端还是在手机端，均能给您带来原生 app 般的使用体验。

### 界面欣赏
-----
![主界面(电脑端)](https://user-images.githubusercontent.com/16880885/30487091-f7b45980-9a64-11e7-9588-8b6b87ac6763.jpg)

![播放列表界面(电脑端)](https://user-images.githubusercontent.com/16880885/30487141-1f8ad416-9a65-11e7-960c-a102c47a3d0e.jpg)

![歌曲搜索与播放](https://user-images.githubusercontent.com/16880885/30487344-c93a0306-9a65-11e7-92f3-552072b1dbce.jpg)


### 相关链接
-----
**详细介绍** [http://mkblog.cn/1060/](http://mkblog.cn/1060/)

**GitHub** [https://github.com/mengkunsoft/MKOnlineMusicPlayer](https://github.com/mengkunsoft/MKOnlineMusicPlayer)

### 注意事项
-----
#### 运行环境
php 5.4+, curl_exec, file_get_contents, json_decode, openssl_encrypt

#### 兼容性
本播放器设计支持 IE9及以上的现代浏览器。并且已在 Chrome、firefox、IE11 等浏览器测试使用正常。

#### 版权
本播放器由 [mengkun(http://mkblog.cn)](http://mkblog.cn) 开发，您可以随意修改、使用、转载。使用或转载时`请务必保留出处`，抱拳了各位老铁们！

#### 歌曲
播放器中的歌曲来自各大音乐平台，歌曲版权归各大平台享有。请支持正版音乐。

### 常见问题
-----
**歌单读取失败 - 404**

本程序需要上传至网站空间(服务器)使用，不支持在本地打开

**歌单读取失败 - 200**

请确保你的服务器支持 PHP ，并且 PHP 版本 >= 5.4


**歌单页封面显示不出来**

请打开 `api.php`，将第十行的 `define('HTTPS', true);` 修改为 `define('HTTPS', false);`

### 待解决的问题
-----
- 高音质音乐下载功能
- IOS 歌曲播放问题
- 歌曲播放模式切换(单曲循环、随机播放、列表循环)功能

### 开发文档[待完善]
-----
#### 播放列表DIY教程
本播放器支持后台自定义播放列表。打开 `js/musicList.js`，按照里面的说明对应修改即可。

#### 播放器DIY教程
除了自定义播放列表，本播放器还支持一些 DIY 设定，比如修改 api.php 文件的默认路径、修改搜索框的默认搜索内容等。具体请打开 `js/player.js` 查看

#### rem 变量表
程序中的rem数组用于存储全局变量，具体的成员(部分)及作用见下表：

| 变量名    | 用途   |
| ----------- | ----------- |
| rem.audio | audio dom |
| rem.playlist | 当前正在播放的播放列表编号 |
| rem.playid | 正在播放的这首歌在播放列表中的编号 |
| rem.dislist | 当前显示的列表的列表编号 |
| rem.loadPage | 搜索功能已加载的页码 |
| rem.wd | 当前的搜索词 |
| rem.source | 当前选定的音乐源 |
| rem.uid | 当前已同步的用户的网易云 ID |
| rem.uname | 已登录用户的用户名 |
| rem.sheetList | 歌单容器操作对象 |
| rem.mainList | 歌曲列表容器操作对象 |
| rem.isMobile | 是否是手机浏览 |

### 致谢
-----
#### 特别感谢 `@metowolf`、`网易云音乐`、`QQ音乐`、`虾米`、`酷狗`、`百度音乐`

#### 采用的开源模块
- **Jquery**：js主流开发框架 [http://jquery.com/](http://jquery.com/)
- **Meting**：一个高效的多平台音乐 API 框架 [https://github.com/metowolf/Meting](https://github.com/metowolf/Meting)
- **layer**：一款强大的web弹层组件 [http://layer.layui.com/](http://layer.layui.com/)
- **mCustomScrollbar**：jQuery自定义滚动条样式插件 [http://manos.malihu.gr/jquery-custom-content-scroller/](http://manos.malihu.gr/jquery-custom-content-scroller/)
- **background-blur**：跨浏览器磨砂效果背景图片模糊特效插件 [https://msurguy.github.io/background-blur/](https://msurguy.github.io/background-blur/)
- **Let's Kill IE6**：消灭IE [http://overtrue.me](http://overtrue.me)
