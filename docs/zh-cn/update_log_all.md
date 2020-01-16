## 2019.03.04
### 重点更新
* [iOS-update] 升级适配 WeexSDK 0.21.0 版本；
* [iOS-update] 基础库（ErosPluginBaseLibrary）更新 1.3.5 版本;

 >  说明：由于 Android 新版本 WeexSDK 变化较大，升级需要修改的地方过多，请再给小哥哥一些时间，迟一些发布更新；

### iOS 升级
编辑 Podfile 修改 `WeexSDK`、`WXDevtool`、`ErosPluginBaseLibrary` 三个库的引用

```ruby
#WeexSDK
pod 'WeexSDK', :git => 'https://github.com/bmfe/incubator-weex.git'
#Weex debugger 调试工具，只在开发模式集成
pod 'WXDevtool', :git => 'https://github.com/bmfe/weex-devtool-iOS.git', :configurations => ['Debug']
#Eros iOS 基础库
pod 'ErosPluginBaseLibrary', :git => 'https://github.com/bmfe/eros-plugin-ios-baseLibrary.git', :tag => '1.3.5'
```
2.执行 `pod update` 拉取新版本依赖；

## 2018.11.23
### 重点更新
* [iOS-update] 解决WeexSDK 与 微信SDK`WXLogLevel`命名冲突问题，请按下面的方式修复WeexSDK依赖方式，继续；
* [iOS-update] 基础库（ErosPluginBaseLibrary）更新 1.3.4 版本，1.优化App启动逻辑，避免热更新时重复初始化Weex环境；2.解决BMEvent `off` 方法不能取消监听事件的问题；
* [iOS-教程] 升级 Xcode 10后会编译报错，请参考这篇文章来解决相关问题；[请戳这里](https://www.jianshu.com/p/6d94278d62b3)
* WeexSDK 0.19.0 更新内容 [请戳这里](https://github.com/apache/incubator-weex/releases) <br>

 >  说明：由于 Android 新版本 WeexSDK 变化较大，升级需要修改的地方过多，请再给小哥哥一些时间，迟一些发布更新；

### iOS 升级
1.修改 WeexSDK 依赖Eros仓库版本 0.19 <br>
2.修改 ErosPluginBaseLibrary 基础库为 1.3.4 版本

```ruby
# 其他依赖库不用修改
pod 'WeexSDK', :git => 'https://github.com/bmfe/WeexiOSSDK.git', :tag => '0.19'
pod 'ErosPluginBaseLibrary', :git => 'https://github.com/bmfe/eros-plugin-ios-baseLibrary.git', :tag => '1.3.4'
```
2.执行 `pod update` 拉取新版本依赖；

## 2018.11.14
### 重点更新
* [iOS-update] 适配WeexSDK 0.19.0版本，基础库（ErosPluginBaseLibrary）更新 1.3.3 版本；
* [iOS-教程] 升级 Xcode 10后会编译报错，请参考这篇文章来解决相关问题；[请戳这里](https://www.jianshu.com/p/6d94278d62b3)
* WeexSDK 0.19.0 更新内容 [请戳这里](https://github.com/apache/incubator-weex/releases) <br>

 >  说明：由于 Android 新版本 WeexSDK 变化较大，升级需要修改的地方过多，请给小哥哥一些时间，迟一些发布更新；

### iOS 升级
1.修改 WeexSDK 依赖版本 0.19.0 <br>
2.修改 ErosPluginBaseLibrary 基础库为 1.3.3 版本

```ruby
# 其他依赖库不用修改
pod 'WeexSDK', '0.19.0'
pod 'ErosPluginBaseLibrary', :git => 'https://github.com/bmfe/eros-plugin-ios-baseLibrary.git', :tag => '1.3.3'
```
2.执行 `pod update` 拉取新版本依赖；

## 2018.10.11
### 重点更新
* [iOS-bugfix] 修复拓展的上拉加载更多loadMore事件与weex默认的loadmore事件冲突的问题；感谢 陈远•Frank，M、的贡献，[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/base_extend?id=上拉加载更多)
* [iOS-bugfix] 修复iPhoneX的判断方法；感谢 Shawn唐的贡献；
* [iOS-bugfix] 修复使用Xcode10开发并运行在iOS12系统上设置导航栏背景色无效的问题；
* [iOS-bugfix] 解决使用`bmBundleUpdate`module进行热更新，当解压缩失败时没有回调callback的问题；
* [iOS-optimize] 网络请求一些代码优化；
* [iOS-update] 基础库包名已修改（ErosPluginBaseLibrary）；
* [iOS-教程] 升级 Xcode 10后会编译报错，请参考这篇文章来解决相关问题；[请戳这里](https://www.jianshu.com/p/6d94278d62b3)
* [Android-update] 基础库包名已修改（所有 com.benmu 的包名均修改成 com.eros）；

### iOS 升级
1.升级 ErosPluginBaseLibrary 基础库为 1.3.2 版本

```ruby
pod 'ErosPluginBaseLibrary', :git => 'https://github.com/bmfe/eros-plugin-ios-baseLibrary.git', :tag => '1.3.2'
```
2.执行 `pod update` 拉取新版本依赖；

### Android 升级
1、模板代码修改 `/platforms/android/WeexFrameworkWrapper/app/src/main/AndroidManifest.xml`文件[参考此文件](https://github.com/bmfe/eros-template/blob/master/platforms/android/WeexFrameworkWrapper/app/src/main/AndroidManifest.xml)。<br/> 其他 `com.eros.wx（老包 是 com.benmu.wx）` 包下 文件也需要对应修改[参考此目录](https://github.com/bmfe/eros-template/tree/master/platforms/android/WeexFrameworkWrapper/app/src/main/java/com/eros/wx)。

> 如果您已经自己修改包名 则不需要 修改 模板里的代码。 只需要更新库目录下的代码即可

2、其他库目录可 直接 切换到 一下`tag`， 如并未使用tag 可直接 `git pull `获取最新代码即可。
```
nexus 1.1.0
wxframework 1.1.1
erospluginwxshare 1.1.2
erospluginwxpay 1.1.2
erosplugingt 1.1.1
```

3、 如果有对eros 代码做深度定制开发的同学 升级遇到什么问题可以群里直接 @jony


## 2018.09.06
### 重点更新
* [bugfix]友盟分享接口，添加`userName`字段，分享至小程序需要传入此值；
* [feature]友盟统计新增自定义事件统计；[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/plugin_umAnalytics)
* [feature]更新Umeng 库。
* [feature]安卓添加虚拟按键高度全局属性 virtualButtonsHeight
* [bugfix]input组件，type为number时不能输入小数点
* [bugfix]安卓安全漏洞
* [bugfix]修复微信支付模块 isInstallWXApp方法无效问题.
* [bugfix]修复判断前后台方法错误问题.

### iOS 升级
1.升级 ErosPluginUMAnalytics 库为 1.0.1 版本；
2.升级 ErosPluginWXShare 库为 1.0.5 版本；

```ruby
pod 'ErosPluginUMAnalytics', :git => 'https://github.com/bmfe/eros-plugin-ios-UMAnalytics.git', :tag => '1.0.1'
pod 'ErosPluginWXShare', :git => 'https://github.com/bmfe/eros-plugin-ios-wxshare.git', :tag => '1.0.5'
```
2.执行 `pod update` 拉取新版本依赖；

### Android 升级
进入 `/platforms/android/WeexFrameworkWrapper/nexus` 目录 切换tag 到 1.0.9 <br>
进入`/platforms/android/WeexFrameworkWrapper/wxframework` 目录 切换tag 到1.1.0 <br>
进入 `/platforms/android/WeexFrameworkWrapper/erospluginum` 目录 切换tag 到 1.0.1 <br>
进入 `/platforms/android/WeexFrameworkWrapper/erospluginwxpay` 目录 切换tag 到 1.1.1 <br>
进入 `/platforms/android/WeexFrameworkWrapper/erospluginumeng` 目录 切换tag 到 1.1.1 <br>

> 如果您没有使用tag控制版本，可以直接 git pull 更新下github 上代码即可。如果您并没有使用到这些插件则不需要切换tag或者git pull

由于更新了 umeng相关库，以及修复一些安全漏洞同时对模板也做了一些修改，请对应修改一下文件。
1. com.benmu.wx.wxapi  包 目录下的 `WXEntryActivity` 和 `WXPayEntryActivity`
2. `/platforms/android/WeexFrameworkWrapper/app/src/main/AndroidManifest.xml` 

> 如果您并没有对这些文件做修改可以直接 下载文件覆盖即可。


## 2018.08.02
### 重点更新
* [bugfix-iOS]`<web>`标签加载`bmlocal`资源报错的问题；
* [feature]`bmNavigator` module 添加隐藏状态栏功能；[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/eros_sdk_module?id=bmnavigator)
* [feature]`bmBundleUpdate` module 添加获取 JSVersion 方法；[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/eros_sdk_module?id=bmbundleupdate)
* [optimize]`bmchart`component 支持加载自定义 html 文件；[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/eros_sdk_component?id=图表组件)

### iOS 升级
1.升级 BMBaseLibrary 基础库为 1.3.0 版本

```ruby
pod 'ErosPluginBaseLibrary', :git => 'https://github.com/bmfe/eros-plugin-ios-baseLibrary.git', :tag => => '1.3.0'
```
2.执行 `pod update` 拉取新版本依赖；

### Android 升级
进入 `/platforms/android/WeexFrameworkWrapper/nexus` 目录 切换tag 到 1.0.8 <br>
进入`/platforms/android/WeexFrameworkWrapper/wxframework` 目录 切换tag 到1.0.9 。

> 如果您没有使用tag控制版本，可以直接 git pull 更新下github 上代码即可。

## 2018.07.26
### 重点更新
* [bugfix-Android]`tabbar` 多页面 `watchIndex` 只有一个生效问题
* [bugfix-Android]`tabbar` 生命周期触发不正常问题。
* [bugfix-Android]`tabbar` 设置 Navigator 会设置多个`tab`问题
* [bugfix-Android] 提交google play收到SSL Error Handler错误问题添加文档说明。[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/QA?id=q-android-%E6%8F%90%E4%BA%A4google-play%E6%94%B6%E5%88%B0ssl-error-handler%E9%94%99%E8%AF%AF)
* [bugfix-Android] 解决部分页面内存泄漏问题
* [bugfix-Android] 优化图片加载过多 的OOM 问题。
* [bugfix-Android] `web`标签通过url传参参数丢失问题；
* [bugfix-iOS] `web`标签通过url传参参数丢失问题；
* [bugfix-iOS] 微信分享插件、微信支付插件判断是否安装微信方法无效的问题（请升级最新版本）；
* [optimize-iOS] 优化 `bmChart` 加载本地js资源的方法；


### iOS 升级
1.升级 BMBaseLibrary 基础库为 1.2.9 版本

```ruby
pod 'ErosPluginBaseLibrary', :git => 'https://github.com/bmfe/eros-plugin-ios-baseLibrary.git', :tag => => '1.2.9'
```
2.执行 `pod update` 拉取新版本依赖；

3.使用微信支付或微信分享的用户请分别升级插件库到最新版本；

### Android 升级
进入 `/platforms/android/WeexFrameworkWrapper/nexus` 目录 切换tag 到 1.0.7 <br>
进入`/platforms/android/WeexFrameworkWrapper/wxframework` 目录 切换tag 到1.0.8 。

> 如果您没有使用tag控制版本，可以直接 git pull 更新下github 上代码即可。


## 2018.07.18
### 重点更新
* [bugfix-Android]`input`标签动态切换`type = password`不生效；
* [bugfix-Android]从后台进入app、tabbar上所有页面都会触发生命周期，应该只有当前显示的页面触发；
* [bugfix-Android]`image`标签动态设置高度图片变形；
* [bugfix-Android]加载本地`html`参数丢失的问题；
* [bugfix-iOS]加载本地`html`参数丢失的问题；
* [bugfix-iOS]`mediator.js`中使用`bmRouter`跳转页面无效;
* [feature]`bmTabbar` 新增监听切换页面方法、获取当前下标方法、及动态修改tabbar配置信息。[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/eros_sdk_module?id=bmTabbar)；
* [feature-Android]更新`jsbundle`添加弹窗提示，行为保持跟iOS一致；
* [feature]新增`bmBundleUpdate`module，开发者可以自定义更新`jsbundle`逻辑。[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/eros_sdk_module?id=bmBundleUpdate)；
* [feature]`weex.config.eros`中添加`tabbarHeight`原生`TabBar`高度参数；
* [feature]`bmImage`module 新增 `scanImage()`方法，识别图片二维码。[文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/eros_sdk_module?id=bmimage)；感谢 [scholar-ink](https://github.com/scholar-ink)提供pr；
* [feature]`bmRouter`module 添加 `claerHomePage()` 方法清楚之前设置的首页;
* [feature]新增友盟统计插件。[使用文档请戳](https://bmfe.github.io/eros-docs/#/zh-cn/plugin_umAnalytics)

### iOS 升级
1.升级 BMBaseLibrary 基础库为 1.2.8 版本

```ruby
pod 'ErosPluginBaseLibrary', :git => 'https://github.com/bmfe/eros-plugin-ios-baseLibrary.git', :tag => => '1.2.8'
```
2.执行 `pod update` 拉取新版本依赖；

### Android 升级
进入 `/platforms/android/WeexFrameworkWrapper/nexus` 目录 切换tag 到 1.0.6 <br>
进入`/platforms/android/WeexFrameworkWrapper/wxframework` 目录 切换tag 到1.0.7 。

> 如果您没有使用tag控制版本，可以直接 git pull 更新下github 上代码即可。
