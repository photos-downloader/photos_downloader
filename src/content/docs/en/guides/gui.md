---
title: GUI
description: How the Flutter GUI will select a vendor and start a download. No installer is published yet.
---

The Photos Downloader GUI is a Flutter app that calls vendor downloaders over Rust FFI. **No installer is published yet.**

## Expected flow

1. Open the app and pick a vendor card.
2. Only **iCloud** and **HUAWEI Cloud** are marked ready; the rest are in development.
3. Choose a local download directory.
4. iCloud: enter an Apple ID and complete 2FA. Sessions default to `~/.photos_downloader/icloud/`.
5. HUAWEI: select a browser-exported `cookies.json`.
6. Optional: Copy / Sync / Move, `--recent`, skip videos, dry-run.
7. Start the download and watch progress.

The GUI does not upload passwords or cookies to Photos Downloader servers; authentication goes only to the vendor cloud.
