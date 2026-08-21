---
title: iCloud
description: 使用 icloud-photos-downloader 认证、列出并下载 iCloud 照片。
---

`icloud-photos-downloader` 是纯 Rust CLI，语义对齐 [icloudpd](https://github.com/icloud-photos-downloader/icloud_photos_downloader)。二进制尚未随本站发布。

## 账号前提

在 iPhone / iPad 上确认：

- 已开启「允许通过网页访问 iCloud 数据」
- **未**开启 Advanced Data Protection（ADP）

ADP 与 FIDO 不受支持。

## 认证

首次登录需要 Apple ID 密码和 2FA（设备推送或短信）。成功后 session 会写到 `~/.photos_downloader/icloud/`（Windows 为 `%USERPROFILE%\.photos_downloader\icloud\`）。

```sh
icloud-photos-downloader --auth-only
icloud-photos-downloader --username you@example.com --auth-only
icloud-photos-downloader --mfa-method device --auth-only
icloud-photos-downloader --domain cn --auth-only
```

中国区账号使用 `--domain cn`。不要使用 app-specific password。

## 三种模式

| 模式 | 行为 | 参数 |
| --- | --- | --- |
| Copy（默认） | 只下载本地没有的文件 | 无额外参数 |
| Sync | 下载后，删除本地已进入「最近删除」的文件 | `--auto-delete` |
| Move | 下载后从 iCloud 删除（可保留最近 N 天） | `--keep-icloud-recent-days N` |

破坏性操作先加 `--dry-run`。

## 常用命令

```sh
icloud-photos-downloader --directory /photos --recent 10
icloud-photos-downloader --list-libraries
icloud-photos-downloader --list-albums
icloud-photos-downloader --album Favorites --directory /photos
icloud-photos-downloader --recent 5 --dry-run --directory ./tmp-icloud --folder-structure none
icloud-photos-downloader --auto-delete --directory /photos --dry-run
icloud-photos-downloader --keep-icloud-recent-days 0 --directory /photos --dry-run
icloud-photos-downloader --watch-with-interval 3600 --directory /photos
icloud-photos-downloader --skip-created-before 2020-01-01 --directory /photos
```

默认目录结构是 `{:%Y/%m/%d}`。`--folder-structure none` 会平铺到目标目录。

## 配置文件

可把非密钥默认值放在工作目录 `.env`。命令行 flag 覆盖环境变量。不要提交 `.env`。
