---
title: 安装说明
description: 二进制发布前的安装预期，以及从源码构建的现状。
---

## 预编译包（即将发布）

1. 从 [下载](/download/) 取对应平台压缩包。
2. 校验校验和（发布说明中提供）。
3. 解压后把可执行文件放到 `PATH`，或在当前目录运行。

Windows 示例：

```powershell
icloud-photos-downloader.exe --help
huawei-photos-downloader.exe --help
```

Unix 示例：

```sh
chmod +x icloud-photos-downloader
./icloud-photos-downloader --help
```

## 从源码构建

厂商 crate 与 Flutter GUI **尚未**在本公开仓库提供。当前无法从本站仓库 `cargo build` 或 `flutter build`。

## 配置文件

- iCloud：工作目录下的 `.env`（不要提交）。详见 [iCloud 指南](/guides/icloud/)。
- 华为：浏览器导出的 `cookies.json`。详见 [HUAWEI 指南](/guides/huawei/)。
- Session 默认目录：`~/.photos_downloader/`（Windows 为 `%USERPROFILE%\.photos_downloader\`）。
