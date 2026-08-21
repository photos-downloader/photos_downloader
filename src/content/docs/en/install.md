---
title: Install
description: What installation will look like once binaries ship, and why source builds are unavailable here.
---

## Prebuilt packages (coming soon)

1. Grab the archive for your platform from [Download](/en/download/).
2. Check the checksums published with the release.
3. Extract and put the binary on your `PATH`, or run it in place.

Windows:

```powershell
icloud-photos-downloader.exe --help
huawei-photos-downloader.exe --help
```

Unix:

```sh
chmod +x icloud-photos-downloader
./icloud-photos-downloader --help
```

## Build from source

Vendor crates and the Flutter GUI are **not** in this public repository. You cannot `cargo build` or `flutter build` from this site repo today.

## Config

- iCloud: a working-directory `.env` (never commit it). See the [iCloud guide](/en/guides/icloud/).
- HUAWEI: a browser-exported `cookies.json`. See the [HUAWEI guide](/en/guides/huawei/).
- Default session directory: `~/.photos_downloader/` (`%USERPROFILE%\.photos_downloader\` on Windows).
