MKOnlineMusicPlayer
========
MKOnlineMusicPlayer 是一款开源的基于 `Meting` 的在线音乐播放器。具有音乐搜索、播放、下载、歌词同步显示、个人网易云音乐播放列表同步等功能。

前端界面参照 QQ 音乐网页版进行布局，同时采用了流行的响应式设计，无论是在PC端还是在手机端，均能给您带来原生 app 般的使用体验。

### 界面欣赏
-----
![主界面(电脑端)](https://user-images.githubusercontent.com/16880885/30487091-f7b45980-9a64-11e7-9588-8b6b87ac6763.jpg)

![播放列表界面(电脑端)](https://user-images.githubusercontent.com/16880885/30487141-1f8ad416-9a65-11e7-960c-a102c47a3d0e.jpg)

![歌曲搜索与播放](https://user-images.githubusercontent.com/16880885/30487344-c93a0306-9a65-11e7-92f3-552072b1dbce.jpg)


### 相关链接
-----
**在线演示** [http://test.zwblog.cn/music/](http://test.zwblog.cn/music/)

**详细介绍** [http://mkblog.cn/1060/](http://mkblog.cn/1060/)

**GitHub** [https://github.com/zwchn/zaixianmusic](https://github.com/zwchn/zaixianmusic)

### 注意事项
-----
#### 运行环境
php 5.4+, curl_exec, file_get_contents, json_decode, openssl_encrypt

#### 兼容性
本播放器设计支持 IE9及以上的现代浏览器。并且已在 Chrome、firefox、IE11 等浏览器测试使用正常。

#### 版权
本播放器由 [mengkun(https://mkblog.cn)](https://mkblog.cn) 开发，您可以随意修改、使用、转载。使用或转载时`请务必保留出处`，抱拳了各位老铁们！

#### 歌曲
播放器中的歌曲来自各大音乐平台，歌曲版权归各大平台享有。请支持正版音乐。

#### 其它
作者很忙，非诚勿扰。欢迎提交 BUG 及好的建议，不欢迎一上来就问一些基础的东西及唠东唠西。
`如果要提交问题，请务必告知您的网址，否则无法处理`

### 常见问题
-----
[请前往 wiki 查阅](https://github.com/mengkunsoft/MKOnlineMusicPlayer/wiki)
`遇到问题请详细阅读以上 wiki，已经进行解答的问题将不再回复！`

#### v2.41 `2018/3/13`
- 修复 IE 下播放键错位的 BUG
- 修改默认背景为黑色
- 其它一些细节优化

#### v2.4 `2018/3/11`
- 修复网易云音乐无法播放
- 增加标题栏滚动效果(感谢@lzcykevin)
- 增加歌曲循环播放控制(感谢@yuxizhe)
- 修复百度音乐无法播放
- 优化连续播放失败的歌曲过多时，自动终止播放。防止卡死
- 压缩图片素材，限制封面图片尺寸，优化页面加载速度

#### v2.32 `2017/9/15`
- 修复播放历史记录歌曲时播放失败的 BUG
- 新增播放歌曲时浏览器标题栏显示相关信息
- 一些细节的完善

#### v2.31 `2017/9/13`
- 优化下载功能，支持直接弹出下载
- 下载或分享无版权音乐时给出提示
- 再次降低移动端背景特效内存占用
- 修复某些手机浏览器列表页右侧菜单按钮下移 BUG
- 升级 Meting 至最新版本

#### v2.3 `2017/9/9`
- 全面支持网易云、QQ、虾米、酷狗、百度音乐源切换
- 移动端歌曲列表支持直接分享、下载歌曲
- 降低内存占用，解决移动端背景特效卡顿问题
- 新增对 https 的支持(酷狗、百度音乐源除外)
- 新增运行环境自检功能
- 优化中等屏幕下显示效果
- 修复长歌词定位错乱的 BUG
- 修复无法获取自定义专辑封面的 BUG
- 修复移动端无法自动播放下一曲的 BUG
- 修复切换播放列表后滚动条未归位的 BUG
- 修复某些情况下歌词与歌曲不对应的 BUG
- 修复中小屏幕下顶部 tab 激活错乱的 BUG
- 修复搜索分页的 BUG
- 去除超时检测


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


