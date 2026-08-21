---
title: HUAWEI
description: Download HUAWEI Cloud Gallery using a browser-exported cookies.json.
---

`huawei-photos-downloader` talks to the HUAWEI Cloud Gallery web API with cookies exported from a logged-in browser. Binaries are not published with this site yet.

## Export cookies

1. Sign in at [https://cloud.huawei.com](https://cloud.huawei.com).
2. Open the **Gallery** page.
3. Export cookies as JSON (Cookie-Editor or EditThisCookie).
4. Save as `cookies.json`. Do not commit that file to Git, issues, or chat logs.

## Run

```sh
huawei-photos-downloader --directory /photos --cookie-file cookies.json
huawei-photos-downloader --auth-only --cookie-file cookies.json
huawei-photos-downloader --recent 20 --dry-run --cookie-file cookies.json
```

Useful flags: `--recent`, `--until-found`, `--skip-videos`, `--skip-photos`, `--filename-pattern`, `--watch-interval`, `--concurrency`.

When cookies expire, export a fresh file. Never paste reusable cookie values in public channels.
