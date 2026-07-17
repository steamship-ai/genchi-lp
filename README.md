# ゲンチ LP

自治体ごとに独立した、画像とテキストのみで構成する静的LPです。GitHub Pagesで公開します。

## ページを追加する

`docs/` 配下に自治体ごとのフォルダを追加し、その中にページで使うものをすべて置きます。

```text
docs/<municipality-slug>/
├── index.html
├── styles.css
└── assets/
    └── ...
```

たとえば `docs/sample-city/` は `https://steamship-ai.github.io/genchi-lp/sample-city/` で公開されます。全体のトップページは設けません。

## 公開

GitHubの `steamship-ai/genchi-lp` で **Settings → Pages** を開き、`main` ブランチの `/docs` を公開元に設定します。
