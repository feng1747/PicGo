<div align="center">
  <img src="https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/New%20LOGO-150.png" alt="">
  <h1>PicGo</h1>
  <blockquote>图片上传+管理新体验 </blockquote>
  <a href="https://github.com/Molunerfinn/PicGo/actions">
    <img src="https://img.shields.io/badge/code%20style-standard-green.svg?style=flat-square" alt="">
  </a>
  <a href="https://github.com/Molunerfinn/PicGo/actions">
    <img src="https://github.com/Molunerfinn/PicGo/actions/workflows/main.yml/badge.svg" alt="">
  </a>
  <a href="https://github.com/Molunerfinn/PicGo/releases">
    <img src="https://img.shields.io/github/downloads/Molunerfinn/PicGo/total.svg?style=flat-square" alt="">
  </a>
  <a href="https://github.com/Molunerfinn/PicGo/releases/latest">
    <img src="https://img.shields.io/github/release/Molunerfinn/PicGo.svg?style=flat-square" alt="">
  </a>
  <a href="https://github.com/PicGo/bump-version">
    <img src="https://img.shields.io/badge/picgo-convention-blue.svg?style=flat-square" alt="">
  </a>
</div>

## 应用概述

**PicGo: 一个用于快速上传图片并获取图片 URL 链接的工具**

PicGo 本体支持如下图床：

- `七牛图床` v1.0
- `腾讯云 COS v4\v5 版本` v1.1 & v1.5.0
- `又拍云` v1.2.0
- `GitHub` v1.5.0
- `SM.MS V2` v2.3.0-beta.0
- `阿里云 OSS` v1.6.0
- `Imgur` v1.6.0

