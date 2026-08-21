---
title: Contributing
description: How to improve this public documentation site.
---

The public repository currently accepts **website and user-guide** contributions only.

- Typos, translations, and clearer safety notes: welcome as PRs.
- Do not commit cookies, passwords, sessions, or signed URLs.
- Do not attach prebuilt binaries to this repo.
- Vendor CLI / GUI source is not public yet.

Local preview:

```sh
npm install
npm run dev
npm run build
```

Chinese pages live in `src/content/docs/`. English pages live in `src/content/docs/en/` and must use the same file names.
