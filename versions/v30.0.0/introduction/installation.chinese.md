---
标题: 安装指南
---

开发 Expo 应用程序你需要两种工具：一种本地开发工具和一种可以打开你的应用的手机客户端。

## 本地开发工具: Expo CLI

Expo CLI 是开发Expo应用程序的工具。除了命令行界面（CLI）它也有一个图形用户界面，可以在你的web浏览器里弹出。通过Expo开发者工具你可以快速设置您的测试设备,查看日志等等。

您的电脑需要安装有Node（版本>=6）,[下载最新Node.js版本](https://nodejs.org/en/).

通过运行如下代码安装Expo CLI:

```
npm install -g expo-cli
```

## 手机客户端: Expo 对应 iOS 和 Android

Expo客户端帮助您查看正在开发中的项目。当您通过Expo CLI部署启动您的项目时，它会生成一个开发地址URL，您可以通过Expo客户端打开这个地址预览您的应用程序。
在Android手机上，您也可以通过Expo客户端浏览其他人[expo.io](https://expo.io)的项目。Expo客户端工作在设备、模拟器和仿真器上。

### 在您的设备上

[Android用户从Google Play Store上下载](https://play.google.com/store/apps/details?id=host.exp.exponent) or [iOS 用户可以到 App Store下载](https://itunes.com/apps/exponent)

> **要求 Android 和 iOS 最低版本配置:** Expo在 Android中最低支持 Android4.4,IOS 最低版本iOS 9.0。

您不需要去手动安装Expo客户端在您的仿真器和模拟器上，因为Expo CLI在安装的过程中会为您自动完成这些操作。详情见本指南下一章节。

### iOS 模拟器

安装[Xcode 通过 the Apple App Store](https://itunes.apple.com/app/xcode/id497799835). 这可能需要一段时间，去打个盹吧。下一步，打开Xcode，打开偏好选项卡并且从列表中选择一个模拟器进行安装。

启动一个模拟器并在Expo开发工具中启动一个项目，如此在工具中您点击 _Run on iOS simulator_ 运行工程，它将安装Expo客户端到您的模拟器中并且在当前客户端启动您的app。

> **不能工作?** Expo CLI 在自动安装Expo客户端方面偶尔会出现问题，通常是由于您的环境与Xcode存在微小的差异。如果您需要手动的安装Expo客户端到您的模拟器，您可以跟着如下步骤进行操作：
>
> - 下载 [最新的 simulator 构建程序](http://expo.io/--/api/v2/versions/download-ios-simulator-build).
> - 抽象这个过程如下:
    `mkdir Exponent-X.XX.X.app && tar xvf Exponent-X.XX.X.tar.gz -C Exponent-X.XX.X.app`. 你应该可以得到类似 `Exponent-X.XX.X.app`这样的目录文件。
> - 确定模拟器是在运行的.
> - 启动一个终端, 运行如下代码 `xcrun simctl install booted [path to Exponent-X.XX.X.app]`.

### Android 模拟器

跟着 [Android Studio emulator guide](../workflow/android-studio-emulator.html) 启动Android工具和创建一个虚拟机设备， 准备好之后启动这个虚拟机设备。

启动设备并且在Expo开发工具中启动一个项目, 在Expo开发工具中您可以按下 _Run on Android device/emulator_ ，这一操作构建完成会自动安装Expo客户端到您的模拟器，并且在其内部启动当前应用程序。

## Watchman

一些 macOS 用户遭遇问题时，没有安装Watchman在他们的机器上，因此我们推荐您安装，因此可以监测问题发生。Watchman监测文件和记录的改变，然后触发这一行为的反应，一般被使用在React Native的内部。[下载 和 安装 Watchman](https://facebook.github.io/watchman/docs/install.html).