**本体不再增加默认的图床支持。你可以自行开发第三方图床插件。详见 [PicGo-Core](https://picgo.github.io/PicGo-Core-Doc/)**。

## 特色功能

- 支持拖拽图片上传
- 支持快捷键上传剪贴板里第一张图片
- Windows 和 macOS 支持右键图片文件通过菜单上传 (v2.1.0+)
- 上传图片后自动复制链接到剪贴板
- 支持自定义复制到剪贴板的链接格式
- 支持修改快捷键，默认快速上传快捷键：`command+shift+p`（macOS）| `control+shift+p`（Windows\Linux)
- 支持插件系统，已有插件支持 Gitee、青云等第三方图床
  - 更多第三方插件以及使用了 PicGo 底层的应用可以在 [Awesome-PicGo](https://github.com/PicGo/Awesome-PicGo) 找到。欢迎贡献！
- 支持通过发送 HTTP 请求调用 PicGo 上传（v2.2.0+)
- 更多功能等你自己去发现，同时也会不断开发新功能
  - 开发进度可以查看 [Projects](https://github.com/Molunerfinn/PicGo/projects)，会同步更新开发进度
  - 欢迎加入 [官方讨论区](https://github.com/Molunerfinn/PicGo/discussions) 与我交流

**如果第一次使用，请参考应用 [使用文档](https://picgo.github.io/PicGo-Doc/zh/guide/getting-started.html)。遇到问题了还可以看看 [FAQ](https://github.com/Molunerfinn/PicGo/blob/dev/FAQ.md) 以及被关闭的 [issues](https://github.com/Molunerfinn/PicGo/issues?q=is%3Aissue+is%3Aclosed)。**

## 下载安装

点击此处下载 [应用](https://github.com/Molunerfinn/PicGo/releases)。从 2.3.1-beta.4 版本开始，在下载页提供 [腾讯云COS](https://cloud.tencent.com/product/cos) 下载链接，供国内用户快速下载使用。感谢 [腾讯云COS](https://cloud.tencent.com/product/cos) 提供的赞助支持！

还可以通过山东大学镜像站提供的镜像地址下载 [应用](https://mirrors.sdu.edu.cn/github-release/Molunerfinn_PicGo)。感谢山东大学镜像站提供的镜像服务！

### Windows

Windows 用户请下载最新版本的 `exe` 文件。

**还可以使用 [Scoop](https://scoop.sh/) 来安装 PicGo: `scoop bucket add helbing https://github.com/helbing/scoop-bucket` & `scoop install picgo`。 感谢 @helbing 的贡献！**

**还可以使用 [Chocolatey](https://chocolatey.org/) 来安装 PicGo: `choco install picgo`。 感谢 @iYato 的贡献！**

### macOS

macOS 用户请下载最新版本的 `dmg` 文件。

**还可以使用 [Homebrew](https://brew.sh/) 来安装 PicGo: `brew install picgo --cask`。感谢 @womeimingzi11 的贡献！**

### Linux

Linux 用户请下载 `AppImage` 文件。

**如果你是 Arch 类的 Linux 用户，可以直接通过 `yay -S picgo-appimage` 来安装 PicGo （若是没有则先安装 yay ，是 aur 仓库助手）。感谢 @houbaron 的贡献！**

## 应用截图

![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/picgo-2.0.gif)

![picgo-menubar](https://user-images.githubusercontent.com/12621342/34242310-b5056510-e655-11e7-8568-60ffd4f71910.gif)

## 开发说明

> 目前仅针对 Mac、Windows。Linux 平台并未测试。

如果你想要学习、开发、修改或自行构建 PicGo，可以依照下面的指示：

> 如果想学习 Electron-vue 的开发，可以查看我写的系列教程——[Electron-vue 开发实战](https://molunerfinn.com/tags/Electron-vue/)

1. 你需要有 Node、Git 环境，了解 npm 的相关知识。
2. `git clone https://github.com/Molunerfinn/PicGo.git` 并进入项目。
3. `yarn` 下载依赖。注意如果你没有 `yarn`，请去 [官网](https://classic.yarnpkg.com/en/docs/install) 下载安装后再使用。 **用 `npm install` 将导致未知错误！**
4. Mac 需要有 Xcode 环境，Windows 需要有 VS 环境。

### 开发模式

输入 `npm run electron:serve` 进入开发模式，开发模式具有热重载特性。不过需要注意的是，开发模式不稳定，会有进程崩溃的情况。此时需要：

```bash
ctrl+c # 退出开发模式
npm run electron:serve # 重新进入开发模式
```

**注：Windows 开发模式运行之后会在底部任务栏的右下角应用区出现 PicGo 的应用图标。**

### 生产模式

如果你需要自行构建，可以 `npm run electron:build` 开始进行构建。构建成功后，会在 `dist_electron` 目录里出现构建成功的相应安装文件。

**注意**：如果你的网络环境不太好，可能会出现 `electron-builder` 下载 `electron` 二进制文件失败的情况。这个时候需要在 `npm run electron:build` 之前指定一下 `electron` 的源为国内源：

```bash
export ELECTRON_MIRROR="https://npmmirror.com/mirrors/electron/"
# 在 Windows 上，则可以使用 set ELECTRON_MIRROR=https://npmmirror.com/mirrors/electron/ （无需引号）
npm run electron:build
```

只需第一次构建的时候指定一下国内源即可。后续构建不需要特地指定。二进制文件下载在 `~/.electron/` 目录下。如果想要更新 `electron` 构建版本，可以删除 `~/.electron/` 目录，然后重新运行上一步，让 `electron-builder `去下载最新的 `electron` 二进制文件。

## 其他相关

- [vs-picgo](https://github.com/PicGo/vs-picgo)：PicGo 的 VS Code 版。
- [flutter-picgo](https://github.com/PicGo/flutter-picgo)：PicGo 的手机版（支持 Android 和 iOS ）。

## 赞助

如果你喜欢 PicGo 并且它对你确实有帮助，欢迎给我打赏一杯咖啡哈~

支付宝：

![](https://user-images.githubusercontent.com/12621342/34188165-e7cdf372-e56f-11e7-8732-1338c88b9bb7.jpg)

微信：

![](https://user-images.githubusercontent.com/12621342/34188201-212cda84-e570-11e7-9b7a-abb298699d85.jpg)

## License

[MIT](http://opensource.org/licenses/MIT)

Copyright (c) 2017 - 2019 Molunerfinn
