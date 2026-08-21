---
title: HUAWEI
description: 用浏览器导出的 cookies.json 下载华为云相册。
---

`huawei-photos-downloader` 通过华为云相册网页 API 工作，使用你从已登录浏览器导出的 cookie。二进制尚未随本站发布。

## 导出 cookie

1. 在浏览器登录 [https://cloud.huawei.com](https://cloud.huawei.com)。
2. 打开**图库 / Gallery** 页面。
3. 用 Cookie-Editor 或 EditThisCookie 把 cookie 导出为 JSON。
4. 保存为 `cookies.json`。不要把该文件提交到 Git、issue 或聊天记录。

## 运行

```sh
huawei-photos-downloader --directory /photos --cookie-file cookies.json
huawei-photos-downloader --auth-only --cookie-file cookies.json
huawei-photos-downloader --recent 20 --dry-run --cookie-file cookies.json
```

常用参数：`--recent`、`--until-found`、`--skip-videos`、`--skip-photos`、`--filename-pattern`、`--watch-interval`、`--concurrency`。

Cookie 过期后重新导出即可，不要把可复用的 cookie 值贴到公开渠道。
