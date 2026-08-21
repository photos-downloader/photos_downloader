# Photos Downloader

Public website and user guides for [Photos Downloader](https://photos.jqknono.com): unofficial tools that download photos and videos from iCloud, HUAWEI, Xiaomi, vivo, OPPO, and HONOR cloud galleries.

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

Hosted on Alibaba Cloud ESA Pages. Staging is the default publish target; production is bound to `photos.jqknono.com`.

```sh
npm run build
esa-cli commit --name photos-downloader --assets dist --description "docs site" --no-bundle
esa-cli deploy --name photos-downloader --environment staging --no-bundle
```

## License

MIT
