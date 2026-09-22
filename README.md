# Photos Downloader

Public website and user guides for [Photos Downloader](https://photos-downloader.jqknono.com): unofficial tools that download photos and videos from iCloud, HUAWEI, Xiaomi, vivo, OPPO, and HONOR cloud galleries.

This repository does **not** currently publish CLI/GUI source or release binaries. Download pages are placeholders until GitHub Releases are available.

## Local development

```sh
npm install
npm run dev
```

Production build:

```sh
npm run build
```

The static site is written to `dist/`.

## Locales

- Chinese (default): `/`
- English: `/en/`

## Deploy

Hosted on Alibaba Cloud ESA Pages. Public site: [https://photos-downloader.jqknono.com](https://photos-downloader.jqknono.com). Staging remains available for preview; production currently serves version `1787580081861957043`.

```sh
npm run build
esa-cli commit --name photos-downloader --assets dist --description "docs site" --no-bundle
esa-cli deploy --name photos-downloader --environment staging --no-bundle
esa-cli deploy --name photos-downloader --environment production --version <version>
esa-cli domain add photos-downloader.jqknono.com
```

Public DNS for `photos-downloader.jqknono.com` is a CNAME to the ESA record `photos-downloader.jqknono.com.a1.initbb.com`. Custom-domain cutover and DNS verification follow the jqknono ESA Pages runbook; this README does not duplicate it.

## License

MIT
