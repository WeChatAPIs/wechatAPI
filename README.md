### 🌍 *[English](README-en.md) ∙ [简体中文](README.md)*


# 🚀WeChatApi - 你的微信接口和 Hook 解决方案

- WechatAPI 基于微信 Windows 协议和微信安卓协议开发，为你提供一套强大的微信 API工具。
- 我们的目标是让你的微信接入更开放，更可定制。[**立即试用**](https://www.wechatsdk.com/docs/readme/立即试用.md)，体验我们的优势。
- 适合懂任一编程语言的个人开发者使用
- 适合团队中有技术人员的团队使用
- 支持 3.9.5、**3.9.10** 版本 (全量API适配，欢迎测试体验)
- **出3.9.5源码（仅供学习使用），欢迎同学联系**

## 如果您之前使用的`wechaty-padlocal`并且无法使用了，可以考虑使用我们的解决方案
- 这里有github用户贡献的脚手架代码作为参考，已帮助大家快速上手
  - [ts语言](https://github.com/WeChatAPIs/WeChatAPI_puppet)（由独立开发者贡献项目）
  - [go语言](https://github.com/dchaofei/puppet-win)（由独立开发者开源脚手架）
  - 欢迎大家贡献更多语言的脚手架


---
## ✨ 特色功能
- **✅[稳定不被封]()**：
```
  官方风控策略很多包括设备、行为内容、频率、网络等方面，我们能保证不会因为本软件而被封号。
  同时会提供内容、频率、行为等方面风控建议文档
  ```
- **✅[多开微信]()**：```原生支持多开微信```
- **✅[附近人](https://www.wechatsdk.com/docs/社交/获取附近的人.md)**：```支持添加[附近的人] 添加任意位置的附近人```
- **✅[语音条](https://www.wechatsdk.com/docs/发送消息/发送语音.md)**：```融合安卓版本[发送语音条]```
- **✅[视频号](https://www.wechatsdk.com/docs/视频号)**：```融合安卓版本[视频号API] 视频号暴力曝光```
- **✅[朋友圈](https://www.wechatsdk.com/docs/朋友圈)**：```融合安卓版本[朋友圈API] 朋友圈统计复刻```
- **✅[直播间](https://www.wechatsdk.com/docs/直播间)**：```融合安卓版本[直播间API] 直播间刷屏爬虫```
- **✅[公众号API](https://www.wechatsdk.com/docs/公众号)**：```融合安卓版本[公众号API] 公众号文章爬虫，点赞阅读数```
- **✅[查看更多](menu.md)**：[查看更多API](menu.md)

---
## ✨ 与市面上开源产品的区别：
```
- **实现逻辑可见性**：
  - ❌开源产品的代码官方也能看到，因此官方很容易的识别出来，并能针对性的检测风控。
  - ✅而我们的产品是经过多端协议混淆的，并且具有主动诱导策略，所以很难被识别到，如果风控了我们正常用户也无法使用了。
- **风控策略及时性**：
  - ❌由于开源产品作者无收益，因此在遇到官方更改风控策略后没有很强的动力去维护，因此可能会导致用户封号。
  - ✅我们有专业的全职团队，封号率是技术的考核目标，因此我们有很强的动力去维护，也因此能及时的应对官方的风控策略。
- **支持的版本**：
  - ❌开源产品支持的微信版本较低，试想一下如果你是官方，你之前用的版本是3.9.5，突然间开始使用3.9.2的版本了，你会不会认为这个号有问题？
  - ✅我们的产品虽然只支持安装的3.9.5、3.9.10版本，但在内部实现逻辑里已经使用了一部分最新版本的协议主动诱导，因此可以做到稳定。
```
---
## 🚀 免费试用
- [🚀 **立即试用**](https://www.wechatsdk.com/docs/readme/立即试用.md)，体验我们的优势。

---
## 🤝 贡献和反馈
我们欢迎并鼓励社区贡献和反馈。如果您有任何建议或想要贡献代码，请通过 Issues 或 Pull Requests 与我们联系。

---
## 🌐 社交媒体和社区
暂无

---
## 🔖 标签
`微信` `API` `Hook` `微信开发` `协议兼容` `多开微信` `WeChatAPI` `WeChatSDK`

---
## 📅 更新历史记录
### 2024年
- **06月06日**：
  - 扩大`http server`的工作线程数量，现在最大支持64个工作线程，此特性在未来可能会继续调整。
  - 修复了一个Bug，该Bug曾导致：[数据库获取群聊列表](https://www.wechatsdk.com/docs/数据库/获取群聊列表.md)接口获取到的群聊不全，同时更新了[查询数据库](https://www.wechatsdk.com/docs/数据库/查询数据库.md)页面下的部分sql示例。
  - 修改了记录日志的参数，现在写入的内容会尽快可见。
  - 现在，在调用[cdn上传、cdn下载](https://www.wechatsdk.com/docs/CDN)接口时会尝试选择延迟最低的服务器。
  - [发送消息](https://www.wechatsdk.com/docs/发送消息)和[CDN](https://www.wechatsdk.com/docs/CDN)分类下的接口已支持一个`bAsync`参数，如果将该参数设置为true，则任务不再阻塞，接口响应内容会通过消息处理器返回，消息推送类型为0，同时，如果提供了`asyncUserData`参数（该参数不限定类型），会随调用结果一起推送。
  - 群聊事件推送进行了小幅度优化，添加了`subType`并将变更的成员和离开群聊的成员分开，此功能最近会尝试继续优化，以便监控自己的退群进群事件。
  - [cdn上传、cdn下载](https://www.wechatsdk.com/docs/CDN)的可选类型已更新并添加了补充说明。
  - ws服务器重启后前几条消息可能收不到，做了些优化可能会改善，但机制不能保证100%解决，最佳实践应该是避免重启服务器
  - 发布3.9.10版本的[1.0.5]()
- **05月29日**：
  - 尝试修复一个Bug，该Bug曾导致：个别电脑消息发送量大时出现消息阻塞的情况。（该现象与电脑配置有关）
  - 优化API:[检测链接是否被封禁](https://www.wechatsdk.com/docs/安全/检测链接是否被封禁.md)。
  - 发布3.9.10版本的[1.0.4.f3]()
- **05月27日**：
  - 修复了一个Bug，该Bug曾导致：个别电脑消息量大时出现[发送文本](https://www.wechatsdk.com/docs/发送消息/发送文本.md)消息阻塞的情况。
  - [下载朋友圈图片](https://www.wechatsdk.com/docs/朋友圈/下载朋友圈图片视频.md)文档整理。
  - 对于经常碰到的问题的API整理下了文档，关于如何接收消息请参考：[http消息处理器](https://www.wechatsdk.com/docs/处理消息/http处理器.md)下方的代码示例，如果是远程推送则推荐ws协议。
  - 发布3.9.10版本的[1.0.4.f2]()
- **05月24日**：
  - 修复了一个Bug，该Bug曾导致：调用[cdn下载](https://www.wechatsdk.com/docs/CDN/CDN下载.md)接口下载图片报错400。
  - [设置API访问秘钥](https://www.wechatsdk.com/docs/安全/设置API访问秘钥.md)接口所需参数名修改为newSecretKey，现在可以正确的取消访问秘钥。
  - [视频号作品解密接口](https://www.wechatsdk.com/docs/视频号/视频号作品解密.md)现在可以接受一个64位的decodeKey，可以用于解密朋友圈视频（含缩略图）、图片。
  - 发布3.9.10版本的[1.0.4.f1]()
- **05月20日**：
  - 新增[数据库获取联系人信息](https://www.wechatsdk.com/docs/数据库/获取联系人信息.md)接口，支持传入列表以获取多个联系人信息，同时可以指定群id，此时会尝试匹配成员在群内的信息。
  - 新增[数据库获取群聊信息](https://www.wechatsdk.com/docs/数据库/获取群聊信息.md)接口。
  - 新增[数据库获取群聊列表](https://www.wechatsdk.com/docs/数据库/获取群聊列表.md)接口，群很多的话可能会比较慢。
  - 新增群聊事件推送（新成员进群、退群、群成员修改群内昵称），该功能默认不启动，可以使用[群聊信息变更通知接口](https://www.wechatsdk.com/docs/群管理/开启-关闭群聊信息变更通知.md)进行开关。
  - 收到群消息时，现在会尝试匹配群成员的群内昵称一起推送。
  - 获取[群成员详细信息](https://www.wechatsdk.com/docs/群管理/获取群成员详细信息.md)接口，新增version参数，默认为0（获取所有信息），可以通过数据库获取群聊信息接口获取本地version。
  - [转换wxgf文件接口](https://www.wechatsdk.com/docs/表情包/转换wxgf文件.md)优化，现在会按照jpg->png->gif的顺序尝试解码，此项更改已同步应用到cdn下载中。
  - 发布3.9.10版本的[1.0.4]()
- **05月16日**：
  - 整理API文档目录，新增[安全](https://www.wechatsdk.com/docs/安全)目录
  - 解决已知机型启动微信失败问题
  - 发布3.9.10版本的[1.0.3]()
- **05月13日**：
  - 登录过程中推送二维码事件（扫描、确认、取消、过期），如有验证码，会在扫描事件中推送。
  - 修复Bug：启用防撤回会导致下载文件不会正常结束并且自己也无法撤回消息。
  - [设置API访问密钥](https://www.wechatsdk.com/docs/其他功能/设置API访问秘钥.md)修改参数
  - 解决登录过程中可能出现的崩溃问题。
  - 支持win11、arm等系统
  - 新增[发送企业用户名片](https://www.wechatsdk.com/docs/发送消息/发送企业用户名片.md)接口
  - 发布3.9.10版本的[1.0.2]()
- **05月07日**：
  - 全面支持3.9.10版本，全量API兼容，公测中
  - 支持win11、arm等系统
  - 发布3.9.10版本的[1.0.1]()
- **04月29日**：
  - 增加[发送公众号名片](https://www.wechatsdk.com/docs/发送消息/发送公众号名片.md)
  - 增加[发送视频号名片](https://www.wechatsdk.com/docs/发送消息/发送视频号名片.md)
  - 增加[发送视频号消息](https://www.wechatsdk.com/docs/发送消息/发送视频号消息.md)
  - 增加[打语音](https://www.wechatsdk.com/docs/发送消息/音视频聊天(发起).md)，只能用作提醒，对方接听后会自动挂断
  - 增加[打视频](https://www.wechatsdk.com/docs/发送消息/音视频聊天(挂断).md)，只能用作提醒，对方接听后会自动挂断
  - 增加[TCP服务器](https://www.wechatsdk.com/docs/处理消息/TCP处理器.md)
  - 增加[消息变已读](https://www.wechatsdk.com/docs/处理消息/消息设置为已读.md)
  - 增加[消息变未读](https://www.wechatsdk.com/docs/处理消息/消息设置为未读.md)
  - 增加[打开小程序](https://www.wechatsdk.com/docs/小程序/打开小程序.md)
  - 增加[打开浏览器](https://www.wechatsdk.com/docs/其他功能/打开浏览器.md)
  - 增加[获取H5Key](https://www.wechatsdk.com/docs/公众号/获取H5Key.md)
  - 增加[获得热点视频](https://www.wechatsdk.com/docs/视频号/获取热点视频.md)
  - 增加[设置API访问密钥](https://www.wechatsdk.com/docs/其他功能/设置API访问秘钥.md)
  - 增加[转化wxgf文件](https://www.wechatsdk.com/docs/表情包/转换wxgf文件.md)
  - 增加新的启动方式，不再依赖启动器了
  - 修复bug：登录失败时会导致微信退出
  - 发布新版本[1.1.10]()
- **04月22日**：
  - **解决版本过低无法登录的提示问题**
  - 1.1.8版本的api部分用户测试中，当前较为稳定
  - 发布了版本[1.1.9]()
- **04月18日**：
  - 增加了一些新功能api，目前只有部分用户有用到，待反馈后补充API文档
  - 发布了版本[1.1.8]()
- **04月11日**：
  - 代码优化，修复了一些bug
  - 稳定性优化
  - 发布了版本[1.1.7]()
- **04月03日**：
  - 修了一堆偶发的bug，具体修复了什么也记不起来了（因为要下班了）
  - 优化了一版代码
  - 微信风控策略又加强了一版，也加强了防封策略、主动诱导策略强化了一版
  - 发布了版本[1.1.6]()
- **03月25日**：
  - 对WechatAPI的文档结构进行了调整
  - [查找附近的人](https://www.wechatsdk.com/docs/社交/获取附近的人.md)现在可以使用经纬度来查询附近的人
  - 现在支持[添加附近的人](https://www.wechatsdk.com/docs/通讯录/添加好友.md)
  - 现在支持获取[公众号历史推送文章](https://www.wechatsdk.com/docs/公众号/获取历史推送消息.md)
  - 现在支持[收款码收款提醒](https://www.wechatsdk.com/docs/处理消息/http处理器.md)
  - 发布了版本[wechatAPI_1.1.5]()
- **03月19日**：
  - 对API文档进行了更新
  - 修复了部分API接口对企业微信好友不友好的问题
  - 新增了API：[企业好友信息](https://www.wechatsdk.com/docs/通讯录/获取企业用户信息.md)
  - 发布了版本[wechatAPI_1.1.4]()
- **03月13日**：
  - 更新了使用手册
  - 修复了部分API接口偶尔不能使用的问题
  - 发布了朋友圈API并增加了防识别扰乱参数：[发布朋友圈](https://www.wechatsdk.com/docs/朋友圈/发布朋友圈.md)，请谨慎使用，部分账号可能会触发风控
  - 发布了版本[wechatAPI_1.1.3.f2]()，增强了防封策略，加入了主动扰乱识别机制。
- **03月06日**：
  - 更新了使用手册
  - 更新了文档，增加了更多示例：[获取所有好友列表](https://www.wechatsdk.com/docs/通讯录/获取所有好友列表.md)
  - 新增了API：[获取企业用户信息](https://www.wechatsdk.com/docs/通讯录/获取企业用户信息.md)
  - 新增了API：[获取群列表](https://www.wechatsdk.com/docs/群管理/获取所有群列表.md)
  - 新增了文档：[微信数据库简述](https://www.wechatsdk.com/docs/数据库/微信数据库简述.md)
  - 发布了版本:[wechatAPI_1.1.3]()，优化了防封机制，增加了避免被识别的机制。
- **02月21日**：
  - 更新了使用手册
  - 不再支持ARM系统（如打开启动器后乱码，则表示不支持）
  - 新增了[获取所有好友列表](https://www.wechatsdk.com/docs/通讯录/获取所有好友列表.md)
- **02月18日**：
  - 开工大吉！
  - 发布了修复版:[1.1.2.f1]()，解决了启动器由于电脑因弱网环境崩溃问题，增加了已知避免被识别的机制。
  - 修复了[微信防撤回通知](https://www.wechatsdk.com/docs/其他功能/开启关闭防撤回.md)接口偶尔不能使用的问题。
  - 新增了[删除单个消息回调处理器](https://www.wechatsdk.com/docs/处理消息/移除处理器.md)接口
- **02月04日**：
  - 修复了[添加群成员到通讯录](https://www.wechatsdk.com/docs/群管理/添加群成员到通讯录.md)接口偶尔出现的异常
  - 更新了[发送语音条](https://www.wechatsdk.com/docs/发送消息/发送语音.md)接口文档，功能没有变更
  - 年前最后一次更新，祝大家新年快乐
- **01月31日**：
  - 新增了[转发图片.md](https://www.wechatsdk.com/docs/发送消息/转发图片.md)接口。
  - 新增了[转发文件.md](https://www.wechatsdk.com/docs/发送消息/转发文件.md)接口。
  - 新增了[转发视频.md](https://www.wechatsdk.com/docs/发送消息/转发视频.md)接口。
  - 新增了[转发语音.md](https://www.wechatsdk.com/docs/发送消息/转发语音.md)接口。
  - 通过好友申请接口新增了scene字段，可以从消息xml中获取。
  - 发布了版本:1.1.2
- **01月24日**：
  - 添加了[开启/关闭防撤回](https://www.wechatsdk.com/docs/其他功能/开启关闭防撤回.md)接口。监听到撤回消息时，会将原消息内容一起推送
  - 新增了[文本翻译](https://www.wechatsdk.com/docs/其他功能/文本翻译.md)接口。
- **1月03日**：
  - 准备发朋友圈接口xml示例 xml详见：[点击查看](https://github.com/WeChatApis/wechatSDK)
  - 准备发送小程序xml示例

### 2023年

- **12月23日**：
  - 后续不再持续支持3.9.2.*版本的新api。现有api将持续支持，有bug会修复。
  - 修复了[视频号作品解密](https://www.wechatsdk.com/docs/视频号/视频号作品解密.md)
  - 新增了[发送视频.md](https://www.wechatsdk.com/docs/发送消息/发送视频.md)
  - 新增了[发送链接.md](https://www.wechatsdk.com/docs/发送消息/发送链接.md)
- **11月24日**：
  - [获取用户信息](https://www.wechatsdk.com/docs/通讯录/获取用户信息.md)接口新增了字段，支持通过群聊获取用户信息。
  - 新增了[添加群成员到通讯录](https://www.wechatsdk.com/docs/群管理/添加群成员到通讯录.md)接口。
  - 新增了[WebSocket处理器](https://www.wechatsdk.com/docs/处理消息/WebSocket处理器.md)
  - 新增了[获取消息处理器列表](https://www.wechatsdk.com/docs/处理消息/获取消息处理器列表.md)接口。
  - 新增了[退出登录](https://www.wechatsdk.com/docs/登录相关/退出登录.md)接口。
  - 消息推送与主动调用格式进行了优化。
  - 修复了多线程调用时的Bug。
  - 对[获取个人信息](https://www.wechatsdk.com/docs/个人信息/获取个人信息.md)接口进行了优化。
- **11月11日**：
  - 优化了退出事件监听。
  - 优化了消息推送。
  - 新增了点对点消息处理器。
  - 新增了一种接口调用方式。
  - 优化了python示例代码。
- **9月19日**：
  - 修复了发送文本消息导致微信崩溃的Bug。
- **9月14日**：
  - 过滤掉部分主动发送消息的推送。
  - 修复了邀请加入群聊接口导致的Bug。
  - 修复了x64版本在初始化登录时调用接口无返回的Bug。
  - 通过接口发送的文本消息现在会显示到微信客户端。
  - 优化了登录事件推送。
  - 优化了添加好友接口。
- **9月6日**：
  - 支持了主动发送消息的推送。
  - 新增了邀请加入群聊接口。
  - 新增了群聊邀请验证接口。
- **8月28日**：
  - 修改了HttpServer逻辑，解决了并发调用报错的问题。
  - 获取小程序code接口编号发生了变更。
  - 锁定微信接口编号发生了变更。
  - 小程序授权接口编号发生了变更。
  - 新增了操作云函数接口。
  - 新增了刷新小程序会话接口。
  - 新增了获取小程序使用记录接口。
  - 新增了更新小程序使用记录接口。
  - 新增了获取小程序信息接口。
  - 新增了批量获取小程序信息接口。
  - 新增了获取小程序包下载地址接口。
  - 解除了虚拟机不可用的限制。
- **8月15日**：
  - 修复了cdn下载接口下载文件不完整的Bug。
  - 更新了3.9.5.8164位版本SDK。
- **8月10日**：
  - 修复了3.9.5.81版本调用任意接口后触发微信重新登录的Bug。
  - 修复了删除群成员接口无效的Bug。
  - 修复了关闭群聊免打扰接口无效的Bug。
  - 修复了保存收款码接口无效或引发微信崩溃的Bug。
  - 修复了3.9.5.81版本部分接口调用失败的Bug。
  - 修复了查询数据库接口执行错误sql后的Bug。
  - 新增了小程序授权接口。
  - 新增了锁定微信接口。
- **7月20日**：
  - 开放了一系列视频号相关接口。
  - 开放了获取小程序code接口。
  - 尝试修复了获取通讯录接口卡死的Bug。
  - 调整了文档结构。
- **7月9日**：
  - 修复了搜一搜接口设置的偏移无效的Bug。
  - 优化了获取数据库信息接口。
  - 开放了数据库备份接口。
- **7月6日**：
  - 新增了注入时自动patch掉微信的检查更新功能。
  - 新增了获取H5Key接口。
  - 新增了获取数据库信息接口。
  - 新增了查询数据库接口。
- **6月30日**：
  - 解决了cdn下载接口报错的问题。
- **6月29日**：
  - 获取用户信息接口添加了remark字段。
  - 优化了批量获取用户信息接口。
  - 修复了http服务崩溃的Bug。
 
**官网**
[官方网站](https://www.wechatsdk.com/)
