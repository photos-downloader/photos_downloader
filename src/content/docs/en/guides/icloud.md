---
title: iCloud
description: Authenticate, list, and download iCloud photos with icloud-photos-downloader.
---

`icloud-photos-downloader` is a pure-Rust CLI with semantics aligned to [icloudpd](https://github.com/icloud-photos-downloader/icloud_photos_downloader). Binaries are not published with this site yet.

## Account prerequisites

On iPhone / iPad:

- Enable access to iCloud data on the web
- **Disable** Advanced Data Protection (ADP)

ADP and FIDO are unsupported.

## Authentication

The first login needs an Apple ID password and 2FA (device push or SMS). Sessions are stored under `~/.photos_downloader/icloud/` (`%USERPROFILE%\.photos_downloader\icloud\` on Windows).

```sh
icloud-photos-downloader --auth-only
icloud-photos-downloader --username you@example.com --auth-only
icloud-photos-downloader --mfa-method device --auth-only
icloud-photos-downloader --domain cn --auth-only
```

China accounts use `--domain cn`. Do not use an app-specific password.

## Modes

| Mode | Behavior | Flag |
| --- | --- | --- |
| Download only (default) | Download files that are not already local | none |
| Download and delete from cloud | After a successful download, delete from iCloud (optionally keep recent N days) | `--keep-icloud-recent-days N` |

Always add `--dry-run` before destructive runs.

## Common commands

```sh
icloud-photos-downloader --directory /photos --recent 10
icloud-photos-downloader --list-libraries
icloud-photos-downloader --list-albums
icloud-photos-downloader --album Favorites --directory /photos
icloud-photos-downloader --recent 5 --dry-run --directory ./tmp-icloud --folder-structure none
icloud-photos-downloader --keep-icloud-recent-days 0 --directory /photos --dry-run
icloud-photos-downloader --watch-with-interval 3600 --directory /photos
icloud-photos-downloader --skip-created-before 2020-01-01 --directory /photos
```

The default folder layout is `{:%Y/%m/%d}`. `--folder-structure none` writes a flat directory.

## Config file

Non-secret defaults can live in a working-directory `.env`. CLI flags override environment variables. Never commit `.env`.
