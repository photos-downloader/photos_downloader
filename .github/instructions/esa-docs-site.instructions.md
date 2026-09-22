---
description: "Use when publishing, deploying, renaming, or operating the Photos Downloader docs site on Alibaba Cloud ESA Pages. Covers esa-cli, custom domains, CNAME, hard cutover, photos-downloader.jqknono.com, and production versions."
applyTo:
  - "esa.jsonc"
  - "astro.config.mjs"
  - "README.md"
---

# Docs site ESA pointer

This repository is the public docs site only. Do not copy ESA runbooks here.

- Project name: `photos-downloader`
- Public host: `photos-downloader.jqknono.com`
- Work from this directory (`photos_downloader/`), not the parent workspace root
- Canonical URL lives in `astro.config.mjs` `site` and `package.json` `homepage`
- Deploy and custom-domain steps: jqknono skill `jqknono-esa`, especially `references/pages-custom-domain.md`
- Public DNS (`alidns` CNAME, no `CreateRecord`): `jqknono-aliyun`
- Hard cutover (no 301): change canonical → commit/deploy production → `esa domain add` → read `RecordCname` → add only the new CNAME → verify with public DoH / `--resolve` → then delete the old ESA domain and DNS record
- Local `Resolve-DnsName` to `28.0.3.x` / `fc00::` is Mihomo fake-ip, not a cert failure
- Do not echo `esa_er_token` or treat `*.er.aliyun-esa.net` as the public site
