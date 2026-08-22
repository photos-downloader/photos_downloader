---
title: 图形界面
description: Flutter GUI 如何选择厂商并启动下载。安装包尚未发布。
---

Photos Downloader GUI 是 Flutter 应用，通过 Rust FFI 调用各厂商下载器。安装包**尚未发布**。

## 预期流程

1. 打开应用，选择云厂商卡片。
2. 仅 **iCloud** 与 **HUAWEI Cloud** 标记为可用；其余为开发中。
3. 填写本地下载目录。
4. iCloud：输入 Apple ID，完成 2FA；session 默认写到 `~/.photos_downloader/icloud/`。
5. 华为：选择浏览器导出的 `cookies.json`。
6. 选择仅下载或下载并删除云原件，设置 `--recent`、跳过视频、dry-run。
7. 开始下载并查看进度。

GUI 不会把密码或 cookie 上传到 Photos Downloader 的服务器；认证只打向对应厂商云服务。
