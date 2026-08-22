---
title: Status
description: Vendor implementation progress and what comes after the documentation site.
---

## Now

- The documentation site is public: this repository.
- iCloud CLI: authentication, listing, download-only, and download-and-delete-cloud flags.
- HUAWEI CLI: cloud album download from browser cookies.
- Xiaomi / vivo / OPPO: scaffolds only.
- HONOR: accepts cookies but sends no live requests until the Gallery API is verified.
- GUI: Flutter + Rust FFI exists privately; no installer is published.

## Next

1. Publish Windows / Linux / macOS (x64 + arm64) binaries for ready CLIs.
2. Wire this site's download page to GitHub Releases.
3. Finish remaining vendor protocols before documenting them as ready.
4. Open-source crates and the GUI when appropriate.

## Out of scope

- iCloud Advanced Data Protection (ADP) and FIDO.
- Storing passwords, cookies, sessions, or signed URLs in the repo or issues.
- Treating the Flutter web debug server as the public website.
